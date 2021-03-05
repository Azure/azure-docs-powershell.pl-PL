---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c205354b68def88b00fb67959669633d5ba1fc1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999978"
---
# <span data-ttu-id="51aec-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="51aec-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="51aec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51aec-102">SYNOPSIS</span></span>
<span data-ttu-id="51aec-103">Zatwierdza zestaw zasobów uwzględniony w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="51aec-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="51aec-104">Operacja zatwierdzania jest wyzwalana dla operacji moveResources w operacji moveState "CommitPending" lub "CommitFailed" po pomyślnym ukończeniu operacji moveResource moveState przejście do stanu Zatwierdzone.</span><span class="sxs-lookup"><span data-stu-id="51aec-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="51aec-105">Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.</span><span class="sxs-lookup"><span data-stu-id="51aec-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="51aec-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="51aec-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="51aec-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="51aec-107">DESCRIPTION</span></span>
<span data-ttu-id="51aec-108">Zatwierdza zestaw zasobów uwzględniony w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="51aec-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="51aec-109">Operacja zatwierdzania jest wyzwalana dla operacji moveResources w operacji moveState "CommitPending" lub "CommitFailed" po pomyślnym ukończeniu operacji moveResource moveState przejście do stanu Zatwierdzone.</span><span class="sxs-lookup"><span data-stu-id="51aec-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="51aec-110">Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.</span><span class="sxs-lookup"><span data-stu-id="51aec-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="51aec-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="51aec-111">EXAMPLES</span></span>

### <span data-ttu-id="51aec-112">Przykład 1. Sprawdź poprawność zależności przed zatwierdzeniem zasobów.</span><span class="sxs-lookup"><span data-stu-id="51aec-112">Example 1: Validate the dependecies before commit of the resources.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:38:26 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/c194298b-b2eb-4aab-80b4-129d1473b75c
Message        : 
Name           : c194298b-b2eb-4aab-80b4-129d1473b75c
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:38:25 PM
Status         : Succeeded

```

<span data-ttu-id="51aec-113">Sprawdź poprawność zależności przed zatwierdzeniem zasobów.</span><span class="sxs-lookup"><span data-stu-id="51aec-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="51aec-114">Przykład 2. Zatwierdzenie zestawu zasobów w zbiorze przenoszenia przy użyciu jako danych wejściowych "MoveResource Name".</span><span class="sxs-lookup"><span data-stu-id="51aec-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemorm-vnet') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:41:13 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/80c04850-7f3f-4e9c-aa68-b868978b59f3
Message        : 
Name           : 80c04850-7f3f-4e9c-aa68-b868978b59f3
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:41:05 PM
Status         : Succeeded


```

<span data-ttu-id="51aec-115">Zatwierdzanie zestawu zasobów w kolekcji przenoszenia przy użyciu wartości "MoveResource Name" jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="51aec-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="51aec-116">Przykład 3. Zatwierdzenie zestawu zasobów w zbiorze przenoszenia przy użyciu funkcji "SourceARMID" jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="51aec-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:42:46 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/d36ca519-8ced-48c9-a968-cb5e9c4db731
Message        : 
Name           : d36ca519-8ced-48c9-a968-cb5e9c4db731
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:42:41 PM
Status         : Succeeded


```

<span data-ttu-id="51aec-117">Zatwierdzanie zestawu zasobów w kolekcji przenoszenia przy użyciu jako danych wejściowych "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="51aec-117">Commit the set of resources in the Move Collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="51aec-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51aec-118">PARAMETERS</span></span>

### <span data-ttu-id="51aec-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="51aec-119">-AsJob</span></span>
<span data-ttu-id="51aec-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="51aec-120">Run the command as a job</span></span>

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

### <span data-ttu-id="51aec-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51aec-121">-DefaultProfile</span></span>
<span data-ttu-id="51aec-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="51aec-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51aec-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="51aec-123">-MoveCollectionName</span></span>
<span data-ttu-id="51aec-124">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="51aec-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="51aec-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="51aec-125">-MoveResource</span></span>
<span data-ttu-id="51aec-126">Pobiera lub ustawia listę identyfikatorów zasobów, domyślnie akceptuje przenoszenie identyfikatorów zasobów, chyba że typ wejściowy zostanie przełączony za pomocą właściwości moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="51aec-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="51aec-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="51aec-127">-MoveResourceInputType</span></span>
<span data-ttu-id="51aec-128">Definiuje typ danych wejściowych zasobu przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="51aec-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="51aec-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="51aec-129">-NoWait</span></span>
<span data-ttu-id="51aec-130">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="51aec-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="51aec-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51aec-131">-ResourceGroupName</span></span>
<span data-ttu-id="51aec-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="51aec-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="51aec-133">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51aec-133">-SubscriptionId</span></span>
<span data-ttu-id="51aec-134">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="51aec-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="51aec-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="51aec-135">-ValidateOnly</span></span>
<span data-ttu-id="51aec-136">Pobiera lub ustawia wartość wskazującą, czy operacja wymaga tylko wstępnego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="51aec-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="51aec-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="51aec-137">-Confirm</span></span>
<span data-ttu-id="51aec-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="51aec-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51aec-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51aec-139">-WhatIf</span></span>
<span data-ttu-id="51aec-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51aec-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51aec-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="51aec-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51aec-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51aec-142">CommonParameters</span></span>
<span data-ttu-id="51aec-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51aec-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51aec-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51aec-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51aec-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51aec-145">INPUTS</span></span>

## <span data-ttu-id="51aec-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51aec-146">OUTPUTS</span></span>

### <span data-ttu-id="51aec-147">Microsoft.Azure.PowerShell.cmdlet.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="51aec-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="51aec-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="51aec-148">NOTES</span></span>

<span data-ttu-id="51aec-149">ALIASY</span><span class="sxs-lookup"><span data-stu-id="51aec-149">ALIASES</span></span>

## <span data-ttu-id="51aec-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51aec-150">RELATED LINKS</span></span>

