---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/update-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
ms.openlocfilehash: f7dd02a214fa32223e052c1999329699f1c653e9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200842"
---
# <span data-ttu-id="7e809-101">Update-AzBotService</span><span class="sxs-lookup"><span data-stu-id="7e809-101">Update-AzBotService</span></span>

## <span data-ttu-id="7e809-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e809-102">SYNOPSIS</span></span>
<span data-ttu-id="7e809-103">Aktualizacja usługi bota</span><span class="sxs-lookup"><span data-stu-id="7e809-103">Updates a Bot Service</span></span>

## <span data-ttu-id="7e809-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7e809-104">SYNTAX</span></span>

### <span data-ttu-id="7e809-105">UpdateExpanded (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="7e809-105">UpdateExpanded (Default)</span></span>
```
Update-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7e809-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="7e809-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBotService -InputObject <IBotServiceIdentity> [-Description <String>]
 [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7e809-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7e809-107">DESCRIPTION</span></span>
<span data-ttu-id="7e809-108">Aktualizacja usługi bota</span><span class="sxs-lookup"><span data-stu-id="7e809-108">Updates a Bot Service</span></span>

## <span data-ttu-id="7e809-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7e809-109">EXAMPLES</span></span>

### <span data-ttu-id="7e809-110">Przykład 1. Aktualizowanie bota według nazw i nazw grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7e809-110">Example 1: Update the Bot by Name and ResourceGroupName</span></span>
```powershell
PS C:\> Update-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest' -kind Bot

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"0700e71b-0000-1800-0000-5fd73ed80000" Bot  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="7e809-111">Aktualizowanie bota według nazw i nazw grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7e809-111">Update the Bot by Name and ResourceGroupName</span></span>

### <span data-ttu-id="7e809-112">Przykład 2. Aktualizowanie bota przez InputObject</span><span class="sxs-lookup"><span data-stu-id="7e809-112">Example 2: Update the Bot by InputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest'
Update-AzBotService -InputObject $getAzbot -kind sdk

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"07008b1c-0000-1800-0000-5fd73f9e0000" sdk  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="7e809-113">Aktualizowanie bota przez InputObject</span><span class="sxs-lookup"><span data-stu-id="7e809-113">Update the Bot by InputObject</span></span>

## <span data-ttu-id="7e809-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7e809-114">PARAMETERS</span></span>

### <span data-ttu-id="7e809-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e809-115">-DefaultProfile</span></span>
<span data-ttu-id="7e809-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7e809-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7e809-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="7e809-117">-Description</span></span>
<span data-ttu-id="7e809-118">Opis bota</span><span class="sxs-lookup"><span data-stu-id="7e809-118">The description of the bot</span></span>

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

### <span data-ttu-id="7e809-119">- DeveloperAppInsightKey</span><span class="sxs-lookup"><span data-stu-id="7e809-119">-DeveloperAppInsightKey</span></span>
<span data-ttu-id="7e809-120">Klucz szczegółowych informacji o aplikacji</span><span class="sxs-lookup"><span data-stu-id="7e809-120">The Application Insights key</span></span>

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

### <span data-ttu-id="7e809-121">-DeveloperAppInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="7e809-121">-DeveloperAppInsightsApiKey</span></span>
<span data-ttu-id="7e809-122">Klucz interfejsu API szczegółowych informacji aplikacji</span><span class="sxs-lookup"><span data-stu-id="7e809-122">The Application Insights Api Key</span></span>

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

### <span data-ttu-id="7e809-123">-DeveloperAppInsightsApplicationId</span><span class="sxs-lookup"><span data-stu-id="7e809-123">-DeveloperAppInsightsApplicationId</span></span>
<span data-ttu-id="7e809-124">Identyfikator aplikacji Szczegółowe informacje o aplikacji</span><span class="sxs-lookup"><span data-stu-id="7e809-124">The Application Insights App Id</span></span>

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

### <span data-ttu-id="7e809-125">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="7e809-125">-DisplayName</span></span>
<span data-ttu-id="7e809-126">Nazwa bota</span><span class="sxs-lookup"><span data-stu-id="7e809-126">The Name of the bot</span></span>

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

### <span data-ttu-id="7e809-127">- Punkt końcowy</span><span class="sxs-lookup"><span data-stu-id="7e809-127">-Endpoint</span></span>
<span data-ttu-id="7e809-128">Punkt końcowy bota</span><span class="sxs-lookup"><span data-stu-id="7e809-128">The bot's endpoint</span></span>

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

### <span data-ttu-id="7e809-129">— Otagowanie</span><span class="sxs-lookup"><span data-stu-id="7e809-129">-Etag</span></span>
<span data-ttu-id="7e809-130">Tag jednostki</span><span class="sxs-lookup"><span data-stu-id="7e809-130">Entity Tag</span></span>

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

### <span data-ttu-id="7e809-131">- IconUrl</span><span class="sxs-lookup"><span data-stu-id="7e809-131">-IconUrl</span></span>
<span data-ttu-id="7e809-132">Adres URL ikony bota</span><span class="sxs-lookup"><span data-stu-id="7e809-132">The Icon Url of the bot</span></span>

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

### <span data-ttu-id="7e809-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7e809-133">-InputObject</span></span>
<span data-ttu-id="7e809-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="7e809-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7e809-135">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="7e809-135">-Kind</span></span>
<span data-ttu-id="7e809-136">Wymagane.</span><span class="sxs-lookup"><span data-stu-id="7e809-136">Required.</span></span>
<span data-ttu-id="7e809-137">Pobiera lub ustawia rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="7e809-137">Gets or sets the Kind of the resource.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Support.Kind
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e809-138">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7e809-138">-Location</span></span>
<span data-ttu-id="7e809-139">Określa lokalizację zasobu.</span><span class="sxs-lookup"><span data-stu-id="7e809-139">Specifies the location of the resource.</span></span>

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

### <span data-ttu-id="7e809-140">-LuisAppId</span><span class="sxs-lookup"><span data-stu-id="7e809-140">-LuisAppId</span></span>
<span data-ttu-id="7e809-141">Kolekcja identyfikatorów aplikacji USŁUGI LUIS</span><span class="sxs-lookup"><span data-stu-id="7e809-141">Collection of LUIS App Ids</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e809-142">-LuisKey</span><span class="sxs-lookup"><span data-stu-id="7e809-142">-LuisKey</span></span>
<span data-ttu-id="7e809-143">Klucz USŁUGI LUIS</span><span class="sxs-lookup"><span data-stu-id="7e809-143">The LUIS Key</span></span>

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

### <span data-ttu-id="7e809-144">- MsaAppId</span><span class="sxs-lookup"><span data-stu-id="7e809-144">-MsaAppId</span></span>
<span data-ttu-id="7e809-145">Identyfikator aplikacji Firmy Microsoft dla bota</span><span class="sxs-lookup"><span data-stu-id="7e809-145">Microsoft App Id for the bot</span></span>

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

### <span data-ttu-id="7e809-146">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7e809-146">-Name</span></span>
<span data-ttu-id="7e809-147">Nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="7e809-147">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="7e809-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e809-148">-ResourceGroupName</span></span>
<span data-ttu-id="7e809-149">Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7e809-149">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="7e809-150">-SKUName</span><span class="sxs-lookup"><span data-stu-id="7e809-150">-SkuName</span></span>
<span data-ttu-id="7e809-151">Nazwa sKU</span><span class="sxs-lookup"><span data-stu-id="7e809-151">The sku name</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Support.SkuName
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7e809-152">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7e809-152">-SubscriptionId</span></span>
<span data-ttu-id="7e809-153">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7e809-153">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="7e809-154">— Tag</span><span class="sxs-lookup"><span data-stu-id="7e809-154">-Tag</span></span>
<span data-ttu-id="7e809-155">Tagi zasobów zdefiniowane jako pary klucz/wartość.</span><span class="sxs-lookup"><span data-stu-id="7e809-155">Contains resource tags defined as key/value pairs.</span></span>

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

### <span data-ttu-id="7e809-156">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7e809-156">-Confirm</span></span>
<span data-ttu-id="7e809-157">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7e809-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e809-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e809-158">-WhatIf</span></span>
<span data-ttu-id="7e809-159">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7e809-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e809-160">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7e809-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e809-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e809-161">CommonParameters</span></span>
<span data-ttu-id="7e809-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e809-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e809-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7e809-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e809-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7e809-164">INPUTS</span></span>

### <span data-ttu-id="7e809-165">Microsoft.Azure.PowerShell.Cmdlet.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="7e809-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="7e809-166">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="7e809-166">OUTPUTS</span></span>

### <span data-ttu-id="7e809-167">Microsoft.Azure.PowerShell.cmdlet.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="7e809-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="7e809-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7e809-168">NOTES</span></span>

<span data-ttu-id="7e809-169">ALIASY</span><span class="sxs-lookup"><span data-stu-id="7e809-169">ALIASES</span></span>

<span data-ttu-id="7e809-170">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7e809-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="7e809-171">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="7e809-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="7e809-172">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="7e809-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="7e809-173">INPUTOBJECT: <IBotServiceIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="7e809-173">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="7e809-174">`[ChannelName <ChannelName?>]`: nazwa zasobu Kanał.</span><span class="sxs-lookup"><span data-stu-id="7e809-174">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="7e809-175">`[ConnectionName <String>]`: nazwa zasobu ustawień połączenia usługi bota</span><span class="sxs-lookup"><span data-stu-id="7e809-175">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="7e809-176">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="7e809-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="7e809-177">`[ResourceGroupName <String>]`: nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7e809-177">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="7e809-178">`[ResourceName <String>]`: nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="7e809-178">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="7e809-179">`[SubscriptionId <String>]`: Azure Subscription ID.</span><span class="sxs-lookup"><span data-stu-id="7e809-179">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="7e809-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7e809-180">RELATED LINKS</span></span>

