---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGateway.md
ms.openlocfilehash: ff836268c92b575db05e05b1843c57af2bc6dca7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552867"
---
# <span data-ttu-id="bf8a6-101">Set-AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf8a6-101">Set-AzureRmApplicationGateway</span></span>

## <span data-ttu-id="bf8a6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf8a6-102">SYNOPSIS</span></span>
<span data-ttu-id="bf8a6-103">Umożliwia zaktualizowanie bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bf8a6-103">Updates an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf8a6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf8a6-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bf8a6-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bf8a6-105">DESCRIPTION</span></span>
<span data-ttu-id="bf8a6-106">Polecenie cmdlet **Set-AzureRmApplicationGateway** umożliwia zaktualizowanie bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bf8a6-106">The **Set-AzureRmApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="bf8a6-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf8a6-107">EXAMPLES</span></span>

### <span data-ttu-id="bf8a6-108">Przykład 1: aktualizowanie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="bf8a6-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzureRmApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="bf8a6-109">To polecenie aktualizuje bramę aplikacji za pomocą ustawień w zmiennej $AppGw i przechowuje zaktualizowaną bramę w zmiennej $UpdatedAppGw.</span><span class="sxs-lookup"><span data-stu-id="bf8a6-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="bf8a6-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf8a6-110">PARAMETERS</span></span>

### <span data-ttu-id="bf8a6-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf8a6-111">-ApplicationGateway</span></span>
<span data-ttu-id="bf8a6-112">Określa obiekt bramy aplikacji reprezentujący stan, w którym należy ustawić bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="bf8a6-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="bf8a6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf8a6-113">-AsJob</span></span>
<span data-ttu-id="bf8a6-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="bf8a6-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="bf8a6-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf8a6-115">-DefaultProfile</span></span>
<span data-ttu-id="bf8a6-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf8a6-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf8a6-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf8a6-117">CommonParameters</span></span>
<span data-ttu-id="bf8a6-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf8a6-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf8a6-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf8a6-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf8a6-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf8a6-120">INPUTS</span></span>

### <span data-ttu-id="bf8a6-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf8a6-121">PSApplicationGateway</span></span>
<span data-ttu-id="bf8a6-122">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="bf8a6-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="bf8a6-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf8a6-123">OUTPUTS</span></span>

### <span data-ttu-id="bf8a6-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf8a6-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="bf8a6-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf8a6-125">NOTES</span></span>

## <span data-ttu-id="bf8a6-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf8a6-126">RELATED LINKS</span></span>

[<span data-ttu-id="bf8a6-127">Start — AzureRmApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="bf8a6-127">Start-AzureRmApplicationGateway</span></span>](./Start-AzureRmApplicationGateway.md)


