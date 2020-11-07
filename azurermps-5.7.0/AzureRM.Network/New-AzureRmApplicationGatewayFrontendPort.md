---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfrontendport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendPort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayFrontendPort.md
ms.openlocfilehash: bccdcb5f94cc90dca04229ca643fd23f29a276e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717100"
---
# <span data-ttu-id="06956-101">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="06956-101">New-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="06956-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="06956-102">SYNOPSIS</span></span>
<span data-ttu-id="06956-103">Tworzy port frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="06956-103">Creates a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06956-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="06956-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFrontendPort -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06956-105">Opis</span><span class="sxs-lookup"><span data-stu-id="06956-105">DESCRIPTION</span></span>
<span data-ttu-id="06956-106">Polecenie cmdlet **New-AzureRmApplicationGatewayFrontendPort** tworzy port frontonu dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="06956-106">The **New-AzureRmApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="06956-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="06956-107">EXAMPLES</span></span>

### <span data-ttu-id="06956-108">Example1: Tworzenie portu frontonu</span><span class="sxs-lookup"><span data-stu-id="06956-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="06956-109">To polecenie tworzy port frontonu o nazwie FrontEndPort01 na porcie 80 i zapisuje wynik w zmiennej o nazwie $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="06956-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="06956-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="06956-110">PARAMETERS</span></span>

### <span data-ttu-id="06956-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06956-111">-DefaultProfile</span></span>
<span data-ttu-id="06956-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="06956-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06956-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="06956-113">-Name</span></span>
<span data-ttu-id="06956-114">Określa nazwę portu frontonu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06956-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06956-115">-Port</span><span class="sxs-lookup"><span data-stu-id="06956-115">-Port</span></span>
<span data-ttu-id="06956-116">Określa numer portu na porcie frontonu.</span><span class="sxs-lookup"><span data-stu-id="06956-116">Specifies the port number of the front-end port.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06956-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06956-117">CommonParameters</span></span>
<span data-ttu-id="06956-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06956-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06956-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06956-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06956-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06956-120">INPUTS</span></span>

### <span data-ttu-id="06956-121">System. String</span><span class="sxs-lookup"><span data-stu-id="06956-121">System.String</span></span>

## <span data-ttu-id="06956-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="06956-122">OUTPUTS</span></span>

### <span data-ttu-id="06956-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="06956-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="06956-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="06956-124">NOTES</span></span>

## <span data-ttu-id="06956-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06956-125">RELATED LINKS</span></span>

[<span data-ttu-id="06956-126">Dodaj-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="06956-126">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="06956-127">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="06956-127">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="06956-128">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="06956-128">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="06956-129">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="06956-129">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


