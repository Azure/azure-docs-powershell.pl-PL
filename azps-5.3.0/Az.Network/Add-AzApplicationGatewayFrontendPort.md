---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 9cd7cd0b859ff806b084ebfe1c76e07aed3a7c43
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380326"
---
# <span data-ttu-id="74eb7-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="74eb7-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="74eb7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="74eb7-102">SYNOPSIS</span></span>
<span data-ttu-id="74eb7-103">Dodaje port frontonu do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="74eb7-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="74eb7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="74eb7-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="74eb7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="74eb7-105">DESCRIPTION</span></span>
<span data-ttu-id="74eb7-106">Polecenie cmdlet **Add-AzApplicationGatewayFrontendPort** dodaje port frontonu do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="74eb7-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="74eb7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="74eb7-107">EXAMPLES</span></span>

### <span data-ttu-id="74eb7-108">Przykład 1. Dodaj port frontonu do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="74eb7-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="74eb7-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 należącej do grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="74eb7-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="74eb7-110">Drugie polecenie dodaje port 80 jako port frontonu dla bramy aplikacji przechowywanej w $AppGw i nadaje nazwę portowi FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="74eb7-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="74eb7-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74eb7-111">PARAMETERS</span></span>

### <span data-ttu-id="74eb7-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74eb7-112">-ApplicationGateway</span></span>
<span data-ttu-id="74eb7-113">Określa bramę aplikacji, z którą to polecenie cmdlet dodaje port frontonu.</span><span class="sxs-lookup"><span data-stu-id="74eb7-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="74eb7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74eb7-114">-DefaultProfile</span></span>
<span data-ttu-id="74eb7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="74eb7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74eb7-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="74eb7-116">-Name</span></span>
<span data-ttu-id="74eb7-117">Określa nazwę portu frontonu.</span><span class="sxs-lookup"><span data-stu-id="74eb7-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="74eb7-118">-Port</span><span class="sxs-lookup"><span data-stu-id="74eb7-118">-Port</span></span>
<span data-ttu-id="74eb7-119">Określa numer portu.</span><span class="sxs-lookup"><span data-stu-id="74eb7-119">Specifies the port number.</span></span>

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

### <span data-ttu-id="74eb7-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74eb7-120">CommonParameters</span></span>
<span data-ttu-id="74eb7-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74eb7-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74eb7-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74eb7-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74eb7-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74eb7-123">INPUTS</span></span>

### <span data-ttu-id="74eb7-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74eb7-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="74eb7-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="74eb7-125">OUTPUTS</span></span>

### <span data-ttu-id="74eb7-126">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="74eb7-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="74eb7-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="74eb7-127">NOTES</span></span>

## <span data-ttu-id="74eb7-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74eb7-128">RELATED LINKS</span></span>

[<span data-ttu-id="74eb7-129">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="74eb7-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="74eb7-130">Nowe — AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="74eb7-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="74eb7-131">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="74eb7-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="74eb7-132">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="74eb7-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


