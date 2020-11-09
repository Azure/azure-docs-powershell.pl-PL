---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverinitiatemove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverInitiateMove.md
ms.openlocfilehash: c1942358ea438d596afc3f147e65a894b270f0d7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317658"
---
# <span data-ttu-id="d8df8-101">Invoke-AzResourceMoverInitiateMove</span><span class="sxs-lookup"><span data-stu-id="d8df8-101">Invoke-AzResourceMoverInitiateMove</span></span>

## <span data-ttu-id="d8df8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8df8-102">SYNOPSIS</span></span>
<span data-ttu-id="d8df8-103">Powoduje przeniesienie zestawu zasobów uwzględnionych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="d8df8-103">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="d8df8-104">Operacja przenoszenia jest wyzwalana, gdy moveResources znajduje się w moveState "MovePending" lub "MoveFailed", po poprawnym wykonaniu moveResource moveState, aby przejść do CommitPending.</span><span class="sxs-lookup"><span data-stu-id="d8df8-104">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="d8df8-105">Aby pomóc użytkownikowi na wstępną konieczność działania, z którym klient może nawiązać operację, należy ustawić właściwość validateOnly równą true.</span><span class="sxs-lookup"><span data-stu-id="d8df8-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="d8df8-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8df8-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverInitiateMove -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d8df8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="d8df8-107">DESCRIPTION</span></span>
<span data-ttu-id="d8df8-108">Powoduje przeniesienie zestawu zasobów uwzględnionych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="d8df8-108">Moves the set of resources included in the request body.</span></span>
<span data-ttu-id="d8df8-109">Operacja przenoszenia jest wyzwalana, gdy moveResources znajduje się w moveState "MovePending" lub "MoveFailed", po poprawnym wykonaniu moveResource moveState, aby przejść do CommitPending.</span><span class="sxs-lookup"><span data-stu-id="d8df8-109">The move operation is triggered after the moveResources are in the moveState 'MovePending' or 'MoveFailed', on a successful completion the moveResource moveState do a transition to CommitPending.</span></span>
<span data-ttu-id="d8df8-110">Aby pomóc użytkownikowi na wstępną konieczność działania, z którym klient może nawiązać operację, należy ustawić właściwość validateOnly równą true.</span><span class="sxs-lookup"><span data-stu-id="d8df8-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="d8df8-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8df8-111">EXAMPLES</span></span>

### <span data-ttu-id="d8df8-112">Przykład 1. Sprawdź poprawność dependecies przed rozpoczęciem przenoszenia zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8df8-112">Example 1: Validate the dependecies before Initiate Move for the resources.</span></span>
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

<span data-ttu-id="d8df8-113">Sprawdź poprawność dependecies przed rozpoczęciem przenoszenia zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8df8-113">Validate the dependecies before Initiate Move for the resources.</span></span>

### <span data-ttu-id="d8df8-114">Przykład 2: Inicjowanie przeniesienia zestawu zasobów w kolekcji Move przy użyciu funkcji "MoveResource Name" jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="d8df8-114">Example 2: Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input</span></span>
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

<span data-ttu-id="d8df8-115">Inicjuj przenoszenie zestawu zasobów w kolekcji Move przy użyciu funkcji "MoveResource Name" jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d8df8-115">Initiate Move for the set of resources in the Move collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="d8df8-116">Przykład 3: Inicjowanie przeniesienia zestawu zasobów w kolekcji Move przy użyciu funkcji "SourceARMID" jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="d8df8-116">Example 3: Initiate Move for the set of resources in the Move Collection using "SourceARMID" as input</span></span>
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

<span data-ttu-id="d8df8-117">Rozpocznij przenoszenie zestawu zasobów w kolekcji Move przy użyciu funkcji "SourceARMID" jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d8df8-117">Initiate Move for the set of resources in the Move collection using "SourceARMID" as input.</span></span>

## <span data-ttu-id="d8df8-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8df8-118">PARAMETERS</span></span>

### <span data-ttu-id="d8df8-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8df8-119">-AsJob</span></span>
<span data-ttu-id="d8df8-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="d8df8-120">Run the command as a job</span></span>

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

### <span data-ttu-id="d8df8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8df8-121">-DefaultProfile</span></span>
<span data-ttu-id="d8df8-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8df8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8df8-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="d8df8-123">-MoveCollectionName</span></span>
<span data-ttu-id="d8df8-124">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="d8df8-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="d8df8-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="d8df8-125">-MoveResource</span></span>
<span data-ttu-id="d8df8-126">Pobiera lub ustawia listę identyfikatorów zasobów domyślnie przyjmuje identyfikator "Przenieś zasób", chyba że typ wejściowy zostanie przełączony za pomocą właściwości moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="d8df8-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="d8df8-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="d8df8-127">-MoveResourceInputType</span></span>
<span data-ttu-id="d8df8-128">Określa typ wejścia zasobu do przeniesienia.</span><span class="sxs-lookup"><span data-stu-id="d8df8-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="d8df8-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="d8df8-129">-NoWait</span></span>
<span data-ttu-id="d8df8-130">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="d8df8-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d8df8-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8df8-131">-ResourceGroupName</span></span>
<span data-ttu-id="d8df8-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8df8-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="d8df8-133">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d8df8-133">-SubscriptionId</span></span>
<span data-ttu-id="d8df8-134">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="d8df8-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="d8df8-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="d8df8-135">-ValidateOnly</span></span>
<span data-ttu-id="d8df8-136">Pobiera lub ustawia wartość wskazującą, czy operacja wymaga tylko wymagania wstępnego.</span><span class="sxs-lookup"><span data-stu-id="d8df8-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="d8df8-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8df8-137">-Confirm</span></span>
<span data-ttu-id="d8df8-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8df8-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8df8-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8df8-139">-WhatIf</span></span>
<span data-ttu-id="d8df8-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8df8-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8df8-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d8df8-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8df8-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8df8-142">CommonParameters</span></span>
<span data-ttu-id="d8df8-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8df8-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8df8-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d8df8-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8df8-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8df8-145">INPUTS</span></span>

## <span data-ttu-id="d8df8-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8df8-146">OUTPUTS</span></span>

### <span data-ttu-id="d8df8-147">Microsoft. Azure. PowerShell. polecenia. ResourceMover. models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="d8df8-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="d8df8-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8df8-148">NOTES</span></span>

<span data-ttu-id="d8df8-149">PISUJE</span><span class="sxs-lookup"><span data-stu-id="d8df8-149">ALIASES</span></span>

## <span data-ttu-id="d8df8-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8df8-150">RELATED LINKS</span></span>

