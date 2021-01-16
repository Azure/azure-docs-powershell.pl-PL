---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: c8eb7c58300e3252422d8b599422a3a14eb5c1fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337054"
---
# <span data-ttu-id="0ea90-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="0ea90-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="0ea90-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ea90-102">SYNOPSIS</span></span>
<span data-ttu-id="0ea90-103">Umożliwia zaktualizowanie istniejącej usługi healthcareApis fhir.</span><span class="sxs-lookup"><span data-stu-id="0ea90-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="0ea90-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ea90-104">SYNTAX</span></span>

### <span data-ttu-id="0ea90-105">ServiceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0ea90-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-CosmosKeyVaultKeyUri <String>] [-Authority <String>] [-Audience <String>] [-EnableSmartProxy]
 [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>] [-CorsMethod <String[]>]
 [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential] [-ExportStorageAccountName <String>]
 [-AccessPolicyObjectId <String[]>] [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>]
 [-AsJob] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ea90-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ea90-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-ExportStorageAccountName <String>] [-AccessPolicyObjectId <String[]>]
 [-EnableManagedIdentity] [-DisableManagedIdentity] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0ea90-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0ea90-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0ea90-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0ea90-108">DESCRIPTION</span></span>
<span data-ttu-id="0ea90-109">Umożliwia zaktualizowanie istniejącej usługi healthcareApis fhir.</span><span class="sxs-lookup"><span data-stu-id="0ea90-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="0ea90-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ea90-110">EXAMPLES</span></span>

### <span data-ttu-id="0ea90-111">Przykład 1: umożliwia zaktualizowanie istniejącej usługi healthcareapis o nazwie Moja usługa w grupie zasobu moja grupa zasobów przy użyciu cosmosdb OfferThroughputd = 500.</span><span class="sxs-lookup"><span data-stu-id="0ea90-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

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

### <span data-ttu-id="0ea90-112">Przykład 2: umożliwia zaktualizowanie istniejącej usługi healthcareapis o nazwie Moja usługa w grupie zasobu moja grupa zasobów przy użyciu cosmosdb OfferThroughputd = 500 i identyfikatora URI klucza magazynu kluczy "https:// \<my-keyvault> . Vault.Azure.NET/Keys/ \<my-key> "</span><span class="sxs-lookup"><span data-stu-id="0ea90-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>

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

## <span data-ttu-id="0ea90-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ea90-113">PARAMETERS</span></span>

### <span data-ttu-id="0ea90-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="0ea90-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="0ea90-115">Lista identyfikatorów obiektów zasad programu Access.</span><span class="sxs-lookup"><span data-stu-id="0ea90-115">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="0ea90-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="0ea90-116">-AllowCorsCredential</span></span>
<span data-ttu-id="0ea90-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="0ea90-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

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

### <span data-ttu-id="0ea90-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0ea90-118">-AsJob</span></span>
<span data-ttu-id="0ea90-119">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="0ea90-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="0ea90-120">-Odbiorca</span><span class="sxs-lookup"><span data-stu-id="0ea90-120">-Audience</span></span>
<span data-ttu-id="0ea90-121">HealthcareApis FhirService odbiorców.</span><span class="sxs-lookup"><span data-stu-id="0ea90-121">HealthcareApis FhirService Audience.</span></span>

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

### <span data-ttu-id="0ea90-122">-Authority</span><span class="sxs-lookup"><span data-stu-id="0ea90-122">-Authority</span></span>
<span data-ttu-id="0ea90-123">HealthcareApis FhirService Authority.</span><span class="sxs-lookup"><span data-stu-id="0ea90-123">HealthcareApis FhirService Authority.</span></span>

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

### <span data-ttu-id="0ea90-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="0ea90-124">-CorsHeader</span></span>
<span data-ttu-id="0ea90-125">HealthcareApis FhirService lista nagłówków CORS.</span><span class="sxs-lookup"><span data-stu-id="0ea90-125">HealthcareApis FhirService List of Cors Headers.</span></span>
<span data-ttu-id="0ea90-126">Określ nagłówki HTTP, których można użyć podczas żądania.</span><span class="sxs-lookup"><span data-stu-id="0ea90-126">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="0ea90-127">W dowolnym nagłówku Użyj znaku "\*".</span><span class="sxs-lookup"><span data-stu-id="0ea90-127">Use " \* " for any header.</span></span>

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

### <span data-ttu-id="0ea90-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="0ea90-128">-CorsMaxAge</span></span>
<span data-ttu-id="0ea90-129">Maksymalny wiek HealthcareApis FhirService CORS.</span><span class="sxs-lookup"><span data-stu-id="0ea90-129">HealthcareApis FhirService Cors Max Age.</span></span>
<span data-ttu-id="0ea90-130">Określ, jak długo wynik żądania może być buforowany w sekundach.</span><span class="sxs-lookup"><span data-stu-id="0ea90-130">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="0ea90-131">Przykład: 600 oznacza 10 minut.</span><span class="sxs-lookup"><span data-stu-id="0ea90-131">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="0ea90-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="0ea90-132">-CorsMethod</span></span>
<span data-ttu-id="0ea90-133">HealthcareApis FhirService listą metod CORS.</span><span class="sxs-lookup"><span data-stu-id="0ea90-133">HealthcareApis FhirService List of Cors Methods.</span></span>

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

### <span data-ttu-id="0ea90-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="0ea90-134">-CorsOrigin</span></span>
<span data-ttu-id="0ea90-135">HealthcareApis FhirService lista pochodzenia CORS.</span><span class="sxs-lookup"><span data-stu-id="0ea90-135">HealthcareApis FhirService List of Cors Origins.</span></span>
<span data-ttu-id="0ea90-136">Określ adresy URL witryn pochodzenia, które mogą uzyskiwać dostęp do tego interfejsu API, lub użyj znaku "\*", aby zezwolić na dostęp z dowolnej witryny.</span><span class="sxs-lookup"><span data-stu-id="0ea90-136">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

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

### <span data-ttu-id="0ea90-137">-CosmosKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="0ea90-137">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="0ea90-138">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="0ea90-138">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="0ea90-139">Identyfikator URI klucza zarządzanego przez klienta dla kopii zapasowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0ea90-139">The URI of the customer-managed key for the backing database.</span></span>

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

### <span data-ttu-id="0ea90-140">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="0ea90-140">-CosmosOfferThroughput</span></span>
<span data-ttu-id="0ea90-141">HealthcareApis FhirService CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="0ea90-141">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="0ea90-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ea90-142">-DefaultProfile</span></span>
<span data-ttu-id="0ea90-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0ea90-143">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0ea90-144">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="0ea90-144">-DisableCorsCredential</span></span>
<span data-ttu-id="0ea90-145">HealthcareApis FhirService CorsCredentials nie jest dozwolone.</span><span class="sxs-lookup"><span data-stu-id="0ea90-145">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

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

### <span data-ttu-id="0ea90-146">-DisableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="0ea90-146">-DisableManagedIdentity</span></span>
<span data-ttu-id="0ea90-147">Wyłącz zarządzaną tożsamość.</span><span class="sxs-lookup"><span data-stu-id="0ea90-147">Disable Managed Identity.</span></span>

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

### <span data-ttu-id="0ea90-148">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="0ea90-148">-DisableSmartProxy</span></span>
<span data-ttu-id="0ea90-149">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="0ea90-149">HealthcareApis FhirService DisableSmartProxy.</span></span>

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

### <span data-ttu-id="0ea90-150">-EnableManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="0ea90-150">-EnableManagedIdentity</span></span>
<span data-ttu-id="0ea90-151">Włącz zarządzaną tożsamość.</span><span class="sxs-lookup"><span data-stu-id="0ea90-151">Enable Managed Identity.</span></span>

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

### <span data-ttu-id="0ea90-152">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="0ea90-152">-EnableSmartProxy</span></span>
<span data-ttu-id="0ea90-153">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="0ea90-153">HealthcareApis FhirService EnableSmartProxy.</span></span>

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

### <span data-ttu-id="0ea90-154">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0ea90-154">-ExportStorageAccountName</span></span>
<span data-ttu-id="0ea90-155">Usługa Fhir HealthcareApis eksportowanie nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="0ea90-155">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="0ea90-156">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="0ea90-156">-InputObject</span></span>
<span data-ttu-id="0ea90-157">Usługa fhir HealthcareApis pozostała w potoku od get-AzHealthcareApisFhirService.</span><span class="sxs-lookup"><span data-stu-id="0ea90-157">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

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

### <span data-ttu-id="0ea90-158">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0ea90-158">-Name</span></span>
<span data-ttu-id="0ea90-159">Nazwa usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="0ea90-159">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="0ea90-160">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="0ea90-160">-PublicNetworkAccess</span></span>
<span data-ttu-id="0ea90-161">Typ dostępu do sieci dla usługi Fhir.</span><span class="sxs-lookup"><span data-stu-id="0ea90-161">The network access type for Fhir service.</span></span> <span data-ttu-id="0ea90-162">Często `Enabled` lub `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="0ea90-162">Commonly `Enabled` or `Disabled`.</span></span>

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

### <span data-ttu-id="0ea90-163">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ea90-163">-ResourceGroupName</span></span>
<span data-ttu-id="0ea90-164">Nazwa grupy zasobów usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="0ea90-164">HealthcareApis Service Resource Group Name.</span></span>

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

### <span data-ttu-id="0ea90-165">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0ea90-165">-ResourceId</span></span>
<span data-ttu-id="0ea90-166">Identyfikator zasobu usługi Fhir HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="0ea90-166">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="0ea90-167">-Tag</span><span class="sxs-lookup"><span data-stu-id="0ea90-167">-Tag</span></span>
<span data-ttu-id="0ea90-168">Znaczniki kont usługi HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="0ea90-168">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="0ea90-169">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0ea90-169">-Confirm</span></span>
<span data-ttu-id="0ea90-170">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ea90-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ea90-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ea90-171">-WhatIf</span></span>
<span data-ttu-id="0ea90-172">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0ea90-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0ea90-173">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0ea90-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ea90-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ea90-174">CommonParameters</span></span>
<span data-ttu-id="0ea90-175">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ea90-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ea90-176">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ea90-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ea90-177">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ea90-177">INPUTS</span></span>

### <span data-ttu-id="0ea90-178">Microsoft. Azure. Commands. HealthcareApis. models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="0ea90-178">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

### <span data-ttu-id="0ea90-179">System. String</span><span class="sxs-lookup"><span data-stu-id="0ea90-179">System.String</span></span>

## <span data-ttu-id="0ea90-180">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ea90-180">OUTPUTS</span></span>

### <span data-ttu-id="0ea90-181">Microsoft. Azure. Commands. HealthcareApis. models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="0ea90-181">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="0ea90-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ea90-182">NOTES</span></span>

## <span data-ttu-id="0ea90-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ea90-183">RELATED LINKS</span></span>
