---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: e849d4c7eaf007a6e2fd8d6cbbda1cc49cbf2fb0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101996535"
---
# <span data-ttu-id="66145-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="66145-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="66145-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66145-102">SYNOPSIS</span></span>
<span data-ttu-id="66145-103">Pobiera słuchacza HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="66145-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="66145-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="66145-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66145-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="66145-105">DESCRIPTION</span></span>
<span data-ttu-id="66145-106">Polecenie **cmdlet Get-AzApplicationGatewayHttpListener** pobiera słuchacza HTTP bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="66145-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="66145-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="66145-107">EXAMPLES</span></span>

### <span data-ttu-id="66145-108">Przykład 1. Uzyskiwanie określonego słuchacza HTTP</span><span class="sxs-lookup"><span data-stu-id="66145-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="66145-109">To polecenie pobiera słuchacza HTTP o nazwie Słuchacz01.</span><span class="sxs-lookup"><span data-stu-id="66145-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="66145-110">Przykład 2. Uzyskiwanie listy słuchaczy HTTP</span><span class="sxs-lookup"><span data-stu-id="66145-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="66145-111">To polecenie pobiera listę słuchaczy HTTP.</span><span class="sxs-lookup"><span data-stu-id="66145-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="66145-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66145-112">PARAMETERS</span></span>

### <span data-ttu-id="66145-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66145-113">-ApplicationGateway</span></span>
<span data-ttu-id="66145-114">Określa obiekt bramy aplikacji, który zawiera słuchacza HTTP.</span><span class="sxs-lookup"><span data-stu-id="66145-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="66145-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66145-115">-DefaultProfile</span></span>
<span data-ttu-id="66145-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="66145-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="66145-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="66145-117">-Name</span></span>
<span data-ttu-id="66145-118">Określa nazwę słuchacza HTTP, do którego otrzymuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="66145-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="66145-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66145-119">CommonParameters</span></span>
<span data-ttu-id="66145-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66145-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66145-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="66145-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66145-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66145-122">INPUTS</span></span>

### <span data-ttu-id="66145-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="66145-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="66145-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="66145-124">OUTPUTS</span></span>

### <span data-ttu-id="66145-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="66145-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="66145-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="66145-126">NOTES</span></span>

## <span data-ttu-id="66145-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="66145-127">RELATED LINKS</span></span>

[<span data-ttu-id="66145-128">Add-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="66145-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="66145-129">New-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="66145-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="66145-130">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="66145-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="66145-131">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="66145-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


