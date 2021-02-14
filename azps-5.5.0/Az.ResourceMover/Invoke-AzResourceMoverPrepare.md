---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 86e8cc42b10cb79216bd0252c02c6756a9d16af6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183722"
---
# <span data-ttu-id="1db68-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="1db68-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="1db68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1db68-102">SYNOPSIS</span></span>
<span data-ttu-id="1db68-103">Inicjuje przygotowywanie zestawu zasobów zawartych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="1db68-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="1db68-104">Operacja przygotowywania znajduje się na stronie moveResources, które znajdują się w operacji moveState "PreparePending" lub "PrepareFailed", po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do operacji MovePending.</span><span class="sxs-lookup"><span data-stu-id="1db68-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="1db68-105">Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.</span><span class="sxs-lookup"><span data-stu-id="1db68-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="1db68-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1db68-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1db68-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1db68-107">DESCRIPTION</span></span>
<span data-ttu-id="1db68-108">Inicjuje przygotowywanie zestawu zasobów zawartych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="1db68-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="1db68-109">Operacja przygotowywania znajduje się na stronie moveResources, które znajdują się w operacji moveState "PreparePending" lub "PrepareFailed", po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do operacji MovePending.</span><span class="sxs-lookup"><span data-stu-id="1db68-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="1db68-110">Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.</span><span class="sxs-lookup"><span data-stu-id="1db68-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="1db68-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1db68-111">EXAMPLES</span></span>

### <span data-ttu-id="1db68-112">Przykład 1. Sprawdzanie poprawność zależności przed przygotowaniem się na zasoby</span><span class="sxs-lookup"><span data-stu-id="1db68-112">Example 1: Validate the dependecies before prepare for the resources</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm') -ValidateOnly

AdditionalInfo : {Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationErrorAdditionalInfo}
Code           : MoveCollectionMissingRequiredDependentResources
Detail         : {}
EndTime        : 8/21/2020 6:04:15 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RegionMoveRG-centralus-westcentralus/providers/Microsoft.Migr
                 ate/MoveCollections/MoveCollection-cus-wcus-eus2/operations/12d055bd-ac52-427f-8b05-b4b21c4b51e8
Message        : The operation has failed as required move resources are missing from the input.
                     Possible Causes: Dependent resources are missing from the input.
                     Recommended Action: Retry the operation with all required resources, if the issue persist contact support.

Name           : 12d055bd-ac52-427f-8b05-b4b21c4b51e8
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:04:14 AM
Status         : Failed

```

<span data-ttu-id="1db68-113">Sprawdź poprawność zależności przed przygotowaniem się na zasoby.</span><span class="sxs-lookup"><span data-stu-id="1db68-113">Validate the dependecies before prepare for the resources.</span></span>

### <span data-ttu-id="1db68-114">Przykład 2. Inicjowanie przygotowywania zestawu zasobów w kolekcji przenoszenia przy użyciu jako danych wejściowych "MoveResource Name"</span><span class="sxs-lookup"><span data-stu-id="1db68-114">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName "PS-centralus-westcentralus-demoRM"  -MoveResource $('psdemovm','psdemovm62', 'PSDemoVM-ip', 'PSDemoRM-vnet','PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/19/2020 6:18:09 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/da65e9c7-7fb9-44ef-af99-6f65b21e9951
Message        :
Name           : da65e9c7-7fb9-44ef-af99-6f65b21e9951
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/19/2020 6:18:08 AM
Status         : Succeeded
```

<span data-ttu-id="1db68-115">Zainicjuj przygotowywanie zestawu zasobów w kolekcji przenoszenia, używając jako danych wejściowych "MoveResource Name".</span><span class="sxs-lookup"><span data-stu-id="1db68-115">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="1db68-116">Przykład 3. Zainicjuj przygotowywanie zestawu zasobów w kolekcji przenoszenia przy użyciu funkcji "SourceARMID"</span><span class="sxs-lookup"><span data-stu-id="1db68-116">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID"</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 5:35:30 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Message        :
Name           : c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 5:35:27 AM
Status         : Succeeded

```

<span data-ttu-id="1db68-117">Zainicjuj przygotowywanie zestawu zasobów w kolekcji przenoszenia za pomocą pliku "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="1db68-117">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="1db68-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1db68-118">PARAMETERS</span></span>

### <span data-ttu-id="1db68-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1db68-119">-AsJob</span></span>
<span data-ttu-id="1db68-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="1db68-120">Run the command as a job</span></span>

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

### <span data-ttu-id="1db68-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1db68-121">-DefaultProfile</span></span>
<span data-ttu-id="1db68-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1db68-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1db68-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="1db68-123">-MoveCollectionName</span></span>
<span data-ttu-id="1db68-124">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="1db68-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="1db68-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="1db68-125">-MoveResource</span></span>
<span data-ttu-id="1db68-126">Pobiera lub ustawia listę identyfikatorów zasobów, domyślnie akceptuje przenoszenie identyfikatorów zasobów, chyba że typ wejściowy zostanie przełączony za pomocą właściwości moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="1db68-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="1db68-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="1db68-127">-MoveResourceInputType</span></span>
<span data-ttu-id="1db68-128">Definiuje typ danych wejściowych zasobu przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="1db68-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="1db68-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1db68-129">-NoWait</span></span>
<span data-ttu-id="1db68-130">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="1db68-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1db68-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1db68-131">-ResourceGroupName</span></span>
<span data-ttu-id="1db68-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1db68-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="1db68-133">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1db68-133">-SubscriptionId</span></span>
<span data-ttu-id="1db68-134">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1db68-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="1db68-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="1db68-135">-ValidateOnly</span></span>
<span data-ttu-id="1db68-136">Pobiera lub ustawia wartość wskazującą, czy operacja wymaga tylko wstępnego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="1db68-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="1db68-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1db68-137">-Confirm</span></span>
<span data-ttu-id="1db68-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1db68-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1db68-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1db68-139">-WhatIf</span></span>
<span data-ttu-id="1db68-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1db68-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1db68-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1db68-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1db68-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1db68-142">CommonParameters</span></span>
<span data-ttu-id="1db68-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1db68-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1db68-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1db68-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1db68-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1db68-145">INPUTS</span></span>

## <span data-ttu-id="1db68-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1db68-146">OUTPUTS</span></span>

### <span data-ttu-id="1db68-147">Microsoft.Azure.PowerShell.cmdlet.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="1db68-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="1db68-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1db68-148">NOTES</span></span>

<span data-ttu-id="1db68-149">ALIASY</span><span class="sxs-lookup"><span data-stu-id="1db68-149">ALIASES</span></span>

## <span data-ttu-id="1db68-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1db68-150">RELATED LINKS</span></span>

