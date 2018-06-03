---
swagger: "2.0"
info:
  title: Paylocity
  description: 'For general questions and support of the API, contact: vendorrelations@paylocity.com#
    OverviewPaylocity Web Services API is an externally facing RESTful Internet protocol.
    The Paylocity API uses HTTP verbs and a RESTful endpoint structure. OAuth 2.0
    is used as the API Authorization framework. Request and response payloads are
    formatted as JSON.Paylocity supports v1 and v2 versions of its API endpoints.
    v1, while supported, won''t be enhanced with additional functionality. For direct
    link to v1 documentation, please click [here](https://docs.paylocity.com/weblink/guides/Paylocity_Web_Services_API/v1/Paylocity_Web_Services_API.htm).
    For additional resources regarding v1/v2 differences and conversion path, please
    contact vendorrelations@paylocity.com.##### SetupPaylocity will provide the secure
    client credentials and set up the scope (type of requests and allowed company
    numbers). You will receive the unique client id, secret, and Paylocity public
    key for the data encryption. The secret will expire in 365 days. * Paylocity will
    send you an e-mail 10 days prior to the expiration date for the current secret.
    If not renewed, the second e-mail notification will be sent 5 days prior to secret''s
    expiration. Each email will contain the code necessary to renew the client secret.
    * You can obtain the new secret by calling API endpoint using your current not
    yet expired credentials and the code that was sent with the notification email.
    For details on API endpoint, please see Client Credentials section. * Both the
    current secret value and the new secret value will be recognized during the transition
    period. After the current secret expires, you must use the new secret. * If you
    were unable to renew the secret via API endpoint, you can still contact Service
    and they will email you new secret via secure email.When validating the request,
    Paylocity API will honor the defaults and required fields set up for the company
    default New Hire Template as defined in Web Pay.# AuthorizationPaylocity Web Services
    API uses OAuth2.0 Authentication with JSON Message Format.All requests of the
    Paylocity Web Services API require a bearer token which can be obtained by authenticating
    the client with the Paylocity Web Services API via OAuth 2.0.The client must request
    a bearer token from the authorization endpoint:auth-server for production: https://api.paylocity.com/IdentityServer/connect/tokenauth-server
    for testing: https://apisandbox.paylocity.com/IdentityServer/connect/token#####
    Authorization HeaderThe request is expected to be in the form of a basic authentication
    request, with the &quot;Authorization&quot; header containing the client-id and
    client-secret. This means the standard base-64 encoded user:password, prefixed
    with &quot;Basic&quot; as the value for the Authorization header, where user is
    the client-id and password is the client-secret.##### Content-Type HeaderThe &quot;Content-Type&quot;
    header is required to be &quot;application/x-www-form-urlencoded&quot;.##### Additional
    ValuesThe request must post the following form encoded values within the request
    body:    grant_type = client_credentials    scope = WebLinkAPI##### ResponsesSuccess
    will return HTTP 200 OK with JSON content:    {      &quot;access_token&quot;:
    &quot;xxx&quot;,      &quot;expires_in&quot;: 3600,      &quot;token_type&quot;:
    &quot;Bearer&quot;    }# EncryptionPaylocity uses a combination of RSA and AES
    cryptography. As part of the setup, each client is issued a public RSA key.Paylocity
    recommends the encryption of the incoming requests as additional protection of
    the sensitive data. Clients can opt-out of the encryption during the initial setup
    process. Opt-out will allow Paylocity to process un-encrypted requests.The Paylocity
    Public Key has the following properties:* 2048 bit key size* PKCS1 key format*
    PEM encoding##### Properties* key (base 64 encoded): The AES symmetric key encrypted
    with the Paylocity Public Key. It is the key used to encrypt the content. Paylocity
    will decrypt the AES key using RSA decryption and use it to decrypt the content.*
    iv (base 64 encoded): The AES IV (Initialization Vector) used when encrypting
    the content.* content (base 64 encoded): The AES encrypted request. The key and
    iv provided in the secureContent request are used by Paylocity for decryption
    of the content.We suggest using the following for the AES:* CBC cipher mode* PKCS7
    padding* 128 bit block size* 256 bit key size##### Sample Example    {      &quot;secureContent&quot;:
    {        &quot;key&quot;: &quot;eS3aw6H/qzHMJ00gSi6gQ3xa08DPMazk8BFY96Pd99ODA==&quot;,        &quot;iv&quot;:
    &quot;NLyXMGq9svw0XO5aI9BzWw==&quot;,        &quot;content&quot;: &quot;gAEOiQltO1w+LzGUoIK8FiYbU42hug94EasSl7N+Q1w=&quot;      }    }#####
    Sample C# Code    using Newtonsoft.Json;    using System;    using System.IO;    using
    System.Security.Cryptography;    using System.Text;    public class SecuredContent    {      [JsonProperty(&quot;key&quot;)]      public
    string Key { get; set; }      [JsonProperty(&quot;iv&quot;)]      public string
    Iv { get; set; }      [JsonProperty(&quot;content&quot;)]      public string Content
    { get; set; }    }    public class EndUserSecureRequestExample    {      public
    string CreateSecuredRequest(FileInfo paylocityPublicKey, string unsecuredJsonRequest)      {        string
    publicKeyXml = File.ReadAllText(paylocityPublicKey.FullName, Encoding.UTF8);        SecuredContent
    secureContent = this.CreateSecuredContent(publicKeyXml, unsecuredJsonRequest);        string
    secureRequest = JsonConvert.SerializeObject(new { secureContent });        return
    secureRequest;      }      private SecuredContent CreateSecuredContent(string
    publicKeyXml, string request)      {        using (AesCryptoServiceProvider aesCsp
    = new AesCryptoServiceProvider())        {          aesCsp.Mode = CipherMode.CBC;          aesCsp.Padding
    = PaddingMode.PKCS7;          aesCsp.BlockSize = 128;          aesCsp.KeySize
    = 256;          using (ICryptoTransform crt = aesCsp.CreateEncryptor(aesCsp.Key,
    aesCsp.IV))          {            using (MemoryStream outputStream = new MemoryStream())            {              using
    (CryptoStream encryptStream = new CryptoStream(outputStream, crt, CryptoStreamMode.Write))              {                byte[]
    encodedRequest = Encoding.UTF8.GetBytes(request);                encryptStream.Write(encodedRequest,
    0, encodedRequest.Length);                encryptStream.FlushFinalBlock();                byte[]
    encryptedRequest = outputStream.ToArray();                using (RSACryptoServiceProvider
    crp = new RSACryptoServiceProvider())                {                  crp.FromXmlstring(publicKeyXml);                  byte[]
    encryptedKey = crp.Encrypt(aesCsp.Key, false);                  return new SecuredContent()                  {                    Key
    = Convert.ToBase64string(encryptedKey),                    Iv = Convert.ToBase64string(aesCsp.IV),                    Content
    = Convert.ToBase64string(encryptedRequest)                  };                }              }            }          }        }      }    }##
    SupportQuestions about using the Paylocity API? Please contact vendorrelations@paylocity.com.#
    Deductions (v1)Deductions API provides endpoints to retrieve, add, update and
    delete deductions for a company''s employees. For schema details, click &lt;a
    href=&quot;https://docs.paylocity.com/weblink/guides/Paylocity_Web_Services_API/v1/Paylocity_Web_Services_API.htm&quot;
    target=&quot;_blank&quot;&gt;here&lt;/a&gt;.# OnBoarding (v1)Onboarding API sends
    employee data into Paylocity Onboarding to help ensure an easy and accurate hiring
    process for subsequent completion into Web Pay. For schema details, click &lt;a
    href=&quot;https://docs.paylocity.com/weblink/guides/Paylocity_Web_Services_API/v1/Paylocity_Web_Services_API.htm&quot;
    target=&quot;_blank&quot;&gt;here&lt;/a&gt;.'
  termsOfService: WebLink.OpenApiDoc.TermsOfService
  version: "2"
host: api.paylocity.com
basePath: /api
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /v2/companies/{companyId}/employees/{employeeId}/earnings/{earningCode}:
    get:
      summary: Get Earnings by Earning Code
      description: Get Earnings returns all earnings with the provided earning code
        for the selected employee
      operationId: v2.companies.companyId.employees.employeeId.earnings.earningCode.get
      parameters:
      - in: header
        name: Authorization
        description: Bearer + JWT
      - in: path
        name: companyId
        description: Company Id
      - in: path
        name: earningCode
        description: Earning Code
      - in: path
        name: employeeId
        description: Employee Id
      responses:
        200:
          description: OK
      tags:
      - v2
      - companies
      - companyid
      - employees
      - employeeid
      - earnings
      - earningcode
definitions:
  addClientSecret:
    properties:
      code:
        description: This is a default description.
        type: post
  benefitSetup:
    properties:
      benefitClass:
        description: This is a default description.
        type: post
      benefitClassEffectiveDate:
        description: This is a default description.
        type: post
      benefitSalary:
        description: This is a default description.
        type: post
      benefitSalaryEffectiveDate:
        description: This is a default description.
        type: post
      doNotApplyAdministrativePeriod:
        description: This is a default description.
        type: post
      isMeasureAcaEligibility:
        description: This is a default description.
        type: post
  customFieldDefinition:
    properties:
      category:
        description: This is a default description.
        type: post
      defaultValue:
        description: This is a default description.
        type: post
      isRequired:
        description: This is a default description.
        type: post
      label:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
      values:
        description: This is a default description.
        type: post
  earning:
    properties:
      agency:
        description: This is a default description.
        type: post
      amount:
        description: This is a default description.
        type: post
      annualMaximum:
        description: This is a default description.
        type: post
      calculationCode:
        description: This is a default description.
        type: post
      costCenter1:
        description: This is a default description.
        type: post
      costCenter2:
        description: This is a default description.
        type: post
      costCenter3:
        description: This is a default description.
        type: post
      earningCode:
        description: This is a default description.
        type: post
      effectiveDate:
        description: This is a default description.
        type: post
      endDate:
        description: This is a default description.
        type: post
  employee:
    properties:
      additionalDirectDeposit:
        description: This is a default description.
        type: post
      benefitSetup:
        description: This is a default description.
        type: post
      birthDate:
        description: This is a default description.
        type: post
      companyName:
        description: This is a default description.
        type: post
      customBooleanFields:
        description: This is a default description.
        type: post
      customDateFields:
        description: This is a default description.
        type: post
      customDropDownFields:
        description: This is a default description.
        type: post
      customNumberFields:
        description: This is a default description.
        type: post
      customTextFields:
        description: This is a default description.
        type: post
      departmentPosition:
        description: This is a default description.
        type: post
  employeeIdResponse:
    properties:
      employeeId:
        description: This is a default description.
        type: post
  error:
    properties:
      field:
        description: This is a default description.
        type: post
      message:
        description: This is a default description.
        type: post
      options:
        description: This is a default description.
        type: post
      path:
        description: This is a default description.
        type: post
  localTax:
    properties:
      exemptions:
        description: This is a default description.
        type: post
      exemptions2:
        description: This is a default description.
        type: post
      filingStatus:
        description: This is a default description.
        type: post
      residentPSD:
        description: This is a default description.
        type: post
      taxCode:
        description: This is a default description.
        type: post
      workPSD:
        description: This is a default description.
        type: post
  nonPrimaryStateTax:
    properties:
      amount:
        description: This is a default description.
        type: post
      exemptions:
        description: This is a default description.
        type: post
      exemptions2:
        description: This is a default description.
        type: post
      filingStatus:
        description: This is a default description.
        type: post
      percentage:
        description: This is a default description.
        type: post
      reciprocityCode:
        description: This is a default description.
        type: post
      specialCheckCalc:
        description: This is a default description.
        type: post
      taxCalculationCode:
        description: This is a default description.
        type: post
      taxCode:
        description: This is a default description.
        type: post
  stagedEmployee:
    properties:
      additionalDirectDeposit:
        description: This is a default description.
        type: post
      benefitSetup:
        description: This is a default description.
        type: post
      birthDate:
        description: This is a default description.
        type: post
      customBooleanFields:
        description: This is a default description.
        type: post
      customDateFields:
        description: This is a default description.
        type: post
      customDropDownFields:
        description: This is a default description.
        type: post
      customNumberFields:
        description: This is a default description.
        type: post
      customTextFields:
        description: This is a default description.
        type: post
      departmentPosition:
        description: This is a default description.
        type: post
      disabilityDescription:
        description: This is a default description.
        type: post
  stateTax:
    properties:
      amount:
        description: This is a default description.
        type: post
      exemptions:
        description: This is a default description.
        type: post
      exemptions2:
        description: This is a default description.
        type: post
      filingStatus:
        description: This is a default description.
        type: post
      percentage:
        description: This is a default description.
        type: post
      specialCheckCalc:
        description: This is a default description.
        type: post
      taxCalculationCode:
        description: This is a default description.
        type: post
      taxCode:
        description: This is a default description.
        type: post
  trackingNumberResponse:
    properties:
      trackingNumber:
        description: This is a default description.
        type: post
x-collection-name: Paylocity
x-streamrank:
  polling_total_time_average: "0"
  polling_size_download_average: "0"
  streaming_total_time_average: "0"
  streaming_size_download_average: "0"
  change_yes: "0"
  change_no: "0"
  time_percentage: "0"
  size_percentage: "0"
  change_percentage: "200"
  last_run: ~
  days_run: "0"
  minute_run: "0"
---