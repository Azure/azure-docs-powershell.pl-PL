---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/powershell/module/az.botservice/new-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
ms.openlocfilehash: 11f3124c98e84dcaec40c3b8ecd9b8831b572617
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009297"
---
# <span data-ttu-id="58423-101">New-AzBotService</span><span class="sxs-lookup"><span data-stu-id="58423-101">New-AzBotService</span></span>

## <span data-ttu-id="58423-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58423-102">SYNOPSIS</span></span>
<span data-ttu-id="58423-103">Zwraca wartość botservice określoną w parametrach.</span><span class="sxs-lookup"><span data-stu-id="58423-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="58423-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="58423-104">SYNTAX</span></span>

### <span data-ttu-id="58423-105">Rejestracja (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="58423-105">Registration (Default)</span></span>
```
New-AzBotService -ApplicationId <String> -Location <String> [-BotTemplateType <String>]
 [-Description <String>] [-DisplayName <String>] [-Endpoint <String>] [-Language <String>] [-Name <String>]
 [-Registration] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="58423-106">WebApp</span><span class="sxs-lookup"><span data-stu-id="58423-106">WebApp</span></span>
```
New-AzBotService -ApplicationId <String> -ApplicationSecret <SecureString> -Location <String>
 [-BotTemplateType <String>] [-Description <String>] [-ExistingServerFarmId <String>] [-Language <String>]
 [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Webapp] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="58423-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="58423-107">DESCRIPTION</span></span>
<span data-ttu-id="58423-108">Zwraca wartość botservice określoną w parametrach.</span><span class="sxs-lookup"><span data-stu-id="58423-108">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="58423-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="58423-109">EXAMPLES</span></span>

### <span data-ttu-id="58423-110">Przykład 1. Tworzenie nowego bota</span><span class="sxs-lookup"><span data-stu-id="58423-110">Example 1: Create a new bot</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-bot1 -ApplicationId "af5fce4d-ee68-4b25-be09-f3222582e133"-Location eastus -Sku F0 -Description "123134" -Registration

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="58423-111">Tworzenie nowego bota według nazw ResourceGroupName i ApplicationId</span><span class="sxs-lookup"><span data-stu-id="58423-111">Create a new Bot by ResourceGroupName and ApplicationId</span></span>

### <span data-ttu-id="58423-112">Przykład 2. Tworzenie nowej aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="58423-112">Example 2: Create a new Web App</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-apptest14 -ApplicationId "b1ab1727-0465-4255-a1bb-976210af972c" -Location eastus -Sku F0 -Description "123134" -Webapp

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest14 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="58423-113">Tworzenie nowej aplikacji sieci Web według nazw ResourceGroupName i ApplicationId</span><span class="sxs-lookup"><span data-stu-id="58423-113">Create a new Web App by ResourceGroupName and ApplicationId</span></span>

## <span data-ttu-id="58423-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="58423-114">PARAMETERS</span></span>

### <span data-ttu-id="58423-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="58423-115">-ApplicationId</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58423-116">-ApplicationSecret</span><span class="sxs-lookup"><span data-stu-id="58423-116">-ApplicationSecret</span></span>


```yaml
Type: System.Security.SecureString
Parameter Sets: WebApp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58423-117">-BotTemplateType</span><span class="sxs-lookup"><span data-stu-id="58423-117">-BotTemplateType</span></span>


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

### <span data-ttu-id="58423-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58423-118">-DefaultProfile</span></span>
<span data-ttu-id="58423-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="58423-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58423-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="58423-120">-Description</span></span>


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

### <span data-ttu-id="58423-121">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="58423-121">-DisplayName</span></span>


```yaml
Type: System.String
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58423-122">- Punkt końcowy</span><span class="sxs-lookup"><span data-stu-id="58423-122">-Endpoint</span></span>


```yaml
Type: System.String
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58423-123">-ExistingServerFarmId</span><span class="sxs-lookup"><span data-stu-id="58423-123">-ExistingServerFarmId</span></span>


```yaml
Type: System.String
Parameter Sets: WebApp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58423-124">— język</span><span class="sxs-lookup"><span data-stu-id="58423-124">-Language</span></span>


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

### <span data-ttu-id="58423-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="58423-125">-Location</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58423-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="58423-126">-Name</span></span>
<span data-ttu-id="58423-127">Nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="58423-127">The name of the Bot resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BotName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58423-128">— Rejestracja</span><span class="sxs-lookup"><span data-stu-id="58423-128">-Registration</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Registration
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58423-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58423-129">-ResourceGroupName</span></span>
<span data-ttu-id="58423-130">Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="58423-130">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="58423-131">- SKU</span><span class="sxs-lookup"><span data-stu-id="58423-131">-Sku</span></span>
<span data-ttu-id="58423-132">Nazwa sKU</span><span class="sxs-lookup"><span data-stu-id="58423-132">The sku name</span></span>

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

### <span data-ttu-id="58423-133">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="58423-133">-SubscriptionId</span></span>
<span data-ttu-id="58423-134">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="58423-134">Azure Subscription ID.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58423-135">— Webapp</span><span class="sxs-lookup"><span data-stu-id="58423-135">-Webapp</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WebApp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58423-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58423-136">CommonParameters</span></span>
<span data-ttu-id="58423-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="58423-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58423-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="58423-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58423-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58423-139">INPUTS</span></span>

## <span data-ttu-id="58423-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="58423-140">OUTPUTS</span></span>

### <span data-ttu-id="58423-141">Microsoft.Azure.PowerShell.cmdlet.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="58423-141">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="58423-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="58423-142">NOTES</span></span>

<span data-ttu-id="58423-143">ALIASY</span><span class="sxs-lookup"><span data-stu-id="58423-143">ALIASES</span></span>

## <span data-ttu-id="58423-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="58423-144">RELATED LINKS</span></span>

