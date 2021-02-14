---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
ms.openlocfilehash: 708ad613c2dbab7e7224dbd392809d9502c9b447
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181955"
---
# <span data-ttu-id="231b1-101">Update-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="231b1-101">Update-AzBlockchainMember</span></span>

## <span data-ttu-id="231b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="231b1-102">SYNOPSIS</span></span>
<span data-ttu-id="231b1-103">Zaktualizuj członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="231b1-103">Update a blockchain member.</span></span>

## <span data-ttu-id="231b1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="231b1-104">SYNTAX</span></span>

### <span data-ttu-id="231b1-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="231b1-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="231b1-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="231b1-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainMember -InputObject <IBlockchainIdentity>
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="231b1-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="231b1-107">DESCRIPTION</span></span>
<span data-ttu-id="231b1-108">Zaktualizuj członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="231b1-108">Update a blockchain member.</span></span>

## <span data-ttu-id="231b1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="231b1-109">EXAMPLES</span></span>

### <span data-ttu-id="231b1-110">Przykład 1. Aktualizowanie członka zespołu</span><span class="sxs-lookup"><span data-stu-id="231b1-110">Example 1: Update a blockchain member</span></span>
```powershell
PS C:\> $passwd2 = 'strongMemberAccountPassword@2' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Update-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Password $passwd2

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="231b1-111">To polecenie aktualizuje członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="231b1-111">This command updates a blockchain member.</span></span>

### <span data-ttu-id="231b1-112">Przykład 2. Aktualizowanie członka zespołu</span><span class="sxs-lookup"><span data-stu-id="231b1-112">Example 2: Update a blockchain member</span></span>
```powershell
PS C:\> $tag = @{'againupdate'='password'}
PS C:\> $member = Get-AzBlockchainMember -Name $env.blockchainMember -ResourceGroupName $env.resourceGroup
PS C:\> Update-AzBlockchainMember -InputObject $member -Tag $tag

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="231b1-113">To polecenie aktualizuje członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="231b1-113">This command updates a blockchain member.</span></span>

## <span data-ttu-id="231b1-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="231b1-114">PARAMETERS</span></span>

### <span data-ttu-id="231b1-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="231b1-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="231b1-116">Ustawia hasło do konta zarządzanego przedsiębiorstwa zarządzania.</span><span class="sxs-lookup"><span data-stu-id="231b1-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="231b1-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="231b1-117">-DefaultProfile</span></span>
<span data-ttu-id="231b1-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="231b1-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="231b1-119">- FirewallRule</span><span class="sxs-lookup"><span data-stu-id="231b1-119">-FirewallRule</span></span>
<span data-ttu-id="231b1-120">Pobiera lub ustawia reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="231b1-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="231b1-121">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach FIREWALLRULE i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="231b1-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="231b1-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="231b1-122">-InputObject</span></span>
<span data-ttu-id="231b1-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="231b1-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="231b1-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="231b1-124">-Name</span></span>
<span data-ttu-id="231b1-125">Nie ma w tym celu nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="231b1-125">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="231b1-126">— Hasło</span><span class="sxs-lookup"><span data-stu-id="231b1-126">-Password</span></span>
<span data-ttu-id="231b1-127">Ustawia hasło uwierzytelniania podstawowego punktu końcowego dns węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="231b1-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="231b1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="231b1-128">-ResourceGroupName</span></span>
<span data-ttu-id="231b1-129">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="231b1-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="231b1-130">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="231b1-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="231b1-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="231b1-131">-SubscriptionId</span></span>
<span data-ttu-id="231b1-132">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="231b1-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="231b1-133">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia usługi.</span><span class="sxs-lookup"><span data-stu-id="231b1-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="231b1-134">— Tag</span><span class="sxs-lookup"><span data-stu-id="231b1-134">-Tag</span></span>
<span data-ttu-id="231b1-135">Tagi usługi, która jest listą kluczy par wartości opisującą zasób.</span><span class="sxs-lookup"><span data-stu-id="231b1-135">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="231b1-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="231b1-136">-Confirm</span></span>
<span data-ttu-id="231b1-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="231b1-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="231b1-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="231b1-138">-WhatIf</span></span>
<span data-ttu-id="231b1-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="231b1-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="231b1-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="231b1-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="231b1-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="231b1-141">CommonParameters</span></span>
<span data-ttu-id="231b1-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="231b1-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="231b1-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="231b1-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="231b1-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="231b1-144">INPUTS</span></span>

### <span data-ttu-id="231b1-145">Microsoft.Azure.PowerShell.cmdlet.uściśl.models.iBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="231b1-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="231b1-146">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="231b1-146">OUTPUTS</span></span>

### <span data-ttu-id="231b1-147">Microsoft.Azure.PowerShell.cmdlet.uściśl.models.api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="231b1-147">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="231b1-148">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="231b1-148">NOTES</span></span>

<span data-ttu-id="231b1-149">ALIASY</span><span class="sxs-lookup"><span data-stu-id="231b1-149">ALIASES</span></span>

<span data-ttu-id="231b1-150">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="231b1-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="231b1-151">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="231b1-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="231b1-152">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="231b1-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="231b1-153">FIREWALLRULE <IFirewallRule[]>: Pobiera lub ustawia reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="231b1-153">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="231b1-154">`[EndIPAddress <String>]`: pobiera lub ustawia końcowy adres IP zakresu reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="231b1-154">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="231b1-155">`[RuleName <String>]`: pobiera lub ustawia nazwę reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="231b1-155">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="231b1-156">`[StartIPAddress <String>]`: pobiera lub ustawia pierwszy adres IP zakresu reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="231b1-156">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="231b1-157">INPUTOBJECT: <IBlockchainIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="231b1-157">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="231b1-158">`[BlockchainMemberName <String>]`: Dodano nazwę członka.</span><span class="sxs-lookup"><span data-stu-id="231b1-158">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="231b1-159">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="231b1-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="231b1-160">`[Location <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="231b1-160">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="231b1-161">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="231b1-161">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="231b1-162">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="231b1-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="231b1-163">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="231b1-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="231b1-164">`[SubscriptionId <String>]`: pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="231b1-164">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="231b1-165">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia usługi.</span><span class="sxs-lookup"><span data-stu-id="231b1-165">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="231b1-166">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="231b1-166">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="231b1-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="231b1-167">RELATED LINKS</span></span>

