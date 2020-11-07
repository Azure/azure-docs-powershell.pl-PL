---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 04b011279d88f294e1caf95519e29a8368b08546
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/15/2020
ms.locfileid: "93890038"
---
# <span data-ttu-id="dccb2-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="dccb2-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="dccb2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dccb2-102">SYNOPSIS</span></span>
<span data-ttu-id="dccb2-103">Zamykanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="dccb2-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="dccb2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dccb2-104">SYNTAX</span></span>

### <span data-ttu-id="dccb2-105">Zamknięcie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="dccb2-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dccb2-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="dccb2-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dccb2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dccb2-107">DESCRIPTION</span></span>
<span data-ttu-id="dccb2-108">Zamykanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="dccb2-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="dccb2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dccb2-109">EXAMPLES</span></span>

### <span data-ttu-id="dccb2-110">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="dccb2-110">EXAMPLE 1</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="dccb2-111">Zamykanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="dccb2-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="dccb2-112">W przypadku niepowodzenia jest zgłaszany wyjątek.</span><span class="sxs-lookup"><span data-stu-id="dccb2-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="dccb2-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dccb2-113">PARAMETERS</span></span>

### <span data-ttu-id="dccb2-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dccb2-114">-Name</span></span>
<span data-ttu-id="dccb2-115">Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="dccb2-115">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="dccb2-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dccb2-116">-Location</span></span>
<span data-ttu-id="dccb2-117">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="dccb2-117">Location of the resource.</span></span>

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

### <span data-ttu-id="dccb2-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dccb2-118">-ResourceGroupName</span></span>
<span data-ttu-id="dccb2-119">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="dccb2-119">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="dccb2-120">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dccb2-120">-ResourceId</span></span>
<span data-ttu-id="dccb2-121">Identyfikator zasobu wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="dccb2-121">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="dccb2-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dccb2-122">-AsJob</span></span>
<span data-ttu-id="dccb2-123">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="dccb2-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="dccb2-124">-Force</span><span class="sxs-lookup"><span data-stu-id="dccb2-124">-Force</span></span>
<span data-ttu-id="dccb2-125">Nie pytaj o potwierdzenie</span><span class="sxs-lookup"><span data-stu-id="dccb2-125">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="dccb2-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dccb2-126">-WhatIf</span></span>
<span data-ttu-id="dccb2-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dccb2-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dccb2-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dccb2-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dccb2-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dccb2-129">-Confirm</span></span>
<span data-ttu-id="dccb2-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dccb2-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dccb2-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dccb2-131">CommonParameters</span></span>
<span data-ttu-id="dccb2-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dccb2-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dccb2-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dccb2-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dccb2-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dccb2-134">INPUTS</span></span>

## <span data-ttu-id="dccb2-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dccb2-135">OUTPUTS</span></span>

## <span data-ttu-id="dccb2-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dccb2-136">NOTES</span></span>

## <span data-ttu-id="dccb2-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dccb2-137">RELATED LINKS</span></span>
