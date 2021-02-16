---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186851"
---
# <span data-ttu-id="17459-101">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="17459-101">Set-AzNetworkInterface</span></span>

## <span data-ttu-id="17459-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17459-102">SYNOPSIS</span></span>
<span data-ttu-id="17459-103">Aktualizuje interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="17459-103">Updates a network interface.</span></span>

## <span data-ttu-id="17459-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="17459-104">SYNTAX</span></span>

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17459-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="17459-105">DESCRIPTION</span></span>
<span data-ttu-id="17459-106">**Set-AzNetworkInterface** aktualizuje interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="17459-106">The **Set-AzNetworkInterface** updates a network interface.</span></span>

## <span data-ttu-id="17459-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="17459-107">EXAMPLES</span></span>

### <span data-ttu-id="17459-108">Przykład 1. Konfigurowanie interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="17459-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="17459-109">W tym przykładzie skonfigurowano interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="17459-109">This example configures a network interface.</span></span>
<span data-ttu-id="17459-110">Pierwsze polecenie otrzymuje interfejs sieciowy o nazwie NetworkInterface1 w grupie zasobów ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="17459-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="17459-111">Drugie polecenie ustawia prywatny adres IP konfiguracji ip.</span><span class="sxs-lookup"><span data-stu-id="17459-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="17459-112">Trzecie polecenie ustawia dla prywatnej metody alokacji adresów IP ustawienie Statyczne.</span><span class="sxs-lookup"><span data-stu-id="17459-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="17459-113">Czwarte polecenie ustawia tag w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="17459-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="17459-114">Piąte polecenie używa informacji przechowywanych w $Nic sieciowej do ustawienia interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="17459-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="17459-115">Przykład 2. Zmienianie ustawień DNS w interfejsie sieciowym</span><span class="sxs-lookup"><span data-stu-id="17459-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="17459-116">Pierwsze polecenie otrzymuje interfejs sieciowy o nazwie NetworkInterface1, który istnieje w grupie zasobów ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="17459-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="17459-117">Drugie polecenie dodaje do tego interfejsu serwer DNS 192.168.1.100.</span><span class="sxs-lookup"><span data-stu-id="17459-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="17459-118">Trzecie polecenie powoduje zastosowanie tych zmian do interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="17459-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="17459-119">Aby usunąć serwer DNS, postępuj zgodnie z poleceniami wymienionymi powyżej, ale zastąp ". Dodaj" z ". Usuń" w drugim poleceniu.</span><span class="sxs-lookup"><span data-stu-id="17459-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="17459-120">Przykład 3. Włączanie przesyłania dalej adresów IP w interfejsie sieciowym</span><span class="sxs-lookup"><span data-stu-id="17459-120">Example 3: Enable IP forwarding on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="17459-121">Pierwsze polecenie uzyskuje istniejący interfejs sieciowy o nazwie NetworkInterface1 i przechowuje je w $nic zmienną.</span><span class="sxs-lookup"><span data-stu-id="17459-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="17459-122">Drugie polecenie zmienia wartość przesyłania dalej adresów IP na prawda.</span><span class="sxs-lookup"><span data-stu-id="17459-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="17459-123">Trzecie polecenie powoduje zastosowanie zmian do interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="17459-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="17459-124">Aby wyłączyć przesyłanie dalej adresów IP w interfejsie sieciowym, wykonaj przykład, ale pamiętaj, aby zmienić drugie polecenie na "$nic. EnableIPForwarding = 0".</span><span class="sxs-lookup"><span data-stu-id="17459-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="17459-125">Przykład 4. Zmienianie podsieci interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="17459-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="17459-126">Pierwsze polecenie pobiera interfejs sieciowy NetworkInterface1 i zapisuje je w zmiennej $nic sieci.</span><span class="sxs-lookup"><span data-stu-id="17459-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="17459-127">Drugie polecenie pobiera sieć wirtualną skojarzoną z podsiecią, z która zostanie skojarzony interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="17459-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="17459-128">Drugie polecenie pobiera podsieci i przechowuje je w zmiennej $subnet 2.</span><span class="sxs-lookup"><span data-stu-id="17459-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="17459-129">Trzecie polecenie skojarzyło podstawowy prywatny adres IP interfejsu sieciowego z nową podsiecią.</span><span class="sxs-lookup"><span data-stu-id="17459-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="17459-130">Ostatnie polecenie zastosować te zmiany w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="17459-130">Finally the last command applied these changes on the network interface.</span></span>
>[!NOTE] 
><span data-ttu-id="17459-131">Konfiguracje adresów IP muszą być dynamiczne, aby można było zmienić podsieci.</span><span class="sxs-lookup"><span data-stu-id="17459-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="17459-132">Jeśli masz statyczne konfiguracje ADRESÓW IP, zmień je na dynamiczne przed rozpoczęciem pracy.</span><span class="sxs-lookup"><span data-stu-id="17459-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 
>[!NOTE]
><span data-ttu-id="17459-133">Jeśli interfejs sieciowy ma wiele konfiguracji adresów IP, należy wykonać następujące polecenie dla wszystkich tych konfiguracji adresów IP, zanim zostanie Set-AzNetworkInterface wykonania ostatecznego polecenia adresu IP.</span><span class="sxs-lookup"><span data-stu-id="17459-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzNetworkInterface command is executed.</span></span> <span data-ttu-id="17459-134">Można to zrobić zgodnie z poleceniami, ale zamieniając liczbę "0" na odpowiednią liczbę.</span><span class="sxs-lookup"><span data-stu-id="17459-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="17459-135">Jeśli interfejs sieciowy ma konfiguracje protokołu IP N, musi istnieć N-1 tych poleceń.</span><span class="sxs-lookup"><span data-stu-id="17459-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="17459-136">Przykład 5. Kojarzenie/kojarzenie grupy zabezpieczeń sieciowych z interfejsem sieciowym</span><span class="sxs-lookup"><span data-stu-id="17459-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="17459-137">Pierwsze polecenie uzyskuje istniejący interfejs sieciowy o nazwie NetworkInterface1 i przechowuje je w $nic zmienną.</span><span class="sxs-lookup"><span data-stu-id="17459-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="17459-138">Drugie polecenie pobiera istniejącą grupę zabezpieczeń sieciową o nazwie MyNSG i przechowuje ją w $nsg sieci.</span><span class="sxs-lookup"><span data-stu-id="17459-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="17459-139">Trzecie polecenie przypisuje $nsg do $nic.</span><span class="sxs-lookup"><span data-stu-id="17459-139">The third command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="17459-140">Na koniec polecenie z drugiej strony powoduje zastosowanie zmian do interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="17459-140">Finally, the forth command applies the changes to the Network interface.</span></span> <span data-ttu-id="17459-141">Aby rozdzielić grupy zabezpieczeń sieciowych z interfejsu sieciowego, $nsg zastąpić je trzecim poleceniem $null.</span><span class="sxs-lookup"><span data-stu-id="17459-141">To dissociate network security groups from a network interface, simple replace $nsg in the third command with $null.</span></span>

## <span data-ttu-id="17459-142">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17459-142">PARAMETERS</span></span>

### <span data-ttu-id="17459-143">— AsJob</span><span class="sxs-lookup"><span data-stu-id="17459-143">-AsJob</span></span>
<span data-ttu-id="17459-144">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="17459-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="17459-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17459-145">-DefaultProfile</span></span>
<span data-ttu-id="17459-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="17459-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17459-147">- NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="17459-147">-NetworkInterface</span></span>
<span data-ttu-id="17459-148">Określa obiekt interfejsu sieciowego reprezentujący stan, dla którego powinien zostać ustawiony interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="17459-148">Specifies a network interface object representing the state to which the network interface should be set.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkInterface
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="17459-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17459-149">CommonParameters</span></span>
<span data-ttu-id="17459-150">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17459-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17459-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17459-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17459-152">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17459-152">INPUTS</span></span>

### <span data-ttu-id="17459-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="17459-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="17459-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="17459-154">OUTPUTS</span></span>

### <span data-ttu-id="17459-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="17459-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="17459-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="17459-156">NOTES</span></span>

## <span data-ttu-id="17459-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17459-157">RELATED LINKS</span></span>

[<span data-ttu-id="17459-158">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="17459-158">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="17459-159">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="17459-159">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="17459-160">New-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="17459-160">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="17459-161">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="17459-161">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)
