---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 56bed1addaa37a71396739a64bce9fe70e2f7f44
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225777"
---
# <span data-ttu-id="b3f70-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="b3f70-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="b3f70-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b3f70-102">SYNOPSIS</span></span>
<span data-ttu-id="b3f70-103">Usuwanie członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="b3f70-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="b3f70-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b3f70-104">SYNTAX</span></span>

### <span data-ttu-id="b3f70-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="b3f70-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b3f70-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="b3f70-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b3f70-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b3f70-107">DESCRIPTION</span></span>
<span data-ttu-id="b3f70-108">Usuwanie członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="b3f70-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="b3f70-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b3f70-109">EXAMPLES</span></span>

### <span data-ttu-id="b3f70-110">Przykład 1. Usuń członka Blockchain</span><span class="sxs-lookup"><span data-stu-id="b3f70-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="b3f70-111">To polecenie usuwa członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="b3f70-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="b3f70-112">Przykład 2: Usuwanie członka Blockchain</span><span class="sxs-lookup"><span data-stu-id="b3f70-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="b3f70-113">To polecenie usuwa członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="b3f70-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="b3f70-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3f70-114">PARAMETERS</span></span>

### <span data-ttu-id="b3f70-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b3f70-115">-AsJob</span></span>
<span data-ttu-id="b3f70-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="b3f70-116">Run the command as a job</span></span>

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

### <span data-ttu-id="b3f70-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3f70-117">-DefaultProfile</span></span>
<span data-ttu-id="b3f70-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b3f70-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b3f70-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b3f70-119">-InputObject</span></span>
<span data-ttu-id="b3f70-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="b3f70-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b3f70-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b3f70-121">-Name</span></span>
<span data-ttu-id="b3f70-122">Nazwa członka Blockchain</span><span class="sxs-lookup"><span data-stu-id="b3f70-122">Blockchain member name</span></span>

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

### <span data-ttu-id="b3f70-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="b3f70-123">-NoWait</span></span>
<span data-ttu-id="b3f70-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="b3f70-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="b3f70-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b3f70-125">-PassThru</span></span>
<span data-ttu-id="b3f70-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="b3f70-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="b3f70-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3f70-127">-ResourceGroupName</span></span>
<span data-ttu-id="b3f70-128">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="b3f70-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b3f70-129">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="b3f70-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b3f70-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b3f70-130">-SubscriptionId</span></span>
<span data-ttu-id="b3f70-131">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b3f70-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b3f70-132">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="b3f70-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b3f70-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3f70-133">-Confirm</span></span>
<span data-ttu-id="b3f70-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3f70-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3f70-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3f70-135">-WhatIf</span></span>
<span data-ttu-id="b3f70-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3f70-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3f70-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b3f70-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3f70-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3f70-138">CommonParameters</span></span>
<span data-ttu-id="b3f70-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3f70-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3f70-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b3f70-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3f70-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3f70-141">INPUTS</span></span>

### <span data-ttu-id="b3f70-142">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="b3f70-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="b3f70-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b3f70-143">OUTPUTS</span></span>

### <span data-ttu-id="b3f70-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="b3f70-144">System.Boolean</span></span>

## <span data-ttu-id="b3f70-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b3f70-145">NOTES</span></span>

<span data-ttu-id="b3f70-146">PISUJE</span><span class="sxs-lookup"><span data-stu-id="b3f70-146">ALIASES</span></span>

<span data-ttu-id="b3f70-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b3f70-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b3f70-148">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b3f70-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b3f70-149">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b3f70-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b3f70-150">INPUTobject <IBlockchainIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="b3f70-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b3f70-151">`[BlockchainMemberName <String>]`: Blockchain nazwa członka.</span><span class="sxs-lookup"><span data-stu-id="b3f70-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="b3f70-152">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b3f70-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b3f70-153">`[Location <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b3f70-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="b3f70-154">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="b3f70-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="b3f70-155">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="b3f70-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b3f70-156">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="b3f70-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b3f70-157">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b3f70-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="b3f70-158">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="b3f70-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="b3f70-159">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="b3f70-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="b3f70-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3f70-160">RELATED LINKS</span></span>

