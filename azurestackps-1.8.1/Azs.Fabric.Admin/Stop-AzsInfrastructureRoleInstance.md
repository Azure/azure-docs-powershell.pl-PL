---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 47e4c38d3ccd98350721d358cb98eec55341ba97
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93889942"
---
# <span data-ttu-id="f906e-101">Stop-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="f906e-101">Stop-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="f906e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f906e-102">SYNOPSIS</span></span>
<span data-ttu-id="f906e-103">Wyłącz opcję wyłączania roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="f906e-103">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="f906e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f906e-104">SYNTAX</span></span>

### <span data-ttu-id="f906e-105">PowerOff (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f906e-105">PowerOff (Default)</span></span>
```
Stop-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-AsJob]
 [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f906e-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="f906e-106">ResourceId</span></span>
```
Stop-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f906e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f906e-107">DESCRIPTION</span></span>
<span data-ttu-id="f906e-108">Wyłącz opcję wyłączania roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="f906e-108">Power off an infrastructure role instance.</span></span>

## <span data-ttu-id="f906e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f906e-109">EXAMPLES</span></span>

### <span data-ttu-id="f906e-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="f906e-110">EXAMPLE 1</span></span>
```
Stop-AzsInfrastructureRoleInstancef -Name "AzS-ACS01"
```

<span data-ttu-id="f906e-111">Wyłącz funkcję wyłączania roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="f906e-111">Power off a infrastructure role instance.</span></span>

## <span data-ttu-id="f906e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f906e-112">PARAMETERS</span></span>

### <span data-ttu-id="f906e-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f906e-113">-Name</span></span>
<span data-ttu-id="f906e-114">Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="f906e-114">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f906e-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f906e-115">-Location</span></span>
<span data-ttu-id="f906e-116">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="f906e-116">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f906e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f906e-117">-ResourceGroupName</span></span>
<span data-ttu-id="f906e-118">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="f906e-118">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: PowerOff
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f906e-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f906e-119">-ResourceId</span></span>
<span data-ttu-id="f906e-120">Identyfikator zasobu wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="f906e-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="f906e-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f906e-121">-AsJob</span></span>
<span data-ttu-id="f906e-122">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="f906e-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="f906e-123">-Force</span><span class="sxs-lookup"><span data-stu-id="f906e-123">-Force</span></span>
<span data-ttu-id="f906e-124">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f906e-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="f906e-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f906e-125">-WhatIf</span></span>
<span data-ttu-id="f906e-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f906e-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f906e-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f906e-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f906e-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f906e-128">-Confirm</span></span>
<span data-ttu-id="f906e-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f906e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f906e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f906e-130">CommonParameters</span></span>
<span data-ttu-id="f906e-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f906e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f906e-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f906e-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f906e-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f906e-133">INPUTS</span></span>

## <span data-ttu-id="f906e-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f906e-134">OUTPUTS</span></span>

## <span data-ttu-id="f906e-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f906e-135">NOTES</span></span>

## <span data-ttu-id="f906e-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f906e-136">RELATED LINKS</span></span>
