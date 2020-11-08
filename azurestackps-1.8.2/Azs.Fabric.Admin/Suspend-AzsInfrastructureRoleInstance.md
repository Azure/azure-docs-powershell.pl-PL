---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04b011279d88f294e1caf95519e29a8368b08546
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94055846"
---
# <span data-ttu-id="0cc4f-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="0cc4f-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="0cc4f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0cc4f-102">SYNOPSIS</span></span>
<span data-ttu-id="0cc4f-103">Zamykanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="0cc4f-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="0cc4f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0cc4f-104">SYNTAX</span></span>

### <span data-ttu-id="0cc4f-105">Zamknięcie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="0cc4f-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0cc4f-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="0cc4f-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0cc4f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0cc4f-107">DESCRIPTION</span></span>
<span data-ttu-id="0cc4f-108">Zamykanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="0cc4f-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="0cc4f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0cc4f-109">EXAMPLES</span></span>

### <span data-ttu-id="0cc4f-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="0cc4f-110">EXAMPLE 1</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="0cc4f-111">Zamykanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="0cc4f-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="0cc4f-112">W przypadku niepowodzenia jest zgłaszany wyjątek.</span><span class="sxs-lookup"><span data-stu-id="0cc4f-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="0cc4f-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0cc4f-113">PARAMETERS</span></span>

### <span data-ttu-id="0cc4f-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0cc4f-114">-Name</span></span>
<span data-ttu-id="0cc4f-115">Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="0cc4f-115">Name of an infrastructure role instance.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc4f-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="0cc4f-116">-Location</span></span>
<span data-ttu-id="0cc4f-117">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="0cc4f-117">Location of the resource.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc4f-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0cc4f-118">-ResourceGroupName</span></span>
<span data-ttu-id="0cc4f-119">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="0cc4f-119">Resource group in which the resource provider has been registered.</span></span>

```yaml
Type: String
Parameter Sets: Shutdown
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0cc4f-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0cc4f-120">-ResourceId</span></span>
<span data-ttu-id="0cc4f-121">Identyfikator zasobu wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="0cc4f-121">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="0cc4f-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0cc4f-122">-AsJob</span></span>
<span data-ttu-id="0cc4f-123">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="0cc4f-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="0cc4f-124">-Force</span><span class="sxs-lookup"><span data-stu-id="0cc4f-124">-Force</span></span>
<span data-ttu-id="0cc4f-125">Nie pytaj o potwierdzenie</span><span class="sxs-lookup"><span data-stu-id="0cc4f-125">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="0cc4f-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0cc4f-126">-WhatIf</span></span>
<span data-ttu-id="0cc4f-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cc4f-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0cc4f-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0cc4f-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0cc4f-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0cc4f-129">-Confirm</span></span>
<span data-ttu-id="0cc4f-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0cc4f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0cc4f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0cc4f-131">CommonParameters</span></span>
<span data-ttu-id="0cc4f-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0cc4f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0cc4f-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0cc4f-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0cc4f-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0cc4f-134">INPUTS</span></span>

## <span data-ttu-id="0cc4f-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0cc4f-135">OUTPUTS</span></span>

## <span data-ttu-id="0cc4f-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0cc4f-136">NOTES</span></span>

## <span data-ttu-id="0cc4f-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0cc4f-137">RELATED LINKS</span></span>
