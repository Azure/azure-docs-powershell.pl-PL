---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: ca39d93f8cafbdf5b8895b6978a7558e1fc5b2a6
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317647"
---
# <span data-ttu-id="8c360-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="8c360-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="8c360-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8c360-102">SYNOPSIS</span></span>
<span data-ttu-id="8c360-103">Usuwa kolekcję Przenieś.</span><span class="sxs-lookup"><span data-stu-id="8c360-103">Deletes a move collection.</span></span>

## <span data-ttu-id="8c360-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8c360-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="8c360-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8c360-105">DESCRIPTION</span></span>
<span data-ttu-id="8c360-106">Usuwa kolekcję Przenieś.</span><span class="sxs-lookup"><span data-stu-id="8c360-106">Deletes a move collection.</span></span>

## <span data-ttu-id="8c360-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8c360-107">EXAMPLES</span></span>

### <span data-ttu-id="8c360-108">Przykład 1: usuwanie kolekcji Move z określonego abonamentu</span><span class="sxs-lookup"><span data-stu-id="8c360-108">Example 1: Remove the Move Collection from the specified subscription</span></span>
```powershell
PS C:\> Remove-AzResourceMoverMoveCollection -ResourceGroupName "RG-MoveCollection-demoRM" -MoveCollectionName "PS-centralus-westcentralus-demoRM"

    AdditionalInfo :
    Code           :
    Detail         :
    EndTime        : 8/12/2020 3:27:28 PM
    Id             : /subscriptions/e80eb9fa-c996-4435-aa32-5af6f3d3077c/resourceGroups/RG-MoveCollection-demoRM/providers/Microsoft.Migrate/MoveColl
                    ections/PS-centralus-westcentralus-demoRM/operations/3c2aae83-0a05-432c-be8e-a156351866c5
    Message        :
    Name           : 3c2aae83-0a05-432c-be8e-a156351866d6
    Property       : Microsoft.Azure.PowerShell.Cmdlets.RegionMove.Models.Api20191001Preview.OperationStatusProperties
    StartTime      : 8/12/2020 3:27:27 PM
    Status         : Succeeded
```

<span data-ttu-id="8c360-109">Usuwanie kolekcji Move z określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8c360-109">Remove the Move collection from the specified subscription.</span></span>

## <span data-ttu-id="8c360-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c360-110">PARAMETERS</span></span>

### <span data-ttu-id="8c360-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8c360-111">-AsJob</span></span>
<span data-ttu-id="8c360-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="8c360-112">Run the command as a job</span></span>

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

### <span data-ttu-id="8c360-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c360-113">-DefaultProfile</span></span>
<span data-ttu-id="8c360-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c360-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c360-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8c360-115">-Name</span></span>
<span data-ttu-id="8c360-116">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="8c360-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="8c360-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="8c360-117">-NoWait</span></span>
<span data-ttu-id="8c360-118">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="8c360-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="8c360-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="8c360-119">-PassThru</span></span>
<span data-ttu-id="8c360-120">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="8c360-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="8c360-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c360-121">-ResourceGroupName</span></span>
<span data-ttu-id="8c360-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c360-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="8c360-123">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8c360-123">-SubscriptionId</span></span>
<span data-ttu-id="8c360-124">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="8c360-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="8c360-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c360-125">-Confirm</span></span>
<span data-ttu-id="8c360-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c360-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c360-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c360-127">-WhatIf</span></span>
<span data-ttu-id="8c360-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c360-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c360-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8c360-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c360-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c360-130">CommonParameters</span></span>
<span data-ttu-id="8c360-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c360-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c360-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c360-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c360-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c360-133">INPUTS</span></span>

## <span data-ttu-id="8c360-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8c360-134">OUTPUTS</span></span>

### <span data-ttu-id="8c360-135">Microsoft. Azure. PowerShell. polecenia. ResourceMover. models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="8c360-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="8c360-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8c360-136">NOTES</span></span>

<span data-ttu-id="8c360-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="8c360-137">ALIASES</span></span>

## <span data-ttu-id="8c360-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c360-138">RELATED LINKS</span></span>

