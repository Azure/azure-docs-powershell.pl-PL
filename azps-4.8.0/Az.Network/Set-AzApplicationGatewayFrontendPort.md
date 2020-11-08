---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 85C0A1C3-FC6D-496A-B6B5-8DC2A73B8032
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 08637412afafe9220107e95dd3cb7dcc5154ba26
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221936"
---
# <span data-ttu-id="2aaf0-101">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2aaf0-101">Set-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="2aaf0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2aaf0-102">SYNOPSIS</span></span>
<span data-ttu-id="2aaf0-103">Modyfikuje port frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2aaf0-103">Modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="2aaf0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2aaf0-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2aaf0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2aaf0-105">DESCRIPTION</span></span>
<span data-ttu-id="2aaf0-106">Polecenie cmdlet **Set-AzApplicationGatewayFrontendPort** modyfikuje port frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="2aaf0-106">The **Set-AzApplicationGatewayFrontendPort** cmdlet modifies a front-end port for an application gateway.</span></span>

## <span data-ttu-id="2aaf0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2aaf0-107">EXAMPLES</span></span>

### <span data-ttu-id="2aaf0-108">Przykład 1. Ustaw port frontonu bramy aplikacji na 80</span><span class="sxs-lookup"><span data-stu-id="2aaf0-108">Example 1: Set an application gateway front-end port to 80</span></span>
```
PS C:\> $AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="2aaf0-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="2aaf0-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="2aaf0-110">Drugie polecenie modyfikuje bramę w $AppGw, aby używać portu 80 dla portu frontonu o nazwie FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="2aaf0-110">The second command modifies the gateway in $AppGw to use port 80 for the front-end port named FrontEndPort01.</span></span>

## <span data-ttu-id="2aaf0-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2aaf0-111">PARAMETERS</span></span>

### <span data-ttu-id="2aaf0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2aaf0-112">-ApplicationGateway</span></span>
<span data-ttu-id="2aaf0-113">Określa obiekt bramy aplikacji, za pomocą którego to polecenie cmdlet kojarzy port frontonu.</span><span class="sxs-lookup"><span data-stu-id="2aaf0-113">Specifies the application gateway object with which this cmdlet associates the front-end port.</span></span>

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

### <span data-ttu-id="2aaf0-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2aaf0-114">-DefaultProfile</span></span>
<span data-ttu-id="2aaf0-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2aaf0-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2aaf0-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2aaf0-116">-Name</span></span>
<span data-ttu-id="2aaf0-117">Określa nazwę portu frontonu do zmodyfikowania.</span><span class="sxs-lookup"><span data-stu-id="2aaf0-117">Specifies the name of the front-end port to modify.</span></span>

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

### <span data-ttu-id="2aaf0-118">-Port</span><span class="sxs-lookup"><span data-stu-id="2aaf0-118">-Port</span></span>
<span data-ttu-id="2aaf0-119">Określa numer portu, który ma być używany dla portu frontonu.</span><span class="sxs-lookup"><span data-stu-id="2aaf0-119">Specifies the port number to use for the front-end port.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2aaf0-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2aaf0-120">CommonParameters</span></span>
<span data-ttu-id="2aaf0-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2aaf0-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2aaf0-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2aaf0-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2aaf0-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2aaf0-123">INPUTS</span></span>

### <span data-ttu-id="2aaf0-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2aaf0-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2aaf0-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2aaf0-125">OUTPUTS</span></span>

### <span data-ttu-id="2aaf0-126">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="2aaf0-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="2aaf0-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2aaf0-127">NOTES</span></span>

## <span data-ttu-id="2aaf0-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2aaf0-128">RELATED LINKS</span></span>

[<span data-ttu-id="2aaf0-129">Dodaj-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2aaf0-129">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="2aaf0-130">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2aaf0-130">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="2aaf0-131">Nowe — AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2aaf0-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="2aaf0-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="2aaf0-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)
