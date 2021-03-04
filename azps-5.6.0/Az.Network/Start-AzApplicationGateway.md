---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: 4d2f3f225e185678dd1e3b0047810a5e68d4273f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952001"
---
# <span data-ttu-id="ac426-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac426-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="ac426-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ac426-102">SYNOPSIS</span></span>
<span data-ttu-id="ac426-103">Pozwala na rozpoczęcie pracy z bramą aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ac426-103">Starts an application gateway.</span></span>

## <span data-ttu-id="ac426-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ac426-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ac426-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ac426-105">DESCRIPTION</span></span>
<span data-ttu-id="ac426-106">Polecenie **cmdlet Start-AzApplicationGateway** umożliwia uruchomienie bramy aplikacji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="ac426-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="ac426-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ac426-107">EXAMPLES</span></span>

### <span data-ttu-id="ac426-108">Przykład1. Uruchamianie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="ac426-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="ac426-109">To polecenie uruchamia bramę aplikacji przechowywaną w $AppGw aplikacji.</span><span class="sxs-lookup"><span data-stu-id="ac426-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="ac426-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ac426-110">PARAMETERS</span></span>

### <span data-ttu-id="ac426-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac426-111">-ApplicationGateway</span></span>
<span data-ttu-id="ac426-112">Określa bramę aplikacji uruchamianą przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ac426-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="ac426-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac426-113">-DefaultProfile</span></span>
<span data-ttu-id="ac426-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ac426-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac426-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac426-115">CommonParameters</span></span>
<span data-ttu-id="ac426-116">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac426-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac426-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac426-117">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac426-118">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac426-118">INPUTS</span></span>

### <span data-ttu-id="ac426-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac426-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ac426-120">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ac426-120">OUTPUTS</span></span>

### <span data-ttu-id="ac426-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac426-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ac426-122">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ac426-122">NOTES</span></span>

## <span data-ttu-id="ac426-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ac426-123">RELATED LINKS</span></span>

[<span data-ttu-id="ac426-124">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ac426-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)


