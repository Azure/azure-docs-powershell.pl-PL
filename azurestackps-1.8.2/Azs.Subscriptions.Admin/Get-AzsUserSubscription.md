---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055951"
---
# <span data-ttu-id="ccb45-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="ccb45-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="ccb45-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ccb45-102">SYNOPSIS</span></span>
<span data-ttu-id="ccb45-103">Pobierz listę abonamentów użytkowników jako administrator.</span><span class="sxs-lookup"><span data-stu-id="ccb45-103">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="ccb45-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ccb45-104">SYNTAX</span></span>

### <span data-ttu-id="ccb45-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="ccb45-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="ccb45-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="ccb45-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="ccb45-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ccb45-107">DESCRIPTION</span></span>
<span data-ttu-id="ccb45-108">Pobierz listę abonamentów użytkowników jako administrator.</span><span class="sxs-lookup"><span data-stu-id="ccb45-108">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="ccb45-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ccb45-109">EXAMPLES</span></span>

### <span data-ttu-id="ccb45-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ccb45-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="ccb45-111">Pobierz listę abonamentów użytkowników jako administrator.</span><span class="sxs-lookup"><span data-stu-id="ccb45-111">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="ccb45-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ccb45-112">PARAMETERS</span></span>

### <span data-ttu-id="ccb45-113">-Filter</span><span class="sxs-lookup"><span data-stu-id="ccb45-113">-Filter</span></span>
<span data-ttu-id="ccb45-114">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="ccb45-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="ccb45-115">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ccb45-115">-SubscriptionId</span></span>
<span data-ttu-id="ccb45-116">Parametr identyfikatora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ccb45-116">Subscription Id parameter.</span></span>

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

### <span data-ttu-id="ccb45-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ccb45-117">CommonParameters</span></span>
<span data-ttu-id="ccb45-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ccb45-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ccb45-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ccb45-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ccb45-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ccb45-120">INPUTS</span></span>

## <span data-ttu-id="ccb45-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ccb45-121">OUTPUTS</span></span>

### <span data-ttu-id="ccb45-122">Microsoft. AzureStack. Management. Subscriptions. admin. modele. Subscription</span><span class="sxs-lookup"><span data-stu-id="ccb45-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="ccb45-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ccb45-123">NOTES</span></span>

## <span data-ttu-id="ccb45-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ccb45-124">RELATED LINKS</span></span>

