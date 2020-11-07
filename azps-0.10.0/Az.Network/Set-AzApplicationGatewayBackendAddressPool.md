---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: fd9d9c1b7956c16ab981b5426e9453de4d730dd6
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892861"
---
# <span data-ttu-id="f25a1-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f25a1-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="f25a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f25a1-102">SYNOPSIS</span></span>
<span data-ttu-id="f25a1-103">Aktualizuje pulę adresów zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f25a1-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="f25a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f25a1-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f25a1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f25a1-105">DESCRIPTION</span></span>
<span data-ttu-id="f25a1-106">Polecenie cmdlet **Set-AzApplicationGatewayBackendAddressPool** umożliwia zaktualizowanie puli adresów zaplecza dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f25a1-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="f25a1-107">Adresy zaplecza można określać jako adresy IP, w pełni kwalifikowanych nazw domen (FQDN) lub identyfikatory konfiguracji adresów IP.</span><span class="sxs-lookup"><span data-stu-id="f25a1-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="f25a1-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f25a1-108">EXAMPLES</span></span>

### <span data-ttu-id="f25a1-109">Przykład 1: Ustawianie puli adresów zaplecza przy użyciu nazw FQDN</span><span class="sxs-lookup"><span data-stu-id="f25a1-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="f25a1-110">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f25a1-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f25a1-111">Drugie polecenie umożliwia zaktualizowanie puli adresów zaplecza bramy aplikacji w $AppGw przy użyciu nazw FQDN.</span><span class="sxs-lookup"><span data-stu-id="f25a1-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="f25a1-112">Przykład 2: Ustawianie puli adresów zaplecza przy użyciu adresów IP serwera zaplecza</span><span class="sxs-lookup"><span data-stu-id="f25a1-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="f25a1-113">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f25a1-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f25a1-114">Drugie polecenie umożliwia zaktualizowanie puli adresów zaplecza bramy aplikacji w $AppGw przy użyciu adresów IP.</span><span class="sxs-lookup"><span data-stu-id="f25a1-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

### <span data-ttu-id="f25a1-115">Przykład 3: Ustawianie puli adresów zaplecza przy użyciu identyfikatora adresu IP serwera wewnętrznej bazy danych</span><span class="sxs-lookup"><span data-stu-id="f25a1-115">Example 3: Setting a back-end address pool by using the ID of the backend server?s IP address</span></span>
```
PS C:\> $Nic01 = Get-AzNetworkInterface -Name "Nic01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Nic02 = Get-AzNetworkInterface -Name "Nic02" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPConfigurationIds $nic01.Properties.IpConfigurations[0].Id, $nic02.Properties.IpConfiguration[0].Id
```

<span data-ttu-id="f25a1-116">Pierwsze polecenie pobiera obiekt interfejsu sieciowego o nazwie Nic01 należący do grupy zasobów o nazwie ResourceGroup01 i zapisuje go w zmiennej $Nic 01.</span><span class="sxs-lookup"><span data-stu-id="f25a1-116">The first command gets a network interface object named Nic01 that belongs to the resource group named ResourceGroup01, and stores it in the $Nic01 variable.</span></span>

<span data-ttu-id="f25a1-117">Drugie polecenie pobiera obiekt interfejsu sieciowego o nazwie Nic02 należący do grupy zasobów o nazwie ResourceGroup02 i zapisuje go w zmiennej $Nic 02.</span><span class="sxs-lookup"><span data-stu-id="f25a1-117">The second command gets a network interface object named Nic02 that belongs to the resource group named ResourceGroup02, and stores it in the $Nic02 variable.</span></span>

<span data-ttu-id="f25a1-118">Trzecia komenda uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f25a1-118">The third command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="f25a1-119">W poleceniu z są używane identyfikatory konfiguracji IP zaplecza z $Nic 01 i $Nic 02 w celu zaktualizowania puli adresów zaplecza bramy aplikacji w $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f25a1-119">The forth command uses the back-end IP configuration IDs from $Nic01 and $Nic02 to update the back-end address pool of the application gateway in $AppGw.</span></span>

## <span data-ttu-id="f25a1-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f25a1-120">PARAMETERS</span></span>

### <span data-ttu-id="f25a1-121">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f25a1-121">-ApplicationGateway</span></span>
<span data-ttu-id="f25a1-122">Określa bramę aplikacji, z którą to polecenie cmdlet kojarzy pulę adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f25a1-122">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="f25a1-123">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="f25a1-123">-BackendFqdns</span></span>
<span data-ttu-id="f25a1-124">Określa listę wewnętrznych adresów IP, które mają być używane jako Pula serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f25a1-124">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="f25a1-125">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="f25a1-125">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="f25a1-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f25a1-126">-DefaultProfile</span></span>
<span data-ttu-id="f25a1-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f25a1-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f25a1-128">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f25a1-128">-Name</span></span>
<span data-ttu-id="f25a1-129">Określa nazwę puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f25a1-129">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="f25a1-130">Ta pula adresów zaplecza musi istnieć w bramie Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f25a1-130">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="f25a1-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f25a1-131">-Confirm</span></span>
<span data-ttu-id="f25a1-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f25a1-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f25a1-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f25a1-133">-WhatIf</span></span>
<span data-ttu-id="f25a1-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f25a1-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f25a1-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f25a1-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f25a1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f25a1-136">CommonParameters</span></span>
<span data-ttu-id="f25a1-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f25a1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f25a1-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f25a1-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f25a1-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f25a1-139">INPUTS</span></span>

### <span data-ttu-id="f25a1-140">System. String</span><span class="sxs-lookup"><span data-stu-id="f25a1-140">System.String</span></span>

## <span data-ttu-id="f25a1-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f25a1-141">OUTPUTS</span></span>

### <span data-ttu-id="f25a1-142">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f25a1-142">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f25a1-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f25a1-143">NOTES</span></span>

## <span data-ttu-id="f25a1-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f25a1-144">RELATED LINKS</span></span>

[<span data-ttu-id="f25a1-145">Dodaj-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f25a1-145">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f25a1-146">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f25a1-146">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f25a1-147">Nowe — AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f25a1-147">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="f25a1-148">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="f25a1-148">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


