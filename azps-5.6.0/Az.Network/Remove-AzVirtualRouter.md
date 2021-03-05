---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
ms.openlocfilehash: 6def67720ee11a2057267845ef458d0759aec589
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102005937"
---
# <span data-ttu-id="f17d0-101">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="f17d0-101">Remove-AzVirtualRouter</span></span>

## <span data-ttu-id="f17d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f17d0-102">SYNOPSIS</span></span>
<span data-ttu-id="f17d0-103">Usuwa wirtualny przekierowy azure.</span><span class="sxs-lookup"><span data-stu-id="f17d0-103">Deletes an Azure VirtualRouter.</span></span>

## <span data-ttu-id="f17d0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f17d0-104">SYNTAX</span></span>

### <span data-ttu-id="f17d0-105">VirtualRouterNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f17d0-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f17d0-106">VirtualRouterInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f17d0-106">VirtualRouterInputObjectParameterSet</span></span>
```
Remove-AzVirtualRouter -InputObject <PSVirtualRouter> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f17d0-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f17d0-107">VirtualRouterResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouter -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f17d0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="f17d0-108">DESCRIPTION</span></span>
<span data-ttu-id="f17d0-109">Polecenie **cmdlet Remove-AzVirtualRouter** usuwa element Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="f17d0-109">The **Remove-AzVirtualRouter** cmdlet deletes an Azure VirtualRouter</span></span>

## <span data-ttu-id="f17d0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f17d0-110">EXAMPLES</span></span>

### <span data-ttu-id="f17d0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f17d0-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="f17d0-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f17d0-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Remove-AzVirtualRouter -ResourceId $virtualRouterId
```

### <span data-ttu-id="f17d0-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="f17d0-113">Example 3</span></span>
```powershell
$virtualRouter = Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
Remove-AzVirtualRouter -InputObject $virtualRouter
```

## <span data-ttu-id="f17d0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f17d0-114">PARAMETERS</span></span>

### <span data-ttu-id="f17d0-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="f17d0-115">-AsJob</span></span>
<span data-ttu-id="f17d0-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f17d0-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f17d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f17d0-117">-DefaultProfile</span></span>
<span data-ttu-id="f17d0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f17d0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f17d0-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="f17d0-119">-Force</span></span>
<span data-ttu-id="f17d0-120">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="f17d0-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f17d0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f17d0-121">-InputObject</span></span>
<span data-ttu-id="f17d0-122">Obiekt wejściowy routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="f17d0-122">The virtual router input object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualRouter
Parameter Sets: VirtualRouterInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f17d0-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f17d0-123">-PassThru</span></span>
<span data-ttu-id="f17d0-124">Zwraca obiekt reprezentujący element, na którym jest wykonywana ta operacja.</span><span class="sxs-lookup"><span data-stu-id="f17d0-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="f17d0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f17d0-125">-ResourceGroupName</span></span>
<span data-ttu-id="f17d0-126">Nazwa grupy zasobów routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="f17d0-126">The resource group name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f17d0-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f17d0-127">-ResourceId</span></span>
<span data-ttu-id="f17d0-128">Identyfikator zasobu routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="f17d0-128">The virtual router resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f17d0-129">-RouterName</span><span class="sxs-lookup"><span data-stu-id="f17d0-129">-RouterName</span></span>
<span data-ttu-id="f17d0-130">Nazwa routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="f17d0-130">The name of the virtual router.</span></span>

```yaml
Type: System.String
Parameter Sets: VirtualRouterNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f17d0-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f17d0-131">-Confirm</span></span>
<span data-ttu-id="f17d0-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f17d0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f17d0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f17d0-133">-WhatIf</span></span>
<span data-ttu-id="f17d0-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f17d0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f17d0-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="f17d0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f17d0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f17d0-136">CommonParameters</span></span>
<span data-ttu-id="f17d0-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f17d0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f17d0-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f17d0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f17d0-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f17d0-139">INPUTS</span></span>

### <span data-ttu-id="f17d0-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f17d0-140">System.String</span></span>

### <span data-ttu-id="f17d0-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="f17d0-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="f17d0-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f17d0-142">OUTPUTS</span></span>

### <span data-ttu-id="f17d0-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f17d0-143">System.Boolean</span></span>

## <span data-ttu-id="f17d0-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f17d0-144">NOTES</span></span>

## <span data-ttu-id="f17d0-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f17d0-145">RELATED LINKS</span></span>
