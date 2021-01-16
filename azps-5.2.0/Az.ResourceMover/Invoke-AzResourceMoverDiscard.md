---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverdiscard
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverDiscard.md
ms.openlocfilehash: c4af588c119cb819fcb87fbc7dbdd869540825ce
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98349114"
---
# <span data-ttu-id="e22a9-101">Invoke-AzResourceMoverDiscard</span><span class="sxs-lookup"><span data-stu-id="e22a9-101">Invoke-AzResourceMoverDiscard</span></span>

## <span data-ttu-id="e22a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e22a9-102">SYNOPSIS</span></span>
<span data-ttu-id="e22a9-103">Odrzuca zestaw zasobów uwzględnionych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="e22a9-103">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="e22a9-104">Operacja Odrzuć jest wyzwalana na moveResources w moveState "CommitPending" lub "DiscardFailed", po poprawnym zakończeniu, moveResource moveState, aby przejść do MovePending.</span><span class="sxs-lookup"><span data-stu-id="e22a9-104">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="e22a9-105">Aby pomóc użytkownikowi na wstępną konieczność działania, z którym klient może nawiązać operację, należy ustawić właściwość validateOnly równą true.</span><span class="sxs-lookup"><span data-stu-id="e22a9-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="e22a9-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e22a9-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverDiscard -Name <String> -ResourceGroupName <String> -MoveResource <String[]>
 [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>] [-ValidateOnly]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="e22a9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e22a9-107">DESCRIPTION</span></span>
<span data-ttu-id="e22a9-108">Odrzuca zestaw zasobów uwzględnionych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="e22a9-108">Discards the set of resources included in the request body.</span></span>
<span data-ttu-id="e22a9-109">Operacja Odrzuć jest wyzwalana na moveResources w moveState "CommitPending" lub "DiscardFailed", po poprawnym zakończeniu, moveResource moveState, aby przejść do MovePending.</span><span class="sxs-lookup"><span data-stu-id="e22a9-109">The discard operation is triggered on the moveResources in the moveState 'CommitPending' or 'DiscardFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="e22a9-110">Aby pomóc użytkownikowi na wstępną konieczność działania, z którym klient może nawiązać operację, należy ustawić właściwość validateOnly równą true.</span><span class="sxs-lookup"><span data-stu-id="e22a9-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="e22a9-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e22a9-111">EXAMPLES</span></span>

### <span data-ttu-id="e22a9-112">Przykład 1. Sprawdź poprawność dependecies przed odrzuceniem zasobów.</span><span class="sxs-lookup"><span data-stu-id="e22a9-112">Example 1: Validate the dependecies before Discard of  the resources.</span></span>
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

<span data-ttu-id="e22a9-113">Sprawdź poprawność dependecies przed odrzuceniem zasobów.</span><span class="sxs-lookup"><span data-stu-id="e22a9-113">Validate the dependecies before Discard of  the resources.</span></span>

### <span data-ttu-id="e22a9-114">Przykład 2: odrzucanie przeniesień zasobów przy użyciu funkcji "MoveResource Name" jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="e22a9-114">Example 2: Discards the move of the resources using "MoveResource Name" as input</span></span>
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

<span data-ttu-id="e22a9-115">Odrzucanie przenoszonych zasobów przy użyciu funkcji "MoveResource Name" jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e22a9-115">Discards the move of the resources using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="e22a9-116">Przykład 3: odrzucanie przeniesień zasobów przy użyciu "SourceARMID" jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="e22a9-116">Example 3: Discards the move of the resources using "SourceARMID" as input</span></span>
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

<span data-ttu-id="e22a9-117">Odrzucanie przenoszonych zasobów przy użyciu "SourceARMID" jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e22a9-117">Discards the move of the resources using "SourceARMID" as input.</span></span>

## <span data-ttu-id="e22a9-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e22a9-118">PARAMETERS</span></span>

### <span data-ttu-id="e22a9-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e22a9-119">-AsJob</span></span>
<span data-ttu-id="e22a9-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="e22a9-120">Run the command as a job</span></span>

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

### <span data-ttu-id="e22a9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e22a9-121">-DefaultProfile</span></span>
<span data-ttu-id="e22a9-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e22a9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e22a9-123">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="e22a9-123">-MoveResource</span></span>
<span data-ttu-id="e22a9-124">Pobiera lub ustawia listę identyfikatorów zasobów domyślnie przyjmuje identyfikator "Przenieś zasób", chyba że typ wejściowy zostanie przełączony za pomocą właściwości moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="e22a9-124">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="e22a9-125">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="e22a9-125">-MoveResourceInputType</span></span>
<span data-ttu-id="e22a9-126">Określa typ wejścia zasobu do przeniesienia.</span><span class="sxs-lookup"><span data-stu-id="e22a9-126">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="e22a9-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e22a9-127">-Name</span></span>
<span data-ttu-id="e22a9-128">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="e22a9-128">The Move Collection Name.</span></span>

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

### <span data-ttu-id="e22a9-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="e22a9-129">-NoWait</span></span>
<span data-ttu-id="e22a9-130">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="e22a9-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="e22a9-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e22a9-131">-ResourceGroupName</span></span>
<span data-ttu-id="e22a9-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e22a9-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="e22a9-133">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="e22a9-133">-SubscriptionId</span></span>
<span data-ttu-id="e22a9-134">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="e22a9-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="e22a9-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="e22a9-135">-ValidateOnly</span></span>
<span data-ttu-id="e22a9-136">Pobiera lub ustawia wartość wskazującą, czy operacja wymaga tylko wymagania wstępnego.</span><span class="sxs-lookup"><span data-stu-id="e22a9-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="e22a9-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e22a9-137">-Confirm</span></span>
<span data-ttu-id="e22a9-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e22a9-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e22a9-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e22a9-139">-WhatIf</span></span>
<span data-ttu-id="e22a9-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e22a9-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e22a9-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e22a9-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e22a9-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e22a9-142">CommonParameters</span></span>
<span data-ttu-id="e22a9-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e22a9-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e22a9-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e22a9-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e22a9-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e22a9-145">INPUTS</span></span>

## <span data-ttu-id="e22a9-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e22a9-146">OUTPUTS</span></span>

### <span data-ttu-id="e22a9-147">Microsoft. Azure. PowerShell. polecenia. ResourceMover. models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="e22a9-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="e22a9-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e22a9-148">NOTES</span></span>

<span data-ttu-id="e22a9-149">PISUJE</span><span class="sxs-lookup"><span data-stu-id="e22a9-149">ALIASES</span></span>

## <span data-ttu-id="e22a9-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e22a9-150">RELATED LINKS</span></span>

