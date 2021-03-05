---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: aa34a094631441c1ee13418d4d40306715c934b3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999882"
---
# <span data-ttu-id="51268-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="51268-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="51268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51268-102">SYNOPSIS</span></span>
<span data-ttu-id="51268-103">Usuwa kolekcję przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="51268-103">Deletes a move collection.</span></span>

## <span data-ttu-id="51268-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="51268-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="51268-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="51268-105">DESCRIPTION</span></span>
<span data-ttu-id="51268-106">Usuwa kolekcję przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="51268-106">Deletes a move collection.</span></span>

## <span data-ttu-id="51268-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="51268-107">EXAMPLES</span></span>

### <span data-ttu-id="51268-108">Przykład 1. Usunięcie kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="51268-108">Example 1: Remove the Move Collection.</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS"

AdditionalInfo : 
Code           : 
Detail         : 
EndTime        : 
Id             : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralu
                 s-demoRMS/operations/ec788761-2f1b-46a2-97b7-f5056afd334d
Message        : 
Name           : 
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 
Status         : Succeeded
```

<span data-ttu-id="51268-109">Usuń kolekcję przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="51268-109">Remove the Move Collection.</span></span>

## <span data-ttu-id="51268-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51268-110">PARAMETERS</span></span>

### <span data-ttu-id="51268-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="51268-111">-AsJob</span></span>
<span data-ttu-id="51268-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="51268-112">Run the command as a job</span></span>

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

### <span data-ttu-id="51268-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51268-113">-DefaultProfile</span></span>
<span data-ttu-id="51268-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="51268-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51268-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="51268-115">-Name</span></span>
<span data-ttu-id="51268-116">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="51268-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="51268-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="51268-117">-NoWait</span></span>
<span data-ttu-id="51268-118">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="51268-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="51268-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51268-119">-PassThru</span></span>
<span data-ttu-id="51268-120">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="51268-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="51268-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51268-121">-ResourceGroupName</span></span>
<span data-ttu-id="51268-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="51268-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="51268-123">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="51268-123">-SubscriptionId</span></span>
<span data-ttu-id="51268-124">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="51268-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="51268-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="51268-125">-Confirm</span></span>
<span data-ttu-id="51268-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="51268-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51268-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51268-127">-WhatIf</span></span>
<span data-ttu-id="51268-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="51268-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="51268-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="51268-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51268-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51268-130">CommonParameters</span></span>
<span data-ttu-id="51268-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="51268-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51268-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="51268-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51268-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51268-133">INPUTS</span></span>

## <span data-ttu-id="51268-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="51268-134">OUTPUTS</span></span>

### <span data-ttu-id="51268-135">Microsoft.Azure.PowerShell.cmdlet.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="51268-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="51268-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="51268-136">NOTES</span></span>

<span data-ttu-id="51268-137">ALIASY</span><span class="sxs-lookup"><span data-stu-id="51268-137">ALIASES</span></span>

## <span data-ttu-id="51268-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="51268-138">RELATED LINKS</span></span>

