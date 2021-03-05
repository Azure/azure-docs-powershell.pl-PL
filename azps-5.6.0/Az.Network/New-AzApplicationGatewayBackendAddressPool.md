---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C257E62F-1535-4626-A12B-F4572D00BB13
online version: https://docs.microsoft.com/powershell/module/az.network/new-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 3ce9cb761bb945c777a39e728ac8ebea2c40b885
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010353"
---
# <span data-ttu-id="a8ad8-101">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a8ad8-101">New-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="a8ad8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a8ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="a8ad8-103">Tworzy pulę adresów back-end dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="a8ad8-103">Creates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="a8ad8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a8ad8-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendAddressPool -Name <String> [-BackendIPAddresses <String[]>]
 [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a8ad8-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a8ad8-105">DESCRIPTION</span></span>
<span data-ttu-id="a8ad8-106">Polecenie **cmdlet New-AzApplicationGatewayBackendAddressPool** tworzy pulę adresów zaplecza dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ad8-106">The **New-AzApplicationGatewayBackendAddressPool** cmdlet creates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="a8ad8-107">Adres końcowy można określić jako adres IP, w pełni kwalifikowaną nazwę domeny (FQDN) lub identyfikator konfiguracji adresu IP.</span><span class="sxs-lookup"><span data-stu-id="a8ad8-107">A back-end address can be specified as an IP address, a fully-qualified domain name (FQDN) or an IP configuration ID.</span></span>

## <span data-ttu-id="a8ad8-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a8ad8-108">EXAMPLES</span></span>

### <span data-ttu-id="a8ad8-109">Przykład 1. Tworzenie puli adresów back-end przy użyciu domeny FQDN serwera back-end</span><span class="sxs-lookup"><span data-stu-id="a8ad8-109">Example 1: Create a back-end address pool by using the FQDN of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool01" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="a8ad8-110">To polecenie tworzy pulę adresów końcowych o nazwie Pool01 przy użyciu nazw FQN serwerów końcowych i przechowuje ją w $Pool danych.</span><span class="sxs-lookup"><span data-stu-id="a8ad8-110">This command creates a back-end address pool named Pool01 by using the FQDNs of back-end servers, and stores it in the $Pool variable.</span></span>

### <span data-ttu-id="a8ad8-111">Przykład 2. Tworzenie puli adresów back-end przy użyciu adresu IP serwera back-end</span><span class="sxs-lookup"><span data-stu-id="a8ad8-111">Example 2: Create a back-end address pool by using the IP address of a back-end server</span></span>
```
PS C:\>$Pool = New-AzApplicationGatewayBackendAddressPool -Name "Pool02" -BackendFqdns "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="a8ad8-112">To polecenie tworzy pulę adresów back-end o nazwie Pool02 przy użyciu adresów IP serwerów końcowych i zapisuje ją w $Pool danych.</span><span class="sxs-lookup"><span data-stu-id="a8ad8-112">This command creates a back-end address pool named Pool02 by using the IP addresses of back-end servers, and stores it in the $Pool variable.</span></span>

## <span data-ttu-id="a8ad8-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a8ad8-113">PARAMETERS</span></span>

### <span data-ttu-id="a8ad8-114">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="a8ad8-114">-BackendFqdns</span></span>
<span data-ttu-id="a8ad8-115">Określa listę serwerów FQN typu back-end, które to polecenie cmdlet skojarzy z pulą serwerów typu back-end.</span><span class="sxs-lookup"><span data-stu-id="a8ad8-115">Specifies a list of back-end FQDNs that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="a8ad8-116">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="a8ad8-116">-BackendIPAddresses</span></span>
<span data-ttu-id="a8ad8-117">Określa listę serwerów końcowych adresów IP, które to polecenie cmdlet skojarzy z pulą serwerów typu back-end.</span><span class="sxs-lookup"><span data-stu-id="a8ad8-117">Specifies a list of back-end IP addresses that this cmdlet associates with the back-end server pool.</span></span>

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

### <span data-ttu-id="a8ad8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8ad8-118">-DefaultProfile</span></span>
<span data-ttu-id="a8ad8-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a8ad8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a8ad8-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a8ad8-120">-Name</span></span>
<span data-ttu-id="a8ad8-121">Określa nazwę puli serwerów back-end, która jest owana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8ad8-121">Specifies the name of the back-end server pool that this cmdlet creates.</span></span>

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

### <span data-ttu-id="a8ad8-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a8ad8-122">-Confirm</span></span>
<span data-ttu-id="a8ad8-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a8ad8-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8ad8-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8ad8-124">-WhatIf</span></span>
<span data-ttu-id="a8ad8-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8ad8-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8ad8-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a8ad8-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8ad8-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8ad8-127">CommonParameters</span></span>
<span data-ttu-id="a8ad8-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8ad8-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8ad8-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8ad8-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8ad8-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8ad8-130">INPUTS</span></span>

### <span data-ttu-id="a8ad8-131">Brak</span><span class="sxs-lookup"><span data-stu-id="a8ad8-131">None</span></span>

## <span data-ttu-id="a8ad8-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8ad8-132">OUTPUTS</span></span>

### <span data-ttu-id="a8ad8-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a8ad8-133">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="a8ad8-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a8ad8-134">NOTES</span></span>

## <span data-ttu-id="a8ad8-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8ad8-135">RELATED LINKS</span></span>

[<span data-ttu-id="a8ad8-136">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a8ad8-136">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a8ad8-137">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a8ad8-137">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a8ad8-138">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a8ad8-138">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="a8ad8-139">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="a8ad8-139">Set-AzApplicationGatewayBackendAddressPool</span></span>](./Set-AzApplicationGatewayBackendAddressPool.md)


