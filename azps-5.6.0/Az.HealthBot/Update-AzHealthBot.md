---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/update-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Update-AzHealthBot.md
ms.openlocfilehash: a0dc204bb6dc1a91031a87fd113c525f282f090e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013210"
---
# <span data-ttu-id="44ba7-101">Update-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="44ba7-101">Update-AzHealthBot</span></span>

## <span data-ttu-id="44ba7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="44ba7-103">Popraw poprawki robota HealthBot.</span><span class="sxs-lookup"><span data-stu-id="44ba7-103">Patch a HealthBot.</span></span>

## <span data-ttu-id="44ba7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="44ba7-104">SYNTAX</span></span>

### <span data-ttu-id="44ba7-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="44ba7-105">UpdateExpanded (Default)</span></span>
```
Update-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>] [-Sku <SkuName>]
 [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="44ba7-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="44ba7-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzHealthBot -InputObject <IHealthBotIdentity> [-Sku <SkuName>] [-Tag <Hashtable>]
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="44ba7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="44ba7-107">DESCRIPTION</span></span>
<span data-ttu-id="44ba7-108">Popraw poprawki robota HealthBot.</span><span class="sxs-lookup"><span data-stu-id="44ba7-108">Patch a HealthBot.</span></span>

## <span data-ttu-id="44ba7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="44ba7-109">EXAMPLES</span></span>

### <span data-ttu-id="44ba7-110">Przykład 1. Aktualizowanie pliku HealthBot według nazwy grupy zasobów i nazwy</span><span class="sxs-lookup"><span data-stu-id="44ba7-110">Example 1: update HealthBot by Resourcegroupname and Name</span></span>
```powershell
PS C:\> update-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot -Sku S1

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="44ba7-111">aktualizowanie pola HealthBot według nazw i nazw grup zasobów</span><span class="sxs-lookup"><span data-stu-id="44ba7-111">update HealthBot by Resourcegroupname and Name</span></span>

### <span data-ttu-id="44ba7-112">Przykład 2. Aktualizowanie robota HealthBot przez InputObject</span><span class="sxs-lookup"><span data-stu-id="44ba7-112">Example 2: update HealthBot by InputObject</span></span>
```powershell
PS C:\> $getHealth = Get-AzHealthBot -ResourceGroupName youriTest -Name yourihealthbot
Update-AzHealthBot -InputObject $getHealth -Sku F0

Location Name           SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy SystemDataLastModifiedByType Type
-------- ----           ------------------- -------------------   ----------------------- ------------------------ ------------------------ ---------------------------- ----
eastus   yourihealthbot 2020/12/29 8:19:10  test@microsoft.com User                    2020/12/30 6:12:33       test@microsoft.com    User                         Microsoft.HealthBot/health…
```

<span data-ttu-id="44ba7-113">aktualizowanie robota HealthBot przez InputObject</span><span class="sxs-lookup"><span data-stu-id="44ba7-113">update HealthBot by InputObject</span></span>

## <span data-ttu-id="44ba7-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44ba7-114">PARAMETERS</span></span>

### <span data-ttu-id="44ba7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44ba7-115">-DefaultProfile</span></span>
<span data-ttu-id="44ba7-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="44ba7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44ba7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="44ba7-117">-InputObject</span></span>
<span data-ttu-id="44ba7-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="44ba7-118">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="44ba7-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="44ba7-119">-Name</span></span>
<span data-ttu-id="44ba7-120">Nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="44ba7-120">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ba7-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="44ba7-121">-ResourceGroupName</span></span>
<span data-ttu-id="44ba7-122">Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="44ba7-122">The name of the Bot resource group in the user subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ba7-123">- SKU</span><span class="sxs-lookup"><span data-stu-id="44ba7-123">-Sku</span></span>
<span data-ttu-id="44ba7-124">Nazwa sku HealthBot</span><span class="sxs-lookup"><span data-stu-id="44ba7-124">The name of the HealthBot SKU</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ba7-125">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="44ba7-125">-SubscriptionId</span></span>
<span data-ttu-id="44ba7-126">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="44ba7-126">Azure Subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ba7-127">— Tag</span><span class="sxs-lookup"><span data-stu-id="44ba7-127">-Tag</span></span>
<span data-ttu-id="44ba7-128">Tagi dla robota HealthBot.</span><span class="sxs-lookup"><span data-stu-id="44ba7-128">Tags for a HealthBot.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="44ba7-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="44ba7-129">-Confirm</span></span>
<span data-ttu-id="44ba7-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="44ba7-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44ba7-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44ba7-131">-WhatIf</span></span>
<span data-ttu-id="44ba7-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44ba7-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44ba7-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="44ba7-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44ba7-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44ba7-134">CommonParameters</span></span>
<span data-ttu-id="44ba7-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44ba7-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44ba7-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44ba7-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44ba7-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44ba7-137">INPUTS</span></span>

### <span data-ttu-id="44ba7-138">Microsoft.Azure.PowerShell.Cmdlet.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="44ba7-138">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="44ba7-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44ba7-139">OUTPUTS</span></span>

### <span data-ttu-id="44ba7-140">Microsoft.Azure.PowerShell.Cmdlet.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="44ba7-140">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="44ba7-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="44ba7-141">NOTES</span></span>

<span data-ttu-id="44ba7-142">ALIASY</span><span class="sxs-lookup"><span data-stu-id="44ba7-142">ALIASES</span></span>

<span data-ttu-id="44ba7-143">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="44ba7-143">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="44ba7-144">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="44ba7-144">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="44ba7-145">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="44ba7-145">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="44ba7-146">INPUTOBJECT: <IHealthBotIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="44ba7-146">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="44ba7-147">`[BotName <String>]`: nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="44ba7-147">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="44ba7-148">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="44ba7-148">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="44ba7-149">`[ResourceGroupName <String>]`: nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="44ba7-149">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="44ba7-150">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="44ba7-150">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="44ba7-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44ba7-151">RELATED LINKS</span></span>

