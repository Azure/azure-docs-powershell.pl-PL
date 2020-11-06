---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/get-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/Get-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/Get-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 8f9cfda051542327fdb6175da081c99e6b8b6b3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526494"
---
# <span data-ttu-id="c7668-101">Get-AzureRmSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="c7668-101">Get-AzureRmSubscriptionDefinition</span></span>

## <span data-ttu-id="c7668-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c7668-102">SYNOPSIS</span></span>
<span data-ttu-id="c7668-103">Pobierz definicję subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c7668-103">Get a subscription definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7668-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c7668-104">SYNTAX</span></span>

### <span data-ttu-id="c7668-105">Pobierz Definicje subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c7668-105">Get subscription definitions.</span></span>
```
Get-AzureRmSubscriptionDefinition
```

## <span data-ttu-id="c7668-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c7668-106">EXAMPLES</span></span>

### <span data-ttu-id="c7668-107">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c7668-107">Example 1</span></span>
```
PS C:\> Get-AzureRmSubscriptionDefinition

Name                    : MyProdSubscription1
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyProdSubscription1
OfferType               : MS-AZR-0017P

Name                    : MyProdSubscription2
SubscriptionId          : 368425df-b536-4f42-b1ba-64613cfcc4b5
SubscriptionDisplayName : MyProdSubscription2
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="c7668-108">Pobiera wszystkie definicje abonamentów.</span><span class="sxs-lookup"><span data-stu-id="c7668-108">Gets all subscription definitions.</span></span>

### <span data-ttu-id="c7668-109">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c7668-109">Example 2</span></span>
```
PS C:\> Get-AzureRmSubscriptionDefinition -Name MyProdSubscription2

Name                    : MyProdSubscription2
SubscriptionId          : 368425df-b536-4f42-b1ba-64613cfcc4b5
SubscriptionDisplayName : MyProdSubscription2
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="c7668-110">Pobiera definicję subskrypcji o nazwie MyProdSubscription2.</span><span class="sxs-lookup"><span data-stu-id="c7668-110">Gets a subscription definition with the name MyProdSubscription2.</span></span>

## <span data-ttu-id="c7668-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c7668-111">PARAMETERS</span></span>

### <span data-ttu-id="c7668-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c7668-112">-Name</span></span>
<span data-ttu-id="c7668-113">Nazwa definicji subskrypcji do pobrania.</span><span class="sxs-lookup"><span data-stu-id="c7668-113">The name of the subscription definition to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c7668-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7668-114">CommonParameters</span></span>
<span data-ttu-id="c7668-115">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7668-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7668-116">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7668-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7668-117">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7668-117">INPUTS</span></span>

### <span data-ttu-id="c7668-118">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c7668-118">None</span></span>

## <span data-ttu-id="c7668-119">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c7668-119">OUTPUTS</span></span>

### <span data-ttu-id="c7668-120">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. SubscriptionDefinition. MODELES. PSSubscriptionDefinition, Microsoft. Azure. Commands. SubscriptionDefinition, Version = 0.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c7668-120">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.SubscriptionDefinition.Models.PSSubscriptionDefinition, Microsoft.Azure.Commands.SubscriptionDefinition, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c7668-121">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c7668-121">NOTES</span></span>

## <span data-ttu-id="c7668-122">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7668-122">RELATED LINKS</span></span>

