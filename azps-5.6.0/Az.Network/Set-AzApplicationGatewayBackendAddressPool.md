---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: C2C5E0C0-E212-4554-966B-940B1B6FE235
online version: https://docs.microsoft.com/powershell/module/az.network/set-azapplicationgatewaybackendaddresspool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendAddressPool.md
ms.openlocfilehash: 672286da502500101846d6fae694af059328c3cf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960266"
---
# <span data-ttu-id="c87a1-101">Set-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c87a1-101">Set-AzApplicationGatewayBackendAddressPool</span></span>

## <span data-ttu-id="c87a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c87a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c87a1-103">Aktualizuje pulę adresów końcowych dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c87a1-103">Updates a back-end address pool for an application gateway.</span></span>

## <span data-ttu-id="c87a1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c87a1-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway <PSApplicationGateway> -Name <String>
 [-BackendIPAddresses <String[]>] [-BackendFqdns <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c87a1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c87a1-105">DESCRIPTION</span></span>
<span data-ttu-id="c87a1-106">Polecenie **cmdlet Set-AzApplicationGatewayBackendAddressPool** aktualizuje pulę adresów zaplecza dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c87a1-106">The **Set-AzApplicationGatewayBackendAddressPool** cmdlet updates a back-end address pool for an Azure application gateway.</span></span>
<span data-ttu-id="c87a1-107">Adresy końcowe można określić jako adresy IP, w pełni kwalifikowane nazwy domen (FQDN) lub identyfikatory konfiguracji adresów IP.</span><span class="sxs-lookup"><span data-stu-id="c87a1-107">Back-end addresses can be specified as IP addresses, fully-qualified domain names (FQDN) or IP configurations IDs.</span></span>

## <span data-ttu-id="c87a1-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c87a1-108">EXAMPLES</span></span>

### <span data-ttu-id="c87a1-109">Przykład 1. Ustawianie puli adresów back-end przy użyciu sieci FQNS</span><span class="sxs-lookup"><span data-stu-id="c87a1-109">Example 1: Setting a back-end address pool by using FQDNs</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendFqdns "contoso1.com", "contoso2.com"
```

<span data-ttu-id="c87a1-110">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w $AppGw zmienną.</span><span class="sxs-lookup"><span data-stu-id="c87a1-110">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c87a1-111">Drugie polecenie aktualizuje pulę adresów back-end bramy aplikacji w programie $AppGw przy użyciu sieci FQNS.</span><span class="sxs-lookup"><span data-stu-id="c87a1-111">The second command updates the back-end address pool of the application gateway in $AppGw by using FQDNs.</span></span>

### <span data-ttu-id="c87a1-112">Przykład 2. Ustawianie puli adresów zaplecza przy użyciu adresów IP serwera zaplecza</span><span class="sxs-lookup"><span data-stu-id="c87a1-112">Example 2: Setting a back-end address pool by using backend server IP addresses</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendAddressPool -ApplicationGateway $AppGw -Name "Pool02" -BackendIPAddresses "10.10.10.10", "10.10.10.11"
```

<span data-ttu-id="c87a1-113">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 w grupie zasobów o nazwie ResourceGroup01 i zapisuje ją w $AppGw zmienną.</span><span class="sxs-lookup"><span data-stu-id="c87a1-113">The first command gets the application gateway named ApplicationGateway01 in the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="c87a1-114">Drugie polecenie aktualizuje pulę adresów back-end bramy aplikacji w programie $AppGw przy użyciu adresów IP.</span><span class="sxs-lookup"><span data-stu-id="c87a1-114">The second command updates the back-end address pool of the application gateway in $AppGw by using IP addresses.</span></span>

## <span data-ttu-id="c87a1-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c87a1-115">PARAMETERS</span></span>

### <span data-ttu-id="c87a1-116">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c87a1-116">-ApplicationGateway</span></span>
<span data-ttu-id="c87a1-117">Określa bramę aplikacji, z którą to polecenie cmdlet skojarzy pulę adresów back-end.</span><span class="sxs-lookup"><span data-stu-id="c87a1-117">Specifies the application gateway with which this cmdlet associates the back-end address pool.</span></span>

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

### <span data-ttu-id="c87a1-118">-BackendFqdns</span><span class="sxs-lookup"><span data-stu-id="c87a1-118">-BackendFqdns</span></span>
<span data-ttu-id="c87a1-119">Określa listę serwerów końcowych adresów IP, które mają być wykorzystywane jako pula serwerów typu back-end.</span><span class="sxs-lookup"><span data-stu-id="c87a1-119">Specifies a list of back-end IP addresses to use as a back-end server pool.</span></span>

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

### <span data-ttu-id="c87a1-120">-BackendIPAddresses</span><span class="sxs-lookup"><span data-stu-id="c87a1-120">-BackendIPAddresses</span></span>
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

### <span data-ttu-id="c87a1-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c87a1-121">-DefaultProfile</span></span>
<span data-ttu-id="c87a1-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c87a1-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c87a1-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c87a1-123">-Name</span></span>
<span data-ttu-id="c87a1-124">Określa nazwę puli adresów na zawęzie.</span><span class="sxs-lookup"><span data-stu-id="c87a1-124">Specifies the name of the back-end address pool.</span></span>
<span data-ttu-id="c87a1-125">Ta pula adresów back-end musi istnieć w bramie aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c87a1-125">This back-end address pool must exist in the application gateway.</span></span>

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

### <span data-ttu-id="c87a1-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c87a1-126">-Confirm</span></span>
<span data-ttu-id="c87a1-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c87a1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c87a1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c87a1-128">-WhatIf</span></span>
<span data-ttu-id="c87a1-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c87a1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c87a1-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c87a1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c87a1-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c87a1-131">CommonParameters</span></span>
<span data-ttu-id="c87a1-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c87a1-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c87a1-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c87a1-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c87a1-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c87a1-134">INPUTS</span></span>

### <span data-ttu-id="c87a1-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c87a1-135">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c87a1-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c87a1-136">OUTPUTS</span></span>

### <span data-ttu-id="c87a1-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c87a1-137">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c87a1-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c87a1-138">NOTES</span></span>

## <span data-ttu-id="c87a1-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c87a1-139">RELATED LINKS</span></span>

[<span data-ttu-id="c87a1-140">Add-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c87a1-140">Add-AzApplicationGatewayBackendAddressPool</span></span>](./Add-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="c87a1-141">Get-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c87a1-141">Get-AzApplicationGatewayBackendAddressPool</span></span>](./Get-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="c87a1-142">New-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c87a1-142">New-AzApplicationGatewayBackendAddressPool</span></span>](./New-AzApplicationGatewayBackendAddressPool.md)

[<span data-ttu-id="c87a1-143">Remove-AzApplicationGatewayBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="c87a1-143">Remove-AzApplicationGatewayBackendAddressPool</span></span>](./Remove-AzApplicationGatewayBackendAddressPool.md)


