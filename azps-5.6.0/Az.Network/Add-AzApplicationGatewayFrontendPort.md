---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 40198C86-A4EB-494A-86D5-DF632518EB95
online version: https://docs.microsoft.com/powershell/module/az.network/add-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 5926b2fb4b97d42ff8743ad227fdfb1b32326a20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967969"
---
# <span data-ttu-id="5504d-101">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5504d-101">Add-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="5504d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5504d-102">SYNOPSIS</span></span>
<span data-ttu-id="5504d-103">Dodaje port frontoronowy do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5504d-103">Adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="5504d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5504d-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayFrontendPort -ApplicationGateway <PSApplicationGateway> -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5504d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5504d-105">DESCRIPTION</span></span>
<span data-ttu-id="5504d-106">Polecenie **cmdlet Add-AzApplicationGatewayFrontendPort** dodaje port front end do bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="5504d-106">The **Add-AzApplicationGatewayFrontendPort** cmdlet adds a front-end port to an application gateway.</span></span>

## <span data-ttu-id="5504d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5504d-107">EXAMPLES</span></span>

### <span data-ttu-id="5504d-108">Przykład 1. Dodawanie portu frontoronu do bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="5504d-108">Example 1: Add a front-end port to an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Add-AzApplicationGatewayFrontendPort -ApplicationGateway $AppGw -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="5504d-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01, która należy do grupy zasobów o nazwie ResourceGroup01, i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="5504d-109">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="5504d-110">Drugie polecenie dodaje port 80 jako port fronto end bramy aplikacji przechowywanej w programie $AppGw i nadaje nazwę portowi FrontEndPort01.</span><span class="sxs-lookup"><span data-stu-id="5504d-110">The second command adds port 80 as a front-end port for the application gateway stored in $AppGw and names the port FrontEndPort01.</span></span>

## <span data-ttu-id="5504d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5504d-111">PARAMETERS</span></span>

### <span data-ttu-id="5504d-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5504d-112">-ApplicationGateway</span></span>
<span data-ttu-id="5504d-113">Określa bramę aplikacji, do której to polecenie cmdlet dodaje port frontoronu.</span><span class="sxs-lookup"><span data-stu-id="5504d-113">Specifies the application gateway to which this cmdlet adds a front-end port.</span></span>

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

### <span data-ttu-id="5504d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5504d-114">-DefaultProfile</span></span>
<span data-ttu-id="5504d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5504d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5504d-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5504d-116">-Name</span></span>
<span data-ttu-id="5504d-117">Określa nazwę portu frontoronu.</span><span class="sxs-lookup"><span data-stu-id="5504d-117">Specifies the name of the front-end port.</span></span>

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

### <span data-ttu-id="5504d-118">— Port</span><span class="sxs-lookup"><span data-stu-id="5504d-118">-Port</span></span>
<span data-ttu-id="5504d-119">Określa numer portu.</span><span class="sxs-lookup"><span data-stu-id="5504d-119">Specifies the port number.</span></span>

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

### <span data-ttu-id="5504d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5504d-120">CommonParameters</span></span>
<span data-ttu-id="5504d-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5504d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5504d-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5504d-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5504d-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5504d-123">INPUTS</span></span>

### <span data-ttu-id="5504d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5504d-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5504d-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5504d-125">OUTPUTS</span></span>

### <span data-ttu-id="5504d-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5504d-126">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5504d-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5504d-127">NOTES</span></span>

## <span data-ttu-id="5504d-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5504d-128">RELATED LINKS</span></span>

[<span data-ttu-id="5504d-129">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5504d-129">Get-AzApplicationGatewayFrontendPort</span></span>](./Get-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5504d-130">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5504d-130">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5504d-131">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5504d-131">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="5504d-132">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="5504d-132">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


