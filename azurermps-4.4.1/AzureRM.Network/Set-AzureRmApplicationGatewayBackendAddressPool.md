---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: dd5a0a14a0c2146ce6187a3ae08fda1bc3e60702
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719615"
---
# <span data-ttu-id="4d3ca-101">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4d3ca-101">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="4d3ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4d3ca-102">SYNOPSIS</span></span>
<span data-ttu-id="4d3ca-103">Aktualizuje pulę adresów zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-103">Updates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d3ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4d3ca-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d3ca-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4d3ca-105">DESCRIPTION</span></span>
<span data-ttu-id="4d3ca-106">Polecenie cmdlet **Set-AzureRmApplicationGatewayBackendAddressPool** umożliwia zaktualizowanie puli adresów zaplecza dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-106">The **Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="4d3ca-107">Adresy zaplecza można określać jako adresy IP, w pełni kwalifikowanych nazw domen (FQDN) lub identyfikatory konfiguracji adresów IP.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="4d3ca-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4d3ca-108">EXAMPLES</span></span>

### <span data-ttu-id="4d3ca-109">Przykład 1: Ustawianie puli adresów zaplecza przy użyciu nazw FQDN</span><span class="sxs-lookup"><span data-stu-id="4d3ca-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="4d3ca-110">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="4d3ca-111">Drugie polecenie umożliwia zaktualizowanie puli adresów zaplecza bramy aplikacji w $AppGw przy użyciu nazw FQDN.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="4d3ca-112">Przykład 2: Ustawianie puli adresów zaplecza przy użyciu adresów IP serwera zaplecza</span><span class="sxs-lookup"><span data-stu-id="4d3ca-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="4d3ca-113">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="4d3ca-114">Drugie polecenie umożliwia zaktualizowanie puli adresów zaplecza bramy aplikacji w $AppGw przy użyciu adresów IP.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="4d3ca-115">Przykład 3: Ustawianie puli adresów zaplecza przy użyciu identyfikatora adresu IP serwera wewnętrznej bazy danych</span><span class="sxs-lookup"><span data-stu-id="4d3ca-115">Example 3: Setting a back-end address pool by using the ID of the backend server?s IP address</span></span>
```
PS C:\>$Nic01 = Get-AzureRmNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzureRmNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="4d3ca-116">Pierwsze polecenie pobiera obiekt interfejsu sieciowego o nazwie Nic01 należący do grupy zasobów o nazwie ResourceGroup01 i zapisuje go w zmiennej $Nic 01.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-116">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.</span></span>

<span data-ttu-id="4d3ca-117">Drugie polecenie pobiera obiekt interfejsu sieciowego o nazwie Nic02 należący do grupy zasobów o nazwie ResourceGroup02 i zapisuje go w zmiennej $Nic 02.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-117">The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.</span></span>

<span data-ttu-id="4d3ca-118">Trzecia komenda uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-118">The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="4d3ca-119">W poleceniu z są używane identyfikatory konfiguracji IP zaplecza z $Nic 01 i $Nic 02 w celu zaktualizowania puli adresów zaplecza bramy aplikacji w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-119">The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to update the back-end address pool of the application gateway in $AppGw.</span></span>

## <span data-ttu-id="4d3ca-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4d3ca-120">PARAMETERS</span></span>

### <span data-ttu-id="4d3ca-121">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d3ca-121">-ApplicationGateway</span></span>
<span data-ttu-id="4d3ca-122">Określa bramę aplikacji, z którą to polecenie cmdlet kojarzy pulę adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-122">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="4d3ca-123">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="4d3ca-123">-BackendFqdns</span></span>
<span data-ttu-id="4d3ca-124">Określa listę wewnętrznych adresów IP, które mają być używane jako Pula serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-124">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="4d3ca-125">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="4d3ca-125">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="4d3ca-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4d3ca-126">-Name</span></span>
<span data-ttu-id="4d3ca-127">Określa nazwę puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-127">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="4d3ca-128">Ta pula adresów zaplecza musi istnieć w bramie Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-128">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="4d3ca-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d3ca-129">-Confirm</span></span>
<span data-ttu-id="4d3ca-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d3ca-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d3ca-131">-WhatIf</span></span>
<span data-ttu-id="4d3ca-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d3ca-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d3ca-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d3ca-134">-DefaultProfile</span></span>
<span data-ttu-id="4d3ca-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d3ca-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d3ca-136">CommonParameters</span></span>
<span data-ttu-id="4d3ca-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d3ca-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d3ca-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d3ca-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d3ca-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d3ca-139">INPUTS</span></span>

### <span data-ttu-id="4d3ca-140">System. String</span><span class="sxs-lookup"><span data-stu-id="4d3ca-140">System.String</span></span>

## <span data-ttu-id="4d3ca-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4d3ca-141">OUTPUTS</span></span>

### <span data-ttu-id="4d3ca-142">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4d3ca-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4d3ca-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4d3ca-143">NOTES</span></span>

## <span data-ttu-id="4d3ca-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d3ca-144">RELATED LINKS</span></span>

[<span data-ttu-id="4d3ca-145">Dodaj-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4d3ca-145">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4d3ca-146">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4d3ca-146">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4d3ca-147">Nowe — AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4d3ca-147">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="4d3ca-148">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="4d3ca-148">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)


