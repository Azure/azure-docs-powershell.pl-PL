---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermserviceendpointpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmServiceEndpointPolicy.md
ms.openlocfilehash: ecd5a8eafc70a88b4ebda17a83f2b40139f5463f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717385"
---
# <span data-ttu-id="2b8b8-101">Set-AzureRmServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2b8b8-101">Set-AzureRmServiceEndpointPolicy</span></span>

## <span data-ttu-id="2b8b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b8b8-102">SYNOPSIS</span></span>
<span data-ttu-id="2b8b8-103">{{Wpisz w postaci streszczenia}}</span><span class="sxs-lookup"><span data-stu-id="2b8b8-103">{{Fill in the Synopsis}}</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2b8b8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b8b8-104">SYNTAX</span></span>

```
Set-AzureRmServiceEndpointPolicy -ServiceEndpointPolicy <PSServiceEndpointPolicy>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b8b8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2b8b8-105">DESCRIPTION</span></span>
<span data-ttu-id="2b8b8-106">Polecenie cmdlet **Set-AzureRmServiceEndpointPolicy** Tworzenie zasad punktu końcowego usługi.</span><span class="sxs-lookup"><span data-stu-id="2b8b8-106">The **Set-AzureRmServiceEndpointPolicy** cmdlet create a service endpoint policy.</span></span>

## <span data-ttu-id="2b8b8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b8b8-107">EXAMPLES</span></span>

### <span data-ttu-id="2b8b8-108">Przykład 1: Ustawianie zasad punktu końcowego usługi</span><span class="sxs-lookup"><span data-stu-id="2b8b8-108">Example 1: Sets a service endpoint policy</span></span>
```
$serviceEndpointPolicy = Set-AzureRmServiceEndpointPolicy -Name "Policy1" -ServiceEndpointPolicy $serviceEndpointPolicy -ResourceGroup "resourcegroup1"
```

<span data-ttu-id="2b8b8-109">To polecenie aktualizuje zasady punktu końcowego usługi o nazwie Policy1 zdefiniowane przez obiekt $serviceEndpointPolicy należą do obiektu resourceName "resourcegroup1".</span><span class="sxs-lookup"><span data-stu-id="2b8b8-109">This command updates a service endpoint policy named Policy1 defined by the object $serviceEndpointPolicy belong to the resourcegroup "resourcegroup1".</span></span>

## <span data-ttu-id="2b8b8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b8b8-110">PARAMETERS</span></span>

### <span data-ttu-id="2b8b8-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b8b8-111">-DefaultProfile</span></span>
<span data-ttu-id="2b8b8-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b8b8-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2b8b8-113">-ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2b8b8-113">-ServiceEndpointPolicy</span></span>
<span data-ttu-id="2b8b8-114">ServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2b8b8-114">The ServiceEndpointPolicy</span></span>

```yaml
Type: PSServiceEndpointPolicy
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b8b8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b8b8-115">CommonParameters</span></span>
<span data-ttu-id="2b8b8-116">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b8b8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2b8b8-117">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b8b8-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b8b8-118">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b8b8-118">INPUTS</span></span>

### <span data-ttu-id="2b8b8-119">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2b8b8-119">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="2b8b8-120">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b8b8-120">OUTPUTS</span></span>

### <span data-ttu-id="2b8b8-121">Microsoft. Azure. Commands. Network. models. PSServiceEndpointPolicy</span><span class="sxs-lookup"><span data-stu-id="2b8b8-121">Microsoft.Azure.Commands.Network.Models.PSServiceEndpointPolicy</span></span>


## <span data-ttu-id="2b8b8-122">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b8b8-122">NOTES</span></span>

## <span data-ttu-id="2b8b8-123">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b8b8-123">RELATED LINKS</span></span>
