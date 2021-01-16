---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: 33f1af70b0fef7e89ccb584ed3b69f32e2810690
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368776"
---
# <span data-ttu-id="d7491-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="d7491-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="d7491-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d7491-102">SYNOPSIS</span></span>
<span data-ttu-id="d7491-103">Tworzy metadane wystąpienia usługi.</span><span class="sxs-lookup"><span data-stu-id="d7491-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="d7491-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d7491-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-CosmosKeyVaultKeyUri <String>] [-ExportStorageAccountName <String>]
 [-EnableSmartProxy] [-ManagedIdentity] [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob]
 [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d7491-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d7491-105">DESCRIPTION</span></span>
<span data-ttu-id="d7491-106">Umożliwia utworzenie lub zaktualizowanie metadanych wystąpienia usługi.</span><span class="sxs-lookup"><span data-stu-id="d7491-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="d7491-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d7491-107">EXAMPLES</span></span>

### <span data-ttu-id="d7491-108">Przykład 1: tworzy nową nową usługę Azure healthcareapis fhir o nazwie Moja usługa w grupie zasobu moja grupa w lokalizacji westus2 z cosmosdb przepływem pracy = 400</span><span class="sxs-lookup"><span data-stu-id="d7491-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
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

### <span data-ttu-id="d7491-109">Przykład 2: tworzy nową nową usługę Azure healthcareapis fhir o nazwie Moja usługa w grupie zasób w lokalizacji westus2 ze cosmosdb ofertą = 400 i identyfikatorem URI klucza magazynu kluczy "https:// \<my-keyvault> . Vault.Azure.NET/Keys/ \<my-key> "</span><span class="sxs-lookup"><span data-stu-id="d7491-109">Example 2 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400 and key vault key uri "https://\<my-keyvault>.vault.azure.net/keys/\<my-key>"</span></span>
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

## <span data-ttu-id="d7491-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d7491-110">PARAMETERS</span></span>

### <span data-ttu-id="d7491-111">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="d7491-111">-AccessPolicyObjectId</span></span>
<span data-ttu-id="d7491-112">Lista identyfikatorów obiektów zasad programu Access.</span><span class="sxs-lookup"><span data-stu-id="d7491-112">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="d7491-113">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="d7491-113">-AllowCorsCredential</span></span>
<span data-ttu-id="d7491-114">HealthcareApis Fhir Service AllowCorsCredentials.</span><span class="sxs-lookup"><span data-stu-id="d7491-114">HealthcareApis Fhir Service AllowCorsCredentials.</span></span>

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

### <span data-ttu-id="d7491-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d7491-115">-AsJob</span></span>
<span data-ttu-id="d7491-116">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="d7491-116">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="d7491-117">-Odbiorca</span><span class="sxs-lookup"><span data-stu-id="d7491-117">-Audience</span></span>
<span data-ttu-id="d7491-118">HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="d7491-118">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="d7491-119">-Authority</span><span class="sxs-lookup"><span data-stu-id="d7491-119">-Authority</span></span>
<span data-ttu-id="d7491-120">HealthcareApis Fhir Service Authority.</span><span class="sxs-lookup"><span data-stu-id="d7491-120">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="d7491-121">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="d7491-121">-CorsHeader</span></span>
<span data-ttu-id="d7491-122">Lista usługi HealthcareApis Fhir nagłówka CORS.</span><span class="sxs-lookup"><span data-stu-id="d7491-122">HealthcareApis Fhir Service List of Cors Header.</span></span>
<span data-ttu-id="d7491-123">Określ nagłówki HTTP, których można użyć podczas żądania.</span><span class="sxs-lookup"><span data-stu-id="d7491-123">Specify HTTP headers which can be used during the request.</span></span>
<span data-ttu-id="d7491-124">W dowolnym nagłówku Użyj znaku "\*".</span><span class="sxs-lookup"><span data-stu-id="d7491-124">Use " \* " for any header.</span></span>

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

### <span data-ttu-id="d7491-125">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="d7491-125">-CorsMaxAge</span></span>
<span data-ttu-id="d7491-126">Maksymalny wiek usługi HealthcareApis Fhir service cors.</span><span class="sxs-lookup"><span data-stu-id="d7491-126">HealthcareApis Fhir Service Cors Max Age.</span></span>
<span data-ttu-id="d7491-127">Określ, jak długo wynik żądania może być buforowany w sekundach.</span><span class="sxs-lookup"><span data-stu-id="d7491-127">Specify how long a result from a request can be cached in seconds.</span></span>
<span data-ttu-id="d7491-128">Przykład: 600 oznacza 10 minut.</span><span class="sxs-lookup"><span data-stu-id="d7491-128">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="d7491-129">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="d7491-129">-CorsMethod</span></span>
<span data-ttu-id="d7491-130">HealthcareApis Fhir Service (lista) Metoda CORS.</span><span class="sxs-lookup"><span data-stu-id="d7491-130">HealthcareApis Fhir Service List of Cors Method.</span></span>

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

### <span data-ttu-id="d7491-131">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="d7491-131">-CorsOrigin</span></span>
<span data-ttu-id="d7491-132">HealthcareApis Fhir Service (lista pochodzenia CORS).</span><span class="sxs-lookup"><span data-stu-id="d7491-132">HealthcareApis Fhir Service List of Cors Origin.</span></span>
<span data-ttu-id="d7491-133">Określ adresy URL witryn pochodzenia, które mogą uzyskiwać dostęp do tego interfejsu API, lub użyj znaku "\*", aby zezwolić na dostęp z dowolnej witryny.</span><span class="sxs-lookup"><span data-stu-id="d7491-133">Specify URLs of origin sites that can access this API, or use " \* " to allow access from any site.</span></span>

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

### <span data-ttu-id="d7491-134">-CosmosKeyVaultKeyUri</span><span class="sxs-lookup"><span data-stu-id="d7491-134">-CosmosKeyVaultKeyUri</span></span>
<span data-ttu-id="d7491-135">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span><span class="sxs-lookup"><span data-stu-id="d7491-135">HealthcareApis Fhir Service CosmosKeyVaultKeyUri.</span></span>
<span data-ttu-id="d7491-136">Identyfikator URI klucza zarządzanego przez klienta dla kopii zapasowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d7491-136">The URI of the customer-managed key for the backing database.</span></span>

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

### <span data-ttu-id="d7491-137">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="d7491-137">-CosmosOfferThroughput</span></span>
<span data-ttu-id="d7491-138">HealthcareApis Fhir Service CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="d7491-138">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="d7491-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7491-139">-DefaultProfile</span></span>
<span data-ttu-id="d7491-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d7491-140">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d7491-141">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="d7491-141">-EnableSmartProxy</span></span>
<span data-ttu-id="d7491-142">HealthcareApis Fhir Service EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="d7491-142">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="d7491-143">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="d7491-143">-ExportStorageAccountName</span></span>
<span data-ttu-id="d7491-144">Usługa Fhir HealthcareApis eksportowanie nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="d7491-144">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="d7491-145">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="d7491-145">-FhirVersion</span></span>
<span data-ttu-id="d7491-146">Wersja Fhir.</span><span class="sxs-lookup"><span data-stu-id="d7491-146">Fhir Version.</span></span>

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

### <span data-ttu-id="d7491-147">-Kind</span><span class="sxs-lookup"><span data-stu-id="d7491-147">-Kind</span></span>
<span data-ttu-id="d7491-148">Rodzaj usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="d7491-148">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="d7491-149">Wartość domyślna to Fhir</span><span class="sxs-lookup"><span data-stu-id="d7491-149">The default value is Fhir</span></span>

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

### <span data-ttu-id="d7491-150">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d7491-150">-Location</span></span>
<span data-ttu-id="d7491-151">Lokalizacja usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="d7491-151">HealthcareApis Service Location.</span></span>

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

### <span data-ttu-id="d7491-152">-ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="d7491-152">-ManagedIdentity</span></span>
<span data-ttu-id="d7491-153">Użyć tożsamości zarządzanej?</span><span class="sxs-lookup"><span data-stu-id="d7491-153">Use Managed Identity?</span></span>

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

### <span data-ttu-id="d7491-154">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d7491-154">-Name</span></span>
<span data-ttu-id="d7491-155">Nazwa usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="d7491-155">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="d7491-156">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="d7491-156">-PublicNetworkAccess</span></span>
<span data-ttu-id="d7491-157">Typ dostępu do sieci dla usługi Fhir.</span><span class="sxs-lookup"><span data-stu-id="d7491-157">The network access type for Fhir service.</span></span> <span data-ttu-id="d7491-158">Często `Enabled` lub `Disabled` .</span><span class="sxs-lookup"><span data-stu-id="d7491-158">Commonly `Enabled` or `Disabled`.</span></span>

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

### <span data-ttu-id="d7491-159">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d7491-159">-ResourceGroupName</span></span>
<span data-ttu-id="d7491-160">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d7491-160">Resource Group Name.</span></span>

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

### <span data-ttu-id="d7491-161">-Tag</span><span class="sxs-lookup"><span data-stu-id="d7491-161">-Tag</span></span>
<span data-ttu-id="d7491-162">Znaczniki kont usługi HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="d7491-162">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="d7491-163">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d7491-163">-Confirm</span></span>
<span data-ttu-id="d7491-164">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7491-164">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d7491-165">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d7491-165">-WhatIf</span></span>
<span data-ttu-id="d7491-166">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d7491-166">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d7491-167">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d7491-167">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d7491-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7491-168">CommonParameters</span></span>
<span data-ttu-id="d7491-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7491-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7491-170">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d7491-170">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7491-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7491-171">INPUTS</span></span>

### <span data-ttu-id="d7491-172">System. String</span><span class="sxs-lookup"><span data-stu-id="d7491-172">System.String</span></span>

## <span data-ttu-id="d7491-173">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d7491-173">OUTPUTS</span></span>

### <span data-ttu-id="d7491-174">Microsoft. Azure. Commands. HealthcareApis. models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="d7491-174">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="d7491-175">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d7491-175">NOTES</span></span>

## <span data-ttu-id="d7491-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7491-176">RELATED LINKS</span></span>
