---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-aznetworkinterface
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzNetworkInterface.md
ms.openlocfilehash: 9b851bcbaa545dee99628dc066956854181df7f7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223739"
---
# <span data-ttu-id="a2540-101">Set-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a2540-101">Set-AzNetworkInterface</span></span>

## <span data-ttu-id="a2540-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a2540-102">SYNOPSIS</span></span>
<span data-ttu-id="a2540-103">Umożliwia zaktualizowanie interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a2540-103">Updates a network interface.</span></span>

## <span data-ttu-id="a2540-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a2540-104">SYNTAX</span></span>

```
Set-AzNetworkInterface -NetworkInterface <PSNetworkInterface> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a2540-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a2540-105">DESCRIPTION</span></span>
<span data-ttu-id="a2540-106">**Zestaw-AzNetworkInterface** aktualizuje interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="a2540-106">The **Set-AzNetworkInterface** updates a network interface.</span></span>

## <span data-ttu-id="a2540-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a2540-107">EXAMPLES</span></span>

### <span data-ttu-id="a2540-108">Przykład 1: Konfigurowanie interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="a2540-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="a2540-109">W tym przykładzie jest konfigurowany interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="a2540-109">This example configures a network interface.</span></span>
<span data-ttu-id="a2540-110">Pierwsze polecenie uzyskuje interfejs sieciowy o nazwie NetworkInterface1 w grupie zasób ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="a2540-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="a2540-111">Drugie polecenie ustawia prywatny adres IP konfiguracji adresu IP.</span><span class="sxs-lookup"><span data-stu-id="a2540-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="a2540-112">Trzecie polecenie ustawia statyczną metodę przydzielania adresów IP.</span><span class="sxs-lookup"><span data-stu-id="a2540-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="a2540-113">Czwarte polecenie ustawia znacznik na interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="a2540-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="a2540-114">W piątym poleceniu jest używana informacja przechowywana w zmiennej $Nic w celu ustawienia interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="a2540-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="a2540-115">Przykład 2: Zmienianie ustawień DNS na interfejsie sieciowym</span><span class="sxs-lookup"><span data-stu-id="a2540-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="a2540-116">Pierwsze polecenie uzyskuje interfejs sieciowy o nazwie NetworkInterface1, który istnieje w grupie zasób ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="a2540-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="a2540-117">Drugie polecenie doda serwer DNS 192.168.1.100 do tego interfejsu.</span><span class="sxs-lookup"><span data-stu-id="a2540-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="a2540-118">W trzecim poleceniu są stosowane te zmiany w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="a2540-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="a2540-119">Aby usunąć serwer DNS, postępuj zgodnie z wymienionymi powyżej poleceniami, a następnie Zamień ". Dodaj "z". Usuń "w drugim poleceniu.</span><span class="sxs-lookup"><span data-stu-id="a2540-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="a2540-120">Przykład 3: Włączanie przesyłania dalej IP na interfejsie sieciowym</span><span class="sxs-lookup"><span data-stu-id="a2540-120">Example 3: Enable IP forwarding on a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="a2540-121">Pierwsze polecenie pobiera istniejący interfejs sieciowy o nazwie NetworkInterface1 i zapisuje go w zmiennej $nic.</span><span class="sxs-lookup"><span data-stu-id="a2540-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="a2540-122">Drugie polecenie zmieni wartość przesyłania dalej IP na wartość true.</span><span class="sxs-lookup"><span data-stu-id="a2540-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="a2540-123">Na koniec trzecie polecenie zastosuje zmiany w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="a2540-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="a2540-124">Aby wyłączyć przesyłanie dalej adresów IP w interfejsie sieciowym, postępuj zgodnie z przykładową próbką, ale pamiętaj, aby zmienić drugie polecenie na "$nic. EnableIPForwarding = 0 ".</span><span class="sxs-lookup"><span data-stu-id="a2540-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="a2540-125">Przykład 4: Zmienianie podsieci interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="a2540-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="a2540-126">Pierwsze polecenie uzyskuje interfejs sieciowy NetworkInterface1 i zapisuje go w zmiennej $nic.</span><span class="sxs-lookup"><span data-stu-id="a2540-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="a2540-127">Drugie polecenie pobiera sieć wirtualną skojarzoną z podsiecią, z którą ma być skojarzony interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="a2540-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="a2540-128">Drugie polecenie pobiera podsieć i zapisuje ją w zmiennej $subnet 2.</span><span class="sxs-lookup"><span data-stu-id="a2540-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="a2540-129">Trzecie polecenie skojarzył podstawowy prywatny adres IP interfejsu sieciowego z nową podsiecią.</span><span class="sxs-lookup"><span data-stu-id="a2540-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="a2540-130">Na koniec ostatnie polecenie zastosowało te zmiany w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="a2540-130">Finally the last command applied these changes on the network interface.</span></span>
>[!NOTE] 
><span data-ttu-id="a2540-131">Aby można było zmienić podsieć, konfiguracje adresów IP muszą być dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="a2540-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="a2540-132">Jeśli masz statyczne konfiguracje IP, przed kontynuowaniem zmień je na dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="a2540-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 
>[!NOTE]
><span data-ttu-id="a2540-133">Jeśli interfejs sieciowy ma wiele konfiguracji adresów IP, przed wykonaniem ostatecznego polecenia Set-AzNetworkInterface należy wykonać polecenie dalej dla wszystkich tych konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="a2540-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzNetworkInterface command is executed.</span></span> <span data-ttu-id="a2540-134">Można to zrobić, tak jak w połączeniu z, ale zamieniając "0" na odpowiedni numer.</span><span class="sxs-lookup"><span data-stu-id="a2540-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="a2540-135">Jeśli interfejs sieciowy ma N konfiguracji protokołu IP, to muszą istnieć N-1 z tych poleceń.</span><span class="sxs-lookup"><span data-stu-id="a2540-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="a2540-136">Przykład 5: Skojarz/Usuń grupę zabezpieczeń sieci z interfejsem sieciowym</span><span class="sxs-lookup"><span data-stu-id="a2540-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzNetworkInterface
```

<span data-ttu-id="a2540-137">Pierwsze polecenie pobiera istniejący interfejs sieciowy o nazwie NetworkInterface1 i zapisuje go w zmiennej $nic.</span><span class="sxs-lookup"><span data-stu-id="a2540-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="a2540-138">Drugie polecenie pobiera istniejącą grupę zabezpieczeń sieci o nazwie MyNSG i zapisuje ją w zmiennej $nsg.</span><span class="sxs-lookup"><span data-stu-id="a2540-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="a2540-139">Trzecie polecenie przypisuje $nsg do $nic.</span><span class="sxs-lookup"><span data-stu-id="a2540-139">The third command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="a2540-140">Na koniec polecenie Dalej powoduje zastosowanie zmian w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="a2540-140">Finally, the forth command applies the changes to the Network interface.</span></span> <span data-ttu-id="a2540-141">Aby odłączyć grupy zabezpieczeń sieci od interfejsu sieciowego, proste $nsg zamieniane w trzecim poleceniu z $null.</span><span class="sxs-lookup"><span data-stu-id="a2540-141">To dissociate network security groups from a network interface, simple replace $nsg in the third command with $null.</span></span>

## <span data-ttu-id="a2540-142">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a2540-142">PARAMETERS</span></span>

### <span data-ttu-id="a2540-143">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a2540-143">-AsJob</span></span>
<span data-ttu-id="a2540-144">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a2540-144">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a2540-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2540-145">-DefaultProfile</span></span>
<span data-ttu-id="a2540-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a2540-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a2540-147">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a2540-147">-NetworkInterface</span></span>
<span data-ttu-id="a2540-148">Określa obiekt interfejsu sieciowego reprezentujący stan, w którym ma zostać ustawiony interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="a2540-148">Specifies a network interface object representing the state to which the network interface should be set.</span></span>

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

### <span data-ttu-id="a2540-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2540-149">CommonParameters</span></span>
<span data-ttu-id="a2540-150">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a2540-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2540-151">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2540-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2540-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a2540-152">INPUTS</span></span>

### <span data-ttu-id="a2540-153">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a2540-153">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="a2540-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a2540-154">OUTPUTS</span></span>

### <span data-ttu-id="a2540-155">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a2540-155">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="a2540-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a2540-156">NOTES</span></span>

## <span data-ttu-id="a2540-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a2540-157">RELATED LINKS</span></span>

[<span data-ttu-id="a2540-158">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a2540-158">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="a2540-159">Get-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a2540-159">Get-AzNetworkInterface</span></span>](./Get-AzNetworkInterface.md)

[<span data-ttu-id="a2540-160">Nowe — AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a2540-160">New-AzNetworkInterface</span></span>](./New-AzNetworkInterface.md)

[<span data-ttu-id="a2540-161">Remove-AzNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="a2540-161">Remove-AzNetworkInterface</span></span>](./Remove-AzNetworkInterface.md)
