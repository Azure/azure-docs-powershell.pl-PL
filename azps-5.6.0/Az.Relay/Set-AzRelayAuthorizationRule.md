---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/powershell/module/az.relay/set-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
ms.openlocfilehash: 3165905cc86d2255670127cd90c015ce20096c14
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102000426"
---
# <span data-ttu-id="dfd4d-101">Set-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="dfd4d-101">Set-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="dfd4d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dfd4d-102">SYNOPSIS</span></span>
<span data-ttu-id="dfd4d-103">Aktualizuje opis określonej reguły autoryzacji dla określonych obiektów przekazywania (Przestrzeń nazw/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="dfd4d-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="dfd4d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dfd4d-104">SYNTAX</span></span>

### <span data-ttu-id="dfd4d-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="dfd4d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfd4d-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="dfd4d-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfd4d-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="dfd4d-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dfd4d-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="dfd4d-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dfd4d-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="dfd4d-109">AuthoRulePropertiesSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dfd4d-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="dfd4d-110">DESCRIPTION</span></span>
<span data-ttu-id="dfd4d-111">Polecenie **cmdlet Set-AzRelayAuthorizationRule** aktualizuje opis określonej reguły autoryzacji dla określonych obiektów przekazywania (Przestrzeń nazw/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="dfd4d-111">The **Set-AzRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="dfd4d-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dfd4d-112">EXAMPLES</span></span>

### <span data-ttu-id="dfd4d-113">Przykład 1.1 . Przestrzeń nazw z inputObject</span><span class="sxs-lookup"><span data-stu-id="dfd4d-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="dfd4d-114">Dodaje **wyślij** z praw dostępu reguły autoryzacji w `AuthoRule1` przestrzeni `TestNameSpace-Relay1` nazw.</span><span class="sxs-lookup"><span data-stu-id="dfd4d-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="dfd4d-115">Przykład 1.2. Przestrzeń nazw z parametrem Rights</span><span class="sxs-lookup"><span data-stu-id="dfd4d-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="dfd4d-116">Dodaje **wyślij** z praw dostępu reguły autoryzacji w `AuthoRule1` przestrzeni `TestNameSpace-Relay1` nazw.</span><span class="sxs-lookup"><span data-stu-id="dfd4d-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="dfd4d-117">Przykład 2.1 — WcfRelay z InputObject</span><span class="sxs-lookup"><span data-stu-id="dfd4d-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="dfd4d-118">Dodaje **wyślij** do praw dostępu reguły autoryzacji `AuthoRule1` WcfRelay. `TestWCFRelay1`</span><span class="sxs-lookup"><span data-stu-id="dfd4d-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="dfd4d-119">Przykład 2.2. WcfRelay z parametrem Rights</span><span class="sxs-lookup"><span data-stu-id="dfd4d-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="dfd4d-120">Dodaje **wyślij** do praw dostępu reguły autoryzacji `AuthoRule1` WcfRelay. `TestWCFRelay1`</span><span class="sxs-lookup"><span data-stu-id="dfd4d-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="dfd4d-121">Przykład 3.1 . HybridConnection with InputObject</span><span class="sxs-lookup"><span data-stu-id="dfd4d-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="dfd4d-122">Dodaje **usługę Wyślij** do praw dostępu reguły autoryzacji `AuthoRule1` połączenia `TestHybridConnection` hybrydowego.</span><span class="sxs-lookup"><span data-stu-id="dfd4d-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="dfd4d-123">Przykład 3.2. HybridConnection z parametrem Rights</span><span class="sxs-lookup"><span data-stu-id="dfd4d-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="dfd4d-124">Dodaje **usługę Wyślij** do praw dostępu reguły autoryzacji `AuthoRule1` połączenia `TestHybridConnection` hybrydowego.</span><span class="sxs-lookup"><span data-stu-id="dfd4d-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="dfd4d-125">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dfd4d-125">PARAMETERS</span></span>

### <span data-ttu-id="dfd4d-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfd4d-126">-DefaultProfile</span></span>
<span data-ttu-id="dfd4d-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dfd4d-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd4d-128">- HybridConnection</span><span class="sxs-lookup"><span data-stu-id="dfd4d-128">-HybridConnection</span></span>
<span data-ttu-id="dfd4d-129">Nazwa połączenia hybrydowego.</span><span class="sxs-lookup"><span data-stu-id="dfd4d-129">HybridConnection Name.</span></span>

```yaml
Type: System.String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd4d-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dfd4d-130">-InputObject</span></span>
<span data-ttu-id="dfd4d-131">Obiekt Relay AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="dfd4d-131">Relay AuthorizationRule Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd4d-132">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dfd4d-132">-Name</span></span>
<span data-ttu-id="dfd4d-133">Nazwa podmiotu autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="dfd4d-133">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd4d-134">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="dfd4d-134">-Namespace</span></span>
<span data-ttu-id="dfd4d-135">Nazwa przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="dfd4d-135">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd4d-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfd4d-136">-ResourceGroupName</span></span>
<span data-ttu-id="dfd4d-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dfd4d-137">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd4d-138">— Prawa</span><span class="sxs-lookup"><span data-stu-id="dfd4d-138">-Rights</span></span>
<span data-ttu-id="dfd4d-139">Prawa, np. @("Posłuchaj","Wyślij","Zarządzaj")</span><span class="sxs-lookup"><span data-stu-id="dfd4d-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfd4d-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="dfd4d-140">-WcfRelay</span></span>
<span data-ttu-id="dfd4d-141">Nazwa aplikacji WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="dfd4d-141">WcfRelay Name.</span></span>

```yaml
Type: System.String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dfd4d-142">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dfd4d-142">-Confirm</span></span>
<span data-ttu-id="dfd4d-143">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dfd4d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfd4d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfd4d-144">-WhatIf</span></span>
<span data-ttu-id="dfd4d-145">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dfd4d-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfd4d-146">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dfd4d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfd4d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfd4d-147">CommonParameters</span></span>
<span data-ttu-id="dfd4d-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfd4d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfd4d-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfd4d-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfd4d-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dfd4d-150">INPUTS</span></span>

### <span data-ttu-id="dfd4d-151">System.String</span><span class="sxs-lookup"><span data-stu-id="dfd4d-151">System.String</span></span>

### <span data-ttu-id="dfd4d-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="dfd4d-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="dfd4d-153">System.String[]</span><span class="sxs-lookup"><span data-stu-id="dfd4d-153">System.String[]</span></span>

## <span data-ttu-id="dfd4d-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dfd4d-154">OUTPUTS</span></span>

### <span data-ttu-id="dfd4d-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="dfd4d-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="dfd4d-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dfd4d-156">NOTES</span></span>

## <span data-ttu-id="dfd4d-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dfd4d-157">RELATED LINKS</span></span>
