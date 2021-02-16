---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 6f39e869137996a64c5fc440ee0c2c8bb559542b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177946"
---
# <span data-ttu-id="83e3e-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="83e3e-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="83e3e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="83e3e-103">Ponownie generuj klucze interfejsu API dla członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="83e3e-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="83e3e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="83e3e-104">SYNTAX</span></span>

### <span data-ttu-id="83e3e-105">Generuj ponownieRozwiń (domyślne)</span><span class="sxs-lookup"><span data-stu-id="83e3e-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="83e3e-106">Generuj generujViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="83e3e-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="83e3e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="83e3e-107">DESCRIPTION</span></span>
<span data-ttu-id="83e3e-108">Ponownie generuj klucze interfejsu API dla członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="83e3e-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="83e3e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="83e3e-109">EXAMPLES</span></span>

### <span data-ttu-id="83e3e-110">Przykład 1. Generuj klucze interfejsu Api dla węzła transakcji przy użyciu nazwy.</span><span class="sxs-lookup"><span data-stu-id="83e3e-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="83e3e-111">To polecenie generuje klucze interfejsu Api dla węzła transakcji przy użyciu nazwy, grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="83e3e-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="83e3e-112">Przykład 2. Generuj klucze interfejsu Api dla węzła transakcji</span><span class="sxs-lookup"><span data-stu-id="83e3e-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="83e3e-113">To polecenie generuje klucze interfejsu Api dla węzła transakcji przy użyciu właściwości idenity.</span><span class="sxs-lookup"><span data-stu-id="83e3e-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="83e3e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="83e3e-114">PARAMETERS</span></span>

### <span data-ttu-id="83e3e-115">-Wymusz na użytkownikach</span><span class="sxs-lookup"><span data-stu-id="83e3e-115">-BlockchainMemberName</span></span>
<span data-ttu-id="83e3e-116">Nie ma w tym celu nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="83e3e-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="83e3e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83e3e-117">-DefaultProfile</span></span>
<span data-ttu-id="83e3e-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="83e3e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="83e3e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="83e3e-119">-InputObject</span></span>
<span data-ttu-id="83e3e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="83e3e-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="83e3e-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="83e3e-121">-KeyName</span></span>
<span data-ttu-id="83e3e-122">Pobiera lub ustawia nazwę klucza interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="83e3e-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="83e3e-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83e3e-123">-ResourceGroupName</span></span>
<span data-ttu-id="83e3e-124">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="83e3e-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="83e3e-125">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="83e3e-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="83e3e-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="83e3e-126">-SubscriptionId</span></span>
<span data-ttu-id="83e3e-127">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="83e3e-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="83e3e-128">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="83e3e-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="83e3e-129">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="83e3e-129">-TransactionNodeName</span></span>
<span data-ttu-id="83e3e-130">Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="83e3e-130">Transaction node name.</span></span>

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

### <span data-ttu-id="83e3e-131">— Wartość</span><span class="sxs-lookup"><span data-stu-id="83e3e-131">-Value</span></span>
<span data-ttu-id="83e3e-132">Pobiera lub ustawia wartość klucza interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="83e3e-132">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="83e3e-133">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="83e3e-133">-Confirm</span></span>
<span data-ttu-id="83e3e-134">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="83e3e-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="83e3e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="83e3e-135">-WhatIf</span></span>
<span data-ttu-id="83e3e-136">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="83e3e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="83e3e-137">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="83e3e-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="83e3e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83e3e-138">CommonParameters</span></span>
<span data-ttu-id="83e3e-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="83e3e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83e3e-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83e3e-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83e3e-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="83e3e-141">INPUTS</span></span>

### <span data-ttu-id="83e3e-142">Microsoft.Azure.PowerShell.cmdlet.uściśl.models.iBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="83e3e-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="83e3e-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="83e3e-143">OUTPUTS</span></span>

### <span data-ttu-id="83e3e-144">Microsoft.Azure.PowerShell.cmdlet.u7.models.api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="83e3e-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="83e3e-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="83e3e-145">NOTES</span></span>

<span data-ttu-id="83e3e-146">ALIASY</span><span class="sxs-lookup"><span data-stu-id="83e3e-146">ALIASES</span></span>

<span data-ttu-id="83e3e-147">COMPLEX PARAMETER PROPERTIES</span><span class="sxs-lookup"><span data-stu-id="83e3e-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="83e3e-148">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="83e3e-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="83e3e-149">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="83e3e-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="83e3e-150">INPUTOBJECT: <IBlockchainIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="83e3e-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="83e3e-151">`[BlockchainMemberName <String>]`: Dodano nazwę członka.</span><span class="sxs-lookup"><span data-stu-id="83e3e-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="83e3e-152">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="83e3e-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="83e3e-153">`[Location <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="83e3e-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="83e3e-154">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="83e3e-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="83e3e-155">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="83e3e-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="83e3e-156">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="83e3e-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="83e3e-157">`[SubscriptionId <String>]`: pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="83e3e-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="83e3e-158">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="83e3e-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="83e3e-159">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="83e3e-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="83e3e-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="83e3e-160">RELATED LINKS</span></span>

