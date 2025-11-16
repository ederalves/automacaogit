# automacaogit
Repositório para armazenamento de códigos necessários para automações já conhecidas ou já desenvolvidas.
Import-Module ActiveDirectory

$Samaccountname= 


Get-AdPrincipalGroupMembership -Identity $Samaccountname | Where-Object -Property Name -Ne -Value 'Domain Users' | Remove-AdGroupMember -Members $Samaccountname -confirm:$false

