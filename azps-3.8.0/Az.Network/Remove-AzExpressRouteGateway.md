---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: 73bf40456b1fa99093f2c84c11f71e945004a8fa
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053020"
---
# <span data-ttu-id="14f57-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="14f57-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="14f57-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="14f57-102">SYNOPSIS</span></span>
<span data-ttu-id="14f57-103">Polecenie cmdlet Remove-AzExpressRouteGateway usuwa bramę usługi Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="14f57-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="14f57-104">Jest to brama specyficzna dla łączności z definicją oprogramowania wirtualnej sieci WAN firmy Azure.</span><span class="sxs-lookup"><span data-stu-id="14f57-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="14f57-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="14f57-105">SYNTAX</span></span>

### <span data-ttu-id="14f57-106">ByExpressRouteGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="14f57-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14f57-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="14f57-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="14f57-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="14f57-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="14f57-109">Opis</span><span class="sxs-lookup"><span data-stu-id="14f57-109">DESCRIPTION</span></span>
<span data-ttu-id="14f57-110">Polecenie cmdlet Remove-AzExpressRouteGateway usuwa bramę usługi Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="14f57-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="14f57-111">Jest to brama specyficzna dla łączności z definicją oprogramowania wirtualnej sieci WAN firmy Azure.</span><span class="sxs-lookup"><span data-stu-id="14f57-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="14f57-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="14f57-112">EXAMPLES</span></span>

### <span data-ttu-id="14f57-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="14f57-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="14f57-114">W tym przykładzie jest tworzona Grupa zasobów, wirtualna sieć WAN, wirtualny koncentrator, skalowalna Brama ExpressRoute w centrum centrali w Stanach Zjednoczonych, a następnie natychmiast usuwana.</span><span class="sxs-lookup"><span data-stu-id="14f57-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="14f57-115">Aby zapobiec wyświetlaniu monitu podczas usuwania bramy wirtualnej, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="14f57-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="14f57-116">Spowoduje to usunięcie ExpressRouteGateway i wszystkich skojarzonych z nim ExpressRouteConnections.</span><span class="sxs-lookup"><span data-stu-id="14f57-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="14f57-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="14f57-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="14f57-118">W tym przykładzie jest tworzona Grupa zasobów, wirtualna sieć WAN, wirtualny koncentrator, skalowalna Brama ExpressRoute w Stanach Zjednoczonych, a następnie natychmiast usunięty.</span><span class="sxs-lookup"><span data-stu-id="14f57-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="14f57-119">To usunięcie jest wykonywane przy użyciu połączeń rurowych programu PowerShell, które używają obiektu ExpressRouteGateway zwróconego przez polecenie Get-AzExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="14f57-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="14f57-120">Aby zapobiec wyświetlaniu monitu podczas usuwania bramy wirtualnej, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="14f57-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="14f57-121">Spowoduje to usunięcie ExpressRouteGateway i wszystkich skojarzonych z nim ExpressRouteConnections.</span><span class="sxs-lookup"><span data-stu-id="14f57-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="14f57-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="14f57-122">PARAMETERS</span></span>

### <span data-ttu-id="14f57-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14f57-123">-DefaultProfile</span></span>
<span data-ttu-id="14f57-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="14f57-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14f57-125">-Force</span><span class="sxs-lookup"><span data-stu-id="14f57-125">-Force</span></span>
<span data-ttu-id="14f57-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="14f57-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="14f57-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="14f57-127">-InputObject</span></span>
<span data-ttu-id="14f57-128">Obiekt ExpressRouteGateway, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="14f57-128">The ExpressRouteGateway object to be deleted.</span></span>

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

### <span data-ttu-id="14f57-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="14f57-129">-Name</span></span>
<span data-ttu-id="14f57-130">Nazwa ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="14f57-130">The ExpressRouteGateway name.</span></span>

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

### <span data-ttu-id="14f57-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="14f57-131">-PassThru</span></span>
<span data-ttu-id="14f57-132">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="14f57-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="14f57-133">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="14f57-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="14f57-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14f57-134">-ResourceGroupName</span></span>
<span data-ttu-id="14f57-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="14f57-135">The resource group name.</span></span>

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

### <span data-ttu-id="14f57-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="14f57-136">-ResourceId</span></span>
<span data-ttu-id="14f57-137">Identyfikator zasobu platformy Azure dla ExpressRouteGateway, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="14f57-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="14f57-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="14f57-138">-Confirm</span></span>
<span data-ttu-id="14f57-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14f57-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14f57-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14f57-140">-WhatIf</span></span>
<span data-ttu-id="14f57-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="14f57-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="14f57-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="14f57-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14f57-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14f57-143">CommonParameters</span></span>
<span data-ttu-id="14f57-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14f57-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14f57-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14f57-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14f57-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14f57-146">INPUTS</span></span>

### <span data-ttu-id="14f57-147">Microsoft. Azure. Commands. Network. models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="14f57-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="14f57-148">System. String</span><span class="sxs-lookup"><span data-stu-id="14f57-148">System.String</span></span>

## <span data-ttu-id="14f57-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="14f57-149">OUTPUTS</span></span>

### <span data-ttu-id="14f57-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="14f57-150">System.Boolean</span></span>

## <span data-ttu-id="14f57-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="14f57-151">NOTES</span></span>

## <span data-ttu-id="14f57-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14f57-152">RELATED LINKS</span></span>
