---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 382c4cd1b189e0dc95edd4824dec58a280dbb889
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898876"
---
# <span data-ttu-id="0270f-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0270f-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="0270f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0270f-102">SYNOPSIS</span></span>
<span data-ttu-id="0270f-103">Uruchamia bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0270f-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0270f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0270f-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0270f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0270f-105">DESCRIPTION</span></span>
<span data-ttu-id="0270f-106">Polecenie cmdlet **Start-AzureRmApplicationGateway** uruchamia bramę aplikacji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="0270f-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="0270f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0270f-107">EXAMPLES</span></span>

### <span data-ttu-id="0270f-108">Example1: uruchamianie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="0270f-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="0270f-109">To polecenie uruchamia bramkę aplikacji przechowywaną w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0270f-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="0270f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0270f-110">PARAMETERS</span></span>

### <span data-ttu-id="0270f-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0270f-111">-ApplicationGateway</span></span>
<span data-ttu-id="0270f-112">Określa bramę aplikacji, która jest uruchamiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0270f-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="0270f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0270f-113">-DefaultProfile</span></span>
<span data-ttu-id="0270f-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0270f-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0270f-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0270f-115">CommonParameters</span></span>
<span data-ttu-id="0270f-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0270f-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0270f-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0270f-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0270f-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0270f-118">INPUTS</span></span>

### <span data-ttu-id="0270f-119">System. String</span><span class="sxs-lookup"><span data-stu-id="0270f-119">System.String</span></span>

## <span data-ttu-id="0270f-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0270f-120">OUTPUTS</span></span>

### <span data-ttu-id="0270f-121">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0270f-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0270f-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0270f-122">NOTES</span></span>

## <span data-ttu-id="0270f-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0270f-123">RELATED LINKS</span></span>

[<span data-ttu-id="0270f-124">Zatrzymaj — AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0270f-124">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


