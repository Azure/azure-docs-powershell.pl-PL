---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: c60245b9e6b8d44d8c465427c41c69e5cd442bb0
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889681"
---
# <span data-ttu-id="891c2-101">Disable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="891c2-101">Disable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="891c2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="891c2-102">SYNOPSIS</span></span>
<span data-ttu-id="891c2-103">Uruchom tryb konserwacji dla węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="891c2-103">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="891c2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="891c2-104">SYNTAX</span></span>

### <span data-ttu-id="891c2-105">Wyłącz (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="891c2-105">Disable (Default)</span></span>
```
Disable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="891c2-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="891c2-106">ResourceId</span></span>
```
Disable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="891c2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="891c2-107">DESCRIPTION</span></span>
<span data-ttu-id="891c2-108">Uruchom tryb konserwacji dla węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="891c2-108">Start maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="891c2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="891c2-109">EXAMPLES</span></span>

### <span data-ttu-id="891c2-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="891c2-110">EXAMPLE 1</span></span>
```
Disable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="891c2-111">Włącz tryb konserwacji dla węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="891c2-111">Enable maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="891c2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="891c2-112">PARAMETERS</span></span>

### <span data-ttu-id="891c2-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="891c2-113">-Name</span></span>
<span data-ttu-id="891c2-114">Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="891c2-114">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891c2-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="891c2-115">-Location</span></span>
<span data-ttu-id="891c2-116">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="891c2-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891c2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="891c2-117">-ResourceGroupName</span></span>
<span data-ttu-id="891c2-118">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="891c2-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Disable
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891c2-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="891c2-119">-ResourceId</span></span>
<span data-ttu-id="891c2-120">Identyfikator zasobu węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="891c2-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="891c2-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="891c2-121">-AsJob</span></span>
<span data-ttu-id="891c2-122">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="891c2-122">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891c2-123">-Force</span><span class="sxs-lookup"><span data-stu-id="891c2-123">-Force</span></span>
<span data-ttu-id="891c2-124">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="891c2-124">Don't ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891c2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="891c2-125">-WhatIf</span></span>
<span data-ttu-id="891c2-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="891c2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="891c2-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="891c2-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891c2-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="891c2-128">-Confirm</span></span>
<span data-ttu-id="891c2-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="891c2-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="891c2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="891c2-130">CommonParameters</span></span>
<span data-ttu-id="891c2-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="891c2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="891c2-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="891c2-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="891c2-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="891c2-133">INPUTS</span></span>

## <span data-ttu-id="891c2-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="891c2-134">OUTPUTS</span></span>

## <span data-ttu-id="891c2-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="891c2-135">NOTES</span></span>

## <span data-ttu-id="891c2-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="891c2-136">RELATED LINKS</span></span>
