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
ms.locfileid: "93524101"
---
# <span data-ttu-id="334f9-101">Suspend-AzsInfrastructureRoleInstance</span><span class="sxs-lookup"><span data-stu-id="334f9-101">Suspend-AzsInfrastructureRoleInstance</span></span>

## <span data-ttu-id="334f9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="334f9-102">SYNOPSIS</span></span>
<span data-ttu-id="334f9-103">Zamykanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="334f9-103">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="334f9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="334f9-104">SYNTAX</span></span>

### <span data-ttu-id="334f9-105">Zamknięcie (domyślne)</span><span class="sxs-lookup"><span data-stu-id="334f9-105">Shutdown (Default)</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name <String> [-Location <String>] [-ResourceGroupName <String>]
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="334f9-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="334f9-106">ResourceId</span></span>
```
Suspend-AzsInfrastructureRoleInstance -ResourceId <String> [-AsJob] [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="334f9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="334f9-107">DESCRIPTION</span></span>
<span data-ttu-id="334f9-108">Zamykanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="334f9-108">Shut down an infrastructure role instance.</span></span>

## <span data-ttu-id="334f9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="334f9-109">EXAMPLES</span></span>

### <span data-ttu-id="334f9-110">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="334f9-110">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Suspend-AzsInfrastructureRoleInstance -Name "AzS-ACS01"
```

<span data-ttu-id="334f9-111">Zamykanie wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="334f9-111">Shut down an infrastructure role instance.</span></span>
<span data-ttu-id="334f9-112">W przypadku niepowodzenia jest zgłaszany wyjątek.</span><span class="sxs-lookup"><span data-stu-id="334f9-112">On failure an exception is thrown.</span></span>

## <span data-ttu-id="334f9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="334f9-113">PARAMETERS</span></span>

### <span data-ttu-id="334f9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="334f9-114">-AsJob</span></span>
<span data-ttu-id="334f9-115">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="334f9-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="334f9-116">-Force</span><span class="sxs-lookup"><span data-stu-id="334f9-116">-Force</span></span>
<span data-ttu-id="334f9-117">Nie pytaj o potwierdzenie</span><span class="sxs-lookup"><span data-stu-id="334f9-117">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="334f9-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="334f9-118">-Location</span></span>
<span data-ttu-id="334f9-119">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="334f9-119">Location of the resource.</span></span>

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

### <span data-ttu-id="334f9-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="334f9-120">-Name</span></span>
<span data-ttu-id="334f9-121">Nazwa wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="334f9-121">Name of an infrastructure role instance.</span></span>

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

### <span data-ttu-id="334f9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="334f9-122">-ResourceGroupName</span></span>
<span data-ttu-id="334f9-123">Grupa zasobów, w której dostawca zasobów został zarejestrowany.</span><span class="sxs-lookup"><span data-stu-id="334f9-123">Resource group in which the resource provider has been registered.</span></span>

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

### <span data-ttu-id="334f9-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="334f9-124">-ResourceId</span></span>
<span data-ttu-id="334f9-125">Identyfikator zasobu wystąpienia roli infrastruktury.</span><span class="sxs-lookup"><span data-stu-id="334f9-125">Infrastructure role instance resource ID.</span></span>

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

### <span data-ttu-id="334f9-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="334f9-126">-Confirm</span></span>
<span data-ttu-id="334f9-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="334f9-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="334f9-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="334f9-128">-WhatIf</span></span>
<span data-ttu-id="334f9-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="334f9-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="334f9-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="334f9-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="334f9-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="334f9-131">CommonParameters</span></span>
<span data-ttu-id="334f9-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="334f9-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="334f9-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="334f9-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="334f9-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="334f9-134">INPUTS</span></span>

## <span data-ttu-id="334f9-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="334f9-135">OUTPUTS</span></span>

## <span data-ttu-id="334f9-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="334f9-136">NOTES</span></span>

## <span data-ttu-id="334f9-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="334f9-137">RELATED LINKS</span></span>

