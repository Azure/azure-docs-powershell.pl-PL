---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48f7fd6280596e70810d330f3fe69b37059e15cd
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93888921"
---
# <span data-ttu-id="20d21-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="20d21-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="20d21-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20d21-102">SYNOPSIS</span></span>
<span data-ttu-id="20d21-103">Włączanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="20d21-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="20d21-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20d21-104">SYNTAX</span></span>

### <span data-ttu-id="20d21-105">PowerOn (domyślny)</span><span class="sxs-lookup"><span data-stu-id="20d21-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="20d21-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="20d21-106">ResourceId</span></span>
```
Start-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20d21-107">Opis</span><span class="sxs-lookup"><span data-stu-id="20d21-107">DESCRIPTION</span></span>
<span data-ttu-id="20d21-108">Włączanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="20d21-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="20d21-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20d21-109">EXAMPLES</span></span>

### <span data-ttu-id="20d21-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="20d21-110">EXAMPLE 1</span></span>
```
Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="20d21-111">Włączanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="20d21-111">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="20d21-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20d21-112">PARAMETERS</span></span>

### <span data-ttu-id="20d21-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="20d21-113">-Name</span></span>
<span data-ttu-id="20d21-114">Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="20d21-114">Name of the infrastructure role instance.</span></span>

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

### <span data-ttu-id="20d21-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="20d21-115">-Location</span></span>
<span data-ttu-id="20d21-116">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="20d21-116">Location of the resource.</span></span>

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

### <span data-ttu-id="20d21-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20d21-117">-ResourceGroupName</span></span>
<span data-ttu-id="20d21-118">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="20d21-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="20d21-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="20d21-119">-ResourceId</span></span>
<span data-ttu-id="20d21-120">Identyfikator zasobu wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="20d21-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="20d21-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="20d21-121">-AsJob</span></span>
<span data-ttu-id="20d21-122">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="20d21-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="20d21-123">-Force</span><span class="sxs-lookup"><span data-stu-id="20d21-123">-Force</span></span>
<span data-ttu-id="20d21-124">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="20d21-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="20d21-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20d21-125">-WhatIf</span></span>
<span data-ttu-id="20d21-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20d21-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20d21-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="20d21-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20d21-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="20d21-128">-Confirm</span></span>
<span data-ttu-id="20d21-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20d21-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20d21-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20d21-130">CommonParameters</span></span>
<span data-ttu-id="20d21-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20d21-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20d21-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20d21-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20d21-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20d21-133">INPUTS</span></span>

## <span data-ttu-id="20d21-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20d21-134">OUTPUTS</span></span>

## <span data-ttu-id="20d21-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20d21-135">NOTES</span></span>

## <span data-ttu-id="20d21-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20d21-136">RELATED LINKS</span></span>
