---
external help file: Azs.InfrastructureInsights.Admin-help.xml
Module Name: Azs.Infrastructureinsights.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: a3a64a045d988d59c2b1aefa650aa695ba09486f
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889125"
---
# <span data-ttu-id="29604-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="29604-101">Get-AzsAlert</span></span>

## <span data-ttu-id="29604-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="29604-102">SYNOPSIS</span></span>
<span data-ttu-id="29604-103">Zwraca listę wszystkich alertów w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="29604-103">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="29604-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="29604-104">SYNTAX</span></span>

### <span data-ttu-id="29604-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="29604-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-Filter <String>] [-Top <Int32>]
 [-Skip <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="29604-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="29604-106">Get</span></span>
```
Get-AzsAlert [-Name] <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="29604-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="29604-107">ResourceId</span></span>
```
Get-AzsAlert -ResourceId <String> [<CommonParameters>]
```

## <span data-ttu-id="29604-108">Opis</span><span class="sxs-lookup"><span data-stu-id="29604-108">DESCRIPTION</span></span>
<span data-ttu-id="29604-109">Zwraca listę wszystkich alertów w danej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="29604-109">Returns the list of all alerts in a given location.</span></span>

## <span data-ttu-id="29604-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="29604-110">EXAMPLES</span></span>

### <span data-ttu-id="29604-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="29604-111">EXAMPLE 1</span></span>
```
Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="29604-112">Uzyskaj alert według nazwy.</span><span class="sxs-lookup"><span data-stu-id="29604-112">Get an alert by Name.</span></span>

### <span data-ttu-id="29604-113">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="29604-113">EXAMPLE 2</span></span>
```
Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="29604-114">Pobieranie wszystkich aktywnych alertów i wyświetlanie ich usterek i tytułów.</span><span class="sxs-lookup"><span data-stu-id="29604-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="29604-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="29604-115">PARAMETERS</span></span>

### <span data-ttu-id="29604-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="29604-116">-Name</span></span>
<span data-ttu-id="29604-117">Identyfikator alertu.</span><span class="sxs-lookup"><span data-stu-id="29604-117">The alert identifier.</span></span>

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

### <span data-ttu-id="29604-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="29604-118">-Location</span></span>
<span data-ttu-id="29604-119">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="29604-119">Name of the location.</span></span>

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

### <span data-ttu-id="29604-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29604-120">-ResourceGroupName</span></span>
<span data-ttu-id="29604-121">Nazwa grupy zasobów alertu.</span><span class="sxs-lookup"><span data-stu-id="29604-121">Resource group name of the alert.</span></span>

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

### <span data-ttu-id="29604-122">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="29604-122">-ResourceId</span></span>
<span data-ttu-id="29604-123">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="29604-123">The resource id.</span></span>

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

### <span data-ttu-id="29604-124">-Filter</span><span class="sxs-lookup"><span data-stu-id="29604-124">-Filter</span></span>
<span data-ttu-id="29604-125">Parametr filtru OData.</span><span class="sxs-lookup"><span data-stu-id="29604-125">OData filter parameter.</span></span>

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

### <span data-ttu-id="29604-126">-Początek</span><span class="sxs-lookup"><span data-stu-id="29604-126">-Top</span></span>
<span data-ttu-id="29604-127">Zwraca N pierwszych elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="29604-127">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="29604-128">Obowiązuje po parametrze-Skip.</span><span class="sxs-lookup"><span data-stu-id="29604-128">Applies after the -Skip parameter.</span></span>

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

### <span data-ttu-id="29604-129">-Skip</span><span class="sxs-lookup"><span data-stu-id="29604-129">-Skip</span></span>
<span data-ttu-id="29604-130">Pomijanie pierwszych N elementów określonych przez wartość parametru.</span><span class="sxs-lookup"><span data-stu-id="29604-130">Skip the first N items as specified by the parameter value.</span></span>

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

### <span data-ttu-id="29604-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29604-131">CommonParameters</span></span>
<span data-ttu-id="29604-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29604-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29604-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29604-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29604-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="29604-134">INPUTS</span></span>

## <span data-ttu-id="29604-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="29604-135">OUTPUTS</span></span>

### <span data-ttu-id="29604-136">Microsoft. AzureStack. Management. InfrastructureInsights. admin. models. alert</span><span class="sxs-lookup"><span data-stu-id="29604-136">Microsoft.AzureStack.Management.InfrastructureInsights.Admin.Models.Alert</span></span>

## <span data-ttu-id="29604-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="29604-137">NOTES</span></span>

## <span data-ttu-id="29604-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="29604-138">RELATED LINKS</span></span>
