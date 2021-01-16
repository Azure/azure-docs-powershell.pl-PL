---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: a6bd4f7d8d3058de948d0ecef636c2ec9e1ca1e9
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341878"
---
# <span data-ttu-id="c5df8-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="c5df8-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="c5df8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c5df8-102">SYNOPSIS</span></span>
<span data-ttu-id="c5df8-103">Utwórz członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="c5df8-103">Create a blockchain member.</span></span>

## <span data-ttu-id="c5df8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c5df8-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c5df8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c5df8-105">DESCRIPTION</span></span>
<span data-ttu-id="c5df8-106">Utwórz członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="c5df8-106">Create a blockchain member.</span></span>

## <span data-ttu-id="c5df8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c5df8-107">EXAMPLES</span></span>

### <span data-ttu-id="c5df8-108">Przykład 1. Tworzenie nowego członka Blockchain</span><span class="sxs-lookup"><span data-stu-id="c5df8-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="c5df8-109">To polecenie tworzy nowego członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="c5df8-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="c5df8-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5df8-110">PARAMETERS</span></span>

### <span data-ttu-id="c5df8-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c5df8-111">-AsJob</span></span>
<span data-ttu-id="c5df8-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="c5df8-112">Run the command as a job</span></span>

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

### <span data-ttu-id="c5df8-113">-Konsorcjum</span><span class="sxs-lookup"><span data-stu-id="c5df8-113">-Consortium</span></span>
<span data-ttu-id="c5df8-114">Pobiera lub ustawia konsorcjum dla członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="c5df8-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="c5df8-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="c5df8-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="c5df8-116">Ustawia hasło konta zarządzanego zarządzania dla kierownictwa.</span><span class="sxs-lookup"><span data-stu-id="c5df8-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="c5df8-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="c5df8-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="c5df8-118">Pobiera nazwę wyświetlaną członka w konsorcjum.</span><span class="sxs-lookup"><span data-stu-id="c5df8-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="c5df8-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="c5df8-119">-ConsortiumRole</span></span>
<span data-ttu-id="c5df8-120">Pobiera rolę członka w konsorcjum.</span><span class="sxs-lookup"><span data-stu-id="c5df8-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="c5df8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5df8-121">-DefaultProfile</span></span>
<span data-ttu-id="c5df8-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c5df8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c5df8-123">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="c5df8-123">-FirewallRule</span></span>
<span data-ttu-id="c5df8-124">Pobiera lub ustawia reguły zapory do skonstruowania, zobacz sekcja notatki dla właściwości FIREWALLRULE i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="c5df8-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="c5df8-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c5df8-125">-Location</span></span>
<span data-ttu-id="c5df8-126">Lokalizacja geograficzna usługi Blockchain.</span><span class="sxs-lookup"><span data-stu-id="c5df8-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="c5df8-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c5df8-127">-Name</span></span>
<span data-ttu-id="c5df8-128">Nazwa członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="c5df8-128">Blockchain member name.</span></span>

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

### <span data-ttu-id="c5df8-129">-Nowait</span><span class="sxs-lookup"><span data-stu-id="c5df8-129">-NoWait</span></span>
<span data-ttu-id="c5df8-130">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="c5df8-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c5df8-131">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="c5df8-131">-Password</span></span>
<span data-ttu-id="c5df8-132">Ustawia podstawowe hasło uwierzytelniania elementu członkowskiego Blockchain.</span><span class="sxs-lookup"><span data-stu-id="c5df8-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="c5df8-133">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="c5df8-133">-Protocol</span></span>
<span data-ttu-id="c5df8-134">Pobiera lub ustawia protokół Blockchain.</span><span class="sxs-lookup"><span data-stu-id="c5df8-134">Gets or sets the blockchain protocol.</span></span>

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

### <span data-ttu-id="c5df8-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5df8-135">-ResourceGroupName</span></span>
<span data-ttu-id="c5df8-136">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="c5df8-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="c5df8-137">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="c5df8-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="c5df8-138">-SKU</span><span class="sxs-lookup"><span data-stu-id="c5df8-138">-Sku</span></span>
<span data-ttu-id="c5df8-139">Pobiera lub ustawia nazwę jednostki SKU.</span><span class="sxs-lookup"><span data-stu-id="c5df8-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="c5df8-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="c5df8-140">-SkuTier</span></span>
<span data-ttu-id="c5df8-141">Pobiera lub ustawia warstwę SKU</span><span class="sxs-lookup"><span data-stu-id="c5df8-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="c5df8-142">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="c5df8-142">-SubscriptionId</span></span>
<span data-ttu-id="c5df8-143">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="c5df8-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="c5df8-144">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="c5df8-144">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="c5df8-145">-Tag</span><span class="sxs-lookup"><span data-stu-id="c5df8-145">-Tag</span></span>
<span data-ttu-id="c5df8-146">Tagi usługi, która jest listą par wartości klucza opisujących zasób.</span><span class="sxs-lookup"><span data-stu-id="c5df8-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="c5df8-147">-ValidatorNodeSkuCapacity</span><span class="sxs-lookup"><span data-stu-id="c5df8-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="c5df8-148">Pobiera lub ustawia pojemność węzłów.</span><span class="sxs-lookup"><span data-stu-id="c5df8-148">Gets or sets the nodes capacity.</span></span>

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

### <span data-ttu-id="c5df8-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c5df8-149">-Confirm</span></span>
<span data-ttu-id="c5df8-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5df8-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5df8-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c5df8-151">-WhatIf</span></span>
<span data-ttu-id="c5df8-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c5df8-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c5df8-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c5df8-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5df8-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5df8-154">CommonParameters</span></span>
<span data-ttu-id="c5df8-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5df8-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5df8-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c5df8-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5df8-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5df8-157">INPUTS</span></span>

## <span data-ttu-id="c5df8-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c5df8-158">OUTPUTS</span></span>

### <span data-ttu-id="c5df8-159">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="c5df8-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="c5df8-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c5df8-160">NOTES</span></span>

<span data-ttu-id="c5df8-161">PISUJE</span><span class="sxs-lookup"><span data-stu-id="c5df8-161">ALIASES</span></span>

<span data-ttu-id="c5df8-162">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5df8-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c5df8-163">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c5df8-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c5df8-164">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c5df8-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c5df8-165">FIREWALLRULE <IFirewallRule [] >: Pobiera lub ustawia reguły zapory</span><span class="sxs-lookup"><span data-stu-id="c5df8-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="c5df8-166">`[EndIPAddress <String>]`: Pobiera lub ustawia końcowy adres IP zakresu reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="c5df8-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="c5df8-167">`[RuleName <String>]`: Pobiera lub ustawia nazwy reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="c5df8-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="c5df8-168">`[StartIPAddress <String>]`: Pobiera lub ustawia początkowy adres IP zakresu reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="c5df8-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="c5df8-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5df8-169">RELATED LINKS</span></span>

