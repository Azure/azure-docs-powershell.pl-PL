---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverprepare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverPrepare.md
ms.openlocfilehash: 95ad5dad6bd375595a452881e1dfe72a9f314207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999937"
---
# <span data-ttu-id="ad977-101">Invoke-AzResourceMoverPrepare</span><span class="sxs-lookup"><span data-stu-id="ad977-101">Invoke-AzResourceMoverPrepare</span></span>

## <span data-ttu-id="ad977-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad977-102">SYNOPSIS</span></span>
<span data-ttu-id="ad977-103">Inicjuje przygotowywanie zestawu zasobów zawartych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="ad977-103">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="ad977-104">Operacja przygotowywania znajduje się na stronie moveResources, które znajdują się w operacji moveState "PreparePending" lub "PrepareFailed", po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do operacji MovePending.</span><span class="sxs-lookup"><span data-stu-id="ad977-104">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="ad977-105">Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.</span><span class="sxs-lookup"><span data-stu-id="ad977-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="ad977-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ad977-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverPrepare -MoveCollectionName <String> -ResourceGroupName <String>
 -MoveResource <String[]> [-SubscriptionId <String>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="ad977-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ad977-107">DESCRIPTION</span></span>
<span data-ttu-id="ad977-108">Inicjuje przygotowywanie zestawu zasobów zawartych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="ad977-108">Initiates prepare for the set of resources included in the request body.</span></span>
<span data-ttu-id="ad977-109">Operacja przygotowywania znajduje się na stronie moveResources, które znajdują się w operacji moveState "PreparePending" lub "PrepareFailed", po pomyślnym ukończeniu operacji moveResource moveState wykonaj przejście do operacji MovePending.</span><span class="sxs-lookup"><span data-stu-id="ad977-109">The prepare operation is on the moveResources that are in the moveState 'PreparePending' or 'PrepareFailed', on a successful completion the moveResource moveState do a transition to MovePending.</span></span>
<span data-ttu-id="ad977-110">Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.</span><span class="sxs-lookup"><span data-stu-id="ad977-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="ad977-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ad977-111">EXAMPLES</span></span>

### <span data-ttu-id="ad977-112">Przykład 1. Sprawdzanie zależności przed przygotowaniem zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad977-112">Example 1: Validate the dependecies before prepare of the resources.</span></span> <span data-ttu-id="ad977-113">Uzyskaj wymagane zasoby zależne, które również muszą być przygotowane.</span><span class="sxs-lookup"><span data-stu-id="ad977-113">Get the required dependent resources that also need to be prepared.</span></span>
```powershell
PS C:\> $resp = Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('psdemovm') -ValidateOnly

AdditionalInfo : {Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.OperationErrorAdditionalInfo}
Code           : MoveCollectionMissingRequiredDependentResources
Detail         : {}
EndTime        : 2/9/2021 9:04:15 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RegionMoveRG-centralus-westcentralus/providers/Microsoft.Migr
                 ate/MoveCollections/PS-centralus-westcentralus-demoRMS/12d055bd-ac52-427f-8b05-b4b21c4b51e8
Message        : The operation has failed as required move resources are missing from the input.
                     Possible Causes: Dependent resources are missing from the input.
                     Recommended Action: Retry the operation with all required resources, if the issue persist contact support.

Name           : 12d055bd-ac52-427f-8b05-b4b21c4b51e8
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 9:04:14 AM
Status         : Failed

PS C:> $resp.Code
MoveCollectionMissingRequiredDependentResources

PS C:> $resp.AdditionalInfo[0].InfoMoveResource

SourceId                                                                                                                                  
--------                                                                                                                                  
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networkinterfaces/psdemovm111     
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/psdemorm/providers/Microsoft.Network/virtualNetworks/psdemorm-vnet     
/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourcegroups/psdemorm/providers/microsoft.network/networksecuritygroups/psdemovm-nsg

```

<span data-ttu-id="ad977-114">Sprawdź poprawność zależności przed przygotowaniem zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad977-114">Validate the dependecies before prepare of the resources.</span></span>
<span data-ttu-id="ad977-115">Uzyskaj wymagane zasoby zależne, które również muszą być przygotowane.</span><span class="sxs-lookup"><span data-stu-id="ad977-115">Get the required dependent resources that also need to be prepared.</span></span>

### <span data-ttu-id="ad977-116">Przykład 2. Zainicjuj przygotowywanie zestawu zasobów w kolekcji przenoszenia, używając jako danych wejściowych "MoveResource Name".</span><span class="sxs-lookup"><span data-stu-id="ad977-116">Example 2: Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM','psdemovm111', 'PSDemoRM-vnet','PSDemoVM-nsg')

AAdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/9/2021 11:25:13 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/49e4429
                 4-24ac-4eac-93da-e7e1c815554d
Message        : 
Name           : 49e44294-24ac-4eac-93da-e7e1c815554d
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 10:55:53 AM
Status         : Succeeded
```

<span data-ttu-id="ad977-117">Zainicjuj przygotowywanie zestawu zasobów w kolekcji przenoszenia, używając jako danych wejściowych "MoveResource Name".</span><span class="sxs-lookup"><span data-stu-id="ad977-117">Initiate prepare for the set of resources in the Move Collection using "MoveResource Name" as input.</span></span>

### <span data-ttu-id="ad977-118">Przykład 3. Zainicjuj przygotowywanie zestawu zasobów w kolekcji przenoszenia przy użyciu funkcji "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="ad977-118">Example 3: Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverPrepare -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -MoveResourceInputType MoveResourceSourceId  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRMS/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg')

AdditionalInfo :
Code           :
Detail         :
EndTime        : 2/9/2021 11:09:30 AM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/MoveColl
                 ections/PS-centralus-westcentralus-demoRMS/operations/c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Message        :
Name           : c7b13d43-a6fe-48e3-bb8c-3ad9e6ba3355
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 11:05:27 AM
Status         : Succeeded

```

<span data-ttu-id="ad977-119">Zainicjuj przygotowywanie zestawu zasobów w kolekcji przenoszenia przy użyciu funkcji "SourceARMID".</span><span class="sxs-lookup"><span data-stu-id="ad977-119">Initiate prepare for the set of resources in the Move Collection using "SourceARMID".</span></span>

## <span data-ttu-id="ad977-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad977-120">PARAMETERS</span></span>

### <span data-ttu-id="ad977-121">— AsJob</span><span class="sxs-lookup"><span data-stu-id="ad977-121">-AsJob</span></span>
<span data-ttu-id="ad977-122">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="ad977-122">Run the command as a job</span></span>

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

### <span data-ttu-id="ad977-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad977-123">-DefaultProfile</span></span>
<span data-ttu-id="ad977-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad977-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad977-125">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="ad977-125">-MoveCollectionName</span></span>
<span data-ttu-id="ad977-126">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="ad977-126">The Move Collection Name.</span></span>

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

### <span data-ttu-id="ad977-127">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="ad977-127">-MoveResource</span></span>
<span data-ttu-id="ad977-128">Pobiera lub ustawia listę identyfikatorów zasobów, domyślnie akceptuje przenoszenie identyfikatorów zasobów, chyba że typ wejściowy zostanie przełączony za pomocą właściwości moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="ad977-128">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

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

### <span data-ttu-id="ad977-129">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="ad977-129">-MoveResourceInputType</span></span>
<span data-ttu-id="ad977-130">Definiuje typ danych wejściowych zasobu przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="ad977-130">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="ad977-131">-NoWait</span><span class="sxs-lookup"><span data-stu-id="ad977-131">-NoWait</span></span>
<span data-ttu-id="ad977-132">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="ad977-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="ad977-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad977-133">-ResourceGroupName</span></span>
<span data-ttu-id="ad977-134">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad977-134">The Resource Group Name.</span></span>

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

### <span data-ttu-id="ad977-135">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="ad977-135">-SubscriptionId</span></span>
<span data-ttu-id="ad977-136">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ad977-136">The Subscription ID.</span></span>

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

### <span data-ttu-id="ad977-137">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="ad977-137">-ValidateOnly</span></span>
<span data-ttu-id="ad977-138">Pobiera lub ustawia wartość wskazującą, czy operacja wymaga tylko wstępnego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="ad977-138">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="ad977-139">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad977-139">-Confirm</span></span>
<span data-ttu-id="ad977-140">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ad977-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad977-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad977-141">-WhatIf</span></span>
<span data-ttu-id="ad977-142">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad977-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad977-143">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ad977-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad977-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad977-144">CommonParameters</span></span>
<span data-ttu-id="ad977-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad977-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad977-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad977-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad977-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad977-147">INPUTS</span></span>

## <span data-ttu-id="ad977-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad977-148">OUTPUTS</span></span>

### <span data-ttu-id="ad977-149">Microsoft.Azure.PowerShell.cmdlet.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="ad977-149">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="ad977-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ad977-150">NOTES</span></span>

<span data-ttu-id="ad977-151">ALIASY</span><span class="sxs-lookup"><span data-stu-id="ad977-151">ALIASES</span></span>

## <span data-ttu-id="ad977-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad977-152">RELATED LINKS</span></span>

