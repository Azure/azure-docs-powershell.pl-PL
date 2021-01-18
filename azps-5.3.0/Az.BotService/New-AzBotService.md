---
external help file: ''
Module Name: Az.BotService
online version: https://docs.microsoft.com/en-us/powershell/module/az.botservice/new-azbotservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/BotService/help/New-AzBotService.md
ms.openlocfilehash: 4e40665e4fdb7332865342132982d6d598bd8d30
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502036"
---
# <span data-ttu-id="2a8a3-101">New-AzBotService</span><span class="sxs-lookup"><span data-stu-id="2a8a3-101">New-AzBotService</span></span>

## <span data-ttu-id="2a8a3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2a8a3-102">SYNOPSIS</span></span>
<span data-ttu-id="2a8a3-103">Zwraca wartość typu BotService określona przez parametry.</span><span class="sxs-lookup"><span data-stu-id="2a8a3-103">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="2a8a3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2a8a3-104">SYNTAX</span></span>

### <span data-ttu-id="2a8a3-105">Rejestracja (domyślna)</span><span class="sxs-lookup"><span data-stu-id="2a8a3-105">Registration (Default)</span></span>
```
New-AzBotService -ApplicationId <String> -Location <String> [-BotTemplateType <String>]
 [-Description <String>] [-DisplayName <String>] [-Endpoint <String>] [-Language <String>] [-Name <String>]
 [-Registration] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2a8a3-106">Aplikacji</span><span class="sxs-lookup"><span data-stu-id="2a8a3-106">WebApp</span></span>
```
New-AzBotService -ApplicationId <String> -ApplicationSecret <SecureString> -Location <String>
 [-BotTemplateType <String>] [-Description <String>] [-ExistingServerFarmId <String>] [-Language <String>]
 [-Name <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Webapp] [-Sku <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2a8a3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2a8a3-107">DESCRIPTION</span></span>
<span data-ttu-id="2a8a3-108">Zwraca wartość typu BotService określona przez parametry.</span><span class="sxs-lookup"><span data-stu-id="2a8a3-108">Returns a BotService specified by the parameters.</span></span>

## <span data-ttu-id="2a8a3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2a8a3-109">EXAMPLES</span></span>

### <span data-ttu-id="2a8a3-110">Przykład 1. Utwórz nowy bota</span><span class="sxs-lookup"><span data-stu-id="2a8a3-110">Example 1: Create a new bot</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-bot1 -ApplicationId "af5fce4d-ee68-4b25-be09-f3222582e133"-Location eastus -Sku F0 -Description "123134" -Registration

Etag                                   Kind Location Name       SkuName SkuTier Type
----                                   ---- -------- ----       ------- ------- ----
"060085fb-0000-1800-0000-5fd71d7c0000" bot  global   youri-bot1 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="2a8a3-111">Tworzenie nowego bota przez ResourceGroupName i identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="2a8a3-111">Create a new Bot by ResourceGroupName and ApplicationId</span></span>

### <span data-ttu-id="2a8a3-112">Przykład 2: Tworzenie nowej aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="2a8a3-112">Example 2: Create a new Web App</span></span>
```powershell
PS C:\> New-AzBotService -resourcegroupname youriBotTest -name youri-apptest14 -ApplicationId "b1ab1727-0465-4255-a1bb-976210af972c" -Location eastus -Sku F0 -Description "123134" -Webapp

Etag                                   Kind Location Name            SkuName SkuTier Type
----                                   ---- -------- ----            ------- ------- ----
"06008351-0000-0200-0000-5fd732870000" sdk  global   youri-apptest14 F0              Microsoft.BotService/botServices
```

<span data-ttu-id="2a8a3-113">Tworzenie nowej aplikacji sieci Web według ResourceGroupName i aplikacji</span><span class="sxs-lookup"><span data-stu-id="2a8a3-113">Create a new Web App by ResourceGroupName and ApplicationId</span></span>

## <span data-ttu-id="2a8a3-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2a8a3-114">PARAMETERS</span></span>

### <span data-ttu-id="2a8a3-115">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="2a8a3-115">-ApplicationId</span></span>


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

### <span data-ttu-id="2a8a3-116">-ApplicationSecret</span><span class="sxs-lookup"><span data-stu-id="2a8a3-116">-ApplicationSecret</span></span>


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

### <span data-ttu-id="2a8a3-117">-BotTemplateType</span><span class="sxs-lookup"><span data-stu-id="2a8a3-117">-BotTemplateType</span></span>


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

### <span data-ttu-id="2a8a3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a8a3-118">-DefaultProfile</span></span>
<span data-ttu-id="2a8a3-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2a8a3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a8a3-120">— Opis</span><span class="sxs-lookup"><span data-stu-id="2a8a3-120">-Description</span></span>


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

### <span data-ttu-id="2a8a3-121">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2a8a3-121">-DisplayName</span></span>


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

### <span data-ttu-id="2a8a3-122">-Endpoint</span><span class="sxs-lookup"><span data-stu-id="2a8a3-122">-Endpoint</span></span>


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

### <span data-ttu-id="2a8a3-123">-ExistingServerFarmId</span><span class="sxs-lookup"><span data-stu-id="2a8a3-123">-ExistingServerFarmId</span></span>


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

### <span data-ttu-id="2a8a3-124">-Language</span><span class="sxs-lookup"><span data-stu-id="2a8a3-124">-Language</span></span>


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

### <span data-ttu-id="2a8a3-125">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2a8a3-125">-Location</span></span>


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

### <span data-ttu-id="2a8a3-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2a8a3-126">-Name</span></span>
<span data-ttu-id="2a8a3-127">Nazwa zasobu bota.</span><span class="sxs-lookup"><span data-stu-id="2a8a3-127">The name of the Bot resource.</span></span>

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

### <span data-ttu-id="2a8a3-128">— Rejestracja</span><span class="sxs-lookup"><span data-stu-id="2a8a3-128">-Registration</span></span>


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

### <span data-ttu-id="2a8a3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a8a3-129">-ResourceGroupName</span></span>
<span data-ttu-id="2a8a3-130">Nazwa grupy zasobów bota w subskrypcji użytkownika.</span><span class="sxs-lookup"><span data-stu-id="2a8a3-130">The name of the Bot resource group in the user subscription.</span></span>

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

### <span data-ttu-id="2a8a3-131">-SKU</span><span class="sxs-lookup"><span data-stu-id="2a8a3-131">-Sku</span></span>
<span data-ttu-id="2a8a3-132">Nazwa jednostki SKU</span><span class="sxs-lookup"><span data-stu-id="2a8a3-132">The sku name</span></span>

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

### <span data-ttu-id="2a8a3-133">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2a8a3-133">-SubscriptionId</span></span>
<span data-ttu-id="2a8a3-134">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2a8a3-134">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="2a8a3-135">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="2a8a3-135">-Webapp</span></span>


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

### <span data-ttu-id="2a8a3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a8a3-136">CommonParameters</span></span>
<span data-ttu-id="2a8a3-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a8a3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a8a3-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2a8a3-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a8a3-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2a8a3-139">INPUTS</span></span>

## <span data-ttu-id="2a8a3-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2a8a3-140">OUTPUTS</span></span>

### <span data-ttu-id="2a8a3-141">Microsoft. Azure. PowerShell. polecenia. BotService. models. Api20180712. IBot</span><span class="sxs-lookup"><span data-stu-id="2a8a3-141">Microsoft.Azure.PowerShell.Cmdlets.BotService.Models.Api20180712.IBot</span></span>

## <span data-ttu-id="2a8a3-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2a8a3-142">NOTES</span></span>

<span data-ttu-id="2a8a3-143">PISUJE</span><span class="sxs-lookup"><span data-stu-id="2a8a3-143">ALIASES</span></span>

## <span data-ttu-id="2a8a3-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2a8a3-144">RELATED LINKS</span></span>

