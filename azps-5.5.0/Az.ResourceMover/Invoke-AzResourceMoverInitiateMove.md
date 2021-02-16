---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: c1942358ea438d596afc3f147e65a894b270f0d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186530"
---
# <span data-ttu-id="edcc9-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="edcc9-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="edcc9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edcc9-102">SYNOPSIS</span></span>
<span data-ttu-id="edcc9-103">Przenosi zestaw zasobów uwzględniony w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="edcc9-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="edcc9-104">Operacja przenoszenia jest wyzwalana po tym, jak moveResources znajdują się w stanie moveState "MovePending" lub "MoveFailed", po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do commitPending.</span><span class="sxs-lookup"><span data-stu-id="edcc9-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="edcc9-105">Aby pomóc użytkownikowi wstępnie skonfigurować operację, klient może wywołać operację z ustawioną tylko wartością validateOnly property ustawioną na true.</span><span class="sxs-lookup"><span data-stu-id="edcc9-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="edcc9-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="edcc9-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="edcc9-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="edcc9-107">DESCRIPTION</span></span>
<span data-ttu-id="edcc9-108">Przenosi zestaw zasobów uwzględniony w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="edcc9-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="edcc9-109">Operacja przenoszenia jest wyzwalana po tym, jak moveResources znajdują się w stanie moveState "MovePending" lub "MoveFailed", po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do commitPending.</span><span class="sxs-lookup"><span data-stu-id="edcc9-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="edcc9-110">Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.</span><span class="sxs-lookup"><span data-stu-id="edcc9-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="edcc9-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="edcc9-111">EXAMPLES</span></span>

### <span data-ttu-id="edcc9-112">Przykład 1. Sprawdzanie poprawności zależności przed zainicjowanie przeniesienia zasobów.</span><span class="sxs-lookup"><span data-stu-id="edcc9-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg')  -ValidateOnly


AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:07:36 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Message        :
Name           : 8d6fbc01-9e5f-4a62-9bd7-03c18bd770f2
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:07:35 AM
Status         : Succeeded

```

<span data-ttu-id="edcc9-113">Sprawdź poprawność zależności przed zainicjowanie przeniesienia zasobów.</span><span class="sxs-lookup"><span data-stu-id="edcc9-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="edcc9-114">Przykład 2. Inicjowanie przenoszenia zestawu zasobów w kolekcji przenoszenia przy użyciu jako danych wejściowych "MoveResource Name"</span><span class="sxs-lookup"><span data-stu-id="edcc9-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM  -MoveResource $('PSDemoVM-nsg') 

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:24:21 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/bc30d933-c2b6-47c9-b583-240d375b5864
Message        :
Name           : bc30d933-c2b6-47c9-b583-240d375b5864
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:24:21 AM
Status         : Succeeded

```

<span data-ttu-id="edcc9-115">Zainicjuj przenoszenie zestawu zasobów w kolekcji przenoszenia, używając jako danych wejściowych "MoveResource Name".</span><span class="sxs-lookup"><span data-stu-id="edcc9-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="edcc9-116">Przykład 3. Inicjowanie przenoszenia zestawu zasobów w kolekcji przenoszenia przy użyciu wartości wejściowej "SourceARMID"</span><span class="sxs-lookup"><span data-stu-id="edcc9-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverInitiateMove -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:38:33 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/cbc0f921-de9b-45d5-91da-60e36b841b10
Message        :
Name           : cbc0f921-de9b-45d5-91da-60e36b841b10
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:37:23 AM
Status         : Succeeded

```

<span data-ttu-id="edcc9-117">Zainicjuj przenoszenie zestawu zasobów w kolekcji Przenoszenia, używając jako danych wejściowych "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="edcc9-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="edcc9-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edcc9-118">PARAMETERS</span></span>

### <span data-ttu-id="edcc9-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="edcc9-119">-AsJob</span></span>
<span data-ttu-id="edcc9-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="edcc9-120">Run the command as a job</span></span>

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

### <span data-ttu-id="edcc9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edcc9-121">-DefaultProfile</span></span>
<span data-ttu-id="edcc9-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="edcc9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edcc9-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="edcc9-123">-MoveCollectionName</span></span>
<span data-ttu-id="edcc9-124">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="edcc9-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="edcc9-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="edcc9-125">-MoveResource</span></span>
<span data-ttu-id="edcc9-126">Pobiera lub ustawia listę identyfikatorów zasobów, domyślnie akceptuje przenoszenie identyfikatorów zasobów, chyba że typ wejściowy zostanie przełączony za pomocą właściwości moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="edcc9-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="edcc9-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="edcc9-127">-MoveResourceInputType</span></span>
<span data-ttu-id="edcc9-128">Definiuje typ danych wejściowych zasobu przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="edcc9-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="edcc9-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="edcc9-129">-NoWait</span></span>
<span data-ttu-id="edcc9-130">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="edcc9-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="edcc9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="edcc9-131">-ResourceGroupName</span></span>
<span data-ttu-id="edcc9-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="edcc9-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="edcc9-133">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="edcc9-133">-SubscriptionId</span></span>
<span data-ttu-id="edcc9-134">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="edcc9-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="edcc9-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="edcc9-135">-ValidateOnly</span></span>
<span data-ttu-id="edcc9-136">Pobiera lub ustawia wartość wskazującą, czy operacja wymaga tylko wstępnego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="edcc9-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="edcc9-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="edcc9-137">-Confirm</span></span>
<span data-ttu-id="edcc9-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="edcc9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="edcc9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="edcc9-139">-WhatIf</span></span>
<span data-ttu-id="edcc9-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="edcc9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="edcc9-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="edcc9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="edcc9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edcc9-142">CommonParameters</span></span>
<span data-ttu-id="edcc9-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="edcc9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edcc9-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="edcc9-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edcc9-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="edcc9-145">INPUTS</span></span>

## <span data-ttu-id="edcc9-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="edcc9-146">OUTPUTS</span></span>

### <span data-ttu-id="edcc9-147">Microsoft.Azure.PowerShell.cmdlet.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="edcc9-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="edcc9-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="edcc9-148">NOTES</span></span>

<span data-ttu-id="edcc9-149">ALIASY</span><span class="sxs-lookup"><span data-stu-id="edcc9-149">ALIASES</span></span>

## <span data-ttu-id="edcc9-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="edcc9-150">RELATED LINKS</span></span>

