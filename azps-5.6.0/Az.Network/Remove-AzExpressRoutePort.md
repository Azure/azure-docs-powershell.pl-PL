---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
ms.openlocfilehash: c0110186277df7e41b9110b1cfdf2fa7b948b50e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996381"
---
# <span data-ttu-id="77058-101">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="77058-101">Remove-AzExpressRoutePort</span></span>

## <span data-ttu-id="77058-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="77058-102">SYNOPSIS</span></span>
<span data-ttu-id="77058-103">Usuwa port ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="77058-103">Removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="77058-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="77058-104">SYNTAX</span></span>

### <span data-ttu-id="77058-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="77058-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77058-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="77058-106">InputObjectParameterSet</span></span>
```
Remove-AzExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77058-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="77058-107">ResourceIdParameterSet</span></span>
```
Remove-AzExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77058-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="77058-108">DESCRIPTION</span></span>
<span data-ttu-id="77058-109">Polecenie **cmdlet Remove-AzExpressRoutePort** usuwa port ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="77058-109">The **Remove-AzExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="77058-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="77058-110">EXAMPLES</span></span>

### <span data-ttu-id="77058-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77058-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="77058-112">Usuwa $PortName ExpressRoutePort w $rg grupy zasobów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="77058-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="77058-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="77058-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -InputObject $erPort
```

<span data-ttu-id="77058-114">Usuwa zasób ExpressRoutePort z inputObject.</span><span class="sxs-lookup"><span data-stu-id="77058-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="77058-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="77058-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="77058-116">Usuwa zasób ExpressRoutePort przy użyciu $id ResourceId.</span><span class="sxs-lookup"><span data-stu-id="77058-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="77058-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="77058-117">PARAMETERS</span></span>

### <span data-ttu-id="77058-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="77058-118">-AsJob</span></span>
<span data-ttu-id="77058-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="77058-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="77058-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77058-120">-DefaultProfile</span></span>
<span data-ttu-id="77058-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="77058-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77058-122">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="77058-122">-Force</span></span>
<span data-ttu-id="77058-123">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="77058-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="77058-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="77058-124">-InputObject</span></span>
<span data-ttu-id="77058-125">Obiekt portu trasy ekspresowej</span><span class="sxs-lookup"><span data-stu-id="77058-125">The express route port object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77058-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="77058-126">-Name</span></span>
<span data-ttu-id="77058-127">Nazwa portu expressroutePort.</span><span class="sxs-lookup"><span data-stu-id="77058-127">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77058-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77058-128">-PassThru</span></span>
<span data-ttu-id="77058-129">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="77058-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="77058-130">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="77058-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="77058-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77058-131">-ResourceGroupName</span></span>
<span data-ttu-id="77058-132">Nazwa grupy zasobów dlaportu ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="77058-132">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77058-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="77058-133">-ResourceId</span></span>
<span data-ttu-id="77058-134">ResourceId portu trasy ekspresowej.</span><span class="sxs-lookup"><span data-stu-id="77058-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="77058-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="77058-135">-Confirm</span></span>
<span data-ttu-id="77058-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="77058-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77058-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77058-137">-WhatIf</span></span>
<span data-ttu-id="77058-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77058-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77058-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="77058-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77058-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77058-140">CommonParameters</span></span>
<span data-ttu-id="77058-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77058-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77058-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77058-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77058-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77058-143">INPUTS</span></span>

### <span data-ttu-id="77058-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="77058-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="77058-145">System.String</span><span class="sxs-lookup"><span data-stu-id="77058-145">System.String</span></span>

## <span data-ttu-id="77058-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77058-146">OUTPUTS</span></span>

### <span data-ttu-id="77058-147">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="77058-147">System.Boolean</span></span>

## <span data-ttu-id="77058-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="77058-148">NOTES</span></span>

## <span data-ttu-id="77058-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77058-149">RELATED LINKS</span></span>

[<span data-ttu-id="77058-150">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="77058-150">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="77058-151">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="77058-151">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="77058-152">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="77058-152">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
