---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/get-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
ms.openlocfilehash: 6d9c099457c25831d0ce97786b8d710cf4c0dc98
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98500947"
---
# <span data-ttu-id="7b1ca-101">Get-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="7b1ca-101">Get-AzHealthcareApisService</span></span>

## <span data-ttu-id="7b1ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7b1ca-102">SYNOPSIS</span></span>
<span data-ttu-id="7b1ca-103">Uzyskiwanie metadanych wystąpienia usługi.</span><span class="sxs-lookup"><span data-stu-id="7b1ca-103">Get the metadata of a service instance.</span></span>

## <span data-ttu-id="7b1ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7b1ca-104">SYNTAX</span></span>

### <span data-ttu-id="7b1ca-105">ListParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7b1ca-105">ListParameterSet (Default)</span></span>
```
Get-AzHealthcareApisService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7b1ca-106">ServiceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b1ca-106">ServiceNameParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b1ca-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b1ca-107">ResourceIdParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b1ca-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7b1ca-108">DESCRIPTION</span></span>
<span data-ttu-id="7b1ca-109">Umożliwia pobieranie istniejących kont usługi healthcareApis fhir utworzonych w ramach określonej subskrypcji lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b1ca-109">Gets existing healthcareApis fhir service accounts created within the specified subscription or a resource group.</span></span>

## <span data-ttu-id="7b1ca-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7b1ca-110">EXAMPLES</span></span>

### <span data-ttu-id="7b1ca-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7b1ca-111">Example 1</span></span>
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

### <span data-ttu-id="7b1ca-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7b1ca-112">Example 2</span></span>

<span data-ttu-id="7b1ca-113">Pobiera metadane wszystkich usług HealthcareApis w podanej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b1ca-113">Gets the metadata for all HealthcareApis services in the provided Resource Group.</span></span>

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

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  :
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

### <span data-ttu-id="7b1ca-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="7b1ca-114">Example 3</span></span>

<span data-ttu-id="7b1ca-115">Pobiera metadane wszystkich usług HealthcareApis w danej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7b1ca-115">Gets the metadata for all HealthcareApis services in the given subscription</span></span>

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

AccessPolicies          : {77777777-6666-5555-4444-1111111111111}
Audience                : https://azurehealthcareapis.com
Authority               : https://login.microsoftonline.com/72f988bf-86f1-41af-91ab-2d7cd011db478
CorsAllowCredentials    : False
CorsHeaders             : {}
CorsMaxAge              : 0
CorsMethods             : {}
CorsOrigins             : {}
CosmosDbKeyVaultKeyUri  :
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

## <span data-ttu-id="7b1ca-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7b1ca-116">PARAMETERS</span></span>

### <span data-ttu-id="7b1ca-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b1ca-117">-DefaultProfile</span></span>
<span data-ttu-id="7b1ca-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7b1ca-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b1ca-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7b1ca-119">-Name</span></span>
<span data-ttu-id="7b1ca-120">Nazwa usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="7b1ca-120">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="7b1ca-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b1ca-121">-ResourceGroupName</span></span>
<span data-ttu-id="7b1ca-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7b1ca-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="7b1ca-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b1ca-123">-ResourceId</span></span>
<span data-ttu-id="7b1ca-124">Nazwa identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="7b1ca-124">Resource Id Name.</span></span>

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

### <span data-ttu-id="7b1ca-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b1ca-125">CommonParameters</span></span>
<span data-ttu-id="7b1ca-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b1ca-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b1ca-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7b1ca-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b1ca-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b1ca-128">INPUTS</span></span>

### <span data-ttu-id="7b1ca-129">System. String</span><span class="sxs-lookup"><span data-stu-id="7b1ca-129">System.String</span></span>

## <span data-ttu-id="7b1ca-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7b1ca-130">OUTPUTS</span></span>

### <span data-ttu-id="7b1ca-131">Microsoft. Azure. Commands. HealthcareApis. models. PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="7b1ca-131">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="7b1ca-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7b1ca-132">NOTES</span></span>

## <span data-ttu-id="7b1ca-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b1ca-133">RELATED LINKS</span></span>
