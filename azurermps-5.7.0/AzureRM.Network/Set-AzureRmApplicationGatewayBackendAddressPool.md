---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: bafc55d3e630b936d2d30efa168f60919cc6c69d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719573"
---
# <span data-ttu-id="1abb3-101">Set-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1abb3-101">Set-AzureRmApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="1abb3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1abb3-102">SYNOPSIS</span></span>
<span data-ttu-id="1abb3-103">Aktualizuje pulę adresów zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="1abb3-103">Updates a back-end address pool for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1abb3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1abb3-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <System.Collections.Generic.List`1[System.String]>]
 [-BackendFqdns <System.Collections.Generic.List`1[System.String]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1abb3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1abb3-105">DESCRIPTION</span></span>
<span data-ttu-id="1abb3-106">Polecenie cmdlet **Set-AzureRmApplicationGatewayBackendAddressPool** umożliwia zaktualizowanie puli adresów zaplecza dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1abb3-106">The **Set-AzureRmApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="1abb3-107">Adresy zaplecza można określać jako adresy IP, w pełni kwalifikowanych nazw domen (FQDN) lub identyfikatory konfiguracji adresów IP.</span><span class="sxs-lookup"><span data-stu-id="1abb3-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="1abb3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1abb3-108">EXAMPLES</span></span>

### <span data-ttu-id="1abb3-109">Przykład 1: Ustawianie puli adresów zaplecza przy użyciu nazw FQDN</span><span class="sxs-lookup"><span data-stu-id="1abb3-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="1abb3-110">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1abb3-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="1abb3-111">Drugie polecenie umożliwia zaktualizowanie puli adresów zaplecza bramy aplikacji w $AppGw przy użyciu nazw FQDN.</span><span class="sxs-lookup"><span data-stu-id="1abb3-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="1abb3-112">Przykład 2: Ustawianie puli adresów zaplecza przy użyciu adresów IP serwera zaplecza</span><span class="sxs-lookup"><span data-stu-id="1abb3-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="1abb3-113">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="1abb3-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="1abb3-114">Drugie polecenie umożliwia zaktualizowanie puli adresów zaplecza bramy aplikacji w $AppGw przy użyciu adresów IP.</span><span class="sxs-lookup"><span data-stu-id="1abb3-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="1abb3-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1abb3-115">PARAMETERS</span></span>

### <span data-ttu-id="1abb3-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1abb3-116">-ApplicationGateway</span></span>
<span data-ttu-id="1abb3-117">Określa bramę aplikacji, z którą to polecenie cmdlet kojarzy pulę adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="1abb3-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="1abb3-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="1abb3-118">-BackendFqdns</span></span>
<span data-ttu-id="1abb3-119">Określa listę wewnętrznych adresów IP, które mają być używane jako Pula serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="1abb3-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="1abb3-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="1abb3-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="1abb3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1abb3-121">-DefaultProfile</span></span>
<span data-ttu-id="1abb3-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1abb3-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1abb3-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1abb3-123">-Name</span></span>
<span data-ttu-id="1abb3-124">Określa nazwę puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="1abb3-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="1abb3-125">Ta pula adresów zaplecza musi istnieć w bramie Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="1abb3-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="1abb3-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1abb3-126">-Confirm</span></span>
<span data-ttu-id="1abb3-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1abb3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1abb3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1abb3-128">-WhatIf</span></span>
<span data-ttu-id="1abb3-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1abb3-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1abb3-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1abb3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1abb3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1abb3-131">CommonParameters</span></span>
<span data-ttu-id="1abb3-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1abb3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1abb3-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1abb3-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1abb3-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1abb3-134">INPUTS</span></span>

### <span data-ttu-id="1abb3-135">System. String</span><span class="sxs-lookup"><span data-stu-id="1abb3-135">System.String</span></span>

## <span data-ttu-id="1abb3-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1abb3-136">OUTPUTS</span></span>

### <span data-ttu-id="1abb3-137">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1abb3-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1abb3-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1abb3-138">NOTES</span></span>

## <span data-ttu-id="1abb3-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1abb3-139">RELATED LINKS</span></span>

[<span data-ttu-id="1abb3-140">Dodaj-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1abb3-140">Add-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Add-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="1abb3-141">Get-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1abb3-141">Get-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Get-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="1abb3-142">Nowe — AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1abb3-142">New-AzureRmApplicationGatewayBackendAddressPool</span></span>](./New-AzureRmApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="1abb3-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="1abb3-143">Remove-AzureRmApplicationGatewayBackendAddressPool</span></span>](./Remove-AzureRmApplicationGatewayBackendAddressPool.md)


