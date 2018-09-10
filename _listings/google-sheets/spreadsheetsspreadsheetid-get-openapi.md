---
swagger: "2.0"
info:
  title: Google Sheets
  description: Reads and writes Google Sheets.
  termsOfService: https://developers.google.com/terms/
  contact:
    name: Google
    url: https://google.com
  version: v4
host: sheets.googleapis.com
basePath: v4/
schemes:
- http
produces:
- application/json
consumes:
- application/json
paths:
  /spreadsheets/{spreadsheetId}:
    get:
      summary: Get Spreadsheet
      description: Returns the spreadsheet at the given ID
      operationId: sheets.spreadsheets.get
      x-api-path-slug: spreadsheetsspreadsheetid-get
      parameters:
      - in: query
        name: includeGridData
        description: True if grid data should be returned
      - in: query
        name: ranges
        description: The ranges to retrieve from the spreadsheet
      - in: path
        name: spreadsheetId
        description: The spreadsheet to request
      responses:
        200:
          description: OK
      tags:
      - spreadsheet
definitions:
  AddBandingRequest:
    properties: []
  AddBandingResponse:
    properties: []
  AddChartRequest:
    properties: []
  AddChartResponse:
    properties: []
  AddConditionalFormatRuleRequest:
    properties:
      index:
        description: This is a default description.
        type: post
  AddFilterViewRequest:
    properties: []
  AddFilterViewResponse:
    properties: []
  AddNamedRangeRequest:
    properties: []
  AddNamedRangeResponse:
    properties: []
  AddProtectedRangeRequest:
    properties: []
  AddProtectedRangeResponse:
    properties: []
  AddSheetRequest:
    properties: []
  AddSheetResponse:
    properties: []
  AppendCellsRequest:
    properties:
      fields:
        description: This is a default description.
        type: post
      rows:
        description: This is a default description.
        type: post
      sheetId:
        description: This is a default description.
        type: post
  AppendDimensionRequest:
    properties:
      dimension:
        description: This is a default description.
        type: post
      length:
        description: This is a default description.
        type: post
      sheetId:
        description: This is a default description.
        type: post
  AppendValuesResponse:
    properties:
      spreadsheetId:
        description: This is a default description.
        type: post
      tableRange:
        description: This is a default description.
        type: post
  AutoFillRequest:
    properties:
      useAlternateSeries:
        description: This is a default description.
        type: post
  AutoResizeDimensionsRequest:
    properties: []
  BandedRange:
    properties:
      bandedRangeId:
        description: This is a default description.
        type: post
  BandingProperties:
    properties: []
  BasicChartAxis:
    properties:
      position:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
  BasicChartDomain:
    properties:
      reversed:
        description: This is a default description.
        type: post
  BasicChartSeries:
    properties:
      targetAxis:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  BasicChartSpec:
    properties:
      axis:
        description: This is a default description.
        type: post
      chartType:
        description: This is a default description.
        type: post
      domains:
        description: This is a default description.
        type: post
      headerCount:
        description: This is a default description.
        type: post
      legendPosition:
        description: This is a default description.
        type: post
      series:
        description: This is a default description.
        type: post
      compareMode:
        description: This is a default description.
        type: post
      interpolateNulls:
        description: This is a default description.
        type: post
      lineSmoothing:
        description: This is a default description.
        type: post
      stackedType:
        description: This is a default description.
        type: post
  BasicFilter:
    properties:
      criteria:
        description: This is a default description.
        type: post
      sortSpecs:
        description: This is a default description.
        type: post
  BatchClearValuesRequest:
    properties:
      ranges:
        description: This is a default description.
        type: post
  BatchClearValuesResponse:
    properties:
      clearedRanges:
        description: This is a default description.
        type: post
      spreadsheetId:
        description: This is a default description.
        type: post
  BatchGetValuesResponse:
    properties:
      spreadsheetId:
        description: This is a default description.
        type: post
      valueRanges:
        description: This is a default description.
        type: post
  BatchUpdateSpreadsheetRequest:
    properties:
      includeSpreadsheetInResponse:
        description: This is a default description.
        type: post
      requests:
        description: This is a default description.
        type: post
      responseIncludeGridData:
        description: This is a default description.
        type: post
      responseRanges:
        description: This is a default description.
        type: post
  BatchUpdateSpreadsheetResponse:
    properties:
      replies:
        description: This is a default description.
        type: post
      spreadsheetId:
        description: This is a default description.
        type: post
  BatchUpdateValuesRequest:
    properties:
      data:
        description: This is a default description.
        type: post
      includeValuesInResponse:
        description: This is a default description.
        type: post
      responseDateTimeRenderOption:
        description: This is a default description.
        type: post
      responseValueRenderOption:
        description: This is a default description.
        type: post
      valueInputOption:
        description: This is a default description.
        type: post
  BatchUpdateValuesResponse:
    properties:
      responses:
        description: This is a default description.
        type: post
      spreadsheetId:
        description: This is a default description.
        type: post
      totalUpdatedCells:
        description: This is a default description.
        type: post
      totalUpdatedColumns:
        description: This is a default description.
        type: post
      totalUpdatedRows:
        description: This is a default description.
        type: post
      totalUpdatedSheets:
        description: This is a default description.
        type: post
  BooleanCondition:
    properties:
      type:
        description: This is a default description.
        type: post
      values:
        description: This is a default description.
        type: post
  BooleanRule:
    properties: []
  Border:
    properties:
      style:
        description: This is a default description.
        type: post
      width:
        description: This is a default description.
        type: post
  Borders:
    properties: []
  CellData:
    properties:
      formattedValue:
        description: This is a default description.
        type: post
      hyperlink:
        description: This is a default description.
        type: post
      note:
        description: This is a default description.
        type: post
      textFormatRuns:
        description: This is a default description.
        type: post
  CellFormat:
    properties:
      horizontalAlignment:
        description: This is a default description.
        type: post
      hyperlinkDisplayType:
        description: This is a default description.
        type: post
      textDirection:
        description: This is a default description.
        type: post
      verticalAlignment:
        description: This is a default description.
        type: post
      wrapStrategy:
        description: This is a default description.
        type: post
  ChartData:
    properties: []
  ChartSourceRange:
    properties:
      sources:
        description: This is a default description.
        type: post
  ChartSpec:
    properties:
      hiddenDimensionStrategy:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
      altText:
        description: This is a default description.
        type: post
      fontName:
        description: This is a default description.
        type: post
      maximized:
        description: This is a default description.
        type: post
      subtitle:
        description: This is a default description.
        type: post
  ClearBasicFilterRequest:
    properties:
      sheetId:
        description: This is a default description.
        type: post
  ClearValuesRequest:
    properties: []
  ClearValuesResponse:
    properties:
      clearedRange:
        description: This is a default description.
        type: post
      spreadsheetId:
        description: This is a default description.
        type: post
  Color:
    properties:
      alpha:
        description: This is a default description.
        type: post
      blue:
        description: This is a default description.
        type: post
      green:
        description: This is a default description.
        type: post
      red:
        description: This is a default description.
        type: post
  ConditionValue:
    properties:
      relativeDate:
        description: This is a default description.
        type: post
      userEnteredValue:
        description: This is a default description.
        type: post
  ConditionalFormatRule:
    properties:
      ranges:
        description: This is a default description.
        type: post
  CopyPasteRequest:
    properties:
      pasteOrientation:
        description: This is a default description.
        type: post
      pasteType:
        description: This is a default description.
        type: post
  CopySheetToAnotherSpreadsheetRequest:
    properties:
      destinationSpreadsheetId:
        description: This is a default description.
        type: post
  CutPasteRequest:
    properties:
      pasteType:
        description: This is a default description.
        type: post
  DataValidationRule:
    properties:
      inputMessage:
        description: This is a default description.
        type: post
      showCustomUi:
        description: This is a default description.
        type: post
      strict:
        description: This is a default description.
        type: post
  DeleteBandingRequest:
    properties:
      bandedRangeId:
        description: This is a default description.
        type: post
  DeleteConditionalFormatRuleRequest:
    properties:
      index:
        description: This is a default description.
        type: post
      sheetId:
        description: This is a default description.
        type: post
  DeleteConditionalFormatRuleResponse:
    properties: []
  DeleteDimensionRequest:
    properties: []
  DeleteEmbeddedObjectRequest:
    properties:
      objectId:
        description: This is a default description.
        type: post
  DeleteFilterViewRequest:
    properties:
      filterId:
        description: This is a default description.
        type: post
  DeleteNamedRangeRequest:
    properties:
      namedRangeId:
        description: This is a default description.
        type: post
  DeleteProtectedRangeRequest:
    properties:
      protectedRangeId:
        description: This is a default description.
        type: post
  DeleteRangeRequest:
    properties:
      shiftDimension:
        description: This is a default description.
        type: post
  DeleteSheetRequest:
    properties:
      sheetId:
        description: This is a default description.
        type: post
  DimensionProperties:
    properties:
      hiddenByFilter:
        description: This is a default description.
        type: post
      hiddenByUser:
        description: This is a default description.
        type: post
      pixelSize:
        description: This is a default description.
        type: post
      developerMetadata:
        description: This is a default description.
        type: post
  DimensionRange:
    properties:
      dimension:
        description: This is a default description.
        type: post
      endIndex:
        description: This is a default description.
        type: post
      sheetId:
        description: This is a default description.
        type: post
      startIndex:
        description: This is a default description.
        type: post
  DuplicateFilterViewRequest:
    properties:
      filterId:
        description: This is a default description.
        type: post
  DuplicateFilterViewResponse:
    properties: []
  DuplicateSheetRequest:
    properties:
      insertSheetIndex:
        description: This is a default description.
        type: post
      newSheetId:
        description: This is a default description.
        type: post
      newSheetName:
        description: This is a default description.
        type: post
      sourceSheetId:
        description: This is a default description.
        type: post
  DuplicateSheetResponse:
    properties: []
  Editors:
    properties:
      domainUsersCanEdit:
        description: This is a default description.
        type: post
      groups:
        description: This is a default description.
        type: post
      users:
        description: This is a default description.
        type: post
  EmbeddedChart:
    properties:
      chartId:
        description: This is a default description.
        type: post
  EmbeddedObjectPosition:
    properties:
      newSheet:
        description: This is a default description.
        type: post
      sheetId:
        description: This is a default description.
        type: post
  ErrorValue:
    properties:
      message:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  ExtendedValue:
    properties:
      boolValue:
        description: This is a default description.
        type: post
      formulaValue:
        description: This is a default description.
        type: post
      numberValue:
        description: This is a default description.
        type: post
      stringValue:
        description: This is a default description.
        type: post
  FilterCriteria:
    properties:
      hiddenValues:
        description: This is a default description.
        type: post
  FilterView:
    properties:
      criteria:
        description: This is a default description.
        type: post
      filterViewId:
        description: This is a default description.
        type: post
      namedRangeId:
        description: This is a default description.
        type: post
      sortSpecs:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
  FindReplaceRequest:
    properties:
      allSheets:
        description: This is a default description.
        type: post
      find:
        description: This is a default description.
        type: post
      includeFormulas:
        description: This is a default description.
        type: post
      matchCase:
        description: This is a default description.
        type: post
      matchEntireCell:
        description: This is a default description.
        type: post
      replacement:
        description: This is a default description.
        type: post
      searchByRegex:
        description: This is a default description.
        type: post
      sheetId:
        description: This is a default description.
        type: post
  FindReplaceResponse:
    properties:
      formulasChanged:
        description: This is a default description.
        type: post
      occurrencesChanged:
        description: This is a default description.
        type: post
      rowsChanged:
        description: This is a default description.
        type: post
      sheetsChanged:
        description: This is a default description.
        type: post
      valuesChanged:
        description: This is a default description.
        type: post
  GradientRule:
    properties: []
  GridCoordinate:
    properties:
      columnIndex:
        description: This is a default description.
        type: post
      rowIndex:
        description: This is a default description.
        type: post
      sheetId:
        description: This is a default description.
        type: post
  GridData:
    properties:
      columnMetadata:
        description: This is a default description.
        type: post
      rowData:
        description: This is a default description.
        type: post
      rowMetadata:
        description: This is a default description.
        type: post
      startColumn:
        description: This is a default description.
        type: post
      startRow:
        description: This is a default description.
        type: post
  GridProperties:
    properties:
      columnCount:
        description: This is a default description.
        type: post
      frozenColumnCount:
        description: This is a default description.
        type: post
      frozenRowCount:
        description: This is a default description.
        type: post
      hideGridlines:
        description: This is a default description.
        type: post
      rowCount:
        description: This is a default description.
        type: post
  GridRange:
    properties:
      endColumnIndex:
        description: This is a default description.
        type: post
      endRowIndex:
        description: This is a default description.
        type: post
      sheetId:
        description: This is a default description.
        type: post
      startColumnIndex:
        description: This is a default description.
        type: post
      startRowIndex:
        description: This is a default description.
        type: post
  InsertDimensionRequest:
    properties:
      inheritFromBefore:
        description: This is a default description.
        type: post
  InsertRangeRequest:
    properties:
      shiftDimension:
        description: This is a default description.
        type: post
  InterpolationPoint:
    properties:
      type:
        description: This is a default description.
        type: post
      value:
        description: This is a default description.
        type: post
  IterativeCalculationSettings:
    properties:
      convergenceThreshold:
        description: This is a default description.
        type: post
      maxIterations:
        description: This is a default description.
        type: post
  MergeCellsRequest:
    properties:
      mergeType:
        description: This is a default description.
        type: post
  MoveDimensionRequest:
    properties:
      destinationIndex:
        description: This is a default description.
        type: post
  NamedRange:
    properties:
      name:
        description: This is a default description.
        type: post
      namedRangeId:
        description: This is a default description.
        type: post
  NumberFormat:
    properties:
      pattern:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  OverlayPosition:
    properties:
      heightPixels:
        description: This is a default description.
        type: post
      offsetXPixels:
        description: This is a default description.
        type: post
      offsetYPixels:
        description: This is a default description.
        type: post
      widthPixels:
        description: This is a default description.
        type: post
  Padding:
    properties:
      bottom:
        description: This is a default description.
        type: post
      left:
        description: This is a default description.
        type: post
      right:
        description: This is a default description.
        type: post
      top:
        description: This is a default description.
        type: post
  PasteDataRequest:
    properties:
      data:
        description: This is a default description.
        type: post
      delimiter:
        description: This is a default description.
        type: post
      html:
        description: This is a default description.
        type: post
      type:
        description: This is a default description.
        type: post
  PieChartSpec:
    properties:
      legendPosition:
        description: This is a default description.
        type: post
      pieHole:
        description: This is a default description.
        type: post
      threeDimensional:
        description: This is a default description.
        type: post
  PivotFilterCriteria:
    properties:
      visibleValues:
        description: This is a default description.
        type: post
  PivotGroup:
    properties:
      showTotals:
        description: This is a default description.
        type: post
      sortOrder:
        description: This is a default description.
        type: post
      sourceColumnOffset:
        description: This is a default description.
        type: post
      valueMetadata:
        description: This is a default description.
        type: post
      label:
        description: This is a default description.
        type: post
      repeatHeadings:
        description: This is a default description.
        type: post
  PivotGroupSortValueBucket:
    properties:
      buckets:
        description: This is a default description.
        type: post
      valuesIndex:
        description: This is a default description.
        type: post
  PivotGroupValueMetadata:
    properties:
      collapsed:
        description: This is a default description.
        type: post
  PivotTable:
    properties:
      columns:
        description: This is a default description.
        type: post
      criteria:
        description: This is a default description.
        type: post
      rows:
        description: This is a default description.
        type: post
      valueLayout:
        description: This is a default description.
        type: post
      values:
        description: This is a default description.
        type: post
  PivotValue:
    properties:
      formula:
        description: This is a default description.
        type: post
      name:
        description: This is a default description.
        type: post
      sourceColumnOffset:
        description: This is a default description.
        type: post
      summarizeFunction:
        description: This is a default description.
        type: post
      calculatedDisplayType:
        description: This is a default description.
        type: post
  ProtectedRange:
    properties:
      description:
        description: This is a default description.
        type: post
      namedRangeId:
        description: This is a default description.
        type: post
      protectedRangeId:
        description: This is a default description.
        type: post
      requestingUserCanEdit:
        description: This is a default description.
        type: post
      unprotectedRanges:
        description: This is a default description.
        type: post
      warningOnly:
        description: This is a default description.
        type: post
  RepeatCellRequest:
    properties:
      fields:
        description: This is a default description.
        type: post
  Request:
    properties: []
  Response:
    properties: []
  RowData:
    properties:
      values:
        description: This is a default description.
        type: post
  SetBasicFilterRequest:
    properties: []
  SetDataValidationRequest:
    properties: []
  Sheet:
    properties:
      bandedRanges:
        description: This is a default description.
        type: post
      charts:
        description: This is a default description.
        type: post
      conditionalFormats:
        description: This is a default description.
        type: post
      data:
        description: This is a default description.
        type: post
      filterViews:
        description: This is a default description.
        type: post
      merges:
        description: This is a default description.
        type: post
      protectedRanges:
        description: This is a default description.
        type: post
      developerMetadata:
        description: This is a default description.
        type: post
  SheetProperties:
    properties:
      hidden:
        description: This is a default description.
        type: post
      index:
        description: This is a default description.
        type: post
      rightToLeft:
        description: This is a default description.
        type: post
      sheetId:
        description: This is a default description.
        type: post
      sheetType:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
  SortRangeRequest:
    properties:
      sortSpecs:
        description: This is a default description.
        type: post
  SortSpec:
    properties:
      dimensionIndex:
        description: This is a default description.
        type: post
      sortOrder:
        description: This is a default description.
        type: post
  SourceAndDestination:
    properties:
      dimension:
        description: This is a default description.
        type: post
      fillLength:
        description: This is a default description.
        type: post
  Spreadsheet:
    properties:
      namedRanges:
        description: This is a default description.
        type: post
      sheets:
        description: This is a default description.
        type: post
      spreadsheetId:
        description: This is a default description.
        type: post
      spreadsheetUrl:
        description: This is a default description.
        type: post
      developerMetadata:
        description: This is a default description.
        type: post
  SpreadsheetProperties:
    properties:
      autoRecalc:
        description: This is a default description.
        type: post
      locale:
        description: This is a default description.
        type: post
      timeZone:
        description: This is a default description.
        type: post
      title:
        description: This is a default description.
        type: post
  TextFormat:
    properties:
      bold:
        description: This is a default description.
        type: post
      fontFamily:
        description: This is a default description.
        type: post
      fontSize:
        description: This is a default description.
        type: post
      italic:
        description: This is a default description.
        type: post
      strikethrough:
        description: This is a default description.
        type: post
      underline:
        description: This is a default description.
        type: post
  TextFormatRun:
    properties:
      startIndex:
        description: This is a default description.
        type: post
  TextRotation:
    properties:
      angle:
        description: This is a default description.
        type: post
      vertical:
        description: This is a default description.
        type: post
  TextToColumnsRequest:
    properties:
      delimiter:
        description: This is a default description.
        type: post
      delimiterType:
        description: This is a default description.
        type: post
  UnmergeCellsRequest:
    properties: []
  UpdateBandingRequest:
    properties:
      fields:
        description: This is a default description.
        type: post
  UpdateBordersRequest:
    properties: []
  UpdateCellsRequest:
    properties:
      fields:
        description: This is a default description.
        type: post
      rows:
        description: This is a default description.
        type: post
  UpdateChartSpecRequest:
    properties:
      chartId:
        description: This is a default description.
        type: post
  UpdateConditionalFormatRuleRequest:
    properties:
      index:
        description: This is a default description.
        type: post
      newIndex:
        description: This is a default description.
        type: post
      sheetId:
        description: This is a default description.
        type: post
  UpdateConditionalFormatRuleResponse:
    properties:
      newIndex:
        description: This is a default description.
        type: post
      oldIndex:
        description: This is a default description.
        type: post
  UpdateDimensionPropertiesRequest:
    properties:
      fields:
        description: This is a default description.
        type: post
  UpdateEmbeddedObjectPositionRequest:
    properties:
      fields:
        description: This is a default description.
        type: post
      objectId:
        description: This is a default description.
        type: post
  UpdateEmbeddedObjectPositionResponse:
    properties: []
  UpdateFilterViewRequest:
    properties:
      fields:
        description: This is a default description.
        type: post
  UpdateNamedRangeRequest:
    properties:
      fields:
        description: This is a default description.
        type: post
  UpdateProtectedRangeRequest:
    properties:
      fields:
        description: This is a default description.
        type: post
  UpdateSheetPropertiesRequest:
    properties:
      fields:
        description: This is a default description.
        type: post
  UpdateSpreadsheetPropertiesRequest:
    properties:
      fields:
        description: This is a default description.
        type: post
  UpdateValuesResponse:
    properties:
      spreadsheetId:
        description: This is a default description.
        type: post
      updatedCells:
        description: This is a default description.
        type: post
      updatedColumns:
        description: This is a default description.
        type: post
      updatedRange:
        description: This is a default description.
        type: post
      updatedRows:
        description: This is a default description.
        type: post
  ValueRange:
    properties:
      majorDimension:
        description: This is a default description.
        type: post
      range:
        description: This is a default description.
        type: post
      values:
        description: This is a default description.
        type: post
  BatchClearValuesByDataFilterRequest:
    properties:
      dataFilters:
        description: This is a default description.
        type: post
  BatchClearValuesByDataFilterResponse:
    properties:
      clearedRanges:
        description: This is a default description.
        type: post
      spreadsheetId:
        description: This is a default description.
        type: post
  BatchGetValuesByDataFilterRequest:
    properties:
      dataFilters:
        description: This is a default description.
        type: post
      dateTimeRenderOption:
        description: This is a default description.
        type: post
      majorDimension:
        description: This is a default description.
        type: post
      valueRenderOption:
        description: This is a default description.
        type: post
  BatchGetValuesByDataFilterResponse:
    properties:
      spreadsheetId:
        description: This is a default description.
        type: post
      valueRanges:
        description: This is a default description.
        type: post
  BatchUpdateValuesByDataFilterRequest:
    properties:
      data:
        description: This is a default description.
        type: post
      includeValuesInResponse:
        description: This is a default description.
        type: post
      responseDateTimeRenderOption:
        description: This is a default description.
        type: post
      responseValueRenderOption:
        description: This is a default description.
        type: post
      valueInputOption:
        description: This is a default description.
        type: post
  BatchUpdateValuesByDataFilterResponse:
    properties:
      responses:
        description: This is a default description.
        type: post
      spreadsheetId:
        description: This is a default description.
        type: post
      totalUpdatedCells:
        description: This is a default description.
        type: post
      totalUpdatedColumns:
        description: This is a default description.
        type: post
      totalUpdatedRows:
        description: This is a default description.
        type: post
      totalUpdatedSheets:
        description: This is a default description.
        type: post
  BubbleChartSpec:
    properties:
      bubbleMaxRadiusSize:
        description: This is a default description.
        type: post
      bubbleMinRadiusSize:
        description: This is a default description.
        type: post
      bubbleOpacity:
        description: This is a default description.
        type: post
      legendPosition:
        description: This is a default description.
        type: post
  CandlestickChartSpec:
    properties:
      data:
        description: This is a default description.
        type: post
  CandlestickData:
    properties: []
  CandlestickDomain:
    properties:
      reversed:
        description: This is a default description.
        type: post
  CandlestickSeries:
    properties: []
  CreateDeveloperMetadataRequest:
    properties: []
  CreateDeveloperMetadataResponse:
    properties: []
  DataFilter:
    properties:
      a1Range:
        description: This is a default description.
        type: post
  DataFilterValueRange:
    properties:
      majorDimension:
        description: This is a default description.
        type: post
      values:
        description: This is a default description.
        type: post
  DeleteDeveloperMetadataRequest:
    properties: []
  DeleteDeveloperMetadataResponse:
    properties:
      deletedDeveloperMetadata:
        description: This is a default description.
        type: post
  DeveloperMetadata:
    properties:
      metadataId:
        description: This is a default description.
        type: post
      metadataKey:
        description: This is a default description.
        type: post
      metadataValue:
        description: This is a default description.
        type: post
      visibility:
        description: This is a default description.
        type: post
  DeveloperMetadataLocation:
    properties:
      locationType:
        description: This is a default description.
        type: post
      sheetId:
        description: This is a default description.
        type: post
      spreadsheet:
        description: This is a default description.
        type: post
  DeveloperMetadataLookup:
    properties:
      locationMatchingStrategy:
        description: This is a default description.
        type: post
      locationType:
        description: This is a default description.
        type: post
      metadataId:
        description: This is a default description.
        type: post
      metadataKey:
        description: This is a default description.
        type: post
      metadataValue:
        description: This is a default description.
        type: post
      visibility:
        description: This is a default description.
        type: post
  GetSpreadsheetByDataFilterRequest:
    properties:
      dataFilters:
        description: This is a default description.
        type: post
      includeGridData:
        description: This is a default description.
        type: post
  HistogramChartSpec:
    properties:
      bucketSize:
        description: This is a default description.
        type: post
      legendPosition:
        description: This is a default description.
        type: post
      outlierPercentile:
        description: This is a default description.
        type: post
      series:
        description: This is a default description.
        type: post
      showItemDividers:
        description: This is a default description.
        type: post
  HistogramRule:
    properties:
      end:
        description: This is a default description.
        type: post
      interval:
        description: This is a default description.
        type: post
      start:
        description: This is a default description.
        type: post
  HistogramSeries:
    properties: []
  LineStyle:
    properties:
      type:
        description: This is a default description.
        type: post
      width:
        description: This is a default description.
        type: post
  ManualRule:
    properties:
      groups:
        description: This is a default description.
        type: post
  ManualRuleGroup:
    properties:
      items:
        description: This is a default description.
        type: post
  MatchedDeveloperMetadata:
    properties:
      dataFilters:
        description: This is a default description.
        type: post
  MatchedValueRange:
    properties:
      dataFilters:
        description: This is a default description.
        type: post
  OrgChartSpec:
    properties:
      nodeSize:
        description: This is a default description.
        type: post
  PivotGroupRule:
    properties: []
  RandomizeRangeRequest:
    properties: []
  SearchDeveloperMetadataRequest:
    properties:
      dataFilters:
        description: This is a default description.
        type: post
  SearchDeveloperMetadataResponse:
    properties:
      matchedDeveloperMetadata:
        description: This is a default description.
        type: post
  TextPosition:
    properties:
      horizontalAlignment:
        description: This is a default description.
        type: post
  UpdateDeveloperMetadataRequest:
    properties:
      dataFilters:
        description: This is a default description.
        type: post
      fields:
        description: This is a default description.
        type: post
  UpdateDeveloperMetadataResponse:
    properties:
      developerMetadata:
        description: This is a default description.
        type: post
  UpdateValuesByDataFilterResponse:
    properties:
      updatedCells:
        description: This is a default description.
        type: post
      updatedColumns:
        description: This is a default description.
        type: post
      updatedRange:
        description: This is a default description.
        type: post
      updatedRows:
        description: This is a default description.
        type: post
  WaterfallChartColumnStyle:
    properties:
      label:
        description: This is a default description.
        type: post
  WaterfallChartCustomSubtotal:
    properties:
      dataIsSubtotal:
        description: This is a default description.
        type: post
      label:
        description: This is a default description.
        type: post
      subtotalIndex:
        description: This is a default description.
        type: post
  WaterfallChartDomain:
    properties:
      reversed:
        description: This is a default description.
        type: post
  WaterfallChartSeries:
    properties:
      customSubtotals:
        description: This is a default description.
        type: post
      hideTrailingSubtotal:
        description: This is a default description.
        type: post
  WaterfallChartSpec:
    properties:
      firstValueIsTotal:
        description: This is a default description.
        type: post
      hideConnectorLines:
        description: This is a default description.
        type: post
      series:
        description: This is a default description.
        type: post
      stackedType:
        description: This is a default description.
        type: post
x-collection-name: Google Sheets
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