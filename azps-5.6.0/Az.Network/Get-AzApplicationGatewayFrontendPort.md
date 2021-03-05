---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: a0e8cbdb9ec64d4f65b859f70c1a1bb7f843132b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996542"
---
# <span data-ttu-id="50f5d-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="50f5d-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="50f5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50f5d-102">SYNOPSIS</span></span>
<span data-ttu-id="50f5d-103">Pobiera pierwszy port bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="50f5d-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="50f5d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="50f5d-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50f5d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="50f5d-105">DESCRIPTION</span></span>
<span data-ttu-id="50f5d-106">Polecenie **cmdlet Get-AzApplicationGatewayFrontendPort** pobiera pierwszy port bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="50f5d-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="50f5d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="50f5d-107">EXAMPLES</span></span>

### <span data-ttu-id="50f5d-108">Przykład 1. Uzyskiwanie określonego portu frontoronu</span><span class="sxs-lookup"><span data-stu-id="50f5d-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="50f5d-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="50f5d-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="50f5d-110">Drugie polecenie pobiera z sieci frontonu port FrontEndPort0 $AppGw 1 o nazwie FrontEndPort01 i zapisuje go w $FrontEndPort danych.</span><span class="sxs-lookup"><span data-stu-id="50f5d-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="50f5d-111">Przykład 2. Uzyskiwanie listy portów frontoronu</span><span class="sxs-lookup"><span data-stu-id="50f5d-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="50f5d-112">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="50f5d-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="50f5d-113">Drugie polecenie pobiera listę portów frontonu z $AppGw i przechowuje je w $FrontEndPorts zmienną.</span><span class="sxs-lookup"><span data-stu-id="50f5d-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="50f5d-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50f5d-114">PARAMETERS</span></span>

### <span data-ttu-id="50f5d-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50f5d-115">-ApplicationGateway</span></span>
<span data-ttu-id="50f5d-116">Określa obiekt bramy aplikacji zawierający port frontoronu.</span><span class="sxs-lookup"><span data-stu-id="50f5d-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="50f5d-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50f5d-117">-DefaultProfile</span></span>
<span data-ttu-id="50f5d-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="50f5d-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50f5d-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="50f5d-119">-Name</span></span>
<span data-ttu-id="50f5d-120">Określa nazwę portu frontoronu, który ma być uzyskać.</span><span class="sxs-lookup"><span data-stu-id="50f5d-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="50f5d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50f5d-121">CommonParameters</span></span>
<span data-ttu-id="50f5d-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50f5d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50f5d-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="50f5d-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50f5d-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50f5d-124">INPUTS</span></span>

### <span data-ttu-id="50f5d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="50f5d-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="50f5d-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50f5d-126">OUTPUTS</span></span>

### <span data-ttu-id="50f5d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="50f5d-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="50f5d-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="50f5d-128">NOTES</span></span>

## <span data-ttu-id="50f5d-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50f5d-129">RELATED LINKS</span></span>

[<span data-ttu-id="50f5d-130">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="50f5d-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="50f5d-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="50f5d-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="50f5d-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="50f5d-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="50f5d-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="50f5d-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


