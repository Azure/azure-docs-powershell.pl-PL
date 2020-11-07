---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 7C8B47B4-2F6A-45EF-A351-88C8C3F9D0D3
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGateway.md
ms.openlocfilehash: b62a41c2c97055f0ef090ed5def3dc771ae3c1ed
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892878"
---
# <span data-ttu-id="90119-101">Set-AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90119-101">Set-AzApplicationGateway</span></span>

## <span data-ttu-id="90119-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90119-102">SYNOPSIS</span></span>
<span data-ttu-id="90119-103">Umożliwia zaktualizowanie bramy aplikacji.</span><span class="sxs-lookup"><span data-stu-id="90119-103">Updates an application gateway.</span></span>

## <span data-ttu-id="90119-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90119-104">SYNTAX</span></span>

```
Set-AzApplicationGateway -ApplicationGateway <PSApplicationGateway> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90119-105">Opis</span><span class="sxs-lookup"><span data-stu-id="90119-105">DESCRIPTION</span></span>
<span data-ttu-id="90119-106">Polecenie cmdlet **Set-AzApplicationGateway** umożliwia zaktualizowanie bramy aplikacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="90119-106">The **Set-AzApplicationGateway** cmdlet updates an Azure application gateway.</span></span>

## <span data-ttu-id="90119-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90119-107">EXAMPLES</span></span>

### <span data-ttu-id="90119-108">Przykład 1: aktualizowanie bramy aplikacji</span><span class="sxs-lookup"><span data-stu-id="90119-108">Example 1: Update an application gateway</span></span>
```
PS C:\>$UpdatedAppGw = Set-AzApplicationGateway -ApplicationGateway $AppGw
```

<span data-ttu-id="90119-109">To polecenie aktualizuje bramę aplikacji za pomocą ustawień w zmiennej $AppGw i przechowuje zaktualizowaną bramę w zmiennej $UpdatedAppGw.</span><span class="sxs-lookup"><span data-stu-id="90119-109">This command updates the application gateway with settings in the $AppGw variable and stores the updated gateway in the $UpdatedAppGw variable.</span></span>

## <span data-ttu-id="90119-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90119-110">PARAMETERS</span></span>

### <span data-ttu-id="90119-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90119-111">-ApplicationGateway</span></span>
<span data-ttu-id="90119-112">Określa obiekt bramy aplikacji reprezentujący stan, w którym należy ustawić bramę aplikacji.</span><span class="sxs-lookup"><span data-stu-id="90119-112">Specifies an application gateway object representing the state to which the application gateway should be set.</span></span>

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

### <span data-ttu-id="90119-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="90119-113">-AsJob</span></span>
<span data-ttu-id="90119-114">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="90119-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="90119-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90119-115">-DefaultProfile</span></span>
<span data-ttu-id="90119-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90119-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90119-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90119-117">CommonParameters</span></span>
<span data-ttu-id="90119-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90119-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90119-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90119-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90119-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90119-120">INPUTS</span></span>

### <span data-ttu-id="90119-121">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90119-121">PSApplicationGateway</span></span>
<span data-ttu-id="90119-122">Parametr "ApplicationGateway" akceptuje wartość typu "PSApplicationGateway" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="90119-122">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="90119-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90119-123">OUTPUTS</span></span>

### <span data-ttu-id="90119-124">Microsoft. Azure. Commands. Network. models. PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90119-124">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="90119-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90119-125">NOTES</span></span>

## <span data-ttu-id="90119-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90119-126">RELATED LINKS</span></span>

[<span data-ttu-id="90119-127">Start — AzApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="90119-127">Start-AzApplicationGateway</span></span>](./Start-AzApplicationGateway.md)


