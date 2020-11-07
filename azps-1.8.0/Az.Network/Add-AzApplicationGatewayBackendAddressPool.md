---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: e59f09d44c1d6003122992cb5f14f51b411be25e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709721"
---
# <span data-ttu-id="21bdc-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="21bdc-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="21bdc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21bdc-102">SYNOPSIS</span></span>
<span data-ttu-id="21bdc-103">Dodaje pulę adresów zaplecza do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="21bdc-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="21bdc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21bdc-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21bdc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="21bdc-105">DESCRIPTION</span></span>
<span data-ttu-id="21bdc-106">Polecenie cmdlet **Add-AzApplicationGatewayBackendAddressPool** umożliwia dodanie puli adresów zaplecza do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="21bdc-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="21bdc-107">Adres zaplecza można określić przy użyciu adresu IP, w pełni kwalifikowanej nazwy domeny (FQDN) lub identyfikatora konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="21bdc-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="21bdc-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21bdc-108">EXAMPLES</span></span>

### <span data-ttu-id="21bdc-109">Przykład 1: Dodawanie puli adresów zaplecza przy użyciu nazwy FQDN serwera zaplecza</span><span class="sxs-lookup"><span data-stu-id="21bdc-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="21bdc-110">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. Drugie polecenie dodaje pulę adresów zaplecza bram aplikacji przechowywaną w $AppGw przy użyciu nazw FQDN.</span><span class="sxs-lookup"><span data-stu-id="21bdc-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="21bdc-111">Przykład 2: Dodawanie puli adresów zaplecza przy użyciu adresów IP serwera zaplecza</span><span class="sxs-lookup"><span data-stu-id="21bdc-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add -AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="21bdc-112">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. Drugie polecenie dodaje pulę adresów zaplecza bram aplikacji przechowywaną w $AppGw przy użyciu adresów IP.</span><span class="sxs-lookup"><span data-stu-id="21bdc-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="21bdc-113">Przykład 3: seta puli adresów zaplecza przy użyciu identyfikatora adresu IP serwera wewnętrznej bazy danych</span><span class="sxs-lookup"><span data-stu-id="21bdc-113">Example 3: Seta back-end address pool by using the ID of the backend server's IP address</span></span>
```
PS C:\>$Nic01 = Get-AzNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="21bdc-114">Pierwsze polecenie pobiera obiekt interfejsu sieciowego o nazwie Nic01 należący do grupy zasobów o nazwie ResourceGroup01 i zapisuje go w zmiennej $Nic 01. Drugie polecenie pobiera obiekt interfejsu sieciowego o nazwie Nic02 należący do grupy zasobów o nazwie ResourceGroup02 i zapisuje go w zmiennej $Nic 02. Trzecia komenda uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. W poleceniu z są używane identyfikatory konfiguracji IP zaplecza z $Nic 01 i $Nic 02 w celu dodania puli adresów zaplecza bramy Application Gateway przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="21bdc-114">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to add the back-end address pool of the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="21bdc-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21bdc-115">PARAMETERS</span></span>

### <span data-ttu-id="21bdc-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="21bdc-116">-ApplicationGateway</span></span>
<span data-ttu-id="21bdc-117">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje pulę adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="21bdc-117">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="21bdc-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="21bdc-118">-BackendFqdns</span></span>
<span data-ttu-id="21bdc-119">Określa listę nazw FQDN zaplecza, które to polecenie cmdlet dodaje jako pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="21bdc-119">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21bdc-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="21bdc-120">-BackendIPAddresses</span></span>
<span data-ttu-id="21bdc-121">Określa listę wewnętrznych adresów IP, które to polecenie cmdlet dodaje jako pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="21bdc-121">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21bdc-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21bdc-122">-DefaultProfile</span></span>
<span data-ttu-id="21bdc-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21bdc-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21bdc-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21bdc-124">-Name</span></span>
<span data-ttu-id="21bdc-125">Określa nazwę puli serwerów zaplecza, którą dodaje polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21bdc-125">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21bdc-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="21bdc-126">-Confirm</span></span>
<span data-ttu-id="21bdc-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21bdc-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21bdc-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21bdc-128">-WhatIf</span></span>
<span data-ttu-id="21bdc-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="21bdc-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21bdc-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="21bdc-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21bdc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21bdc-131">CommonParameters</span></span>
<span data-ttu-id="21bdc-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21bdc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21bdc-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21bdc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21bdc-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21bdc-134">INPUTS</span></span>

### <span data-ttu-id="21bdc-135">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="21bdc-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="21bdc-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21bdc-136">OUTPUTS</span></span>

### <span data-ttu-id="21bdc-137">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="21bdc-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="21bdc-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21bdc-138">NOTES</span></span>

## <span data-ttu-id="21bdc-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21bdc-139">RELATED LINKS</span></span>

[<span data-ttu-id="21bdc-140">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="21bdc-140">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="21bdc-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="21bdc-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="21bdc-142">Nowe — AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="21bdc-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="21bdc-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="21bdc-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="21bdc-144">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="21bdc-144">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


