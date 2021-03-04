---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/update-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
ms.openlocfilehash: 119dec74416b8447d04aef7ae101016490408b5b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101951569"
---
# <span data-ttu-id="d3691-101">Update-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="d3691-101">Update-AzVirtualRouter</span></span>

## <span data-ttu-id="d3691-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3691-102">SYNOPSIS</span></span>
<span data-ttu-id="d3691-103">Aktualizuje router wirtualny.</span><span class="sxs-lookup"><span data-stu-id="d3691-103">Updates a Virtual Router.</span></span> 

## <span data-ttu-id="d3691-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d3691-104">SYNTAX</span></span>

### <span data-ttu-id="d3691-105">VirtualRouterNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d3691-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d3691-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="d3691-106">VirtualRouterResourceIdParameterSet</span></span>
```
Update-AzVirtualRouter [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d3691-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d3691-107">DESCRIPTION</span></span>
<span data-ttu-id="d3691-108">Aktualizuje router wirtualny, aby włączyć lub wyłączyć ruch gałęzi na rozgałęzienie.</span><span class="sxs-lookup"><span data-stu-id="d3691-108">Updates Virtual Router to enable or disable branch to branch traffic.</span></span>

## <span data-ttu-id="d3691-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d3691-109">EXAMPLES</span></span>

### <span data-ttu-id="d3691-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d3691-110">Example 1</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName -AllowBranchToBranchTraffic
```

<span data-ttu-id="d3691-111">Aktualizuje router wirtualny, aby umożliwić rozgałęzienie ruchu w rozgałęzieniach</span><span class="sxs-lookup"><span data-stu-id="d3691-111">Updates the Virtual Router to allow branch to branch traffic</span></span>

### <span data-ttu-id="d3691-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d3691-112">Example 2</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName
```

<span data-ttu-id="d3691-113">Aktualizuje router wirtualny w celu zablokowania ruchu gałęzi na rozgałęzienie</span><span class="sxs-lookup"><span data-stu-id="d3691-113">Updates the Virtual Router to block branch to branch traffic</span></span>

## <span data-ttu-id="d3691-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d3691-114">PARAMETERS</span></span>

### <span data-ttu-id="d3691-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="d3691-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="d3691-116">Oflaguj, aby zezwolić na ruch gałęzi na router wirtualny.</span><span class="sxs-lookup"><span data-stu-id="d3691-116">Flag to allow branch to branch traffic for virtual router.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3691-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3691-117">-DefaultProfile</span></span>
<span data-ttu-id="d3691-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d3691-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d3691-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3691-119">-ResourceGroupName</span></span>
<span data-ttu-id="d3691-120">Nazwa grupy zasobów routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="d3691-120">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3691-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d3691-121">-ResourceId</span></span>
<span data-ttu-id="d3691-122">ResourceId routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="d3691-122">ResourceId of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3691-123">-RouterName</span><span class="sxs-lookup"><span data-stu-id="d3691-123">-RouterName</span></span>
<span data-ttu-id="d3691-124">Nazwa routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="d3691-124">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d3691-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3691-125">CommonParameters</span></span>
<span data-ttu-id="d3691-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3691-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3691-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d3691-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3691-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3691-128">INPUTS</span></span>

### <span data-ttu-id="d3691-129">System.String</span><span class="sxs-lookup"><span data-stu-id="d3691-129">System.String</span></span>

## <span data-ttu-id="d3691-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d3691-130">OUTPUTS</span></span>

### <span data-ttu-id="d3691-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="d3691-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="d3691-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d3691-132">NOTES</span></span>

## <span data-ttu-id="d3691-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d3691-133">RELATED LINKS</span></span>
