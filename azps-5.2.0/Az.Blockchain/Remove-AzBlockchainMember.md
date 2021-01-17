---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/remove-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Remove-AzBlockchainMember.md
ms.openlocfilehash: 56bed1addaa37a71396739a64bce9fe70e2f7f44
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98365402"
---
# <span data-ttu-id="9b259-101">Remove-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="9b259-101">Remove-AzBlockchainMember</span></span>

## <span data-ttu-id="9b259-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9b259-102">SYNOPSIS</span></span>
<span data-ttu-id="9b259-103">Usuwanie członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="9b259-103">Delete a blockchain member.</span></span>

## <span data-ttu-id="9b259-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9b259-104">SYNTAX</span></span>

### <span data-ttu-id="9b259-105">Usuń (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9b259-105">Delete (Default)</span></span>
```
Remove-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="9b259-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9b259-106">DeleteViaIdentity</span></span>
```
Remove-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="9b259-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9b259-107">DESCRIPTION</span></span>
<span data-ttu-id="9b259-108">Usuwanie członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="9b259-108">Delete a blockchain member.</span></span>

## <span data-ttu-id="9b259-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9b259-109">EXAMPLES</span></span>

### <span data-ttu-id="9b259-110">Przykład 1. Usuń członka Blockchain</span><span class="sxs-lookup"><span data-stu-id="9b259-110">Example 1: Remove a blockchain member</span></span>
```powershell
PS C:\> Remove-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

```

<span data-ttu-id="9b259-111">To polecenie usuwa członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="9b259-111">This command removes a blockchain member.</span></span>

### <span data-ttu-id="9b259-112">Przykład 2: Usuwanie członka Blockchain</span><span class="sxs-lookup"><span data-stu-id="9b259-112">Example 2: Remove a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup
PS C:\> Remove-AzBlockchainMember -InputObject $member

```

<span data-ttu-id="9b259-113">To polecenie usuwa członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="9b259-113">This command removes a blockchain member.</span></span>

## <span data-ttu-id="9b259-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b259-114">PARAMETERS</span></span>

### <span data-ttu-id="9b259-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9b259-115">-AsJob</span></span>
<span data-ttu-id="9b259-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="9b259-116">Run the command as a job</span></span>

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

### <span data-ttu-id="9b259-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b259-117">-DefaultProfile</span></span>
<span data-ttu-id="9b259-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9b259-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9b259-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9b259-119">-InputObject</span></span>
<span data-ttu-id="9b259-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="9b259-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9b259-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9b259-121">-Name</span></span>
<span data-ttu-id="9b259-122">Nazwa członka Blockchain</span><span class="sxs-lookup"><span data-stu-id="9b259-122">Blockchain member name</span></span>

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

### <span data-ttu-id="9b259-123">-Nowait</span><span class="sxs-lookup"><span data-stu-id="9b259-123">-NoWait</span></span>
<span data-ttu-id="9b259-124">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="9b259-124">Run the command asynchronously</span></span>

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

### <span data-ttu-id="9b259-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9b259-125">-PassThru</span></span>
<span data-ttu-id="9b259-126">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="9b259-126">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="9b259-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b259-127">-ResourceGroupName</span></span>
<span data-ttu-id="9b259-128">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="9b259-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="9b259-129">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="9b259-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="9b259-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9b259-130">-SubscriptionId</span></span>
<span data-ttu-id="9b259-131">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9b259-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="9b259-132">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="9b259-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="9b259-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9b259-133">-Confirm</span></span>
<span data-ttu-id="9b259-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b259-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9b259-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9b259-135">-WhatIf</span></span>
<span data-ttu-id="9b259-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9b259-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9b259-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9b259-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9b259-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b259-138">CommonParameters</span></span>
<span data-ttu-id="9b259-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9b259-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b259-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9b259-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b259-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9b259-141">INPUTS</span></span>

### <span data-ttu-id="9b259-142">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="9b259-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="9b259-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9b259-143">OUTPUTS</span></span>

### <span data-ttu-id="9b259-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9b259-144">System.Boolean</span></span>

## <span data-ttu-id="9b259-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9b259-145">NOTES</span></span>

<span data-ttu-id="9b259-146">PISUJE</span><span class="sxs-lookup"><span data-stu-id="9b259-146">ALIASES</span></span>

<span data-ttu-id="9b259-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9b259-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9b259-148">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="9b259-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9b259-149">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9b259-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9b259-150">INPUTobject <IBlockchainIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="9b259-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9b259-151">`[BlockchainMemberName <String>]`: Blockchain nazwa członka.</span><span class="sxs-lookup"><span data-stu-id="9b259-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="9b259-152">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="9b259-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9b259-153">`[Location <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="9b259-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="9b259-154">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="9b259-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="9b259-155">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="9b259-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="9b259-156">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="9b259-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="9b259-157">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="9b259-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="9b259-158">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="9b259-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="9b259-159">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="9b259-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="9b259-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9b259-160">RELATED LINKS</span></span>

