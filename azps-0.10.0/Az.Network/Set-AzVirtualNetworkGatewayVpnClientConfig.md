---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: 1c85bc5e2a935378630728083b19544ace8670b4
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892693"
---
# <span data-ttu-id="2c12d-101">Set-AzVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="2c12d-101">Set-AzVirtualNetworkGatewayVpnClientConfig</span></span>

## <span data-ttu-id="2c12d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2c12d-102">SYNOPSIS</span></span>
<span data-ttu-id="2c12d-103">Ustawia pulę adresów klienta sieci VPN dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2c12d-103">Sets the VPN client address pool for a virtual network gateway.</span></span>

## <span data-ttu-id="2c12d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2c12d-104">SYNTAX</span></span>

### <span data-ttu-id="2c12d-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2c12d-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c12d-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="2c12d-106">RadiusServerConfiguration</span></span>
```
Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2c12d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2c12d-107">DESCRIPTION</span></span>
<span data-ttu-id="2c12d-108">Polecenie cmdlet **Set-AzVirtualNetworkVpnClientConfig** konfiguruje pulę adresów klienta dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2c12d-108">The **Set-AzVirtualNetworkVpnClientConfig** cmdlet configures the client address pool for a virtual network gateway.</span></span>
<span data-ttu-id="2c12d-109">Klientom wirtualnej sieci prywatnej (VPN) łączącym się z tą bramą będzie przypisywany adres IP z tej puli adresów.</span><span class="sxs-lookup"><span data-stu-id="2c12d-109">Virtual private network (VPN) clients that connect to this gateway will be assigned an IP address from this address pool.</span></span>

## <span data-ttu-id="2c12d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2c12d-110">EXAMPLES</span></span>

### <span data-ttu-id="2c12d-111">Przykład 1: przypisywanie puli adresów klienta sieci VPN do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="2c12d-111">Example 1: Assign a VPN client address pool to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

<span data-ttu-id="2c12d-112">W tym przykładzie przypiszesz pulę adresów klienta sieci VPN do bramy sieci wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="2c12d-112">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="2c12d-113">Pierwsze polecenie tworzy odwołanie do obiektu do bramy, a obiekt jest przechowywany w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="2c12d-113">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="2c12d-114">Drugie polecenie w przykładzie używa polecenia cmdlet **Set-AzVirtualNetworkGatewayVpnClientConfig** w celu przypisania puli adresów 10.0.0.0/16 do ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="2c12d-114">The second command in the example then uses the **Set-AzVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span>

### <span data-ttu-id="2c12d-115">Przykład 2: Konfigurowanie uwierzytelniania zewnętrznego opartego na usłudze RADIUS w istniejącej bramie</span><span class="sxs-lookup"><span data-stu-id="2c12d-115">Example 2: Configure external radius based authentication on existing gateway</span></span>
```
PS C:\>$Gateway = Get-AzVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="2c12d-116">W tym przykładzie przypiszesz pulę adresów klienta sieci VPN do bramy sieci wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="2c12d-116">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="2c12d-117">Pierwsze polecenie tworzy odwołanie do obiektu do bramy, a obiekt jest przechowywany w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="2c12d-117">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="2c12d-118">Drugie polecenie w przykładzie używa polecenia cmdlet **Set-AzVirtualNetworkGatewayVpnClientConfig** w celu przypisania puli adresów 10.0.0.0/16 do ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="2c12d-118">The second command in the example then uses the **Set-AzVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span> <span data-ttu-id="2c12d-119">Ponadto konfiguruje zewnętrzny serwer RADIUS "TestRadiusServer", który ma być wykorzystywany do uwierzytelniania klientów VPN.</span><span class="sxs-lookup"><span data-stu-id="2c12d-119">It also configures the external radius server "TestRadiusServer" to be used for authentication for vpn clients.</span></span>

## <span data-ttu-id="2c12d-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2c12d-120">PARAMETERS</span></span>

### <span data-ttu-id="2c12d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c12d-121">-DefaultProfile</span></span>
<span data-ttu-id="2c12d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c12d-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c12d-123">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="2c12d-123">-RadiusServerAddress</span></span>
<span data-ttu-id="2c12d-124">P2S zewnętrzny adres serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="2c12d-124">P2S External Radius server address.</span></span>

```yaml
Type: String
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c12d-125">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="2c12d-125">-RadiusServerSecret</span></span>
<span data-ttu-id="2c12d-126">P2S zewnętrznych kluczy tajnych serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="2c12d-126">P2S External Radius server secret.</span></span>

```yaml
Type: SecureString
Parameter Sets: RadiusServerConfiguration
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c12d-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2c12d-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="2c12d-128">Określa odwołanie do obiektu bramy sieci wirtualnej, które zawiera ustawienia konfiguracji klienta sieci VPN, które to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="2c12d-128">Specifies an object reference to the virtual network gateway that contains the VPN client configuration settings that this cmdlet modifies.</span></span>
<span data-ttu-id="2c12d-129">Odwołanie do obiektu bramy sieci wirtualnej można utworzyć przy użyciu Get-AzVirtualNetworkGateway i określając nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="2c12d-129">You can create an object reference to a virtual network gateway by using the Get-AzVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c12d-130">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="2c12d-130">-VpnClientAddressPool</span></span>
<span data-ttu-id="2c12d-131">Określa adresy IP, które mają być przypisywane klientom łączącym się z tą bramą.</span><span class="sxs-lookup"><span data-stu-id="2c12d-131">Specifies the IP addresses to be assigned to clients connecting to this gateway</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c12d-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2c12d-132">-Confirm</span></span>
<span data-ttu-id="2c12d-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c12d-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c12d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c12d-134">-WhatIf</span></span>
<span data-ttu-id="2c12d-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c12d-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c12d-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2c12d-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c12d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c12d-137">CommonParameters</span></span>
<span data-ttu-id="2c12d-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c12d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c12d-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2c12d-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c12d-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c12d-140">INPUTS</span></span>

###  
<span data-ttu-id="2c12d-141">To polecenie cmdlet akceptuje potokowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="2c12d-141">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="2c12d-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2c12d-142">OUTPUTS</span></span>

###  
<span data-ttu-id="2c12d-143">To polecenie cmdlet modyfikuje istniejące wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="2c12d-143">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="2c12d-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2c12d-144">NOTES</span></span>

## <span data-ttu-id="2c12d-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c12d-145">RELATED LINKS</span></span>

[<span data-ttu-id="2c12d-146">Get-AzVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="2c12d-146">Get-AzVpnClientPackage</span></span>](./Get-AzVpnClientPackage.md)

[<span data-ttu-id="2c12d-147">Get-AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2c12d-147">Get-AzVirtualNetworkGateway</span></span>](./Get-AzVirtualNetworkGateway.md)

[<span data-ttu-id="2c12d-148">Zmienianie rozmiaru — AzVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="2c12d-148">Resize-AzVirtualNetworkGateway</span></span>](./Resize-AzVirtualNetworkGateway.md)


