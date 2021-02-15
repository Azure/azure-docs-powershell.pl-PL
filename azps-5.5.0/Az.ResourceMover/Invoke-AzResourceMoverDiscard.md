---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: c4af588c119cb819fcb87fbc7dbdd869540825ce
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201891"
---
# <span data-ttu-id="8d52a-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="8d52a-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="8d52a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8d52a-102">SYNOPSIS</span></span>
<span data-ttu-id="8d52a-103">Odrzuca zestaw zasobów uwzględniony w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="8d52a-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="8d52a-104">Operacja odrzucania jest wyzwalana dla operacji moveResources w operacji moveState "CommitPending" lub "DiscardFailed" po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do operacji MovePending.</span><span class="sxs-lookup"><span data-stu-id="8d52a-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="8d52a-105">Aby pomóc użytkownikowi wstępnie skonfigurować operację, klient może wywołać operację z ustawioną tylko wartością validateOnly property ustawioną na true.</span><span class="sxs-lookup"><span data-stu-id="8d52a-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="8d52a-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8d52a-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8d52a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="8d52a-107">DESCRIPTION</span></span>
<span data-ttu-id="8d52a-108">Odrzuca zestaw zasobów uwzględniony w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="8d52a-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="8d52a-109">Operacja odrzucania jest wyzwalana dla operacji moveResources w operacji moveState "CommitPending" lub "DiscardFailed" po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do operacji MovePending.</span><span class="sxs-lookup"><span data-stu-id="8d52a-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="8d52a-110">Aby pomóc użytkownikowi wstępnie skonfigurować operację, klient może wywołać operację z ustawioną tylko wartością validateOnly property ustawioną na true.</span><span class="sxs-lookup"><span data-stu-id="8d52a-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="8d52a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8d52a-111">EXAMPLES</span></span>

### <span data-ttu-id="8d52a-112">Przykład 1. Sprawdzanie zależności przed odrzuceniem zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d52a-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') -ValidateOnly

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 9:44:54 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/62861ceb-28c9-4e0c-811b-84692a203181
Message        :
Name           : 62861ceb-28c9-4e0c-811b-84692a203181
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 9:44:54 AM
Status         : Succeeded

```

<span data-ttu-id="8d52a-113">Sprawdź poprawność zależności przed odrzuceniem zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d52a-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="8d52a-114">Przykład 2. Odrzuca przeniesienie zasobów przy użyciu wartości "MoveResource Name" jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="8d52a-114">Example 2: Discards the move of the resources using "MoveResource Name" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverDiscard -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:26:51 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/21f99cd3-89a4-4fcb-8b96-40d0572a6377
Message        :
Name           : 21f99cd3-89a4-4fcb-8b96-40d0572a6377
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:26:39 AM
Status         : Succeeded

```

<span data-ttu-id="8d52a-115">Odrzuca przeniesienie zasobów przy użyciu jako danych wejściowych "MoveResource Name".</span><span class="sxs-lookup"><span data-stu-id="8d52a-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="8d52a-116">Przykład 3. Odrzuca przeniesienie zasobów przy użyciu funkcji "SourceARMID" jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="8d52a-116">Example 3: Discards the move of the resources using "SourceARMID" as input</span></span>
```powershell
PS C:\>  Invoke-AzResourceMoverDiscard -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:33:37 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/b842efcd-e5fd-42b0-a277-01ee8225deed
Message        :
Name           : b842efcd-e5fd-42b0-a277-01ee8225deed
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:33:23 AM
Status         : Succeeded


```

<span data-ttu-id="8d52a-117">Odrzuca przeniesienie zasobów przy użyciu funkcji "SourceARMID" jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="8d52a-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="8d52a-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8d52a-118">PARAMETERS</span></span>

### <span data-ttu-id="8d52a-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8d52a-119">-AsJob</span></span>
<span data-ttu-id="8d52a-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="8d52a-120">Run the command as a job</span></span>

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

### <span data-ttu-id="8d52a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8d52a-121">-DefaultProfile</span></span>
<span data-ttu-id="8d52a-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8d52a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8d52a-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="8d52a-123">-MoveResource</span></span>
<span data-ttu-id="8d52a-124">Pobiera lub ustawia listę identyfikatorów zasobów, domyślnie akceptuje przenoszenie identyfikatorów zasobów, chyba że typ wejściowy zostanie przełączony za pomocą właściwości moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="8d52a-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="8d52a-125">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="8d52a-125">-MoveResourceInputType</span></span>
<span data-ttu-id="8d52a-126">Definiuje typ danych wejściowych zasobu przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="8d52a-126">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="8d52a-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8d52a-127">-Name</span></span>
<span data-ttu-id="8d52a-128">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="8d52a-128">The Move Collection Name.</span></span>

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

### <span data-ttu-id="8d52a-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8d52a-129">-NoWait</span></span>
<span data-ttu-id="8d52a-130">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="8d52a-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8d52a-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8d52a-131">-ResourceGroupName</span></span>
<span data-ttu-id="8d52a-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8d52a-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="8d52a-133">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8d52a-133">-SubscriptionId</span></span>
<span data-ttu-id="8d52a-134">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8d52a-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="8d52a-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="8d52a-135">-ValidateOnly</span></span>
<span data-ttu-id="8d52a-136">Pobiera lub ustawia wartość wskazującą, czy operacja wymaga tylko wstępnego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="8d52a-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="8d52a-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8d52a-137">-Confirm</span></span>
<span data-ttu-id="8d52a-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8d52a-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8d52a-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8d52a-139">-WhatIf</span></span>
<span data-ttu-id="8d52a-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8d52a-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8d52a-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8d52a-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8d52a-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8d52a-142">CommonParameters</span></span>
<span data-ttu-id="8d52a-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8d52a-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8d52a-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8d52a-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8d52a-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d52a-145">INPUTS</span></span>

## <span data-ttu-id="8d52a-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8d52a-146">OUTPUTS</span></span>

### <span data-ttu-id="8d52a-147">Microsoft.Azure.PowerShell.cmdlet.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="8d52a-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="8d52a-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8d52a-148">NOTES</span></span>

<span data-ttu-id="8d52a-149">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8d52a-149">ALIASES</span></span>

## <span data-ttu-id="8d52a-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8d52a-150">RELATED LINKS</span></span>

