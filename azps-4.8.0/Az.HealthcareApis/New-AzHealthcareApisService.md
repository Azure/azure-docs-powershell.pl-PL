---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/new-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/New-AzHealthcareApisService.md
ms.openlocfilehash: f5f8f00a2ab73485b4da6ad6df17ecf526c360bb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223893"
---
# <span data-ttu-id="3e67f-101">New-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="3e67f-101">New-AzHealthcareApisService</span></span>

## <span data-ttu-id="3e67f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3e67f-102">SYNOPSIS</span></span>
<span data-ttu-id="3e67f-103">Tworzy metadane wystąpienia usługi.</span><span class="sxs-lookup"><span data-stu-id="3e67f-103">Creates the metadata of a service instance.</span></span>

## <span data-ttu-id="3e67f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3e67f-104">SYNTAX</span></span>

```
New-AzHealthcareApisService -Name <String> -ResourceGroupName <String> -Location <String> [-Kind <String>]
 [-AccessPolicyObjectId <String[]>] [-AllowCorsCredential] [-Audience <String>] [-Authority <String>]
 [-CorsHeader <String[]>] [-CorsMaxAge <Int32>] [-CorsMethod <String[]>] [-CorsOrigin <String[]>]
 [-CosmosOfferThroughput <Int32>] [-ExportStorageAccountName <String>] [-EnableSmartProxy] [-ManagedIdentity]
 [-FhirVersion <String>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3e67f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3e67f-105">DESCRIPTION</span></span>
<span data-ttu-id="3e67f-106">Umożliwia utworzenie lub zaktualizowanie metadanych wystąpienia usługi.</span><span class="sxs-lookup"><span data-stu-id="3e67f-106">Creates or updates the metadata of a service instance.</span></span>

## <span data-ttu-id="3e67f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3e67f-107">EXAMPLES</span></span>

### <span data-ttu-id="3e67f-108">Przykład 1: tworzy nową nową usługę Azure healthcareapis fhir o nazwie Moja usługa w grupie zasobu moja grupa w lokalizacji westus2 z cosmosdb przepływem pracy = 400</span><span class="sxs-lookup"><span data-stu-id="3e67f-108">Example 1 : Creates a new Azure healthcareapis fhir service named MyService in the resource group MyResourceGroup in a location westus2 with cosmosdb offer throughput = 400</span></span>
```powershell
PS C:\> New-AzHealthcareApisService -Name MyService -ResourceGroupName MyResourceGroup -Location MyLocation -Kind fhir-R4 -CosmosOfferThroughput  400

ResourceGroupName Name Location        Kind   CosmosOfferThroughput
----------------- ----------- -------------------------------
MyResourceGroup   MyService   westus2    fhir-R4   400

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
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

## <span data-ttu-id="3e67f-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3e67f-109">PARAMETERS</span></span>

### <span data-ttu-id="3e67f-110">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="3e67f-110">-AccessPolicyObjectId</span></span>
<span data-ttu-id="3e67f-111">Lista identyfikatorów obiektów zasad programu Access.</span><span class="sxs-lookup"><span data-stu-id="3e67f-111">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="3e67f-112">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="3e67f-112">-AllowCorsCredential</span></span>
<span data-ttu-id="3e67f-113">HealthcareApis Fhir Service AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="3e67f-113">HealthcareApis Fhir Service AllowCorsCredential.</span></span>

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

### <span data-ttu-id="3e67f-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3e67f-114">-AsJob</span></span>
<span data-ttu-id="3e67f-115">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="3e67f-115">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="3e67f-116">-Odbiorca</span><span class="sxs-lookup"><span data-stu-id="3e67f-116">-Audience</span></span>
<span data-ttu-id="3e67f-117">HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="3e67f-117">HealthcareApis Fhir Service Audience.</span></span>

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

### <span data-ttu-id="3e67f-118">-Authority</span><span class="sxs-lookup"><span data-stu-id="3e67f-118">-Authority</span></span>
<span data-ttu-id="3e67f-119">HealthcareApis Fhir Service Authority.</span><span class="sxs-lookup"><span data-stu-id="3e67f-119">HealthcareApis Fhir Service Authority.</span></span>

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

### <span data-ttu-id="3e67f-120">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="3e67f-120">-CorsHeader</span></span>
<span data-ttu-id="3e67f-121">Lista usługi HealthcareApis Fhir nagłówka CORS.</span><span class="sxs-lookup"><span data-stu-id="3e67f-121">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="3e67f-122">Określ nagłówki HTTP, których można użyć podczas żądania.</span><span class="sxs-lookup"><span data-stu-id="3e67f-122">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="3e67f-123">Użyj znaku \* dla dowolnego nagłówka.</span><span class="sxs-lookup"><span data-stu-id="3e67f-123">Use \* for any header.</span></span>

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

### <span data-ttu-id="3e67f-124">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="3e67f-124">-CorsMaxAge</span></span>
<span data-ttu-id="3e67f-125">Maksymalny wiek usługi HealthcareApis Fhir service cors.</span><span class="sxs-lookup"><span data-stu-id="3e67f-125">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="3e67f-126">Określ, jak długo wynik żądania może być buforowany w sekundach.</span><span class="sxs-lookup"><span data-stu-id="3e67f-126">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="3e67f-127">Przykład: 600 oznacza 10 minut.</span><span class="sxs-lookup"><span data-stu-id="3e67f-127">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="3e67f-128">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="3e67f-128">-CorsMethod</span></span>
<span data-ttu-id="3e67f-129">HealthcareApis Fhir Service (lista) Metoda CORS.</span><span class="sxs-lookup"><span data-stu-id="3e67f-129">HealthcareApis Fhir Service List of Cors Method.</span></span>

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

### <span data-ttu-id="3e67f-130">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="3e67f-130">-CorsOrigin</span></span>
<span data-ttu-id="3e67f-131">HealthcareApis Fhir Service (lista pochodzenia CORS).</span><span class="sxs-lookup"><span data-stu-id="3e67f-131">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="3e67f-132">Określ adresy URL witryn pochodzących, które mogą uzyskiwać dostęp do tego interfejsu API, lub użyj znaku \*, aby zezwolić na dostęp z dowolnej witryny.</span><span class="sxs-lookup"><span data-stu-id="3e67f-132">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

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

### <span data-ttu-id="3e67f-133">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="3e67f-133">-CosmosOfferThroughput</span></span>
<span data-ttu-id="3e67f-134">HealthcareApis Fhir Service CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="3e67f-134">HealthcareApis Fhir Service CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="3e67f-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3e67f-135">-DefaultProfile</span></span>
<span data-ttu-id="3e67f-136">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3e67f-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3e67f-137">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="3e67f-137">-EnableSmartProxy</span></span>
<span data-ttu-id="3e67f-138">HealthcareApis Fhir Service EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="3e67f-138">HealthcareApis Fhir Service EnableSmartProxy.</span></span>

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

### <span data-ttu-id="3e67f-139">-ExportStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="3e67f-139">-ExportStorageAccountName</span></span>
<span data-ttu-id="3e67f-140">Usługa Fhir HealthcareApis eksportowanie nazwy konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="3e67f-140">HealthcareApis Fhir Service Export Storage Account Name.</span></span>

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

### <span data-ttu-id="3e67f-141">-FhirVersion</span><span class="sxs-lookup"><span data-stu-id="3e67f-141">-FhirVersion</span></span>
<span data-ttu-id="3e67f-142">Wersja Fhir.</span><span class="sxs-lookup"><span data-stu-id="3e67f-142">Fhir Version.</span></span>

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

### <span data-ttu-id="3e67f-143">-Kind</span><span class="sxs-lookup"><span data-stu-id="3e67f-143">-Kind</span></span>
<span data-ttu-id="3e67f-144">Rodzaj usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="3e67f-144">Kind of HealthcareApis Service.</span></span>
<span data-ttu-id="3e67f-145">Wartość domyślna to Fhir</span><span class="sxs-lookup"><span data-stu-id="3e67f-145">The default value is Fhir</span></span>

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

### <span data-ttu-id="3e67f-146">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3e67f-146">-Location</span></span>
<span data-ttu-id="3e67f-147">Lokalizacja usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="3e67f-147">HealthcareApis Service Location.</span></span>

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

### <span data-ttu-id="3e67f-148">-ManagedIdentity</span><span class="sxs-lookup"><span data-stu-id="3e67f-148">-ManagedIdentity</span></span>
<span data-ttu-id="3e67f-149">Użyć tożsamości zarządzanej?</span><span class="sxs-lookup"><span data-stu-id="3e67f-149">Use Managed Identity?</span></span>

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

### <span data-ttu-id="3e67f-150">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3e67f-150">-Name</span></span>
<span data-ttu-id="3e67f-151">Nazwa usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="3e67f-151">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="3e67f-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3e67f-152">-ResourceGroupName</span></span>
<span data-ttu-id="3e67f-153">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3e67f-153">Resource Group Name.</span></span>

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

### <span data-ttu-id="3e67f-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="3e67f-154">-Tag</span></span>
<span data-ttu-id="3e67f-155">Znaczniki kont usługi HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="3e67f-155">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="3e67f-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3e67f-156">-Confirm</span></span>
<span data-ttu-id="3e67f-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e67f-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3e67f-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3e67f-158">-WhatIf</span></span>
<span data-ttu-id="3e67f-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3e67f-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3e67f-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3e67f-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3e67f-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3e67f-161">CommonParameters</span></span>
<span data-ttu-id="3e67f-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3e67f-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3e67f-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3e67f-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3e67f-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3e67f-164">INPUTS</span></span>

### <span data-ttu-id="3e67f-165">System. String</span><span class="sxs-lookup"><span data-stu-id="3e67f-165">System.String</span></span>

## <span data-ttu-id="3e67f-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3e67f-166">OUTPUTS</span></span>

### <span data-ttu-id="3e67f-167">Microsoft. Azure. Commands. HealthcareApisService. models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="3e67f-167">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="3e67f-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3e67f-168">NOTES</span></span>

## <span data-ttu-id="3e67f-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3e67f-169">RELATED LINKS</span></span>
