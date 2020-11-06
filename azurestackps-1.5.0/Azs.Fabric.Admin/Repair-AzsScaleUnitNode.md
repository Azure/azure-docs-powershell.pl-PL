---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 3ad784757210273cd2e456069c8d3a759e973a0f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523129"
---
# <span data-ttu-id="2e543-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="2e543-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="2e543-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e543-102">SYNOPSIS</span></span>
<span data-ttu-id="2e543-103">Naprawianie węzła klastra.</span><span class="sxs-lookup"><span data-stu-id="2e543-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="2e543-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e543-104">SYNTAX</span></span>

### <span data-ttu-id="2e543-105">Naprawianie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="2e543-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2e543-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="2e543-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2e543-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2e543-107">DESCRIPTION</span></span>
<span data-ttu-id="2e543-108">Naprawianie węzła klastra.</span><span class="sxs-lookup"><span data-stu-id="2e543-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="2e543-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e543-109">EXAMPLES</span></span>

### <span data-ttu-id="2e543-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="2e543-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="2e543-111">Naprawianie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="2e543-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="2e543-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e543-112">PARAMETERS</span></span>

### <span data-ttu-id="2e543-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2e543-113">-AsJob</span></span>
<span data-ttu-id="2e543-114">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="2e543-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="2e543-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="2e543-115">-BMCIPv4Address</span></span>
<span data-ttu-id="2e543-116">Adres BMC komputera fizycznego.</span><span class="sxs-lookup"><span data-stu-id="2e543-116">BMC address of the physical machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e543-117">-Force</span><span class="sxs-lookup"><span data-stu-id="2e543-117">-Force</span></span>
<span data-ttu-id="2e543-118">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2e543-118">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="2e543-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2e543-119">-Location</span></span>
<span data-ttu-id="2e543-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="2e543-120">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e543-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2e543-121">-Name</span></span>
<span data-ttu-id="2e543-122">Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="2e543-122">Name of the scale unit node.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e543-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e543-123">-ResourceGroupName</span></span>
<span data-ttu-id="2e543-124">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="2e543-124">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Repair
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2e543-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e543-125">-ResourceId</span></span>
<span data-ttu-id="2e543-126">Identyfikator zasobu węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="2e543-126">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="2e543-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2e543-127">-Confirm</span></span>
<span data-ttu-id="2e543-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e543-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2e543-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2e543-129">-WhatIf</span></span>
<span data-ttu-id="2e543-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2e543-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2e543-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2e543-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2e543-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e543-132">CommonParameters</span></span>
<span data-ttu-id="2e543-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e543-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e543-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2e543-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e543-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e543-135">INPUTS</span></span>

## <span data-ttu-id="2e543-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e543-136">OUTPUTS</span></span>

## <span data-ttu-id="2e543-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e543-137">NOTES</span></span>

## <span data-ttu-id="2e543-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e543-138">RELATED LINKS</span></span>

