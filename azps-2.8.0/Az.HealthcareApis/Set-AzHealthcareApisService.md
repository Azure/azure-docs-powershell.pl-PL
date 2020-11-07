---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/set-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Set-AzHealthcareApisService.md
ms.openlocfilehash: 36632398d95acdd16d2a7b41c09bed7172391639
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705276"
---
# <span data-ttu-id="7fcb5-101">Set-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="7fcb5-101">Set-AzHealthcareApisService</span></span>

## <span data-ttu-id="7fcb5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7fcb5-102">SYNOPSIS</span></span>
<span data-ttu-id="7fcb5-103">Umożliwia zaktualizowanie istniejącej usługi healthcareApis fhir.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-103">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="7fcb5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7fcb5-104">SYNTAX</span></span>

### <span data-ttu-id="7fcb5-105">ServiceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7fcb5-105">ServiceNameParameterSet (Default)</span></span>
```
Set-AzHealthcareApisService -Name <String> -ResourceGroupName <String> [-CosmosOfferThroughput <Int32>]
 [-Authority <String>] [-Audience <String>] [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>]
 [-CorsHeader <String[]>] [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential]
 [-DisableCorsCredential] [-AccessPolicyObjectId <String[]>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fcb5-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fcb5-106">ResourceIdParameterSet</span></span>
```
Set-AzHealthcareApisService [-CosmosOfferThroughput <Int32>] [-Authority <String>] [-Audience <String>]
 [-EnableSmartProxy] [-DisableSmartProxy] [-CorsOrigin <String[]>] [-CorsHeader <String[]>]
 [-CorsMethod <String[]>] [-CorsMaxAge <Int32>] [-AllowCorsCredential] [-DisableCorsCredential]
 [-AccessPolicyObjectId <String[]>] [-Tag <Hashtable>] -ResourceId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7fcb5-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7fcb5-107">InputObjectParameterSet</span></span>
```
Set-AzHealthcareApisService -InputObject <PSHealthcareApisService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7fcb5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7fcb5-108">DESCRIPTION</span></span>
<span data-ttu-id="7fcb5-109">Umożliwia zaktualizowanie istniejącej usługi healthcareApis fhir.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-109">Updates an existing healthcareApis fhir service.</span></span>

## <span data-ttu-id="7fcb5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7fcb5-110">EXAMPLES</span></span>

### <span data-ttu-id="7fcb5-111">Przykład 1: umożliwia zaktualizowanie istniejącej usługi healthcareapis o nazwie Moja usługa w grupie zasobu moja grupa zasobów przy użyciu cosmosdb OfferThroughputd = 500.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-111">Example 1 : Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

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

### <span data-ttu-id="7fcb5-112">Przykład 2: umożliwia zaktualizowanie istniejącej usługi healthcareapis o nazwie Moja usługa w grupie zasobu moja grupa zasobów przy użyciu cosmosdb OfferThroughputd = 500.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-112">Example 2: Updates the existing healthcareapis service named MyService in the resource group MyResourceGroup  with the cosmosdb OfferThroughput = 500.</span></span>

```powershell
PS C:\> $ResourceId = "/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/MyResourceGroup/providers/Microsoft.HealthcareApis/services/MyService"
PS C:\> Set-AzHealthcareApisService -ResourceId $ResourceId  -CosmosOfferThroughput 500

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db47
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
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

## <span data-ttu-id="7fcb5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7fcb5-113">PARAMETERS</span></span>

### <span data-ttu-id="7fcb5-114">-AccessPolicyObjectId</span><span class="sxs-lookup"><span data-stu-id="7fcb5-114">-AccessPolicyObjectId</span></span>
<span data-ttu-id="7fcb5-115">Lista identyfikatorów obiektów zasad programu Access.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-115">List of Access Policy Object IDs.</span></span>

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

### <span data-ttu-id="7fcb5-116">-AllowCorsCredential</span><span class="sxs-lookup"><span data-stu-id="7fcb5-116">-AllowCorsCredential</span></span>
<span data-ttu-id="7fcb5-117">HealthcareApis FhirService AllowCorsCredential.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-117">HealthcareApis FhirService AllowCorsCredential.</span></span>

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

### <span data-ttu-id="7fcb5-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7fcb5-118">-AsJob</span></span>
<span data-ttu-id="7fcb5-119">Uruchom polecenie cmdlet jako zadanie w tle.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-119">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="7fcb5-120">-Odbiorca</span><span class="sxs-lookup"><span data-stu-id="7fcb5-120">-Audience</span></span>
<span data-ttu-id="7fcb5-121">HealthcareApis FhirService odbiorców.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-121">HealthcareApis FhirService Audience.</span></span>

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

### <span data-ttu-id="7fcb5-122">-Authority</span><span class="sxs-lookup"><span data-stu-id="7fcb5-122">-Authority</span></span>
<span data-ttu-id="7fcb5-123">HealthcareApis FhirService Authority.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-123">HealthcareApis FhirService Authority.</span></span>

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

### <span data-ttu-id="7fcb5-124">-CorsHeader</span><span class="sxs-lookup"><span data-stu-id="7fcb5-124">-CorsHeader</span></span>
<span data-ttu-id="7fcb5-125">Lista usługi HealthcareApis Fhir nagłówka CORS.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-125">HealthcareApis Fhir Service List of Cors Header.</span></span> <span data-ttu-id="7fcb5-126">Określ nagłówki HTTP, których można użyć podczas żądania.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-126">Specify HTTP headers which can be used during the request.</span></span> <span data-ttu-id="7fcb5-127">Użyj znaku \* dla dowolnego nagłówka.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-127">Use \* for any header.</span></span>

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

### <span data-ttu-id="7fcb5-128">-CorsMaxAge</span><span class="sxs-lookup"><span data-stu-id="7fcb5-128">-CorsMaxAge</span></span>
<span data-ttu-id="7fcb5-129">Maksymalny wiek usługi HealthcareApis Fhir service cors.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-129">HealthcareApis Fhir Service Cors Max Age.</span></span> <span data-ttu-id="7fcb5-130">Określ, jak długo wynik żądania może być buforowany w sekundach.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-130">Specify how long a result from a request can be cached in seconds.</span></span> <span data-ttu-id="7fcb5-131">Przykład: 600 oznacza 10 minut.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-131">Example: 600 means 10 minutes.</span></span>

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

### <span data-ttu-id="7fcb5-132">-CorsMethod</span><span class="sxs-lookup"><span data-stu-id="7fcb5-132">-CorsMethod</span></span>
<span data-ttu-id="7fcb5-133">HealthcareApis FhirService listą metod CORS.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-133">HealthcareApis FhirService List of Cors Methods.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ServiceNameParameterSet, ResourceIdParameterSet
Aliases:
Accepted values: DELETE, GET, OPTIONS, PATCH, POST, PUT

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fcb5-134">-CorsOrigin</span><span class="sxs-lookup"><span data-stu-id="7fcb5-134">-CorsOrigin</span></span>
<span data-ttu-id="7fcb5-135">HealthcareApis FhirService lista pochodzenia CORS.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-135">HealthcareApis FhirService List of Cors Origins.</span></span> <span data-ttu-id="7fcb5-136">HealthcareApis Fhir Service (lista pochodzenia CORS).</span><span class="sxs-lookup"><span data-stu-id="7fcb5-136">HealthcareApis Fhir Service List of Cors Origin.</span></span> <span data-ttu-id="7fcb5-137">Określ adresy URL witryn pochodzących, które mogą uzyskiwać dostęp do tego interfejsu API, lub użyj znaku \*, aby zezwolić na dostęp z dowolnej witryny.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-137">Specify URLs of origin sites that can access this API, or use \* to allow access from any site.</span></span>

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

### <span data-ttu-id="7fcb5-138">-CosmosOfferThroughput</span><span class="sxs-lookup"><span data-stu-id="7fcb5-138">-CosmosOfferThroughput</span></span>
<span data-ttu-id="7fcb5-139">HealthcareApis FhirService CosmosOfferThroughput.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-139">HealthcareApis FhirService CosmosOfferThroughput.</span></span>

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

### <span data-ttu-id="7fcb5-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fcb5-140">-DefaultProfile</span></span>
<span data-ttu-id="7fcb5-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fcb5-142">-DisableCorsCredential</span><span class="sxs-lookup"><span data-stu-id="7fcb5-142">-DisableCorsCredential</span></span>
<span data-ttu-id="7fcb5-143">HealthcareApis FhirService CorsCredentials nie jest dozwolone.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-143">HealthcareApis FhirService CorsCredentials Not Allowed.</span></span>

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

### <span data-ttu-id="7fcb5-144">-DisableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="7fcb5-144">-DisableSmartProxy</span></span>
<span data-ttu-id="7fcb5-145">HealthcareApis FhirService DisableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-145">HealthcareApis FhirService DisableSmartProxy.</span></span>

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

### <span data-ttu-id="7fcb5-146">-EnableSmartProxy</span><span class="sxs-lookup"><span data-stu-id="7fcb5-146">-EnableSmartProxy</span></span>
<span data-ttu-id="7fcb5-147">HealthcareApis FhirService EnableSmartProxy.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-147">HealthcareApis FhirService EnableSmartProxy.</span></span>

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

### <span data-ttu-id="7fcb5-148">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7fcb5-148">-InputObject</span></span>
<span data-ttu-id="7fcb5-149">Usługa fhir HealthcareApis pozostała w potoku od get-AzHealthcareApisFhirService.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-149">HealthcareApis fhir service piped from Get-AzHealthcareApisFhirService.</span></span>

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

### <span data-ttu-id="7fcb5-150">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7fcb5-150">-Name</span></span>
<span data-ttu-id="7fcb5-151">Nazwa usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-151">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="7fcb5-152">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fcb5-152">-ResourceGroupName</span></span>
<span data-ttu-id="7fcb5-153">Nazwa grupy zasobów usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-153">HealthcareApis Service Resource Group Name.</span></span>

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

### <span data-ttu-id="7fcb5-154">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7fcb5-154">-ResourceId</span></span>
<span data-ttu-id="7fcb5-155">Identyfikator zasobu usługi Fhir HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-155">HealthcareApis Fhir Service ResourceId.</span></span>

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

### <span data-ttu-id="7fcb5-156">-Tag</span><span class="sxs-lookup"><span data-stu-id="7fcb5-156">-Tag</span></span>
<span data-ttu-id="7fcb5-157">Znaczniki kont usługi HealthcareApis Fhir.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-157">HealthcareApis Fhir Service Account Tags.</span></span>

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

### <span data-ttu-id="7fcb5-158">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7fcb5-158">-Confirm</span></span>
<span data-ttu-id="7fcb5-159">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-159">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fcb5-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fcb5-160">-WhatIf</span></span>
<span data-ttu-id="7fcb5-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fcb5-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-162">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fcb5-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fcb5-163">CommonParameters</span></span>
<span data-ttu-id="7fcb5-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fcb5-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fcb5-165">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7fcb5-165">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fcb5-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7fcb5-166">INPUTS</span></span>

### <span data-ttu-id="7fcb5-167">System. String</span><span class="sxs-lookup"><span data-stu-id="7fcb5-167">System.String</span></span>

### <span data-ttu-id="7fcb5-168">Microsoft. Azure. Commands. HealthcareApisService. models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="7fcb5-168">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="7fcb5-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7fcb5-169">OUTPUTS</span></span>

### <span data-ttu-id="7fcb5-170">Microsoft. Azure. Commands. HealthcareApisService. models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="7fcb5-170">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="7fcb5-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7fcb5-171">NOTES</span></span>

## <span data-ttu-id="7fcb5-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7fcb5-172">RELATED LINKS</span></span>