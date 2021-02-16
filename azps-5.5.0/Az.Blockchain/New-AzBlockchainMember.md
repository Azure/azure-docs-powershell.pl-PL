---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMember.md
ms.openlocfilehash: a6bd4f7d8d3058de948d0ecef636c2ec9e1ca1e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177955"
---
# <span data-ttu-id="fadf6-101">New-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="fadf6-101">New-AzBlockchainMember</span></span>

## <span data-ttu-id="fadf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fadf6-102">SYNOPSIS</span></span>
<span data-ttu-id="fadf6-103">Utwórz nowego członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="fadf6-103">Create a blockchain member.</span></span>

## <span data-ttu-id="fadf6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fadf6-104">SYNTAX</span></span>

```
New-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Consortium <String>] [-ConsortiumManagementAccountPassword <SecureString>]
 [-ConsortiumMemberDisplayName <String>] [-ConsortiumRole <String>] [-FirewallRule <IFirewallRule[]>]
 [-Location <String>] [-Password <SecureString>] [-Protocol <BlockchainProtocol>] [-Sku <String>]
 [-SkuTier <String>] [-Tag <Hashtable>] [-ValidatorNodeSkuCapacity <Int32>] [-DefaultProfile <PSObject>]
 [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="fadf6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fadf6-105">DESCRIPTION</span></span>
<span data-ttu-id="fadf6-106">Utwórz nowego członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="fadf6-106">Create a blockchain member.</span></span>

## <span data-ttu-id="fadf6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fadf6-107">EXAMPLES</span></span>

### <span data-ttu-id="fadf6-108">Przykład 1. Tworzenie nowego członka zespołu</span><span class="sxs-lookup"><span data-stu-id="fadf6-108">Example 1: Create a new blockchain member</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> $csPasswd = 'strongConsortiumManagementPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainMember -Name dolauli002 -ResourceGroupName testgroup -Consortium consor002 -ConsortiumManagementAccountPassword $csPasswd -Location eastus -Password $passwd -Protocol Quorum -Sku S0

Location Name       Type
-------- ----       ----
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="fadf6-109">To polecenie tworzy nowego członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="fadf6-109">This command creates a new blockchain member.</span></span>

## <span data-ttu-id="fadf6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fadf6-110">PARAMETERS</span></span>

### <span data-ttu-id="fadf6-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="fadf6-111">-AsJob</span></span>
<span data-ttu-id="fadf6-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="fadf6-112">Run the command as a job</span></span>

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

### <span data-ttu-id="fadf6-113">— Consortium</span><span class="sxs-lookup"><span data-stu-id="fadf6-113">-Consortium</span></span>
<span data-ttu-id="fadf6-114">Pobiera lub ustawia to organizacji dla tego członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="fadf6-114">Gets or sets the consortium for the blockchain member.</span></span>

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

### <span data-ttu-id="fadf6-115">-ConsortiumManagementAccountPassword</span><span class="sxs-lookup"><span data-stu-id="fadf6-115">-ConsortiumManagementAccountPassword</span></span>
<span data-ttu-id="fadf6-116">Ustawia hasło do konta zarządzanego przedsiębiorstwa zarządzania.</span><span class="sxs-lookup"><span data-stu-id="fadf6-116">Sets the managed consortium management account password.</span></span>

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

### <span data-ttu-id="fadf6-117">-ConsortiumMemberDisplayName</span><span class="sxs-lookup"><span data-stu-id="fadf6-117">-ConsortiumMemberDisplayName</span></span>
<span data-ttu-id="fadf6-118">Pobiera nazwę wyświetlaną członka w organizacji.</span><span class="sxs-lookup"><span data-stu-id="fadf6-118">Gets the display name of the member in the consortium.</span></span>

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

### <span data-ttu-id="fadf6-119">-ConsortiumRole</span><span class="sxs-lookup"><span data-stu-id="fadf6-119">-ConsortiumRole</span></span>
<span data-ttu-id="fadf6-120">Pełni rolę członka w ramach tego przedsiębiorstwa.</span><span class="sxs-lookup"><span data-stu-id="fadf6-120">Gets the role of the member in the consortium.</span></span>

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

### <span data-ttu-id="fadf6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fadf6-121">-DefaultProfile</span></span>
<span data-ttu-id="fadf6-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="fadf6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fadf6-123">- FirewallRule</span><span class="sxs-lookup"><span data-stu-id="fadf6-123">-FirewallRule</span></span>
<span data-ttu-id="fadf6-124">Pobiera lub ustawia reguły zapory, aby utworzyć konstruowanie, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach funkcji FIREWALLRULE i utworzyć tabelę skrótów.</span><span class="sxs-lookup"><span data-stu-id="fadf6-124">Gets or sets firewall rules To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="fadf6-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="fadf6-125">-Location</span></span>
<span data-ttu-id="fadf6-126">Lokalizacja GEOGRAFICZNA usługi.</span><span class="sxs-lookup"><span data-stu-id="fadf6-126">The GEO location of the blockchain service.</span></span>

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

### <span data-ttu-id="fadf6-127">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="fadf6-127">-Name</span></span>
<span data-ttu-id="fadf6-128">Nie ma w tym celu nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="fadf6-128">Blockchain member name.</span></span>

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

### <span data-ttu-id="fadf6-129">-NoWait</span><span class="sxs-lookup"><span data-stu-id="fadf6-129">-NoWait</span></span>
<span data-ttu-id="fadf6-130">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="fadf6-130">Run the command asynchronously</span></span>

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

### <span data-ttu-id="fadf6-131">— Hasło</span><span class="sxs-lookup"><span data-stu-id="fadf6-131">-Password</span></span>
<span data-ttu-id="fadf6-132">Ustawia podstawowe hasło uwierzytelniania członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="fadf6-132">Sets the basic auth password of the blockchain member.</span></span>

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

### <span data-ttu-id="fadf6-133">— Protokół</span><span class="sxs-lookup"><span data-stu-id="fadf6-133">-Protocol</span></span>
<span data-ttu-id="fadf6-134">Pobiera lub ustawia protokół protokołów.</span><span class="sxs-lookup"><span data-stu-id="fadf6-134">Gets or sets the blockchain protocol.</span></span>

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

### <span data-ttu-id="fadf6-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fadf6-135">-ResourceGroupName</span></span>
<span data-ttu-id="fadf6-136">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="fadf6-136">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="fadf6-137">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="fadf6-137">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="fadf6-138">- SKU</span><span class="sxs-lookup"><span data-stu-id="fadf6-138">-Sku</span></span>
<span data-ttu-id="fadf6-139">Pobiera lub ustawia nazwę sku</span><span class="sxs-lookup"><span data-stu-id="fadf6-139">Gets or sets Sku name</span></span>

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

### <span data-ttu-id="fadf6-140">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="fadf6-140">-SkuTier</span></span>
<span data-ttu-id="fadf6-141">Pobiera lub ustawia warstwę SKU</span><span class="sxs-lookup"><span data-stu-id="fadf6-141">Gets or sets Sku tier</span></span>

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

### <span data-ttu-id="fadf6-142">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="fadf6-142">-SubscriptionId</span></span>
<span data-ttu-id="fadf6-143">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="fadf6-143">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="fadf6-144">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="fadf6-144">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="fadf6-145">— Tag</span><span class="sxs-lookup"><span data-stu-id="fadf6-145">-Tag</span></span>
<span data-ttu-id="fadf6-146">Tagi usługi, która jest listą kluczy par wartości opisującą zasób.</span><span class="sxs-lookup"><span data-stu-id="fadf6-146">Tags of the service which is a list of key value pairs that describes the resource.</span></span>

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

### <span data-ttu-id="fadf6-147">-ValidatorNodeSkuCapacity</span><span class="sxs-lookup"><span data-stu-id="fadf6-147">-ValidatorNodeSkuCapacity</span></span>
<span data-ttu-id="fadf6-148">Pobiera lub ustawia pojemność węzłów.</span><span class="sxs-lookup"><span data-stu-id="fadf6-148">Gets or sets the nodes capacity.</span></span>

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

### <span data-ttu-id="fadf6-149">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fadf6-149">-Confirm</span></span>
<span data-ttu-id="fadf6-150">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fadf6-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fadf6-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fadf6-151">-WhatIf</span></span>
<span data-ttu-id="fadf6-152">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fadf6-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fadf6-153">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fadf6-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fadf6-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fadf6-154">CommonParameters</span></span>
<span data-ttu-id="fadf6-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fadf6-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fadf6-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fadf6-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fadf6-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fadf6-157">INPUTS</span></span>

## <span data-ttu-id="fadf6-158">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fadf6-158">OUTPUTS</span></span>

### <span data-ttu-id="fadf6-159">Microsoft.Azure.PowerShell.cmdlet.uściśl.models.api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="fadf6-159">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="fadf6-160">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fadf6-160">NOTES</span></span>

<span data-ttu-id="fadf6-161">ALIASY</span><span class="sxs-lookup"><span data-stu-id="fadf6-161">ALIASES</span></span>

<span data-ttu-id="fadf6-162">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fadf6-162">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="fadf6-163">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="fadf6-163">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="fadf6-164">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="fadf6-164">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="fadf6-165">FIREWALLRULE <IFirewallRule[]>: Pobiera lub ustawia reguły zapory</span><span class="sxs-lookup"><span data-stu-id="fadf6-165">FIREWALLRULE <IFirewallRule[]>: Gets or sets firewall rules</span></span>
  - <span data-ttu-id="fadf6-166">`[EndIPAddress <String>]`: pobiera lub ustawia końcowy adres IP zakresu reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="fadf6-166">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="fadf6-167">`[RuleName <String>]`: pobiera lub ustawia nazwę reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="fadf6-167">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="fadf6-168">`[StartIPAddress <String>]`: pobiera lub ustawia pierwszy adres IP zakresu reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="fadf6-168">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="fadf6-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fadf6-169">RELATED LINKS</span></span>

