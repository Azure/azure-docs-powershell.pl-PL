---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 54678dd00a0edae4af3a90c84e1c930c1c032e84
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972129"
---
# <span data-ttu-id="9a5be-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="9a5be-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="9a5be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a5be-102">SYNOPSIS</span></span>
<span data-ttu-id="9a5be-103">Usuwanie członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="9a5be-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="9a5be-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9a5be-104">SYNTAX</span></span>

### <span data-ttu-id="9a5be-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="9a5be-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9a5be-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9a5be-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9a5be-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="9a5be-107">DESCRIPTION</span></span>
<span data-ttu-id="9a5be-108">Usuwanie członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="9a5be-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="9a5be-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9a5be-109">EXAMPLES</span></span>

### <span data-ttu-id="9a5be-110">Przykład 1. Usuwanie członka zespołu</span><span class="sxs-lookup"><span data-stu-id="9a5be-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="9a5be-111">To polecenie usuwa członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="9a5be-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="9a5be-112">Przykład 2. Usuwanie członka zespołu</span><span class="sxs-lookup"><span data-stu-id="9a5be-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="9a5be-113">To polecenie usuwa członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="9a5be-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="9a5be-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a5be-114">PARAMETERS</span></span>

### <span data-ttu-id="9a5be-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="9a5be-115">-AsJob</span></span>
<span data-ttu-id="9a5be-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="9a5be-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9a5be-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a5be-117">-DefaultProfile</span></span>
<span data-ttu-id="9a5be-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9a5be-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a5be-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a5be-119">-InputObject</span></span>
<span data-ttu-id="9a5be-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="9a5be-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a5be-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9a5be-121">-Name</span></span>
<span data-ttu-id="9a5be-122">Name (Nazwa członka)</span><span class="sxs-lookup"><span data-stu-id="9a5be-122">Blockchain member name</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5be-123">-NoWait</span><span class="sxs-lookup"><span data-stu-id="9a5be-123">-NoWait</span></span>
<span data-ttu-id="9a5be-124">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="9a5be-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9a5be-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9a5be-125">-PassThru</span></span>
<span data-ttu-id="9a5be-126">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="9a5be-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9a5be-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a5be-127">-ResourceGroupName</span></span>
<span data-ttu-id="9a5be-128">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="9a5be-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9a5be-129">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="9a5be-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5be-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="9a5be-130">-SubscriptionId</span></span>
<span data-ttu-id="9a5be-131">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9a5be-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9a5be-132">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="9a5be-132">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a5be-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a5be-133">-Confirm</span></span>
<span data-ttu-id="9a5be-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9a5be-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a5be-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a5be-135">-WhatIf</span></span>
<span data-ttu-id="9a5be-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a5be-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a5be-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9a5be-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a5be-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a5be-138">CommonParameters</span></span>
<span data-ttu-id="9a5be-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a5be-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a5be-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9a5be-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a5be-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a5be-141">INPUTS</span></span>

### <span data-ttu-id="9a5be-142">Microsoft.Azure.PowerShell.cmdlet.uściśl.models.iBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="9a5be-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="9a5be-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a5be-143">OUTPUTS</span></span>

### <span data-ttu-id="9a5be-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9a5be-144">System.Boolean</span></span>

## <span data-ttu-id="9a5be-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9a5be-145">NOTES</span></span>

<span data-ttu-id="9a5be-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="9a5be-146">ALIASES</span></span>

<span data-ttu-id="9a5be-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a5be-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9a5be-148">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="9a5be-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9a5be-149">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9a5be-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9a5be-150">INPUTOBJECT: <IBlockchainIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="9a5be-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9a5be-151">`[BlockchainMemberName <String>]`: Dodano nazwę członka.</span><span class="sxs-lookup"><span data-stu-id="9a5be-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="9a5be-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="9a5be-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9a5be-153">`[Location <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="9a5be-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="9a5be-154">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="9a5be-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="9a5be-155">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="9a5be-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="9a5be-156">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="9a5be-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="9a5be-157">`[SubscriptionId <String>]`: pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9a5be-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="9a5be-158">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="9a5be-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="9a5be-159">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="9a5be-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="9a5be-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a5be-160">RELATED LINKS</span></span>

