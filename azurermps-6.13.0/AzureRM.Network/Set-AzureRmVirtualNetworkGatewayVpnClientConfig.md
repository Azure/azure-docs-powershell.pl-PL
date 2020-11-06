---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: EFB0D7A6-0C8A-4514-873D-672641CCCAF3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermvirtualnetworkgatewayvpnclientconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmVirtualNetworkGatewayVpnClientConfig.md
ms.openlocfilehash: 6d2830836fd29edea2843fad4be1892edfa7fbb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543579"
---
# <span data-ttu-id="f976f-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span><span class="sxs-lookup"><span data-stu-id="f976f-101">Set-AzureRmVirtualNetworkGatewayVpnClientConfig</span></span>

## <span data-ttu-id="f976f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f976f-102">SYNOPSIS</span></span>
<span data-ttu-id="f976f-103">Ustawia pulę adresów klienta sieci VPN dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f976f-103">Sets the VPN client address pool for a virtual network gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f976f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f976f-104">SYNTAX</span></span>

### <span data-ttu-id="f976f-105">Domyślne (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f976f-105">Default (Default)</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f976f-106">RadiusServerConfiguration</span><span class="sxs-lookup"><span data-stu-id="f976f-106">RadiusServerConfiguration</span></span>
```
Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway <PSVirtualNetworkGateway>
 -VpnClientAddressPool <System.Collections.Generic.List`1[System.String]> -RadiusServerAddress <String>
 -RadiusServerSecret <SecureString> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f976f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f976f-107">DESCRIPTION</span></span>
<span data-ttu-id="f976f-108">Polecenie cmdlet **Set-AzureRmVirtualNetworkVpnClientConfig** konfiguruje pulę adresów klienta dla bramy sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f976f-108">The **Set-AzureRmVirtualNetworkVpnClientConfig** cmdlet configures the client address pool for a virtual network gateway.</span></span>
<span data-ttu-id="f976f-109">Klientom wirtualnej sieci prywatnej (VPN) łączącym się z tą bramą będzie przypisywany adres IP z tej puli adresów.</span><span class="sxs-lookup"><span data-stu-id="f976f-109">Virtual private network (VPN) clients that connect to this gateway will be assigned an IP address from this address pool.</span></span>

## <span data-ttu-id="f976f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f976f-110">EXAMPLES</span></span>

### <span data-ttu-id="f976f-111">Przykład 1: przypisywanie puli adresów klienta sieci VPN do bramy sieci wirtualnej</span><span class="sxs-lookup"><span data-stu-id="f976f-111">Example 1: Assign a VPN client address pool to a virtual network gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16"
```

<span data-ttu-id="f976f-112">W tym przykładzie przypiszesz pulę adresów klienta sieci VPN do bramy sieci wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="f976f-112">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="f976f-113">Pierwsze polecenie tworzy odwołanie do obiektu do bramy, a obiekt jest przechowywany w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="f976f-113">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="f976f-114">Drugie polecenie w przykładzie używa polecenia cmdlet **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** w celu przypisania puli adresów 10.0.0.0/16 do ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="f976f-114">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span>

### <span data-ttu-id="f976f-115">Przykład 2: Konfigurowanie uwierzytelniania zewnętrznego opartego na usłudze RADIUS w istniejącej bramie</span><span class="sxs-lookup"><span data-stu-id="f976f-115">Example 2: Configure external radius based authentication on existing gateway</span></span>
```
PS C:\>$Gateway = Get-AzureRmVirtualNetworkGateway -Name "ContosoVirtualGateway"
PS C:\> $Secure_String_Pwd = ConvertTo-SecureString "TestRadiusServerPassword" -AsPlainText -Force
PS C:\> Set-AzureRmVirtualNetworkGatewayVpnClientConfig -VirtualNetworkGateway $Gateway -VpnClientAddressPool "10.0.0.0/16" -RadiusServerAddress "TestRadiusServer" -RadiusServerSecret $Secure_String_Pwd
```

<span data-ttu-id="f976f-116">W tym przykładzie przypiszesz pulę adresów klienta sieci VPN do bramy sieci wirtualnej o nazwie ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="f976f-116">This example assigns a VPN client address pool to a virtual network gateway named ContosoVirtualGateway.</span></span>
<span data-ttu-id="f976f-117">Pierwsze polecenie tworzy odwołanie do obiektu do bramy, a obiekt jest przechowywany w zmiennej o nazwie $Gateway.</span><span class="sxs-lookup"><span data-stu-id="f976f-117">The first command creates an object reference to the gateway and the object is stored in a variable named $Gateway.</span></span>
<span data-ttu-id="f976f-118">Drugie polecenie w przykładzie używa polecenia cmdlet **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** w celu przypisania puli adresów 10.0.0.0/16 do ContosoVirtualGateway.</span><span class="sxs-lookup"><span data-stu-id="f976f-118">The second command in the example then uses the **Set-AzureRmVirtualNetworkGatewayVpnClientConfig** cmdlet to assign the address pool 10.0.0.0/16 to ContosoVirtualGateway.</span></span> <span data-ttu-id="f976f-119">Ponadto konfiguruje zewnętrzny serwer RADIUS "TestRadiusServer", który ma być wykorzystywany do uwierzytelniania klientów VPN.</span><span class="sxs-lookup"><span data-stu-id="f976f-119">It also configures the external radius server "TestRadiusServer" to be used for authentication for vpn clients.</span></span>

## <span data-ttu-id="f976f-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f976f-120">PARAMETERS</span></span>

### <span data-ttu-id="f976f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f976f-121">-DefaultProfile</span></span>
<span data-ttu-id="f976f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f976f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f976f-123">-RadiusServerAddress</span><span class="sxs-lookup"><span data-stu-id="f976f-123">-RadiusServerAddress</span></span>
<span data-ttu-id="f976f-124">P2S zewnętrzny adres serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="f976f-124">P2S External Radius server address.</span></span>

```yaml
Type: System.String
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f976f-125">-RadiusServerSecret</span><span class="sxs-lookup"><span data-stu-id="f976f-125">-RadiusServerSecret</span></span>
<span data-ttu-id="f976f-126">P2S zewnętrznych kluczy tajnych serwera RADIUS.</span><span class="sxs-lookup"><span data-stu-id="f976f-126">P2S External Radius server secret.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RadiusServerConfiguration
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f976f-127">-VirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f976f-127">-VirtualNetworkGateway</span></span>
<span data-ttu-id="f976f-128">Określa odwołanie do obiektu bramy sieci wirtualnej, które zawiera ustawienia konfiguracji klienta sieci VPN, które to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="f976f-128">Specifies an object reference to the virtual network gateway that contains the VPN client configuration settings that this cmdlet modifies.</span></span>
<span data-ttu-id="f976f-129">Odwołanie do obiektu bramy sieci wirtualnej można utworzyć przy użyciu Get-AzureRmVirtualNetworkGateway i określając nazwę bramy.</span><span class="sxs-lookup"><span data-stu-id="f976f-129">You can create an object reference to a virtual network gateway by using the Get-AzureRmVirtualNetworkGateway and specifying the name of the gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f976f-130">-VpnClientAddressPool</span><span class="sxs-lookup"><span data-stu-id="f976f-130">-VpnClientAddressPool</span></span>
<span data-ttu-id="f976f-131">Określa adresy IP, które mają być przypisywane klientom łączącym się z tą bramą.</span><span class="sxs-lookup"><span data-stu-id="f976f-131">Specifies the IP addresses to be assigned to clients connecting to this gateway</span></span>

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

### <span data-ttu-id="f976f-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f976f-132">-Confirm</span></span>
<span data-ttu-id="f976f-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f976f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f976f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f976f-134">-WhatIf</span></span>
<span data-ttu-id="f976f-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f976f-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f976f-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f976f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f976f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f976f-137">CommonParameters</span></span>
<span data-ttu-id="f976f-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f976f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f976f-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f976f-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f976f-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f976f-140">INPUTS</span></span>

### <span data-ttu-id="f976f-141">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f976f-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>
<span data-ttu-id="f976f-142">Parametry: VirtualNetworkGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f976f-142">Parameters: VirtualNetworkGateway (ByValue)</span></span>

### <span data-ttu-id="f976f-143">System. Collections. Generic. list "1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f976f-143">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f976f-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f976f-144">System.String</span></span>

### <span data-ttu-id="f976f-145">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="f976f-145">System.Security.SecureString</span></span>

## <span data-ttu-id="f976f-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f976f-146">OUTPUTS</span></span>

### <span data-ttu-id="f976f-147">Microsoft. Azure. Commands. Network. models. PSVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f976f-147">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="f976f-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f976f-148">NOTES</span></span>

## <span data-ttu-id="f976f-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f976f-149">RELATED LINKS</span></span>

[<span data-ttu-id="f976f-150">Get-AzureRmVpnClientPackage</span><span class="sxs-lookup"><span data-stu-id="f976f-150">Get-AzureRmVpnClientPackage</span></span>](./Get-AzureRmVpnClientPackage.md)

[<span data-ttu-id="f976f-151">Get-AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f976f-151">Get-AzureRmVirtualNetworkGateway</span></span>](./Get-AzureRmVirtualNetworkGateway.md)

[<span data-ttu-id="f976f-152">Zmienianie rozmiaru — AzureRmVirtualNetworkGateway</span><span class="sxs-lookup"><span data-stu-id="f976f-152">Resize-AzureRmVirtualNetworkGateway</span></span>](./Resize-AzureRmVirtualNetworkGateway.md)


