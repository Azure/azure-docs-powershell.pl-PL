---
external help file: ''
Module Name: Az.ResourceMover
online version: https://docs.microsoft.com/en-us/powershell/module/az.resourcemover/remove-azresourcemovermovecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ResourceMover/help/Remove-AzResourceMoverMoveCollection.md
ms.openlocfilehash: ca39d93f8cafbdf5b8895b6978a7558e1fc5b2a6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94222973"
---
# <span data-ttu-id="218dc-101">Remove-AzResourceMoverMoveCollection</span><span class="sxs-lookup"><span data-stu-id="218dc-101">Remove-AzResourceMoverMoveCollection</span></span>

## <span data-ttu-id="218dc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="218dc-102">SYNOPSIS</span></span>
<span data-ttu-id="218dc-103">Usuwa kolekcję Przenieś.</span><span class="sxs-lookup"><span data-stu-id="218dc-103">Deletes a move collection.</span></span>

## <span data-ttu-id="218dc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="218dc-104">SYNTAX</span></span>

```
Remove-AzResourceMoverMoveCollection -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="218dc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="218dc-105">DESCRIPTION</span></span>
<span data-ttu-id="218dc-106">Usuwa kolekcję Przenieś.</span><span class="sxs-lookup"><span data-stu-id="218dc-106">Deletes a move collection.</span></span>

## <span data-ttu-id="218dc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="218dc-107">EXAMPLES</span></span>

### <span data-ttu-id="218dc-108">Przykład 1: usuwanie kolekcji Move z określonego abonamentu</span><span class="sxs-lookup"><span data-stu-id="218dc-108">Example 1: Remove the Move Collection from the specified subscription</span></span>
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

<span data-ttu-id="218dc-109">Usuwanie kolekcji Move z określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="218dc-109">Remove the Move collection from the specified subscription.</span></span>

## <span data-ttu-id="218dc-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="218dc-110">PARAMETERS</span></span>

### <span data-ttu-id="218dc-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="218dc-111">-AsJob</span></span>
<span data-ttu-id="218dc-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="218dc-112">Run the command as a job</span></span>

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

### <span data-ttu-id="218dc-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="218dc-113">-DefaultProfile</span></span>
<span data-ttu-id="218dc-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="218dc-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="218dc-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="218dc-115">-Name</span></span>
<span data-ttu-id="218dc-116">Nazwa kolekcji przenoszenia.</span><span class="sxs-lookup"><span data-stu-id="218dc-116">The Move Collection Name.</span></span>

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

### <span data-ttu-id="218dc-117">-Nowait</span><span class="sxs-lookup"><span data-stu-id="218dc-117">-NoWait</span></span>
<span data-ttu-id="218dc-118">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="218dc-118">Run the command asynchronously</span></span>

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

### <span data-ttu-id="218dc-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="218dc-119">-PassThru</span></span>
<span data-ttu-id="218dc-120">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="218dc-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="218dc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="218dc-121">-ResourceGroupName</span></span>
<span data-ttu-id="218dc-122">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="218dc-122">The Resource Group Name.</span></span>

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

### <span data-ttu-id="218dc-123">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="218dc-123">-SubscriptionId</span></span>
<span data-ttu-id="218dc-124">Identyfikator abonamentu.</span><span class="sxs-lookup"><span data-stu-id="218dc-124">The Subscription ID.</span></span>

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

### <span data-ttu-id="218dc-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="218dc-125">-Confirm</span></span>
<span data-ttu-id="218dc-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="218dc-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="218dc-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="218dc-127">-WhatIf</span></span>
<span data-ttu-id="218dc-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="218dc-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="218dc-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="218dc-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="218dc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="218dc-130">CommonParameters</span></span>
<span data-ttu-id="218dc-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="218dc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="218dc-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="218dc-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="218dc-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="218dc-133">INPUTS</span></span>

## <span data-ttu-id="218dc-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="218dc-134">OUTPUTS</span></span>

### <span data-ttu-id="218dc-135">Microsoft. Azure. PowerShell. polecenia. ResourceMover. models. Api20191001Preview. IOperationStatus</span><span class="sxs-lookup"><span data-stu-id="218dc-135">Microsoft.Azure.PowerShell.Cmdlets.ResourceMover.Models.Api20191001Preview.IOperationStatus</span></span>

## <span data-ttu-id="218dc-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="218dc-136">NOTES</span></span>

<span data-ttu-id="218dc-137">PISUJE</span><span class="sxs-lookup"><span data-stu-id="218dc-137">ALIASES</span></span>

## <span data-ttu-id="218dc-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="218dc-138">RELATED LINKS</span></span>

