---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRoutePort.md
ms.openlocfilehash: 7e6ee711de551de00a54930be2bdb285998e3ccb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317905"
---
# <span data-ttu-id="8b04e-101">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8b04e-101">Remove-AzExpressRoutePort</span></span>

## <span data-ttu-id="8b04e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8b04e-102">SYNOPSIS</span></span>
<span data-ttu-id="8b04e-103">Usuwa ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="8b04e-103">Removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="8b04e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8b04e-104">SYNTAX</span></span>

### <span data-ttu-id="8b04e-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8b04e-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzExpressRoutePort -ResourceGroupName <String> -Name <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b04e-106">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b04e-106">InputObjectParameterSet</span></span>
```
Remove-AzExpressRoutePort -InputObject <PSExpressRoutePort> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8b04e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8b04e-107">ResourceIdParameterSet</span></span>
```
Remove-AzExpressRoutePort -ResourceId <String> [-Force] [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8b04e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8b04e-108">DESCRIPTION</span></span>
<span data-ttu-id="8b04e-109">Polecenie cmdlet **Remove-AzExpressRoutePort** usuwa ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="8b04e-109">The **Remove-AzExpressRoutePort** cmdlet removes an ExpressRoutePort.</span></span>

## <span data-ttu-id="8b04e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8b04e-110">EXAMPLES</span></span>

### <span data-ttu-id="8b04e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8b04e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $PortName -ResourceGroupName $rg
```

<span data-ttu-id="8b04e-112">Usuwa $PortName zasób ExpressRoutePort w $rg grupy zasobów w subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8b04e-112">Removes $PortName ExpressRoutePort resource in $rg resource group in your subscription.</span></span>

### <span data-ttu-id="8b04e-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8b04e-113">Example 2</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -InputObject $erPort
```

<span data-ttu-id="8b04e-114">Usuwa zasób ExpressRoutePort w polu Inputobject.</span><span class="sxs-lookup"><span data-stu-id="8b04e-114">Removes the ExpressRoutePort resource in InputObject.</span></span>

### <span data-ttu-id="8b04e-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8b04e-115">Example 3</span></span>
```powershell
PS C:\> Remove-AzExpressRoutePort -Name $ResourceId $id
```

<span data-ttu-id="8b04e-116">Usuwa zasób ExpressRoutePort o identyfikatorze ResourceId $id.</span><span class="sxs-lookup"><span data-stu-id="8b04e-116">Removes the ExpressRoutePort resource with ResourceId $id.</span></span>

## <span data-ttu-id="8b04e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8b04e-117">PARAMETERS</span></span>

### <span data-ttu-id="8b04e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8b04e-118">-AsJob</span></span>
<span data-ttu-id="8b04e-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="8b04e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8b04e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b04e-120">-DefaultProfile</span></span>
<span data-ttu-id="8b04e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b04e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b04e-122">-Force</span><span class="sxs-lookup"><span data-stu-id="8b04e-122">-Force</span></span>
<span data-ttu-id="8b04e-123">Nie pytaj o potwierdzenie, czy chcesz usunąć zasób</span><span class="sxs-lookup"><span data-stu-id="8b04e-123">Do not ask for confirmation if you want to delete resource</span></span>

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

### <span data-ttu-id="8b04e-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8b04e-124">-InputObject</span></span>
<span data-ttu-id="8b04e-125">Obiekt port routingu Express</span><span class="sxs-lookup"><span data-stu-id="8b04e-125">The express route port object</span></span>

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

### <span data-ttu-id="8b04e-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8b04e-126">-Name</span></span>
<span data-ttu-id="8b04e-127">Nazwa ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="8b04e-127">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="8b04e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b04e-128">-PassThru</span></span>
<span data-ttu-id="8b04e-129">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="8b04e-129">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="8b04e-130">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="8b04e-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="8b04e-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b04e-131">-ResourceGroupName</span></span>
<span data-ttu-id="8b04e-132">Nazwa grupy zasobów ExpressRoutePort.</span><span class="sxs-lookup"><span data-stu-id="8b04e-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="8b04e-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8b04e-133">-ResourceId</span></span>
<span data-ttu-id="8b04e-134">Identyfikator zasobu Express Route port.</span><span class="sxs-lookup"><span data-stu-id="8b04e-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="8b04e-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8b04e-135">-Confirm</span></span>
<span data-ttu-id="8b04e-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b04e-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b04e-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b04e-137">-WhatIf</span></span>
<span data-ttu-id="8b04e-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b04e-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b04e-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8b04e-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b04e-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b04e-140">CommonParameters</span></span>
<span data-ttu-id="8b04e-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b04e-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b04e-142">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8b04e-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b04e-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b04e-143">INPUTS</span></span>

### <span data-ttu-id="8b04e-144">Microsoft. Azure. Commands. Network. models. PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8b04e-144">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="8b04e-145">System. String</span><span class="sxs-lookup"><span data-stu-id="8b04e-145">System.String</span></span>

## <span data-ttu-id="8b04e-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8b04e-146">OUTPUTS</span></span>

### <span data-ttu-id="8b04e-147">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8b04e-147">System.Boolean</span></span>

## <span data-ttu-id="8b04e-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8b04e-148">NOTES</span></span>

## <span data-ttu-id="8b04e-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b04e-149">RELATED LINKS</span></span>

[<span data-ttu-id="8b04e-150">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8b04e-150">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="8b04e-151">Nowe — AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8b04e-151">New-AzExpressRoutePort</span></span>](./New-AzExpressRoutePort.md)

[<span data-ttu-id="8b04e-152">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="8b04e-152">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
