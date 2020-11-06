---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 503661f4e50ddd7575cc9c98ef4c19e2028ddf83
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523753"
---
# <span data-ttu-id="d4dc2-101">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="d4dc2-101">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="d4dc2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d4dc2-102">SYNOPSIS</span></span>
<span data-ttu-id="d4dc2-103">Pobieranie listy przydziałów dostawców zasobów abonamentu w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-103">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="d4dc2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d4dc2-104">SYNTAX</span></span>

### <span data-ttu-id="d4dc2-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="d4dc2-105">List (Default)</span></span>
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="d4dc2-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="d4dc2-106">Get</span></span>
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="d4dc2-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="d4dc2-107">ResourceId</span></span>
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="d4dc2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d4dc2-108">DESCRIPTION</span></span>
<span data-ttu-id="d4dc2-109">Pobieranie listy przydziałów w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-109">Get the list of quotas at a location.</span></span>

## <span data-ttu-id="d4dc2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d4dc2-110">EXAMPLES</span></span>

### <span data-ttu-id="d4dc2-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d4dc2-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionsQuota
```

<span data-ttu-id="d4dc2-112">Pobieranie listy przydziałów dostawców zasobów abonamentu w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-112">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="d4dc2-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d4dc2-113">PARAMETERS</span></span>

### <span data-ttu-id="d4dc2-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d4dc2-114">-Location</span></span>
<span data-ttu-id="d4dc2-115">Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-115">The AzureStack location.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: ArmLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4dc2-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d4dc2-116">-Name</span></span>
<span data-ttu-id="d4dc2-117">Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-117">Name of the quota.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d4dc2-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d4dc2-118">-ResourceId</span></span>
<span data-ttu-id="d4dc2-119">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-119">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4dc2-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4dc2-120">CommonParameters</span></span>
<span data-ttu-id="d4dc2-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d4dc2-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4dc2-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4dc2-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4dc2-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d4dc2-123">INPUTS</span></span>

## <span data-ttu-id="d4dc2-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d4dc2-124">OUTPUTS</span></span>

### <span data-ttu-id="d4dc2-125">Microsoft. AzureStack. Management. Subscriptions. admin. modele. przydział</span><span class="sxs-lookup"><span data-stu-id="d4dc2-125">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Quota</span></span>

## <span data-ttu-id="d4dc2-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d4dc2-126">NOTES</span></span>

## <span data-ttu-id="d4dc2-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d4dc2-127">RELATED LINKS</span></span>

