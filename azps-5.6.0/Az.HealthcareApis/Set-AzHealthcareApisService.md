---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: 2ff0f9f03524368e01b6edbcad5b8db8fef4fb21
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013162"
---
# <span data-ttu-id="b037a-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="b037a-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="b037a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b037a-102">SYNOPSIS</span></span>
<span data-ttu-id="b037a-103">Aktualizuje istniejącą usługę opieki zdrowotnej.</span><span class="sxs-lookup"><span data-stu-id="b037a-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="b037a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b037a-104">SYNTAX</span></span>

### <span data-ttu-id="b037a-105">ServiceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b037a-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-CosmosKeyVaultKeyUri <String>] [-Authority <String>] [-Audience <String>] [-EnableSmartProxy]
 [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>] [-CorsMethod <String[]>]
 [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential] [-ExportStorageAccountName <String>]
 [-AccessPolicyObjectId <String[]>] [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>]
 [-AsJob] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b037a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b037a-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>]
 [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b037a-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b037a-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b037a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b037a-108">DESCRIPTION</span></span>
<span data-ttu-id="b037a-109">Aktualizuje istniejącą usługę opieki zdrowotnej.</span><span class="sxs-lookup"><span data-stu-id="b037a-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="b037a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b037a-110">EXAMPLES</span></span>

### <span data-ttu-id="b037a-111">Przykład 1. Aktualizuje istniejącą usługę opieki zdrowotnej o nazwie MyService w grupie zasobów MyResourceGroup przy użyciu plikudb OfferThroughput = 500.</span><span class="sxs-lookup"><span data-stu-id="b037a-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> Set-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosKeyVaultKeyUri    : 
CosmosDbOfferThroughput : 500
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="b037a-112">Przykład 2. Aktualizuje istniejącą usługę healthcareapis o nazwie MyService w grupie zasobów MyResourceGroup przy użyciu domenysdb OfferThroughput = 500 i uri klucza magazynu klucza "https:// \<my-keyvault> \<my-key> .vault.azure.net/keys/"</span><span class="sxs-lookup"><span data-stu-id="b037a-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>

```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService"
PS C:\> Set-AzHealthcareApisService -ResourceId $ResourceId  -CosmosOfferThroughput 500 -CosmosKeyVaultKeyUri "https://<my-keyvault>.vault.azure.net/keys/<my-key>"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosKeyVaultKeyUri    : https://<my-keyvault>.vault.azure.net/keys/<my-key>
CosmosDbOfferThroughput : 500
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

## <span data-ttu-id="b037a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b037a-113">PARAMETERS</span></span>

### <span data-ttu-id="b037a-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="b037a-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="b037a-115">Lista identyfikatorów obiektów zasad programu Access.</span><span class="sxs-lookup"><span data-stu-id="b037a-115">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="b037a-116">-AllowCorsCredential</span></span>
<span data-ttu-id="b037a-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="b037a-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b037a-118">-AsJob</span></span>
<span data-ttu-id="b037a-119">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="b037a-119">Run cmdlet as a job in the background.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-120">— Odbiorcy</span><span class="sxs-lookup"><span data-stu-id="b037a-120">-Audience</span></span>
<span data-ttu-id="b037a-121">HealthcareApis FhirService Audience.</span><span class="sxs-lookup"><span data-stu-id="b037a-121">HealthcareApis FhirService Audience.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-122">— Urząd</span><span class="sxs-lookup"><span data-stu-id="b037a-122">-Authority</span></span>
<span data-ttu-id="b037a-123">HealthcareApis FhirService Authority.</span><span class="sxs-lookup"><span data-stu-id="b037a-123">HealthcareApis FhirService Authority.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="b037a-124">-CorsHeader</span></span>
<span data-ttu-id="b037a-125">HealthcareApis FhirService List of Cors Headers.</span><span class="sxs-lookup"><span data-stu-id="b037a-125">HealthcareApis FhirService List of Cors Headers.</span></span>
<span data-ttu-id="b037a-126">Określ nagłówki HTTP, których można używać podczas żądania.</span><span class="sxs-lookup"><span data-stu-id="b037a-126">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="b037a-127">W dowolnym nagłówku użyj " \*".</span><span class="sxs-lookup"><span data-stu-id="b037a-127">Use " \* " for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="b037a-128">-CorsMaxAge</span></span>
<span data-ttu-id="b037a-129">HealthcareApis FhirService Cors Max Age.</span><span class="sxs-lookup"><span data-stu-id="b037a-129">HealthcareApis FhirService Cors Max Age.</span></span>
<span data-ttu-id="b037a-130">Określ, jak długo wynik żądania może być buforowany w ciągu kilku sekund.</span><span class="sxs-lookup"><span data-stu-id="b037a-130">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="b037a-131">Przykład: 600 oznacza 10 minut.</span><span class="sxs-lookup"><span data-stu-id="b037a-131">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="b037a-132">-CorsMethod</span></span>
<span data-ttu-id="b037a-133">HealthcareApis FhirService List of Cors Methods.</span><span class="sxs-lookup"><span data-stu-id="b037a-133">HealthcareApis FhirService List of Cors Methods.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="b037a-134">-CorsOrigin</span></span>
<span data-ttu-id="b037a-135">HealthcareApis FhirService List of Cors Origins.</span><span class="sxs-lookup"><span data-stu-id="b037a-135">HealthcareApis FhirService List of Cors Origins.</span></span>
<span data-ttu-id="b037a-136">Określ adresy URL witryn pochodzenia, które mogą uzyskać dostęp do tego interfejsu API, lub użyj "\*", aby zezwolić na dostęp z dowolnej witryny.</span><span class="sxs-lookup"><span data-stu-id="b037a-136">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-137">-AlegosKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="b037a-137">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="b037a-138">HealthcareApis Fhir Service JednaksKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="b037a-138">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="b037a-139">URI klucza zarządzanego przez klienta dla bazy danych kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b037a-139">The URI of the customer-managed key for the backing database.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-140">-NamysłOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="b037a-140">-CosmosOfferThroughput</span></span>
<span data-ttu-id="b037a-141">HealthcareApis FhirService JednaksOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="b037a-141">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b037a-142">-DefaultProfile</span></span>
<span data-ttu-id="b037a-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b037a-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-144">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="b037a-144">-DisableCorsCredential</span></span>
<span data-ttu-id="b037a-145">HealthcareApis FhirService CorsCredentials Not Allowed.</span><span class="sxs-lookup"><span data-stu-id="b037a-145">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-146">-DisableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="b037a-146">-DisableManagedIdentity</span></span>
<span data-ttu-id="b037a-147">Wyłącz tożsamość zarządzaną.</span><span class="sxs-lookup"><span data-stu-id="b037a-147">Disable Managed Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-148">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="b037a-148">-DisableSmartProxy</span></span>
<span data-ttu-id="b037a-149">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="b037a-149">HealthcareApis FhirService DisableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-150">-EnableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="b037a-150">-EnableManagedIdentity</span></span>
<span data-ttu-id="b037a-151">Włącz tożsamość zarządzaną.</span><span class="sxs-lookup"><span data-stu-id="b037a-151">Enable Managed Identity.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-152">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="b037a-152">-EnableSmartProxy</span></span>
<span data-ttu-id="b037a-153">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="b037a-153">HealthcareApis FhirService EnableSmartProxy.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-154">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b037a-154">-ExportStorageAccountName</span></span>
<span data-ttu-id="b037a-155">Nazwa konta magazynu eksportu usługi HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="b037a-155">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-156">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b037a-156">-InputObject</span></span>
<span data-ttu-id="b037a-157">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span><span class="sxs-lookup"><span data-stu-id="b037a-157">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

```yaml
Type: Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-158">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b037a-158">-Name</span></span>
<span data-ttu-id="b037a-159">Nazwa usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="b037a-159">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-160">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="b037a-160">-PublicNetworkAccess</span></span>
<span data-ttu-id="b037a-161">Typ dostępu sieciowego dla usługi Fhir.</span><span class="sxs-lookup"><span data-stu-id="b037a-161">The network access type for Fhir service.</span></span> <span data-ttu-id="b037a-162">Często `Enabled` lub `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="b037a-162">Commonly `Enabled` or `Disabled`.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b037a-163">-ResourceGroupName</span></span>
<span data-ttu-id="b037a-164">Nazwa grupy zasobów usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="b037a-164">HealthcareApis Service Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-165">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b037a-165">-ResourceId</span></span>
<span data-ttu-id="b037a-166">HealthcareApis Fhir Service ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b037a-166">HealthcareApis Fhir Service ResourceId.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-167">— Tag</span><span class="sxs-lookup"><span data-stu-id="b037a-167">-Tag</span></span>
<span data-ttu-id="b037a-168">Znaczniki konta usługi HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="b037a-168">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-169">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b037a-169">-Confirm</span></span>
<span data-ttu-id="b037a-170">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b037a-170">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b037a-171">-WhatIf</span></span>
<span data-ttu-id="b037a-172">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b037a-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b037a-173">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b037a-173">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b037a-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b037a-174">CommonParameters</span></span>
<span data-ttu-id="b037a-175">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b037a-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b037a-176">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b037a-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b037a-177">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b037a-177">INPUTS</span></span>

### <span data-ttu-id="b037a-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="b037a-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="b037a-179">System.String</span><span class="sxs-lookup"><span data-stu-id="b037a-179">System.String</span></span>

## <span data-ttu-id="b037a-180">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b037a-180">OUTPUTS</span></span>

### <span data-ttu-id="b037a-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="b037a-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="b037a-182">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b037a-182">NOTES</span></span>

## <span data-ttu-id="b037a-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b037a-183">RELATED LINKS</span></span>
