---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: 33f1af70b0fef7e89ccb584ed3b69f32e2810690
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196267"
---
# <span data-ttu-id="2c91e-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="2c91e-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="2c91e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c91e-102">SYNOPSIS</span></span>
<span data-ttu-id="2c91e-103">Tworzy metadane wystąpienia usługi.</span><span class="sxs-lookup"><span data-stu-id="2c91e-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="2c91e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2c91e-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>] [-ExportStorageAccountName <String>]
 [-EnableSmartProxy] [-ManagedIdentity] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c91e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2c91e-105">DESCRIPTION</span></span>
<span data-ttu-id="2c91e-106">Tworzy lub aktualizuje metadane wystąpienia usługi.</span><span class="sxs-lookup"><span data-stu-id="2c91e-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="2c91e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2c91e-107">EXAMPLES</span></span>

### <span data-ttu-id="2c91e-108">Przykład 1. Tworzy nową usługę Azure healthcareapis fhir o nazwie MyService w grupie zasobów MyResourceGroup w lokalizacji westus2 z przepływnością oferty dla usługi azure healthcareapis = 400</span><span class="sxs-lookup"><span data-stu-id="2c91e-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  : 
CosmosDbOfferThroughput : 400
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

### <span data-ttu-id="2c91e-109">Przykład 2. Tworzy nową usługę Azure healthcareapis fhir o nazwie MyService w grupie zasobów MyResourceGroup w lokalizacji westus2 z przepływnością oferty w usłudze azure healthcareapis = 400 oraz uri klucza magazynu kluczy "https:// \<my-keyvault> \<my-key> .vault.azure.net/keys/".</span><span class="sxs-lookup"><span data-stu-id="2c91e-109">Example 2 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput 400 -CosmosKeyVaultKeyUri "https://<my-keyvault>.vault.azure.net/keys/<my-key>"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  : https://<my-keyvault>.vault.azure.net/keys/<my-key>
CosmosDbOfferThroughput : 400
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

## <span data-ttu-id="2c91e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c91e-110">PARAMETERS</span></span>

### <span data-ttu-id="2c91e-111">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="2c91e-111">-AccessPolicyObjectId</span></span>
<span data-ttu-id="2c91e-112">Lista identyfikatorów obiektów zasad programu Access.</span><span class="sxs-lookup"><span data-stu-id="2c91e-112">List of Access Policy Object IDs.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c91e-113">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="2c91e-113">-AllowCorsCredential</span></span>
<span data-ttu-id="2c91e-114">HealthcareApis Fhir Service AllowCorsCredentials.</span><span class="sxs-lookup"><span data-stu-id="2c91e-114">HealthcareApis Fhir Service AllowCorsCredentials.</span></span>

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

### <span data-ttu-id="2c91e-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="2c91e-115">-AsJob</span></span>
<span data-ttu-id="2c91e-116">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="2c91e-116">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="2c91e-117">— Odbiorcy</span><span class="sxs-lookup"><span data-stu-id="2c91e-117">-Audience</span></span>
<span data-ttu-id="2c91e-118">HealthcareApis Fhir Service Audience.</span><span class="sxs-lookup"><span data-stu-id="2c91e-118">HealthcareApis Fhir Service Audience.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c91e-119">— Urząd</span><span class="sxs-lookup"><span data-stu-id="2c91e-119">-Authority</span></span>
<span data-ttu-id="2c91e-120">HealthcareApis Fhir Service Authority.</span><span class="sxs-lookup"><span data-stu-id="2c91e-120">HealthcareApis Fhir Service Authority.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c91e-121">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="2c91e-121">-CorsHeader</span></span>
<span data-ttu-id="2c91e-122">HealthcareApis Fhir Service List of Cors Header.</span><span class="sxs-lookup"><span data-stu-id="2c91e-122">HealthcareApis Fhir Service List of Cors Header.</span></span>
<span data-ttu-id="2c91e-123">Określ nagłówki HTTP, których można używać podczas żądania.</span><span class="sxs-lookup"><span data-stu-id="2c91e-123">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="2c91e-124">W dowolnym nagłówku użyj " \*".</span><span class="sxs-lookup"><span data-stu-id="2c91e-124">Use " \* " for any header.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c91e-125">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="2c91e-125">-CorsMaxAge</span></span>
<span data-ttu-id="2c91e-126">HealthcareApis Fhir Service Cors Max Age.</span><span class="sxs-lookup"><span data-stu-id="2c91e-126">HealthcareApis Fhir Service Cors Max Age.</span></span>
<span data-ttu-id="2c91e-127">Określ, jak długo wynik żądania może być buforowany w ciągu kilku sekund.</span><span class="sxs-lookup"><span data-stu-id="2c91e-127">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="2c91e-128">Przykład: 600 oznacza 10 minut.</span><span class="sxs-lookup"><span data-stu-id="2c91e-128">Example: 600 means 10 minutes.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c91e-129">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="2c91e-129">-CorsMethod</span></span>
<span data-ttu-id="2c91e-130">HealthcareApis Fhir Service List of Cors Method.</span><span class="sxs-lookup"><span data-stu-id="2c91e-130">HealthcareApis Fhir Service List of Cors Method.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c91e-131">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="2c91e-131">-CorsOrigin</span></span>
<span data-ttu-id="2c91e-132">HealthcareApis Fhir Service List of Cors Origin.</span><span class="sxs-lookup"><span data-stu-id="2c91e-132">HealthcareApis Fhir Service List of Cors Origin.</span></span>
<span data-ttu-id="2c91e-133">Określ adresy URL witryn pochodzenia, które mogą uzyskać dostęp do tego interfejsu API, lub użyj "\*", aby zezwolić na dostęp z dowolnej witryny.</span><span class="sxs-lookup"><span data-stu-id="2c91e-133">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c91e-134">-AlegosKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="2c91e-134">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="2c91e-135">HealthcareApis Fhir Service JednaksKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="2c91e-135">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="2c91e-136">URI klucza zarządzanego przez klienta dla bazy danych kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="2c91e-136">The URI of the customer-managed key for the backing database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c91e-137">-NamysłOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="2c91e-137">-CosmosOfferThroughput</span></span>
<span data-ttu-id="2c91e-138">HealthcareApis Fhir Service DosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="2c91e-138">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c91e-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c91e-139">-DefaultProfile</span></span>
<span data-ttu-id="2c91e-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c91e-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c91e-141">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="2c91e-141">-EnableSmartProxy</span></span>
<span data-ttu-id="2c91e-142">HealthcareApis Fhir Service EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="2c91e-142">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="2c91e-143">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2c91e-143">-ExportStorageAccountName</span></span>
<span data-ttu-id="2c91e-144">Nazwa konta magazynu eksportu usługi HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="2c91e-144">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c91e-145">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="2c91e-145">-FhirVersion</span></span>
<span data-ttu-id="2c91e-146">Wersja Fhir.</span><span class="sxs-lookup"><span data-stu-id="2c91e-146">Fhir Version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c91e-147">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="2c91e-147">-Kind</span></span>
<span data-ttu-id="2c91e-148">Rodzaj usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="2c91e-148">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="2c91e-149">Wartość domyślna to Fhir</span><span class="sxs-lookup"><span data-stu-id="2c91e-149">The default value is Fhir</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c91e-150">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2c91e-150">-Location</span></span>
<span data-ttu-id="2c91e-151">Lokalizacja usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="2c91e-151">HealthcareApis Service Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c91e-152">- ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="2c91e-152">-ManagedIdentity</span></span>
<span data-ttu-id="2c91e-153">Używasz tożsamości zarządzanej?</span><span class="sxs-lookup"><span data-stu-id="2c91e-153">Use Managed Identity?</span></span>

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

### <span data-ttu-id="2c91e-154">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2c91e-154">-Name</span></span>
<span data-ttu-id="2c91e-155">Nazwa usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="2c91e-155">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c91e-156">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="2c91e-156">-PublicNetworkAccess</span></span>
<span data-ttu-id="2c91e-157">Typ dostępu sieciowego dla usługi Fhir.</span><span class="sxs-lookup"><span data-stu-id="2c91e-157">The network access type for Fhir service.</span></span> <span data-ttu-id="2c91e-158">Często `Enabled` lub `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="2c91e-158">Commonly `Enabled` or `Disabled`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c91e-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c91e-159">-ResourceGroupName</span></span>
<span data-ttu-id="2c91e-160">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2c91e-160">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c91e-161">— Tag</span><span class="sxs-lookup"><span data-stu-id="2c91e-161">-Tag</span></span>
<span data-ttu-id="2c91e-162">Znaczniki konta usługi HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="2c91e-162">HealthcareApis Fhir Service Account Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c91e-163">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2c91e-163">-Confirm</span></span>
<span data-ttu-id="2c91e-164">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2c91e-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c91e-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c91e-165">-WhatIf</span></span>
<span data-ttu-id="2c91e-166">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c91e-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c91e-167">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2c91e-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c91e-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c91e-168">CommonParameters</span></span>
<span data-ttu-id="2c91e-169">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c91e-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c91e-170">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c91e-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c91e-171">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c91e-171">INPUTS</span></span>

### <span data-ttu-id="2c91e-172">System.String</span><span class="sxs-lookup"><span data-stu-id="2c91e-172">System.String</span></span>

## <span data-ttu-id="2c91e-173">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2c91e-173">OUTPUTS</span></span>

### <span data-ttu-id="2c91e-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="2c91e-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="2c91e-175">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2c91e-175">NOTES</span></span>

## <span data-ttu-id="2c91e-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c91e-176">RELATED LINKS</span></span>
