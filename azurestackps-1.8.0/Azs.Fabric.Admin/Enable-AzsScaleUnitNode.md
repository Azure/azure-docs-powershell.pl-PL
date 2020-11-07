---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3d77229892da63973513dd8870a949ff296f5538
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889002"
---
# <span data-ttu-id="88718-101">Enable-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="88718-101">Enable-AzsScaleUnitNode</span></span>

## <span data-ttu-id="88718-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88718-102">SYNOPSIS</span></span>
<span data-ttu-id="88718-103">Zatrzymaj tryb konserwacji węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="88718-103">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="88718-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88718-104">SYNTAX</span></span>

### <span data-ttu-id="88718-105">Włącz (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="88718-105">Enable (Default)</span></span>
```
Enable-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88718-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="88718-106">ResourceId</span></span>
```
Enable-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88718-107">Opis</span><span class="sxs-lookup"><span data-stu-id="88718-107">DESCRIPTION</span></span>
<span data-ttu-id="88718-108">Zatrzymaj tryb konserwacji węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="88718-108">Stop maintenance mode for a scale unit node.</span></span>

## <span data-ttu-id="88718-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88718-109">EXAMPLES</span></span>

### <span data-ttu-id="88718-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="88718-110">EXAMPLE 1</span></span>
```
Enable-AzsScaleUnitNode -Name "HC1n25r2236"
```

<span data-ttu-id="88718-111">Zatrzymaj tryb konserwacji węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="88718-111">Stop maintenance mode on a scale unit node.</span></span>

## <span data-ttu-id="88718-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88718-112">PARAMETERS</span></span>

### <span data-ttu-id="88718-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88718-113">-Name</span></span>
<span data-ttu-id="88718-114">Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="88718-114">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="88718-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="88718-115">-Location</span></span>
<span data-ttu-id="88718-116">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="88718-116">Location of the resource.</span></span>

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

### <span data-ttu-id="88718-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88718-117">-ResourceGroupName</span></span>
<span data-ttu-id="88718-118">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="88718-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="88718-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88718-119">-ResourceId</span></span>
<span data-ttu-id="88718-120">Identyfikator zasobu węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="88718-120">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="88718-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88718-121">-AsJob</span></span>
<span data-ttu-id="88718-122">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="88718-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="88718-123">-Force</span><span class="sxs-lookup"><span data-stu-id="88718-123">-Force</span></span>
<span data-ttu-id="88718-124">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="88718-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="88718-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88718-125">-WhatIf</span></span>
<span data-ttu-id="88718-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88718-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88718-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="88718-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88718-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88718-128">-Confirm</span></span>
<span data-ttu-id="88718-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88718-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88718-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88718-130">CommonParameters</span></span>
<span data-ttu-id="88718-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88718-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88718-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88718-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88718-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88718-133">INPUTS</span></span>

## <span data-ttu-id="88718-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88718-134">OUTPUTS</span></span>

## <span data-ttu-id="88718-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88718-135">NOTES</span></span>

## <span data-ttu-id="88718-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88718-136">RELATED LINKS</span></span>
