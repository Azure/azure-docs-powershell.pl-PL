---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 781b920bf955a84554b9152f54c9847a00a8b160
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055702"
---
# <span data-ttu-id="f82fb-101">Restart-AzsInfrastructureRole</span><span class="sxs-lookup"><span data-stu-id="f82fb-101">Restart-AzsInfrastructureRole</span></span>

## <span data-ttu-id="f82fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f82fb-102">SYNOPSIS</span></span>
<span data-ttu-id="f82fb-103">Ponownie uruchamia żądaną rolę infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="f82fb-103">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="f82fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f82fb-104">SYNTAX</span></span>

### <span data-ttu-id="f82fb-105">Uruchom ponownie (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="f82fb-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRole -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f82fb-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="f82fb-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRole -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f82fb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f82fb-107">DESCRIPTION</span></span>
<span data-ttu-id="f82fb-108">Ponownie uruchamia żądaną rolę infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="f82fb-108">Restarts the requestd infrastructure role.</span></span>

## <span data-ttu-id="f82fb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f82fb-109">EXAMPLES</span></span>

### <span data-ttu-id="f82fb-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="f82fb-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRole -Name "Active Directory Federation Services"
```

<span data-ttu-id="f82fb-111">Uruchom ponownie rolę infrastruktury, która uległa awarii.</span><span class="sxs-lookup"><span data-stu-id="f82fb-111">Restart an infrastructure role which has crashed.</span></span>

## <span data-ttu-id="f82fb-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f82fb-112">PARAMETERS</span></span>

### <span data-ttu-id="f82fb-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f82fb-113">-Name</span></span>
<span data-ttu-id="f82fb-114">Nazwa roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="f82fb-114">Infrastructure role name.</span></span>

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

### <span data-ttu-id="f82fb-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f82fb-115">-Location</span></span>
<span data-ttu-id="f82fb-116">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="f82fb-116">Location of the resource.</span></span>

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

### <span data-ttu-id="f82fb-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f82fb-117">-ResourceGroupName</span></span>
<span data-ttu-id="f82fb-118">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="f82fb-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="f82fb-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f82fb-119">-ResourceId</span></span>
<span data-ttu-id="f82fb-120">Identyfikator zasobu roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="f82fb-120">Infrastructure role resource ID.</span></span>

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

### <span data-ttu-id="f82fb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f82fb-121">-AsJob</span></span>
<span data-ttu-id="f82fb-122">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="f82fb-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="f82fb-123">-Force</span><span class="sxs-lookup"><span data-stu-id="f82fb-123">-Force</span></span>
<span data-ttu-id="f82fb-124">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f82fb-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f82fb-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f82fb-125">-WhatIf</span></span>
<span data-ttu-id="f82fb-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f82fb-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f82fb-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f82fb-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f82fb-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f82fb-128">-Confirm</span></span>
<span data-ttu-id="f82fb-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f82fb-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f82fb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f82fb-130">CommonParameters</span></span>
<span data-ttu-id="f82fb-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f82fb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f82fb-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f82fb-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f82fb-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f82fb-133">INPUTS</span></span>

## <span data-ttu-id="f82fb-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f82fb-134">OUTPUTS</span></span>

## <span data-ttu-id="f82fb-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f82fb-135">NOTES</span></span>

## <span data-ttu-id="f82fb-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f82fb-136">RELATED LINKS</span></span>
