---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 8D41EDAC-17D9-494B-8336-67906F4E1E81
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azapplicationgatewayhttplistener
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Get-AzApplicationGatewayHttpListener.md
ms.openlocfilehash: 67652681b5a0cf5468fa42fb9090446f2a11158e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93890881"
---
# <span data-ttu-id="aad6c-101">Get-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="aad6c-101">Get-AzApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="aad6c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="aad6c-102">SYNOPSIS</span></span>
<span data-ttu-id="aad6c-103">Pobiera odbiornik HTTP bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="aad6c-103">Gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="aad6c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="aad6c-104">SYNTAX</span></span>

```
Get-AzApplicationGatewayHttpListener [-Name <String>] -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="aad6c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="aad6c-105">DESCRIPTION</span></span>
<span data-ttu-id="aad6c-106">Polecenie cmdlet **Get-AzApplicationGatewayHttpListener** pobiera odbiornik http bramy Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="aad6c-106">The **Get-AzApplicationGatewayHttpListener** cmdlet gets the HTTP listener of an application gateway.</span></span>

## <span data-ttu-id="aad6c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="aad6c-107">EXAMPLES</span></span>

### <span data-ttu-id="aad6c-108">Przykład 1: uzyskiwanie określonego odbiornika HTTP</span><span class="sxs-lookup"><span data-stu-id="aad6c-108">Example 1: Get a specific HTTP listener</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listener = Get-AzApplicationGatewayHttpListener -Name "Listener01" -ApplicationGateway $Appgw
```

<span data-ttu-id="aad6c-109">To polecenie pobiera odbiornik HTTP o nazwie Listener01.</span><span class="sxs-lookup"><span data-stu-id="aad6c-109">This command gets an HTTP listener named Listener01.</span></span>

### <span data-ttu-id="aad6c-110">Przykład 2: uzyskiwanie listy detektorów HTTP</span><span class="sxs-lookup"><span data-stu-id="aad6c-110">Example 2: Get a list of HTTP listeners</span></span>
```
PS C:\>$Appgw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $Listeners = Get-AzApplicationGatewayHttpListener -ApplicationGateway $Appgw
```

<span data-ttu-id="aad6c-111">To polecenie powoduje wyświetlenie listy detektorów HTTP.</span><span class="sxs-lookup"><span data-stu-id="aad6c-111">This command gets a list of HTTP listeners.</span></span>

## <span data-ttu-id="aad6c-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="aad6c-112">PARAMETERS</span></span>

### <span data-ttu-id="aad6c-113">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="aad6c-113">-ApplicationGateway</span></span>
<span data-ttu-id="aad6c-114">Określa obiekt bramy aplikacji, który zawiera odbiornik HTTP.</span><span class="sxs-lookup"><span data-stu-id="aad6c-114">Specifies the application gateway object that contains the HTTP listener.</span></span>

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

### <span data-ttu-id="aad6c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aad6c-115">-DefaultProfile</span></span>
<span data-ttu-id="aad6c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="aad6c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aad6c-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="aad6c-117">-Name</span></span>
<span data-ttu-id="aad6c-118">Określa nazwę odbiornika HTTP, który ma być pobierany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aad6c-118">Specifies the name of the HTTP listener which this cmdlet gets.</span></span>

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

### <span data-ttu-id="aad6c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aad6c-119">CommonParameters</span></span>
<span data-ttu-id="aad6c-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aad6c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aad6c-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="aad6c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aad6c-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aad6c-122">INPUTS</span></span>

### <span data-ttu-id="aad6c-123">System. String</span><span class="sxs-lookup"><span data-stu-id="aad6c-123">System.String</span></span>

## <span data-ttu-id="aad6c-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="aad6c-124">OUTPUTS</span></span>

### <span data-ttu-id="aad6c-125">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="aad6c-125">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener</span></span>

## <span data-ttu-id="aad6c-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="aad6c-126">NOTES</span></span>

## <span data-ttu-id="aad6c-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aad6c-127">RELATED LINKS</span></span>

[<span data-ttu-id="aad6c-128">Dodaj-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="aad6c-128">Add-AzApplicationGatewayHttpListener</span></span>](./Add-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="aad6c-129">Nowe — AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="aad6c-129">New-AzApplicationGatewayHttpListener</span></span>](./New-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="aad6c-130">Remove-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="aad6c-130">Remove-AzApplicationGatewayHttpListener</span></span>](./Remove-AzApplicationGatewayHttpListener.md)

[<span data-ttu-id="aad6c-131">Set-AzApplicationGatewayHttpListener</span><span class="sxs-lookup"><span data-stu-id="aad6c-131">Set-AzApplicationGatewayHttpListener</span></span>](./Set-AzApplicationGatewayHttpListener.md)


