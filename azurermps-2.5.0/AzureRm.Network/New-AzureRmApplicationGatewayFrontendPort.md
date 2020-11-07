---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 3C046A0A-A2B6-413C-8D3B-8991A1FC4926
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayfrontendport
schema: 2.0.0
ms.openlocfilehash: f8b9d6b981300c32badbe69ec153865c04814dd6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898897"
---
# <span data-ttu-id="f4e9b-101">New-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f4e9b-101">New-AzureRmApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="f4e9b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f4e9b-102">SYNOPSIS</span></span>
<span data-ttu-id="f4e9b-103">Tworzy port frontonu dla bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f4e9b-103">Creates a front-end port for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4e9b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f4e9b-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayFrontendPort -Name <String> -Port <Int32>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f4e9b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f4e9b-105">DESCRIPTION</span></span>
<span data-ttu-id="f4e9b-106">Polecenie cmdlet **New-AzureRmApplicationGatewayFrontendPort** tworzy port frontonu dla bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f4e9b-106">The **New-AzureRmApplicationGatewayFrontendPort** cmdlet creates a front-end port for an Azure application gateway.</span></span>

## <span data-ttu-id="f4e9b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f4e9b-107">EXAMPLES</span></span>

### <span data-ttu-id="f4e9b-108">Example1: Tworzenie portu frontonu</span><span class="sxs-lookup"><span data-stu-id="f4e9b-108">Example1: Create a front-end port</span></span>
```
PS C:\>$FrontEndPort = New-AzureRmApplicationGatewayFrontendPort -Name "FrontEndPort01" -Port 80
```

<span data-ttu-id="f4e9b-109">To polecenie tworzy port frontonu o nazwie FrontEndPort01 na porcie 80 i zapisuje wynik w zmiennej o nazwie $FrontEndPort.</span><span class="sxs-lookup"><span data-stu-id="f4e9b-109">This command creates a front-end port named FrontEndPort01 on port 80 and stores the result in the variable named $FrontEndPort.</span></span>

## <span data-ttu-id="f4e9b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f4e9b-110">PARAMETERS</span></span>

### <span data-ttu-id="f4e9b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4e9b-111">-DefaultProfile</span></span>
<span data-ttu-id="f4e9b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f4e9b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f4e9b-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f4e9b-113">-Name</span></span>
<span data-ttu-id="f4e9b-114">Określa nazwę portu frontonu tworzonego przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f4e9b-114">Specifies the name of the front-end port that this cmdlet creates.</span></span>

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

### <span data-ttu-id="f4e9b-115">-Port</span><span class="sxs-lookup"><span data-stu-id="f4e9b-115">-Port</span></span>
<span data-ttu-id="f4e9b-116">Określa numer portu na porcie frontonu.</span><span class="sxs-lookup"><span data-stu-id="f4e9b-116">Specifies the port number of the front-end port.</span></span>

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

### <span data-ttu-id="f4e9b-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4e9b-117">CommonParameters</span></span>
<span data-ttu-id="f4e9b-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f4e9b-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4e9b-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4e9b-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4e9b-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f4e9b-120">INPUTS</span></span>

### <span data-ttu-id="f4e9b-121">System. String</span><span class="sxs-lookup"><span data-stu-id="f4e9b-121">System.String</span></span>

## <span data-ttu-id="f4e9b-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f4e9b-122">OUTPUTS</span></span>

### <span data-ttu-id="f4e9b-123">Microsoft. Azure. Commands. Network. models. PSApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f4e9b-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayFrontendPort</span></span>

## <span data-ttu-id="f4e9b-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f4e9b-124">NOTES</span></span>

## <span data-ttu-id="f4e9b-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f4e9b-125">RELATED LINKS</span></span>

[<span data-ttu-id="f4e9b-126">Dodaj-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f4e9b-126">Add-AzureRmApplicationGatewayFrontendPort</span></span>](./Add-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f4e9b-127">Get-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f4e9b-127">Get-AzureRmApplicationGatewayFrontendPort</span></span>](./Get-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f4e9b-128">Remove-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f4e9b-128">Remove-AzureRmApplicationGatewayFrontendPort</span></span>](./Remove-AzureRmApplicationGatewayFrontendPort.md)

[<span data-ttu-id="f4e9b-129">Set-AzureRmApplicationGatewayFrontendPort</span><span class="sxs-lookup"><span data-stu-id="f4e9b-129">Set-AzureRmApplicationGatewayFrontendPort</span></span>](./Set-AzureRmApplicationGatewayFrontendPort.md)


