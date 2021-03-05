---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/powershell/module/az.resourcemover/resolve-azresourcemovermovecollectiondependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
ms.openlocfilehash: 6812849fc8fe4aa8dab21f9bbcfc13891c45e0ac
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101999850"
---
# <span data-ttu-id="d9d03-101">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="d9d03-101">Resolve-AzResourceMoverMoveCollectionDependency</span></span>

## <span data-ttu-id="d9d03-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9d03-102">SYNOPSIS</span></span>
<span data-ttu-id="d9d03-103">Oblicza, oblicza i sprawdza zależności elementów moveResources w kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="d9d03-103">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="d9d03-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d9d03-104">SYNTAX</span></span>

```
Resolve-AzResourceMoverMoveCollectionDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="d9d03-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d9d03-105">DESCRIPTION</span></span>
<span data-ttu-id="d9d03-106">Oblicza, oblicza i sprawdza zależności elementów moveResources w kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="d9d03-106">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="d9d03-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d9d03-107">EXAMPLES</span></span>

### <span data-ttu-id="d9d03-108">Przykład 1. Obliczanie, rozwiązywanie i weryfikowanie zależności elementów Move Resources w kolekcji Przenoszenie.</span><span class="sxs-lookup"><span data-stu-id="d9d03-108">Example 1: Compute, resolve and validate the dependencies of the Move Resources in the Move collection.</span></span>
```powershell
PS C:\> Resolve-AzResourceMoverMoveCollectionDependency -ResourceGroupName "RG-MoveCollection-demoRMS" -MoveCollectionName "PS-centralus-westcentralus-demoRMS" 

AdditionalInfo : 
Code           : MoveCollectionResolveDependenciesOperationFailed
Detail         : {}
EndTime        : 2/9/2021 2:05:04 AM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRMS/providers/Microsoft.Migrate/moveCollections/PS-centralus-westcentralus-demoRMS/operations/c2ad006
                 6-6a69-45fe-aa70-193c240a9bc0
Message        : The resolve dependencies operation of one or more resources has failed. Check the move status of the resource for more details.
                     Possible Causes: The resolve dependencies operation of one ore more resources has failed.
                     Recommended Action: Retry the operation after resolving errors if any. If issue persists, contact support.
                     
Name           : c2ad0066-6a69-45fe-aa70-193c240a9bc0
Property       : Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Any
StartTime      : 2/9/2021 2:05:00 AM
Status         : Succeeded
```

<span data-ttu-id="d9d03-109">Obliczanie, rozwiązywanie i sprawdzanie zależności właściwości Przenieś zasoby w kolekcji Przenoszenie.</span><span class="sxs-lookup"><span data-stu-id="d9d03-109">Compute, resolve and validate the dependencies of the Move Resources in the Move collection.</span></span>

## <span data-ttu-id="d9d03-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d9d03-110">PARAMETERS</span></span>

### <span data-ttu-id="d9d03-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d9d03-111">-AsJob</span></span>
<span data-ttu-id="d9d03-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="d9d03-112">Run the command as a job</span></span>

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

### <span data-ttu-id="d9d03-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9d03-113">-DefaultProfile</span></span>
<span data-ttu-id="d9d03-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d9d03-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9d03-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="d9d03-115">-MoveCollectionName</span></span>
<span data-ttu-id="d9d03-116">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="d9d03-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="d9d03-117">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d9d03-117">-NoWait</span></span>
<span data-ttu-id="d9d03-118">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="d9d03-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d9d03-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9d03-119">-ResourceGroupName</span></span>
<span data-ttu-id="d9d03-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d9d03-120">The Resource Group Name.</span></span>

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

### <span data-ttu-id="d9d03-121">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d9d03-121">-SubscriptionId</span></span>
<span data-ttu-id="d9d03-122">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d9d03-122">The Subscription ID.</span></span>

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

### <span data-ttu-id="d9d03-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d9d03-123">-Confirm</span></span>
<span data-ttu-id="d9d03-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d9d03-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9d03-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9d03-125">-WhatIf</span></span>
<span data-ttu-id="d9d03-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d9d03-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9d03-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d9d03-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9d03-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9d03-128">CommonParameters</span></span>
<span data-ttu-id="d9d03-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d9d03-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9d03-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d9d03-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9d03-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9d03-131">INPUTS</span></span>

## <span data-ttu-id="d9d03-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d9d03-132">OUTPUTS</span></span>

### <span data-ttu-id="d9d03-133">Microsoft.Azure.PowerShell.cmdlet.ResourceMover.Models.Api202101.IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="d9d03-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api202101.IOperationStatus</span></span>

## <span data-ttu-id="d9d03-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d9d03-134">NOTES</span></span>

<span data-ttu-id="d9d03-135">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d9d03-135">ALIASES</span></span>

## <span data-ttu-id="d9d03-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d9d03-136">RELATED LINKS</span></span>

