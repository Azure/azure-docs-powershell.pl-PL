---
external help file: Azs.Subscriptions.Admin-help.xml
Module Name: Azs.Subscriptions.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3874c581d1d030f9c0b77abe82b5a5a289d8960d
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889250"
---
# <span data-ttu-id="c97f8-101">Get-AzsSubscriptionsQuota</span><span class="sxs-lookup"><span data-stu-id="c97f8-101">Get-AzsSubscriptionsQuota</span></span>

## <span data-ttu-id="c97f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c97f8-102">SYNOPSIS</span></span>
<span data-ttu-id="c97f8-103">Pobieranie listy przydziałów dostawców zasobów abonamentu w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c97f8-103">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="c97f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c97f8-104">SYNTAX</span></span>

### <span data-ttu-id="c97f8-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="c97f8-105">List (Default)</span></span>
```
Get-AzsSubscriptionsQuota [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="c97f8-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="c97f8-106">Get</span></span>
```
Get-AzsSubscriptionsQuota -Name <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="c97f8-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="c97f8-107">ResourceId</span></span>
```
Get-AzsSubscriptionsQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="c97f8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c97f8-108">DESCRIPTION</span></span>
<span data-ttu-id="c97f8-109">Pobieranie listy przydziałów w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c97f8-109">Get the list of quotas at a location.</span></span>

## <span data-ttu-id="c97f8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c97f8-110">EXAMPLES</span></span>

### <span data-ttu-id="c97f8-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c97f8-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsSubscriptionsQuota
```

<span data-ttu-id="c97f8-112">Pobieranie listy przydziałów dostawców zasobów abonamentu w lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="c97f8-112">Get the list of subscription resource provider quotas at a location.</span></span>

## <span data-ttu-id="c97f8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c97f8-113">PARAMETERS</span></span>

### <span data-ttu-id="c97f8-114">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c97f8-114">-Location</span></span>
<span data-ttu-id="c97f8-115">Lokalizacja AzureStack.</span><span class="sxs-lookup"><span data-stu-id="c97f8-115">The AzureStack location.</span></span>

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

### <span data-ttu-id="c97f8-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c97f8-116">-Name</span></span>
<span data-ttu-id="c97f8-117">Nazwa przydziału.</span><span class="sxs-lookup"><span data-stu-id="c97f8-117">Name of the quota.</span></span>

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

### <span data-ttu-id="c97f8-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c97f8-118">-ResourceId</span></span>
<span data-ttu-id="c97f8-119">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="c97f8-119">The resource id.</span></span>

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

### <span data-ttu-id="c97f8-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c97f8-120">CommonParameters</span></span>
<span data-ttu-id="c97f8-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c97f8-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c97f8-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c97f8-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c97f8-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c97f8-123">INPUTS</span></span>

## <span data-ttu-id="c97f8-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c97f8-124">OUTPUTS</span></span>

### <span data-ttu-id="c97f8-125">Microsoft. AzureStack. Management. Subscriptions. admin. modele. przydział</span><span class="sxs-lookup"><span data-stu-id="c97f8-125">Microsoft.AzureStack.Management.Subscriptions.Admin.Models.Quota</span></span>

## <span data-ttu-id="c97f8-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c97f8-126">NOTES</span></span>

## <span data-ttu-id="c97f8-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c97f8-127">RELATED LINKS</span></span>

