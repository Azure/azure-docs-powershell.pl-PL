---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 418786855833164c3f9c15dcd2716ad00c8c6d8f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954874"
---
# <span data-ttu-id="7fd48-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="7fd48-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="7fd48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fd48-102">SYNOPSIS</span></span>
<span data-ttu-id="7fd48-103">Ponownie generuj klucze interfejsu API dla członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="7fd48-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="7fd48-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7fd48-104">SYNTAX</span></span>

### <span data-ttu-id="7fd48-105">Generuj ponownieRozwiń (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7fd48-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7fd48-106">Generuj generujViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7fd48-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7fd48-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7fd48-107">DESCRIPTION</span></span>
<span data-ttu-id="7fd48-108">Ponownie generuj klucze interfejsu API dla członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="7fd48-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="7fd48-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7fd48-109">EXAMPLES</span></span>

### <span data-ttu-id="7fd48-110">Przykład 1. Generuj klucze interfejsu Api dla węzła transakcji przy użyciu nazwy.</span><span class="sxs-lookup"><span data-stu-id="7fd48-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="7fd48-111">To polecenie generuje klucze interfejsu Api dla węzła transakcji przy użyciu nazwy, grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7fd48-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="7fd48-112">Przykład 2. Generuj klucze interfejsu Api dla węzła transakcji</span><span class="sxs-lookup"><span data-stu-id="7fd48-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="7fd48-113">To polecenie generuje klucze interfejsu Api dla węzła transakcji przy użyciu właściwości idenity.</span><span class="sxs-lookup"><span data-stu-id="7fd48-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="7fd48-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7fd48-114">PARAMETERS</span></span>

### <span data-ttu-id="7fd48-115">-Wymusz na użytkownikach</span><span class="sxs-lookup"><span data-stu-id="7fd48-115">-BlockchainMemberName</span></span>
<span data-ttu-id="7fd48-116">Nie ma w tym celu nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7fd48-116">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd48-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fd48-117">-DefaultProfile</span></span>
<span data-ttu-id="7fd48-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7fd48-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fd48-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7fd48-119">-InputObject</span></span>
<span data-ttu-id="7fd48-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7fd48-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: RegenerateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7fd48-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="7fd48-121">-KeyName</span></span>
<span data-ttu-id="7fd48-122">Pobiera lub ustawia nazwę klucza interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="7fd48-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="7fd48-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fd48-123">-ResourceGroupName</span></span>
<span data-ttu-id="7fd48-124">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="7fd48-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="7fd48-125">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="7fd48-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd48-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7fd48-126">-SubscriptionId</span></span>
<span data-ttu-id="7fd48-127">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7fd48-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="7fd48-128">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="7fd48-128">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd48-129">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="7fd48-129">-TransactionNodeName</span></span>
<span data-ttu-id="7fd48-130">Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="7fd48-130">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: RegenerateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fd48-131">— Wartość</span><span class="sxs-lookup"><span data-stu-id="7fd48-131">-Value</span></span>
<span data-ttu-id="7fd48-132">Pobiera lub ustawia wartość klucza interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="7fd48-132">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="7fd48-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7fd48-133">-Confirm</span></span>
<span data-ttu-id="7fd48-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7fd48-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7fd48-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7fd48-135">-WhatIf</span></span>
<span data-ttu-id="7fd48-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7fd48-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7fd48-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7fd48-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7fd48-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fd48-138">CommonParameters</span></span>
<span data-ttu-id="7fd48-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fd48-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fd48-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7fd48-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fd48-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7fd48-141">INPUTS</span></span>

### <span data-ttu-id="7fd48-142">Microsoft.Azure.PowerShell.cmdlet.uściśl.models.iBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="7fd48-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="7fd48-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7fd48-143">OUTPUTS</span></span>

### <span data-ttu-id="7fd48-144">Microsoft.Azure.PowerShell.cmdlet.u7.models.api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="7fd48-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="7fd48-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7fd48-145">NOTES</span></span>

<span data-ttu-id="7fd48-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="7fd48-146">ALIASES</span></span>

<span data-ttu-id="7fd48-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7fd48-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7fd48-148">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7fd48-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7fd48-149">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7fd48-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7fd48-150">INPUTOBJECT: <IBlockchainIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="7fd48-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7fd48-151">`[BlockchainMemberName <String>]`: Dodano nazwę członka.</span><span class="sxs-lookup"><span data-stu-id="7fd48-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="7fd48-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="7fd48-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7fd48-153">`[Location <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="7fd48-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="7fd48-154">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="7fd48-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="7fd48-155">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="7fd48-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="7fd48-156">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="7fd48-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="7fd48-157">`[SubscriptionId <String>]`: pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="7fd48-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="7fd48-158">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="7fd48-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="7fd48-159">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="7fd48-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="7fd48-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7fd48-160">RELATED LINKS</span></span>

