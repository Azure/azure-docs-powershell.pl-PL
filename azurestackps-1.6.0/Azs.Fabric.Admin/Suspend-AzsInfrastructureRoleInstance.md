---
external help file: Azs.Fabric.Admin-help.xml
Module Name: Azs.Fabric.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 348582b008d50371bc937961cd76edbf1ba13762
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523621"
---
# <span data-ttu-id="3ecca-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="3ecca-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="3ecca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3ecca-102">SYNOPSIS</span></span>
<span data-ttu-id="3ecca-103">Zamykanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="3ecca-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="3ecca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3ecca-104">SYNTAX</span></span>

### <span data-ttu-id="3ecca-105">Zamknięcie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="3ecca-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3ecca-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="3ecca-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ecca-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3ecca-107">DESCRIPTION</span></span>
<span data-ttu-id="3ecca-108">Zamykanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="3ecca-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="3ecca-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3ecca-109">EXAMPLES</span></span>

### <span data-ttu-id="3ecca-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="3ecca-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="3ecca-111">Zamykanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="3ecca-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="3ecca-112">W przypadku niepowodzenia jest zgłaszany wyjątek.</span><span class="sxs-lookup"><span data-stu-id="3ecca-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="3ecca-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3ecca-113">PARAMETERS</span></span>

### <span data-ttu-id="3ecca-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3ecca-114">-AsJob</span></span>
<span data-ttu-id="3ecca-115">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="3ecca-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="3ecca-116">-Force</span><span class="sxs-lookup"><span data-stu-id="3ecca-116">-Force</span></span>
<span data-ttu-id="3ecca-117">Nie pytaj o potwierdzenie</span><span class="sxs-lookup"><span data-stu-id="3ecca-117">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="3ecca-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="3ecca-118">-Location</span></span>
<span data-ttu-id="3ecca-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="3ecca-119">Location of the resource.</span></span>

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

### <span data-ttu-id="3ecca-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3ecca-120">-Name</span></span>
<span data-ttu-id="3ecca-121">Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="3ecca-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="3ecca-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3ecca-122">-ResourceGroupName</span></span>
<span data-ttu-id="3ecca-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="3ecca-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="3ecca-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3ecca-124">-ResourceId</span></span>
<span data-ttu-id="3ecca-125">Identyfikator zasobu wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="3ecca-125">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="3ecca-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3ecca-126">-Confirm</span></span>
<span data-ttu-id="3ecca-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ecca-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ecca-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ecca-128">-WhatIf</span></span>
<span data-ttu-id="3ecca-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3ecca-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ecca-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3ecca-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ecca-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ecca-131">CommonParameters</span></span>
<span data-ttu-id="3ecca-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ecca-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ecca-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ecca-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ecca-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3ecca-134">INPUTS</span></span>

## <span data-ttu-id="3ecca-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3ecca-135">OUTPUTS</span></span>

## <span data-ttu-id="3ecca-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3ecca-136">NOTES</span></span>

## <span data-ttu-id="3ecca-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3ecca-137">RELATED LINKS</span></span>

