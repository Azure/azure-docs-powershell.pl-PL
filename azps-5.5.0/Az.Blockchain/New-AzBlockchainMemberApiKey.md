---
external help file: ''
Module Name: Az.Blockchain
online version: https://docs.microsoft.com/en-us/powershell/module/az.blockchain/new-azblockchainmemberapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blockchain/help/New-AzBlockchainMemberApiKey.md
ms.openlocfilehash: 7571195b00778b4bce37b3ad7e06d9a6c35cfaaa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177954"
---
# <span data-ttu-id="74de0-101">New-AzBlockchainMemberApiKey</span><span class="sxs-lookup"><span data-stu-id="74de0-101">New-AzBlockchainMemberApiKey</span></span>

## <span data-ttu-id="74de0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74de0-102">SYNOPSIS</span></span>
<span data-ttu-id="74de0-103">Ponownie generuj klucze interfejsu API dla członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="74de0-103">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="74de0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="74de0-104">SYNTAX</span></span>

### <span data-ttu-id="74de0-105">Generuj ponownieRozwiń (domyślne)</span><span class="sxs-lookup"><span data-stu-id="74de0-105">RegenerateExpanded (Default)</span></span>
```
New-AzBlockchainMemberApiKey -BlockchainMemberName <String> -ResourceGroupName <String>
 [-SubscriptionId <String>] [-KeyName <String>] [-Value <String>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="74de0-106">Generuj generujViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="74de0-106">RegenerateViaIdentityExpanded</span></span>
```
New-AzBlockchainMemberApiKey -InputObject <IBlockchainIdentity> [-KeyName <String>] [-Value <String>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="74de0-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="74de0-107">DESCRIPTION</span></span>
<span data-ttu-id="74de0-108">Ponownie generuj klucze interfejsu API dla członka zespołu.</span><span class="sxs-lookup"><span data-stu-id="74de0-108">Regenerate the API keys for a blockchain member.</span></span>

## <span data-ttu-id="74de0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="74de0-109">EXAMPLES</span></span>

### <span data-ttu-id="74de0-110">Przykład 1. Generuj klucze interfejsu Api dla członka zespołu używającego nazwy</span><span class="sxs-lookup"><span data-stu-id="74de0-110">Example 1: Regenerate Api keys for a blockchain member using name</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    D7wyajHMZcBw4MndMgytqanz
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="74de0-111">To polecenie ponownie generuje klucze interfejsu Api dla członka zespołu korzystającego z nazwy, grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="74de0-111">This command regenerates Api keys for a blockchain member using name, resource group.</span></span>

### <span data-ttu-id="74de0-112">Przykład 2. Generuj klucze interfejsu Api dla członka zespołu korzystającego z idenity</span><span class="sxs-lookup"><span data-stu-id="74de0-112">Example 2: Regenerate Api keys for a blockchain member using idenity</span></span>
```powershell
PS C:\> $keyPair = Get-AzBlockchainMemberApiKey -BlockchainMemberName myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> $bcMember = Get-AzBlockchainMember -Name myblockchainhlqc92 -ResourceGroupName bc-rg
PS C:\> New-AzBlockchainMemberApiKey -InputObject $bcMember -KeyName $keyPair[0].KeyName

KeyName Value
------- -----
key1    DdsyaaHsdasd46asd8Bw4Mnd
key2    eu9kx94TKH506R0i4JhYBmsx
```

<span data-ttu-id="74de0-113">To polecenie ponownie generuje klucze interfejsu Api dla użytkownika korzystającego z tożsamości.</span><span class="sxs-lookup"><span data-stu-id="74de0-113">This command regenerates Api keys for a blockchain member using identity.</span></span>

## <span data-ttu-id="74de0-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74de0-114">PARAMETERS</span></span>

### <span data-ttu-id="74de0-115">-Wymusz na użytkownikach</span><span class="sxs-lookup"><span data-stu-id="74de0-115">-BlockchainMemberName</span></span>
<span data-ttu-id="74de0-116">Nie ma w tym celu nazwy użytkownika.</span><span class="sxs-lookup"><span data-stu-id="74de0-116">Blockchain member name.</span></span>

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

### <span data-ttu-id="74de0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74de0-117">-DefaultProfile</span></span>
<span data-ttu-id="74de0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="74de0-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74de0-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="74de0-119">-InputObject</span></span>
<span data-ttu-id="74de0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="74de0-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="74de0-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="74de0-121">-KeyName</span></span>
<span data-ttu-id="74de0-122">Pobiera lub ustawia nazwę klucza interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="74de0-122">Gets or sets the API key name.</span></span>

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

### <span data-ttu-id="74de0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74de0-123">-ResourceGroupName</span></span>
<span data-ttu-id="74de0-124">Nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="74de0-124">The name of the resource group that contains the resource.</span></span>
<span data-ttu-id="74de0-125">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="74de0-125">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>

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

### <span data-ttu-id="74de0-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="74de0-126">-SubscriptionId</span></span>
<span data-ttu-id="74de0-127">Pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="74de0-127">Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span>
<span data-ttu-id="74de0-128">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="74de0-128">The subscription ID is part of the URI for every service call.</span></span>

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

### <span data-ttu-id="74de0-129">— Wartość</span><span class="sxs-lookup"><span data-stu-id="74de0-129">-Value</span></span>
<span data-ttu-id="74de0-130">Pobiera lub ustawia wartość klucza interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="74de0-130">Gets or sets the API key value.</span></span>

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

### <span data-ttu-id="74de0-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74de0-131">-Confirm</span></span>
<span data-ttu-id="74de0-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="74de0-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74de0-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74de0-133">-WhatIf</span></span>
<span data-ttu-id="74de0-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74de0-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74de0-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="74de0-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74de0-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74de0-136">CommonParameters</span></span>
<span data-ttu-id="74de0-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74de0-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74de0-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="74de0-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74de0-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74de0-139">INPUTS</span></span>

### <span data-ttu-id="74de0-140">Microsoft.Azure.PowerShell.cmdlet.uściśl.models.iBlockchainIdentity</span><span class="sxs-lookup"><span data-stu-id="74de0-140">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.IBlockchainIdentity</span></span>

## <span data-ttu-id="74de0-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74de0-141">OUTPUTS</span></span>

### <span data-ttu-id="74de0-142">Microsoft.Azure.PowerShell.cmdlet.u7.models.api20180601Preview.IApiKey</span><span class="sxs-lookup"><span data-stu-id="74de0-142">Microsoft.Azure.PowerShell.Cmdlets.Blockchain.Models.Api20180601Preview.IApiKey</span></span>

## <span data-ttu-id="74de0-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="74de0-143">NOTES</span></span>

<span data-ttu-id="74de0-144">ALIASY</span><span class="sxs-lookup"><span data-stu-id="74de0-144">ALIASES</span></span>

<span data-ttu-id="74de0-145">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="74de0-145">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="74de0-146">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="74de0-146">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="74de0-147">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="74de0-147">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="74de0-148">INPUTOBJECT: <IBlockchainIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="74de0-148">INPUTOBJECT <IBlockchainIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="74de0-149">`[BlockchainMemberName <String>]`: Dodano nazwę członka.</span><span class="sxs-lookup"><span data-stu-id="74de0-149">`[BlockchainMemberName <String>]`: Blockchain member name.</span></span>
  - <span data-ttu-id="74de0-150">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="74de0-150">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="74de0-151">`[Location <String>]`: nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="74de0-151">`[Location <String>]`: Location name.</span></span>
  - <span data-ttu-id="74de0-152">`[OperationId <String>]`: Identyfikator operacji.</span><span class="sxs-lookup"><span data-stu-id="74de0-152">`[OperationId <String>]`: Operation Id.</span></span>
  - <span data-ttu-id="74de0-153">`[ResourceGroupName <String>]`: nazwa grupy zasobów, która zawiera zasób.</span><span class="sxs-lookup"><span data-stu-id="74de0-153">`[ResourceGroupName <String>]`: The name of the resource group that contains the resource.</span></span> <span data-ttu-id="74de0-154">Tę wartość można uzyskać z interfejsu API usługi Azure Resource Manager lub portalu.</span><span class="sxs-lookup"><span data-stu-id="74de0-154">You can obtain this value from the Azure Resource Manager API or the portal.</span></span>
  - <span data-ttu-id="74de0-155">`[SubscriptionId <String>]`: pobiera identyfikator subskrypcji, który jednoznacznie identyfikuje subskrypcję platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="74de0-155">`[SubscriptionId <String>]`: Gets the subscription Id which uniquely identifies the Microsoft Azure subscription.</span></span> <span data-ttu-id="74de0-156">Identyfikator subskrypcji jest częścią identyfikatora URI dla każdego wywołania usługi.</span><span class="sxs-lookup"><span data-stu-id="74de0-156">The subscription ID is part of the URI for every service call.</span></span>
  - <span data-ttu-id="74de0-157">`[TransactionNodeName <String>]`: Nazwa węzła transakcji.</span><span class="sxs-lookup"><span data-stu-id="74de0-157">`[TransactionNodeName <String>]`: Transaction node name.</span></span>

## <span data-ttu-id="74de0-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74de0-158">RELATED LINKS</span></span>

