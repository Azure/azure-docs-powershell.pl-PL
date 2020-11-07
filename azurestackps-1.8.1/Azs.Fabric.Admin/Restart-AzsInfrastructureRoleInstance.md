---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 03dfddb3ec666df5096184c5e00692862e091626
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93890061"
---
# <span data-ttu-id="e3bd6-101">Restart-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="e3bd6-101">Restart-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="e3bd6-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e3bd6-102">SYNOPSIS</span></span>
<span data-ttu-id="e3bd6-103">Uruchom ponownie wystąpienie roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-103">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="e3bd6-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e3bd6-104">SYNTAX</span></span>

### <span data-ttu-id="e3bd6-105">Uruchom ponownie (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="e3bd6-105">Restart (Default)</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e3bd6-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="e3bd6-106">ResourceId</span></span>
```
Restart-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e3bd6-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e3bd6-107">DESCRIPTION</span></span>
<span data-ttu-id="e3bd6-108">Uruchom ponownie wystąpienie roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-108">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="e3bd6-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e3bd6-109">EXAMPLES</span></span>

### <span data-ttu-id="e3bd6-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="e3bd6-110">EXAMPLE 1</span></span>
```
Restart-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="e3bd6-111">Uruchom ponownie wystąpienie roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-111">Reboot an infrastructure role instance.</span></span>

## <span data-ttu-id="e3bd6-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e3bd6-112">PARAMETERS</span></span>

### <span data-ttu-id="e3bd6-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e3bd6-113">-Name</span></span>
<span data-ttu-id="e3bd6-114">Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-114">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="e3bd6-115">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="e3bd6-115">-Location</span></span>
<span data-ttu-id="e3bd6-116">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-116">Location of the resource.</span></span>

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

### <span data-ttu-id="e3bd6-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e3bd6-117">-ResourceGroupName</span></span>
<span data-ttu-id="e3bd6-118">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-118">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="e3bd6-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e3bd6-119">-ResourceId</span></span>
<span data-ttu-id="e3bd6-120">Identyfikator zasobu wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-120">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="e3bd6-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e3bd6-121">-AsJob</span></span>
<span data-ttu-id="e3bd6-122">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-122">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="e3bd6-123">-Force</span><span class="sxs-lookup"><span data-stu-id="e3bd6-123">-Force</span></span>
<span data-ttu-id="e3bd6-124">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-124">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="e3bd6-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e3bd6-125">-WhatIf</span></span>
<span data-ttu-id="e3bd6-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e3bd6-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e3bd6-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e3bd6-128">-Confirm</span></span>
<span data-ttu-id="e3bd6-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e3bd6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3bd6-130">CommonParameters</span></span>
<span data-ttu-id="e3bd6-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e3bd6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3bd6-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e3bd6-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3bd6-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e3bd6-133">INPUTS</span></span>

## <span data-ttu-id="e3bd6-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e3bd6-134">OUTPUTS</span></span>

## <span data-ttu-id="e3bd6-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e3bd6-135">NOTES</span></span>

## <span data-ttu-id="e3bd6-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e3bd6-136">RELATED LINKS</span></span>
