---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5ff90957a655837dbdf75ce3f4242222615f2a73
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710763"
---
# <span data-ttu-id="b1395-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="b1395-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="b1395-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b1395-102">SYNOPSIS</span></span>
<span data-ttu-id="b1395-103">Pobieranie listy abonamentów użytkowników jako operatora.</span><span class="sxs-lookup"><span data-stu-id="b1395-103">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="b1395-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b1395-104">SYNTAX</span></span>

### <span data-ttu-id="b1395-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b1395-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="b1395-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="b1395-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="b1395-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b1395-107">DESCRIPTION</span></span>
<span data-ttu-id="b1395-108">Pobieranie listy abonamentów użytkowników jako operatora.</span><span class="sxs-lookup"><span data-stu-id="b1395-108">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="b1395-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b1395-109">EXAMPLES</span></span>

### <span data-ttu-id="b1395-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="b1395-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="b1395-111">Pobieranie listy abonamentów użytkowników jako operatora.</span><span class="sxs-lookup"><span data-stu-id="b1395-111">Get the list of user subscriptions as operator.</span></span>

## <span data-ttu-id="b1395-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b1395-112">PARAMETERS</span></span>

### <span data-ttu-id="b1395-113">-Filter</span><span class="sxs-lookup"><span data-stu-id="b1395-113">-Filter</span></span>
<span data-ttu-id="b1395-114">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="b1395-114">OData filter parameter.</span></span>

```yaml
Type: String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1395-115">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b1395-115">-SubscriptionId</span></span>
<span data-ttu-id="b1395-116">Parametr identyfikatora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="b1395-116">Subscription Id parameter.</span></span>

```yaml
Type: Guid
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1395-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1395-117">CommonParameters</span></span>
<span data-ttu-id="b1395-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b1395-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1395-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1395-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1395-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b1395-120">INPUTS</span></span>

## <span data-ttu-id="b1395-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b1395-121">OUTPUTS</span></span>

### <span data-ttu-id="b1395-122">Microsoft. AzureStack. Management. Subscriptions. admin. modele. Subscription</span><span class="sxs-lookup"><span data-stu-id="b1395-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="b1395-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b1395-123">NOTES</span></span>

## <span data-ttu-id="b1395-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b1395-124">RELATED LINKS</span></span>

