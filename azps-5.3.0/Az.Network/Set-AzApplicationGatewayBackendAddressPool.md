---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: a5b0fa1054136354725ec404960bcf680a104d06
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504415"
---
# <span data-ttu-id="b9697-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b9697-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="b9697-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b9697-102">SYNOPSIS</span></span>
<span data-ttu-id="b9697-103">Aktualizuje pulę adresów zaplecza dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="b9697-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="b9697-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b9697-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b9697-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b9697-105">DESCRIPTION</span></span>
<span data-ttu-id="b9697-106">Polecenie cmdlet **Set-AzApplicationGatewayBackendAddressPool** umożliwia zaktualizowanie puli adresów zaplecza dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b9697-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="b9697-107">Adresy zaplecza można określać jako adresy IP, w pełni kwalifikowanych nazw domen (FQDN) lub identyfikatory konfiguracji adresów IP.</span><span class="sxs-lookup"><span data-stu-id="b9697-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="b9697-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b9697-108">EXAMPLES</span></span>

### <span data-ttu-id="b9697-109">Przykład 1: Ustawianie puli adresów zaplecza przy użyciu nazw FQDN</span><span class="sxs-lookup"><span data-stu-id="b9697-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="b9697-110">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b9697-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b9697-111">Drugie polecenie umożliwia zaktualizowanie puli adresów zaplecza bramy aplikacji w $AppGw przy użyciu nazw FQDN.</span><span class="sxs-lookup"><span data-stu-id="b9697-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="b9697-112">Przykład 2: Ustawianie puli adresów zaplecza przy użyciu adresów IP serwera zaplecza</span><span class="sxs-lookup"><span data-stu-id="b9697-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="b9697-113">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="b9697-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="b9697-114">Drugie polecenie umożliwia zaktualizowanie puli adresów zaplecza bramy aplikacji w $AppGw przy użyciu adresów IP.</span><span class="sxs-lookup"><span data-stu-id="b9697-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="b9697-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b9697-115">PARAMETERS</span></span>

### <span data-ttu-id="b9697-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9697-116">-ApplicationGateway</span></span>
<span data-ttu-id="b9697-117">Określa bramę aplikacji, z którą to polecenie cmdlet kojarzy pulę adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b9697-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="b9697-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="b9697-118">-BackendFqdns</span></span>
<span data-ttu-id="b9697-119">Określa listę wewnętrznych adresów IP, które mają być używane jako Pula serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b9697-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="b9697-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="b9697-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="b9697-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b9697-121">-DefaultProfile</span></span>
<span data-ttu-id="b9697-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b9697-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b9697-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b9697-123">-Name</span></span>
<span data-ttu-id="b9697-124">Określa nazwę puli adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b9697-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="b9697-125">Ta pula adresów zaplecza musi istnieć w bramie Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="b9697-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="b9697-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b9697-126">-Confirm</span></span>
<span data-ttu-id="b9697-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9697-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b9697-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b9697-128">-WhatIf</span></span>
<span data-ttu-id="b9697-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b9697-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b9697-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b9697-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b9697-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b9697-131">CommonParameters</span></span>
<span data-ttu-id="b9697-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b9697-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b9697-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b9697-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b9697-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b9697-134">INPUTS</span></span>

### <span data-ttu-id="b9697-135">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9697-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9697-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b9697-136">OUTPUTS</span></span>

### <span data-ttu-id="b9697-137">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="b9697-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="b9697-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b9697-138">NOTES</span></span>

## <span data-ttu-id="b9697-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b9697-139">RELATED LINKS</span></span>

[<span data-ttu-id="b9697-140">Dodaj-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b9697-140">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b9697-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b9697-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b9697-142">Nowe — AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b9697-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="b9697-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="b9697-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


