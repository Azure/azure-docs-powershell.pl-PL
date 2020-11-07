---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnGateway.md
ms.openlocfilehash: 17731d3f864f429fdad58bf767fb5cb25950387d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709051"
---
# <span data-ttu-id="a5add-101">Remove-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a5add-101">Remove-AzVpnGateway</span></span>

## <span data-ttu-id="a5add-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5add-102">SYNOPSIS</span></span>
<span data-ttu-id="a5add-103">Polecenie cmdlet Remove-AzVpnGateway powoduje usunięcie bramy sieci VPN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a5add-103">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="a5add-104">Jest to brama specyficzna dla łączności z definicją oprogramowania wirtualnej sieci WAN firmy Azure.</span><span class="sxs-lookup"><span data-stu-id="a5add-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="a5add-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5add-105">SYNTAX</span></span>

### <span data-ttu-id="a5add-106">ByVpnGatewayName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a5add-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5add-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="a5add-107">ByVpnGatewayObject</span></span>
```
Remove-AzVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5add-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="a5add-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5add-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a5add-109">DESCRIPTION</span></span>
<span data-ttu-id="a5add-110">Polecenie cmdlet Remove-AzVpnGateway powoduje usunięcie bramy sieci VPN platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a5add-110">The Remove-AzVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="a5add-111">Jest to brama specyficzna dla łączności z definicją oprogramowania wirtualnej sieci WAN firmy Azure.</span><span class="sxs-lookup"><span data-stu-id="a5add-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="a5add-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5add-112">EXAMPLES</span></span>

### <span data-ttu-id="a5add-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a5add-113">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="a5add-114">W tym przykładzie jest tworzona Grupa zasobów, wirtualna sieć WAN, wirtualny koncentrator, skalowalna Brama sieci VPN w obszarze Centrala Amerykańska, a następnie natychmiast usuwana.</span><span class="sxs-lookup"><span data-stu-id="a5add-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="a5add-115">Aby zapobiec wyświetlaniu monitu podczas usuwania bramy wirtualnej, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="a5add-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="a5add-116">Spowoduje to usunięcie VpnGateway i wszystkich skojarzonych z nim VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="a5add-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="a5add-117">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a5add-117">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzVpnGateway-Passthru
```

<span data-ttu-id="a5add-118">W tym przykładzie jest tworzona Grupa zasobów, wirtualna sieć WAN, wirtualny koncentrator, skalowalna Brama sieci VPN w obszarze Centrala Amerykańska, a następnie natychmiast usuwana.</span><span class="sxs-lookup"><span data-stu-id="a5add-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="a5add-119">To usunięcie jest wykonywane przy użyciu połączeń rurowych programu PowerShell, które używają obiektu VpnGateway zwróconego przez polecenie Get-AzVpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a5add-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzVpnGateway command.</span></span>
<span data-ttu-id="a5add-120">Aby zapobiec wyświetlaniu monitu podczas usuwania bramy wirtualnej, Użyj flagi-Force.</span><span class="sxs-lookup"><span data-stu-id="a5add-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="a5add-121">Spowoduje to usunięcie VpnGateway i wszystkich skojarzonych z nim VpnConnections.</span><span class="sxs-lookup"><span data-stu-id="a5add-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="a5add-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5add-122">PARAMETERS</span></span>

### <span data-ttu-id="a5add-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5add-123">-DefaultProfile</span></span>
<span data-ttu-id="a5add-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5add-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5add-125">-Force</span><span class="sxs-lookup"><span data-stu-id="a5add-125">-Force</span></span>
<span data-ttu-id="a5add-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a5add-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a5add-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a5add-127">-InputObject</span></span>
<span data-ttu-id="a5add-128">Obiekt vpnGateway, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="a5add-128">The vpnGateway object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5add-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a5add-129">-Name</span></span>
<span data-ttu-id="a5add-130">Nazwa vpnGateway.</span><span class="sxs-lookup"><span data-stu-id="a5add-130">The vpnGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5add-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5add-131">-PassThru</span></span>
<span data-ttu-id="a5add-132">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="a5add-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a5add-133">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="a5add-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a5add-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5add-134">-ResourceGroupName</span></span>
<span data-ttu-id="a5add-135">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a5add-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5add-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a5add-136">-ResourceId</span></span>
<span data-ttu-id="a5add-137">Identyfikator zasobu platformy Azure dla vpnGateway, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="a5add-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: vpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5add-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a5add-138">-Confirm</span></span>
<span data-ttu-id="a5add-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5add-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5add-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5add-140">-WhatIf</span></span>
<span data-ttu-id="a5add-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5add-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5add-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a5add-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5add-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5add-143">CommonParameters</span></span>
<span data-ttu-id="a5add-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5add-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5add-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5add-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5add-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5add-146">INPUTS</span></span>

### <span data-ttu-id="a5add-147">Microsoft. Azure. Commands. Network. models. PSVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a5add-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="a5add-148">System. String</span><span class="sxs-lookup"><span data-stu-id="a5add-148">System.String</span></span>

## <span data-ttu-id="a5add-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5add-149">OUTPUTS</span></span>

### <span data-ttu-id="a5add-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a5add-150">System.Boolean</span></span>

## <span data-ttu-id="a5add-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5add-151">NOTES</span></span>

## <span data-ttu-id="a5add-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5add-152">RELATED LINKS</span></span>

[<span data-ttu-id="a5add-153">Get-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a5add-153">Get-AzVpnGateway</span></span>](./Get-AzVpnGateway.md)

[<span data-ttu-id="a5add-154">Nowe — AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a5add-154">New-AzVpnGateway</span></span>](./New-AzVpnGateway.md)

[<span data-ttu-id="a5add-155">Update-AzVpnGateway</span><span class="sxs-lookup"><span data-stu-id="a5add-155">Update-AzVpnGateway</span></span>](./Update-AzVpnGateway.md)
