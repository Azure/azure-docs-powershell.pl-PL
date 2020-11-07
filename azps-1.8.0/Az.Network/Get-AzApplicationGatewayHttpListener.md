---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 91b2791b7f61c7586c1fbd4bca954e374ccbb43c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709614"
---
# <span data-ttu-id="ee964-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ee964-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ee964-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ee964-102">SYNOPSIS</span></span>
<span data-ttu-id="ee964-103">Pobiera odbiornik HTTP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ee964-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="ee964-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ee964-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ee964-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ee964-105">DESCRIPTION</span></span>
<span data-ttu-id="ee964-106">Polecenie cmdlet **Get-AzApplicationGatewayHttpListener** pobiera odbiornik http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="ee964-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="ee964-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ee964-107">EXAMPLES</span></span>

### <span data-ttu-id="ee964-108">Przykład 1: uzyskiwanie określonego odbiornika HTTP</span><span class="sxs-lookup"><span data-stu-id="ee964-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="ee964-109">To polecenie pobiera odbiornik HTTP o nazwie Listener01.</span><span class="sxs-lookup"><span data-stu-id="ee964-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="ee964-110">Przykład 2: uzyskiwanie listy detektorów HTTP</span><span class="sxs-lookup"><span data-stu-id="ee964-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="ee964-111">To polecenie powoduje wyświetlenie listy detektorów HTTP.</span><span class="sxs-lookup"><span data-stu-id="ee964-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="ee964-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ee964-112">PARAMETERS</span></span>

### <span data-ttu-id="ee964-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ee964-113">-ApplicationGateway</span></span>
<span data-ttu-id="ee964-114">Określa obiekt bramy aplikacji, który zawiera odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="ee964-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="ee964-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee964-115">-DefaultProfile</span></span>
<span data-ttu-id="ee964-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ee964-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ee964-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ee964-117">-Name</span></span>
<span data-ttu-id="ee964-118">Określa nazwę odbiornika HTTP, który ma być pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ee964-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="ee964-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee964-119">CommonParameters</span></span>
<span data-ttu-id="ee964-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee964-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee964-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ee964-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee964-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ee964-122">INPUTS</span></span>

### <span data-ttu-id="ee964-123">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ee964-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ee964-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ee964-124">OUTPUTS</span></span>

### <span data-ttu-id="ee964-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ee964-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="ee964-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ee964-126">NOTES</span></span>

## <span data-ttu-id="ee964-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ee964-127">RELATED LINKS</span></span>

[<span data-ttu-id="ee964-128">Dodaj-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ee964-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ee964-129">Nowe — AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ee964-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ee964-130">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ee964-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="ee964-131">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="ee964-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)

