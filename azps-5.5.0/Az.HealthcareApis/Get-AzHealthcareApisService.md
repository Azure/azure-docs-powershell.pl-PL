---
external help file: Microsoft.Azure.PowerShell.Cmdlets.HealthcareApis.dll-Help.xml
Module Name: Az.HealthcareApis
online version: https://docs.microsoft.com/en-us/powershell/module/az.healthcareapis/get-azhealthcareapisservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthcareApis/HealthcareApis/help/Get-AzHealthcareApisService.md
ms.openlocfilehash: 6d9c099457c25831d0ce97786b8d710cf4c0dc98
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200147"
---
# <span data-ttu-id="737f2-101">Get-AzHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="737f2-101">Get-AzHealthcareApisService</span></span>

## <span data-ttu-id="737f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="737f2-102">SYNOPSIS</span></span>
<span data-ttu-id="737f2-103">Pobierz metadane wystąpienia usługi.</span><span class="sxs-lookup"><span data-stu-id="737f2-103">Get the metadata of a service instance.</span></span>

## <span data-ttu-id="737f2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="737f2-104">SYNTAX</span></span>

### <span data-ttu-id="737f2-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="737f2-105">ListParameterSet (Default)</span></span>
```
Get-AzHealthcareApisService [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="737f2-106">ServiceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="737f2-106">ServiceNameParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="737f2-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="737f2-107">ResourceIdParameterSet</span></span>
```
Get-AzHealthcareApisService -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="737f2-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="737f2-108">DESCRIPTION</span></span>
<span data-ttu-id="737f2-109">Pobiera istniejące konta usług opieki zdrowotnej utworzone w ramach określonej subskrypcji lub grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="737f2-109">Gets existing healthcareApis fhir service accounts created within the specified subscription or a resource group.</span></span>

## <span data-ttu-id="737f2-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="737f2-110">EXAMPLES</span></span>

### <span data-ttu-id="737f2-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="737f2-111">Example 1</span></span>
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

### <span data-ttu-id="737f2-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="737f2-112">Example 2</span></span>

<span data-ttu-id="737f2-113">Pobiera metadane dla wszystkich usług HealthcareApis w podanej grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="737f2-113">Gets the metadata for all HealthcareApis services in the provided Resource Group.</span></span>

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

### <span data-ttu-id="737f2-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="737f2-114">Example 3</span></span>

<span data-ttu-id="737f2-115">Pobiera metadane dla wszystkich usług HealthcareApis w danej subskrypcji</span><span class="sxs-lookup"><span data-stu-id="737f2-115">Gets the metadata for all HealthcareApis services in the given subscription</span></span>

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

## <span data-ttu-id="737f2-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="737f2-116">PARAMETERS</span></span>

### <span data-ttu-id="737f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="737f2-117">-DefaultProfile</span></span>
<span data-ttu-id="737f2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="737f2-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="737f2-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="737f2-119">-Name</span></span>
<span data-ttu-id="737f2-120">Nazwa usługi HealthcareApis.</span><span class="sxs-lookup"><span data-stu-id="737f2-120">HealthcareApis Service Name.</span></span>

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

### <span data-ttu-id="737f2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="737f2-121">-ResourceGroupName</span></span>
<span data-ttu-id="737f2-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="737f2-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="737f2-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="737f2-123">-ResourceId</span></span>
<span data-ttu-id="737f2-124">Nazwa identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="737f2-124">Resource Id Name.</span></span>

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

### <span data-ttu-id="737f2-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="737f2-125">CommonParameters</span></span>
<span data-ttu-id="737f2-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="737f2-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="737f2-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="737f2-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="737f2-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="737f2-128">INPUTS</span></span>

### <span data-ttu-id="737f2-129">System.String</span><span class="sxs-lookup"><span data-stu-id="737f2-129">System.String</span></span>

## <span data-ttu-id="737f2-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="737f2-130">OUTPUTS</span></span>

### <span data-ttu-id="737f2-131">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span><span class="sxs-lookup"><span data-stu-id="737f2-131">Microsoft.Azure.Commands.HealthcareApis.Models.PSHealthcareApisService</span></span>

## <span data-ttu-id="737f2-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="737f2-132">NOTES</span></span>

## <span data-ttu-id="737f2-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="737f2-133">RELATED LINKS</span></span>
