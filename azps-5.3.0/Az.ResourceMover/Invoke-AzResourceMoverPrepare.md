---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 86e8cc42b10cb79216bd0252c02c6756a9d16af6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490649"
---
# <span data-ttu-id="502ee-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="502ee-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="502ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="502ee-102">SYNOPSIS</span></span>
<span data-ttu-id="502ee-103">Inicjuje przygotowanie zestawu zasobów uwzględnionych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="502ee-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="502ee-104">Operacja przygotowywania znajduje się na moveResourcesie, który znajduje się w moveState "PreparePending" lub "PrepareFailed", po poprawnym wykonaniu moveResource moveState to przejście do MovePending.</span><span class="sxs-lookup"><span data-stu-id="502ee-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="502ee-105">Aby pomóc użytkownikowi na wstępną konieczność działania, z którym klient może nawiązać operację, należy ustawić właściwość validateOnly równą true.</span><span class="sxs-lookup"><span data-stu-id="502ee-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="502ee-106">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="502ee-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="502ee-107">Opis</span><span class="sxs-lookup"><span data-stu-id="502ee-107">DESCRIPTION</span></span>
<span data-ttu-id="502ee-108">Inicjuje przygotowanie zestawu zasobów uwzględnionych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="502ee-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="502ee-109">Operacja przygotowywania znajduje się na moveResourcesie, który znajduje się w moveState "PreparePending" lub "PrepareFailed", po poprawnym wykonaniu moveResource moveState to przejście do MovePending.</span><span class="sxs-lookup"><span data-stu-id="502ee-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="502ee-110">Aby pomóc użytkownikowi na wstępną konieczność działania, z którym klient może nawiązać operację, należy ustawić właściwość validateOnly równą true.</span><span class="sxs-lookup"><span data-stu-id="502ee-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="502ee-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="502ee-111">EXAMPLES</span></span>

### <span data-ttu-id="502ee-112">Przykład 1. Sprawdź poprawność dependecies przed przygotowaniem zasobów</span><span class="sxs-lookup"><span data-stu-id="502ee-112">Example 1: Validate the dependecies before prepare for the resources</span></span>
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

<span data-ttu-id="502ee-113">Sprawdź poprawność dependecies przed przygotowaniem zasobów.</span><span class="sxs-lookup"><span data-stu-id="502ee-113">Validate the dependecies before prepare for the resources.</span></span>

### <span data-ttu-id="502ee-114">Przykład 2: Inicjowanie przygotowywania zestawu zasobów w kolekcji Move przy użyciu funkcji "MoveResource Name" jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="502ee-114">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input</span></span>
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

<span data-ttu-id="502ee-115">Rozpocznij przygotowywanie zestawu zasobów w kolekcji Move przy użyciu funkcji "MoveResource Name" jako danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="502ee-115">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="502ee-116">Przykład 3: Inicjowanie przygotowywania zestawu zasobów w kolekcji Move przy użyciu "SourceARMID"</span><span class="sxs-lookup"><span data-stu-id="502ee-116">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID"</span></span>
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

<span data-ttu-id="502ee-117">Zainicjuj przygotowywanie zestawu zasobów w kolekcji Move przy użyciu "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="502ee-117">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="502ee-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="502ee-118">PARAMETERS</span></span>

### <span data-ttu-id="502ee-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="502ee-119">-AsJob</span></span>
<span data-ttu-id="502ee-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="502ee-120">Run the command as a job</span></span>

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

### <span data-ttu-id="502ee-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="502ee-121">-DefaultProfile</span></span>
<span data-ttu-id="502ee-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="502ee-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="502ee-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="502ee-123">-MoveCollectionName</span></span>
<span data-ttu-id="502ee-124">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="502ee-124">The Move Collection Name.</span></span>

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

### <span data-ttu-id="502ee-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="502ee-125">-MoveResource</span></span>
<span data-ttu-id="502ee-126">Pobiera lub ustawia listę identyfikatorów zasobów domyślnie przyjmuje identyfikator "Przenieś zasób", chyba że typ wejściowy zostanie przełączony za pomocą właściwości moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="502ee-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="502ee-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="502ee-127">-MoveResourceInputType</span></span>
<span data-ttu-id="502ee-128">Określa typ wejścia zasobu do przeniesienia.</span><span class="sxs-lookup"><span data-stu-id="502ee-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="502ee-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="502ee-129">-NoWait</span></span>
<span data-ttu-id="502ee-130">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="502ee-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="502ee-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="502ee-131">-ResourceGroupName</span></span>
<span data-ttu-id="502ee-132">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="502ee-132">The Resource Group Name.</span></span>

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

### <span data-ttu-id="502ee-133">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="502ee-133">-SubscriptionId</span></span>
<span data-ttu-id="502ee-134">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="502ee-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="502ee-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="502ee-135">-ValidateOnly</span></span>
<span data-ttu-id="502ee-136">Pobiera lub ustawia wartość wskazującą, czy operacja wymaga tylko wymagania wstępnego.</span><span class="sxs-lookup"><span data-stu-id="502ee-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="502ee-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="502ee-137">-Confirm</span></span>
<span data-ttu-id="502ee-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="502ee-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="502ee-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="502ee-139">-WhatIf</span></span>
<span data-ttu-id="502ee-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="502ee-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="502ee-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="502ee-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="502ee-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="502ee-142">CommonParameters</span></span>
<span data-ttu-id="502ee-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="502ee-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="502ee-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="502ee-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="502ee-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="502ee-145">INPUTS</span></span>

## <span data-ttu-id="502ee-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="502ee-146">OUTPUTS</span></span>

### <span data-ttu-id="502ee-147">Microsoft. Azure. PowerShell. polecenia. ResourceMover. models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="502ee-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="502ee-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="502ee-148">NOTES</span></span>

<span data-ttu-id="502ee-149">PISUJE</span><span class="sxs-lookup"><span data-stu-id="502ee-149">ALIASES</span></span>

## <span data-ttu-id="502ee-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="502ee-150">RELATED LINKS</span></span>

