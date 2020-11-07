---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: 9ec81a9cf82851905d308fa0e0dd1fa45aeb7af9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542484"
---
# <span data-ttu-id="20da3-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="20da3-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>

## <span data-ttu-id="20da3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20da3-102">SYNOPSIS</span></span>
<span data-ttu-id="20da3-103">Ustawia pulę adresów klienta sieci VPN dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="20da3-103">Sets the VPN client address pool for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20da3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20da3-104">SYNTAX</span></span>

### <span data-ttu-id="20da3-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="20da3-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20da3-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="20da3-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20da3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="20da3-107">DESCRIPTION</span></span>
<span data-ttu-id="20da3-108">Polecenie cmdlet **Set-AzureRmVirtualNetworkVpnClientConfig** konfiguruje pulę adresów klienta dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="20da3-108">The **Set-AzureRmVirtualNetworkVpnClientConfig** cmdlet configures the client address pool for a virtual network gateway.</span></span>
<span data-ttu-id="20da3-109">Klientom wirtualnej sieci prywatnej (VPN) łączącym się z tą bramą będzie przypisywany adres IP z tej puli adresów.</span><span class="sxs-lookup"><span data-stu-id="20da3-109">Virtual private network (VPN) clients that connect to this gateway will be assigned an IP address from this address pool.</span></span>

## <span data-ttu-id="20da3-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20da3-110">EXAMPLES</span></span>

### <span data-ttu-id="20da3-111">Przykład 1: przypisywanie puli adresów klienta sieci VPN do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="20da3-111">Example 1: Assign a VPN client address pool to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

<span data-ttu-id="20da3-112">W tym przykładzie przypiszesz pulę adresów klienta sieci VPN do bramy sieci wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="20da3-112">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="20da3-113">Pierwsze polecenie tworzy odwołanie do obiektu do bramy, a obiekt jest przechowywany w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="20da3-113">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="20da3-114">Drugie polecenie w przykładzie używa polecenia cmdlet **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** w celu przypisania puli adresów 10.0.0.0/16 do ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="20da3-114">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span>

### <span data-ttu-id="20da3-115">Przykład 2: Konfigurowanie uwierzytelniania zewnętrznego opartego na usłudze RADIUS w istniejącej bramie</span><span class="sxs-lookup"><span data-stu-id="20da3-115">Example 2: Configure external radius based authentication on existing gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="20da3-116">W tym przykładzie przypiszesz pulę adresów klienta sieci VPN do bramy sieci wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="20da3-116">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>

<span data-ttu-id="20da3-117">Pierwsze polecenie tworzy odwołanie do obiektu do bramy, a obiekt jest przechowywany w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="20da3-117">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>

<span data-ttu-id="20da3-118">Drugie polecenie w przykładzie używa polecenia cmdlet **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** w celu przypisania puli adresów 10.0.0.0/16 do ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="20da3-118">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span> <span data-ttu-id="20da3-119">Ponadto konfiguruje zewnętrzny serwer RADIUS "TestRadiusServer", który ma być wykorzystywany do uwierzytelniania klientów VPN.</span><span class="sxs-lookup"><span data-stu-id="20da3-119">It also configures the external radius server "TestRadiusServer" to be used for authentication for vpn clients.</span></span>

## <span data-ttu-id="20da3-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20da3-120">PARAMETERS</span></span>

### <span data-ttu-id="20da3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20da3-121">-DefaultProfile</span></span>
<span data-ttu-id="20da3-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="20da3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20da3-123">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="20da3-123">-RadiusServerAddress</span></span>
<span data-ttu-id="20da3-124">P2S zewnętrzny adres serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="20da3-124">P2S External Radius server address.</span></span>

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

### <span data-ttu-id="20da3-125">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="20da3-125">-RadiusServerSecret</span></span>
<span data-ttu-id="20da3-126">P2S zewnętrznych kluczy tajnych serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="20da3-126">P2S External Radius server secret.</span></span>

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

### <span data-ttu-id="20da3-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20da3-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="20da3-128">Określa odwołanie do obiektu bramy sieci wirtualnej, które zawiera ustawienia konfiguracji klienta sieci VPN, które to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="20da3-128">Specifies an object reference to the virtual network gateway that contains the VPN client configuration settings that this cmdlet modifies.</span></span>
<span data-ttu-id="20da3-129">Odwołanie do obiektu bramy sieci wirtualnej można utworzyć przy użyciu Get-AzureRmVirtualNetworkGateway i określając nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="20da3-129">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

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

### <span data-ttu-id="20da3-130">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="20da3-130">-VpnClientAddressPool</span></span>
<span data-ttu-id="20da3-131">Określa adresy IP, które mają być przypisywane klientom łączącym się z tą bramą.</span><span class="sxs-lookup"><span data-stu-id="20da3-131">Specifies the IP addresses to be assigned to clients connecting to this gateway</span></span>

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

### <span data-ttu-id="20da3-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="20da3-132">-Confirm</span></span>
<span data-ttu-id="20da3-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20da3-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20da3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20da3-134">-WhatIf</span></span>
<span data-ttu-id="20da3-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20da3-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20da3-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="20da3-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20da3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20da3-137">CommonParameters</span></span>
<span data-ttu-id="20da3-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20da3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20da3-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20da3-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20da3-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20da3-140">INPUTS</span></span>

###  
<span data-ttu-id="20da3-141">To polecenie cmdlet akceptuje potokowe wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="20da3-141">This cmdlet accepts pipelined instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="20da3-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20da3-142">OUTPUTS</span></span>

###  
<span data-ttu-id="20da3-143">To polecenie cmdlet modyfikuje istniejące wystąpienia obiektu **Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway** .</span><span class="sxs-lookup"><span data-stu-id="20da3-143">This cmdlet modifies existing instances of the **Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway** object.</span></span>

## <span data-ttu-id="20da3-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20da3-144">NOTES</span></span>

## <span data-ttu-id="20da3-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20da3-145">RELATED LINKS</span></span>

[<span data-ttu-id="20da3-146">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="20da3-146">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="20da3-147">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20da3-147">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="20da3-148">Zmienianie rozmiaru — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="20da3-148">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)

