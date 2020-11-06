---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9c5de84b66283d683d121c99c0cf2e0ea27a4a66
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523505"
---
# <span data-ttu-id="bf8af-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="bf8af-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="bf8af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf8af-102">SYNOPSIS</span></span>
<span data-ttu-id="bf8af-103">Włącz węzeł jednostka skali.</span><span class="sxs-lookup"><span data-stu-id="bf8af-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="bf8af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf8af-104">SYNTAX</span></span>

### <span data-ttu-id="bf8af-105">PowerOn (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bf8af-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bf8af-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="bf8af-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf8af-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bf8af-107">DESCRIPTION</span></span>
<span data-ttu-id="bf8af-108">Włącz węzeł jednostka skali.</span><span class="sxs-lookup"><span data-stu-id="bf8af-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="bf8af-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf8af-109">EXAMPLES</span></span>

### <span data-ttu-id="bf8af-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="bf8af-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="bf8af-111">ProvisioningState: powiodło się</span><span class="sxs-lookup"><span data-stu-id="bf8af-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="bf8af-112">Włącz węzeł jednostka skali.</span><span class="sxs-lookup"><span data-stu-id="bf8af-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="bf8af-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf8af-113">PARAMETERS</span></span>

### <span data-ttu-id="bf8af-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="bf8af-114">-AsJob</span></span>
<span data-ttu-id="bf8af-115">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="bf8af-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="bf8af-116">-Force</span><span class="sxs-lookup"><span data-stu-id="bf8af-116">-Force</span></span>
<span data-ttu-id="bf8af-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bf8af-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="bf8af-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="bf8af-118">-Location</span></span>
<span data-ttu-id="bf8af-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="bf8af-119">Location of the resource.</span></span>

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

### <span data-ttu-id="bf8af-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf8af-120">-Name</span></span>
<span data-ttu-id="bf8af-121">Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="bf8af-121">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="bf8af-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf8af-122">-ResourceGroupName</span></span>
<span data-ttu-id="bf8af-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="bf8af-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="bf8af-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bf8af-124">-ResourceId</span></span>
<span data-ttu-id="bf8af-125">Identyfikator zasobu węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="bf8af-125">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="bf8af-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bf8af-126">-Confirm</span></span>
<span data-ttu-id="bf8af-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf8af-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf8af-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf8af-128">-WhatIf</span></span>
<span data-ttu-id="bf8af-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf8af-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf8af-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bf8af-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf8af-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf8af-131">CommonParameters</span></span>
<span data-ttu-id="bf8af-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf8af-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf8af-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf8af-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf8af-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf8af-134">INPUTS</span></span>

## <span data-ttu-id="bf8af-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf8af-135">OUTPUTS</span></span>

## <span data-ttu-id="bf8af-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf8af-136">NOTES</span></span>

## <span data-ttu-id="bf8af-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf8af-137">RELATED LINKS</span></span>

