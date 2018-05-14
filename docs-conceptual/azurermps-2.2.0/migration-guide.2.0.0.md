# <a name="table-of-contents"></a>Spis treści
1. [Usunięcie parametrów Force](#removal-of-force-parameters)
2. [Zmiana parametrów Tag](#change-of-tag-parameters)
3. [Istotne zmiany w poleceniach cmdlet usługi Storage](#breaking-changes-to-storage-cmdlets)
4. [Istotne zmiany w poleceniach cmdlet usługi AD](#breaking-changes-to-ad-cmdlets)

## <a name="removal-of-force-parameters"></a>Usunięcie parametrów Force

W tej wersji usunęliśmy wszystkie przestarzałe parametry `Force` z poleceń cmdlet i powiązane ostrzeżenia o tym, że parametry zostaną usunięte w przyszłej wersji.

Zmiana ta dotyczy następujących poleceń cmdlet:

**ApiManagement**
- Remove-AzureRmApiManagement
- Remove-AzureRmApiManagementApi
- Remove-AzureRmApiManagementGroup
- Remove-AzureRmApiManagementLogger
- Remove-AzureRmApiManagementOpenIdConnectProvider
- Remove-AzureRmApiManagementOperation
- Remove-AzureRmApiManagementPolicy
- Remove-AzureRmApiManagementProduct
- Remove-AzureRmApiManagementProperty
- Remove-AzureRmApiManagementSubscription
- Remove-AzureRmApiManagementUser

**Automatyzacja**
- Remove-AzureRmAutomationCertificate
- Remove-AzureRmAutomationCredential
- Remove-AzureRmAutomationVariable
- Remove-AzureRmAutomationWebhook

**Batch**
- Remove-AzureBatchCertificate
- Remove-AzureBatchComputeNode
- Remove-AzureBatchComputeNodeUser

**DataFactories**
- Resume-AzureRmDataFactoryPipeline
- Set-AzureRmDataFactoryPipelineActivePeriod
- Suspend-AzureRmDataFactoryPipeline

**DataLakeStore**
- Remove-AzureRmDataLakeStoreItemAclEntry
- Set-AzureRmDataLakeStoreItemAcl
- Set-AzureRmDataLakeStoreItemAclEntry
- Set-AzureRmDataLakeStoreItemOwner

**OperationalInsights**
- Remove-AzureRmOperationalInsightsSavedSearch

**Profil**
- Remove-AzureRmEnvironment

**RedisCache**
- Remove-AzureRmRedisCacheDiagnostics

**Zasoby**
- Register-AzureRmProviderFeature
- Register-AzureRmResourceProvider
- Remove-AzureRmADServicePrincipal
- Remove-AzureRmPolicyAssignment
- Remove-AzureRmResourceGroupDeployment
- Remove-AzureRmRoleAssignment
- Stop-AzureRmResourceGroupDeployment
- Unregister-AzureRmResourceProvider

**Storage**
- Remove-AzureStorageContainerStoredAccessPolicy
- Remove-AzureStorageQueueStoredAccessPolicy
- Remove-AzureStorageShareStoredAccessPolicy
- Remove-AzureStorageTableStoredAccessPolicy

**StreamAnalytics**
- Remove-AzureRmStreamAnalyticsFunction
- Remove-AzureRmStreamAnalyticsInput
- Remove-AzureRmStreamAnalyticsJob
- Remove-AzureRmStreamAnalyticsOutput

**Tag**
- Remove-AzureRmTag

<br>

Jeśli masz skrypt, który wykorzystuje dowolne z powyższych poleceń cmdlet, istotną zmianę można naprawić przez usunięcie parametru `Force`.

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location -Force

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location $location
```

<br>

## <a name="change-of-tag-parameters"></a>Zmiana parametrów Tag

W tej wersji nazwa parametru `Tags` została zmieniona na `Tag`, a typ został zmieniony z `Hashtable[]` na `Hashtable`, co zmienia format par klucz-wartość.

Wcześniej każdy wpis w elemencie `Hashtable[]` reprezentował pojedyncze parowanie klucz-wartość:

```powershell
$tags = @{ Name = "test1"; Value = "testval1" }, @{ Name = "test2", Value = "testval2" }
$tags[0].Name  # Key for the first entry, "test1"
$tags[0].Value # Value for the first entry, "testval1"
$tags[1].Name  # Key for the second entry, "test2"
$tags[1].Value # Value for the second entry, "testval2"
```

Teraz parametry `Name` i `Value` nie są już wymagane, co umożliwia tworzenie par klucz wartość przez przypisanie `Key = "Value"` w elemencie `Hashtable`:

```powershell
$tag = @{ test1 = "testval1"; test2 = "testval2" }
$tag["test1"] # Gets the value associated with the key "test1"
$tag["test2"] # Gets the value associated with the key "test2"
```

Zmiana ta dotyczy następujących poleceń cmdlet:

**Batch**
- Get-AzureRmBatchAccount
- New-AzureRmBatchAccount
- Set-AzureRmBatchAccount

**Obliczanie**
- New-AzureRmVM
- Update-AzureRmVM

**DataLakeAnalytics**
- New-AzureRmDataLakeAnalyticsAccount
- Set-AzureRmDataLakeAnalyticsAccount

**DataLakeStore**
- New-AzureRmDataLakeStoreAccount
- Set-AzureRmDataLakeStoreAccount

**Dns**
- New-AzureRmDnsZone
- Set-AzureRmDnsZone

**KeyVault**
- Get-AzureRmKeyVault
- New-AzureRmKeyVault

**Sieć**
- New-AzureRmApplicationGateway
- New-AzureRmExpressRouteCircuit
- New-AzureRmLoadBalancer
- New-AzureRmLocalNetworkGateway
- New-AzureRmNetworkInterface
- New-AzureRmNetworkSecurityGroup
- New-AzureRmPublicIpAddress
- New-AzureRmRouteTable
- New-AzureRmVirtualNetwork
- New-AzureRmVirtualNetworkGateway
- New-AzureRmVirtualNetworkGatewayConnection
- New-AzureRmVirtualNetworkPeering

**Zasoby**
- Find-AzureRmResource
- Find-AzureRmResourceGroup
- New-AzureRmResource
- New-AzureRmResourceGroup
- Set-AzureRmResource
- Set-AzureRmResourceGroup

**SQL**
- New-AzureRmSqlDatabase
- New-AzureRmSqlDatabaseCopy
- New-AzureRmSqlDatabaseSecondary
- New-AzureRmSqlElasticPool
- New-AzureRmSqlServer
- Set-AzureRmSqlDatabase
- Set-AzureRmSqlElasticPool
- Set-AzureRmSqlServer

**Storage**
- New-AzureRmStorageAccount
- Set-AzureRmStorageAccount

**TrafficManager**
- New-AzureRmTrafficManagerProfile

<br>

Jeśli masz skrypt, który wykorzystuje dowolne z powyższych poleceń cmdlet, istotną zmianę można naprawić, zmieniając parametr `Tags` na `Tag`, jak również zmieniając element `Tag` na nowy format.

```powershell
# Old
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tags @{ Name = "testtag"; Value = "testval" }

# New
New-AzureRmResourceGroup -Name $resourceGroupName -Location -location -Tag @{ testtag = "testval" }
```

<br>

## <a name="breaking-changes-to-storage-cmdlets"></a>Istotne zmiany w poleceniach cmdlet usługi Storage

Następujące polecenia cmdlet miały wpływ na tę wersję:

**Get-AzureRmStorageAccountKey**
- Polecenie cmdlet zwraca teraz listę kluczy, a nie obiekt z właściwościami dla każdego klucza

```powershell
# Old
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Key1

# New
$key = (Get-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName)[0].Value
```

**New-AzureRmStorageAccountKey**
- Nazwa pola `StorageAccountRegenerateKeyResponse` w danych wyjściowych tego polecenia cmdlet została zmieniona na `StorageAccountListKeysResults` i teraz jest to lista kluczy, a nie obiekt z właściwościami dla każdego klucza

```powershell
# Old
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).StorageAccountKeys.Key1

# New
$key = (New-AzureRmStorageAccountKey -ResourceGroupName $resourceGroupName -Name $accountName).Keys[0].Value
```

**New/Get/Set-AzureRmStorageAccount**
- Nazwa pola `AccountType` w danych wyjściowych tego polecenia cmdlet została zmieniona na `Sku.Name`
- Typ wyjściowy dla obiektu blob/tabeli/kolejki/pliku głównych punktów końcowych/pomocniczych obiektów końcowych zmienił się z `Uri` na `String`

```powershell
# Old
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).AccountType

# New
$accountType = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).Sku.Name
```

```powershell
# Old 
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.AbsolutePath

# New
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob.ToString()
$blobEndpoint = (Get-AzureRmStorageAccount -ResourceGroupName $resourceGroupName -Name $accountName).PrimaryEndpoints.Blob
```

<br>

## <a name="breaking-changes-to-ad-cmdlets"></a>Istotne zmiany w poleceniach cmdlet usługi AD

Następujące polecenia cmdlet miały wpływ na tę wersję:

**Get-AzureRMADServicePrincipal**
- Nazwa pola `ServicePrincipalName` w danych wyjściowych tego polecenia cmdlet została zmieniona na `ServicePrincipalNames` i obecnie to pole jest kolekcją. Teraz wyświetla ono również nazwę `ApplicationId` jako jedną z głównych nazw usługi wraz z parametrem identifierUri.

```powershell
# Old
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalName

# New
$servicePrincipals = Get-AzureRmADServicePrincipal -SearchString $displayName
$spn = $servicePrincipals[0].ServicePrincipalNames[0]
```

**Get-AzureRmADApplication**
- Nazwa parametru `ApplicationObjectId` została zmieniona na `ObjectId`.
- Nazwa elementu `ApplicationObjectId` w danych wyjściowych tego polecenia cmdlet została zmieniona na `ObjectId`.

```powershell
# Old
$app = Get-AzureRmADApplication -ApplicationObjectId $applicationObjectId
$objectId = $app.ApplicationObjectId

# New
$app = Get-AzureRmADApplication -ObjectId $objectId
$objectId = $app.ObjectId
```

**Remove-AzureRmADApplication**
- Nazwa parametru `ApplicationObjectId` została zmieniona na `ObjectId`.

```powershell
# Old
$app = Remove-AzureRmADApplication -ApplicationObjectId $applicationObjectId -Force

# New
$app = Remove-AzureRmADApplication -ObjectId $objectId -Force
```

**New-AzureRmADApplication**
- Nazwa elementu `ApplicationObjectId` w danych wyjściowych tego polecenia cmdlet została zmieniona na `ObjectId`.
- Parametry `KeyValue`, `KeyUsage`, `KeyType` zostały usunięte.

```powershell
# Old
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris -KeyValue $kv -KeyType $kt -KeyUsage $ku
$id = $app.ApplicationObjectId

# New
$app = New-AzureRmADApplication -DisplayName $displayName -HomePage $homePage -IdentifierUris $identifierUris
$id = $app.ObjectId
New-AzureRmADAppCredential -ObjectId $id -Password $kv
```

**Get-AzureRmADGroup**
- Usunięto pole `Mail` z danych wyjściowych.

**Get-AzureRmADUser**
- Usunięto pole `Mail` z danych wyjściowych.

**New-AzureRmADServicePrincipal**
- Usunięto parametr `DisableAccount`.

```powershell
# Old
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password -DisableAccount true

# New
$servicePrincipal = New-AzureRmADServicePrincipal -DisplayName $displayName -Password $password
Remove-AzureRmADServicePrincipal -ObjectId $servicePrincipal.ObjectId
```