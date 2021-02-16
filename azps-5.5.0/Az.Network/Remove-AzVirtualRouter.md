---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualRouter.md
ms.openlocfilehash: 691abfe3f6ca58e1fbef6c1120ce13b64fd62566
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193434"
---
# <span data-ttu-id="6fe17-101">Remove-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="6fe17-101">Remove-AzVirtualRouter</span></span>

## <span data-ttu-id="6fe17-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fe17-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe17-103">Usuwa wirtualny przekierowy azure.</span><span class="sxs-lookup"><span data-stu-id="6fe17-103">Deletes an Azure VirtualRouter.</span></span>

## <span data-ttu-id="6fe17-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6fe17-104">SYNTAX</span></span>

### <span data-ttu-id="6fe17-105">VirtualRouterNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6fe17-105">VirtualRouterNameParameterSet (Default)</span></span>
```
Remove-AzVirtualRouter -ResourceGroupName <String> -RouterName <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fe17-106">VirtualRouterInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fe17-106">VirtualRouterInputObjectParameterSet</span></span>
```
Remove-AzVirtualRouter -InputObject <PSVirtualRouter> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6fe17-107">VirtualRouterResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fe17-107">VirtualRouterResourceIdParameterSet</span></span>
```
Remove-AzVirtualRouter -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6fe17-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6fe17-108">DESCRIPTION</span></span>
<span data-ttu-id="6fe17-109">Polecenie **cmdlet Remove-AzVirtualRouter** usuwa element Azure VirtualRouter</span><span class="sxs-lookup"><span data-stu-id="6fe17-109">The **Remove-AzVirtualRouter** cmdlet deletes an Azure VirtualRouter</span></span>

## <span data-ttu-id="6fe17-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6fe17-110">EXAMPLES</span></span>

### <span data-ttu-id="6fe17-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6fe17-111">Example 1</span></span>
```powershell
Remove-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
```

### <span data-ttu-id="6fe17-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6fe17-112">Example 2</span></span>
```powershell
$virtualRouterId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualRouters/virtualRouter'
Remove-AzVirtualRouter -ResourceId $virtualRouterId
```

### <span data-ttu-id="6fe17-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="6fe17-113">Example 3</span></span>
```powershell
$virtualRouter = Get-AzVirtualRouter -ResourceGroupName virtualRouterRG -RouterName virtualRouter
Remove-AzVirtualRouter -InputObject $virtualRouter
```

## <span data-ttu-id="6fe17-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fe17-114">PARAMETERS</span></span>

### <span data-ttu-id="6fe17-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="6fe17-115">-AsJob</span></span>
<span data-ttu-id="6fe17-116">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6fe17-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6fe17-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fe17-117">-DefaultProfile</span></span>
<span data-ttu-id="6fe17-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fe17-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fe17-119">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="6fe17-119">-Force</span></span>
<span data-ttu-id="6fe17-120">Nie pytaj o potwierdzenie, jeśli chcesz zastąpić zasób</span><span class="sxs-lookup"><span data-stu-id="6fe17-120">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6fe17-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6fe17-121">-InputObject</span></span>
<span data-ttu-id="6fe17-122">Obiekt wejściowy routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="6fe17-122">The virtual router input object.</span></span>

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

### <span data-ttu-id="6fe17-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6fe17-123">-PassThru</span></span>
<span data-ttu-id="6fe17-124">Zwraca obiekt reprezentujący element, na którym jest wykonywana ta operacja.</span><span class="sxs-lookup"><span data-stu-id="6fe17-124">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="6fe17-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fe17-125">-ResourceGroupName</span></span>
<span data-ttu-id="6fe17-126">Nazwa grupy zasobów routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="6fe17-126">The resource group name of the virtual router.</span></span>

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

### <span data-ttu-id="6fe17-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6fe17-127">-ResourceId</span></span>
<span data-ttu-id="6fe17-128">Identyfikator zasobu routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="6fe17-128">The virtual router resource Id.</span></span>

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

### <span data-ttu-id="6fe17-129">-RouterName</span><span class="sxs-lookup"><span data-stu-id="6fe17-129">-RouterName</span></span>
<span data-ttu-id="6fe17-130">Nazwa routera wirtualnego.</span><span class="sxs-lookup"><span data-stu-id="6fe17-130">The name of the virtual router.</span></span>

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

### <span data-ttu-id="6fe17-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6fe17-131">-Confirm</span></span>
<span data-ttu-id="6fe17-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6fe17-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fe17-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fe17-133">-WhatIf</span></span>
<span data-ttu-id="6fe17-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6fe17-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fe17-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6fe17-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fe17-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe17-136">CommonParameters</span></span>
<span data-ttu-id="6fe17-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fe17-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe17-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6fe17-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe17-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fe17-139">INPUTS</span></span>

### <span data-ttu-id="6fe17-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6fe17-140">System.String</span></span>

### <span data-ttu-id="6fe17-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="6fe17-141">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="6fe17-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fe17-142">OUTPUTS</span></span>

### <span data-ttu-id="6fe17-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6fe17-143">System.Boolean</span></span>

## <span data-ttu-id="6fe17-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6fe17-144">NOTES</span></span>

## <span data-ttu-id="6fe17-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fe17-145">RELATED LINKS</span></span>
