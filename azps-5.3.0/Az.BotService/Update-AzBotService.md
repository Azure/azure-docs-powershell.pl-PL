---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/update-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Update-AzBotService.md
ms.openlocfilehash: f7dd02a214fa32223e052c1999329699f1c653e9
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504222"
---
# <span data-ttu-id="dde2d-101">Update-AzBotService</span><span class="sxs-lookup"><span data-stu-id="dde2d-101">Update-AzBotService</span></span>

## <span data-ttu-id="dde2d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dde2d-102">SYNOPSIS</span></span>
<span data-ttu-id="dde2d-103">Aktualizowanie usługi bota</span><span class="sxs-lookup"><span data-stu-id="dde2d-103">Updates a Bot Service</span></span>

## <span data-ttu-id="dde2d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dde2d-104">SYNTAX</span></span>

### <span data-ttu-id="dde2d-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dde2d-105">UpdateExpanded (Default)</span></span>
```
Update-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-Description <String>] [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="dde2d-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="dde2d-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzBotService -InputObject <IBotServiceIdentity> [-Description <String>]
 [-DeveloperAppInsightKey <String>] [-DeveloperAppInsightsApiKey <String>]
 [-DeveloperAppInsightsApplicationId <String>] [-DisplayName <String>] [-Endpoint <String>] [-Etag <String>]
 [-IconUrl <String>] [-Kind <Kind>] [-Location <String>] [-LuisAppId <String[]>] [-LuisKey <String>]
 [-MsaAppId <String>] [-SkuName <SkuName>] [-Tag <Hashtable>] [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="dde2d-107">Opis</span><span class="sxs-lookup"><span data-stu-id="dde2d-107">DESCRIPTION</span></span>
<span data-ttu-id="dde2d-108">Aktualizowanie usługi bota</span><span class="sxs-lookup"><span data-stu-id="dde2d-108">Updates a Bot Service</span></span>

## <span data-ttu-id="dde2d-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dde2d-109">EXAMPLES</span></span>

### <span data-ttu-id="dde2d-110">Przykład 1: aktualizowanie bota za pomocą nazwy i ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dde2d-110">Example 1: Update the Bot by Name and ResourceGroupName</span></span>
```powershell
PS C:\> Update-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest' -kind Bot

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"0700e71b-0000-1800-0000-5fd73ed80000" Bot  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="dde2d-111">Aktualizowanie bota za pomocą nazwy i ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dde2d-111">Update the Bot by Name and ResourceGroupName</span></span>

### <span data-ttu-id="dde2d-112">Przykład 2: aktualizowanie bota za pomocą narzędzia Inputobject</span><span class="sxs-lookup"><span data-stu-id="dde2d-112">Example 2: Update the Bot by InputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-apptest' -ResourceGroupName 'youriBotTest'
Update-AzBotService -InputObject $getAzbot -kind sdk

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"07008b1c-0000-1800-0000-5fd73f9e0000" sdk  global   youri-apptest                 Microsoft.BotService/botServices
```

<span data-ttu-id="dde2d-113">Aktualizowanie bota za pomocą narzędzia Inputobject</span><span class="sxs-lookup"><span data-stu-id="dde2d-113">Update the Bot by InputObject</span></span>

## <span data-ttu-id="dde2d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dde2d-114">PARAMETERS</span></span>

### <span data-ttu-id="dde2d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dde2d-115">-DefaultProfile</span></span>
<span data-ttu-id="dde2d-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dde2d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dde2d-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="dde2d-117">-Description</span></span>
<span data-ttu-id="dde2d-118">Opis bota</span><span class="sxs-lookup"><span data-stu-id="dde2d-118">The description of the bot</span></span>

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

### <span data-ttu-id="dde2d-119">-DeveloperAppInsightKey</span><span class="sxs-lookup"><span data-stu-id="dde2d-119">-DeveloperAppInsightKey</span></span>
<span data-ttu-id="dde2d-120">Klucz Application Insights</span><span class="sxs-lookup"><span data-stu-id="dde2d-120">The Application Insights key</span></span>

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

### <span data-ttu-id="dde2d-121">-DeveloperAppInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="dde2d-121">-DeveloperAppInsightsApiKey</span></span>
<span data-ttu-id="dde2d-122">Klucz interfejsu API usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="dde2d-122">The Application Insights Api Key</span></span>

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

### <span data-ttu-id="dde2d-123">-DeveloperAppInsightsApplicationId</span><span class="sxs-lookup"><span data-stu-id="dde2d-123">-DeveloperAppInsightsApplicationId</span></span>
<span data-ttu-id="dde2d-124">Identyfikator aplikacji usługi Application Insights</span><span class="sxs-lookup"><span data-stu-id="dde2d-124">The Application Insights App Id</span></span>

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

### <span data-ttu-id="dde2d-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dde2d-125">-DisplayName</span></span>
<span data-ttu-id="dde2d-126">Nazwa bota</span><span class="sxs-lookup"><span data-stu-id="dde2d-126">The Name of the bot</span></span>

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

### <span data-ttu-id="dde2d-127">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="dde2d-127">-Endpoint</span></span>
<span data-ttu-id="dde2d-128">Punkt końcowy bota</span><span class="sxs-lookup"><span data-stu-id="dde2d-128">The bot's endpoint</span></span>

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

### <span data-ttu-id="dde2d-129">-ETag</span><span class="sxs-lookup"><span data-stu-id="dde2d-129">-Etag</span></span>
<span data-ttu-id="dde2d-130">Tag encja</span><span class="sxs-lookup"><span data-stu-id="dde2d-130">Entity Tag</span></span>

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

### <span data-ttu-id="dde2d-131">-IconUrl</span><span class="sxs-lookup"><span data-stu-id="dde2d-131">-IconUrl</span></span>
<span data-ttu-id="dde2d-132">Adres URL ikony bota</span><span class="sxs-lookup"><span data-stu-id="dde2d-132">The Icon Url of the bot</span></span>

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

### <span data-ttu-id="dde2d-133">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dde2d-133">-InputObject</span></span>
<span data-ttu-id="dde2d-134">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="dde2d-134">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="dde2d-135">-Kind</span><span class="sxs-lookup"><span data-stu-id="dde2d-135">-Kind</span></span>
<span data-ttu-id="dde2d-136">Wymagane.</span><span class="sxs-lookup"><span data-stu-id="dde2d-136">Required.</span></span>
<span data-ttu-id="dde2d-137">Pobiera lub ustawia Rodzaj zasobu.</span><span class="sxs-lookup"><span data-stu-id="dde2d-137">Gets or sets the Kind of the resource.</span></span>

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

### <span data-ttu-id="dde2d-138">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dde2d-138">-Location</span></span>
<span data-ttu-id="dde2d-139">Określa lokalizację zasobu.</span><span class="sxs-lookup"><span data-stu-id="dde2d-139">Specifies the location of the resource.</span></span>

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

### <span data-ttu-id="dde2d-140">-LuisAppId</span><span class="sxs-lookup"><span data-stu-id="dde2d-140">-LuisAppId</span></span>
<span data-ttu-id="dde2d-141">Kolekcja identyfikatorów aplikacji LUIS</span><span class="sxs-lookup"><span data-stu-id="dde2d-141">Collection of LUIS App Ids</span></span>

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

### <span data-ttu-id="dde2d-142">-LuisKey</span><span class="sxs-lookup"><span data-stu-id="dde2d-142">-LuisKey</span></span>
<span data-ttu-id="dde2d-143">Klucz LUIS</span><span class="sxs-lookup"><span data-stu-id="dde2d-143">The LUIS Key</span></span>

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

### <span data-ttu-id="dde2d-144">-MsaAppId</span><span class="sxs-lookup"><span data-stu-id="dde2d-144">-MsaAppId</span></span>
<span data-ttu-id="dde2d-145">Identyfikator aplikacji firmy Microsoft dla bota</span><span class="sxs-lookup"><span data-stu-id="dde2d-145">Microsoft App Id for the bot</span></span>

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

### <span data-ttu-id="dde2d-146">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dde2d-146">-Name</span></span>
<span data-ttu-id="dde2d-147">Nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="dde2d-147">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="dde2d-148">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dde2d-148">-ResourceGroupName</span></span>
<span data-ttu-id="dde2d-149">Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dde2d-149">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="dde2d-150">-SkuName</span><span class="sxs-lookup"><span data-stu-id="dde2d-150">-SkuName</span></span>
<span data-ttu-id="dde2d-151">Nazwa jednostki SKU</span><span class="sxs-lookup"><span data-stu-id="dde2d-151">The sku name</span></span>

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

### <span data-ttu-id="dde2d-152">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="dde2d-152">-SubscriptionId</span></span>
<span data-ttu-id="dde2d-153">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dde2d-153">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="dde2d-154">-Tag</span><span class="sxs-lookup"><span data-stu-id="dde2d-154">-Tag</span></span>
<span data-ttu-id="dde2d-155">Zawiera znaczniki zasobów zdefiniowane jako pary klucz/wartość.</span><span class="sxs-lookup"><span data-stu-id="dde2d-155">Contains resource tags defined as key/value pairs.</span></span>

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

### <span data-ttu-id="dde2d-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dde2d-156">-Confirm</span></span>
<span data-ttu-id="dde2d-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dde2d-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dde2d-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dde2d-158">-WhatIf</span></span>
<span data-ttu-id="dde2d-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dde2d-159">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dde2d-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dde2d-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dde2d-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dde2d-161">CommonParameters</span></span>
<span data-ttu-id="dde2d-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dde2d-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dde2d-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dde2d-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dde2d-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dde2d-164">INPUTS</span></span>

### <span data-ttu-id="dde2d-165">Microsoft. Azure. PowerShell. polecenia. BotService. models. IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="dde2d-165">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="dde2d-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dde2d-166">OUTPUTS</span></span>

### <span data-ttu-id="dde2d-167">Microsoft. Azure. PowerShell. polecenia. BotService. models. Api20180712. IBot</span><span class="sxs-lookup"><span data-stu-id="dde2d-167">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="dde2d-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dde2d-168">NOTES</span></span>

<span data-ttu-id="dde2d-169">PISUJE</span><span class="sxs-lookup"><span data-stu-id="dde2d-169">ALIASES</span></span>

<span data-ttu-id="dde2d-170">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dde2d-170">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="dde2d-171">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="dde2d-171">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="dde2d-172">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="dde2d-172">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="dde2d-173">INPUTobject <IBotServiceIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="dde2d-173">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="dde2d-174">`[ChannelName <ChannelName?>]`: Nazwa zasobu kanału.</span><span class="sxs-lookup"><span data-stu-id="dde2d-174">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="dde2d-175">`[ConnectionName <String>]`: Nazwa zasobu Ustawienia połączenia z usługą bota</span><span class="sxs-lookup"><span data-stu-id="dde2d-175">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="dde2d-176">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="dde2d-176">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="dde2d-177">`[ResourceGroupName <String>]`: Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="dde2d-177">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="dde2d-178">`[ResourceName <String>]`: Nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="dde2d-178">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="dde2d-179">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dde2d-179">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="dde2d-180">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dde2d-180">RELATED LINKS</span></span>

