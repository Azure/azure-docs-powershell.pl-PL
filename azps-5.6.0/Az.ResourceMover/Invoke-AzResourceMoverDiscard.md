---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: 5e54501e6337943561489a80adf4e8789a55a394
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999953"
---
# <span data-ttu-id="272ee-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="272ee-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="272ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="272ee-102">SYNOPSIS</span></span>
<span data-ttu-id="272ee-103">Odrzuca zestaw zasobów uwzględniony w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="272ee-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="272ee-104">Operacja odrzucania jest wyzwalana dla operacji moveResources w operacji moveState "CommitPending" lub "DiscardFailed" po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do operacji MovePending.</span><span class="sxs-lookup"><span data-stu-id="272ee-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="272ee-105">Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.</span><span class="sxs-lookup"><span data-stu-id="272ee-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="272ee-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="272ee-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="272ee-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="272ee-107">DESCRIPTION</span></span>
<span data-ttu-id="272ee-108">Odrzuca zestaw zasobów uwzględniony w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="272ee-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="272ee-109">Operacja odrzucania jest wyzwalana dla operacji moveResources w operacji moveState "CommitPending" lub "DiscardFailed" po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do operacji MovePending.</span><span class="sxs-lookup"><span data-stu-id="272ee-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="272ee-110">Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.</span><span class="sxs-lookup"><span data-stu-id="272ee-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="272ee-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="272ee-111">EXAMPLES</span></span>

### <span data-ttu-id="272ee-112">Przykład 1. Sprawdzanie zależności przed odrzuceniem zasobów.</span><span class="sxs-lookup"><span data-stu-id="272ee-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:39:48 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/095f3d5
                 1-ebd1-4c5b-9a65-d78ebe3ac345
Message        : 
Name           : 095f3d51-ebd1-4c5b-9a65-d78ebe3ac345
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:39:37 PM
Status         : Succeeded

```

<span data-ttu-id="272ee-113">Sprawdź poprawność zależności przed odrzuceniem zasobów.</span><span class="sxs-lookup"><span data-stu-id="272ee-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="272ee-114">Przykład 2. Odrzuca przeniesienie zasobów przy użyciu wartości "MoveResource Name" jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="272ee-114">Example 2: Discards the move of the resources using "MoveResource Name" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:56:33 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/290472e3-c8de-4c55-aba1-3a34a7a4ab38
Message        : 
Name           : 290472e3-c8de-4c55-aba1-3a34a7a4ab38
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:55:21 PM
Status         : Succeeded

```

<span data-ttu-id="272ee-115">Odrzuca przeniesienie zasobów przy użyciu jako danych wejściowych "MoveResource Name".</span><span class="sxs-lookup"><span data-stu-id="272ee-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="272ee-116">Przykład 3. Odrzuca przeniesienie zasobów przy użyciu funkcji "SourceARMID" jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="272ee-116">Example 3: Discards the move of the resources using "SourceARMID" as input.</span></span>
```powershell
PS C:\>  Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:01:32 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/955fd43c-10b6-481e-888b-d26d6ec42aea
Message        : 
Name           : 955fd43c-10b6-481e-888b-d26d6ec42aea
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:00:00 PM
Status         : Succeeded


```

<span data-ttu-id="272ee-117">Odrzuca przeniesienie zasobów przy użyciu funkcji "SourceARMID" jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="272ee-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="272ee-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="272ee-118">PARAMETERS</span></span>

### <span data-ttu-id="272ee-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="272ee-119">-AsJob</span></span>
<span data-ttu-id="272ee-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="272ee-120">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272ee-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="272ee-121">-DefaultProfile</span></span>
<span data-ttu-id="272ee-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="272ee-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272ee-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="272ee-123">-MoveResource</span></span>
<span data-ttu-id="272ee-124">Pobiera lub ustawia listę identyfikatorów zasobów, domyślnie akceptuje przenoszenie identyfikatorów zasobów, chyba że typ wejściowy zostanie przełączony za pomocą właściwości moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="272ee-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272ee-125">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="272ee-125">-MoveResourceInputType</span></span>
<span data-ttu-id="272ee-126">Definiuje typ danych wejściowych zasobu przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="272ee-126">Defines the move resource input type.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Support.MoveResourceInputType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272ee-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="272ee-127">-Name</span></span>
<span data-ttu-id="272ee-128">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="272ee-128">The Move Collection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveCollectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272ee-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="272ee-129">-NoWait</span></span>
<span data-ttu-id="272ee-130">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="272ee-130">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272ee-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="272ee-131">-ResourceGroupName</span></span>
<span data-ttu-id="272ee-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="272ee-132">The Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272ee-133">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="272ee-133">-SubscriptionId</span></span>
<span data-ttu-id="272ee-134">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="272ee-134">The Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272ee-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="272ee-135">-ValidateOnly</span></span>
<span data-ttu-id="272ee-136">Pobiera lub ustawia wartość wskazującą, czy operacja wymaga tylko wstępnego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="272ee-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272ee-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="272ee-137">-Confirm</span></span>
<span data-ttu-id="272ee-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="272ee-138">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272ee-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="272ee-139">-WhatIf</span></span>
<span data-ttu-id="272ee-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="272ee-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="272ee-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="272ee-141">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="272ee-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="272ee-142">CommonParameters</span></span>
<span data-ttu-id="272ee-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="272ee-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="272ee-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="272ee-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="272ee-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="272ee-145">INPUTS</span></span>

## <span data-ttu-id="272ee-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="272ee-146">OUTPUTS</span></span>

### <span data-ttu-id="272ee-147">Microsoft.Azure.PowerShell.cmdlet.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="272ee-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="272ee-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="272ee-148">NOTES</span></span>

<span data-ttu-id="272ee-149">ALIASY</span><span class="sxs-lookup"><span data-stu-id="272ee-149">ALIASES</span></span>

## <span data-ttu-id="272ee-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="272ee-150">RELATED LINKS</span></span>

