---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemovercommit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverCommit.md
ms.openlocfilehash: 9c0ee11b728c3fd8b1ed2b73e8b144728255a009
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98377876"
---
# <span data-ttu-id="8f6d2-101">Invoke-AzResourceMoverCommit</span><span class="sxs-lookup"><span data-stu-id="8f6d2-101">Invoke-AzResourceMoverCommit</span></span>

## <span data-ttu-id="8f6d2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8f6d2-102">SYNOPSIS</span></span>
<span data-ttu-id="8f6d2-103">Zatwierdza zbiór zasobów uwzględnionych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="8f6d2-103">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="8f6d2-104">Operacja Zatwierdź jest wyzwalana na moveResources w moveState "CommitPending" lub "CommitFailed", po poprawnym zakończeniu, moveResource moveState to przejście do zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="8f6d2-104">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="8f6d2-105">Aby pomóc użytkownikowi na wstępną konieczność działania, z którym klient może nawiązać operację, należy ustawić właściwość validateOnly równą true.</span><span class="sxs-lookup"><span data-stu-id="8f6d2-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="8f6d2-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8f6d2-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverCommit -MoveCollectionName <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8f6d2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8f6d2-107">DESCRIPTION</span></span>
<span data-ttu-id="8f6d2-108">Zatwierdza zbiór zasobów uwzględnionych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="8f6d2-108">Commits the set of resources included in the request body.</span></span>
<span data-ttu-id="8f6d2-109">Operacja Zatwierdź jest wyzwalana na moveResources w moveState "CommitPending" lub "CommitFailed", po poprawnym zakończeniu, moveResource moveState to przejście do zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="8f6d2-109">The commit operation is triggered on the moveResources in the moveState 'CommitPending' or 'CommitFailed', on a successful completion the moveResource moveState do a transition to Committed.</span></span>
<span data-ttu-id="8f6d2-110">Aby pomóc użytkownikowi na wstępną konieczność działania, z którym klient może nawiązać operację, należy ustawić właściwość validateOnly równą true.</span><span class="sxs-lookup"><span data-stu-id="8f6d2-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="8f6d2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8f6d2-111">EXAMPLES</span></span>

### <span data-ttu-id="8f6d2-112">Przykład 1. Sprawdź poprawność dependecies przed zatwierdzeniem zasobów</span><span class="sxs-lookup"><span data-stu-id="8f6d2-112">Example 1: Validate the dependecies before commit of the resources</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResource $('psdemorm') -ValidateOnly


AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:17:00 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Message        :
Name           : 5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:16:59 AM
Status         : Succeeded

```

<span data-ttu-id="8f6d2-113">Sprawdź poprawność dependecies przed zatwierdzeniem zasobów.</span><span class="sxs-lookup"><span data-stu-id="8f6d2-113">Validate the dependecies before commit of the resources.</span></span>

### <span data-ttu-id="8f6d2-114">Przykład 2: zatwierdzanie zestawu zasobów w kolekcji Move przy użyciu funkcji "MoveResource Name" jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="8f6d2-114">Example 2: Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
```powershell
PS C:\>Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResource $('psdemorm')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:17:00 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Message        :
Name           : 5524d3f4-dd47-4572-9d8d-c62d3b513ee0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:16:59 AM
Status         : Succeeded


```

<span data-ttu-id="8f6d2-115">Zatwierdzanie zestawu zasobów w kolekcji Move przy użyciu funkcji "MoveResource Name" jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="8f6d2-115">Commit the set of resources in the Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="8f6d2-116">Przykład 3: zatwierdzanie zestawu zasobów w kolekcji Move przy użyciu funkcji "SourceARMID" jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="8f6d2-116">Example 3: Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverCommit -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/PSDemoRM')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 8/21/2020 6:19:29 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRM/operations/aa9e2c4d-2160-4e36-b6fa-7465a3829ae9
Message        :
Name           : aa9e2c4d-2160-4e36-b6fa-7465a3829ae9
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/21/2020 6:19:28 AM
Status         : Succeeded


```

<span data-ttu-id="8f6d2-117">Zatwierdzanie zestawu zasobów w kolekcji przenoszenia przy użyciu danych wejściowych "SourceARMID"</span><span class="sxs-lookup"><span data-stu-id="8f6d2-117">Commit the set of resources in the Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="8f6d2-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8f6d2-118">PARAMETERS</span></span>

### <span data-ttu-id="8f6d2-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8f6d2-119">-AsJob</span></span>
<span data-ttu-id="8f6d2-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="8f6d2-120">Run the command as a job</span></span>

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

### <span data-ttu-id="8f6d2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f6d2-121">-DefaultProfile</span></span>
<span data-ttu-id="8f6d2-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f6d2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f6d2-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="8f6d2-123">-MoveCollectionName</span></span>
<span data-ttu-id="8f6d2-124">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="8f6d2-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="8f6d2-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="8f6d2-125">-MoveResource</span></span>
<span data-ttu-id="8f6d2-126">Pobiera lub ustawia listę identyfikatorów zasobów domyślnie przyjmuje identyfikator "Przenieś zasób", chyba że typ wejściowy zostanie przełączony za pomocą właściwości moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="8f6d2-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="8f6d2-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="8f6d2-127">-MoveResourceInputType</span></span>
<span data-ttu-id="8f6d2-128">Określa typ wejścia zasobu do przeniesienia.</span><span class="sxs-lookup"><span data-stu-id="8f6d2-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="8f6d2-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8f6d2-129">-NoWait</span></span>
<span data-ttu-id="8f6d2-130">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="8f6d2-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8f6d2-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f6d2-131">-ResourceGroupName</span></span>
<span data-ttu-id="8f6d2-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8f6d2-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="8f6d2-133">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8f6d2-133">-SubscriptionId</span></span>
<span data-ttu-id="8f6d2-134">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="8f6d2-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="8f6d2-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="8f6d2-135">-ValidateOnly</span></span>
<span data-ttu-id="8f6d2-136">Pobiera lub ustawia wartość wskazującą, czy operacja wymaga tylko wymagania wstępnego.</span><span class="sxs-lookup"><span data-stu-id="8f6d2-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="8f6d2-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8f6d2-137">-Confirm</span></span>
<span data-ttu-id="8f6d2-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f6d2-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f6d2-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f6d2-139">-WhatIf</span></span>
<span data-ttu-id="8f6d2-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f6d2-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f6d2-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8f6d2-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f6d2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f6d2-142">CommonParameters</span></span>
<span data-ttu-id="8f6d2-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f6d2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f6d2-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f6d2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f6d2-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f6d2-145">INPUTS</span></span>

## <span data-ttu-id="8f6d2-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8f6d2-146">OUTPUTS</span></span>

### <span data-ttu-id="8f6d2-147">Microsoft. Azure. PowerShell. polecenia. ResourceMover. models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="8f6d2-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="8f6d2-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8f6d2-148">NOTES</span></span>

<span data-ttu-id="8f6d2-149">PISUJE</span><span class="sxs-lookup"><span data-stu-id="8f6d2-149">ALIASES</span></span>

## <span data-ttu-id="8f6d2-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f6d2-150">RELATED LINKS</span></span>

