---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/stop-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Stop-AzApplicationGateway.md
ms.openlocfilehash: 4c7001bf69e6dc8f418f1bc56867154bf9d769ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894545"
---
# <span data-ttu-id="0dce1-101">Stop-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0dce1-101">Stop-AzApplicationGateway</span></span>

## <span data-ttu-id="0dce1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0dce1-102">SYNOPSIS</span></span>
<span data-ttu-id="0dce1-103">Zatrzymuje bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="0dce1-103">Stops an application gateway</span></span>

## <span data-ttu-id="0dce1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0dce1-104">SYNTAX</span></span>

```
Stop-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0dce1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0dce1-105">DESCRIPTION</span></span>
<span data-ttu-id="0dce1-106">Polecenie cmdlet **stop-AzApplicationGateway** zatrzymuje bramę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="0dce1-106">The **Stop-AzApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="0dce1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0dce1-107">EXAMPLES</span></span>

### <span data-ttu-id="0dce1-108">Przykład 1: zatrzymywanie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="0dce1-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="0dce1-109">To polecenie zatrzymuje bramę aplikacji przechowywaną w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="0dce1-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="0dce1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0dce1-110">PARAMETERS</span></span>

### <span data-ttu-id="0dce1-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0dce1-111">-ApplicationGateway</span></span>
<span data-ttu-id="0dce1-112">Określa bramę aplikacji, która zostanie zatrzymana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0dce1-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="0dce1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0dce1-113">-AsJob</span></span>
<span data-ttu-id="0dce1-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="0dce1-114">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dce1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dce1-115">-DefaultProfile</span></span>
<span data-ttu-id="0dce1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0dce1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0dce1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dce1-117">CommonParameters</span></span>
<span data-ttu-id="0dce1-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0dce1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dce1-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0dce1-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dce1-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0dce1-120">INPUTS</span></span>

### <span data-ttu-id="0dce1-121">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0dce1-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0dce1-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0dce1-122">OUTPUTS</span></span>

### <span data-ttu-id="0dce1-123">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0dce1-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="0dce1-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0dce1-124">NOTES</span></span>

## <span data-ttu-id="0dce1-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0dce1-125">RELATED LINKS</span></span>

[<span data-ttu-id="0dce1-126">Get-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0dce1-126">Get-AzApplicationGateway</span></span>](./Get-AzApplicationGateway.md)

[<span data-ttu-id="0dce1-127">Nowe — AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0dce1-127">New-AzApplicationGateway</span></span>](./New-AzApplicationGateway.md)

[<span data-ttu-id="0dce1-128">Remove-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0dce1-128">Remove-AzApplicationGateway</span></span>](./Remove-AzApplicationGateway.md)

[<span data-ttu-id="0dce1-129">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0dce1-129">Set-AzApplicationGateway</span></span>](./Set-AzApplicationGateway.md)

[<span data-ttu-id="0dce1-130">Start — AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="0dce1-130">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


