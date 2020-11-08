---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: a6bd4f7d8d3058de948d0ecef636c2ec9e1ca1e9
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234014"
---
# <span data-ttu-id="4260e-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="4260e-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="4260e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4260e-102">SYNOPSIS</span></span>
<span data-ttu-id="4260e-103">Utwórz członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="4260e-103">Create a blockchain member.</span></span>

## <span data-ttu-id="4260e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4260e-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4260e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4260e-105">DESCRIPTION</span></span>
<span data-ttu-id="4260e-106">Utwórz członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="4260e-106">Create a blockchain member.</span></span>

## <span data-ttu-id="4260e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4260e-107">EXAMPLES</span></span>

### <span data-ttu-id="4260e-108">Przykład 1. Tworzenie nowego członka Blockchain</span><span class="sxs-lookup"><span data-stu-id="4260e-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="4260e-109">To polecenie tworzy nowego członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="4260e-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="4260e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4260e-110">PARAMETERS</span></span>

### <span data-ttu-id="4260e-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="4260e-111">-AsJob</span></span>
<span data-ttu-id="4260e-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="4260e-112">Run the command as a job</span></span>

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

### <span data-ttu-id="4260e-113">-Konsorcjum</span><span class="sxs-lookup"><span data-stu-id="4260e-113">-Consortium</span></span>
<span data-ttu-id="4260e-114">Pobiera lub ustawia konsorcjum dla członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="4260e-114">Gets or sets the consortium for the blockchain member.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4260e-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="4260e-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="4260e-116">Ustawia hasło konta zarządzanego zarządzania dla kierownictwa.</span><span class="sxs-lookup"><span data-stu-id="4260e-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="4260e-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="4260e-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="4260e-118">Pobiera nazwę wyświetlaną członka w konsorcjum.</span><span class="sxs-lookup"><span data-stu-id="4260e-118">Gets the display name of the member in the consortium.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4260e-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="4260e-119">-ConsortiumRole</span></span>
<span data-ttu-id="4260e-120">Pobiera rolę członka w konsorcjum.</span><span class="sxs-lookup"><span data-stu-id="4260e-120">Gets the role of the member in the consortium.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4260e-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4260e-121">-DefaultProfile</span></span>
<span data-ttu-id="4260e-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4260e-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4260e-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="4260e-123">-FirewallRule</span></span>
<span data-ttu-id="4260e-124">Pobiera lub ustawia reguły zapory do skonstruowania, zobacz sekcja notatki dla właściwości FIREWALLRULE i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="4260e-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="4260e-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4260e-125">-Location</span></span>
<span data-ttu-id="4260e-126">Lokalizacja geograficzna usługi Blockchain.</span><span class="sxs-lookup"><span data-stu-id="4260e-126">The GEO location of the blockchain service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4260e-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4260e-127">-Name</span></span>
<span data-ttu-id="4260e-128">Nazwa członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="4260e-128">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4260e-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="4260e-129">-NoWait</span></span>
<span data-ttu-id="4260e-130">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="4260e-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="4260e-131">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="4260e-131">-Password</span></span>
<span data-ttu-id="4260e-132">Ustawia podstawowe hasło uwierzytelniania elementu członkowskiego Blockchain.</span><span class="sxs-lookup"><span data-stu-id="4260e-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="4260e-133">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="4260e-133">-Protocol</span></span>
<span data-ttu-id="4260e-134">Pobiera lub ustawia protokół Blockchain.</span><span class="sxs-lookup"><span data-stu-id="4260e-134">Gets or sets the blockchain protocol.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Support.BlockchainProtocol
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4260e-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4260e-135">-ResourceGroupName</span></span>
<span data-ttu-id="4260e-136">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="4260e-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4260e-137">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="4260e-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4260e-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="4260e-138">-Sku</span></span>
<span data-ttu-id="4260e-139">Pobiera lub ustawia nazwę jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="4260e-139">Gets or sets Sku name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4260e-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="4260e-140">-SkuTier</span></span>
<span data-ttu-id="4260e-141">Pobiera lub ustawia warstwę SKU</span><span class="sxs-lookup"><span data-stu-id="4260e-141">Gets or sets Sku tier</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4260e-142">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4260e-142">-SubscriptionId</span></span>
<span data-ttu-id="4260e-143">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4260e-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4260e-144">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="4260e-144">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4260e-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="4260e-145">-Tag</span></span>
<span data-ttu-id="4260e-146">Tagi usługi, która jest listą par wartości klucza opisujących zasób.</span><span class="sxs-lookup"><span data-stu-id="4260e-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="4260e-147">-ValidatorNodeSkuCapacity</span><span class="sxs-lookup"><span data-stu-id="4260e-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="4260e-148">Pobiera lub ustawia pojemność węzłów.</span><span class="sxs-lookup"><span data-stu-id="4260e-148">Gets or sets the nodes capacity.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4260e-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4260e-149">-Confirm</span></span>
<span data-ttu-id="4260e-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4260e-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4260e-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4260e-151">-WhatIf</span></span>
<span data-ttu-id="4260e-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4260e-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4260e-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4260e-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4260e-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4260e-154">CommonParameters</span></span>
<span data-ttu-id="4260e-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4260e-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4260e-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4260e-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4260e-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4260e-157">INPUTS</span></span>

## <span data-ttu-id="4260e-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4260e-158">OUTPUTS</span></span>

### <span data-ttu-id="4260e-159">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="4260e-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="4260e-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4260e-160">NOTES</span></span>

<span data-ttu-id="4260e-161">PISUJE</span><span class="sxs-lookup"><span data-stu-id="4260e-161">ALIASES</span></span>

<span data-ttu-id="4260e-162">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4260e-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4260e-163">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4260e-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4260e-164">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4260e-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4260e-165">FIREWALLRULE <IFirewallRule [] >: Pobiera lub ustawia reguły zapory</span><span class="sxs-lookup"><span data-stu-id="4260e-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="4260e-166">`[EndIPAddress <String>]`: Pobiera lub ustawia końcowy adres IP zakresu reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="4260e-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="4260e-167">`[RuleName <String>]`: Pobiera lub ustawia nazwy reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="4260e-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="4260e-168">`[StartIPAddress <String>]`: Pobiera lub ustawia początkowy adres IP zakresu reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="4260e-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="4260e-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4260e-169">RELATED LINKS</span></span>

