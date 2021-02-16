---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
ms.openlocfilehash: dcff41ecac3181da09ee2f1cf0673e4225c2802d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177891"
---
# <span data-ttu-id="d1324-101">Update-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="d1324-101">Update-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="d1324-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1324-102">SYNOPSIS</span></span>
<span data-ttu-id="d1324-103">Zaktualizuj węzeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="d1324-103">Update the transaction node.</span></span>

## <span data-ttu-id="d1324-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d1324-104">SYNTAX</span></span>

### <span data-ttu-id="d1324-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="d1324-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="d1324-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="d1324-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="d1324-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d1324-107">DESCRIPTION</span></span>
<span data-ttu-id="d1324-108">Zaktualizuj węzeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="d1324-108">Update the transaction node.</span></span>

## <span data-ttu-id="d1324-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d1324-109">EXAMPLES</span></span>

### <span data-ttu-id="d1324-110">Przykład 1. Aktualizowanie węzła transkacji</span><span class="sxs-lookup"><span data-stu-id="d1324-110">Example 1: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key1'='update'}
PS C:\> Update-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode002 -ResourceGroupName testgroup -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="d1324-111">To polecenie aktualizuje węzeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="d1324-111">This command updates a transaction node.</span></span>

### <span data-ttu-id="d1324-112">Przykład 2. Aktualizowanie węzła transkacji</span><span class="sxs-lookup"><span data-stu-id="d1324-112">Example 2: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key2'='update'}
PS C:\> $tNode = Get-AzBlockchainMember -BlockchainMemberName dolauli002 -ResourceGroupName testgroup -Name transacnode002
PS C:\> Update-AzBlockchainTransactionNode -InputObject $tNode -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="d1324-113">To polecenie aktualizuje węzeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="d1324-113">This command updates a transaction node.</span></span>

## <span data-ttu-id="d1324-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d1324-114">PARAMETERS</span></span>

### <span data-ttu-id="d1324-115">-Nawiązywane NazwyMemberów</span><span class="sxs-lookup"><span data-stu-id="d1324-115">-BlockchainMemberName</span></span>
<span data-ttu-id="d1324-116">Nie ma w tym celu nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="d1324-116">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1324-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1324-117">-DefaultProfile</span></span>
<span data-ttu-id="d1324-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d1324-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1324-119">- FirewallRule</span><span class="sxs-lookup"><span data-stu-id="d1324-119">-FirewallRule</span></span>
<span data-ttu-id="d1324-120">Pobiera lub ustawia reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="d1324-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="d1324-121">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach FIREWALLRULE i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="d1324-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IFirewallRule[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1324-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1324-122">-InputObject</span></span>
<span data-ttu-id="d1324-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="d1324-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1324-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d1324-124">-Name</span></span>
<span data-ttu-id="d1324-125">Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="d1324-125">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1324-126">— Hasło</span><span class="sxs-lookup"><span data-stu-id="d1324-126">-Password</span></span>
<span data-ttu-id="d1324-127">Ustawia hasło uwierzytelniania podstawowego punktu końcowego dns węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="d1324-127">Sets the transaction node dns endpoint basic auth password.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1324-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1324-128">-ResourceGroupName</span></span>
<span data-ttu-id="d1324-129">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="d1324-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="d1324-130">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="d1324-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1324-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1324-131">-SubscriptionId</span></span>
<span data-ttu-id="d1324-132">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d1324-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="d1324-133">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia usługi.</span><span class="sxs-lookup"><span data-stu-id="d1324-133">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1324-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d1324-134">-Confirm</span></span>
<span data-ttu-id="d1324-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d1324-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1324-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1324-136">-WhatIf</span></span>
<span data-ttu-id="d1324-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d1324-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1324-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d1324-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1324-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1324-139">CommonParameters</span></span>
<span data-ttu-id="d1324-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d1324-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1324-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d1324-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1324-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d1324-142">INPUTS</span></span>

### <span data-ttu-id="d1324-143">Microsoft.Azure.PowerShell.cmdlet.uściśl.models.iBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="d1324-143">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="d1324-144">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d1324-144">OUTPUTS</span></span>

### <span data-ttu-id="d1324-145">Microsoft.Azure.PowerShell.cmdlet.udziec.models.api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="d1324-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="d1324-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d1324-146">NOTES</span></span>

<span data-ttu-id="d1324-147">ALIASY</span><span class="sxs-lookup"><span data-stu-id="d1324-147">ALIASES</span></span>

<span data-ttu-id="d1324-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d1324-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="d1324-149">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="d1324-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d1324-150">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="d1324-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="d1324-151">FIREWALLRULE <IFirewallRule[]>: Pobiera lub ustawia reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="d1324-151">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="d1324-152">`[EndIPAddress <String>]`: pobiera lub ustawia końcowy adres IP zakresu reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="d1324-152">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="d1324-153">`[RuleName <String>]`: pobiera lub ustawia nazwę reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="d1324-153">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="d1324-154">`[StartIPAddress <String>]`: pobiera lub ustawia pierwszy adres IP zakresu reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="d1324-154">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="d1324-155">INPUTOBJECT: <IBlockchainIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="d1324-155">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d1324-156">`[BlockchainMemberName <String>]`: Dodano nazwę członka.</span><span class="sxs-lookup"><span data-stu-id="d1324-156">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="d1324-157">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="d1324-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d1324-158">`[Location <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d1324-158">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="d1324-159">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="d1324-159">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="d1324-160">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="d1324-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="d1324-161">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="d1324-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="d1324-162">`[SubscriptionId <String>]`: pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="d1324-162">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="d1324-163">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia usługi.</span><span class="sxs-lookup"><span data-stu-id="d1324-163">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="d1324-164">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="d1324-164">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="d1324-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d1324-165">RELATED LINKS</span></span>

