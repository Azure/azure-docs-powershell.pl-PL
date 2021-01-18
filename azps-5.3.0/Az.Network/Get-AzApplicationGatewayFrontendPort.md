---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 404a9ff22f6b6af480e167c5a4f958b9ac4b5d52
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504503"
---
# <span data-ttu-id="21829-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="21829-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="21829-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="21829-102">SYNOPSIS</span></span>
<span data-ttu-id="21829-103">Pobiera port frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="21829-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="21829-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="21829-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="21829-105">Opis</span><span class="sxs-lookup"><span data-stu-id="21829-105">DESCRIPTION</span></span>
<span data-ttu-id="21829-106">Polecenie cmdlet **Get-AzApplicationGatewayFrontendPort** pobiera port frontonu bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="21829-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="21829-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="21829-107">EXAMPLES</span></span>

### <span data-ttu-id="21829-108">Przykład 1: uzyskiwanie określonego portu frontonu</span><span class="sxs-lookup"><span data-stu-id="21829-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="21829-109">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="21829-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="21829-110">Drugie polecenie pobiera port frontonu o nazwie FrontEndPort01 z $AppGw i zapisuje go w zmiennej $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="21829-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="21829-111">Przykład 2: uzyskiwanie listy portów frontonu</span><span class="sxs-lookup"><span data-stu-id="21829-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="21829-112">Pierwsze polecenie pobiera bramkę Application Gateway o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i zapisuje ją w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="21829-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="21829-113">Drugie polecenie pobiera listę portów frontonu z $AppGw i zapisuje je w zmiennej $FrontEndPorts.</span><span class="sxs-lookup"><span data-stu-id="21829-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="21829-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="21829-114">PARAMETERS</span></span>

### <span data-ttu-id="21829-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="21829-115">-ApplicationGateway</span></span>
<span data-ttu-id="21829-116">Określa obiekt bramy aplikacji, który zawiera port frontonu.</span><span class="sxs-lookup"><span data-stu-id="21829-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="21829-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21829-117">-DefaultProfile</span></span>
<span data-ttu-id="21829-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="21829-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21829-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="21829-119">-Name</span></span>
<span data-ttu-id="21829-120">Określa nazwę portu frontonu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="21829-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="21829-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21829-121">CommonParameters</span></span>
<span data-ttu-id="21829-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21829-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21829-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="21829-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21829-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="21829-124">INPUTS</span></span>

### <span data-ttu-id="21829-125">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="21829-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="21829-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="21829-126">OUTPUTS</span></span>

### <span data-ttu-id="21829-127">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="21829-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="21829-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="21829-128">NOTES</span></span>

## <span data-ttu-id="21829-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="21829-129">RELATED LINKS</span></span>

[<span data-ttu-id="21829-130">Dodaj-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="21829-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="21829-131">Nowe — AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="21829-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="21829-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="21829-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="21829-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="21829-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


