---
external help file: Azs.Network.Admin-help.xml
Module Name: Azs.Network.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: cb5d980efc5f4e4ad7aff13a8f91832589175039
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710758"
---
# <span data-ttu-id="89966-101">Get-AzsNetworkQuota</span><span class="sxs-lookup"><span data-stu-id="89966-101">Get-AzsNetworkQuota</span></span>

## <span data-ttu-id="89966-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="89966-102">SYNOPSIS</span></span>
<span data-ttu-id="89966-103">Lista wszystkich przydziałów.</span><span class="sxs-lookup"><span data-stu-id="89966-103">List all quotas.</span></span>

## <span data-ttu-id="89966-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="89966-104">SYNTAX</span></span>

### <span data-ttu-id="89966-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="89966-105">List (Default)</span></span>
```
Get-AzsNetworkQuota [-Location <String>] [-Filter <String>] [<CommonParameters>]
```

### <span data-ttu-id="89966-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="89966-106">Get</span></span>
```
Get-AzsNetworkQuota [-Name] <String> [-Location <String>] [<CommonParameters>]
```

### <span data-ttu-id="89966-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="89966-107">ResourceId</span></span>
```
Get-AzsNetworkQuota -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="89966-108">Opis</span><span class="sxs-lookup"><span data-stu-id="89966-108">DESCRIPTION</span></span>
<span data-ttu-id="89966-109">Lista wszystkich przydziałów.</span><span class="sxs-lookup"><span data-stu-id="89966-109">List all quotas.</span></span>
<span data-ttu-id="89966-110">Ograniczanie listy przez przekazanie nazwy lub filtru.</span><span class="sxs-lookup"><span data-stu-id="89966-110">Limit the list by passing a name or filter.</span></span>

## <span data-ttu-id="89966-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="89966-111">EXAMPLES</span></span>

### <span data-ttu-id="89966-112">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="89966-112">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsNetworkQuota
```

<span data-ttu-id="89966-113">Wyświetla listę wszystkich przydziałów sieci.</span><span class="sxs-lookup"><span data-stu-id="89966-113">Lists all the  network quotas.</span></span>

### <span data-ttu-id="89966-114">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="89966-114">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Get-AzsNetworkQuota -Name NetworkQuota1
```

<span data-ttu-id="89966-115">Pobiera określony przydział sieci.</span><span class="sxs-lookup"><span data-stu-id="89966-115">Gets the specified network quota.</span></span>

## <span data-ttu-id="89966-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="89966-116">PARAMETERS</span></span>

### <span data-ttu-id="89966-117">-Filter</span><span class="sxs-lookup"><span data-stu-id="89966-117">-Filter</span></span>
<span data-ttu-id="89966-118">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="89966-118">OData filter parameter.</span></span>

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

### <span data-ttu-id="89966-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="89966-119">-Location</span></span>
<span data-ttu-id="89966-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="89966-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: List, Get
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89966-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="89966-121">-Name</span></span>
<span data-ttu-id="89966-122">Nazwa zasobu przydziału sieci.</span><span class="sxs-lookup"><span data-stu-id="89966-122">Network quota resource name.</span></span>

```yaml
Type: String
Parameter Sets: Get
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="89966-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="89966-123">-ResourceId</span></span>
<span data-ttu-id="89966-124">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="89966-124">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89966-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89966-125">CommonParameters</span></span>
<span data-ttu-id="89966-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="89966-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89966-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89966-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89966-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="89966-128">INPUTS</span></span>

## <span data-ttu-id="89966-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="89966-129">OUTPUTS</span></span>

### <span data-ttu-id="89966-130">Microsoft. AzureStack. Management. Network. admin. modele. przydział</span><span class="sxs-lookup"><span data-stu-id="89966-130">Microsoft.AzureStack.Management.Network.Admin.Models.Quota</span></span>

## <span data-ttu-id="89966-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="89966-131">NOTES</span></span>

## <span data-ttu-id="89966-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="89966-132">RELATED LINKS</span></span>
