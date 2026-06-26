 @AbapCatalog.viewEnhancementCategory: [#NONE]
@AccessControl.authorizationCheck: #NOT_REQUIRED
@EndUserText.label: 'Custom SO View'
@Metadata.ignorePropagatedAnnotations: true
@ObjectModel.usageType:{
  serviceQuality: #X,
  sizeCategory: #S,
  dataClass: #MIXED
}
define view entity ZI_CUSTSO_VIEW as select from zebst_status_log
 association[1..1] to Zstatus_VH as _VH on $projection.Status = _VH.Value
{
  key salesorder as Salesorder,
  key itemno as Itemno,
  status as Status,
  timestamp as Timestamp,
  _VH.Description as statusdesc
  //statusdesc as Statusdesc
} where _VH.lang = $session.system_language
