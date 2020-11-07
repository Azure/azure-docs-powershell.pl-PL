---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermapplicationgatewayhttplistener
schema: 2.0.0
ms.openlocfilehash: 79b61f5d96307afea47851b210fc1a1ee97acf61
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898901"
---
# <span data-ttu-id="bf4a6-101">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bf4a6-101">Get-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="bf4a6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf4a6-102">SYNOPSIS</span></span>
<span data-ttu-id="bf4a6-103">Pobiera odbiornik HTTP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="bf4a6-103">Gets the HTTP listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf4a6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf4a6-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf4a6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bf4a6-105">DESCRIPTION</span></span>
<span data-ttu-id="bf4a6-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayHttpListener** pobiera odbiornik http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="bf4a6-106">The **Get-AzureRmApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="bf4a6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf4a6-107">EXAMPLES</span></span>

### <span data-ttu-id="bf4a6-108">Przykład 1: uzyskiwanie określonego odbiornika HTTP</span><span class="sxs-lookup"><span data-stu-id="bf4a6-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzureRmApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="bf4a6-109">To polecenie pobiera odbiornik HTTP o nazwie Listener01.</span><span class="sxs-lookup"><span data-stu-id="bf4a6-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="bf4a6-110">Przykład 2: uzyskiwanie listy detektorów HTTP</span><span class="sxs-lookup"><span data-stu-id="bf4a6-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzureRmApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="bf4a6-111">To polecenie powoduje wyświetlenie listy detektorów HTTP.</span><span class="sxs-lookup"><span data-stu-id="bf4a6-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="bf4a6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf4a6-112">PARAMETERS</span></span>

### <span data-ttu-id="bf4a6-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf4a6-113">-ApplicationGateway</span></span>
<span data-ttu-id="bf4a6-114">Określa obiekt bramy aplikacji, który zawiera odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="bf4a6-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf4a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf4a6-115">-DefaultProfile</span></span>
<span data-ttu-id="bf4a6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf4a6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf4a6-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf4a6-117">-Name</span></span>
<span data-ttu-id="bf4a6-118">Określa nazwę odbiornika HTTP, który ma być pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf4a6-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bf4a6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf4a6-119">CommonParameters</span></span>
<span data-ttu-id="bf4a6-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf4a6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf4a6-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf4a6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf4a6-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf4a6-122">INPUTS</span></span>

### <span data-ttu-id="bf4a6-123">System. String</span><span class="sxs-lookup"><span data-stu-id="bf4a6-123">System.String</span></span>

## <span data-ttu-id="bf4a6-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf4a6-124">OUTPUTS</span></span>

### <span data-ttu-id="bf4a6-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bf4a6-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="bf4a6-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf4a6-126">NOTES</span></span>

## <span data-ttu-id="bf4a6-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf4a6-127">RELATED LINKS</span></span>

[<span data-ttu-id="bf4a6-128">Dodaj-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bf4a6-128">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="bf4a6-129">Nowe — AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bf4a6-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="bf4a6-130">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bf4a6-130">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="bf4a6-131">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="bf4a6-131">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


