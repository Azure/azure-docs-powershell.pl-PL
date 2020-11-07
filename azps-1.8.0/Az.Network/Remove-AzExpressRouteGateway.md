---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteGateway.md
ms.openlocfilehash: b4b0253814c6488c5f7269c6a79d51790a2f39fd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709136"
---
# <span data-ttu-id="86933-101">Remove-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="86933-101">Remove-AzExpressRouteGateway</span></span>

## <span data-ttu-id="86933-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86933-102">SYNOPSIS</span></span>
<span data-ttu-id="86933-103">Polecenie cmdlet Remove-AzExpressRouteGateway usuwa bramę usługi Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="86933-103">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="86933-104">Jest to brama specyficzna dla łączności z definicją oprogramowania wirtualnej sieci WAN firmy Azure.</span><span class="sxs-lookup"><span data-stu-id="86933-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="86933-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86933-105">SYNTAX</span></span>

### <span data-ttu-id="86933-106">ByExpressRouteGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="86933-106">ByExpressRouteGatewayName (Default)</span></span>
```
Remove-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86933-107">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="86933-107">ByExpressRouteGatewayObject</span></span>
```
Remove-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86933-108">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="86933-108">ByExpressRouteGatewayResourceId</span></span>
```
Remove-AzExpressRouteGateway -ResourceId <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86933-109">Opis</span><span class="sxs-lookup"><span data-stu-id="86933-109">DESCRIPTION</span></span>
<span data-ttu-id="86933-110">Polecenie cmdlet Remove-AzExpressRouteGateway usuwa bramę usługi Azure ExpressRoute.</span><span class="sxs-lookup"><span data-stu-id="86933-110">The Remove-AzExpressRouteGateway cmdlet removes an Azure ExpressRoute gateway.</span></span> <span data-ttu-id="86933-111">Jest to brama specyficzna dla łączności z definicją oprogramowania wirtualnej sieci WAN firmy Azure.</span><span class="sxs-lookup"><span data-stu-id="86933-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="86933-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86933-112">EXAMPLES</span></span>

### <span data-ttu-id="86933-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="86933-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Remove-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -Passthru
```

<span data-ttu-id="86933-114">W tym przykładzie jest tworzona Grupa zasobów, wirtualna sieć WAN, wirtualny koncentrator, skalowalna Brama ExpressRoute w centrum centrali w Stanach Zjednoczonych, a następnie natychmiast usuwana.</span><span class="sxs-lookup"><span data-stu-id="86933-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="86933-115">Aby zapobiec wyświetlaniu monitu podczas usuwania bramy wirtualnej, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="86933-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="86933-116">Spowoduje to usunięcie ExpressRouteGateway i wszystkich skojarzonych z nim ExpressRouteConnections.</span><span class="sxs-lookup"><span data-stu-id="86933-116">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

### <span data-ttu-id="86933-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="86933-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West Central US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West Central US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\> Get-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testExpressRoutegw" | Remove-AzExpressRouteGateway-Passthru
```

<span data-ttu-id="86933-118">W tym przykładzie jest tworzona Grupa zasobów, wirtualna sieć WAN, wirtualny koncentrator, skalowalna Brama ExpressRoute w Stanach Zjednoczonych, a następnie natychmiast usunięty.</span><span class="sxs-lookup"><span data-stu-id="86933-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable ExpressRoute gateway in West Central US and then immediately deletes it.</span></span> <span data-ttu-id="86933-119">To usunięcie jest wykonywane przy użyciu połączeń rurowych programu PowerShell, które używają obiektu ExpressRouteGateway zwróconego przez polecenie Get-AzExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="86933-119">This deletion happens using powershell piping, which uses the ExpressRouteGateway object returned by the Get-AzExpressRouteGateway command.</span></span>
<span data-ttu-id="86933-120">Aby zapobiec wyświetlaniu monitu podczas usuwania bramy wirtualnej, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="86933-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="86933-121">Spowoduje to usunięcie ExpressRouteGateway i wszystkich skojarzonych z nim ExpressRouteConnections.</span><span class="sxs-lookup"><span data-stu-id="86933-121">This will delete the ExpressRouteGateway and all ExpressRouteConnections attached to it.</span></span>

## <span data-ttu-id="86933-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86933-122">PARAMETERS</span></span>

### <span data-ttu-id="86933-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86933-123">-DefaultProfile</span></span>
<span data-ttu-id="86933-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="86933-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="86933-125">-Force</span><span class="sxs-lookup"><span data-stu-id="86933-125">-Force</span></span>
<span data-ttu-id="86933-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="86933-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="86933-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="86933-127">-InputObject</span></span>
<span data-ttu-id="86933-128">Obiekt ExpressRouteGateway, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="86933-128">The ExpressRouteGateway object to be deleted.</span></span>

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

### <span data-ttu-id="86933-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="86933-129">-Name</span></span>
<span data-ttu-id="86933-130">Nazwa ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="86933-130">The ExpressRouteGateway name.</span></span>

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

### <span data-ttu-id="86933-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86933-131">-PassThru</span></span>
<span data-ttu-id="86933-132">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="86933-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="86933-133">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="86933-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="86933-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86933-134">-ResourceGroupName</span></span>
<span data-ttu-id="86933-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="86933-135">The resource group name.</span></span>

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

### <span data-ttu-id="86933-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86933-136">-ResourceId</span></span>
<span data-ttu-id="86933-137">Identyfikator zasobu platformy Azure dla ExpressRouteGateway, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="86933-137">The Azure resource ID for the ExpressRouteGateway to be deleted.</span></span>

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

### <span data-ttu-id="86933-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="86933-138">-Confirm</span></span>
<span data-ttu-id="86933-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86933-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86933-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86933-140">-WhatIf</span></span>
<span data-ttu-id="86933-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86933-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86933-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="86933-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86933-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86933-143">CommonParameters</span></span>
<span data-ttu-id="86933-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86933-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86933-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86933-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86933-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86933-146">INPUTS</span></span>

### <span data-ttu-id="86933-147">Microsoft. Azure. Commands. Network. models. PSExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="86933-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

### <span data-ttu-id="86933-148">System. String</span><span class="sxs-lookup"><span data-stu-id="86933-148">System.String</span></span>

## <span data-ttu-id="86933-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86933-149">OUTPUTS</span></span>

### <span data-ttu-id="86933-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="86933-150">System.Boolean</span></span>

## <span data-ttu-id="86933-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86933-151">NOTES</span></span>

## <span data-ttu-id="86933-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86933-152">RELATED LINKS</span></span>
