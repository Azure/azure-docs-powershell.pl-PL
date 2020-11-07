---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
ms.openlocfilehash: 6f22c8026d3b72a6c9cd52563252aa3d4bcad039
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898739"
---
# <span data-ttu-id="f2b50-101">Add-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f2b50-101">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="f2b50-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2b50-102">SYNOPSIS</span></span>
<span data-ttu-id="f2b50-103">Dodaje pulę adresów zaplecza do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f2b50-103">Adds a back-end address pool to an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2b50-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2b50-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2b50-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f2b50-105">DESCRIPTION</span></span>
<span data-ttu-id="f2b50-106">Polecenie cmdlet **Add-AzureRmApplicationGatewayBackendAddressPool** umożliwia dodanie puli adresów zaplecza do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f2b50-106">The **Add-AzureRmApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="f2b50-107">Adres zaplecza można określić przy użyciu adresu IP, w pełni kwalifikowanej nazwy domeny (FQDN) lub identyfikatora konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="f2b50-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="f2b50-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2b50-108">EXAMPLES</span></span>

### <span data-ttu-id="f2b50-109">Przykład 1: Dodawanie puli adresów zaplecza przy użyciu nazwy FQDN serwera zaplecza</span><span class="sxs-lookup"><span data-stu-id="f2b50-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="f2b50-110">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. Drugie polecenie dodaje pulę adresów zaplecza bram aplikacji przechowywaną w $AppGw przy użyciu nazw FQDN.</span><span class="sxs-lookup"><span data-stu-id="f2b50-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="f2b50-111">Przykład 2: Dodawanie puli adresów zaplecza przy użyciu adresów IP serwera zaplecza</span><span class="sxs-lookup"><span data-stu-id="f2b50-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add -AzureApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="f2b50-112">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. Drugie polecenie dodaje pulę adresów zaplecza bram aplikacji przechowywaną w $AppGw przy użyciu adresów IP.</span><span class="sxs-lookup"><span data-stu-id="f2b50-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="f2b50-113">Przykład 3: seta puli adresów zaplecza przy użyciu identyfikatora adresu IP serwera wewnętrznej bazy danych</span><span class="sxs-lookup"><span data-stu-id="f2b50-113">Example 3: Seta back-end address pool by using the ID of the backend server's IP address</span></span>
```
PS C:\>$Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="f2b50-114">Pierwsze polecenie pobiera obiekt interfejsu sieciowego o nazwie Nic01 należący do grupy zasobów o nazwie ResourceGroup01 i zapisuje go w zmiennej $Nic 01. Drugie polecenie pobiera obiekt interfejsu sieciowego o nazwie Nic02 należący do grupy zasobów o nazwie ResourceGroup02 i zapisuje go w zmiennej $Nic 02. Trzecia komenda uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. W poleceniu z są używane identyfikatory konfiguracji IP zaplecza z $Nic 01 i $Nic 02 w celu dodania puli adresów zaplecza bramy Application Gateway przechowywanej w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f2b50-114">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to add the back-end address pool of the application gateway stored in $AppGw.</span></span>

## <span data-ttu-id="f2b50-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2b50-115">PARAMETERS</span></span>

### <span data-ttu-id="f2b50-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2b50-116">-ApplicationGateway</span></span>
<span data-ttu-id="f2b50-117">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje pulę adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f2b50-117">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2b50-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="f2b50-118">-BackendFqdns</span></span>
<span data-ttu-id="f2b50-119">Określa listę nazw FQDN zaplecza, które to polecenie cmdlet dodaje jako pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f2b50-119">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b50-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="f2b50-120">-BackendIPAddresses</span></span>
<span data-ttu-id="f2b50-121">Określa listę wewnętrznych adresów IP, które to polecenie cmdlet dodaje jako pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f2b50-121">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b50-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2b50-122">-DefaultProfile</span></span>
<span data-ttu-id="f2b50-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2b50-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2b50-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f2b50-124">-Name</span></span>
<span data-ttu-id="f2b50-125">Określa nazwę puli serwerów zaplecza, którą dodaje polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2b50-125">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b50-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2b50-126">-Confirm</span></span>
<span data-ttu-id="f2b50-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2b50-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b50-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2b50-128">-WhatIf</span></span>
<span data-ttu-id="f2b50-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2b50-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2b50-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f2b50-130">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2b50-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2b50-131">CommonParameters</span></span>
<span data-ttu-id="f2b50-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2b50-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2b50-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2b50-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2b50-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2b50-134">INPUTS</span></span>

###  
<span data-ttu-id="f2b50-135">System. String</span><span class="sxs-lookup"><span data-stu-id="f2b50-135">System.String</span></span>

## <span data-ttu-id="f2b50-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2b50-136">OUTPUTS</span></span>

### <span data-ttu-id="f2b50-137">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f2b50-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f2b50-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2b50-138">NOTES</span></span>

## <span data-ttu-id="f2b50-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2b50-139">RELATED LINKS</span></span>

[<span data-ttu-id="f2b50-140">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f2b50-140">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f2b50-141">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f2b50-141">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f2b50-142">Nowe — AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f2b50-142">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f2b50-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f2b50-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f2b50-144">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f2b50-144">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Set-AzureRmApplicationGatewayBackendAddressPool.md)


