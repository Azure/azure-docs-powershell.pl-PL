---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 19c8f8fce7c3711c5002f9588900e6bdf8efcbb0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888338"
---
# <span data-ttu-id="cb6c1-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="cb6c1-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="cb6c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cb6c1-102">SYNOPSIS</span></span>
<span data-ttu-id="cb6c1-103">Umożliwia wznowienie uruchomionego wcześniej uruchomienia aktualizacji, którego nie udało się wykonać.</span><span class="sxs-lookup"><span data-stu-id="cb6c1-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="cb6c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cb6c1-104">SYNTAX</span></span>

### <span data-ttu-id="cb6c1-105">UpdateRuns_Rerun (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="cb6c1-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb6c1-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="cb6c1-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb6c1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="cb6c1-107">DESCRIPTION</span></span>
<span data-ttu-id="cb6c1-108">Umożliwia wznowienie uruchomionego wcześniej uruchomienia aktualizacji, którego nie udało się wykonać.</span><span class="sxs-lookup"><span data-stu-id="cb6c1-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="cb6c1-109">Wznowiony przebieg aktualizacji zostanie wznowiony w momencie ostatniej awarii.</span><span class="sxs-lookup"><span data-stu-id="cb6c1-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="cb6c1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cb6c1-110">EXAMPLES</span></span>

### <span data-ttu-id="cb6c1-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cb6c1-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="cb6c1-112">Umożliwia wznowienie uruchomionego wcześniej uruchomienia aktualizacji, którego nie udało się wykonać.</span><span class="sxs-lookup"><span data-stu-id="cb6c1-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="cb6c1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cb6c1-113">PARAMETERS</span></span>

### <span data-ttu-id="cb6c1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cb6c1-114">-AsJob</span></span>
<span data-ttu-id="cb6c1-115">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="cb6c1-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="cb6c1-116">-Force</span><span class="sxs-lookup"><span data-stu-id="cb6c1-116">-Force</span></span>
<span data-ttu-id="cb6c1-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cb6c1-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="cb6c1-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cb6c1-118">-Location</span></span>
<span data-ttu-id="cb6c1-119">Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="cb6c1-119">The name of the update location.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb6c1-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cb6c1-120">-Name</span></span>
<span data-ttu-id="cb6c1-121">Identyfikator uruchomienia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="cb6c1-121">Update run identifier.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb6c1-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cb6c1-122">-ResourceGroupName</span></span>
<span data-ttu-id="cb6c1-123">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="cb6c1-123">The resource group the resource is located under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb6c1-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cb6c1-124">-ResourceId</span></span>
<span data-ttu-id="cb6c1-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="cb6c1-125">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb6c1-126">-Updatename</span><span class="sxs-lookup"><span data-stu-id="cb6c1-126">-UpdateName</span></span>
<span data-ttu-id="cb6c1-127">Nazwa wyświetlana aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="cb6c1-127">Display name of the update.</span></span>

```yaml
Type: String
Parameter Sets: UpdateRuns_Rerun
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb6c1-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cb6c1-128">-Confirm</span></span>
<span data-ttu-id="cb6c1-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb6c1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb6c1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb6c1-130">-WhatIf</span></span>
<span data-ttu-id="cb6c1-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb6c1-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb6c1-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cb6c1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cb6c1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb6c1-133">CommonParameters</span></span>
<span data-ttu-id="cb6c1-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb6c1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb6c1-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb6c1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb6c1-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb6c1-136">INPUTS</span></span>

## <span data-ttu-id="cb6c1-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cb6c1-137">OUTPUTS</span></span>

## <span data-ttu-id="cb6c1-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cb6c1-138">NOTES</span></span>

## <span data-ttu-id="cb6c1-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb6c1-139">RELATED LINKS</span></span>

