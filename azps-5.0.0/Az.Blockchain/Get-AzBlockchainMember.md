---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/get-azblockchainmember
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/Get-AzBlockchainMember.md
ms.openlocfilehash: 75e59631988f476faf1651c8a041e9ba7defd15a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234028"
---
# <span data-ttu-id="8c39d-101">Get-AzBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="8c39d-101">Get-AzBlockchainMember</span></span>

## <span data-ttu-id="8c39d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8c39d-102">SYNOPSIS</span></span>
<span data-ttu-id="8c39d-103">Uzyskaj szczegółowe informacje o członku Blockchain.</span><span class="sxs-lookup"><span data-stu-id="8c39d-103">Get details about a blockchain member.</span></span>

## <span data-ttu-id="8c39d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8c39d-104">SYNTAX</span></span>

### <span data-ttu-id="8c39d-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8c39d-105">List1 (Default)</span></span>
```
Get-AzBlockchainMember [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8c39d-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="8c39d-106">Get</span></span>
```
Get-AzBlockchainMember -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8c39d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8c39d-107">GetViaIdentity</span></span>
```
Get-AzBlockchainMember -InputObject <IBlockchainIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8c39d-108">Lista</span><span class="sxs-lookup"><span data-stu-id="8c39d-108">List</span></span>
```
Get-AzBlockchainMember -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c39d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="8c39d-109">DESCRIPTION</span></span>
<span data-ttu-id="8c39d-110">Uzyskaj szczegółowe informacje o członku Blockchain.</span><span class="sxs-lookup"><span data-stu-id="8c39d-110">Get details about a blockchain member.</span></span>

## <span data-ttu-id="8c39d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8c39d-111">EXAMPLES</span></span>

### <span data-ttu-id="8c39d-112">Przykład 1: Lista członków Blockchain</span><span class="sxs-lookup"><span data-stu-id="8c39d-112">Example 1: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember 

Location Name               Type
-------- ----               ----
eastus   blockchainmember01 Microsoft.Blockchain/blockchainMembers
eastus   myblockchain       Microsoft.Blockchain/blockchainMembers
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
eastus   myblockchainuvbqdl Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="8c39d-113">To polecenie wyświetla listę członków Blockchain w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="8c39d-113">This command lists blockchain members under a subscription.</span></span>

### <span data-ttu-id="8c39d-114">Przykład 2: Lista członków Blockchain</span><span class="sxs-lookup"><span data-stu-id="8c39d-114">Example 2: List blockchain members</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
eastus   dolauli002 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="8c39d-115">To polecenie wyświetla listę członków Blockchain w grupie zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c39d-115">This command lists blockchain members under a resource group.</span></span>

### <span data-ttu-id="8c39d-116">Przykład 3: uzyskiwanie członka Blockchain</span><span class="sxs-lookup"><span data-stu-id="8c39d-116">Example 3: Get a blockchain member</span></span>
```powershell
PS C:\> Get-AzBlockchainMember -Name dolauli001 -ResourceGroupName testgroup

Location Name       Type
-------- ----       ----
eastus   dolauli001 Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="8c39d-117">To polecenie pobiera członka Blockchain w ramach grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c39d-117">This command gets a blockchain member under a resource group.</span></span>

### <span data-ttu-id="8c39d-118">Przykład 4: uzyskiwanie członka Blockchain</span><span class="sxs-lookup"><span data-stu-id="8c39d-118">Example 4: Get a blockchain member</span></span>
```powershell
PS C:\> $member = Get-AzBlockchainMember -ResourceGroupName blockchain-rg -Name myblockchaine0f3ol
PS C:\> Get-AzBlockchainMember -InputObject $membe 

Location Name               Type
-------- ----               ----
eastus   myblockchaine0f3ol Microsoft.Blockchain/blockchainMembers
```

<span data-ttu-id="8c39d-119">To polecenie pobiera członka Blockchain w ramach grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c39d-119">This command gets a blockchain member under a resource group.</span></span>

## <span data-ttu-id="8c39d-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c39d-120">PARAMETERS</span></span>

### <span data-ttu-id="8c39d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c39d-121">-DefaultProfile</span></span>
<span data-ttu-id="8c39d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c39d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c39d-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="8c39d-123">-InputObject</span></span>
<span data-ttu-id="8c39d-124">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="8c39d-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="8c39d-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8c39d-125">-Name</span></span>
<span data-ttu-id="8c39d-126">Nazwa członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="8c39d-126">Blockchain member name.</span></span>

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

### <span data-ttu-id="8c39d-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c39d-127">-ResourceGroupName</span></span>
<span data-ttu-id="8c39d-128">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="8c39d-128">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="8c39d-129">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="8c39d-129">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="8c39d-130">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8c39d-130">-SubscriptionId</span></span>
<span data-ttu-id="8c39d-131">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8c39d-131">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="8c39d-132">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="8c39d-132">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="8c39d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c39d-133">CommonParameters</span></span>
<span data-ttu-id="8c39d-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c39d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c39d-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8c39d-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c39d-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c39d-136">INPUTS</span></span>

### <span data-ttu-id="8c39d-137">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="8c39d-137">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="8c39d-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8c39d-138">OUTPUTS</span></span>

### <span data-ttu-id="8c39d-139">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. Api20180601Preview. IBlockchainMember</span><span class="sxs-lookup"><span data-stu-id="8c39d-139">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IBlockchainMember</span></span>

## <span data-ttu-id="8c39d-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8c39d-140">NOTES</span></span>

<span data-ttu-id="8c39d-141">PISUJE</span><span class="sxs-lookup"><span data-stu-id="8c39d-141">ALIASES</span></span>

<span data-ttu-id="8c39d-142">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c39d-142">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="8c39d-143">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="8c39d-143">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8c39d-144">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="8c39d-144">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="8c39d-145">INPUTobject <IBlockchainIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="8c39d-145">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8c39d-146">`[BlockchainMemberName <String>]`: Blockchain nazwa członka.</span><span class="sxs-lookup"><span data-stu-id="8c39d-146">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="8c39d-147">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="8c39d-147">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8c39d-148">`[Location <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="8c39d-148">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="8c39d-149">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="8c39d-149">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="8c39d-150">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="8c39d-150">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="8c39d-151">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="8c39d-151">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="8c39d-152">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8c39d-152">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="8c39d-153">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="8c39d-153">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="8c39d-154">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="8c39d-154">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="8c39d-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c39d-155">RELATED LINKS</span></span>

