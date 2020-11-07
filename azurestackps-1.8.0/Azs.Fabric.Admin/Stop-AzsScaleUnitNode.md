---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1a26c22b5714fc7db448935b31b0af685301217
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889138"
---
# <span data-ttu-id="76b50-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="76b50-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="76b50-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76b50-102">SYNOPSIS</span></span>
<span data-ttu-id="76b50-103">Wyłącz zasilanie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="76b50-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="76b50-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76b50-104">SYNTAX</span></span>

### <span data-ttu-id="76b50-105">Zatrzymaj (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="76b50-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76b50-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="76b50-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76b50-107">Opis</span><span class="sxs-lookup"><span data-stu-id="76b50-107">DESCRIPTION</span></span>
<span data-ttu-id="76b50-108">Wyłącz zasilanie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="76b50-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="76b50-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76b50-109">EXAMPLES</span></span>

### <span data-ttu-id="76b50-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="76b50-110">EXAMPLE 1</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="76b50-111">Zamykanie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="76b50-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="76b50-112">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="76b50-112">EXAMPLE 2</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="76b50-113">Wyłączanie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="76b50-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="76b50-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76b50-114">PARAMETERS</span></span>

### <span data-ttu-id="76b50-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="76b50-115">-Name</span></span>
<span data-ttu-id="76b50-116">Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="76b50-116">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b50-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="76b50-117">-Location</span></span>
<span data-ttu-id="76b50-118">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="76b50-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b50-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76b50-119">-ResourceGroupName</span></span>
<span data-ttu-id="76b50-120">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="76b50-120">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Stop
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="76b50-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76b50-121">-ResourceId</span></span>
<span data-ttu-id="76b50-122">Identyfikator zasobu węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="76b50-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="76b50-123">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="76b50-123">-Shutdown</span></span>
<span data-ttu-id="76b50-124">Jeśli ustawisz łagodnie zamknięcie węzła jednostki skali, wyłączenie w inny sposób wyłączenia węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="76b50-124">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="76b50-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="76b50-125">-AsJob</span></span>
<span data-ttu-id="76b50-126">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="76b50-126">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="76b50-127">-Force</span><span class="sxs-lookup"><span data-stu-id="76b50-127">-Force</span></span>
<span data-ttu-id="76b50-128">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="76b50-128">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="76b50-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76b50-129">-WhatIf</span></span>
<span data-ttu-id="76b50-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76b50-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76b50-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="76b50-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76b50-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76b50-132">-Confirm</span></span>
<span data-ttu-id="76b50-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76b50-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76b50-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76b50-134">CommonParameters</span></span>
<span data-ttu-id="76b50-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76b50-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76b50-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76b50-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76b50-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76b50-137">INPUTS</span></span>

## <span data-ttu-id="76b50-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76b50-138">OUTPUTS</span></span>

## <span data-ttu-id="76b50-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76b50-139">NOTES</span></span>

## <span data-ttu-id="76b50-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76b50-140">RELATED LINKS</span></span>
