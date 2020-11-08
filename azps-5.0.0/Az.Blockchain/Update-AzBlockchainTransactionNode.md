---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainTransactionNode.md
ms.openlocfilehash: dcff41ecac3181da09ee2f1cf0673e4225c2802d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225884"
---
# <span data-ttu-id="32281-101">Update-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="32281-101">Update-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="32281-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="32281-102">SYNOPSIS</span></span>
<span data-ttu-id="32281-103">Aktualizowanie węzła Transaction.</span><span class="sxs-lookup"><span data-stu-id="32281-103">Update the transaction node.</span></span>

## <span data-ttu-id="32281-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="32281-104">SYNTAX</span></span>

### <span data-ttu-id="32281-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="32281-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="32281-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="32281-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="32281-107">Opis</span><span class="sxs-lookup"><span data-stu-id="32281-107">DESCRIPTION</span></span>
<span data-ttu-id="32281-108">Aktualizowanie węzła Transaction.</span><span class="sxs-lookup"><span data-stu-id="32281-108">Update the transaction node.</span></span>

## <span data-ttu-id="32281-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="32281-109">EXAMPLES</span></span>

### <span data-ttu-id="32281-110">Przykład 1: aktualizowanie węzła transkationowego</span><span class="sxs-lookup"><span data-stu-id="32281-110">Example 1: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key1'='update'}
PS C:\> Update-AzBlockchainTransactionNode -BlockchainMemberName dolauli002 -Name transacnode002 -ResourceGroupName testgroup -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="32281-111">To polecenie powoduje zaktualizowanie węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="32281-111">This command updates a transaction node.</span></span>

### <span data-ttu-id="32281-112">Przykład 2: aktualizowanie węzła transkationowego</span><span class="sxs-lookup"><span data-stu-id="32281-112">Example 2: Update a transcation node</span></span>
```powershell
PS C:\> $tag = @{'key2'='update'}
PS C:\> $tNode = Get-AzBlockchainMember -BlockchainMemberName dolauli002 -ResourceGroupName testgroup -Name transacnode002
PS C:\> Update-AzBlockchainTransactionNode -InputObject $tNode -Tag $tag

Name           Type                                                    Location
----           ----                                                    --------
transacnode002 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="32281-113">To polecenie powoduje zaktualizowanie węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="32281-113">This command updates a transaction node.</span></span>

## <span data-ttu-id="32281-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="32281-114">PARAMETERS</span></span>

### <span data-ttu-id="32281-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="32281-115">-BlockchainMemberName</span></span>
<span data-ttu-id="32281-116">Nazwa członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="32281-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="32281-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="32281-117">-DefaultProfile</span></span>
<span data-ttu-id="32281-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="32281-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="32281-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="32281-119">-FirewallRule</span></span>
<span data-ttu-id="32281-120">Pobiera lub ustawia reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="32281-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="32281-121">Aby skonstruować, zobacz sekcję notatki dla właściwości FIREWALLRULE i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="32281-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="32281-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="32281-122">-InputObject</span></span>
<span data-ttu-id="32281-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="32281-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="32281-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="32281-124">-Name</span></span>
<span data-ttu-id="32281-125">Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="32281-125">Transaction node name.</span></span>

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

### <span data-ttu-id="32281-126">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="32281-126">-Password</span></span>
<span data-ttu-id="32281-127">Ustawia hasło uwierzytelniania podstawowego dla punktu końcowego DNS węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="32281-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="32281-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="32281-128">-ResourceGroupName</span></span>
<span data-ttu-id="32281-129">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="32281-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="32281-130">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="32281-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="32281-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="32281-131">-SubscriptionId</span></span>
<span data-ttu-id="32281-132">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="32281-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="32281-133">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="32281-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="32281-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="32281-134">-Confirm</span></span>
<span data-ttu-id="32281-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32281-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="32281-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="32281-136">-WhatIf</span></span>
<span data-ttu-id="32281-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="32281-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="32281-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="32281-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="32281-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32281-139">CommonParameters</span></span>
<span data-ttu-id="32281-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="32281-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32281-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="32281-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32281-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="32281-142">INPUTS</span></span>

### <span data-ttu-id="32281-143">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="32281-143">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="32281-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="32281-144">OUTPUTS</span></span>

### <span data-ttu-id="32281-145">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="32281-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="32281-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="32281-146">NOTES</span></span>

<span data-ttu-id="32281-147">PISUJE</span><span class="sxs-lookup"><span data-stu-id="32281-147">ALIASES</span></span>

<span data-ttu-id="32281-148">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="32281-148">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="32281-149">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="32281-149">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="32281-150">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="32281-150">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="32281-151">FIREWALLRULE <IFirewallRule [] >: Pobiera lub ustawia reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="32281-151">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="32281-152">`[EndIPAddress <String>]`: Pobiera lub ustawia końcowy adres IP zakresu reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="32281-152">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="32281-153">`[RuleName <String>]`: Pobiera lub ustawia nazwy reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="32281-153">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="32281-154">`[StartIPAddress <String>]`: Pobiera lub ustawia początkowy adres IP zakresu reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="32281-154">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="32281-155">INPUTobject <IBlockchainIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="32281-155">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="32281-156">`[BlockchainMemberName <String>]`: Blockchain nazwa członka.</span><span class="sxs-lookup"><span data-stu-id="32281-156">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="32281-157">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="32281-157">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="32281-158">`[Location <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="32281-158">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="32281-159">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="32281-159">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="32281-160">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="32281-160">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="32281-161">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="32281-161">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="32281-162">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="32281-162">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="32281-163">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="32281-163">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="32281-164">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="32281-164">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="32281-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="32281-165">RELATED LINKS</span></span>

