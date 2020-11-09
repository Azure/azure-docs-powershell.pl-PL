---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 7571195b00778b4bce37b3ad7e06d9a6c35cfaaa
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94316746"
---
# <span data-ttu-id="b7ecc-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="b7ecc-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="b7ecc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b7ecc-102">SYNOPSIS</span></span>
<span data-ttu-id="b7ecc-103">Ponowne generowanie kluczy interfejsu API dla członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="b7ecc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b7ecc-104">SYNTAX</span></span>

### <span data-ttu-id="b7ecc-105">RegenerateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b7ecc-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="b7ecc-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="b7ecc-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="b7ecc-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b7ecc-107">DESCRIPTION</span></span>
<span data-ttu-id="b7ecc-108">Ponowne generowanie kluczy interfejsu API dla członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="b7ecc-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b7ecc-109">EXAMPLES</span></span>

### <span data-ttu-id="b7ecc-110">Przykład 1: ponowne generowanie kluczy API dla członka Blockchain przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="b7ecc-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="b7ecc-111">To polecenie generuje klucze API dla członka Blockchain przy użyciu nazwy, grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="b7ecc-112">Przykład 2: ponowne generowanie kluczy API dla elementu członkowskiego Blockchain przy użyciu idenity</span><span class="sxs-lookup"><span data-stu-id="b7ecc-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="b7ecc-113">To polecenie generuje klucze API dla członka Blockchain przy użyciu tożsamości.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="b7ecc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7ecc-114">PARAMETERS</span></span>

### <span data-ttu-id="b7ecc-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="b7ecc-115">-BlockchainMemberName</span></span>
<span data-ttu-id="b7ecc-116">Nazwa członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="b7ecc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ecc-117">-DefaultProfile</span></span>
<span data-ttu-id="b7ecc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7ecc-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b7ecc-119">-InputObject</span></span>
<span data-ttu-id="b7ecc-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="b7ecc-121">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="b7ecc-121">-KeyName</span></span>
<span data-ttu-id="b7ecc-122">Pobiera lub ustawia nazwę klucza interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="b7ecc-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7ecc-123">-ResourceGroupName</span></span>
<span data-ttu-id="b7ecc-124">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="b7ecc-125">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="b7ecc-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b7ecc-126">-SubscriptionId</span></span>
<span data-ttu-id="b7ecc-127">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="b7ecc-128">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="b7ecc-129">-Value</span><span class="sxs-lookup"><span data-stu-id="b7ecc-129">-Value</span></span>
<span data-ttu-id="b7ecc-130">Pobiera lub ustawia wartość klucza interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-130">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="b7ecc-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b7ecc-131">-Confirm</span></span>
<span data-ttu-id="b7ecc-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7ecc-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7ecc-133">-WhatIf</span></span>
<span data-ttu-id="b7ecc-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7ecc-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7ecc-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ecc-136">CommonParameters</span></span>
<span data-ttu-id="b7ecc-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ecc-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b7ecc-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ecc-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7ecc-139">INPUTS</span></span>

### <span data-ttu-id="b7ecc-140">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="b7ecc-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="b7ecc-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b7ecc-141">OUTPUTS</span></span>

### <span data-ttu-id="b7ecc-142">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="b7ecc-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="b7ecc-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b7ecc-143">NOTES</span></span>

<span data-ttu-id="b7ecc-144">PISUJE</span><span class="sxs-lookup"><span data-stu-id="b7ecc-144">ALIASES</span></span>

<span data-ttu-id="b7ecc-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b7ecc-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="b7ecc-146">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="b7ecc-147">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="b7ecc-148">INPUTobject <IBlockchainIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="b7ecc-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="b7ecc-149">`[BlockchainMemberName <String>]`: Blockchain nazwa członka.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="b7ecc-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="b7ecc-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="b7ecc-151">`[Location <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="b7ecc-152">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="b7ecc-153">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="b7ecc-154">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="b7ecc-155">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="b7ecc-156">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="b7ecc-157">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="b7ecc-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="b7ecc-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7ecc-158">RELATED LINKS</span></span>

