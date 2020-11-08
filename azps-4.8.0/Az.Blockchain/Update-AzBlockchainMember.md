---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/update-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Update-AzBlockchainMember.md
ms.openlocfilehash: 708ad613c2dbab7e7224dbd392809d9502c9b447
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94063625"
---
# <span data-ttu-id="a726f-101">Update-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="a726f-101">Update-AzBlockchainMember</span></span>

## <span data-ttu-id="a726f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a726f-102">SYNOPSIS</span></span>
<span data-ttu-id="a726f-103">Aktualizowanie członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="a726f-103">Update a blockchain member.</span></span>

## <span data-ttu-id="a726f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a726f-104">SYNTAX</span></span>

### <span data-ttu-id="a726f-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a726f-105">UpdateExpanded (Default)</span></span>
```
Update-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="a726f-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="a726f-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBlockchainMember -InputObject <IBlockchainIdentity>
 [-ConsortiumManagementAccountPassword <SecureString>] [-FirewallRule <IFirewallRule[]>]
 [-Password <SecureString>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="a726f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a726f-107">DESCRIPTION</span></span>
<span data-ttu-id="a726f-108">Aktualizowanie członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="a726f-108">Update a blockchain member.</span></span>

## <span data-ttu-id="a726f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a726f-109">EXAMPLES</span></span>

### <span data-ttu-id="a726f-110">Przykład 1: aktualizowanie członka Blockchain</span><span class="sxs-lookup"><span data-stu-id="a726f-110">Example 1: Update a blockchain member</span></span>
```powershell
PS C:\> $passwd2 = 'strongMemberAccountPassword@2' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> Update-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Password $passwd2

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="a726f-111">To polecenie aktualizuje członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="a726f-111">This command updates a blockchain member.</span></span>

### <span data-ttu-id="a726f-112">Przykład 2: aktualizowanie członka Blockchain</span><span class="sxs-lookup"><span data-stu-id="a726f-112">Example 2: Update a blockchain member</span></span>
```powershell
PS C:\> $tag = @{'againupdate'='password'}
PS C:\> $member = Get-AzBlockchainMember -Name $env.blockchainMember -ResourceGroupName $env.resourceGroup
PS C:\> Update-AzBlockchainMember -InputObject $member -Tag $tag

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="a726f-113">To polecenie aktualizuje członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="a726f-113">This command updates a blockchain member.</span></span>

## <span data-ttu-id="a726f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a726f-114">PARAMETERS</span></span>

### <span data-ttu-id="a726f-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="a726f-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="a726f-116">Ustawia hasło konta zarządzanego zarządzania dla kierownictwa.</span><span class="sxs-lookup"><span data-stu-id="a726f-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="a726f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a726f-117">-DefaultProfile</span></span>
<span data-ttu-id="a726f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a726f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a726f-119">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="a726f-119">-FirewallRule</span></span>
<span data-ttu-id="a726f-120">Pobiera lub ustawia reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="a726f-120">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="a726f-121">Aby skonstruować, zobacz sekcję notatki dla właściwości FIREWALLRULE i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="a726f-121">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="a726f-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a726f-122">-InputObject</span></span>
<span data-ttu-id="a726f-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="a726f-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="a726f-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a726f-124">-Name</span></span>
<span data-ttu-id="a726f-125">Nazwa członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="a726f-125">Blockchain member name.</span></span>

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

### <span data-ttu-id="a726f-126">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="a726f-126">-Password</span></span>
<span data-ttu-id="a726f-127">Ustawia hasło uwierzytelniania podstawowego dla punktu końcowego DNS węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="a726f-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="a726f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a726f-128">-ResourceGroupName</span></span>
<span data-ttu-id="a726f-129">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="a726f-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="a726f-130">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="a726f-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="a726f-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a726f-131">-SubscriptionId</span></span>
<span data-ttu-id="a726f-132">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a726f-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="a726f-133">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="a726f-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a726f-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="a726f-134">-Tag</span></span>
<span data-ttu-id="a726f-135">Tagi usługi, która jest listą par wartości klucza opisujących zasób.</span><span class="sxs-lookup"><span data-stu-id="a726f-135">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="a726f-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a726f-136">-Confirm</span></span>
<span data-ttu-id="a726f-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a726f-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a726f-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a726f-138">-WhatIf</span></span>
<span data-ttu-id="a726f-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a726f-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a726f-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a726f-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a726f-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a726f-141">CommonParameters</span></span>
<span data-ttu-id="a726f-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a726f-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a726f-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a726f-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a726f-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a726f-144">INPUTS</span></span>

### <span data-ttu-id="a726f-145">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="a726f-145">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="a726f-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a726f-146">OUTPUTS</span></span>

### <span data-ttu-id="a726f-147">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="a726f-147">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="a726f-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a726f-148">NOTES</span></span>

<span data-ttu-id="a726f-149">PISUJE</span><span class="sxs-lookup"><span data-stu-id="a726f-149">ALIASES</span></span>

<span data-ttu-id="a726f-150">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a726f-150">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="a726f-151">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="a726f-151">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a726f-152">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="a726f-152">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="a726f-153">FIREWALLRULE <IFirewallRule [] >: Pobiera lub ustawia reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="a726f-153">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="a726f-154">`[EndIPAddress <String>]`: Pobiera lub ustawia końcowy adres IP zakresu reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="a726f-154">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="a726f-155">`[RuleName <String>]`: Pobiera lub ustawia nazwy reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="a726f-155">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="a726f-156">`[StartIPAddress <String>]`: Pobiera lub ustawia początkowy adres IP zakresu reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="a726f-156">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

<span data-ttu-id="a726f-157">INPUTobject <IBlockchainIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="a726f-157">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a726f-158">`[BlockchainMemberName <String>]`: Blockchain nazwa członka.</span><span class="sxs-lookup"><span data-stu-id="a726f-158">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="a726f-159">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="a726f-159">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a726f-160">`[Location <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="a726f-160">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="a726f-161">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="a726f-161">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="a726f-162">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="a726f-162">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="a726f-163">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="a726f-163">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="a726f-164">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="a726f-164">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="a726f-165">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="a726f-165">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="a726f-166">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="a726f-166">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="a726f-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a726f-167">RELATED LINKS</span></span>

