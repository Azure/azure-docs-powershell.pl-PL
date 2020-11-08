---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 498374f19f83befc5697395eb58bb191555b10ca
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055729"
---
# <span data-ttu-id="c541f-101">Repair-AzsScaleUnitNode</span><span class="sxs-lookup"><span data-stu-id="c541f-101">Repair-AzsScaleUnitNode</span></span>

## <span data-ttu-id="c541f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c541f-102">SYNOPSIS</span></span>
<span data-ttu-id="c541f-103">Naprawianie węzła klastra.</span><span class="sxs-lookup"><span data-stu-id="c541f-103">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="c541f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c541f-104">SYNTAX</span></span>

### <span data-ttu-id="c541f-105">Naprawianie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c541f-105">Repair (Default)</span></span>
```
Repair-AzsScaleUnitNode -Name <String> -BMCIPv4Address <String> [-Location <String>]
 [-ResourceGroupName <String>] [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c541f-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="c541f-106">ResourceId</span></span>
```
Repair-AzsScaleUnitNode -BMCIPv4Address <String> -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c541f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c541f-107">DESCRIPTION</span></span>
<span data-ttu-id="c541f-108">Naprawianie węzła klastra.</span><span class="sxs-lookup"><span data-stu-id="c541f-108">Repairs a node of the cluster.</span></span>

## <span data-ttu-id="c541f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c541f-109">EXAMPLES</span></span>

### <span data-ttu-id="c541f-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="c541f-110">EXAMPLE 1</span></span>
```
Repair-AzsScaleUnitNode -Name "AZS-ERCO03" -BMCIPv4Address ***.***.***.***
```

<span data-ttu-id="c541f-111">Naprawianie węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="c541f-111">Repair a scale unit node.</span></span>

## <span data-ttu-id="c541f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c541f-112">PARAMETERS</span></span>

### <span data-ttu-id="c541f-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c541f-113">-Name</span></span>
<span data-ttu-id="c541f-114">Nazwa węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="c541f-114">Name of the scale unit node.</span></span>

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

### <span data-ttu-id="c541f-115">-BMCIPv4Address</span><span class="sxs-lookup"><span data-stu-id="c541f-115">-BMCIPv4Address</span></span>
<span data-ttu-id="c541f-116">Adres BMC komputera fizycznego.</span><span class="sxs-lookup"><span data-stu-id="c541f-116">BMC address of the physical machine.</span></span>

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

### <span data-ttu-id="c541f-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c541f-117">-Location</span></span>
<span data-ttu-id="c541f-118">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="c541f-118">Location of the resource.</span></span>

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

### <span data-ttu-id="c541f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c541f-119">-ResourceGroupName</span></span>
<span data-ttu-id="c541f-120">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="c541f-120">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="c541f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c541f-121">-ResourceId</span></span>
<span data-ttu-id="c541f-122">Identyfikator zasobu węzła jednostki skali.</span><span class="sxs-lookup"><span data-stu-id="c541f-122">Scale unit node resource ID.</span></span>

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

### <span data-ttu-id="c541f-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c541f-123">-AsJob</span></span>
<span data-ttu-id="c541f-124">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="c541f-124">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="c541f-125">-Force</span><span class="sxs-lookup"><span data-stu-id="c541f-125">-Force</span></span>
<span data-ttu-id="c541f-126">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c541f-126">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="c541f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c541f-127">-WhatIf</span></span>
<span data-ttu-id="c541f-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c541f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c541f-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c541f-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c541f-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c541f-130">-Confirm</span></span>
<span data-ttu-id="c541f-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c541f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c541f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c541f-132">CommonParameters</span></span>
<span data-ttu-id="c541f-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c541f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c541f-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c541f-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c541f-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c541f-135">INPUTS</span></span>

## <span data-ttu-id="c541f-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c541f-136">OUTPUTS</span></span>

## <span data-ttu-id="c541f-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c541f-137">NOTES</span></span>

## <span data-ttu-id="c541f-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c541f-138">RELATED LINKS</span></span>
