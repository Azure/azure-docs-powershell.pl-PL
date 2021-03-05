---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/invoke-azresourcemoverbulkremove
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverBulkRemove.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Invoke-AzResourceMoverBulkRemove.md
ms.openlocfilehash: f9815c32526a5ce462a50ec167771d30bc840b1e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999985"
---
# <span data-ttu-id="2c705-101">Invoke-AzResourceMoverBulkRemove</span><span class="sxs-lookup"><span data-stu-id="2c705-101">Invoke-AzResourceMoverBulkRemove</span></span>

## <span data-ttu-id="2c705-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c705-102">SYNOPSIS</span></span>
<span data-ttu-id="2c705-103">Usuwa z kolekcji przenoszenie zestaw zasobów przeniesienia zawartych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="2c705-103">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="2c705-104">Projekt jest wykonywane przez usługę.</span><span class="sxs-lookup"><span data-stu-id="2c705-104">The orchestration is done by service.</span></span>
<span data-ttu-id="2c705-105">Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.</span><span class="sxs-lookup"><span data-stu-id="2c705-105">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="2c705-106">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2c705-106">SYNTAX</span></span>

```
Invoke-AzResourceMoverBulkRemove -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-MoveResource <String[]>] [-MoveResourceInputType <MoveResourceInputType>]
 [-ValidateOnly] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="2c705-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="2c705-107">DESCRIPTION</span></span>
<span data-ttu-id="2c705-108">Usuwa z kolekcji przenoszenie zestaw zasobów przeniesienia zawartych w treści żądania.</span><span class="sxs-lookup"><span data-stu-id="2c705-108">Removes the set of move resources included in the request body from move collection.</span></span>
<span data-ttu-id="2c705-109">Projekt jest wykonywane przez usługę.</span><span class="sxs-lookup"><span data-stu-id="2c705-109">The orchestration is done by service.</span></span>
<span data-ttu-id="2c705-110">Aby pomóc użytkownikowi wstępnie skonfigurować operację, która może zostać wywołana przez klienta, ustawioną jako prawda właściwość validateOnly.</span><span class="sxs-lookup"><span data-stu-id="2c705-110">To aid the user to prerequisite the operation the client can call operation with validateOnly property set to true.</span></span>

## <span data-ttu-id="2c705-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2c705-111">EXAMPLES</span></span>

### <span data-ttu-id="2c705-112">Przykład 1. Sprawdzanie poprawności zależności przed usunięciem zasobów przenieś z przenieś kolekcji</span><span class="sxs-lookup"><span data-stu-id="2c705-112">Example 1: Validate the dependecies before remove of the Move Resources from Move Collection</span></span>
```powershell
PS C:\> Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM') -MoveResourceInputType "MoveResourceId" -ValidateOnly

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:52:28 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/b4e3f140-b36b-4fd5-a507-b1e663ecf7a3
Message        : 
Name           : b4e3f140-b36b-4fd5-a507-b1e663ecf7a3
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:52:28 PM
Status         : Succeeded

```

<span data-ttu-id="2c705-113">Sprawdź poprawność zależności przed usunięciem zasobów przeniesienia z przenieś kolekcji.</span><span class="sxs-lookup"><span data-stu-id="2c705-113">Validate the dependecies before remove of the move resources from Move Collection.</span></span>

### <span data-ttu-id="2c705-114">Przykład 2. Usunięcie zasobu Przenieś z przenieś kolekcji przy użyciu wartości "MoveResource Name" jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="2c705-114">Example 2: Remove the Move Resource from Move Collection using "MoveResource Name" as input</span></span>
```powershell
Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('PSDemoVM') -MoveResourceInputType "MoveResourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 12:58:10 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/d4827071-b797-45c5-b88c-00ddd7818d42
Message        : 
Name           : d4827071-b797-45c5-b88c-00ddd7818d42
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 12:57:08 PM
Status         : Succeeded
```

<span data-ttu-id="2c705-115">Usuwanie zasobu przenoszenia z kolekcji przenoszenia przy użyciu wartości "MoveResource Name" jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="2c705-115">Remove the Move Resource from Move Collection using "MoveResource Name" as input</span></span>

### <span data-ttu-id="2c705-116">Przykład 3. Usunięcie zasobu przenieś z przenieś kolekcji przy użyciu wartości "SourceARMID" jako danych wejściowych</span><span class="sxs-lookup"><span data-stu-id="2c705-116">Example 3: Remove the Move Resource from Move Collection using "SourceARMID" as input</span></span>
```powershell
Invoke-AzResourceMoverBulkRemove -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"  -MoveResource $('/subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/PSDemoRM/providers/Microsoft.Network/networkSecurityGroups/PSDemoVM-nsg') -MoveResourceInputType "MoveResourceSourceId"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:05:13 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/7b6904e2-fc3f-400d-b248-8908fcb282fb
Message        : 
Name           : 7b6904e2-fc3f-400d-b248-8908fcb282fb
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:05:00 PM
Status         : Succeeded
```

<span data-ttu-id="2c705-117">Usuwanie zasobu przenoszenia z kolekcji przenoszenia przy użyciu jako danych wejściowych "SourceARMID"</span><span class="sxs-lookup"><span data-stu-id="2c705-117">Remove the Move Resource from Move Collection using "SourceARMID" as input</span></span>

## <span data-ttu-id="2c705-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c705-118">PARAMETERS</span></span>

### <span data-ttu-id="2c705-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="2c705-119">-AsJob</span></span>
<span data-ttu-id="2c705-120">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="2c705-120">Run the command as a job</span></span>

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

### <span data-ttu-id="2c705-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c705-121">-DefaultProfile</span></span>
<span data-ttu-id="2c705-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c705-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c705-123">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="2c705-123">-MoveCollectionName</span></span>
<span data-ttu-id="2c705-124">.</span><span class="sxs-lookup"><span data-stu-id="2c705-124">.</span></span>

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

### <span data-ttu-id="2c705-125">-MoveResource</span><span class="sxs-lookup"><span data-stu-id="2c705-125">-MoveResource</span></span>
<span data-ttu-id="2c705-126">Pobiera lub ustawia listę identyfikatorów zasobów, domyślnie akceptuje przenoszenie identyfikatorów zasobów, chyba że typ wejściowy zostanie przełączony za pomocą właściwości moveResourceInputType.</span><span class="sxs-lookup"><span data-stu-id="2c705-126">Gets or sets the list of resource Id's, by default it accepts move resource id's unless the input type is switched via moveResourceInputType property.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c705-127">-MoveResourceInputType</span><span class="sxs-lookup"><span data-stu-id="2c705-127">-MoveResourceInputType</span></span>
<span data-ttu-id="2c705-128">Definiuje typ danych wejściowych zasobu przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="2c705-128">Defines the move resource input type.</span></span>

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

### <span data-ttu-id="2c705-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="2c705-129">-NoWait</span></span>
<span data-ttu-id="2c705-130">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="2c705-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="2c705-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c705-131">-ResourceGroupName</span></span>
<span data-ttu-id="2c705-132">.</span><span class="sxs-lookup"><span data-stu-id="2c705-132">.</span></span>

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

### <span data-ttu-id="2c705-133">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2c705-133">-SubscriptionId</span></span>
<span data-ttu-id="2c705-134">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2c705-134">The Subscription ID.</span></span>

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

### <span data-ttu-id="2c705-135">-ValidateOnly</span><span class="sxs-lookup"><span data-stu-id="2c705-135">-ValidateOnly</span></span>
<span data-ttu-id="2c705-136">Pobiera lub ustawia wartość wskazującą, czy operacja wymaga tylko wstępnego uruchomienia.</span><span class="sxs-lookup"><span data-stu-id="2c705-136">Gets or sets a value indicating whether the operation needs to only run pre-requisite.</span></span>

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

### <span data-ttu-id="2c705-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2c705-137">-Confirm</span></span>
<span data-ttu-id="2c705-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2c705-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c705-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c705-139">-WhatIf</span></span>
<span data-ttu-id="2c705-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c705-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c705-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2c705-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c705-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c705-142">CommonParameters</span></span>
<span data-ttu-id="2c705-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c705-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c705-144">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c705-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c705-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c705-145">INPUTS</span></span>

## <span data-ttu-id="2c705-146">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c705-146">OUTPUTS</span></span>

### <span data-ttu-id="2c705-147">Microsoft.Azure.PowerShell.cmdlet.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="2c705-147">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="2c705-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2c705-148">NOTES</span></span>

<span data-ttu-id="2c705-149">ALIASY</span><span class="sxs-lookup"><span data-stu-id="2c705-149">ALIASES</span></span>

## <span data-ttu-id="2c705-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c705-150">RELATED LINKS</span></span>

