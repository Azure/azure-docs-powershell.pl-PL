---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmApplicationGatewayHttpListener.md
ms.openlocfilehash: 564c586218297b8a22f0763a6747b6b451018a5e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527454"
---
# <span data-ttu-id="383bb-101">Get-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="383bb-101">Get-AzureRmApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="383bb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="383bb-102">SYNOPSIS</span></span>
<span data-ttu-id="383bb-103">Pobiera odbiornik HTTP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="383bb-103">Gets the HTTP listener of an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="383bb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="383bb-104">SYNTAX</span></span>

```
Get-AzureRmApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="383bb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="383bb-105">DESCRIPTION</span></span>
<span data-ttu-id="383bb-106">Polecenie cmdlet **Get-AzureRmApplicationGatewayHttpListener** pobiera odbiornik http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="383bb-106">The **Get-AzureRmApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="383bb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="383bb-107">EXAMPLES</span></span>

### <span data-ttu-id="383bb-108">Przykład 1: uzyskiwanie określonego odbiornika HTTP</span><span class="sxs-lookup"><span data-stu-id="383bb-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzureRmApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="383bb-109">To polecenie pobiera odbiornik HTTP o nazwie Listener01.</span><span class="sxs-lookup"><span data-stu-id="383bb-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="383bb-110">Przykład 2: uzyskiwanie listy detektorów HTTP</span><span class="sxs-lookup"><span data-stu-id="383bb-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzureRmApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="383bb-111">To polecenie powoduje wyświetlenie listy detektorów HTTP.</span><span class="sxs-lookup"><span data-stu-id="383bb-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="383bb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="383bb-112">PARAMETERS</span></span>

### <span data-ttu-id="383bb-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="383bb-113">-ApplicationGateway</span></span>
<span data-ttu-id="383bb-114">Określa obiekt bramy aplikacji, który zawiera odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="383bb-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="383bb-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="383bb-115">-Name</span></span>
<span data-ttu-id="383bb-116">Określa nazwę odbiornika HTTP, który ma być pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="383bb-116">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="383bb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="383bb-117">-DefaultProfile</span></span>
<span data-ttu-id="383bb-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="383bb-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="383bb-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="383bb-119">CommonParameters</span></span>
<span data-ttu-id="383bb-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="383bb-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="383bb-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="383bb-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="383bb-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="383bb-122">INPUTS</span></span>

### <span data-ttu-id="383bb-123">System. String</span><span class="sxs-lookup"><span data-stu-id="383bb-123">System.String</span></span>

## <span data-ttu-id="383bb-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="383bb-124">OUTPUTS</span></span>

### <span data-ttu-id="383bb-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="383bb-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="383bb-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="383bb-126">NOTES</span></span>

## <span data-ttu-id="383bb-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="383bb-127">RELATED LINKS</span></span>

[<span data-ttu-id="383bb-128">Dodaj-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="383bb-128">Add-AzureRmApplicationGatewayHttpListener</span></span>](./Add-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="383bb-129">Nowe — AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="383bb-129">New-AzureRmApplicationGatewayHttpListener</span></span>](./New-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="383bb-130">Remove-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="383bb-130">Remove-AzureRmApplicationGatewayHttpListener</span></span>](./Remove-AzureRmApplicationGatewayHttpListener.md)

[<span data-ttu-id="383bb-131">Set-AzureRmApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="383bb-131">Set-AzureRmApplicationGatewayHttpListener</span></span>](./Set-AzureRmApplicationGatewayHttpListener.md)


