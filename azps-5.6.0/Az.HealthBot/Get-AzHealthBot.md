---
external help file: ''
Module Name: Az.HealthBot
online version: https://docs.microsoft.com/powershell/module/az.healthbot/get-azhealthbot
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/HealthBot/help/Get-AzHealthBot.md
ms.openlocfilehash: 1e9360c7545b1a8c566e1a373b8650e6b6800323
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102013233"
---
# <span data-ttu-id="bfac7-101">Get-AzHealthBot</span><span class="sxs-lookup"><span data-stu-id="bfac7-101">Get-AzHealthBot</span></span>

## <span data-ttu-id="bfac7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bfac7-102">SYNOPSIS</span></span>
<span data-ttu-id="bfac7-103">Uzyskaj robota HealthBot.</span><span class="sxs-lookup"><span data-stu-id="bfac7-103">Get a HealthBot.</span></span>

## <span data-ttu-id="bfac7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bfac7-104">SYNTAX</span></span>

### <span data-ttu-id="bfac7-105">Lista1 (domyślna)</span><span class="sxs-lookup"><span data-stu-id="bfac7-105">List1 (Default)</span></span>
```
Get-AzHealthBot [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bfac7-106">Pobierz</span><span class="sxs-lookup"><span data-stu-id="bfac7-106">Get</span></span>
```
Get-AzHealthBot -Name <String> -ResourceGroupName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bfac7-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="bfac7-107">GetViaIdentity</span></span>
```
Get-AzHealthBot -InputObject <IHealthBotIdentity> [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="bfac7-108">Lista</span><span class="sxs-lookup"><span data-stu-id="bfac7-108">List</span></span>
```
Get-AzHealthBot -ResourceGroupName <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="bfac7-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="bfac7-109">DESCRIPTION</span></span>
<span data-ttu-id="bfac7-110">Uzyskaj robota HealthBot.</span><span class="sxs-lookup"><span data-stu-id="bfac7-110">Get a HealthBot.</span></span>

## <span data-ttu-id="bfac7-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bfac7-111">EXAMPLES</span></span>

### <span data-ttu-id="bfac7-112">Przykład 1. Pobierz wszystkie boty HealthBot</span><span class="sxs-lookup"><span data-stu-id="bfac7-112">Example 1: Get all HealthBot</span></span>
```powershell
PS C:\> Get-AzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="bfac7-113">Uzyskaj wszystkie korzyści HealthBot</span><span class="sxs-lookup"><span data-stu-id="bfac7-113">Get all HealthBot</span></span>

### <span data-ttu-id="bfac7-114">Przykład 2. Uzyskiwanie wszystkich danych HealthBot według nazwa_grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bfac7-114">Example 2: Get all HealthBot by ResourceGroupName</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
eastus   yourihealthbotmemory 2020/12/29 6:54:32  test@microsoft.com User                    2020/12/29 6:54:36       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="bfac7-115">Get all HealthBot by ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfac7-115">Get all HealthBot by ResourceGroupName</span></span>

### <span data-ttu-id="bfac7-116">Przykład 3. Uzyskiwanie robota HealthBot według nazwy i nazwy grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bfac7-116">Example 3: Get HealthBot by ResourceGroupName and Name</span></span>
```powershell
PS C:\> Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="bfac7-117">Uzyskiwanie usługi HealthBot według pola ResourceGroupName i Name</span><span class="sxs-lookup"><span data-stu-id="bfac7-117">Get HealthBot by ResourceGroupName and Name</span></span>

### <span data-ttu-id="bfac7-118">Przykład 4. Uzyskiwanie robota HealthBot według inputObject</span><span class="sxs-lookup"><span data-stu-id="bfac7-118">Example 4: Get HealthBot by InputObject</span></span>
```powershell
PS C:\> $getAzHealthBot = Get-AzHealthBot -ResourceGroupName youriTest -name yourihealthbot
Get-AzHealthBot -InputObject $getAzHealthBot

Location Name                 SystemDataCreatedAt SystemDataCreatedBy   SystemDataCreatedByType SystemDataLastModifiedAt SystemDataLastModifiedBy             SystemDataLastModifiedByType Type
-------- ----                 ------------------- -------------------   ----------------------- ------------------------ ------------------------             ---------------------------- ----
eastus   yourihealthbot       2020/12/29 5:54:14  test@microsoft.com User                    2020/12/29 5:54:19       ********-****-****-****-********** Application                  Microsoft.HealthBot/healthBots
```

<span data-ttu-id="bfac7-119">Uzyskiwanie robota HealthBot przez InputObject</span><span class="sxs-lookup"><span data-stu-id="bfac7-119">Get HealthBot by InputObject</span></span>

## <span data-ttu-id="bfac7-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bfac7-120">PARAMETERS</span></span>

### <span data-ttu-id="bfac7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bfac7-121">-DefaultProfile</span></span>
<span data-ttu-id="bfac7-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bfac7-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bfac7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bfac7-123">-InputObject</span></span>
<span data-ttu-id="bfac7-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span><span class="sxs-lookup"><span data-stu-id="bfac7-124">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bfac7-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bfac7-125">-Name</span></span>
<span data-ttu-id="bfac7-126">Nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="bfac7-126">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="bfac7-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bfac7-127">-ResourceGroupName</span></span>
<span data-ttu-id="bfac7-128">Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bfac7-128">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="bfac7-129">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="bfac7-129">-SubscriptionId</span></span>
<span data-ttu-id="bfac7-130">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bfac7-130">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="bfac7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bfac7-131">CommonParameters</span></span>
<span data-ttu-id="bfac7-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bfac7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bfac7-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bfac7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bfac7-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfac7-134">INPUTS</span></span>

### <span data-ttu-id="bfac7-135">Microsoft.Azure.PowerShell.Cmdlet.HealthBot.Models.IHealthBotIdentity</span><span class="sxs-lookup"><span data-stu-id="bfac7-135">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.IHealthBotIdentity</span></span>

## <span data-ttu-id="bfac7-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bfac7-136">OUTPUTS</span></span>

### <span data-ttu-id="bfac7-137">Microsoft.Azure.PowerShell.Cmdlet.HealthBot.Models.Api20201208.IHealthBot</span><span class="sxs-lookup"><span data-stu-id="bfac7-137">Microsoft.Azure.PowerShell.Cmdlets.HealthBot.Models.Api20201208.IHealthBot</span></span>

## <span data-ttu-id="bfac7-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bfac7-138">NOTES</span></span>

<span data-ttu-id="bfac7-139">ALIASY</span><span class="sxs-lookup"><span data-stu-id="bfac7-139">ALIASES</span></span>

<span data-ttu-id="bfac7-140">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bfac7-140">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="bfac7-141">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="bfac7-141">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="bfac7-142">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="bfac7-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="bfac7-143">INPUTOBJECT: <IHealthBotIdentity> Parametr tożsamości</span><span class="sxs-lookup"><span data-stu-id="bfac7-143">INPUTOBJECT <IHealthBotIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="bfac7-144">`[BotName <String>]`: nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="bfac7-144">`[BotName <String>]`: The name of the Bot resource.</span></span>
  - <span data-ttu-id="bfac7-145">`[Id <String>]`: ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="bfac7-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="bfac7-146">`[ResourceGroupName <String>]`: nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="bfac7-146">`[ResourceGroupName <String>]`: The name of the Bot resource group in the user subscription.</span></span>
  - <span data-ttu-id="bfac7-147">`[SubscriptionId <String>]`: Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="bfac7-147">`[SubscriptionId <String>]`: Azure Subscription ID.</span></span>

## <span data-ttu-id="bfac7-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bfac7-148">RELATED LINKS</span></span>

