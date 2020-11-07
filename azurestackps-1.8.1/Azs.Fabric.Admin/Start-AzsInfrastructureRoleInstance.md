---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 48f7fd6280596e70810d330f3fe69b37059e15cd
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889485"
---
# <span data-ttu-id="e7091-101">Start-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="e7091-101">Start-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="e7091-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e7091-102">SYNOPSIS</span></span>
<span data-ttu-id="e7091-103">Włączanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="e7091-103">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="e7091-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e7091-104">SYNTAX</span></span>

### <span data-ttu-id="e7091-105">PowerOn (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e7091-105">PowerOn (Default)</span></span>
```
Start-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e7091-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="e7091-106">ResourceId</span></span>
```
Start-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e7091-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e7091-107">DESCRIPTION</span></span>
<span data-ttu-id="e7091-108">Włączanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="e7091-108">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="e7091-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e7091-109">EXAMPLES</span></span>

### <span data-ttu-id="e7091-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="e7091-110">EXAMPLE 1</span></span>
```
Start-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="e7091-111">Włączanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="e7091-111">Power on an infrastructure role instance.</span></span>

## <span data-ttu-id="e7091-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e7091-112">PARAMETERS</span></span>

### <span data-ttu-id="e7091-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e7091-113">-Name</span></span>
<span data-ttu-id="e7091-114">Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="e7091-114">Name of the infrastructure role instance.</span></span>

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

### <span data-ttu-id="e7091-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e7091-115">-Location</span></span>
<span data-ttu-id="e7091-116">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="e7091-116">Location of the resource.</span></span>

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

### <span data-ttu-id="e7091-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e7091-117">-ResourceGroupName</span></span>
<span data-ttu-id="e7091-118">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="e7091-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="e7091-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e7091-119">-ResourceId</span></span>
<span data-ttu-id="e7091-120">Identyfikator zasobu wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="e7091-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="e7091-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e7091-121">-AsJob</span></span>
<span data-ttu-id="e7091-122">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="e7091-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="e7091-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e7091-123">-Force</span></span>
<span data-ttu-id="e7091-124">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e7091-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e7091-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e7091-125">-WhatIf</span></span>
<span data-ttu-id="e7091-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7091-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e7091-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e7091-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e7091-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e7091-128">-Confirm</span></span>
<span data-ttu-id="e7091-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e7091-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e7091-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e7091-130">CommonParameters</span></span>
<span data-ttu-id="e7091-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e7091-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e7091-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e7091-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e7091-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e7091-133">INPUTS</span></span>

## <span data-ttu-id="e7091-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e7091-134">OUTPUTS</span></span>

## <span data-ttu-id="e7091-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e7091-135">NOTES</span></span>

## <span data-ttu-id="e7091-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e7091-136">RELATED LINKS</span></span>
