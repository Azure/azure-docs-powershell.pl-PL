---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: 78d3d6449eb5a487c6c4a8a60a732c30fa502600
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965121"
---
# <span data-ttu-id="28999-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="28999-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="28999-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28999-102">SYNOPSIS</span></span>
<span data-ttu-id="28999-103">Utwórz lub zaktualizuj węzeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="28999-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="28999-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="28999-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="28999-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="28999-105">DESCRIPTION</span></span>
<span data-ttu-id="28999-106">Utwórz lub zaktualizuj węzeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="28999-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="28999-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="28999-107">EXAMPLES</span></span>

### <span data-ttu-id="28999-108">Przykład 1. Tworzenie węzła transakcji</span><span class="sxs-lookup"><span data-stu-id="28999-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="28999-109">To polecenie tworzy węzeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="28999-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="28999-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="28999-110">PARAMETERS</span></span>

### <span data-ttu-id="28999-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="28999-111">-AsJob</span></span>
<span data-ttu-id="28999-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="28999-112">Run the command as a job</span></span>

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

### <span data-ttu-id="28999-113">-Wymusz na użytkownikach</span><span class="sxs-lookup"><span data-stu-id="28999-113">-BlockchainMemberName</span></span>
<span data-ttu-id="28999-114">Nie ma w tym celu nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="28999-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="28999-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28999-115">-DefaultProfile</span></span>
<span data-ttu-id="28999-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="28999-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="28999-117">- FirewallRule</span><span class="sxs-lookup"><span data-stu-id="28999-117">-FirewallRule</span></span>
<span data-ttu-id="28999-118">Pobiera lub ustawia reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="28999-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="28999-119">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach FIREWALLRULE i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="28999-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="28999-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="28999-120">-Location</span></span>
<span data-ttu-id="28999-121">Pobiera lub ustawia lokalizację węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="28999-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="28999-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="28999-122">-Name</span></span>
<span data-ttu-id="28999-123">Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="28999-123">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="28999-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="28999-124">-NoWait</span></span>
<span data-ttu-id="28999-125">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="28999-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="28999-126">— Hasło</span><span class="sxs-lookup"><span data-stu-id="28999-126">-Password</span></span>
<span data-ttu-id="28999-127">Ustawia hasło uwierzytelniania podstawowego punktu końcowego dns węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="28999-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="28999-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28999-128">-ResourceGroupName</span></span>
<span data-ttu-id="28999-129">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="28999-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="28999-130">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="28999-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="28999-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="28999-131">-SubscriptionId</span></span>
<span data-ttu-id="28999-132">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="28999-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="28999-133">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="28999-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="28999-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="28999-134">-Confirm</span></span>
<span data-ttu-id="28999-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="28999-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28999-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28999-136">-WhatIf</span></span>
<span data-ttu-id="28999-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="28999-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28999-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="28999-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28999-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28999-139">CommonParameters</span></span>
<span data-ttu-id="28999-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28999-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28999-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="28999-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28999-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28999-142">INPUTS</span></span>

## <span data-ttu-id="28999-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28999-143">OUTPUTS</span></span>

### <span data-ttu-id="28999-144">Microsoft.Azure.PowerShell.cmdlet.nac.models.api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="28999-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="28999-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="28999-145">NOTES</span></span>

<span data-ttu-id="28999-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="28999-146">ALIASES</span></span>

<span data-ttu-id="28999-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28999-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="28999-148">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="28999-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="28999-149">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="28999-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="28999-150">FIREWALLRULE <IFirewallRule[]>: Pobiera lub ustawia reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="28999-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="28999-151">`[EndIPAddress <String>]`: pobiera lub ustawia końcowy adres IP zakresu reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="28999-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="28999-152">`[RuleName <String>]`: pobiera lub ustawia nazwę reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="28999-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="28999-153">`[StartIPAddress <String>]`: pobiera lub ustawia startowy adres IP zakresu reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="28999-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="28999-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28999-154">RELATED LINKS</span></span>

