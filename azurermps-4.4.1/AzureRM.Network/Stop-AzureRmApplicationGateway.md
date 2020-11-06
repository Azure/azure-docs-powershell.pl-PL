---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: 6c2de883a797c445105edddfc562bc2d494fd234
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527377"
---
# <span data-ttu-id="962dd-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="962dd-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="962dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="962dd-102">SYNOPSIS</span></span>
<span data-ttu-id="962dd-103">Zatrzymuje bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="962dd-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="962dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="962dd-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="962dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="962dd-105">DESCRIPTION</span></span>
<span data-ttu-id="962dd-106">Polecenie cmdlet **stop-AzureRmApplicationGateway** zatrzymuje bramę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="962dd-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="962dd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="962dd-107">EXAMPLES</span></span>

### <span data-ttu-id="962dd-108">Przykład 1: zatrzymywanie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="962dd-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="962dd-109">To polecenie zatrzymuje bramę aplikacji przechowywaną w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="962dd-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="962dd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="962dd-110">PARAMETERS</span></span>

### <span data-ttu-id="962dd-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="962dd-111">-ApplicationGateway</span></span>
<span data-ttu-id="962dd-112">Określa bramę aplikacji, która zostanie zatrzymana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="962dd-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="962dd-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="962dd-113">-DefaultProfile</span></span>
<span data-ttu-id="962dd-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="962dd-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="962dd-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="962dd-115">CommonParameters</span></span>
<span data-ttu-id="962dd-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="962dd-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="962dd-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="962dd-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="962dd-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="962dd-118">INPUTS</span></span>

### <span data-ttu-id="962dd-119">System. String</span><span class="sxs-lookup"><span data-stu-id="962dd-119">System.String</span></span>

## <span data-ttu-id="962dd-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="962dd-120">OUTPUTS</span></span>

### <span data-ttu-id="962dd-121">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="962dd-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="962dd-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="962dd-122">NOTES</span></span>

## <span data-ttu-id="962dd-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="962dd-123">RELATED LINKS</span></span>

[<span data-ttu-id="962dd-124">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="962dd-124">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="962dd-125">Nowe — AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="962dd-125">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="962dd-126">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="962dd-126">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="962dd-127">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="962dd-127">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="962dd-128">Start — AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="962dd-128">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


