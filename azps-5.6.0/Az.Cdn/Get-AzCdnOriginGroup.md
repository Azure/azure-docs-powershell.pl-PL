---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: f79b3b4e8347c485230141416461c1f320d3d7b4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996913"
---
# <span data-ttu-id="325eb-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="325eb-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="325eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="325eb-102">SYNOPSIS</span></span>
<span data-ttu-id="325eb-103">Pobiera grupę pochodzenia sieci CDN</span><span class="sxs-lookup"><span data-stu-id="325eb-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="325eb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="325eb-104">SYNTAX</span></span>

### <span data-ttu-id="325eb-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="325eb-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="325eb-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="325eb-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="325eb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="325eb-107">DESCRIPTION</span></span>
<span data-ttu-id="325eb-108">Polecenie Get-AzCdnOriginGroup pobiera grupę pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="325eb-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="325eb-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="325eb-109">EXAMPLES</span></span>

### <span data-ttu-id="325eb-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="325eb-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="325eb-111">To polecenie pobierze grupę pochodzenia w określonym punkcie końcowym.</span><span class="sxs-lookup"><span data-stu-id="325eb-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="325eb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="325eb-112">PARAMETERS</span></span>

### <span data-ttu-id="325eb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="325eb-113">-DefaultProfile</span></span>
<span data-ttu-id="325eb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="325eb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="325eb-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="325eb-115">-EndpointName</span></span>
<span data-ttu-id="325eb-116">Nazwa punktu końcowego sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="325eb-116">Azure CDN endpoint name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325eb-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="325eb-117">-OriginGroupName</span></span>
<span data-ttu-id="325eb-118">Nazwa grupy pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="325eb-118">Azure CDN origin group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325eb-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="325eb-119">-ProfileName</span></span>
<span data-ttu-id="325eb-120">Nazwa profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="325eb-120">Azure CDN profile name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325eb-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="325eb-121">-ResourceGroupName</span></span>
<span data-ttu-id="325eb-122">Grupa zasobów profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="325eb-122">The resource group of the Azure CDN profile.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFieldsParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325eb-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="325eb-123">-ResourceId</span></span>
<span data-ttu-id="325eb-124">Identyfikator zasobu dla grupy pochodzenia</span><span class="sxs-lookup"><span data-stu-id="325eb-124">Resource Id for the the origin group</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="325eb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="325eb-125">CommonParameters</span></span>
<span data-ttu-id="325eb-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="325eb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="325eb-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="325eb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="325eb-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="325eb-128">INPUTS</span></span>

### <span data-ttu-id="325eb-129">Brak</span><span class="sxs-lookup"><span data-stu-id="325eb-129">None</span></span>

## <span data-ttu-id="325eb-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="325eb-130">OUTPUTS</span></span>

### <span data-ttu-id="325eb-131">System.Object</span><span class="sxs-lookup"><span data-stu-id="325eb-131">System.Object</span></span>

## <span data-ttu-id="325eb-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="325eb-132">NOTES</span></span>

## <span data-ttu-id="325eb-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="325eb-133">RELATED LINKS</span></span>
