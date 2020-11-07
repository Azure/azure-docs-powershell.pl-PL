---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6de990526330cdd192cd99707aacc1e06ad49c5d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710725"
---
# <span data-ttu-id="c0686-101">Stop-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="c0686-101">Stop-AzsScaleUnitNode</span></span>

## <span data-ttu-id="c0686-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0686-102">SYNOPSIS</span></span>
<span data-ttu-id="c0686-103">Wyłącz zasilanie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="c0686-103">Power off a scale unit node.</span></span>

## <span data-ttu-id="c0686-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0686-104">SYNTAX</span></span>

### <span data-ttu-id="c0686-105">Zatrzymaj (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="c0686-105">Stop (Default)</span></span>
```
Stop-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-Shutdown] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0686-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="c0686-106">ResourceId</span></span>
```
Stop-AzsScaleUnitNode -ResourceId <String> [-Shutdown] [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0686-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c0686-107">DESCRIPTION</span></span>
<span data-ttu-id="c0686-108">Wyłącz zasilanie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="c0686-108">Power off a scale unit node.</span></span>

## <span data-ttu-id="c0686-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0686-109">EXAMPLES</span></span>

### <span data-ttu-id="c0686-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="c0686-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236" -Shutdown
```

<span data-ttu-id="c0686-111">Zamykanie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="c0686-111">Shutdown a scale unit node.</span></span>

### <span data-ttu-id="c0686-112">--------------------------PRZYKŁAD 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="c0686-112">-------------------------- EXAMPLE 2 --------------------------</span></span>
```
Stop-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="c0686-113">Wyłączanie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="c0686-113">Power down a scale unit node.</span></span>

## <span data-ttu-id="c0686-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0686-114">PARAMETERS</span></span>

### <span data-ttu-id="c0686-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0686-115">-AsJob</span></span>
<span data-ttu-id="c0686-116">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="c0686-116">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c0686-117">-Force</span><span class="sxs-lookup"><span data-stu-id="c0686-117">-Force</span></span>
<span data-ttu-id="c0686-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c0686-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c0686-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c0686-119">-Location</span></span>
<span data-ttu-id="c0686-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="c0686-120">Location of the resource.</span></span>

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

### <span data-ttu-id="c0686-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c0686-121">-Name</span></span>
<span data-ttu-id="c0686-122">Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="c0686-122">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="c0686-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0686-123">-ResourceGroupName</span></span>
<span data-ttu-id="c0686-124">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="c0686-124">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c0686-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0686-125">-ResourceId</span></span>
<span data-ttu-id="c0686-126">Identyfikator zasobu węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="c0686-126">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="c0686-127">-Shutdown</span><span class="sxs-lookup"><span data-stu-id="c0686-127">-Shutdown</span></span>
<span data-ttu-id="c0686-128">Jeśli ustawisz łagodnie zamknięcie węzła jednostki skali, wyłączenie w inny sposób wyłączenia węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="c0686-128">If set gracefully shutdown the scale unit node; otherwise hard power off the scale unit node.</span></span>

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

### <span data-ttu-id="c0686-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0686-129">-Confirm</span></span>
<span data-ttu-id="c0686-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0686-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0686-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0686-131">-WhatIf</span></span>
<span data-ttu-id="c0686-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0686-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0686-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c0686-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0686-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0686-134">CommonParameters</span></span>
<span data-ttu-id="c0686-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0686-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0686-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0686-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0686-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0686-137">INPUTS</span></span>

## <span data-ttu-id="c0686-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0686-138">OUTPUTS</span></span>

## <span data-ttu-id="c0686-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0686-139">NOTES</span></span>

## <span data-ttu-id="c0686-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0686-140">RELATED LINKS</span></span>

