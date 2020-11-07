---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgateway
schema: 2.0.0
ms.openlocfilehash: 1b852be30b513963f5d311940162078bdf6f692a
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899210"
---
# <span data-ttu-id="074b1-101">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="074b1-101">Set-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="074b1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="074b1-102">SYNOPSIS</span></span>
<span data-ttu-id="074b1-103">Umożliwia zaktualizowanie bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="074b1-103">Updates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="074b1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="074b1-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="074b1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="074b1-105">DESCRIPTION</span></span>
<span data-ttu-id="074b1-106">Polecenie cmdlet **Set-AzureRmApplicationGateway** umożliwia zaktualizowanie bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="074b1-106">The **Set-AzureRmApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="074b1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="074b1-107">EXAMPLES</span></span>

### <span data-ttu-id="074b1-108">Przykład 1: aktualizowanie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="074b1-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="074b1-109">To polecenie aktualizuje bramę aplikacji za pomocą ustawień w zmiennej $AppGw i przechowuje zaktualizowaną bramę w zmiennej $UpdatedAppGw.</span><span class="sxs-lookup"><span data-stu-id="074b1-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="074b1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="074b1-110">PARAMETERS</span></span>

### <span data-ttu-id="074b1-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="074b1-111">-ApplicationGateway</span></span>
<span data-ttu-id="074b1-112">Określa obiekt bramy aplikacji reprezentujący stan, w którym należy ustawić bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="074b1-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="074b1-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="074b1-113">-AsJob</span></span>
<span data-ttu-id="074b1-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="074b1-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="074b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="074b1-115">-DefaultProfile</span></span>
<span data-ttu-id="074b1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="074b1-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="074b1-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="074b1-117">CommonParameters</span></span>
<span data-ttu-id="074b1-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="074b1-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="074b1-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="074b1-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="074b1-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="074b1-120">INPUTS</span></span>

### <span data-ttu-id="074b1-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="074b1-121">PSApplicationGateway</span></span>
<span data-ttu-id="074b1-122">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="074b1-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="074b1-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="074b1-123">OUTPUTS</span></span>

### <span data-ttu-id="074b1-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="074b1-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="074b1-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="074b1-125">NOTES</span></span>

## <span data-ttu-id="074b1-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="074b1-126">RELATED LINKS</span></span>

[<span data-ttu-id="074b1-127">Start — AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="074b1-127">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


