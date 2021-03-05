---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/get-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
ms.openlocfilehash: 305e65e95b876e3093f4a14590e8b2e111e44aeb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009313"
---
# <span data-ttu-id="1a63a-101">Get-AzBotService</span><span class="sxs-lookup"><span data-stu-id="1a63a-101">Get-AzBotService</span></span>

## <span data-ttu-id="1a63a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a63a-102">SYNOPSIS</span></span>
<span data-ttu-id="1a63a-103">Zwraca wartość botservice określoną w parametrach.</span><span class="sxs-lookup"><span data-stu-id="1a63a-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="1a63a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1a63a-104">SYNTAX</span></span>

### <span data-ttu-id="1a63a-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="1a63a-105">List1 (Default)</span></span>
```
Get-AzBotService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1a63a-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="1a63a-106">Get</span></span>
```
Get-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1a63a-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1a63a-107">GetViaIdentity</span></span>
```
Get-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="1a63a-108">Lista</span><span class="sxs-lookup"><span data-stu-id="1a63a-108">List</span></span>
```
Get-AzBotService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="1a63a-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="1a63a-109">DESCRIPTION</span></span>
<span data-ttu-id="1a63a-110">Zwraca wartość botservice określoną w parametrach.</span><span class="sxs-lookup"><span data-stu-id="1a63a-110">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="1a63a-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1a63a-111">EXAMPLES</span></span>

### <span data-ttu-id="1a63a-112">Przykład 1. Uzyskiwanie wszystkich usług BotServices</span><span class="sxs-lookup"><span data-stu-id="1a63a-112">Example 1: Get all BotServices</span></span>
```powershell
PS C:\> Get-AzBotService

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="1a63a-113">Uzyskaj wszystkie usługi BotServices</span><span class="sxs-lookup"><span data-stu-id="1a63a-113">Get all BotServices</span></span>

### <span data-ttu-id="1a63a-114">Przykład 2. Uzyskiwanie usługi BotService według nazwy i nazwy grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1a63a-114">Example 2: Get the BotService by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot F0              Microsoft.BotService/botServices
```

<span data-ttu-id="1a63a-115">Uzyskiwanie usługi BotService według nazwy i nazwy grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1a63a-115">Get the BotService by ResourceGroupName and Name</span></span>

### <span data-ttu-id="1a63a-116">Przykład 3. Uzyskiwanie wszystkich usług BotServices według nazwa_grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1a63a-116">Example 3: Get all BotServices by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzBotService -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="1a63a-117">Uzyskiwanie wszystkich usług BotServices według resourcegroupname</span><span class="sxs-lookup"><span data-stu-id="1a63a-117">Get all BotServices by ResourceGroupName</span></span>

### <span data-ttu-id="1a63a-118">Przykład 4. Uzyskiwanie usługi BotService przez inputObject</span><span class="sxs-lookup"><span data-stu-id="1a63a-118">Example 4: Get the BotService by inputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'
Get-AzBotService -InputObject $getAzbot

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="1a63a-119">Uzyskiwanie usługi BotService przez inputObject</span><span class="sxs-lookup"><span data-stu-id="1a63a-119">Get the BotService by inputObject</span></span>

## <span data-ttu-id="1a63a-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a63a-120">PARAMETERS</span></span>

### <span data-ttu-id="1a63a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a63a-121">-DefaultProfile</span></span>
<span data-ttu-id="1a63a-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a63a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1a63a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a63a-123">-InputObject</span></span>
<span data-ttu-id="1a63a-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="1a63a-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a63a-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1a63a-125">-Name</span></span>
<span data-ttu-id="1a63a-126">Nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="1a63a-126">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: BotName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a63a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a63a-127">-ResourceGroupName</span></span>
<span data-ttu-id="1a63a-128">Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1a63a-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="1a63a-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="1a63a-129">-SubscriptionId</span></span>
<span data-ttu-id="1a63a-130">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1a63a-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="1a63a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a63a-131">CommonParameters</span></span>
<span data-ttu-id="1a63a-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a63a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a63a-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a63a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a63a-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a63a-134">INPUTS</span></span>

### <span data-ttu-id="1a63a-135">Microsoft.Azure.PowerShell.cmdlet.BotService.Models.IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="1a63a-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="1a63a-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a63a-136">OUTPUTS</span></span>

### <span data-ttu-id="1a63a-137">Microsoft.Azure.PowerShell.cmdlet.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="1a63a-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="1a63a-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1a63a-138">NOTES</span></span>

<span data-ttu-id="1a63a-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="1a63a-139">ALIASES</span></span>

<span data-ttu-id="1a63a-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1a63a-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="1a63a-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="1a63a-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1a63a-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1a63a-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="1a63a-143">INPUTOBJECT: <IBotServiceIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="1a63a-143">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1a63a-144">`[ChannelName <ChannelName?>]`: nazwa zasobu Kanał.</span><span class="sxs-lookup"><span data-stu-id="1a63a-144">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="1a63a-145">`[ConnectionName <String>]`: nazwa zasobu ustawień połączenia usługi bota</span><span class="sxs-lookup"><span data-stu-id="1a63a-145">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="1a63a-146">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="1a63a-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1a63a-147">`[ResourceGroupName <String>]`: nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="1a63a-147">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="1a63a-148">`[ResourceName <String>]`: nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="1a63a-148">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="1a63a-149">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1a63a-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="1a63a-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a63a-150">RELATED LINKS</span></span>

