---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: c5b5e761306c37e67f6b6a2398a5985872722efa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177947"
---
# <span data-ttu-id="399c1-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="399c1-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="399c1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="399c1-102">SYNOPSIS</span></span>
<span data-ttu-id="399c1-103">Utwórz lub zaktualizuj węzeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="399c1-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="399c1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="399c1-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="399c1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="399c1-105">DESCRIPTION</span></span>
<span data-ttu-id="399c1-106">Utwórz lub zaktualizuj węzeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="399c1-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="399c1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="399c1-107">EXAMPLES</span></span>

### <span data-ttu-id="399c1-108">Przykład 1. Tworzenie węzła transakcji</span><span class="sxs-lookup"><span data-stu-id="399c1-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="399c1-109">To polecenie tworzy węzeł transakcji transakcji.</span><span class="sxs-lookup"><span data-stu-id="399c1-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="399c1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="399c1-110">PARAMETERS</span></span>

### <span data-ttu-id="399c1-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="399c1-111">-AsJob</span></span>
<span data-ttu-id="399c1-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="399c1-112">Run the command as a job</span></span>

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

### <span data-ttu-id="399c1-113">-Wymusz na użytkownikach</span><span class="sxs-lookup"><span data-stu-id="399c1-113">-BlockchainMemberName</span></span>
<span data-ttu-id="399c1-114">Nie ma w tym celu nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="399c1-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="399c1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="399c1-115">-DefaultProfile</span></span>
<span data-ttu-id="399c1-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="399c1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="399c1-117">- FirewallRule</span><span class="sxs-lookup"><span data-stu-id="399c1-117">-FirewallRule</span></span>
<span data-ttu-id="399c1-118">Pobiera lub ustawia reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="399c1-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="399c1-119">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach FIREWALLRULE i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="399c1-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="399c1-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="399c1-120">-Location</span></span>
<span data-ttu-id="399c1-121">Pobiera lub ustawia lokalizację węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="399c1-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="399c1-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="399c1-122">-Name</span></span>
<span data-ttu-id="399c1-123">Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="399c1-123">Transaction node name.</span></span>

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

### <span data-ttu-id="399c1-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="399c1-124">-NoWait</span></span>
<span data-ttu-id="399c1-125">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="399c1-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="399c1-126">— Hasło</span><span class="sxs-lookup"><span data-stu-id="399c1-126">-Password</span></span>
<span data-ttu-id="399c1-127">Ustawia hasło uwierzytelniania podstawowego punktu końcowego dns węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="399c1-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="399c1-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="399c1-128">-ResourceGroupName</span></span>
<span data-ttu-id="399c1-129">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="399c1-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="399c1-130">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="399c1-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="399c1-131">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="399c1-131">-SubscriptionId</span></span>
<span data-ttu-id="399c1-132">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="399c1-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="399c1-133">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="399c1-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="399c1-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="399c1-134">-Confirm</span></span>
<span data-ttu-id="399c1-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="399c1-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="399c1-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="399c1-136">-WhatIf</span></span>
<span data-ttu-id="399c1-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="399c1-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="399c1-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="399c1-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="399c1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="399c1-139">CommonParameters</span></span>
<span data-ttu-id="399c1-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="399c1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="399c1-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="399c1-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="399c1-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="399c1-142">INPUTS</span></span>

## <span data-ttu-id="399c1-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="399c1-143">OUTPUTS</span></span>

### <span data-ttu-id="399c1-144">Microsoft.Azure.PowerShell.cmdlet.udziec.models.api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="399c1-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="399c1-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="399c1-145">NOTES</span></span>

<span data-ttu-id="399c1-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="399c1-146">ALIASES</span></span>

<span data-ttu-id="399c1-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="399c1-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="399c1-148">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="399c1-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="399c1-149">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="399c1-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="399c1-150">FIREWALLRULE <IFirewallRule[]>: Pobiera lub ustawia reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="399c1-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="399c1-151">`[EndIPAddress <String>]`: pobiera lub ustawia końcowy adres IP zakresu reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="399c1-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="399c1-152">`[RuleName <String>]`: pobiera lub ustawia nazwę reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="399c1-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="399c1-153">`[StartIPAddress <String>]`: pobiera lub ustawia pierwszy adres IP zakresu reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="399c1-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="399c1-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="399c1-154">RELATED LINKS</span></span>

