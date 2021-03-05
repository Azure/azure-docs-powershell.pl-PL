---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: d3b8a57fcd170a2a1f1e4e4c539cff8a60885260
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993931"
---
# <span data-ttu-id="5728f-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="5728f-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="5728f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5728f-102">SYNOPSIS</span></span>
<span data-ttu-id="5728f-103">Pobiera konfigurację serwera WAF bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5728f-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="5728f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5728f-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5728f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5728f-105">DESCRIPTION</span></span>
<span data-ttu-id="5728f-106">Polecenie **cmdlet Get-AzApplicationGatewayWebApplicationFirewallConfiguration** pobiera konfigurację zapory aplikacji sieci Web (WAF) bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5728f-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="5728f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5728f-107">EXAMPLES</span></span>

### <span data-ttu-id="5728f-108">Przykład 1. Uzyskiwanie konfiguracji zapory aplikacji bramy sieci Web</span><span class="sxs-lookup"><span data-stu-id="5728f-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="5728f-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01, a następnie zapisuje ją w $AppGW zmienną.</span><span class="sxs-lookup"><span data-stu-id="5728f-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="5728f-110">Drugie polecenie pobiera konfigurację zapory bramy aplikacji w programie $AppGW i zapisuje je w $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="5728f-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="5728f-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5728f-111">PARAMETERS</span></span>

### <span data-ttu-id="5728f-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5728f-112">-ApplicationGateway</span></span>
<span data-ttu-id="5728f-113">Określa obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5728f-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="5728f-114">Możesz użyć Get-AzApplicationGateway cmdlet w celu uzyskania obiektu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5728f-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="5728f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5728f-115">-DefaultProfile</span></span>
<span data-ttu-id="5728f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5728f-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5728f-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5728f-117">CommonParameters</span></span>
<span data-ttu-id="5728f-118">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5728f-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5728f-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5728f-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5728f-120">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5728f-120">INPUTS</span></span>

### <span data-ttu-id="5728f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5728f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5728f-122">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5728f-122">OUTPUTS</span></span>

### <span data-ttu-id="5728f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="5728f-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="5728f-124">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5728f-124">NOTES</span></span>

## <span data-ttu-id="5728f-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5728f-125">RELATED LINKS</span></span>

[<span data-ttu-id="5728f-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5728f-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="5728f-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="5728f-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="5728f-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="5728f-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


