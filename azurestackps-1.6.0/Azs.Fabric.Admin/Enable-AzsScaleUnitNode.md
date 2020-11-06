---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 932d0b77fc6df9a88a2ee13ad92856727db82f06
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93522954"
---
# <span data-ttu-id="e4e20-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="e4e20-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="e4e20-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4e20-102">SYNOPSIS</span></span>
<span data-ttu-id="e4e20-103">Zatrzymaj tryb konserwacji węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="e4e20-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="e4e20-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4e20-104">SYNTAX</span></span>

### <span data-ttu-id="e4e20-105">Włącz (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e4e20-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4e20-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="e4e20-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4e20-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e4e20-107">DESCRIPTION</span></span>
<span data-ttu-id="e4e20-108">Zatrzymaj tryb konserwacji węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="e4e20-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="e4e20-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4e20-109">EXAMPLES</span></span>

### <span data-ttu-id="e4e20-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="e4e20-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="e4e20-111">Zatrzymaj tryb konserwacji węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="e4e20-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="e4e20-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4e20-112">PARAMETERS</span></span>

### <span data-ttu-id="e4e20-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e4e20-113">-AsJob</span></span>
<span data-ttu-id="e4e20-114">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="e4e20-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="e4e20-115">-Force</span><span class="sxs-lookup"><span data-stu-id="e4e20-115">-Force</span></span>
<span data-ttu-id="e4e20-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e4e20-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e4e20-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e4e20-117">-Location</span></span>
<span data-ttu-id="e4e20-118">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="e4e20-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e20-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4e20-119">-Name</span></span>
<span data-ttu-id="e4e20-120">Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="e4e20-120">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e20-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4e20-121">-ResourceGroupName</span></span>
<span data-ttu-id="e4e20-122">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="e4e20-122">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Enable
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4e20-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4e20-123">-ResourceId</span></span>
<span data-ttu-id="e4e20-124">Identyfikator zasobu węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="e4e20-124">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="e4e20-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4e20-125">-Confirm</span></span>
<span data-ttu-id="e4e20-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4e20-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4e20-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4e20-127">-WhatIf</span></span>
<span data-ttu-id="e4e20-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4e20-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4e20-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4e20-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4e20-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4e20-130">CommonParameters</span></span>
<span data-ttu-id="e4e20-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4e20-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4e20-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4e20-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4e20-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4e20-133">INPUTS</span></span>

## <span data-ttu-id="e4e20-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4e20-134">OUTPUTS</span></span>

## <span data-ttu-id="e4e20-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4e20-135">NOTES</span></span>

## <span data-ttu-id="e4e20-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4e20-136">RELATED LINKS</span></span>

