---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: ced1207f07360c0a18674d6f8ae4170be9b87beb
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93889014"
---
# <span data-ttu-id="52ce6-101">Add-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="52ce6-101">Add-AzsScaleUnitNode</span></span>

## <span data-ttu-id="52ce6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="52ce6-102">SYNOPSIS</span></span>
<span data-ttu-id="52ce6-103">Dodaj nową jednostkę skali.</span><span class="sxs-lookup"><span data-stu-id="52ce6-103">Add a new scale unit.</span></span>

## <span data-ttu-id="52ce6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="52ce6-104">SYNTAX</span></span>

### <span data-ttu-id="52ce6-105">ScaleOut (domyślny)</span><span class="sxs-lookup"><span data-stu-id="52ce6-105">ScaleOut (Default)</span></span>
```
Add-AzsScaleUnitNode -Name <String> -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence]
 [-Location <String>] [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52ce6-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="52ce6-106">ResourceId</span></span>
```
Add-AzsScaleUnitNode -NodeList <ScaleOutScaleUnitParameters[]> [-AwaitStorageConvergence] -ResourceId <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52ce6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="52ce6-107">DESCRIPTION</span></span>
<span data-ttu-id="52ce6-108">Dodaj nową jednostkę skali.</span><span class="sxs-lookup"><span data-stu-id="52ce6-108">Add a new scale unit.</span></span>

## <span data-ttu-id="52ce6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="52ce6-109">EXAMPLES</span></span>

### <span data-ttu-id="52ce6-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="52ce6-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Add-AzsScaleUnitNode -ScaleUnitName "Azs-ERC03" -NodeList $nodeList
```

<span data-ttu-id="52ce6-111">Dodaj nowy węzeł jednostka skali.</span><span class="sxs-lookup"><span data-stu-id="52ce6-111">Add a new scale unit node.</span></span>

## <span data-ttu-id="52ce6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="52ce6-112">PARAMETERS</span></span>

### <span data-ttu-id="52ce6-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52ce6-113">-AsJob</span></span>
<span data-ttu-id="52ce6-114">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="52ce6-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="52ce6-115">-AwaitStorageConvergence</span><span class="sxs-lookup"><span data-stu-id="52ce6-115">-AwaitStorageConvergence</span></span>
<span data-ttu-id="52ce6-116">Flaga wskazuje, czy operacja powinna czekać na odłączenie miejsca do magazynowania przed powrotem.</span><span class="sxs-lookup"><span data-stu-id="52ce6-116">Flag indicates if the operation should wait for storage to converge before returning.</span></span>

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

### <span data-ttu-id="52ce6-117">-Force</span><span class="sxs-lookup"><span data-stu-id="52ce6-117">-Force</span></span>
<span data-ttu-id="52ce6-118">Nie pytaj o potwierdzenie</span><span class="sxs-lookup"><span data-stu-id="52ce6-118">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="52ce6-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="52ce6-119">-Location</span></span>
<span data-ttu-id="52ce6-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="52ce6-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ce6-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="52ce6-121">-Name</span></span>
<span data-ttu-id="52ce6-122">{{Opis nazwy}}</span><span class="sxs-lookup"><span data-stu-id="52ce6-122">{{Fill Name Description}}</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ce6-123">-NodeList</span><span class="sxs-lookup"><span data-stu-id="52ce6-123">-NodeList</span></span>
<span data-ttu-id="52ce6-124">Lista węzłów w jednostkach skali.</span><span class="sxs-lookup"><span data-stu-id="52ce6-124">List of nodes in the scale unit.</span></span>

```yaml
Type: ScaleOutScaleUnitParameters[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ce6-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52ce6-125">-ResourceGroupName</span></span>
<span data-ttu-id="52ce6-126">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="52ce6-126">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: ScaleOut
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52ce6-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="52ce6-127">-ResourceId</span></span>
<span data-ttu-id="52ce6-128">Identyfikator zasobu węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="52ce6-128">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="52ce6-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="52ce6-129">-Confirm</span></span>
<span data-ttu-id="52ce6-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52ce6-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52ce6-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52ce6-131">-WhatIf</span></span>
<span data-ttu-id="52ce6-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52ce6-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52ce6-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="52ce6-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52ce6-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52ce6-134">CommonParameters</span></span>
<span data-ttu-id="52ce6-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52ce6-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52ce6-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52ce6-136">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52ce6-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52ce6-137">INPUTS</span></span>

## <span data-ttu-id="52ce6-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="52ce6-138">OUTPUTS</span></span>

## <span data-ttu-id="52ce6-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="52ce6-139">NOTES</span></span>

## <span data-ttu-id="52ce6-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52ce6-140">RELATED LINKS</span></span>

