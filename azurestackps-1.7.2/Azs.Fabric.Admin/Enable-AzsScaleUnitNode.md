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
ms.locfileid: "93888693"
---
# <span data-ttu-id="98faf-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="98faf-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="98faf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98faf-102">SYNOPSIS</span></span>
<span data-ttu-id="98faf-103">Zatrzymaj tryb konserwacji węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="98faf-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="98faf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98faf-104">SYNTAX</span></span>

### <span data-ttu-id="98faf-105">Włącz (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="98faf-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98faf-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="98faf-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98faf-107">Opis</span><span class="sxs-lookup"><span data-stu-id="98faf-107">DESCRIPTION</span></span>
<span data-ttu-id="98faf-108">Zatrzymaj tryb konserwacji węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="98faf-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="98faf-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98faf-109">EXAMPLES</span></span>

### <span data-ttu-id="98faf-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="98faf-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="98faf-111">Zatrzymaj tryb konserwacji węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="98faf-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="98faf-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98faf-112">PARAMETERS</span></span>

### <span data-ttu-id="98faf-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98faf-113">-AsJob</span></span>
<span data-ttu-id="98faf-114">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="98faf-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="98faf-115">-Force</span><span class="sxs-lookup"><span data-stu-id="98faf-115">-Force</span></span>
<span data-ttu-id="98faf-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="98faf-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="98faf-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="98faf-117">-Location</span></span>
<span data-ttu-id="98faf-118">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="98faf-118">Location of the resource.</span></span>

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

### <span data-ttu-id="98faf-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98faf-119">-Name</span></span>
<span data-ttu-id="98faf-120">Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="98faf-120">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="98faf-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98faf-121">-ResourceGroupName</span></span>
<span data-ttu-id="98faf-122">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="98faf-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="98faf-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98faf-123">-ResourceId</span></span>
<span data-ttu-id="98faf-124">Identyfikator zasobu węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="98faf-124">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="98faf-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98faf-125">-Confirm</span></span>
<span data-ttu-id="98faf-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98faf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98faf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98faf-127">-WhatIf</span></span>
<span data-ttu-id="98faf-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98faf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98faf-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="98faf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98faf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98faf-130">CommonParameters</span></span>
<span data-ttu-id="98faf-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98faf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98faf-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98faf-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98faf-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98faf-133">INPUTS</span></span>

## <span data-ttu-id="98faf-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98faf-134">OUTPUTS</span></span>

## <span data-ttu-id="98faf-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98faf-135">NOTES</span></span>

## <span data-ttu-id="98faf-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98faf-136">RELATED LINKS</span></span>

