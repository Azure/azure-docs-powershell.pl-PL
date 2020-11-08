---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3a64a045d988d59c2b1aefa650aa695ba09486f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055882"
---
# <span data-ttu-id="41f34-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="41f34-101">Get-AzsAlert</span></span>

## <span data-ttu-id="41f34-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41f34-102">SYNOPSIS</span></span>
<span data-ttu-id="41f34-103">Zwraca listę wszystkich alertów w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="41f34-103">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="41f34-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41f34-104">SYNTAX</span></span>

### <span data-ttu-id="41f34-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="41f34-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>]
 [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="41f34-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="41f34-106">Get</span></span>
```
Get-AzsAlert [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="41f34-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="41f34-107">ResourceId</span></span>
```
Get-AzsAlert -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="41f34-108">Opis</span><span class="sxs-lookup"><span data-stu-id="41f34-108">DESCRIPTION</span></span>
<span data-ttu-id="41f34-109">Zwraca listę wszystkich alertów w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="41f34-109">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="41f34-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41f34-110">EXAMPLES</span></span>

### <span data-ttu-id="41f34-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="41f34-111">EXAMPLE 1</span></span>
```
Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="41f34-112">Uzyskaj alert według nazwy.</span><span class="sxs-lookup"><span data-stu-id="41f34-112">Get an alert by Name.</span></span>

### <span data-ttu-id="41f34-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="41f34-113">EXAMPLE 2</span></span>
```
Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="41f34-114">Pobieranie wszystkich aktywnych alertów i wyświetlanie ich usterek i tytułów.</span><span class="sxs-lookup"><span data-stu-id="41f34-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="41f34-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41f34-115">PARAMETERS</span></span>

### <span data-ttu-id="41f34-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="41f34-116">-Name</span></span>
<span data-ttu-id="41f34-117">Identyfikator alertu.</span><span class="sxs-lookup"><span data-stu-id="41f34-117">The alert identifier.</span></span>

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

### <span data-ttu-id="41f34-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="41f34-118">-Location</span></span>
<span data-ttu-id="41f34-119">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="41f34-119">Name of the location.</span></span>

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

### <span data-ttu-id="41f34-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="41f34-120">-ResourceGroupName</span></span>
<span data-ttu-id="41f34-121">Nazwa grupy zasobów alertu.</span><span class="sxs-lookup"><span data-stu-id="41f34-121">Resource group name of the alert.</span></span>

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

### <span data-ttu-id="41f34-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="41f34-122">-ResourceId</span></span>
<span data-ttu-id="41f34-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="41f34-123">The resource id.</span></span>

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

### <span data-ttu-id="41f34-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="41f34-124">-Filter</span></span>
<span data-ttu-id="41f34-125">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="41f34-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="41f34-126">-Początek</span><span class="sxs-lookup"><span data-stu-id="41f34-126">-Top</span></span>
<span data-ttu-id="41f34-127">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="41f34-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="41f34-128">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="41f34-128">Applies after the -Skip parameter.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f34-129">-Skip</span><span class="sxs-lookup"><span data-stu-id="41f34-129">-Skip</span></span>
<span data-ttu-id="41f34-130">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="41f34-130">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: Int32
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="41f34-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41f34-131">CommonParameters</span></span>
<span data-ttu-id="41f34-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41f34-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41f34-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41f34-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41f34-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41f34-134">INPUTS</span></span>

## <span data-ttu-id="41f34-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41f34-135">OUTPUTS</span></span>

### <span data-ttu-id="41f34-136">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. alert</span><span class="sxs-lookup"><span data-stu-id="41f34-136">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="41f34-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41f34-137">NOTES</span></span>

## <span data-ttu-id="41f34-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41f34-138">RELATED LINKS</span></span>
