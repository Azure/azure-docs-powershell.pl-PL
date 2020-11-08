---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainTransactionNode.md
ms.openlocfilehash: db3fe0bd635b472dc6b747f6a1f9334d51df0764
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063627"
---
# <span data-ttu-id="3bb19-101">Remove-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="3bb19-101">Remove-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="3bb19-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3bb19-102">SYNOPSIS</span></span>
<span data-ttu-id="3bb19-103">Usuwanie węzła Transaction.</span><span class="sxs-lookup"><span data-stu-id="3bb19-103">Delete the transaction node.</span></span>

## <span data-ttu-id="3bb19-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3bb19-104">SYNTAX</span></span>

### <span data-ttu-id="3bb19-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3bb19-105">Delete (Default)</span></span>
```
Remove-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="3bb19-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="3bb19-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="3bb19-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3bb19-107">DESCRIPTION</span></span>
<span data-ttu-id="3bb19-108">Usuwanie węzła Transaction.</span><span class="sxs-lookup"><span data-stu-id="3bb19-108">Delete the transaction node.</span></span>

## <span data-ttu-id="3bb19-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3bb19-109">EXAMPLES</span></span>

### <span data-ttu-id="3bb19-110">Przykład 1: Usuwanie węzła transakcji</span><span class="sxs-lookup"><span data-stu-id="3bb19-110">Example 1: Remove a transaction node</span></span>
```powershell
PS C:\> Remove-AzBlockchainTransactionNode -Name transacnode002 -BlockchainMemberName dolauli002 -ResourceGroupName testgroup

```

<span data-ttu-id="3bb19-111">To polecenie powoduje usunięcie węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="3bb19-111">This command removes a transaction node.</span></span>

### <span data-ttu-id="3bb19-112">Przykład 2: Usuwanie węzła transakcji</span><span class="sxs-lookup"><span data-stu-id="3bb19-112">Example 2: Remove a transaction node</span></span>
```powershell
PS C:\> $node = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode003 -ResourceGroupName $env.resourceGroup 
PS C:\> Remove-AzBlockchainTransactionNode -InputObject $node
```

<span data-ttu-id="3bb19-113">To polecenie powoduje usunięcie węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="3bb19-113">This command removes a transaction node.</span></span>

## <span data-ttu-id="3bb19-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3bb19-114">PARAMETERS</span></span>

### <span data-ttu-id="3bb19-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3bb19-115">-AsJob</span></span>
<span data-ttu-id="3bb19-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="3bb19-116">Run the command as a job</span></span>

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

### <span data-ttu-id="3bb19-117">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="3bb19-117">-BlockchainMemberName</span></span>
<span data-ttu-id="3bb19-118">Nazwa członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="3bb19-118">Blockchain member name.</span></span>

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

### <span data-ttu-id="3bb19-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3bb19-119">-DefaultProfile</span></span>
<span data-ttu-id="3bb19-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3bb19-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3bb19-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="3bb19-121">-InputObject</span></span>
<span data-ttu-id="3bb19-122">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="3bb19-122">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="3bb19-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3bb19-123">-Name</span></span>
<span data-ttu-id="3bb19-124">Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="3bb19-124">Transaction node name.</span></span>

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

### <span data-ttu-id="3bb19-125">-Nowait</span><span class="sxs-lookup"><span data-stu-id="3bb19-125">-NoWait</span></span>
<span data-ttu-id="3bb19-126">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="3bb19-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="3bb19-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3bb19-127">-PassThru</span></span>
<span data-ttu-id="3bb19-128">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="3bb19-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="3bb19-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3bb19-129">-ResourceGroupName</span></span>
<span data-ttu-id="3bb19-130">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="3bb19-130">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="3bb19-131">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="3bb19-131">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="3bb19-132">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="3bb19-132">-SubscriptionId</span></span>
<span data-ttu-id="3bb19-133">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3bb19-133">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="3bb19-134">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3bb19-134">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="3bb19-135">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3bb19-135">-Confirm</span></span>
<span data-ttu-id="3bb19-136">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bb19-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3bb19-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3bb19-137">-WhatIf</span></span>
<span data-ttu-id="3bb19-138">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3bb19-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3bb19-139">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3bb19-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3bb19-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3bb19-140">CommonParameters</span></span>
<span data-ttu-id="3bb19-141">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3bb19-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3bb19-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3bb19-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3bb19-143">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3bb19-143">INPUTS</span></span>

### <span data-ttu-id="3bb19-144">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="3bb19-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="3bb19-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3bb19-145">OUTPUTS</span></span>

### <span data-ttu-id="3bb19-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="3bb19-146">System.Boolean</span></span>

## <span data-ttu-id="3bb19-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3bb19-147">NOTES</span></span>

<span data-ttu-id="3bb19-148">PISUJE</span><span class="sxs-lookup"><span data-stu-id="3bb19-148">ALIASES</span></span>

<span data-ttu-id="3bb19-149">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3bb19-149">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="3bb19-150">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="3bb19-150">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="3bb19-151">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="3bb19-151">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="3bb19-152">INPUTobject <IBlockchainIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="3bb19-152">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="3bb19-153">`[BlockchainMemberName <String>]`: Blockchain nazwa członka.</span><span class="sxs-lookup"><span data-stu-id="3bb19-153">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="3bb19-154">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="3bb19-154">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="3bb19-155">`[Location <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="3bb19-155">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="3bb19-156">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="3bb19-156">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="3bb19-157">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="3bb19-157">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="3bb19-158">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="3bb19-158">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="3bb19-159">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="3bb19-159">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="3bb19-160">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="3bb19-160">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="3bb19-161">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="3bb19-161">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="3bb19-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3bb19-162">RELATED LINKS</span></span>

