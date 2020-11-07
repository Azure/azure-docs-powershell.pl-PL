---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/start-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Start-AzureRmApplicationGateway.md
ms.openlocfilehash: 88ca18eca50f1e68eab8599ad79f902ff1fd2551
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717260"
---
# <span data-ttu-id="650db-101">Start-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="650db-101">Start-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="650db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="650db-102">SYNOPSIS</span></span>
<span data-ttu-id="650db-103">Uruchamia bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="650db-103">Starts an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="650db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="650db-104">SYNTAX</span></span>

```
Start-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="650db-105">Opis</span><span class="sxs-lookup"><span data-stu-id="650db-105">DESCRIPTION</span></span>
<span data-ttu-id="650db-106">Polecenie cmdlet **Start-AzureRmApplicationGateway** uruchamia bramę aplikacji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="650db-106">The **Start-AzureRmApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="650db-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="650db-107">EXAMPLES</span></span>

### <span data-ttu-id="650db-108">Example1: uruchamianie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="650db-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="650db-109">To polecenie uruchamia bramkę aplikacji przechowywaną w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="650db-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="650db-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="650db-110">PARAMETERS</span></span>

### <span data-ttu-id="650db-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="650db-111">-ApplicationGateway</span></span>
<span data-ttu-id="650db-112">Określa bramę aplikacji, która jest uruchamiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="650db-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="650db-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="650db-113">-DefaultProfile</span></span>
<span data-ttu-id="650db-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="650db-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="650db-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="650db-115">CommonParameters</span></span>
<span data-ttu-id="650db-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="650db-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="650db-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="650db-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="650db-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="650db-118">INPUTS</span></span>

### <span data-ttu-id="650db-119">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="650db-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="650db-120">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="650db-120">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="650db-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="650db-121">OUTPUTS</span></span>

### <span data-ttu-id="650db-122">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="650db-122">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="650db-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="650db-123">NOTES</span></span>

## <span data-ttu-id="650db-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="650db-124">RELATED LINKS</span></span>

[<span data-ttu-id="650db-125">Zatrzymaj — AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="650db-125">Stop-AzureRmApplicationGateway</span></span>](./Stop-AzureRmApplicationGateway.md)


