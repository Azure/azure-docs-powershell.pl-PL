---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: db3fe0bd635b472dc6b747f6a1f9334d51df0764
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177939"
---
# <span data-ttu-id="d29d0-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="d29d0-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="d29d0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d29d0-102">SYNOPSIS</span></span>
<span data-ttu-id="d29d0-103">Usuń węzeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="d29d0-103">Delete the transaction node.</span></span>

## <span data-ttu-id="d29d0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d29d0-104">SYNTAX</span></span>

### <span data-ttu-id="d29d0-105">Delete (Default)</span><span class="sxs-lookup"><span data-stu-id="d29d0-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="d29d0-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d29d0-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d29d0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d29d0-107">DESCRIPTION</span></span>
<span data-ttu-id="d29d0-108">Usuń węzeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="d29d0-108">Delete the transaction node.</span></span>

## <span data-ttu-id="d29d0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d29d0-109">EXAMPLES</span></span>

### <span data-ttu-id="d29d0-110">Przykład 1. Usuwanie węzła transakcji</span><span class="sxs-lookup"><span data-stu-id="d29d0-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="d29d0-111">To polecenie usuwa węzeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="d29d0-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="d29d0-112">Przykład 2. Usuwanie węzła transakcji</span><span class="sxs-lookup"><span data-stu-id="d29d0-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="d29d0-113">To polecenie usuwa węzeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="d29d0-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="d29d0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d29d0-114">PARAMETERS</span></span>

### <span data-ttu-id="d29d0-115">— AsJob</span><span class="sxs-lookup"><span data-stu-id="d29d0-115">-AsJob</span></span>
<span data-ttu-id="d29d0-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="d29d0-116">Run the command as a job</span></span>

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

### <span data-ttu-id="d29d0-117">-Wymusz na użytkownikach</span><span class="sxs-lookup"><span data-stu-id="d29d0-117">-BlockchainMemberName</span></span>
<span data-ttu-id="d29d0-118">Nie ma w tym celu nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d29d0-118">Blockchain member name.</span></span>

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

### <span data-ttu-id="d29d0-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d29d0-119">-DefaultProfile</span></span>
<span data-ttu-id="d29d0-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d29d0-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d29d0-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d29d0-121">-InputObject</span></span>
<span data-ttu-id="d29d0-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d29d0-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d29d0-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d29d0-123">-Name</span></span>
<span data-ttu-id="d29d0-124">Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="d29d0-124">Transaction node name.</span></span>

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

### <span data-ttu-id="d29d0-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="d29d0-125">-NoWait</span></span>
<span data-ttu-id="d29d0-126">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="d29d0-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="d29d0-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d29d0-127">-PassThru</span></span>
<span data-ttu-id="d29d0-128">Zwraca wartość prawda, gdy polecenie zakończy się powodzeniem.</span><span class="sxs-lookup"><span data-stu-id="d29d0-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="d29d0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d29d0-129">-ResourceGroupName</span></span>
<span data-ttu-id="d29d0-130">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="d29d0-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d29d0-131">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="d29d0-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="d29d0-132">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d29d0-132">-SubscriptionId</span></span>
<span data-ttu-id="d29d0-133">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d29d0-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d29d0-134">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia usługi.</span><span class="sxs-lookup"><span data-stu-id="d29d0-134">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d29d0-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d29d0-135">-Confirm</span></span>
<span data-ttu-id="d29d0-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d29d0-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d29d0-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d29d0-137">-WhatIf</span></span>
<span data-ttu-id="d29d0-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d29d0-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d29d0-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d29d0-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d29d0-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d29d0-140">CommonParameters</span></span>
<span data-ttu-id="d29d0-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d29d0-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d29d0-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d29d0-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d29d0-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d29d0-143">INPUTS</span></span>

### <span data-ttu-id="d29d0-144">Microsoft.Azure.PowerShell.cmdlet.uściśl.models.iBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="d29d0-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="d29d0-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d29d0-145">OUTPUTS</span></span>

### <span data-ttu-id="d29d0-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d29d0-146">System.Boolean</span></span>

## <span data-ttu-id="d29d0-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d29d0-147">NOTES</span></span>

<span data-ttu-id="d29d0-148">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d29d0-148">ALIASES</span></span>

<span data-ttu-id="d29d0-149">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="d29d0-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d29d0-150">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótu zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d29d0-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d29d0-151">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d29d0-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d29d0-152">INPUTOBJECT: <IBlockchainIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="d29d0-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d29d0-153">`[BlockchainMemberName <String>]`: Dodano nazwę członka.</span><span class="sxs-lookup"><span data-stu-id="d29d0-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="d29d0-154">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d29d0-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d29d0-155">`[Location <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d29d0-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="d29d0-156">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="d29d0-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="d29d0-157">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="d29d0-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d29d0-158">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="d29d0-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d29d0-159">`[SubscriptionId <String>]`: pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d29d0-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="d29d0-160">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia usługi.</span><span class="sxs-lookup"><span data-stu-id="d29d0-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="d29d0-161">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="d29d0-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="d29d0-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d29d0-162">RELATED LINKS</span></span>

