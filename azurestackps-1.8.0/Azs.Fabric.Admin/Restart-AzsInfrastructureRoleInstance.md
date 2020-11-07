---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03dfddb3ec666df5096184c5e00692862e091626
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93888926"
---
# <span data-ttu-id="af607-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="af607-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="af607-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af607-102">SYNOPSIS</span></span>
<span data-ttu-id="af607-103">Uruchom ponownie wystąpienie roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="af607-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="af607-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af607-104">SYNTAX</span></span>

### <span data-ttu-id="af607-105">Uruchom ponownie (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="af607-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af607-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="af607-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="af607-107">Opis</span><span class="sxs-lookup"><span data-stu-id="af607-107">DESCRIPTION</span></span>
<span data-ttu-id="af607-108">Uruchom ponownie wystąpienie roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="af607-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="af607-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af607-109">EXAMPLES</span></span>

### <span data-ttu-id="af607-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="af607-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="af607-111">Uruchom ponownie wystąpienie roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="af607-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="af607-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af607-112">PARAMETERS</span></span>

### <span data-ttu-id="af607-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="af607-113">-Name</span></span>
<span data-ttu-id="af607-114">Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="af607-114">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="af607-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="af607-115">-Location</span></span>
<span data-ttu-id="af607-116">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="af607-116">Location of the resource.</span></span>

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

### <span data-ttu-id="af607-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af607-117">-ResourceGroupName</span></span>
<span data-ttu-id="af607-118">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="af607-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="af607-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="af607-119">-ResourceId</span></span>
<span data-ttu-id="af607-120">Identyfikator zasobu wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="af607-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="af607-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="af607-121">-AsJob</span></span>
<span data-ttu-id="af607-122">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="af607-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="af607-123">-Force</span><span class="sxs-lookup"><span data-stu-id="af607-123">-Force</span></span>
<span data-ttu-id="af607-124">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="af607-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="af607-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af607-125">-WhatIf</span></span>
<span data-ttu-id="af607-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af607-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af607-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="af607-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af607-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="af607-128">-Confirm</span></span>
<span data-ttu-id="af607-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af607-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af607-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af607-130">CommonParameters</span></span>
<span data-ttu-id="af607-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af607-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af607-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af607-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af607-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af607-133">INPUTS</span></span>

## <span data-ttu-id="af607-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af607-134">OUTPUTS</span></span>

## <span data-ttu-id="af607-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af607-135">NOTES</span></span>

## <span data-ttu-id="af607-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af607-136">RELATED LINKS</span></span>
