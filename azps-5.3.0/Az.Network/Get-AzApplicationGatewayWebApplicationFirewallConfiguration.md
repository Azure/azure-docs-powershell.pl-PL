---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 5D887302-7678-44C0-86F3-CEF2EF8A0991
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewaywebapplicationfirewallconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayWebApplicationFirewallConfiguration.md
ms.openlocfilehash: 9a27e88557bd263df3f08ce8e6d43ea26faa67b6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380228"
---
# <span data-ttu-id="c5888-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5888-101">Get-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="c5888-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c5888-102">SYNOPSIS</span></span>
<span data-ttu-id="c5888-103">Pobiera konfigurację WAF bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c5888-103">Gets the WAF configuration of an application gateway.</span></span>

## <span data-ttu-id="c5888-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c5888-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c5888-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c5888-105">DESCRIPTION</span></span>
<span data-ttu-id="c5888-106">Polecenie cmdlet **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** Pobiera konfigurację zapory aplikacji sieci Web (WAF) bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="c5888-106">The **Get-AzApplicationGatewayWebApplicationFirewallConfiguration** cmdlet gets the web application firewall (WAF) configuration of an application gateway.</span></span>

## <span data-ttu-id="c5888-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c5888-107">EXAMPLES</span></span>

### <span data-ttu-id="c5888-108">Przykład 1: Uzyskiwanie konfiguracji zapory aplikacji sieci Web bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="c5888-108">Example 1: Get an application gateway web application firewall configuration</span></span>
```
PS C:\>$AppGW = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FirewallConfig = Get-AzApplicationGatewayWebApplicationFirewallConfiguration -ApplicationGateway $AppGW
```

<span data-ttu-id="c5888-109">Pierwsze polecenie uzyskuje bramkę Application Gateway o nazwie ApplicationGateway01, a następnie zapisuje ją w zmiennej $AppGW.</span><span class="sxs-lookup"><span data-stu-id="c5888-109">The first command gets the application gateway named ApplicationGateway01, and then stores it in the $AppGW variable.</span></span>
<span data-ttu-id="c5888-110">Drugie polecenie pobiera konfigurację zapory bramy Application Gateway w $AppGW, a następnie przechowuje ją w $FirewallConfig.</span><span class="sxs-lookup"><span data-stu-id="c5888-110">The second command gets the firewall configuration of the application gateway in $AppGW, and then stores it in $FirewallConfig.</span></span>

## <span data-ttu-id="c5888-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5888-111">PARAMETERS</span></span>

### <span data-ttu-id="c5888-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c5888-112">-ApplicationGateway</span></span>
<span data-ttu-id="c5888-113">Określa obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c5888-113">Specifies an application gateway object.</span></span>
<span data-ttu-id="c5888-114">Możesz użyć polecenia cmdlet Get-AzApplicationGateway, aby uzyskać obiekt bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="c5888-114">You can use the Get-AzApplicationGateway cmdlet to get an application gateway object.</span></span>

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

### <span data-ttu-id="c5888-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5888-115">-DefaultProfile</span></span>
<span data-ttu-id="c5888-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c5888-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c5888-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5888-117">CommonParameters</span></span>
<span data-ttu-id="c5888-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5888-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5888-119">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5888-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5888-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5888-120">INPUTS</span></span>

### <span data-ttu-id="c5888-121">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c5888-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="c5888-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c5888-122">OUTPUTS</span></span>

### <span data-ttu-id="c5888-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5888-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayWebApplicationFirewallConfiguration</span></span>

## <span data-ttu-id="c5888-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c5888-124">NOTES</span></span>

## <span data-ttu-id="c5888-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5888-125">RELATED LINKS</span></span>

[<span data-ttu-id="c5888-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="c5888-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="c5888-127">Nowe — AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5888-127">New-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./New-AzApplicationGatewayWebApplicationFirewallConfiguration.md)

[<span data-ttu-id="c5888-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span><span class="sxs-lookup"><span data-stu-id="c5888-128">Set-AzApplicationGatewayWebApplicationFirewallConfiguration</span></span>](./Set-AzApplicationGatewayWebApplicationFirewallConfiguration.md)


