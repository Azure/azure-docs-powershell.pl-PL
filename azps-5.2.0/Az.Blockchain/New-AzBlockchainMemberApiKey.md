---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 7571195b00778b4bce37b3ad7e06d9a6c35cfaaa
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98341842"
---
# <span data-ttu-id="4ad98-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="4ad98-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="4ad98-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4ad98-102">SYNOPSIS</span></span>
<span data-ttu-id="4ad98-103">Ponowne generowanie kluczy interfejsu API dla członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="4ad98-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="4ad98-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4ad98-104">SYNTAX</span></span>

### <span data-ttu-id="4ad98-105">RegenerateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4ad98-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="4ad98-106">RegenerateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="4ad98-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="4ad98-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4ad98-107">DESCRIPTION</span></span>
<span data-ttu-id="4ad98-108">Ponowne generowanie kluczy interfejsu API dla członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="4ad98-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="4ad98-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4ad98-109">EXAMPLES</span></span>

### <span data-ttu-id="4ad98-110">Przykład 1: ponowne generowanie kluczy API dla członka Blockchain przy użyciu nazwy</span><span class="sxs-lookup"><span data-stu-id="4ad98-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="4ad98-111">To polecenie generuje klucze API dla członka Blockchain przy użyciu nazwy, grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4ad98-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="4ad98-112">Przykład 2: ponowne generowanie kluczy API dla elementu członkowskiego Blockchain przy użyciu idenity</span><span class="sxs-lookup"><span data-stu-id="4ad98-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="4ad98-113">To polecenie generuje klucze API dla członka Blockchain przy użyciu tożsamości.</span><span class="sxs-lookup"><span data-stu-id="4ad98-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="4ad98-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ad98-114">PARAMETERS</span></span>

### <span data-ttu-id="4ad98-115">-BlockchainMemberName</span><span class="sxs-lookup"><span data-stu-id="4ad98-115">-BlockchainMemberName</span></span>
<span data-ttu-id="4ad98-116">Nazwa członka Blockchain.</span><span class="sxs-lookup"><span data-stu-id="4ad98-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="4ad98-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4ad98-117">-DefaultProfile</span></span>
<span data-ttu-id="4ad98-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4ad98-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4ad98-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4ad98-119">-InputObject</span></span>
<span data-ttu-id="4ad98-120">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="4ad98-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="4ad98-121">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="4ad98-121">-KeyName</span></span>
<span data-ttu-id="4ad98-122">Pobiera lub ustawia nazwę klucza interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="4ad98-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="4ad98-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4ad98-123">-ResourceGroupName</span></span>
<span data-ttu-id="4ad98-124">Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="4ad98-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="4ad98-125">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="4ad98-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="4ad98-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="4ad98-126">-SubscriptionId</span></span>
<span data-ttu-id="4ad98-127">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4ad98-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="4ad98-128">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="4ad98-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="4ad98-129">-Value</span><span class="sxs-lookup"><span data-stu-id="4ad98-129">-Value</span></span>
<span data-ttu-id="4ad98-130">Pobiera lub ustawia wartość klucza interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="4ad98-130">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="4ad98-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4ad98-131">-Confirm</span></span>
<span data-ttu-id="4ad98-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ad98-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4ad98-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4ad98-133">-WhatIf</span></span>
<span data-ttu-id="4ad98-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4ad98-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4ad98-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4ad98-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4ad98-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4ad98-136">CommonParameters</span></span>
<span data-ttu-id="4ad98-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4ad98-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4ad98-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="4ad98-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4ad98-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4ad98-139">INPUTS</span></span>

### <span data-ttu-id="4ad98-140">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. IBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="4ad98-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="4ad98-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4ad98-141">OUTPUTS</span></span>

### <span data-ttu-id="4ad98-142">Microsoft. Azure. PowerShell. polecenia. Blockchain. models. Api20180601Preview. IApiKey</span><span class="sxs-lookup"><span data-stu-id="4ad98-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="4ad98-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4ad98-143">NOTES</span></span>

<span data-ttu-id="4ad98-144">PISUJE</span><span class="sxs-lookup"><span data-stu-id="4ad98-144">ALIASES</span></span>

<span data-ttu-id="4ad98-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4ad98-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="4ad98-146">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="4ad98-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="4ad98-147">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="4ad98-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="4ad98-148">INPUTobject <IBlockchainIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="4ad98-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="4ad98-149">`[BlockchainMemberName <String>]`: Blockchain nazwa członka.</span><span class="sxs-lookup"><span data-stu-id="4ad98-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="4ad98-150">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="4ad98-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="4ad98-151">`[Location <String>]`: Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="4ad98-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="4ad98-152">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="4ad98-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="4ad98-153">`[ResourceGroupName <String>]`: Nazwa grupy zasobów zawierającej dany zasób.</span><span class="sxs-lookup"><span data-stu-id="4ad98-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="4ad98-154">Tę wartość można uzyskać z interfejsu API Menedżera zasobów platformy Azure lub portalu.</span><span class="sxs-lookup"><span data-stu-id="4ad98-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="4ad98-155">`[SubscriptionId <String>]`: Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="4ad98-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="4ad98-156">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="4ad98-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="4ad98-157">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="4ad98-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="4ad98-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4ad98-158">RELATED LINKS</span></span>

