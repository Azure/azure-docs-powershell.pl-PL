---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2C9609E8-0D8B-471B-9F0E-672BF55C3A0E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/stop-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Stop-AzureRmApplicationGateway.md
ms.openlocfilehash: a235ae8ad4467e135e85599300869bcb36805a30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717258"
---
# <span data-ttu-id="f5fad-101">Stop-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5fad-101">Stop-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="f5fad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f5fad-102">SYNOPSIS</span></span>
<span data-ttu-id="f5fad-103">Zatrzymuje bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f5fad-103">Stops an application gateway</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5fad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f5fad-104">SYNTAX</span></span>

```
Stop-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5fad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f5fad-105">DESCRIPTION</span></span>
<span data-ttu-id="f5fad-106">Polecenie cmdlet **stop-AzureRmApplicationGateway** zatrzymuje bramę Application Gateway.</span><span class="sxs-lookup"><span data-stu-id="f5fad-106">The **Stop-AzureRmApplicationGateway** cmdlet stops an application gateway.</span></span>

## <span data-ttu-id="f5fad-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f5fad-107">EXAMPLES</span></span>

### <span data-ttu-id="f5fad-108">Przykład 1: zatrzymywanie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="f5fad-108">Example 1: Stop an application gateway</span></span>
```
PS C:\>Stop-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="f5fad-109">To polecenie zatrzymuje bramę aplikacji przechowywaną w zmiennej $AppGw.</span><span class="sxs-lookup"><span data-stu-id="f5fad-109">This command stops the application gateway stored in the $AppGw variable.</span></span>

## <span data-ttu-id="f5fad-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f5fad-110">PARAMETERS</span></span>

### <span data-ttu-id="f5fad-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5fad-111">-ApplicationGateway</span></span>
<span data-ttu-id="f5fad-112">Określa bramę aplikacji, która zostanie zatrzymana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5fad-112">Specifies the application gateway that this cmdlet stops.</span></span>

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

### <span data-ttu-id="f5fad-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f5fad-113">-AsJob</span></span>
<span data-ttu-id="f5fad-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f5fad-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f5fad-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5fad-115">-DefaultProfile</span></span>
<span data-ttu-id="f5fad-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5fad-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5fad-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5fad-117">CommonParameters</span></span>
<span data-ttu-id="f5fad-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5fad-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5fad-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5fad-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5fad-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5fad-120">INPUTS</span></span>

### <span data-ttu-id="f5fad-121">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5fad-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>
<span data-ttu-id="f5fad-122">Parametry: ApplicationGateway (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f5fad-122">Parameters: ApplicationGateway (ByValue)</span></span>

## <span data-ttu-id="f5fad-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f5fad-123">OUTPUTS</span></span>

### <span data-ttu-id="f5fad-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5fad-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f5fad-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f5fad-125">NOTES</span></span>

## <span data-ttu-id="f5fad-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5fad-126">RELATED LINKS</span></span>

[<span data-ttu-id="f5fad-127">Get-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5fad-127">Get-AzureRmApplicationGateway</span></span>](./Get-AzureRmApplicationGateway.md)

[<span data-ttu-id="f5fad-128">Nowe — AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5fad-128">New-AzureRmApplicationGateway</span></span>](./New-AzureRmApplicationGateway.md)

[<span data-ttu-id="f5fad-129">Remove-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5fad-129">Remove-AzureRmApplicationGateway</span></span>](./Remove-AzureRmApplicationGateway.md)

[<span data-ttu-id="f5fad-130">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5fad-130">Set-AzureRmApplicationGateway</span></span>](./Set-AzureRmApplicationGateway.md)

[<span data-ttu-id="f5fad-131">Start — AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f5fad-131">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)

