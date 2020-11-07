---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4c51249856d9cd8c8fc47d4968b1bc011040610e
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93890058"
---
# <span data-ttu-id="25d43-101">Start-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="25d43-101">Start-AzsScaleUnitNode</span></span>

## <span data-ttu-id="25d43-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25d43-102">SYNOPSIS</span></span>
<span data-ttu-id="25d43-103">Włącz węzeł jednostka skali.</span><span class="sxs-lookup"><span data-stu-id="25d43-103">Power on a scale unit node.</span></span>

## <span data-ttu-id="25d43-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25d43-104">SYNTAX</span></span>

### <span data-ttu-id="25d43-105">PowerOn (domyślny)</span><span class="sxs-lookup"><span data-stu-id="25d43-105">PowerOn (Default)</span></span>
```
Start-AzsScaleUnitNode -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="25d43-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="25d43-106">ResourceId</span></span>
```
Start-AzsScaleUnitNode -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25d43-107">Opis</span><span class="sxs-lookup"><span data-stu-id="25d43-107">DESCRIPTION</span></span>
<span data-ttu-id="25d43-108">Włącz węzeł jednostka skali.</span><span class="sxs-lookup"><span data-stu-id="25d43-108">Power on a scale unit node.</span></span>

## <span data-ttu-id="25d43-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25d43-109">EXAMPLES</span></span>

### <span data-ttu-id="25d43-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="25d43-110">EXAMPLE 1</span></span>
```
Start-AzsScaleUnitNode -Name "AzS-ACS01"
```

<span data-ttu-id="25d43-111">ProvisioningState: powiodło się</span><span class="sxs-lookup"><span data-stu-id="25d43-111">ProvisioningState : Succeeded</span></span>

<span data-ttu-id="25d43-112">Włącz węzeł jednostka skali.</span><span class="sxs-lookup"><span data-stu-id="25d43-112">Power on a scale unit node.</span></span>

## <span data-ttu-id="25d43-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25d43-113">PARAMETERS</span></span>

### <span data-ttu-id="25d43-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="25d43-114">-Name</span></span>
<span data-ttu-id="25d43-115">Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="25d43-115">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="25d43-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="25d43-116">-Location</span></span>
<span data-ttu-id="25d43-117">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="25d43-117">Location of the resource.</span></span>

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

### <span data-ttu-id="25d43-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25d43-118">-ResourceGroupName</span></span>
<span data-ttu-id="25d43-119">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="25d43-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="25d43-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="25d43-120">-ResourceId</span></span>
<span data-ttu-id="25d43-121">Identyfikator zasobu węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="25d43-121">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="25d43-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="25d43-122">-AsJob</span></span>
<span data-ttu-id="25d43-123">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="25d43-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="25d43-124">-Force</span><span class="sxs-lookup"><span data-stu-id="25d43-124">-Force</span></span>
<span data-ttu-id="25d43-125">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="25d43-125">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="25d43-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25d43-126">-WhatIf</span></span>
<span data-ttu-id="25d43-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25d43-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25d43-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="25d43-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25d43-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25d43-129">-Confirm</span></span>
<span data-ttu-id="25d43-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25d43-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25d43-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25d43-131">CommonParameters</span></span>
<span data-ttu-id="25d43-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25d43-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25d43-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="25d43-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25d43-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25d43-134">INPUTS</span></span>

## <span data-ttu-id="25d43-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25d43-135">OUTPUTS</span></span>

## <span data-ttu-id="25d43-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25d43-136">NOTES</span></span>

## <span data-ttu-id="25d43-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25d43-137">RELATED LINKS</span></span>
