---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: f718f3c133f25a8b7fb401bfb9a390724090ccc4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183699"
---
# <span data-ttu-id="8b032-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="8b032-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="8b032-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b032-102">SYNOPSIS</span></span>
<span data-ttu-id="8b032-103">Usuwa zasób przenieś z kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="8b032-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="8b032-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8b032-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="8b032-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8b032-105">DESCRIPTION</span></span>
<span data-ttu-id="8b032-106">Usuwa zasób przenieś z kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="8b032-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="8b032-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8b032-107">EXAMPLES</span></span>

### <span data-ttu-id="8b032-108">Przykład 1. Usunięcie zasobu z kolekcji Przenieś</span><span class="sxs-lookup"><span data-stu-id="8b032-108">Example 1: Remove the resource from the Move collection</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName RG-MoveCollection-demoRM -MoveCollectionName PS-centralus-westcentralus-demoRM -Name "psdemorm"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/11/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                     ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866c5
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/11/2020 3:27:27 PM
    Status         : Succeeded

```

<span data-ttu-id="8b032-109">Usuń zasób z kolekcji Przenieś w ramach określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8b032-109">Remove the resource from the Move collection within the specified subscription.</span></span>

## <span data-ttu-id="8b032-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8b032-110">PARAMETERS</span></span>

### <span data-ttu-id="8b032-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="8b032-111">-AsJob</span></span>
<span data-ttu-id="8b032-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="8b032-112">Run the command as a job</span></span>

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

### <span data-ttu-id="8b032-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b032-113">-DefaultProfile</span></span>
<span data-ttu-id="8b032-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8b032-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8b032-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="8b032-115">-MoveCollectionName</span></span>
<span data-ttu-id="8b032-116">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="8b032-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="8b032-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8b032-117">-Name</span></span>
<span data-ttu-id="8b032-118">Nazwa zasobu przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="8b032-118">The Move Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: MoveResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8b032-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="8b032-119">-NoWait</span></span>
<span data-ttu-id="8b032-120">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="8b032-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8b032-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8b032-121">-PassThru</span></span>
<span data-ttu-id="8b032-122">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="8b032-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8b032-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b032-123">-ResourceGroupName</span></span>
<span data-ttu-id="8b032-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8b032-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="8b032-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8b032-125">-SubscriptionId</span></span>
<span data-ttu-id="8b032-126">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8b032-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="8b032-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8b032-127">-Confirm</span></span>
<span data-ttu-id="8b032-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8b032-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8b032-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8b032-129">-WhatIf</span></span>
<span data-ttu-id="8b032-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8b032-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8b032-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8b032-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8b032-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b032-132">CommonParameters</span></span>
<span data-ttu-id="8b032-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8b032-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b032-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b032-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b032-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b032-135">INPUTS</span></span>

## <span data-ttu-id="8b032-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8b032-136">OUTPUTS</span></span>

### <span data-ttu-id="8b032-137">Microsoft.Azure.PowerShell.cmdlet.ResourceMover.Models.Api20191001Preview.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="8b032-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="8b032-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8b032-138">NOTES</span></span>

<span data-ttu-id="8b032-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="8b032-139">ALIASES</span></span>

## <span data-ttu-id="8b032-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8b032-140">RELATED LINKS</span></span>

