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
ms.locfileid: "93523126"
---
# <span data-ttu-id="4ddda-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="4ddda-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="4ddda-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ddda-102">SYNOPSIS</span></span>
<span data-ttu-id="4ddda-103">Ponowne uruchomienie żądanej roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="4ddda-103">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="4ddda-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ddda-104">SYNTAX</span></span>

### <span data-ttu-id="4ddda-105">Uruchom ponownie (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="4ddda-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4ddda-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="4ddda-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4ddda-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4ddda-107">DESCRIPTION</span></span>
<span data-ttu-id="4ddda-108">Ponowne uruchomienie żądanej roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="4ddda-108">Restarts the requested infrastructure role.</span></span>

## <span data-ttu-id="4ddda-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ddda-109">EXAMPLES</span></span>

### <span data-ttu-id="4ddda-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="4ddda-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Restart-AzsInfrastructureRole -Name "Compute Controller"
```

<span data-ttu-id="4ddda-111">Uruchom ponownie rolę infrastruktury, która uległa awarii.</span><span class="sxs-lookup"><span data-stu-id="4ddda-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="4ddda-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ddda-112">PARAMETERS</span></span>

### <span data-ttu-id="4ddda-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4ddda-113">-AsJob</span></span>
<span data-ttu-id="4ddda-114">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="4ddda-114">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="4ddda-115">-Force</span><span class="sxs-lookup"><span data-stu-id="4ddda-115">-Force</span></span>
<span data-ttu-id="4ddda-116">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4ddda-116">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="4ddda-117">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4ddda-117">-Location</span></span>
<span data-ttu-id="4ddda-118">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="4ddda-118">Location of the resource.</span></span>

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

### <span data-ttu-id="4ddda-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4ddda-119">-Name</span></span>
<span data-ttu-id="4ddda-120">Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="4ddda-120">Infrastructure role name.</span></span>

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

### <span data-ttu-id="4ddda-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ddda-121">-ResourceGroupName</span></span>
<span data-ttu-id="4ddda-122">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="4ddda-122">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="4ddda-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4ddda-123">-ResourceId</span></span>
<span data-ttu-id="4ddda-124">Identyfikator zasobu roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="4ddda-124">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="4ddda-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ddda-125">-Confirm</span></span>
<span data-ttu-id="4ddda-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ddda-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ddda-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ddda-127">-WhatIf</span></span>
<span data-ttu-id="4ddda-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ddda-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ddda-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4ddda-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ddda-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ddda-130">CommonParameters</span></span>
<span data-ttu-id="4ddda-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ddda-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ddda-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4ddda-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ddda-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ddda-133">INPUTS</span></span>

## <span data-ttu-id="4ddda-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ddda-134">OUTPUTS</span></span>

## <span data-ttu-id="4ddda-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ddda-135">NOTES</span></span>

## <span data-ttu-id="4ddda-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ddda-136">RELATED LINKS</span></span>

