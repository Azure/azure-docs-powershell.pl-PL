---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/get-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/Get-AzBotService.md
ms.openlocfilehash: 4324c1e78ce56cc4b56455eaaff266b52c1d87d7
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502037"
---
# <span data-ttu-id="9643f-101">Get-AzBotService</span><span class="sxs-lookup"><span data-stu-id="9643f-101">Get-AzBotService</span></span>

## <span data-ttu-id="9643f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9643f-102">SYNOPSIS</span></span>
<span data-ttu-id="9643f-103">Zwraca wartość typu BotService określona przez parametry.</span><span class="sxs-lookup"><span data-stu-id="9643f-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="9643f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9643f-104">SYNTAX</span></span>

### <span data-ttu-id="9643f-105">List1 (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9643f-105">List1 (Default)</span></span>
```
Get-AzBotService [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9643f-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="9643f-106">Get</span></span>
```
Get-AzBotService -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9643f-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="9643f-107">GetViaIdentity</span></span>
```
Get-AzBotService -InputObject <IBotServiceIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="9643f-108">Lista</span><span class="sxs-lookup"><span data-stu-id="9643f-108">List</span></span>
```
Get-AzBotService -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="9643f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="9643f-109">DESCRIPTION</span></span>
<span data-ttu-id="9643f-110">Zwraca wartość typu BotService określona przez parametry.</span><span class="sxs-lookup"><span data-stu-id="9643f-110">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="9643f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9643f-111">EXAMPLES</span></span>

### <span data-ttu-id="9643f-112">Przykład 1: Pobierz wszystkie BotServices</span><span class="sxs-lookup"><span data-stu-id="9643f-112">Example 1: Get all BotServices</span></span>
```powershell
PS C:\> Get-AzBotService

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="9643f-113">Pobierz wszystkie BotServices</span><span class="sxs-lookup"><span data-stu-id="9643f-113">Get all BotServices</span></span>

### <span data-ttu-id="9643f-114">Przykład 2: uzyskiwanie BotService przez ResourceGroupName i imię i nazwisko</span><span class="sxs-lookup"><span data-stu-id="9643f-114">Example 2: Get the BotService by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot F0              Microsoft.BotService/botServices
```

<span data-ttu-id="9643f-115">Pobierz BotService przez ResourceGroupName i imię i nazwisko</span><span class="sxs-lookup"><span data-stu-id="9643f-115">Get the BotService by ResourceGroupName and Name</span></span>

### <span data-ttu-id="9643f-116">Przykład 3: Pobierz wszystkie BotServices przez ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9643f-116">Example 3: Get all BotServices by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzBotService -ResourceGroupName 'youriBotTest'

Etag                                   Kind Location Name             SkuName SkuTier Type
----                                   ---- -------- ----             ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest  F0              Microsoft.BotService/botServices
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1       F0              Microsoft.BotService/botServices
"05000ef7-0000-0200-0000-5fd7065a0000" sdk  global   youriechobottest S1              Microsoft.BotService/botServices
"0600ef2b-0000-0200-0000-5fd727a70000" sdk  global   youritest1314    S1              Microsoft.BotService/botServices
```

<span data-ttu-id="9643f-117">Pobierz wszystkie BotServices przez ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9643f-117">Get all BotServices by ResourceGroupName</span></span>

### <span data-ttu-id="9643f-118">Przykład 4: pobieranie BotService za pomocą narzędzia inputobject</span><span class="sxs-lookup"><span data-stu-id="9643f-118">Example 4: Get the BotService by inputObject</span></span>
```powershell
PS C:\> $getAzbot = Get-AzBotService -Name 'youri-bot1' -ResourceGroupName 'youriBotTest'
Get-AzBotService -InputObject $getAzbot

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="9643f-119">Pobierz BotService przez wejście</span><span class="sxs-lookup"><span data-stu-id="9643f-119">Get the BotService by inputObject</span></span>

## <span data-ttu-id="9643f-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9643f-120">PARAMETERS</span></span>

### <span data-ttu-id="9643f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9643f-121">-DefaultProfile</span></span>
<span data-ttu-id="9643f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9643f-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9643f-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9643f-123">-InputObject</span></span>
<span data-ttu-id="9643f-124">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="9643f-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="9643f-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9643f-125">-Name</span></span>
<span data-ttu-id="9643f-126">Nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="9643f-126">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="9643f-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9643f-127">-ResourceGroupName</span></span>
<span data-ttu-id="9643f-128">Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9643f-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="9643f-129">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="9643f-129">-SubscriptionId</span></span>
<span data-ttu-id="9643f-130">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9643f-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="9643f-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9643f-131">CommonParameters</span></span>
<span data-ttu-id="9643f-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9643f-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9643f-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9643f-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9643f-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9643f-134">INPUTS</span></span>

### <span data-ttu-id="9643f-135">Microsoft. Azure. PowerShell. polecenia. BotService. models. IBotServiceIdentity</span><span class="sxs-lookup"><span data-stu-id="9643f-135">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.IBotServiceIdentity</span></span>

## <span data-ttu-id="9643f-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9643f-136">OUTPUTS</span></span>

### <span data-ttu-id="9643f-137">Microsoft. Azure. PowerShell. polecenia. BotService. models. Api20180712. IBot</span><span class="sxs-lookup"><span data-stu-id="9643f-137">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="9643f-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9643f-138">NOTES</span></span>

<span data-ttu-id="9643f-139">PISUJE</span><span class="sxs-lookup"><span data-stu-id="9643f-139">ALIASES</span></span>

<span data-ttu-id="9643f-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9643f-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="9643f-141">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="9643f-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="9643f-142">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="9643f-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="9643f-143">INPUTobject <IBotServiceIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="9643f-143">INPUTOBJECT <IBotServiceIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="9643f-144">`[ChannelName <ChannelName?>]`: Nazwa zasobu kanału.</span><span class="sxs-lookup"><span data-stu-id="9643f-144">`[ChannelName <ChannelName?>]`: The name of the Channel resource.</span></span>
  - <span data-ttu-id="9643f-145">`[ConnectionName <String>]`: Nazwa zasobu Ustawienia połączenia z usługą bota</span><span class="sxs-lookup"><span data-stu-id="9643f-145">`[ConnectionName <String>]`: The name of the Bot Service Connection Setting resource</span></span>
  - <span data-ttu-id="9643f-146">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="9643f-146">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="9643f-147">`[ResourceGroupName <String>]`: Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9643f-147">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="9643f-148">`[ResourceName <String>]`: Nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="9643f-148">`[ResourceName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="9643f-149">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9643f-149">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="9643f-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9643f-150">RELATED LINKS</span></span>

