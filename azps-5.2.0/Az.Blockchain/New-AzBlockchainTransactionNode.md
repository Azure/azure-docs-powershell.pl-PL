---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNode.md
ms.openlocfilehash: c5b5e761306c37e67f6b6a2398a5985872722efa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341818"
---
# <span data-ttu-id="6b8dd-101">New-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="6b8dd-101">New-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="6b8dd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6b8dd-102">SYNOPSIS</span></span>
<span data-ttu-id="6b8dd-103">Tworzenie lub aktualizowanie węzła Transaction.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-103">Create or update the transaction node.</span></span>

## <span data-ttu-id="6b8dd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6b8dd-104">SYNTAX</span></span>

```
New-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-FirewallRule <IFirewallRule[]>] [-Location <String>] [-Password <SecureString>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="6b8dd-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6b8dd-105">DESCRIPTION</span></span>
<span data-ttu-id="6b8dd-106">Tworzenie lub aktualizowanie węzła Transaction.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-106">Create or update the transaction node.</span></span>

## <span data-ttu-id="6b8dd-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6b8dd-107">EXAMPLES</span></span>

### <span data-ttu-id="6b8dd-108">Przykład 1: Tworzenie węzła transakcji Blockchain</span><span class="sxs-lookup"><span data-stu-id="6b8dd-108">Example 1: Create a blockchain transaction node</span></span>
```powershell
PS C:\> $passwd = 'strongMemberAccountPassword@1' | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -Name tranctionnode001 -ResourceGroupName testgroup -Location eastus -Password $passwd

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="6b8dd-109">To polecenie umożliwia utworzenie węzła transakcji Blockchain.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-109">This command creates a blockchain transaction node.</span></span>

## <span data-ttu-id="6b8dd-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b8dd-110">PARAMETERS</span></span>

### <span data-ttu-id="6b8dd-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6b8dd-111">-AsJob</span></span>
<span data-ttu-id="6b8dd-112">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="6b8dd-112">Run the command as a job</span></span>

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

### <span data-ttu-id="6b8dd-113">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="6b8dd-113">-BlockchainMemberName</span></span>
<span data-ttu-id="6b8dd-114">Nazwa członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-114">Blockchain member name.</span></span>

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

### <span data-ttu-id="6b8dd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b8dd-115">-DefaultProfile</span></span>
<span data-ttu-id="6b8dd-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6b8dd-117">-FirewallRule</span><span class="sxs-lookup"><span data-stu-id="6b8dd-117">-FirewallRule</span></span>
<span data-ttu-id="6b8dd-118">Pobiera lub ustawia reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-118">Gets or sets the firewall rules.</span></span>
<span data-ttu-id="6b8dd-119">Aby skonstruować, zobacz sekcję notatki dla właściwości FIREWALLRULE i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-119">To construct, see NOTES section for FIREWALLRULE properties and create a hash table.</span></span>

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

### <span data-ttu-id="6b8dd-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6b8dd-120">-Location</span></span>
<span data-ttu-id="6b8dd-121">Pobiera lub ustawia lokalizację węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-121">Gets or sets the transaction node location.</span></span>

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

### <span data-ttu-id="6b8dd-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6b8dd-122">-Name</span></span>
<span data-ttu-id="6b8dd-123">Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-123">Transaction node name.</span></span>

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

### <span data-ttu-id="6b8dd-124">-Nowait</span><span class="sxs-lookup"><span data-stu-id="6b8dd-124">-NoWait</span></span>
<span data-ttu-id="6b8dd-125">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="6b8dd-125">Run the command asynchronously</span></span>

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

### <span data-ttu-id="6b8dd-126">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="6b8dd-126">-Password</span></span>
<span data-ttu-id="6b8dd-127">Ustawia hasło uwierzytelniania podstawowego dla punktu końcowego DNS węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-127">Sets the transaction node dns endpoint basic auth password.</span></span>

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

### <span data-ttu-id="6b8dd-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6b8dd-128">-ResourceGroupName</span></span>
<span data-ttu-id="6b8dd-129">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-129">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="6b8dd-130">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-130">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="6b8dd-131">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="6b8dd-131">-SubscriptionId</span></span>
<span data-ttu-id="6b8dd-132">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-132">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="6b8dd-133">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-133">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6b8dd-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6b8dd-134">-Confirm</span></span>
<span data-ttu-id="6b8dd-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6b8dd-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6b8dd-136">-WhatIf</span></span>
<span data-ttu-id="6b8dd-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6b8dd-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6b8dd-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b8dd-139">CommonParameters</span></span>
<span data-ttu-id="6b8dd-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b8dd-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6b8dd-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b8dd-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6b8dd-142">INPUTS</span></span>

## <span data-ttu-id="6b8dd-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6b8dd-143">OUTPUTS</span></span>

### <span data-ttu-id="6b8dd-144">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="6b8dd-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="6b8dd-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6b8dd-145">NOTES</span></span>

<span data-ttu-id="6b8dd-146">PISUJE</span><span class="sxs-lookup"><span data-stu-id="6b8dd-146">ALIASES</span></span>

<span data-ttu-id="6b8dd-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6b8dd-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="6b8dd-148">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6b8dd-149">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="6b8dd-150">FIREWALLRULE <IFirewallRule [] >: Pobiera lub ustawia reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-150">FIREWALLRULE <IFirewallRule[]>: Gets or sets the firewall rules.</span></span>
  - <span data-ttu-id="6b8dd-151">`[EndIPAddress <String>]`: Pobiera lub ustawia końcowy adres IP zakresu reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-151">`[EndIPAddress <String>]`: Gets or sets the end IP address of the firewall rule range.</span></span>
  - <span data-ttu-id="6b8dd-152">`[RuleName <String>]`: Pobiera lub ustawia nazwy reguł zapory.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-152">`[RuleName <String>]`: Gets or sets the name of the firewall rules.</span></span>
  - <span data-ttu-id="6b8dd-153">`[StartIPAddress <String>]`: Pobiera lub ustawia początkowy adres IP zakresu reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="6b8dd-153">`[StartIPAddress <String>]`: Gets or sets the start IP address of the firewall rule range.</span></span>

## <span data-ttu-id="6b8dd-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6b8dd-154">RELATED LINKS</span></span>

