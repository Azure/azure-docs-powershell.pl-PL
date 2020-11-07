---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: 34f3de9e2dafe3cfb9b15aad1dda7d75bab67c20
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871143"
---
# <span data-ttu-id="60a1a-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="60a1a-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="60a1a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="60a1a-102">SYNOPSIS</span></span>
<span data-ttu-id="60a1a-103">Umożliwia zaktualizowanie bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="60a1a-103">Updates an application gateway.</span></span>

## <span data-ttu-id="60a1a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="60a1a-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="60a1a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="60a1a-105">DESCRIPTION</span></span>
<span data-ttu-id="60a1a-106">Polecenie cmdlet **Set-AzApplicationGateway** umożliwia zaktualizowanie bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="60a1a-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="60a1a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="60a1a-107">EXAMPLES</span></span>

### <span data-ttu-id="60a1a-108">Przykład 1: aktualizowanie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="60a1a-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="60a1a-109">To polecenie aktualizuje bramę aplikacji za pomocą ustawień w zmiennej $AppGw i przechowuje zaktualizowaną bramę w zmiennej $UpdatedAppGw.</span><span class="sxs-lookup"><span data-stu-id="60a1a-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="60a1a-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="60a1a-110">PARAMETERS</span></span>

### <span data-ttu-id="60a1a-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="60a1a-111">-ApplicationGateway</span></span>
<span data-ttu-id="60a1a-112">Określa obiekt bramy aplikacji reprezentujący stan, w którym należy ustawić bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="60a1a-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="60a1a-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="60a1a-113">-AsJob</span></span>
<span data-ttu-id="60a1a-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="60a1a-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="60a1a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60a1a-115">-DefaultProfile</span></span>
<span data-ttu-id="60a1a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="60a1a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="60a1a-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60a1a-117">CommonParameters</span></span>
<span data-ttu-id="60a1a-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="60a1a-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60a1a-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60a1a-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60a1a-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="60a1a-120">INPUTS</span></span>

### <span data-ttu-id="60a1a-121">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="60a1a-121">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="60a1a-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="60a1a-122">OUTPUTS</span></span>

### <span data-ttu-id="60a1a-123">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="60a1a-123">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="60a1a-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="60a1a-124">NOTES</span></span>

## <span data-ttu-id="60a1a-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="60a1a-125">RELATED LINKS</span></span>

[<span data-ttu-id="60a1a-126">Start — AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="60a1a-126">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


