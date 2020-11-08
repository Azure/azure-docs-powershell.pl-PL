---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchaintransactionnodeapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainTransactionNodeApiKey.md
ms.openlocfilehash: 6f39e869137996a64c5fc440ee0c2c8bb559542b
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94232122"
---
# <span data-ttu-id="b45d5-101">New-AzBlockchainTransactionNodeApiKey</span><span class="sxs-lookup"><span data-stu-id="b45d5-101">New-AzBlockchainTransactionNodeApiKey</span></span>

## <span data-ttu-id="b45d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b45d5-102">SYNOPSIS</span></span>
<span data-ttu-id="b45d5-103">Ponowne generowanie kluczy interfejsu API dla elementu członkowskiego Blockchain.</span><span class="sxs-lookup"><span data-stu-id="b45d5-103">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="b45d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b45d5-104">SYNTAX</span></span>

### <span data-ttu-id="b45d5-105">RegenerateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b45d5-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 -TransactionNodeName <String> [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b45d5-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b45d5-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainTransactionNodeApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b45d5-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b45d5-107">DESCRIPTION</span></span>
<span data-ttu-id="b45d5-108">Ponowne generowanie kluczy interfejsu API dla elementu członkowskiego Blockchain.</span><span class="sxs-lookup"><span data-stu-id="b45d5-108">Regenerate the API keys for the blockchain member.</span></span>

## <span data-ttu-id="b45d5-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b45d5-109">EXAMPLES</span></span>

### <span data-ttu-id="b45d5-110">Przykład 1: ponowne generowanie kluczy API dla węzła transakcji przy użyciu nazwy.</span><span class="sxs-lookup"><span data-stu-id="b45d5-110">Example 1: Regenerate Api keys for a transaction node using name.</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="b45d5-111">To polecenie generuje klucze API dla węzła Transaction przy użyciu nazwy, grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b45d5-111">This command generates Api keys for a transaction node using name, resource group.</span></span>

### <span data-ttu-id="b45d5-112">Przykład 2: ponowne generowanie kluczy interfejsu API dla węzła transakcji</span><span class="sxs-lookup"><span data-stu-id="b45d5-112">Example 2: Regenerate Api keys for a transaction node</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainTransactionNodeApiKey -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> $tNode = Get-AzBlockchainTransactionNode -BlockchainMemberName dolauli001 -ResourceGroupName testgroup -TransactionNodeName tranctionnode001 
PS C:\> New-AzBlockchainTransactionNodeApiKey -InputObject $tNode -KeyName $keyPair[0].KeyName 

KeyName Value
------- -----
key1    0-UCaNSNfS0lwRKRyv09sgb-
key2    0Prk4Dl3lsOKdhyPEFQ-AnQb
```

<span data-ttu-id="b45d5-113">To polecenie generuje klucze interfejsu API dla węzła transakcji przy użyciu idenity.</span><span class="sxs-lookup"><span data-stu-id="b45d5-113">This command generates Api keys for a transaction node using idenity.</span></span>

## <span data-ttu-id="b45d5-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b45d5-114">PARAMETERS</span></span>

### <span data-ttu-id="b45d5-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="b45d5-115">-BlockchainMemberName</span></span>
<span data-ttu-id="b45d5-116">Nazwa członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="b45d5-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="b45d5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b45d5-117">-DefaultProfile</span></span>
<span data-ttu-id="b45d5-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b45d5-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b45d5-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b45d5-119">-InputObject</span></span>
<span data-ttu-id="b45d5-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="b45d5-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b45d5-121">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="b45d5-121">-KeyName</span></span>
<span data-ttu-id="b45d5-122">Pobiera lub ustawia nazwę klucza interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b45d5-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="b45d5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b45d5-123">-ResourceGroupName</span></span>
<span data-ttu-id="b45d5-124">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="b45d5-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b45d5-125">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="b45d5-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b45d5-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b45d5-126">-SubscriptionId</span></span>
<span data-ttu-id="b45d5-127">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b45d5-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b45d5-128">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="b45d5-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b45d5-129">-TransactionNodeName</span><span class="sxs-lookup"><span data-stu-id="b45d5-129">-TransactionNodeName</span></span>
<span data-ttu-id="b45d5-130">Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="b45d5-130">Transaction node name.</span></span>

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

### <span data-ttu-id="b45d5-131">-Value</span><span class="sxs-lookup"><span data-stu-id="b45d5-131">-Value</span></span>
<span data-ttu-id="b45d5-132">Pobiera lub ustawia wartość klucza interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b45d5-132">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="b45d5-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b45d5-133">-Confirm</span></span>
<span data-ttu-id="b45d5-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b45d5-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b45d5-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b45d5-135">-WhatIf</span></span>
<span data-ttu-id="b45d5-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b45d5-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b45d5-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b45d5-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b45d5-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b45d5-138">CommonParameters</span></span>
<span data-ttu-id="b45d5-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b45d5-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b45d5-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b45d5-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b45d5-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b45d5-141">INPUTS</span></span>

### <span data-ttu-id="b45d5-142">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="b45d5-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="b45d5-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b45d5-143">OUTPUTS</span></span>

### <span data-ttu-id="b45d5-144">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="b45d5-144">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="b45d5-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b45d5-145">NOTES</span></span>

<span data-ttu-id="b45d5-146">PISUJE</span><span class="sxs-lookup"><span data-stu-id="b45d5-146">ALIASES</span></span>

<span data-ttu-id="b45d5-147">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b45d5-147">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b45d5-148">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b45d5-148">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b45d5-149">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b45d5-149">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b45d5-150">INPUTobject <IBlockchainIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="b45d5-150">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b45d5-151">`[BlockchainMemberName <String>]`: Blockchain nazwa członka.</span><span class="sxs-lookup"><span data-stu-id="b45d5-151">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="b45d5-152">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b45d5-152">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b45d5-153">`[Location <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b45d5-153">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="b45d5-154">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="b45d5-154">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="b45d5-155">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="b45d5-155">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b45d5-156">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="b45d5-156">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b45d5-157">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b45d5-157">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="b45d5-158">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="b45d5-158">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="b45d5-159">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="b45d5-159">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="b45d5-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b45d5-160">RELATED LINKS</span></span>

