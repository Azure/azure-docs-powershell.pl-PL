---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: f1a26c22b5714fc7db448935b31b0af685301217
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93890053"
---
# <span data-ttu-id="1bc90-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="1bc90-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="1bc90-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1bc90-102">SYNOPSIS</span></span>
<span data-ttu-id="1bc90-103">Wyłącz zasilanie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="1bc90-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="1bc90-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1bc90-104">SYNTAX</span></span>

### <span data-ttu-id="1bc90-105">Zatrzymaj (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="1bc90-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1bc90-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="1bc90-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1bc90-107">Opis</span><span class="sxs-lookup"><span data-stu-id="1bc90-107">DESCRIPTION</span></span>
<span data-ttu-id="1bc90-108">Wyłącz zasilanie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="1bc90-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="1bc90-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1bc90-109">EXAMPLES</span></span>

### <span data-ttu-id="1bc90-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="1bc90-110">EXAMPLE 1</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="1bc90-111">Zamykanie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="1bc90-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="1bc90-112">PRZYKŁAD 2</span><span class="sxs-lookup"><span data-stu-id="1bc90-112">EXAMPLE 2</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="1bc90-113">Wyłączanie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="1bc90-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="1bc90-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1bc90-114">PARAMETERS</span></span>

### <span data-ttu-id="1bc90-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1bc90-115">-Name</span></span>
<span data-ttu-id="1bc90-116">Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="1bc90-116">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="1bc90-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1bc90-117">-Location</span></span>
<span data-ttu-id="1bc90-118">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="1bc90-118">Location of the resource.</span></span>

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

### <span data-ttu-id="1bc90-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1bc90-119">-ResourceGroupName</span></span>
<span data-ttu-id="1bc90-120">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="1bc90-120">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="1bc90-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1bc90-121">-ResourceId</span></span>
<span data-ttu-id="1bc90-122">Identyfikator zasobu węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="1bc90-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="1bc90-123">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="1bc90-123">-Shutdown</span></span>
<span data-ttu-id="1bc90-124">Jeśli ustawisz łagodnie zamknięcie węzła jednostki skali, wyłączenie w inny sposób wyłączenia węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="1bc90-124">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="1bc90-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1bc90-125">-AsJob</span></span>
<span data-ttu-id="1bc90-126">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="1bc90-126">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="1bc90-127">-Force</span><span class="sxs-lookup"><span data-stu-id="1bc90-127">-Force</span></span>
<span data-ttu-id="1bc90-128">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1bc90-128">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="1bc90-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1bc90-129">-WhatIf</span></span>
<span data-ttu-id="1bc90-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bc90-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1bc90-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1bc90-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1bc90-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1bc90-132">-Confirm</span></span>
<span data-ttu-id="1bc90-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1bc90-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1bc90-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1bc90-134">CommonParameters</span></span>
<span data-ttu-id="1bc90-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1bc90-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1bc90-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1bc90-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1bc90-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1bc90-137">INPUTS</span></span>

## <span data-ttu-id="1bc90-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1bc90-138">OUTPUTS</span></span>

## <span data-ttu-id="1bc90-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1bc90-139">NOTES</span></span>

## <span data-ttu-id="1bc90-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1bc90-140">RELATED LINKS</span></span>
