---
external help file: Azs.Update.Admin-help.xml
Module Name: Azs.Update.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb3b784d079d1de3cec1d4fe3ec50a2853a4b054
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061534"
---
# <span data-ttu-id="fc09e-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="fc09e-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="fc09e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc09e-102">SYNOPSIS</span></span>
<span data-ttu-id="fc09e-103">Umożliwia wznowienie uruchomionego wcześniej uruchomienia aktualizacji, którego nie udało się wykonać.</span><span class="sxs-lookup"><span data-stu-id="fc09e-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="fc09e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc09e-104">SYNTAX</span></span>

### <span data-ttu-id="fc09e-105">UpdateRuns_Rerun (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="fc09e-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc09e-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="fc09e-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc09e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fc09e-107">DESCRIPTION</span></span>
<span data-ttu-id="fc09e-108">Umożliwia wznowienie uruchomionego wcześniej uruchomienia aktualizacji, którego nie udało się wykonać.</span><span class="sxs-lookup"><span data-stu-id="fc09e-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="fc09e-109">Wznowiony przebieg aktualizacji zostanie wznowiony w momencie ostatniej awarii.</span><span class="sxs-lookup"><span data-stu-id="fc09e-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="fc09e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc09e-110">EXAMPLES</span></span>

### <span data-ttu-id="fc09e-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="fc09e-111">EXAMPLE 1</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="fc09e-112">Umożliwia wznowienie uruchomionego wcześniej uruchomienia aktualizacji, którego nie udało się wykonać.</span><span class="sxs-lookup"><span data-stu-id="fc09e-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="fc09e-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc09e-113">PARAMETERS</span></span>

### <span data-ttu-id="fc09e-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fc09e-114">-Name</span></span>
<span data-ttu-id="fc09e-115">Identyfikator uruchomienia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="fc09e-115">Update run identifier.</span></span>

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

### <span data-ttu-id="fc09e-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fc09e-116">-Location</span></span>
<span data-ttu-id="fc09e-117">Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="fc09e-117">The name of the update location.</span></span>

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

### <span data-ttu-id="fc09e-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc09e-118">-ResourceGroupName</span></span>
<span data-ttu-id="fc09e-119">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="fc09e-119">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="fc09e-120">-Updatename</span><span class="sxs-lookup"><span data-stu-id="fc09e-120">-UpdateName</span></span>
<span data-ttu-id="fc09e-121">Nazwa wyświetlana aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="fc09e-121">Display name of the update.</span></span>

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

### <span data-ttu-id="fc09e-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc09e-122">-AsJob</span></span>
<span data-ttu-id="fc09e-123">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="fc09e-123">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="fc09e-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fc09e-124">-ResourceId</span></span>
<span data-ttu-id="fc09e-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="fc09e-125">The resource id.</span></span>

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

### <span data-ttu-id="fc09e-126">-Force</span><span class="sxs-lookup"><span data-stu-id="fc09e-126">-Force</span></span>
<span data-ttu-id="fc09e-127">Flaga usunięcia elementu bez potwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="fc09e-127">Flag to remove the item without confirmation.</span></span>

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

### <span data-ttu-id="fc09e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc09e-128">-WhatIf</span></span>
<span data-ttu-id="fc09e-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc09e-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc09e-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fc09e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc09e-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc09e-131">-Confirm</span></span>
<span data-ttu-id="fc09e-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc09e-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc09e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc09e-133">CommonParameters</span></span>
<span data-ttu-id="fc09e-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc09e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc09e-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc09e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc09e-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc09e-136">INPUTS</span></span>

## <span data-ttu-id="fc09e-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc09e-137">OUTPUTS</span></span>

## <span data-ttu-id="fc09e-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc09e-138">NOTES</span></span>

## <span data-ttu-id="fc09e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc09e-139">RELATED LINKS</span></span>
