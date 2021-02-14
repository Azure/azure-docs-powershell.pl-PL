---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/new-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
ms.openlocfilehash: 4e40665e4fdb7332865342132982d6d598bd8d30
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181899"
---
# <span data-ttu-id="cd8cb-101">New-AzBotService</span><span class="sxs-lookup"><span data-stu-id="cd8cb-101">New-AzBotService</span></span>

## <span data-ttu-id="cd8cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd8cb-102">SYNOPSIS</span></span>
<span data-ttu-id="cd8cb-103">Zwraca wartość botservice określoną w parametrach.</span><span class="sxs-lookup"><span data-stu-id="cd8cb-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="cd8cb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cd8cb-104">SYNTAX</span></span>

### <span data-ttu-id="cd8cb-105">Rejestracja (domyślne)</span><span class="sxs-lookup"><span data-stu-id="cd8cb-105">Registration (Default)</span></span>
```
New-AzBotService -ApplicationId <String> -Location <String> [-BotTemplateType <String>]
 [-Description <String>] [-DisplayName <String>] [-Endpoint <String>] [-Language <String>] [-Name <String>]
 [-Registration] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="cd8cb-106">WebApp</span><span class="sxs-lookup"><span data-stu-id="cd8cb-106">WebApp</span></span>
```
New-AzBotService -ApplicationId <String> -ApplicationSecret <SecureString> -Location <String>
 [-BotTemplateType <String>] [-Description <String>] [-ExistingServerFarmId <String>] [-Language <String>]
 [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Webapp] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="cd8cb-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="cd8cb-107">DESCRIPTION</span></span>
<span data-ttu-id="cd8cb-108">Zwraca wartość botservice określoną w parametrach.</span><span class="sxs-lookup"><span data-stu-id="cd8cb-108">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="cd8cb-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cd8cb-109">EXAMPLES</span></span>

### <span data-ttu-id="cd8cb-110">Przykład 1. Tworzenie nowego bota</span><span class="sxs-lookup"><span data-stu-id="cd8cb-110">Example 1: Create a new bot</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-bot1 -ApplicationId "af5fce4d-ee68-4b25-be09-f3222582e133"-Location eastus -Sku F0 -Description "123134" -Registration

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="cd8cb-111">Tworzenie nowego bota według nazw ResourceGroupName i ApplicationId</span><span class="sxs-lookup"><span data-stu-id="cd8cb-111">Create a new Bot by ResourceGroupName and ApplicationId</span></span>

### <span data-ttu-id="cd8cb-112">Przykład 2. Tworzenie nowej aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="cd8cb-112">Example 2: Create a new Web App</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-apptest14 -ApplicationId "b1ab1727-0465-4255-a1bb-976210af972c" -Location eastus -Sku F0 -Description "123134" -Webapp

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest14 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="cd8cb-113">Tworzenie nowej aplikacji sieci Web według nazw ResourceGroupName i ApplicationId</span><span class="sxs-lookup"><span data-stu-id="cd8cb-113">Create a new Web App by ResourceGroupName and ApplicationId</span></span>

## <span data-ttu-id="cd8cb-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cd8cb-114">PARAMETERS</span></span>

### <span data-ttu-id="cd8cb-115">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="cd8cb-115">-ApplicationId</span></span>


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

### <span data-ttu-id="cd8cb-116">-ApplicationSecret</span><span class="sxs-lookup"><span data-stu-id="cd8cb-116">-ApplicationSecret</span></span>


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

### <span data-ttu-id="cd8cb-117">-BotTemplateType</span><span class="sxs-lookup"><span data-stu-id="cd8cb-117">-BotTemplateType</span></span>


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

### <span data-ttu-id="cd8cb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd8cb-118">-DefaultProfile</span></span>
<span data-ttu-id="cd8cb-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd8cb-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cd8cb-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="cd8cb-120">-Description</span></span>


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

### <span data-ttu-id="cd8cb-121">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="cd8cb-121">-DisplayName</span></span>


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

### <span data-ttu-id="cd8cb-122">- Punkt końcowy</span><span class="sxs-lookup"><span data-stu-id="cd8cb-122">-Endpoint</span></span>


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

### <span data-ttu-id="cd8cb-123">-ExistingServerFarmId</span><span class="sxs-lookup"><span data-stu-id="cd8cb-123">-ExistingServerFarmId</span></span>


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

### <span data-ttu-id="cd8cb-124">— język</span><span class="sxs-lookup"><span data-stu-id="cd8cb-124">-Language</span></span>


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

### <span data-ttu-id="cd8cb-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cd8cb-125">-Location</span></span>


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

### <span data-ttu-id="cd8cb-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cd8cb-126">-Name</span></span>
<span data-ttu-id="cd8cb-127">Nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="cd8cb-127">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="cd8cb-128">— Rejestracja</span><span class="sxs-lookup"><span data-stu-id="cd8cb-128">-Registration</span></span>


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

### <span data-ttu-id="cd8cb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd8cb-129">-ResourceGroupName</span></span>
<span data-ttu-id="cd8cb-130">Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="cd8cb-130">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="cd8cb-131">- SKU</span><span class="sxs-lookup"><span data-stu-id="cd8cb-131">-Sku</span></span>
<span data-ttu-id="cd8cb-132">Nazwa sKU</span><span class="sxs-lookup"><span data-stu-id="cd8cb-132">The sku name</span></span>

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

### <span data-ttu-id="cd8cb-133">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="cd8cb-133">-SubscriptionId</span></span>
<span data-ttu-id="cd8cb-134">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="cd8cb-134">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="cd8cb-135">— Webapp</span><span class="sxs-lookup"><span data-stu-id="cd8cb-135">-Webapp</span></span>


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

### <span data-ttu-id="cd8cb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd8cb-136">CommonParameters</span></span>
<span data-ttu-id="cd8cb-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd8cb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd8cb-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cd8cb-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd8cb-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd8cb-139">INPUTS</span></span>

## <span data-ttu-id="cd8cb-140">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd8cb-140">OUTPUTS</span></span>

### <span data-ttu-id="cd8cb-141">Microsoft.Azure.PowerShell.cmdlet.BotService.Models.Api20180712.IBot</span><span class="sxs-lookup"><span data-stu-id="cd8cb-141">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="cd8cb-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cd8cb-142">NOTES</span></span>

<span data-ttu-id="cd8cb-143">ALIASY</span><span class="sxs-lookup"><span data-stu-id="cd8cb-143">ALIASES</span></span>

## <span data-ttu-id="cd8cb-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd8cb-144">RELATED LINKS</span></span>

