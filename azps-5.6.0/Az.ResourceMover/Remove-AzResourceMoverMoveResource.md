---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/remove-azresourcemovermoveresource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveResource.md
ms.openlocfilehash: fc146f4d7581db84b79df82055faf2cdd8b000e3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999857"
---
# <span data-ttu-id="1e2a6-101">Remove-AzResourceMoverMoveResource</span><span class="sxs-lookup"><span data-stu-id="1e2a6-101">Remove-AzResourceMoverMoveResource</span></span>

## <span data-ttu-id="1e2a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e2a6-102">SYNOPSIS</span></span>
<span data-ttu-id="1e2a6-103">Usuwa zasób przenieś z kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="1e2a6-103">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="1e2a6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1e2a6-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveResource -MoveCollectionName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="1e2a6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1e2a6-105">DESCRIPTION</span></span>
<span data-ttu-id="1e2a6-106">Usuwa zasób przenieś z kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="1e2a6-106">Deletes a Move Resource from the move collection.</span></span>

## <span data-ttu-id="1e2a6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1e2a6-107">EXAMPLES</span></span>

### <span data-ttu-id="1e2a6-108">Przykład 1. Usunięcie jednego źródła danych Przenieś z kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="1e2a6-108">Example 1: Remove one Move Rresource from the Move Collection.</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveResource -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" -Name "psdemorm-vnet"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 2/10/2021 1:08:49 PM
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/bee69758-c7cb-4160-b3e0-8e4b69ec3731
Message        : 
Name           : bee69758-c7cb-4160-b3e0-8e4b69ec3731
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/10/2021 1:08:47 PM
Status         : Succeeded

```

<span data-ttu-id="1e2a6-109">Usuń jedno źródło Przenieś nieodwołalnie z kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="1e2a6-109">Remove one Move Rresource from the Move Collection.</span></span>

## <span data-ttu-id="1e2a6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e2a6-110">PARAMETERS</span></span>

### <span data-ttu-id="1e2a6-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1e2a6-111">-AsJob</span></span>
<span data-ttu-id="1e2a6-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="1e2a6-112">Run the command as a job</span></span>

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

### <span data-ttu-id="1e2a6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e2a6-113">-DefaultProfile</span></span>
<span data-ttu-id="1e2a6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1e2a6-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e2a6-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="1e2a6-115">-MoveCollectionName</span></span>
<span data-ttu-id="1e2a6-116">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="1e2a6-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="1e2a6-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1e2a6-117">-Name</span></span>
<span data-ttu-id="1e2a6-118">Nazwa zasobu przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="1e2a6-118">The Move Resource Name.</span></span>

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

### <span data-ttu-id="1e2a6-119">-NoWait</span><span class="sxs-lookup"><span data-stu-id="1e2a6-119">-NoWait</span></span>
<span data-ttu-id="1e2a6-120">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="1e2a6-120">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1e2a6-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e2a6-121">-PassThru</span></span>
<span data-ttu-id="1e2a6-122">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="1e2a6-122">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1e2a6-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e2a6-123">-ResourceGroupName</span></span>
<span data-ttu-id="1e2a6-124">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1e2a6-124">The Resource Group Name.</span></span>

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

### <span data-ttu-id="1e2a6-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1e2a6-125">-SubscriptionId</span></span>
<span data-ttu-id="1e2a6-126">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="1e2a6-126">The Subscription ID.</span></span>

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

### <span data-ttu-id="1e2a6-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1e2a6-127">-Confirm</span></span>
<span data-ttu-id="1e2a6-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1e2a6-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e2a6-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e2a6-129">-WhatIf</span></span>
<span data-ttu-id="1e2a6-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e2a6-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1e2a6-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1e2a6-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e2a6-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e2a6-132">CommonParameters</span></span>
<span data-ttu-id="1e2a6-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e2a6-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e2a6-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e2a6-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e2a6-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e2a6-135">INPUTS</span></span>

## <span data-ttu-id="1e2a6-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e2a6-136">OUTPUTS</span></span>

### <span data-ttu-id="1e2a6-137">Microsoft.Azure.PowerShell.cmdlet.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="1e2a6-137">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="1e2a6-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1e2a6-138">NOTES</span></span>

<span data-ttu-id="1e2a6-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="1e2a6-139">ALIASES</span></span>

## <span data-ttu-id="1e2a6-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e2a6-140">RELATED LINKS</span></span>

