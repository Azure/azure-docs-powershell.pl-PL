---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 404a9ff22f6b6af480e167c5a4f958b9ac4b5d52
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052520"
---
# <span data-ttu-id="326f3-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="326f3-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="326f3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="326f3-102">SYNOPSIS</span></span>
<span data-ttu-id="326f3-103">Pobiera port frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="326f3-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="326f3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="326f3-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="326f3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="326f3-105">DESCRIPTION</span></span>
<span data-ttu-id="326f3-106">Polecenie cmdlet **Get-AzApplicationGatewayFrontendPort** pobiera port frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="326f3-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="326f3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="326f3-107">EXAMPLES</span></span>

### <span data-ttu-id="326f3-108">Przykład 1: uzyskiwanie określonego portu frontonu</span><span class="sxs-lookup"><span data-stu-id="326f3-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="326f3-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="326f3-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="326f3-110">Drugie polecenie pobiera port frontonu o nazwie FrontEndPort01 z $AppGw i zapisuje go w zmiennej $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="326f3-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="326f3-111">Przykład 2: uzyskiwanie listy portów frontonu</span><span class="sxs-lookup"><span data-stu-id="326f3-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="326f3-112">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="326f3-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="326f3-113">Drugie polecenie pobiera listę portów frontonu z $AppGw i zapisuje je w zmiennej $FrontEndPorts.</span><span class="sxs-lookup"><span data-stu-id="326f3-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="326f3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="326f3-114">PARAMETERS</span></span>

### <span data-ttu-id="326f3-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="326f3-115">-ApplicationGateway</span></span>
<span data-ttu-id="326f3-116">Określa obiekt bramy aplikacji, który zawiera port frontonu.</span><span class="sxs-lookup"><span data-stu-id="326f3-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="326f3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="326f3-117">-DefaultProfile</span></span>
<span data-ttu-id="326f3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="326f3-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="326f3-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="326f3-119">-Name</span></span>
<span data-ttu-id="326f3-120">Określa nazwę portu frontonu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="326f3-120">Specifies the name of the front-end port to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="326f3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="326f3-121">CommonParameters</span></span>
<span data-ttu-id="326f3-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="326f3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="326f3-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="326f3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="326f3-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="326f3-124">INPUTS</span></span>

### <span data-ttu-id="326f3-125">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="326f3-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="326f3-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="326f3-126">OUTPUTS</span></span>

### <span data-ttu-id="326f3-127">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="326f3-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="326f3-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="326f3-128">NOTES</span></span>

## <span data-ttu-id="326f3-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="326f3-129">RELATED LINKS</span></span>

[<span data-ttu-id="326f3-130">Dodaj-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="326f3-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="326f3-131">Nowe — AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="326f3-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="326f3-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="326f3-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="326f3-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="326f3-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


