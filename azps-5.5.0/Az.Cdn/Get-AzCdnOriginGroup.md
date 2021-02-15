---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Cdn.dll-Help.xml
Module Name: Az.Cdn
online version: https://docs.microsoft.com/en-us/powershell/module/az.cdn/get-azcdnorigingroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Cdn/Cdn/help/Get-AzCdnOriginGroup.md
ms.openlocfilehash: 98c41f8e9e1592cf0405f42701fc19f3badd9553
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239130"
---
# <span data-ttu-id="d3d8b-101">Get-AzCdnOriginGroup</span><span class="sxs-lookup"><span data-stu-id="d3d8b-101">Get-AzCdnOriginGroup</span></span>

## <span data-ttu-id="d3d8b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3d8b-102">SYNOPSIS</span></span>
<span data-ttu-id="d3d8b-103">Pobiera grupę pochodzenia sieci CDN</span><span class="sxs-lookup"><span data-stu-id="d3d8b-103">Gets a CDN origin group</span></span>

## <span data-ttu-id="d3d8b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d3d8b-104">SYNTAX</span></span>

### <span data-ttu-id="d3d8b-105">ByFieldsParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d3d8b-105">ByFieldsParameterSet (Default)</span></span>
```
Get-AzCdnOriginGroup -EndpointName <String> -OriginGroupName <String> -ProfileName <String>
 -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3d8b-106">ByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3d8b-106">ByResourceIdParameterSet</span></span>
```
Get-AzCdnOriginGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3d8b-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d3d8b-107">DESCRIPTION</span></span>
<span data-ttu-id="d3d8b-108">Polecenie Get-AzCdnOriginGroup pobiera grupę pochodzenia sieci CDN.</span><span class="sxs-lookup"><span data-stu-id="d3d8b-108">The Get-AzCdnOriginGroup cmdlet retrieves a CDN origin group.</span></span>

## <span data-ttu-id="d3d8b-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d3d8b-109">EXAMPLES</span></span>

### <span data-ttu-id="d3d8b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d3d8b-110">Example 1</span></span>
```powershell
PS C:\> Get-AzCdnOriginGroup -ResourceGroupName $resourceGroupName -ProfileName $profileName -EndpointName $endpointName -OriginGroupName $originGroupName
```

<span data-ttu-id="d3d8b-111">To polecenie pobierze grupę pochodzenia w określonym punkcie końcowym.</span><span class="sxs-lookup"><span data-stu-id="d3d8b-111">This command will get the origin group within the specified endpoint.</span></span>

## <span data-ttu-id="d3d8b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3d8b-112">PARAMETERS</span></span>

### <span data-ttu-id="d3d8b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3d8b-113">-DefaultProfile</span></span>
<span data-ttu-id="d3d8b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3d8b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d3d8b-115">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="d3d8b-115">-EndpointName</span></span>
<span data-ttu-id="d3d8b-116">Nazwa punktu końcowego sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="d3d8b-116">Azure CDN endpoint name.</span></span>

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

### <span data-ttu-id="d3d8b-117">-OriginGroupName</span><span class="sxs-lookup"><span data-stu-id="d3d8b-117">-OriginGroupName</span></span>
<span data-ttu-id="d3d8b-118">Nazwa grupy pochodzenia sieci Azure CDN.</span><span class="sxs-lookup"><span data-stu-id="d3d8b-118">Azure CDN origin group name.</span></span>

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

### <span data-ttu-id="d3d8b-119">-ProfileName</span><span class="sxs-lookup"><span data-stu-id="d3d8b-119">-ProfileName</span></span>
<span data-ttu-id="d3d8b-120">Nazwa profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="d3d8b-120">Azure CDN profile name.</span></span>

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

### <span data-ttu-id="d3d8b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3d8b-121">-ResourceGroupName</span></span>
<span data-ttu-id="d3d8b-122">Grupa zasobów profilu azure CDN.</span><span class="sxs-lookup"><span data-stu-id="d3d8b-122">The resource group of the Azure CDN profile.</span></span>

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

### <span data-ttu-id="d3d8b-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3d8b-123">-ResourceId</span></span>
<span data-ttu-id="d3d8b-124">Identyfikator zasobu dla grupy pochodzenia</span><span class="sxs-lookup"><span data-stu-id="d3d8b-124">Resource Id for the the origin group</span></span>

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

### <span data-ttu-id="d3d8b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3d8b-125">CommonParameters</span></span>
<span data-ttu-id="d3d8b-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3d8b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3d8b-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3d8b-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3d8b-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3d8b-128">INPUTS</span></span>

### <span data-ttu-id="d3d8b-129">Brak</span><span class="sxs-lookup"><span data-stu-id="d3d8b-129">None</span></span>

## <span data-ttu-id="d3d8b-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d3d8b-130">OUTPUTS</span></span>

### <span data-ttu-id="d3d8b-131">System.Object</span><span class="sxs-lookup"><span data-stu-id="d3d8b-131">System.Object</span></span>

## <span data-ttu-id="d3d8b-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d3d8b-132">NOTES</span></span>

## <span data-ttu-id="d3d8b-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3d8b-133">RELATED LINKS</span></span>
