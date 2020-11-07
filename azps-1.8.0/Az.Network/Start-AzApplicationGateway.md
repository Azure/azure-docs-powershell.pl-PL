---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 95731734-EDCA-432A-A7BF-94D1E3725FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/start-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Start-AzApplicationGateway.md
ms.openlocfilehash: f90e35e0b8a88d7fa7b5089adf205bf6fe14e18f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708912"
---
# <span data-ttu-id="3d76a-101">Start-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d76a-101">Start-AzApplicationGateway</span></span>

## <span data-ttu-id="3d76a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3d76a-102">SYNOPSIS</span></span>
<span data-ttu-id="3d76a-103">Uruchamia bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="3d76a-103">Starts an application gateway.</span></span>

## <span data-ttu-id="3d76a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3d76a-104">SYNTAX</span></span>

```
Start-AzApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3d76a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="3d76a-105">DESCRIPTION</span></span>
<span data-ttu-id="3d76a-106">Polecenie cmdlet **Start-AzApplicationGateway** uruchamia bramę aplikacji platformy Azure</span><span class="sxs-lookup"><span data-stu-id="3d76a-106">The **Start-AzApplicationGateway** cmdlet starts an Azure application gateway</span></span>

## <span data-ttu-id="3d76a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3d76a-107">EXAMPLES</span></span>

### <span data-ttu-id="3d76a-108">Example1: uruchamianie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="3d76a-108">Example1: Start an application gateway</span></span>
```
PS C:\>$AppGw = Start-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="3d76a-109">To polecenie uruchamia bramkę aplikacji przechowywaną w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="3d76a-109">This command starts the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="3d76a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3d76a-110">PARAMETERS</span></span>

### <span data-ttu-id="3d76a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d76a-111">-ApplicationGateway</span></span>
<span data-ttu-id="3d76a-112">Określa bramę aplikacji, która jest uruchamiana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3d76a-112">Specifies the application gateway that this cmdlet starts.</span></span>

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

### <span data-ttu-id="3d76a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d76a-113">-DefaultProfile</span></span>
<span data-ttu-id="3d76a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3d76a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3d76a-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d76a-115">CommonParameters</span></span>
<span data-ttu-id="3d76a-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3d76a-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d76a-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3d76a-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d76a-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3d76a-118">INPUTS</span></span>

### <span data-ttu-id="3d76a-119">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d76a-119">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3d76a-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3d76a-120">OUTPUTS</span></span>

### <span data-ttu-id="3d76a-121">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d76a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="3d76a-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3d76a-122">NOTES</span></span>

## <span data-ttu-id="3d76a-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3d76a-123">RELATED LINKS</span></span>

[<span data-ttu-id="3d76a-124">Zatrzymaj — AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="3d76a-124">Stop-AzApplicationGateway</span></span>](./Stop-AzApplicationGateway.md)

