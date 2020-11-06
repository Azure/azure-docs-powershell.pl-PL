---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: DDB38A77-E5C0-47DD-BADD-94488F661CD5
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterface.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmNetworkInterface.md
ms.openlocfilehash: 8403a2e26bbc149db35c9c20cdea3075adb88492
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543216"
---
# <span data-ttu-id="09906-101">Set-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="09906-101">Set-AzureRmNetworkInterface</span></span>

## <span data-ttu-id="09906-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="09906-102">SYNOPSIS</span></span>
<span data-ttu-id="09906-103">Ustawia stan celu dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="09906-103">Sets the goal state for a network interface.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09906-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="09906-104">SYNTAX</span></span>

```
Set-AzureRmNetworkInterface -NetworkInterface <PSNetworkInterface> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09906-105">Opis</span><span class="sxs-lookup"><span data-stu-id="09906-105">DESCRIPTION</span></span>
<span data-ttu-id="09906-106">**Zestaw-AzureRmNetworkInterface** ustawia stan celu dla interfejsu sieciowego platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="09906-106">The **Set-AzureRmNetworkInterface** sets the goal state for an Azure network interface.</span></span>

## <span data-ttu-id="09906-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="09906-107">EXAMPLES</span></span>

### <span data-ttu-id="09906-108">Przykład 1: Konfigurowanie interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="09906-108">Example 1: Configure a network interface</span></span>
```
$Nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$Nic.IpConfigurations[0].PrivateIpAddress = "10.0.1.20"
$Nic.IpConfigurations[0].PrivateIpAllocationMethod = "Static"
$Nic.Tag = @{Name = "Name"; Value = "Value"}
Set-AzureRmNetworkInterface -NetworkInterface $Nic
```

<span data-ttu-id="09906-109">W tym przykładzie jest konfigurowany interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="09906-109">This example configures a network interface.</span></span>
<span data-ttu-id="09906-110">Pierwsze polecenie uzyskuje interfejs sieciowy o nazwie NetworkInterface1 w grupie zasób ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="09906-110">The first command gets a network interface named NetworkInterface1 in resource group ResourceGroup1.</span></span>
<span data-ttu-id="09906-111">Drugie polecenie ustawia prywatny adres IP konfiguracji adresu IP.</span><span class="sxs-lookup"><span data-stu-id="09906-111">The second command sets the private IP address of the IP configuration.</span></span>
<span data-ttu-id="09906-112">Trzecie polecenie ustawia statyczną metodę przydzielania adresów IP.</span><span class="sxs-lookup"><span data-stu-id="09906-112">The third command sets the private IP allocation method to Static.</span></span>
<span data-ttu-id="09906-113">Czwarte polecenie ustawia znacznik na interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="09906-113">The fourth command sets a tag on the network interface.</span></span>
<span data-ttu-id="09906-114">W piątym poleceniu jest używana informacja przechowywana w zmiennej $Nic w celu ustawienia interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="09906-114">The fifth command uses the information stored in the $Nic variable to set the network interface.</span></span>

### <span data-ttu-id="09906-115">Przykład 2: Zmienianie ustawień DNS na interfejsie sieciowym</span><span class="sxs-lookup"><span data-stu-id="09906-115">Example 2: Change DNS settings on a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.DnsSettings.DnsServers.Add("192.168.1.100")
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="09906-116">Pierwsze polecenie uzyskuje interfejs sieciowy o nazwie NetworkInterface1, który istnieje w grupie zasób ResourceGroup1.</span><span class="sxs-lookup"><span data-stu-id="09906-116">The first command gets a network interface named NetworkInterface1 that exists within resource group ResourceGroup1.</span></span> <span data-ttu-id="09906-117">Drugie polecenie doda serwer DNS 192.168.1.100 do tego interfejsu.</span><span class="sxs-lookup"><span data-stu-id="09906-117">The second command adds DNS server 192.168.1.100 to this interface.</span></span> <span data-ttu-id="09906-118">W trzecim poleceniu są stosowane te zmiany w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="09906-118">The third command applies these changes to the network interface.</span></span> <span data-ttu-id="09906-119">Aby usunąć serwer DNS, postępuj zgodnie z wymienionymi powyżej poleceniami, a następnie Zamień ". Dodaj "z". Usuń "w drugim poleceniu.</span><span class="sxs-lookup"><span data-stu-id="09906-119">To remove a DNS server, follow the commands listed above, but replace ".Add" with ".Remove" in the second command.</span></span>

### <span data-ttu-id="09906-120">Przykład 3: Włączanie Forwading IP w interfejsie sieciowym</span><span class="sxs-lookup"><span data-stu-id="09906-120">Example 3: Enable IP forwading on a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nic.EnableIPForwarding = 1
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="09906-121">Pierwsze polecenie pobiera istniejący interfejs sieciowy o nazwie NetworkInterface1 i zapisuje go w zmiennej $nic.</span><span class="sxs-lookup"><span data-stu-id="09906-121">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="09906-122">Drugie polecenie zmieni wartość przesyłania dalej IP na wartość true.</span><span class="sxs-lookup"><span data-stu-id="09906-122">The second command changes the IP forwarding value to true.</span></span> <span data-ttu-id="09906-123">Na koniec trzecie polecenie zastosuje zmiany w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="09906-123">Finally, the third command applies the changes to the network interface.</span></span> <span data-ttu-id="09906-124">Aby wyłączyć przesyłanie dalej adresów IP w interfejsie sieciowym, postępuj zgodnie z przykładową próbką, ale pamiętaj, aby zmienić drugie polecenie na "$nic. EnableIPForwarding = 0 ".</span><span class="sxs-lookup"><span data-stu-id="09906-124">To disable IP forwarding on a network interface, follow the sample example, but be sure to change the second command to "$nic.EnableIPForwarding = 0".</span></span>

### <span data-ttu-id="09906-125">Przykład 4: Zmienianie podsieci interfejsu sieciowego</span><span class="sxs-lookup"><span data-stu-id="09906-125">Example 4: Change the subnet of a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$vnet = Get-AzureRmVirtualNetwork -Name VNet1 -ResourceGroupName crosssubcrossversionpeering
$subnet2 = Get-AzureRmVirtualNetworkSubnetConfig -Name Subnet2 -VirtualNetwork $vnet
$nic.IpConfigurations[0].Subnet.Id = $subnet2.Id
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="09906-126">Pierwsze polecenie uzyskuje interfejs sieciowy NetworkInterface1 i zapisuje go w zmiennej $nic.</span><span class="sxs-lookup"><span data-stu-id="09906-126">The first command gets the network interface NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="09906-127">Drugie polecenie pobiera sieć wirtualną skojarzoną z podsiecią, z którą ma być skojarzony interfejs sieciowy.</span><span class="sxs-lookup"><span data-stu-id="09906-127">The second command gets the virtual network associated with the subnet that the network interface is going to be associated with.</span></span> <span data-ttu-id="09906-128">Drugie polecenie pobiera podsieć i zapisuje ją w zmiennej $subnet 2.</span><span class="sxs-lookup"><span data-stu-id="09906-128">The second command gets the subnet and stores it in the $subnet2 variable.</span></span> <span data-ttu-id="09906-129">Trzecie polecenie skojarzył podstawowy prywatny adres IP interfejsu sieciowego z nową podsiecią.</span><span class="sxs-lookup"><span data-stu-id="09906-129">The third command associated the primary private IP address of the network interface with the new subnet.</span></span> <span data-ttu-id="09906-130">Na koniec ostatnie polecenie zastosowało te zmiany w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="09906-130">Finally the last command applied these changes on the network interface.</span></span>

>[!NOTE] 
><span data-ttu-id="09906-131">Aby można było zmienić podsieć, konfiguracje adresów IP muszą być dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="09906-131">The IP configurations must be dynamic before you can change the subnet.</span></span> <span data-ttu-id="09906-132">Jeśli masz statyczne konfiguracje IP, przed kontynuowaniem zmień je na dynamiczne.</span><span class="sxs-lookup"><span data-stu-id="09906-132">If you have static IP configurations, change then to dynamic before proceeding.</span></span> 

>[!NOTE]
><span data-ttu-id="09906-133">Jeśli interfejs sieciowy ma wiele konfiguracji adresów IP, przed wykonaniem ostatecznego polecenia Set-AzureRmNetworkInterface należy wykonać polecenie dalej dla wszystkich tych konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="09906-133">If the network interface has multiple IP configurations, the forth command must be done for all these IP configurations before the final Set-AzureRmNetworkInterface command is executed.</span></span> <span data-ttu-id="09906-134">Można to zrobić, tak jak w połączeniu z, ale zamieniając "0" na odpowiedni numer.</span><span class="sxs-lookup"><span data-stu-id="09906-134">This can be done as in the forth command but by replacing "0" with the appropriate number.</span></span> <span data-ttu-id="09906-135">Jeśli interfejs sieciowy ma N konfiguracji protokołu IP, to muszą istnieć N-1 z tych poleceń.</span><span class="sxs-lookup"><span data-stu-id="09906-135">If a network interface has N IP configurations, then N-1 of these commands must exist.</span></span>

### <span data-ttu-id="09906-136">Przykład 5: Skojarz/Usuń grupę zabezpieczeń sieci z interfejsem sieciowym</span><span class="sxs-lookup"><span data-stu-id="09906-136">Example 5: Associate/Dissociate a Network Security Group to a network interface</span></span>
```
$nic = Get-AzureRmNetworkInterface -ResourceGroupName "ResourceGroup1" -Name "NetworkInterface1"
$nsg = Get-AzureRmNetworkSecurityGroup -ResourceGroupName "ResourceGroup1" -Name "MyNSG"
$nic.NetworkSecurityGroup = $nsg
$nic | Set-AzureRmNetworkInterface
```

<span data-ttu-id="09906-137">Pierwsze polecenie pobiera istniejący interfejs sieciowy o nazwie NetworkInterface1 i zapisuje go w zmiennej $nic.</span><span class="sxs-lookup"><span data-stu-id="09906-137">The first command gets an existing network interface called NetworkInterface1 and stores it in the $nic variable.</span></span> <span data-ttu-id="09906-138">Drugie polecenie pobiera istniejącą grupę zabezpieczeń sieci o nazwie MyNSG i zapisuje ją w zmiennej $nsg.</span><span class="sxs-lookup"><span data-stu-id="09906-138">The second command gets an existing network security group called MyNSG and stores it in the $nsg variable.</span></span> <span data-ttu-id="09906-139">Polecenie Dalej powoduje przypisanie $nsg do $nic.</span><span class="sxs-lookup"><span data-stu-id="09906-139">The forth command assigns the $nsg to the $nic.</span></span> <span data-ttu-id="09906-140">Na koniec piąte polecenie powoduje zastosowanie zmian w interfejsie sieciowym.</span><span class="sxs-lookup"><span data-stu-id="09906-140">Finally, the fifth command applies the changes to the Network interface.</span></span> <span data-ttu-id="09906-141">Aby odłączyć grupy zabezpieczeń sieci od interfejsu sieciowego, proste polecenie Zamień $nsg w połączeniu z $null.</span><span class="sxs-lookup"><span data-stu-id="09906-141">To dissociate network security groups from a network interface, simple replace $nsg in the forth command with $null.</span></span>

## <span data-ttu-id="09906-142">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="09906-142">PARAMETERS</span></span>

### <span data-ttu-id="09906-143">-NetworkInterface</span><span class="sxs-lookup"><span data-stu-id="09906-143">-NetworkInterface</span></span>
<span data-ttu-id="09906-144">Określa obiekt **NetworkInterface** reprezentujący stan celu dla interfejsu sieciowego.</span><span class="sxs-lookup"><span data-stu-id="09906-144">Specifies a **NetworkInterface** object that represents the goal state for a network interface.</span></span>

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

### <span data-ttu-id="09906-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09906-145">-DefaultProfile</span></span>
<span data-ttu-id="09906-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="09906-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09906-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09906-147">CommonParameters</span></span>
<span data-ttu-id="09906-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09906-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09906-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09906-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09906-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="09906-150">INPUTS</span></span>

### <span data-ttu-id="09906-151">PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="09906-151">PSNetworkInterface</span></span>
<span data-ttu-id="09906-152">Parametr "NetworkInterface" akceptuje wartość typu "PSNetworkInterface" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="09906-152">Parameter 'NetworkInterface' accepts value of type 'PSNetworkInterface' from the pipeline</span></span>

## <span data-ttu-id="09906-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="09906-153">OUTPUTS</span></span>

### <span data-ttu-id="09906-154">Microsoft. Azure. Commands. Network. models. PSNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="09906-154">Microsoft.Azure.Commands.Network.Models.PSNetworkInterface</span></span>

## <span data-ttu-id="09906-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="09906-155">NOTES</span></span>

## <span data-ttu-id="09906-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="09906-156">RELATED LINKS</span></span>

[<span data-ttu-id="09906-157">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="09906-157">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="09906-158">Get-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="09906-158">Get-AzureRmNetworkInterface</span></span>](./Get-AzureRmNetworkInterface.md)

[<span data-ttu-id="09906-159">Nowe — AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="09906-159">New-AzureRmNetworkInterface</span></span>](./New-AzureRmNetworkInterface.md)

[<span data-ttu-id="09906-160">Remove-AzureRmNetworkInterface</span><span class="sxs-lookup"><span data-stu-id="09906-160">Remove-AzureRmNetworkInterface</span></span>](./Remove-AzureRmNetworkInterface.md)
