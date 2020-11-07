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
ms.locfileid: "93710668"
---
# <span data-ttu-id="88302-101">Resume-AzsUpdateRun</span><span class="sxs-lookup"><span data-stu-id="88302-101">Resume-AzsUpdateRun</span></span>

## <span data-ttu-id="88302-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88302-102">SYNOPSIS</span></span>
<span data-ttu-id="88302-103">Umożliwia wznowienie uruchomionego wcześniej uruchomienia aktualizacji, którego nie udało się wykonać.</span><span class="sxs-lookup"><span data-stu-id="88302-103">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="88302-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88302-104">SYNTAX</span></span>

### <span data-ttu-id="88302-105">UpdateRuns_Rerun (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="88302-105">UpdateRuns_Rerun (Default)</span></span>
```
Resume-AzsUpdateRun -Name <String> [-Location <String>] [-ResourceGroupName <String>] -UpdateName <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88302-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="88302-106">ResourceId</span></span>
```
Resume-AzsUpdateRun [-AsJob] -ResourceId <String> [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88302-107">Opis</span><span class="sxs-lookup"><span data-stu-id="88302-107">DESCRIPTION</span></span>
<span data-ttu-id="88302-108">Umożliwia wznowienie uruchomionego wcześniej uruchomienia aktualizacji, którego nie udało się wykonać.</span><span class="sxs-lookup"><span data-stu-id="88302-108">Resumes a previously started update run that failed.</span></span> <span data-ttu-id="88302-109">Wznowiony przebieg aktualizacji zostanie wznowiony w momencie ostatniej awarii.</span><span class="sxs-lookup"><span data-stu-id="88302-109">Resumeed update runs will resume at the point they last failed.</span></span>

## <span data-ttu-id="88302-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88302-110">EXAMPLES</span></span>

### <span data-ttu-id="88302-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="88302-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Get-AzsUpdateRun -Name 5173e9f4-3040-494f-b7a7-738a6331d55c -UpdateName Microsoft1.0.180305.1 | Resume-AzsUpdateRun
```

<span data-ttu-id="88302-112">Umożliwia wznowienie uruchomionego wcześniej uruchomienia aktualizacji, którego nie udało się wykonać.</span><span class="sxs-lookup"><span data-stu-id="88302-112">Resumes a previously started update run that failed.</span></span>

## <span data-ttu-id="88302-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88302-113">PARAMETERS</span></span>

### <span data-ttu-id="88302-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88302-114">-AsJob</span></span>
<span data-ttu-id="88302-115">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="88302-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="88302-116">-Force</span><span class="sxs-lookup"><span data-stu-id="88302-116">-Force</span></span>
<span data-ttu-id="88302-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="88302-117">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="88302-118">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="88302-118">-Location</span></span>
<span data-ttu-id="88302-119">Nazwa lokalizacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="88302-119">The name of the update location.</span></span>

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

### <span data-ttu-id="88302-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88302-120">-Name</span></span>
<span data-ttu-id="88302-121">Identyfikator uruchomienia aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="88302-121">Update run identifier.</span></span>

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

### <span data-ttu-id="88302-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88302-122">-ResourceGroupName</span></span>
<span data-ttu-id="88302-123">Grupa zasobów, w której znajduje się zasób.</span><span class="sxs-lookup"><span data-stu-id="88302-123">The resource group the resource is located under.</span></span>

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

### <span data-ttu-id="88302-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="88302-124">-ResourceId</span></span>
<span data-ttu-id="88302-125">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="88302-125">The resource id.</span></span>

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

### <span data-ttu-id="88302-126">-Updatename</span><span class="sxs-lookup"><span data-stu-id="88302-126">-UpdateName</span></span>
<span data-ttu-id="88302-127">Nazwa wyświetlana aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="88302-127">Display name of the update.</span></span>

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

### <span data-ttu-id="88302-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88302-128">-Confirm</span></span>
<span data-ttu-id="88302-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88302-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="88302-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88302-130">-WhatIf</span></span>
<span data-ttu-id="88302-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88302-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88302-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="88302-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="88302-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88302-133">CommonParameters</span></span>
<span data-ttu-id="88302-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88302-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88302-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88302-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88302-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88302-136">INPUTS</span></span>

## <span data-ttu-id="88302-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88302-137">OUTPUTS</span></span>

## <span data-ttu-id="88302-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88302-138">NOTES</span></span>

## <span data-ttu-id="88302-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88302-139">RELATED LINKS</span></span>

