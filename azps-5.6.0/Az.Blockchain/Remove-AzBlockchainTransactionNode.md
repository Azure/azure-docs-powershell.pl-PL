---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: 3de49353a19afbce6ed8996fc5dd7cdeccca1627
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992916"
---
# <span data-ttu-id="20912-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="20912-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="20912-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20912-102">SYNOPSIS</span></span>
<span data-ttu-id="20912-103">Usuń węzeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="20912-103">Delete the transaction node.</span></span>

## <span data-ttu-id="20912-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="20912-104">SYNTAX</span></span>

### <span data-ttu-id="20912-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="20912-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="20912-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="20912-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="20912-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="20912-107">DESCRIPTION</span></span>
<span data-ttu-id="20912-108">Usuń węzeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="20912-108">Delete the transaction node.</span></span>

## <span data-ttu-id="20912-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="20912-109">EXAMPLES</span></span>

### <span data-ttu-id="20912-110">Przykład 1. Usuwanie węzła transakcji</span><span class="sxs-lookup"><span data-stu-id="20912-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="20912-111">To polecenie usuwa węzeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="20912-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="20912-112">Przykład 2. Usuwanie węzła transakcji</span><span class="sxs-lookup"><span data-stu-id="20912-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="20912-113">To polecenie usuwa węzeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="20912-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="20912-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="20912-114">PARAMETERS</span></span>

### <span data-ttu-id="20912-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="20912-115">-AsJob</span></span>
<span data-ttu-id="20912-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="20912-116">Run the command as a job</span></span>

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

### <span data-ttu-id="20912-117">-Wymusz na użytkownikach</span><span class="sxs-lookup"><span data-stu-id="20912-117">-BlockchainMemberName</span></span>
<span data-ttu-id="20912-118">Nie ma w tym celu nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="20912-118">Blockchain member name.</span></span>

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

### <span data-ttu-id="20912-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20912-119">-DefaultProfile</span></span>
<span data-ttu-id="20912-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="20912-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="20912-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="20912-121">-InputObject</span></span>
<span data-ttu-id="20912-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="20912-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="20912-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="20912-123">-Name</span></span>
<span data-ttu-id="20912-124">Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="20912-124">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="20912-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="20912-125">-NoWait</span></span>
<span data-ttu-id="20912-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="20912-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="20912-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="20912-127">-PassThru</span></span>
<span data-ttu-id="20912-128">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="20912-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="20912-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20912-129">-ResourceGroupName</span></span>
<span data-ttu-id="20912-130">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="20912-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="20912-131">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="20912-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="20912-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="20912-132">-SubscriptionId</span></span>
<span data-ttu-id="20912-133">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="20912-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="20912-134">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="20912-134">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="20912-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="20912-135">-Confirm</span></span>
<span data-ttu-id="20912-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="20912-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20912-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20912-137">-WhatIf</span></span>
<span data-ttu-id="20912-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="20912-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="20912-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="20912-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20912-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20912-140">CommonParameters</span></span>
<span data-ttu-id="20912-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20912-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20912-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="20912-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20912-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20912-143">INPUTS</span></span>

### <span data-ttu-id="20912-144">Microsoft.Azure.PowerShell.cmdlet.uściśl.models.iBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="20912-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="20912-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20912-145">OUTPUTS</span></span>

### <span data-ttu-id="20912-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="20912-146">System.Boolean</span></span>

## <span data-ttu-id="20912-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="20912-147">NOTES</span></span>

<span data-ttu-id="20912-148">ALIASY</span><span class="sxs-lookup"><span data-stu-id="20912-148">ALIASES</span></span>

<span data-ttu-id="20912-149">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20912-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="20912-150">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="20912-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="20912-151">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="20912-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="20912-152">INPUTOBJECT: <IBlockchainIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="20912-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="20912-153">`[BlockchainMemberName <String>]`: Dodano nazwę członka.</span><span class="sxs-lookup"><span data-stu-id="20912-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="20912-154">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="20912-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="20912-155">`[Location <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="20912-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="20912-156">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="20912-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="20912-157">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="20912-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="20912-158">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="20912-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="20912-159">`[SubscriptionId <String>]`: pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="20912-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="20912-160">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="20912-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="20912-161">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="20912-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="20912-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20912-162">RELATED LINKS</span></span>

