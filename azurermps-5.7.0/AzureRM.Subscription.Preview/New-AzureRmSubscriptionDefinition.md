---
external help file: Microsoft.Azure.Commands.SubscriptionDefinition.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.subscription.preview/new-azurermsubscriptiondefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Subscription/Commands.Subscription/help/New-AzureRmSubscriptionDefinition.md
ms.openlocfilehash: 7acaca4977114a1a57f88f5050f658753a9b6214
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550468"
---
# <span data-ttu-id="ce9b2-101">New-AzureRmSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="ce9b2-101">New-AzureRmSubscriptionDefinition</span></span>

## <span data-ttu-id="ce9b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ce9b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ce9b2-103">Tworzy definicję subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ce9b2-103">Creates a subscription definition.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce9b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ce9b2-104">SYNTAX</span></span>

### <span data-ttu-id="ce9b2-105">Utwórz definicję subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ce9b2-105">Create subscription definition</span></span>
```
New-AzureRmSubscriptionDefinition -Name <String> -OfferType <String> [-SubscriptionDisplayName <String>]
```

## <span data-ttu-id="ce9b2-106">Opis</span><span class="sxs-lookup"><span data-stu-id="ce9b2-106">DESCRIPTION</span></span>
<span data-ttu-id="ce9b2-107">Polecenie cmdlet **New-AzureRmSubscriptionDefinition** tworzy definicję subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ce9b2-107">The **New-AzureRmSubscriptionDefinition** cmdlet creates a subscription definition.</span></span>

## <span data-ttu-id="ce9b2-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ce9b2-108">EXAMPLES</span></span>

### <span data-ttu-id="ce9b2-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ce9b2-109">Example 1</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MySubDef
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="ce9b2-110">Tworzy definicję subskrypcji z domyślną nazwą wyświetlaną subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ce9b2-110">Creates a subscription definition with a default subscription display name.</span></span>

### <span data-ttu-id="ce9b2-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ce9b2-111">Example 2</span></span>
```
PS C:\> New-AzureRmSubscriptionDefinition -Name MySubDef -OfferType MS-AZR-0017P -SubscriptionDisplayName MyPaygoSub

Name                    : MySubDef
SubscriptionId          : 86869d42-1782-4337-98b0-c905fb937d46
SubscriptionDisplayName : MyPaygoSub
OfferType               : MS-AZR-0017P
```

<span data-ttu-id="ce9b2-112">Tworzy definicję subskrypcji z niestandardową nazwą wyświetlaną subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ce9b2-112">Creates a subscription definition with a custom subscription display name.</span></span>

## <span data-ttu-id="ce9b2-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ce9b2-113">PARAMETERS</span></span>

### <span data-ttu-id="ce9b2-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ce9b2-114">-Name</span></span>
<span data-ttu-id="ce9b2-115">Nazwa definicji subskrypcji do utworzenia.</span><span class="sxs-lookup"><span data-stu-id="ce9b2-115">The name of the subscription definition to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce9b2-116">-Offertype</span><span class="sxs-lookup"><span data-stu-id="ce9b2-116">-OfferType</span></span>
<span data-ttu-id="ce9b2-117">Typ oferty, który ma być używany podczas tworzenia subskrypcji podstawowej.</span><span class="sxs-lookup"><span data-stu-id="ce9b2-117">The type of offer to use when creating the underlying subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce9b2-118">-SubscriptionDisplayName</span><span class="sxs-lookup"><span data-stu-id="ce9b2-118">-SubscriptionDisplayName</span></span>
<span data-ttu-id="ce9b2-119">Nazwa wyświetlana, która ma być używana podczas tworzenia abonamentu podstawowego definicji subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ce9b2-119">The display name to use when creating the subscription definition's underlying subscription.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Name
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce9b2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce9b2-120">CommonParameters</span></span>
<span data-ttu-id="ce9b2-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ce9b2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce9b2-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce9b2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce9b2-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ce9b2-123">INPUTS</span></span>

### <span data-ttu-id="ce9b2-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="ce9b2-124">None</span></span>

## <span data-ttu-id="ce9b2-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ce9b2-125">OUTPUTS</span></span>

### <span data-ttu-id="ce9b2-126">Microsoft. Azure. Commands. SubscriptionDefinition. models. PSSubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="ce9b2-126">Microsoft.Azure.Commands.SubscriptionDefinition.Models.PSSubscriptionDefinition</span></span>

## <span data-ttu-id="ce9b2-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ce9b2-127">NOTES</span></span>

## <span data-ttu-id="ce9b2-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ce9b2-128">RELATED LINKS</span></span>

