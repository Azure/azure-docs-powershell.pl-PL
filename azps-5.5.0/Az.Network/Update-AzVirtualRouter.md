---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzVirtualRouter.md
ms.openlocfilehash: d7f52ded01ce5b785c1e935ba8d3ebf4b1c0a5fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193274"
---
# <span data-ttu-id="88b04-101">Update-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="88b04-101">Update-AzVirtualRouter</span></span>

## <span data-ttu-id="88b04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88b04-102">SYNOPSIS</span></span>
<span data-ttu-id="88b04-103">Aktualizuje router wirtualny.</span><span class="sxs-lookup"><span data-stu-id="88b04-103">Updates a Virtual Router.</span></span> 

## <span data-ttu-id="88b04-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="88b04-104">SYNTAX</span></span>

### <span data-ttu-id="88b04-105">VirtualRouterNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="88b04-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Update-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-AllowBranchToBranchTraffic]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88b04-106">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="88b04-106">VirtualRouterResourceIdParameterSet</span></span>
```
Update-AzVirtualRouter [-AllowBranchToBranchTraffic] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88b04-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="88b04-107">DESCRIPTION</span></span>
<span data-ttu-id="88b04-108">Aktualizuje router wirtualny, aby włączyć lub wyłączyć ruch gałęzi na rozgałęzienie.</span><span class="sxs-lookup"><span data-stu-id="88b04-108">Updates Virtual Router to enable or disable branch to branch traffic.</span></span>

## <span data-ttu-id="88b04-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="88b04-109">EXAMPLES</span></span>

### <span data-ttu-id="88b04-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="88b04-110">Example 1</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName -AllowBranchToBranchTraffic
```

<span data-ttu-id="88b04-111">Aktualizuje router wirtualny, aby umożliwić rozgałęzienie ruchu w rozgałęzieniach</span><span class="sxs-lookup"><span data-stu-id="88b04-111">Updates the Virtual Router to allow branch to branch traffic</span></span>

### <span data-ttu-id="88b04-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="88b04-112">Example 2</span></span>
```powershell
PS C:\> Update-AzVirtualRouter -ResourceGroupName $rgname -RouterName $virtualRouterName
```

<span data-ttu-id="88b04-113">Aktualizuje router wirtualny, aby zablokować ruch gałęzi do gałęzi</span><span class="sxs-lookup"><span data-stu-id="88b04-113">Updates the Virtual Router to block branch to branch traffic</span></span>

## <span data-ttu-id="88b04-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88b04-114">PARAMETERS</span></span>

### <span data-ttu-id="88b04-115">-AllowBranchToBranchTraffic</span><span class="sxs-lookup"><span data-stu-id="88b04-115">-AllowBranchToBranchTraffic</span></span>
<span data-ttu-id="88b04-116">Oflaguj, aby zezwolić na ruch gałęzi na router wirtualny.</span><span class="sxs-lookup"><span data-stu-id="88b04-116">Flag to allow branch to branch traffic for virtual router.</span></span>

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

### <span data-ttu-id="88b04-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b04-117">-DefaultProfile</span></span>
<span data-ttu-id="88b04-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="88b04-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="88b04-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88b04-119">-ResourceGroupName</span></span>
<span data-ttu-id="88b04-120">Nazwa grupy zasobów routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="88b04-120">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="88b04-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88b04-121">-ResourceId</span></span>
<span data-ttu-id="88b04-122">ResourceId routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="88b04-122">ResourceId of the virtual router.</span></span>

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

### <span data-ttu-id="88b04-123">-RouterName</span><span class="sxs-lookup"><span data-stu-id="88b04-123">-RouterName</span></span>
<span data-ttu-id="88b04-124">Nazwa routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="88b04-124">The name of the virtual router.</span></span>

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

### <span data-ttu-id="88b04-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b04-125">CommonParameters</span></span>
<span data-ttu-id="88b04-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88b04-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b04-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88b04-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b04-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88b04-128">INPUTS</span></span>

### <span data-ttu-id="88b04-129">System.String</span><span class="sxs-lookup"><span data-stu-id="88b04-129">System.String</span></span>

## <span data-ttu-id="88b04-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88b04-130">OUTPUTS</span></span>

### <span data-ttu-id="88b04-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="88b04-131">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="88b04-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="88b04-132">NOTES</span></span>

## <span data-ttu-id="88b04-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88b04-133">RELATED LINKS</span></span>
