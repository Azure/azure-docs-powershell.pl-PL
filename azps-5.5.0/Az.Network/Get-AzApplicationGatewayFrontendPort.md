---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 4518D2A9-7DE7-4617-86E0-7778B8CFE48C
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayFrontendPort.md
ms.openlocfilehash: 404a9ff22f6b6af480e167c5a4f958b9ac4b5d52
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179907"
---
# <span data-ttu-id="4c9d0-101">Get-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4c9d0-101">Get-AzApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="4c9d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c9d0-102">SYNOPSIS</span></span>
<span data-ttu-id="4c9d0-103">Pobiera pierwszy port bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4c9d0-103">Gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="4c9d0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4c9d0-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayFrontendPort [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4c9d0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4c9d0-105">DESCRIPTION</span></span>
<span data-ttu-id="4c9d0-106">Polecenie **cmdlet Get-AzApplicationGatewayFrontendPort** pobiera pierwszy port bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4c9d0-106">The **Get-AzApplicationGatewayFrontendPort** cmdlet gets the front-end port of an application gateway.</span></span>

## <span data-ttu-id="4c9d0-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4c9d0-107">EXAMPLES</span></span>

### <span data-ttu-id="4c9d0-108">Przykład 1. Uzyskiwanie określonego portu frontoronu</span><span class="sxs-lookup"><span data-stu-id="4c9d0-108">Example 1: Get a specified front-end port</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPort = Get-AzApplicationGatewayFrontendPort -Name "FrontEndPort01" -ApplicationGateway $AppGw
```

<span data-ttu-id="4c9d0-109">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="4c9d0-109">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4c9d0-110">Drugie polecenie pobiera z sieci frontonu port FrontEndPort01 o nazwie $AppGw FrontEndPort01 i zapisuje go w $FrontEndPort danych.</span><span class="sxs-lookup"><span data-stu-id="4c9d0-110">The second command gets the front-end port named FrontEndPort01 from $AppGw and stores it in the $FrontEndPort variable.</span></span>

### <span data-ttu-id="4c9d0-111">Przykład 2. Uzyskiwanie listy portów frontoronu</span><span class="sxs-lookup"><span data-stu-id="4c9d0-111">Example 2: Get a list of front-end ports</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $FrontEndPorts = Get-AzApplicationGatewayFrontendPort  -ApplicationGateway $AppGw
```

<span data-ttu-id="4c9d0-112">Pierwsze polecenie pobiera bramę aplikacji o nazwie ApplicationGateway01 z grupy zasobów o nazwie ResourceGroup01 i przechowuje ją w zmiennej $AppGw zasobów.</span><span class="sxs-lookup"><span data-stu-id="4c9d0-112">The first command gets an application gateway named ApplicationGateway01 from the resource group named ResourceGroup01, and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="4c9d0-113">Drugie polecenie pobiera listę portów frontonu z $AppGw i przechowuje je w $FrontEndPorts zmienną.</span><span class="sxs-lookup"><span data-stu-id="4c9d0-113">The second command gets a list of the front-end ports from $AppGw and stores it in the $FrontEndPorts variable.</span></span>

## <span data-ttu-id="4c9d0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c9d0-114">PARAMETERS</span></span>

### <span data-ttu-id="4c9d0-115">- ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c9d0-115">-ApplicationGateway</span></span>
<span data-ttu-id="4c9d0-116">Określa obiekt bramy aplikacji, który zawiera port frontonie.</span><span class="sxs-lookup"><span data-stu-id="4c9d0-116">Specifies the application gateway object that contains the front-end port.</span></span>

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

### <span data-ttu-id="4c9d0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c9d0-117">-DefaultProfile</span></span>
<span data-ttu-id="4c9d0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c9d0-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4c9d0-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4c9d0-119">-Name</span></span>
<span data-ttu-id="4c9d0-120">Określa nazwę portu frontoronu, który ma być uzyskać.</span><span class="sxs-lookup"><span data-stu-id="4c9d0-120">Specifies the name of the front-end port to get.</span></span>

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

### <span data-ttu-id="4c9d0-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c9d0-121">CommonParameters</span></span>
<span data-ttu-id="4c9d0-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c9d0-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c9d0-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4c9d0-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c9d0-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c9d0-124">INPUTS</span></span>

### <span data-ttu-id="4c9d0-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="4c9d0-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="4c9d0-126">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c9d0-126">OUTPUTS</span></span>

### <span data-ttu-id="4c9d0-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4c9d0-127">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="4c9d0-128">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4c9d0-128">NOTES</span></span>

## <span data-ttu-id="4c9d0-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c9d0-129">RELATED LINKS</span></span>

[<span data-ttu-id="4c9d0-130">Add-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4c9d0-130">Add-AzApplicationGatewayFrontendPort</span></span>](./Add-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4c9d0-131">New-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4c9d0-131">New-AzApplicationGatewayFrontendPort</span></span>](./New-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4c9d0-132">Remove-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4c9d0-132">Remove-AzApplicationGatewayFrontendPort</span></span>](./Remove-AzApplicationGatewayFrontendPort.md)

[<span data-ttu-id="4c9d0-133">Set-AzApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="4c9d0-133">Set-AzApplicationGatewayFrontendPort</span></span>](./Set-AzApplicationGatewayFrontendPort.md)


