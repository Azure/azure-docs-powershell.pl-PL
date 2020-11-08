---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchaintransactionnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainTransactionNode.md
ms.openlocfilehash: 42e5fb37cff49ab28f33cde4bf62b5c4b40c59a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234020"
---
# <span data-ttu-id="333b2-101">Get-AzBlockchainTransactionNode</span><span class="sxs-lookup"><span data-stu-id="333b2-101">Get-AzBlockchainTransactionNode</span></span>

## <span data-ttu-id="333b2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="333b2-102">SYNOPSIS</span></span>
<span data-ttu-id="333b2-103">Zapoznaj się z informacjami na temat węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="333b2-103">Get the details of the transaction node.</span></span>

## <span data-ttu-id="333b2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="333b2-104">SYNTAX</span></span>

### <span data-ttu-id="333b2-105">Lista (domyślna)</span><span class="sxs-lookup"><span data-stu-id="333b2-105">List (Default)</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="333b2-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="333b2-106">Get</span></span>
```
Get-AzBlockchainTransactionNode -BlockchainMemberName <String> -Name <String> -ResourceGroupName <String>
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="333b2-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="333b2-107">GetViaIdentity</span></span>
```
Get-AzBlockchainTransactionNode -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="333b2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="333b2-108">DESCRIPTION</span></span>
<span data-ttu-id="333b2-109">Zapoznaj się z informacjami na temat węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="333b2-109">Get the details of the transaction node.</span></span>

## <span data-ttu-id="333b2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="333b2-110">EXAMPLES</span></span>

### <span data-ttu-id="333b2-111">Przykład 1: lista węzłów transakcji dla członka Blockchain</span><span class="sxs-lookup"><span data-stu-id="333b2-111">Example 1: List transaction nodes for a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="333b2-112">To polecenie wyświetla listę węzłów transakcji dla członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="333b2-112">This command lists transaction nodes for a blockchain member.</span></span>

### <span data-ttu-id="333b2-113">Przykład 2: pobieranie węzła transakcji</span><span class="sxs-lookup"><span data-stu-id="333b2-113">Example 2: Get a transaction node</span></span>
```powershell
PS C:\> Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="333b2-114">To polecenie umożliwia wyświetlenie węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="333b2-114">This command gets a transaction node.</span></span>

### <span data-ttu-id="333b2-115">Przykład 3: pobieranie węzła transakcji</span><span class="sxs-lookup"><span data-stu-id="333b2-115">Example 3: Get a transaction node</span></span>
```powershell
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -Name tranctionnode001
PS C:\>Get-AzBlockchainTransactionNode -InputObject $tNode

Name             Type                                                    Location
----             ----                                                    --------
tranctionnode001 Microsoft.Blockchain/blockchainMembers/transactionNodes eastus
```

<span data-ttu-id="333b2-116">To polecenie umożliwia wyświetlenie węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="333b2-116">This command gets a transaction node.</span></span>

## <span data-ttu-id="333b2-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="333b2-117">PARAMETERS</span></span>

### <span data-ttu-id="333b2-118">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="333b2-118">-BlockchainMemberName</span></span>
<span data-ttu-id="333b2-119">Nazwa członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="333b2-119">Blockchain member name.</span></span>

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

### <span data-ttu-id="333b2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="333b2-120">-DefaultProfile</span></span>
<span data-ttu-id="333b2-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="333b2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="333b2-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="333b2-122">-InputObject</span></span>
<span data-ttu-id="333b2-123">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="333b2-123">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="333b2-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="333b2-124">-Name</span></span>
<span data-ttu-id="333b2-125">Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="333b2-125">Transaction node name.</span></span>

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

### <span data-ttu-id="333b2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="333b2-126">-ResourceGroupName</span></span>
<span data-ttu-id="333b2-127">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="333b2-127">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="333b2-128">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="333b2-128">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="333b2-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="333b2-129">-SubscriptionId</span></span>
<span data-ttu-id="333b2-130">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="333b2-130">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="333b2-131">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="333b2-131">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="333b2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="333b2-132">CommonParameters</span></span>
<span data-ttu-id="333b2-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="333b2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="333b2-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="333b2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="333b2-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="333b2-135">INPUTS</span></span>

### <span data-ttu-id="333b2-136">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="333b2-136">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="333b2-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="333b2-137">OUTPUTS</span></span>

### <span data-ttu-id="333b2-138">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. Api20180601Preview. ITransactionNode</span><span class="sxs-lookup"><span data-stu-id="333b2-138">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.ITransactionNode</span></span>

## <span data-ttu-id="333b2-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="333b2-139">NOTES</span></span>

<span data-ttu-id="333b2-140">PISUJE</span><span class="sxs-lookup"><span data-stu-id="333b2-140">ALIASES</span></span>

<span data-ttu-id="333b2-141">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="333b2-141">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="333b2-142">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="333b2-142">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="333b2-143">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="333b2-143">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="333b2-144">INPUTobject <IBlockchainIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="333b2-144">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="333b2-145">`[BlockchainMemberName <String>]`: Blockchain nazwa członka.</span><span class="sxs-lookup"><span data-stu-id="333b2-145">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="333b2-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="333b2-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="333b2-147">`[Location <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="333b2-147">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="333b2-148">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="333b2-148">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="333b2-149">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="333b2-149">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="333b2-150">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="333b2-150">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="333b2-151">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="333b2-151">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="333b2-152">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="333b2-152">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="333b2-153">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="333b2-153">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="333b2-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="333b2-154">RELATED LINKS</span></span>

