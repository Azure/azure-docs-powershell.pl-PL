---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 6ec33665bfa8a7f369c90c71fe9b8141682641e7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962474"
---
# <span data-ttu-id="61f1a-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="61f1a-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="61f1a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61f1a-102">SYNOPSIS</span></span>
<span data-ttu-id="61f1a-103">Uzyskaj szczegółowe informacje na temat członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="61f1a-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="61f1a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="61f1a-104">SYNTAX</span></span>

### <span data-ttu-id="61f1a-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="61f1a-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="61f1a-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="61f1a-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="61f1a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="61f1a-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="61f1a-108">Lista</span><span class="sxs-lookup"><span data-stu-id="61f1a-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="61f1a-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="61f1a-109">DESCRIPTION</span></span>
<span data-ttu-id="61f1a-110">Uzyskaj szczegółowe informacje na temat członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="61f1a-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="61f1a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="61f1a-111">EXAMPLES</span></span>

### <span data-ttu-id="61f1a-112">Przykład 1. Lista członków zespołu</span><span class="sxs-lookup"><span data-stu-id="61f1a-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="61f1a-113">To polecenie wyświetla listę członków zespołu w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="61f1a-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="61f1a-114">Przykład 2. Lista członków zespołu</span><span class="sxs-lookup"><span data-stu-id="61f1a-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="61f1a-115">To polecenie wyświetla listę członków grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="61f1a-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="61f1a-116">Przykład 3. Pobierz członka zespołu</span><span class="sxs-lookup"><span data-stu-id="61f1a-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="61f1a-117">To polecenie pobiera członka grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="61f1a-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="61f1a-118">Przykład 4. Pobierz członka zespołu</span><span class="sxs-lookup"><span data-stu-id="61f1a-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="61f1a-119">To polecenie pobiera członka grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="61f1a-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="61f1a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61f1a-120">PARAMETERS</span></span>

### <span data-ttu-id="61f1a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61f1a-121">-DefaultProfile</span></span>
<span data-ttu-id="61f1a-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="61f1a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="61f1a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61f1a-123">-InputObject</span></span>
<span data-ttu-id="61f1a-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="61f1a-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="61f1a-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="61f1a-125">-Name</span></span>
<span data-ttu-id="61f1a-126">Nie ma w tym celu nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="61f1a-126">Blockchain member name.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BlockchainMemberName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f1a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="61f1a-127">-ResourceGroupName</span></span>
<span data-ttu-id="61f1a-128">Nazwa grupy zasobów zawierającej zasób.</span><span class="sxs-lookup"><span data-stu-id="61f1a-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="61f1a-129">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="61f1a-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="61f1a-130">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="61f1a-130">-SubscriptionId</span></span>
<span data-ttu-id="61f1a-131">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="61f1a-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="61f1a-132">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="61f1a-132">The subscription ID is part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List, List1
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="61f1a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61f1a-133">CommonParameters</span></span>
<span data-ttu-id="61f1a-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="61f1a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61f1a-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="61f1a-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61f1a-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61f1a-136">INPUTS</span></span>

### <span data-ttu-id="61f1a-137">Microsoft.Azure.PowerShell.cmdlet.uściśl.models.iBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="61f1a-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="61f1a-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="61f1a-138">OUTPUTS</span></span>

### <span data-ttu-id="61f1a-139">Microsoft.Azure.PowerShell.cmdlet.uściśl.models.api20180601Preview.IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="61f1a-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="61f1a-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="61f1a-140">NOTES</span></span>

<span data-ttu-id="61f1a-141">ALIASY</span><span class="sxs-lookup"><span data-stu-id="61f1a-141">ALIASES</span></span>

<span data-ttu-id="61f1a-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="61f1a-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="61f1a-143">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="61f1a-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="61f1a-144">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="61f1a-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="61f1a-145">INPUTOBJECT: <IBlockchainIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="61f1a-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="61f1a-146">`[BlockchainMemberName <String>]`: Dodano nazwę członka.</span><span class="sxs-lookup"><span data-stu-id="61f1a-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="61f1a-147">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="61f1a-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="61f1a-148">`[Location <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="61f1a-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="61f1a-149">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="61f1a-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="61f1a-150">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="61f1a-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="61f1a-151">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="61f1a-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="61f1a-152">`[SubscriptionId <String>]`: pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="61f1a-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="61f1a-153">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="61f1a-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="61f1a-154">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="61f1a-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="61f1a-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="61f1a-155">RELATED LINKS</span></span>

