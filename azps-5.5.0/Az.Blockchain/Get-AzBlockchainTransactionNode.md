---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 42e5fb37cff49ab28f33cde4bf62b5c4b40c59a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200922"
---
# <span data-ttu-id="cdab8-101">Get-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="cdab8-101">Get-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="cdab8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdab8-102">SYNOPSIS</span></span>
<span data-ttu-id="cdab8-103">Uzyskaj szczegółowe informacje o węźle transakcji.</span><span class="sxs-lookup"><span data-stu-id="cdab8-103">Get the details of the transaction node.</span></span>

## <span data-ttu-id="cdab8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cdab8-104">SYNTAX</span></span>

### <span data-ttu-id="cdab8-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="cdab8-105">List (Default)</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cdab8-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="cdab8-106">Get</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cdab8-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="cdab8-107">GetViaIdentity</span></span>
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="cdab8-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="cdab8-108">DESCRIPTION</span></span>
<span data-ttu-id="cdab8-109">Uzyskaj szczegółowe informacje o węźle transakcji.</span><span class="sxs-lookup"><span data-stu-id="cdab8-109">Get the details of the transaction node.</span></span>

## <span data-ttu-id="cdab8-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cdab8-110">EXAMPLES</span></span>

### <span data-ttu-id="cdab8-111">Przykład 1. Lista węzłów transakcji dla członka zespołu</span><span class="sxs-lookup"><span data-stu-id="cdab8-111">Example 1: List transaction nodes for a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="cdab8-112">To polecenie zawiera listę węzłów transakcji dla członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="cdab8-112">This command lists transaction nodes for a blockchain member.</span></span>

### <span data-ttu-id="cdab8-113">Przykład 2. Uzyskiwanie węzła transakcji</span><span class="sxs-lookup"><span data-stu-id="cdab8-113">Example 2: Get a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="cdab8-114">To polecenie pobiera węzeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="cdab8-114">This command gets a transaction node.</span></span>

### <span data-ttu-id="cdab8-115">Przykład 3. Uzyskiwanie węzła transakcji</span><span class="sxs-lookup"><span data-stu-id="cdab8-115">Example 3: Get a transaction node</span></span>
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="cdab8-116">To polecenie pobiera węzeł transakcji.</span><span class="sxs-lookup"><span data-stu-id="cdab8-116">This command gets a transaction node.</span></span>

## <span data-ttu-id="cdab8-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdab8-117">PARAMETERS</span></span>

### <span data-ttu-id="cdab8-118">-Nawiązywane NazwyMemberów</span><span class="sxs-lookup"><span data-stu-id="cdab8-118">-BlockchainMemberName</span></span>
<span data-ttu-id="cdab8-119">Nie ma w tym celu nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cdab8-119">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdab8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdab8-120">-DefaultProfile</span></span>
<span data-ttu-id="cdab8-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cdab8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdab8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cdab8-122">-InputObject</span></span>
<span data-ttu-id="cdab8-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="cdab8-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cdab8-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cdab8-124">-Name</span></span>
<span data-ttu-id="cdab8-125">Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="cdab8-125">Transaction node name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: TransactionNodeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdab8-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdab8-126">-ResourceGroupName</span></span>
<span data-ttu-id="cdab8-127">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="cdab8-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="cdab8-128">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="cdab8-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdab8-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cdab8-129">-SubscriptionId</span></span>
<span data-ttu-id="cdab8-130">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cdab8-130">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="cdab8-131">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia usługi.</span><span class="sxs-lookup"><span data-stu-id="cdab8-131">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cdab8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdab8-132">CommonParameters</span></span>
<span data-ttu-id="cdab8-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdab8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdab8-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cdab8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdab8-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdab8-135">INPUTS</span></span>

### <span data-ttu-id="cdab8-136">Microsoft.Azure.PowerShell.cmdlet.uściśl.models.iBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="cdab8-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="cdab8-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cdab8-137">OUTPUTS</span></span>

### <span data-ttu-id="cdab8-138">Microsoft.Azure.PowerShell.cmdlet.udziec.models.api20180601Preview.ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="cdab8-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="cdab8-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cdab8-139">NOTES</span></span>

<span data-ttu-id="cdab8-140">ALIASY</span><span class="sxs-lookup"><span data-stu-id="cdab8-140">ALIASES</span></span>

<span data-ttu-id="cdab8-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cdab8-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="cdab8-142">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="cdab8-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="cdab8-143">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="cdab8-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="cdab8-144">INPUTOBJECT: <IBlockchainIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="cdab8-144">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="cdab8-145">`[BlockchainMemberName <String>]`: Dodano nazwę członka.</span><span class="sxs-lookup"><span data-stu-id="cdab8-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="cdab8-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="cdab8-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="cdab8-147">`[Location <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="cdab8-147">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="cdab8-148">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="cdab8-148">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="cdab8-149">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="cdab8-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="cdab8-150">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="cdab8-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="cdab8-151">`[SubscriptionId <String>]`: pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="cdab8-151">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="cdab8-152">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia usługi.</span><span class="sxs-lookup"><span data-stu-id="cdab8-152">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="cdab8-153">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="cdab8-153">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="cdab8-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdab8-154">RELATED LINKS</span></span>

