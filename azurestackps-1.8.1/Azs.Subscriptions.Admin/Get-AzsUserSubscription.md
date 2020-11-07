---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4403232b45b2a1e69d6148a118e69ccaf80e4a1e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889550"
---
# <span data-ttu-id="c07ce-101">Get-AzsUserSubscription</span><span class="sxs-lookup"><span data-stu-id="c07ce-101">Get-AzsUserSubscription</span></span>

## <span data-ttu-id="c07ce-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c07ce-102">SYNOPSIS</span></span>
<span data-ttu-id="c07ce-103">Pobierz listę abonamentów użytkowników jako administrator.</span><span class="sxs-lookup"><span data-stu-id="c07ce-103">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="c07ce-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c07ce-104">SYNTAX</span></span>

### <span data-ttu-id="c07ce-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c07ce-105">List (Default)</span></span>
```
Get-AzsUserSubscription [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="c07ce-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="c07ce-106">Get</span></span>
```
Get-AzsUserSubscription -SubscriptionId <Guid> [<CommonParameters>]
```

## <span data-ttu-id="c07ce-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c07ce-107">DESCRIPTION</span></span>
<span data-ttu-id="c07ce-108">Pobierz listę abonamentów użytkowników jako administrator.</span><span class="sxs-lookup"><span data-stu-id="c07ce-108">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="c07ce-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c07ce-109">EXAMPLES</span></span>

### <span data-ttu-id="c07ce-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c07ce-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUserSubscription
```

<span data-ttu-id="c07ce-111">Pobierz listę abonamentów użytkowników jako administrator.</span><span class="sxs-lookup"><span data-stu-id="c07ce-111">Get the list of user subscriptions as administrator.</span></span>

## <span data-ttu-id="c07ce-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c07ce-112">PARAMETERS</span></span>

### <span data-ttu-id="c07ce-113">-Filter</span><span class="sxs-lookup"><span data-stu-id="c07ce-113">-Filter</span></span>
<span data-ttu-id="c07ce-114">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="c07ce-114">OData filter parameter.</span></span>

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

### <span data-ttu-id="c07ce-115">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c07ce-115">-SubscriptionId</span></span>
<span data-ttu-id="c07ce-116">Parametr identyfikatora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c07ce-116">Subscription Id parameter.</span></span>

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

### <span data-ttu-id="c07ce-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c07ce-117">CommonParameters</span></span>
<span data-ttu-id="c07ce-118">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c07ce-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c07ce-119">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c07ce-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c07ce-120">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c07ce-120">INPUTS</span></span>

## <span data-ttu-id="c07ce-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c07ce-121">OUTPUTS</span></span>

### <span data-ttu-id="c07ce-122">Microsoft. AzureStack. Management. Subscriptions. admin. modele. Subscription</span><span class="sxs-lookup"><span data-stu-id="c07ce-122">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Subscription</span></span>

## <span data-ttu-id="c07ce-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c07ce-123">NOTES</span></span>

## <span data-ttu-id="c07ce-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c07ce-124">RELATED LINKS</span></span>

