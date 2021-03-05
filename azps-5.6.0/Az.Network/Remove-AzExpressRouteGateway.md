---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: 77c41a4565a517a51b02c904d79953d79e908c39
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996395"
---
# <span data-ttu-id="127d9-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="127d9-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="127d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="127d9-102">SYNOPSIS</span></span>
<span data-ttu-id="127d9-103">Polecenie Remove-AzExpressRouteGateway cmdlet usuwa bramę usługi Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="127d9-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="127d9-104">Jest to brama specyficzna dla łączności zdefiniowanej przez oprogramowanie Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="127d9-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="127d9-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="127d9-105">SYNTAX</span></span>

### <span data-ttu-id="127d9-106">ByExpressRouteGatewayName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="127d9-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="127d9-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="127d9-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="127d9-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="127d9-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="127d9-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="127d9-109">DESCRIPTION</span></span>
<span data-ttu-id="127d9-110">Polecenie Remove-AzExpressRouteGateway cmdlet usuwa bramę usługi Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="127d9-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="127d9-111">Jest to brama specyficzna dla łączności zdefiniowanej przez oprogramowanie Azure Virtual WAN.</span><span class="sxs-lookup"><span data-stu-id="127d9-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="127d9-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="127d9-112">EXAMPLES</span></span>

### <span data-ttu-id="127d9-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="127d9-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="127d9-114">W tym przykładzie jest grupę zasobów, wirtualna sieć WAN, centrum wirtualne, skalowalna brama usługi ExpressRoute w centrum STANÓW Zjednoczonych, a następnie natychmiast ją usuwa.</span><span class="sxs-lookup"><span data-stu-id="127d9-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="127d9-115">Aby pominąć monit podczas usuwania bramy wirtualnej, użyj flagi -Force.</span><span class="sxs-lookup"><span data-stu-id="127d9-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="127d9-116">Spowoduje to usunięcie dołączonej do niej bramy ExpressRouteGateway i wszystkich połączonych z nim połączeń usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="127d9-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="127d9-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="127d9-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="127d9-118">W tym przykładzie jest grupę zasobów, wirtualną sieć WAN, centrum wirtualne, skalowalną bramę usługi ExpressRoute w zachód środkowych Stanów Zjednoczonych, a następnie natychmiast ją usuwa.</span><span class="sxs-lookup"><span data-stu-id="127d9-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="127d9-119">To usunięcie odbywa się za pomocą linii rurowych programu PowerShell, która korzysta z obiektu ExpressRouteGateway zwróconego przez Get-AzExpressRouteGateway pliku.</span><span class="sxs-lookup"><span data-stu-id="127d9-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="127d9-120">Aby pominąć monit podczas usuwania bramy wirtualnej, użyj flagi -Force.</span><span class="sxs-lookup"><span data-stu-id="127d9-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="127d9-121">Spowoduje to usunięcie dołączonej do niej bramy ExpressRouteGateway i wszystkich połączonych z nim połączeń usługi ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="127d9-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="127d9-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="127d9-122">PARAMETERS</span></span>

### <span data-ttu-id="127d9-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="127d9-123">-DefaultProfile</span></span>
<span data-ttu-id="127d9-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="127d9-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="127d9-125">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="127d9-125">-Force</span></span>
<span data-ttu-id="127d9-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="127d9-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="127d9-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="127d9-127">-InputObject</span></span>
<span data-ttu-id="127d9-128">Obiekt ExpressRouteGateway do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="127d9-128">The ExpressRouteGateway object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="127d9-129">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="127d9-129">-Name</span></span>
<span data-ttu-id="127d9-130">Nazwa aplikacji ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="127d9-130">The ExpressRouteGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="127d9-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="127d9-131">-PassThru</span></span>
<span data-ttu-id="127d9-132">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="127d9-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="127d9-133">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="127d9-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="127d9-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="127d9-134">-ResourceGroupName</span></span>
<span data-ttu-id="127d9-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="127d9-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="127d9-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="127d9-136">-ResourceId</span></span>
<span data-ttu-id="127d9-137">Identyfikator zasobu Azure dla usługi ExpressRouteGateway do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="127d9-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases: expressRouteGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="127d9-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="127d9-138">-Confirm</span></span>
<span data-ttu-id="127d9-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="127d9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="127d9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="127d9-140">-WhatIf</span></span>
<span data-ttu-id="127d9-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="127d9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="127d9-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="127d9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="127d9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="127d9-143">CommonParameters</span></span>
<span data-ttu-id="127d9-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="127d9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="127d9-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="127d9-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="127d9-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="127d9-146">INPUTS</span></span>

### <span data-ttu-id="127d9-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="127d9-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="127d9-148">System.String</span><span class="sxs-lookup"><span data-stu-id="127d9-148">System.String</span></span>

## <span data-ttu-id="127d9-149">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="127d9-149">OUTPUTS</span></span>

### <span data-ttu-id="127d9-150">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="127d9-150">System.Boolean</span></span>

## <span data-ttu-id="127d9-151">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="127d9-151">NOTES</span></span>

## <span data-ttu-id="127d9-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="127d9-152">RELATED LINKS</span></span>
