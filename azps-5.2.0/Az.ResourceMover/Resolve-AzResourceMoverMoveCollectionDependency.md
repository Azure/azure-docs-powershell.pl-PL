---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/resolve-azresourcemovermovecollectiondependency
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Resolve-AzResourceMoverMoveCollectionDependency.md
ms.openlocfilehash: c37ac4f5db2df62ecf1f76764f69e31f234708e7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353737"
---
# <span data-ttu-id="f0c38-101">Resolve-AzResourceMoverMoveCollectionDependency</span><span class="sxs-lookup"><span data-stu-id="f0c38-101">Resolve-AzResourceMoverMoveCollectionDependency</span></span>

## <span data-ttu-id="f0c38-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f0c38-102">SYNOPSIS</span></span>
<span data-ttu-id="f0c38-103">Oblicza, rozpoznaje i sprawdza poprawność zależności moveResources w kolekcji Move.</span><span class="sxs-lookup"><span data-stu-id="f0c38-103">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="f0c38-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f0c38-104">SYNTAX</span></span>

```
Resolve-AzResourceMoverMoveCollectionDependency -MoveCollectionName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="f0c38-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f0c38-105">DESCRIPTION</span></span>
<span data-ttu-id="f0c38-106">Oblicza, rozpoznaje i sprawdza poprawność zależności moveResources w kolekcji Move.</span><span class="sxs-lookup"><span data-stu-id="f0c38-106">Computes, resolves and validate the dependencies of the moveResources in the move collection.</span></span>

## <span data-ttu-id="f0c38-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f0c38-107">EXAMPLES</span></span>

### <span data-ttu-id="f0c38-108">Przykład 1: oblicza, rozpoznaje i sprawdza poprawność zależności moveresources w kolekcji Move.</span><span class="sxs-lookup"><span data-stu-id="f0c38-108">Example 1: Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>
```powershell
PS C:\> Resolve-AzResourceMoverMoveCollectionDependency -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM" 

AdditionalInfo : 
Code           : MoveCollectionResolveDependenciesOperationFailed
Detail         : {}
EndTime        : 8/16/2020 2:28:18 PM
Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveCollections/PS-ce
                 ntralus-westcentralus-demoRM/operations/bce85a10-1ff3-4815-a677-7b188f7b441a
Message        : The resolve dependencies operation of one ore more resources has failed. Check the move status of the resource for more details. 
Possible Causes: The resolve dependencies operation of one ore more resources has failed.
Recommended Action: Retry the operation after resolving errors if any. If issue persists, contact support.
                     
Name           : bce85a10-1ff3-4815-a677-7b188f7b441a
Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
StartTime      : 8/16/2020 2:28:16 PM
Status         : Succeeded
```

<span data-ttu-id="f0c38-109">Oblicza, rozpoznaje i sprawdza poprawność zależności moveresources w kolekcji Move.</span><span class="sxs-lookup"><span data-stu-id="f0c38-109">Computes, resolves and validate the dependencies of the moveresources in the Move collection.</span></span>

## <span data-ttu-id="f0c38-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f0c38-110">PARAMETERS</span></span>

### <span data-ttu-id="f0c38-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f0c38-111">-AsJob</span></span>
<span data-ttu-id="f0c38-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="f0c38-112">Run the command as a job</span></span>

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

### <span data-ttu-id="f0c38-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0c38-113">-DefaultProfile</span></span>
<span data-ttu-id="f0c38-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f0c38-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f0c38-115">-MoveCollectionName</span><span class="sxs-lookup"><span data-stu-id="f0c38-115">-MoveCollectionName</span></span>
<span data-ttu-id="f0c38-116">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="f0c38-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="f0c38-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="f0c38-117">-NoWait</span></span>
<span data-ttu-id="f0c38-118">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="f0c38-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="f0c38-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0c38-119">-ResourceGroupName</span></span>
<span data-ttu-id="f0c38-120">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f0c38-120">The Resource Group Name.</span></span>

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

### <span data-ttu-id="f0c38-121">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f0c38-121">-SubscriptionId</span></span>
<span data-ttu-id="f0c38-122">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="f0c38-122">The Subscription ID.</span></span>

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

### <span data-ttu-id="f0c38-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f0c38-123">-Confirm</span></span>
<span data-ttu-id="f0c38-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0c38-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f0c38-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0c38-125">-WhatIf</span></span>
<span data-ttu-id="f0c38-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f0c38-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0c38-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f0c38-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f0c38-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0c38-128">CommonParameters</span></span>
<span data-ttu-id="f0c38-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0c38-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0c38-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f0c38-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0c38-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0c38-131">INPUTS</span></span>

## <span data-ttu-id="f0c38-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f0c38-132">OUTPUTS</span></span>

### <span data-ttu-id="f0c38-133">Microsoft. Azure. PowerShell. polecenia. ResourceMover. models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="f0c38-133">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="f0c38-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f0c38-134">NOTES</span></span>

<span data-ttu-id="f0c38-135">PISUJE</span><span class="sxs-lookup"><span data-stu-id="f0c38-135">ALIASES</span></span>

## <span data-ttu-id="f0c38-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0c38-136">RELATED LINKS</span></span>

