---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: da781ee77cb94e7bc442b72ad0655041cf23b546
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523153"
---
# <span data-ttu-id="f1dae-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="f1dae-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="f1dae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f1dae-102">SYNOPSIS</span></span>
<span data-ttu-id="f1dae-103">Ponowne uruchomienie żądanej roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="f1dae-103">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="f1dae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f1dae-104">SYNTAX</span></span>

### <span data-ttu-id="f1dae-105">Uruchom ponownie (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f1dae-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f1dae-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="f1dae-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1dae-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f1dae-107">DESCRIPTION</span></span>
<span data-ttu-id="f1dae-108">Ponowne uruchomienie żądanej roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="f1dae-108">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="f1dae-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f1dae-109">EXAMPLES</span></span>

### <span data-ttu-id="f1dae-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="f1dae-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restart-AzsInfrastructureRole -Name "Compute Controller"
```

<span data-ttu-id="f1dae-111">Uruchom ponownie rolę infrastruktury, która uległa awarii.</span><span class="sxs-lookup"><span data-stu-id="f1dae-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="f1dae-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f1dae-112">PARAMETERS</span></span>

### <span data-ttu-id="f1dae-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f1dae-113">-AsJob</span></span>
<span data-ttu-id="f1dae-114">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="f1dae-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="f1dae-115">-Force</span><span class="sxs-lookup"><span data-stu-id="f1dae-115">-Force</span></span>
<span data-ttu-id="f1dae-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f1dae-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f1dae-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f1dae-117">-Location</span></span>
<span data-ttu-id="f1dae-118">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="f1dae-118">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1dae-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f1dae-119">-Name</span></span>
<span data-ttu-id="f1dae-120">Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="f1dae-120">Infrastructure role name.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1dae-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1dae-121">-ResourceGroupName</span></span>
<span data-ttu-id="f1dae-122">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="f1dae-122">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Restart
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1dae-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f1dae-123">-ResourceId</span></span>
<span data-ttu-id="f1dae-124">Identyfikator zasobu roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="f1dae-124">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="f1dae-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f1dae-125">-Confirm</span></span>
<span data-ttu-id="f1dae-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1dae-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1dae-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1dae-127">-WhatIf</span></span>
<span data-ttu-id="f1dae-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1dae-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1dae-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f1dae-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1dae-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1dae-130">CommonParameters</span></span>
<span data-ttu-id="f1dae-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1dae-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1dae-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1dae-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1dae-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1dae-133">INPUTS</span></span>

## <span data-ttu-id="f1dae-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f1dae-134">OUTPUTS</span></span>

## <span data-ttu-id="f1dae-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f1dae-135">NOTES</span></span>

## <span data-ttu-id="f1dae-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1dae-136">RELATED LINKS</span></span>
