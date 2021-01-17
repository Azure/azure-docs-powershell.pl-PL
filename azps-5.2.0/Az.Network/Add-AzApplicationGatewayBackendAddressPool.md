---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 6FBFAEFF-786D-440A-94B2-8C27BE033A0A
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: c415fb890240ea6f4fb03b71c3a249eece1ba02b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98335266"
---
# <span data-ttu-id="dba73-101">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dba73-101">Add-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="dba73-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dba73-102">SYNOPSIS</span></span>
<span data-ttu-id="dba73-103">Dodaje pulę adresów zaplecza do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dba73-103">Adds a back-end address pool to an application gateway.</span></span>

## <span data-ttu-id="dba73-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dba73-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dba73-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dba73-105">DESCRIPTION</span></span>
<span data-ttu-id="dba73-106">Polecenie cmdlet **Add-AzApplicationGatewayBackendAddressPool** umożliwia dodanie puli adresów zaplecza do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="dba73-106">The **Add-AzApplicationGatewayBackendAddressPool** cmdlet adds a back-end address pool to an application gateway.</span></span>
<span data-ttu-id="dba73-107">Adres zaplecza można określić przy użyciu adresu IP, w pełni kwalifikowanej nazwy domeny (FQDN) lub identyfikatora konfiguracji IP.</span><span class="sxs-lookup"><span data-stu-id="dba73-107">A back-end address can be specified using an IP address, a fully-qualified domain name (FQDN) or IP configuration IDs.</span></span>

## <span data-ttu-id="dba73-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dba73-108">EXAMPLES</span></span>

### <span data-ttu-id="dba73-109">Przykład 1: Dodawanie puli adresów zaplecza przy użyciu nazwy FQDN serwera zaplecza</span><span class="sxs-lookup"><span data-stu-id="dba73-109">Example 1: Add a back-end address pool by using a back-end server FQDN</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", " contoso1.com"
```

<span data-ttu-id="dba73-110">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. Drugie polecenie dodaje pulę adresów zaplecza bram aplikacji przechowywaną w $AppGw przy użyciu nazw FQDN.</span><span class="sxs-lookup"><span data-stu-id="dba73-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="dba73-111">Przykład 2: Dodawanie puli adresów zaplecza przy użyciu adresów IP serwera zaplecza</span><span class="sxs-lookup"><span data-stu-id="dba73-111">Example 2: Add a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayBackendAddressPool -ApplicationGateway $ AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="dba73-112">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw. Drugie polecenie dodaje pulę adresów zaplecza bram aplikacji przechowywaną w $AppGw przy użyciu adresów IP.</span><span class="sxs-lookup"><span data-stu-id="dba73-112">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.The second command adds the back-end address pool of the application gateway stored in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="dba73-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dba73-113">PARAMETERS</span></span>

### <span data-ttu-id="dba73-114">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dba73-114">-ApplicationGateway</span></span>
<span data-ttu-id="dba73-115">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje pulę adresów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="dba73-115">Specifies the application gateway to which this cmdlet adds a back-end address pool.</span></span>

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

### <span data-ttu-id="dba73-116">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="dba73-116">-BackendFqdns</span></span>
<span data-ttu-id="dba73-117">Określa listę nazw FQDN zaplecza, które to polecenie cmdlet dodaje jako pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="dba73-117">Specifies a list of backend FQDNs which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="dba73-118">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="dba73-118">-BackendIPAddresses</span></span>
<span data-ttu-id="dba73-119">Określa listę wewnętrznych adresów IP, które to polecenie cmdlet dodaje jako pulę serwerów zaplecza.</span><span class="sxs-lookup"><span data-stu-id="dba73-119">Specifies a list of back-end IP addresses which this cmdlet adds as a back-end server pool.</span></span>

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

### <span data-ttu-id="dba73-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dba73-120">-DefaultProfile</span></span>
<span data-ttu-id="dba73-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dba73-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dba73-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dba73-122">-Name</span></span>
<span data-ttu-id="dba73-123">Określa nazwę puli serwerów zaplecza, którą dodaje polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dba73-123">Specifies the name of the back-end server pool that this cmdlet adds.</span></span>

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

### <span data-ttu-id="dba73-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dba73-124">-Confirm</span></span>
<span data-ttu-id="dba73-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dba73-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dba73-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dba73-126">-WhatIf</span></span>
<span data-ttu-id="dba73-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dba73-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dba73-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dba73-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dba73-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dba73-129">CommonParameters</span></span>
<span data-ttu-id="dba73-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dba73-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dba73-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dba73-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dba73-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dba73-132">INPUTS</span></span>

### <span data-ttu-id="dba73-133">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dba73-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dba73-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dba73-134">OUTPUTS</span></span>

### <span data-ttu-id="dba73-135">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="dba73-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="dba73-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dba73-136">NOTES</span></span>

## <span data-ttu-id="dba73-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dba73-137">RELATED LINKS</span></span>

[<span data-ttu-id="dba73-138">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dba73-138">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dba73-139">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dba73-139">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dba73-140">Nowe — AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dba73-140">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dba73-141">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dba73-141">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dba73-142">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="dba73-142">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="dba73-143">Set-AzNetworkInterfaceIpConfig</span><span class="sxs-lookup"><span data-stu-id="dba73-143">Set-AzNetworkInterfaceIpConfig</span></span>](./Set-AzNetworkInterfaceIpConfig.md)
