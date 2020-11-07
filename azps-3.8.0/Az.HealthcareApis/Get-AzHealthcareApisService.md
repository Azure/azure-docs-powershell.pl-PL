---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/get-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
ms.openlocfilehash: d1a6edc3365631f93d2bc3b7a0e153ec360c2611
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894437"
---
# <span data-ttu-id="b8d3b-101">Get-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="b8d3b-101">Get-AzHealthcareApisService</span></span>

## <span data-ttu-id="b8d3b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b8d3b-102">SYNOPSIS</span></span>
<span data-ttu-id="b8d3b-103">Uzyskiwanie metadanych wystąpienia usługi.</span><span class="sxs-lookup"><span data-stu-id="b8d3b-103">Get the metadata of a service instance.</span></span>

## <span data-ttu-id="b8d3b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b8d3b-104">SYNTAX</span></span>

### <span data-ttu-id="b8d3b-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b8d3b-105">ListParameterSet (Default)</span></span>
```
Get-AzHealthcareApisService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b8d3b-106">ServiceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8d3b-106">ServiceNameParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b8d3b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b8d3b-107">ResourceIdParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b8d3b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b8d3b-108">DESCRIPTION</span></span>
<span data-ttu-id="b8d3b-109">Umożliwia pobieranie istniejących kont usługi healthcareApis fhir utworzonych w ramach określonej subskrypcji lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b8d3b-109">Gets existing healthcareApis fhir service accounts created within the specified subscription or a resource group.</span></span>

## <span data-ttu-id="b8d3b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b8d3b-110">EXAMPLES</span></span>

### <span data-ttu-id="b8d3b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b8d3b-111">Example 1</span></span>
```powershell
PS C:\> Get-AzHealthcareApisService -Name "MyService" -ResourceGroupName "MyResourceGroup"

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

### <span data-ttu-id="b8d3b-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b8d3b-112">Example 2</span></span>

<span data-ttu-id="b8d3b-113">Pobiera metadane wszystkich usług HealthcareApis w podanej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="b8d3b-113">Gets the metadata for all HealthcareApis services in the provided Resource Group.</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService -ResourceGroupName "MyResourceGroup"

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
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

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

### <span data-ttu-id="b8d3b-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="b8d3b-114">Example 3</span></span>

<span data-ttu-id="b8d3b-115">Pobiera metadane wszystkich usług HealthcareApis w danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b8d3b-115">Gets the metadata for all HealthcareApis services in the given subscription</span></span>

```powershell
PS C:\> Get-AzHealthcareApisService

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db48
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

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbOfferThroughput : 400
Etag                    : "00000000-0000-0000-0000-000000000000"
Id                      : /subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MyResourceGroup/providers/Microsoft
                          .HealthcareApis/services/MyService1
Kind                    : fhir-R4
Location                : westus2
Name                    : MyService1
ResourceGroupName       : MyResourceGroup
Tags                    : {}
ResourceType            : Microsoft.HealthcareApis/services
SmartProxyEnabled       : False
```

## <span data-ttu-id="b8d3b-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b8d3b-116">PARAMETERS</span></span>

### <span data-ttu-id="b8d3b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8d3b-117">-DefaultProfile</span></span>
<span data-ttu-id="b8d3b-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8d3b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b8d3b-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b8d3b-119">-Name</span></span>
<span data-ttu-id="b8d3b-120">Nazwa usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="b8d3b-120">HealthcareApis Service Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceNameParameterSet
Aliases: HealthcareApisName, FhirServiceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b8d3b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b8d3b-121">-ResourceGroupName</span></span>
<span data-ttu-id="b8d3b-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b8d3b-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

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

### <span data-ttu-id="b8d3b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8d3b-123">-ResourceId</span></span>
<span data-ttu-id="b8d3b-124">Nazwa identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="b8d3b-124">Resource Id Name.</span></span>

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

### <span data-ttu-id="b8d3b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8d3b-125">CommonParameters</span></span>
<span data-ttu-id="b8d3b-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8d3b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8d3b-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b8d3b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8d3b-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8d3b-128">INPUTS</span></span>

### <span data-ttu-id="b8d3b-129">System. String</span><span class="sxs-lookup"><span data-stu-id="b8d3b-129">System.String</span></span>

## <span data-ttu-id="b8d3b-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b8d3b-130">OUTPUTS</span></span>

### <span data-ttu-id="b8d3b-131">Microsoft. Azure. Commands. HealthcareApisService. models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="b8d3b-131">Microsoft.Azure.Commands.HealthcareApisService.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="b8d3b-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b8d3b-132">NOTES</span></span>

## <span data-ttu-id="b8d3b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8d3b-133">RELATED LINKS</span></span>
