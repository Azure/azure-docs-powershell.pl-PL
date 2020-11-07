---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c51249856d9cd8c8fc47d4968b1bc011040610e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93888906"
---
# <span data-ttu-id="98807-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="98807-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="98807-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98807-102">SYNOPSIS</span></span>
<span data-ttu-id="98807-103">Włącz węzeł jednostka skali.</span><span class="sxs-lookup"><span data-stu-id="98807-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="98807-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98807-104">SYNTAX</span></span>

### <span data-ttu-id="98807-105">PowerOn (domyślny)</span><span class="sxs-lookup"><span data-stu-id="98807-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98807-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="98807-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98807-107">Opis</span><span class="sxs-lookup"><span data-stu-id="98807-107">DESCRIPTION</span></span>
<span data-ttu-id="98807-108">Włącz węzeł jednostka skali.</span><span class="sxs-lookup"><span data-stu-id="98807-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="98807-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98807-109">EXAMPLES</span></span>

### <span data-ttu-id="98807-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="98807-110">EXAMPLE 1</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="98807-111">ProvisioningState: powiodło się</span><span class="sxs-lookup"><span data-stu-id="98807-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="98807-112">Włącz węzeł jednostka skali.</span><span class="sxs-lookup"><span data-stu-id="98807-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="98807-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98807-113">PARAMETERS</span></span>

### <span data-ttu-id="98807-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="98807-114">-Name</span></span>
<span data-ttu-id="98807-115">Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="98807-115">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98807-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="98807-116">-Location</span></span>
<span data-ttu-id="98807-117">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="98807-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98807-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98807-118">-ResourceGroupName</span></span>
<span data-ttu-id="98807-119">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="98807-119">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOn
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98807-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="98807-120">-ResourceId</span></span>
<span data-ttu-id="98807-121">Identyfikator zasobu węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="98807-121">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="98807-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="98807-122">-AsJob</span></span>
<span data-ttu-id="98807-123">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="98807-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="98807-124">-Force</span><span class="sxs-lookup"><span data-stu-id="98807-124">-Force</span></span>
<span data-ttu-id="98807-125">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="98807-125">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="98807-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98807-126">-WhatIf</span></span>
<span data-ttu-id="98807-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98807-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="98807-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="98807-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98807-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98807-129">-Confirm</span></span>
<span data-ttu-id="98807-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98807-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98807-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98807-131">CommonParameters</span></span>
<span data-ttu-id="98807-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98807-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98807-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98807-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98807-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98807-134">INPUTS</span></span>

## <span data-ttu-id="98807-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98807-135">OUTPUTS</span></span>

## <span data-ttu-id="98807-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98807-136">NOTES</span></span>

## <span data-ttu-id="98807-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98807-137">RELATED LINKS</span></span>
