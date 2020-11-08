---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/set-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/Set-AzRelayAuthorizationRule.md
ms.openlocfilehash: 4ca8156e80a827c9916def7ef749cfa9abb9389a
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220408"
---
# <span data-ttu-id="91171-101">Set-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="91171-101">Set-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="91171-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="91171-102">SYNOPSIS</span></span>
<span data-ttu-id="91171-103">Umożliwia zaktualizowanie określonego opisu reguły autoryzacji dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="91171-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="91171-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="91171-104">SYNTAX</span></span>

### <span data-ttu-id="91171-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="91171-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91171-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="91171-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91171-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="91171-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> [[-InputObject] <PSAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="91171-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="91171-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="91171-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="91171-109">AuthoRulePropertiesSet</span></span>
```
Set-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="91171-110">Opis</span><span class="sxs-lookup"><span data-stu-id="91171-110">DESCRIPTION</span></span>
<span data-ttu-id="91171-111">Polecenie cmdlet **Set-AzRelayAuthorizationRule** aktualizuje opis określonej reguły autoryzacji dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="91171-111">The **Set-AzRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="91171-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="91171-112">EXAMPLES</span></span>

### <span data-ttu-id="91171-113">Przykład 1,1-obszar nazw z funkcją Inputobject</span><span class="sxs-lookup"><span data-stu-id="91171-113">Example 1.1 - Namespace with InputObject</span></span>
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

<span data-ttu-id="91171-114">Dodaje **nadawcę** z praw dostępu do reguły autoryzacji `AuthoRule1` w obszarze nazw `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="91171-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="91171-115">Przykład 1,2-obszar nazw z parametrem Rights</span><span class="sxs-lookup"><span data-stu-id="91171-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="91171-116">Dodaje **nadawcę** z praw dostępu do reguły autoryzacji `AuthoRule1` w obszarze nazw `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="91171-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="91171-117">Przykład 2,1-WcfRelay z funkcją Inputobject</span><span class="sxs-lookup"><span data-stu-id="91171-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="91171-118">Dodaje **do** praw dostępu reguły autoryzacji `AuthoRule1` WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="91171-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="91171-119">Przykład 2,2-WcfRelay z parametrem Rights</span><span class="sxs-lookup"><span data-stu-id="91171-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="91171-120">Dodaje **do** praw dostępu reguły autoryzacji `AuthoRule1` WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="91171-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="91171-121">Przykład 3,1-HybridConnection z funkcją Inputobject</span><span class="sxs-lookup"><span data-stu-id="91171-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="91171-122">Dodaje **do** praw dostępu reguły autoryzacji `AuthoRule1` HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="91171-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="91171-123">Przykład 3,2-HybridConnection z parametrem Rights</span><span class="sxs-lookup"><span data-stu-id="91171-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"

Rights : {Listen, Send}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="91171-124">Dodaje **do** praw dostępu reguły autoryzacji `AuthoRule1` HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="91171-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="91171-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="91171-125">PARAMETERS</span></span>

### <span data-ttu-id="91171-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="91171-126">-DefaultProfile</span></span>
<span data-ttu-id="91171-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="91171-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="91171-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="91171-128">-HybridConnection</span></span>
<span data-ttu-id="91171-129">Nazwa HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="91171-129">HybridConnection Name.</span></span>

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

### <span data-ttu-id="91171-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="91171-130">-InputObject</span></span>
<span data-ttu-id="91171-131">Obiekt przekaźnika AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="91171-131">Relay AuthorizationRule Object.</span></span>

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

### <span data-ttu-id="91171-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="91171-132">-Name</span></span>
<span data-ttu-id="91171-133">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="91171-133">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="91171-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="91171-134">-Namespace</span></span>
<span data-ttu-id="91171-135">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="91171-135">Namespace Name.</span></span>

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

### <span data-ttu-id="91171-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="91171-136">-ResourceGroupName</span></span>
<span data-ttu-id="91171-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="91171-137">Resource Group Name.</span></span>

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

### <span data-ttu-id="91171-138">-Prawa</span><span class="sxs-lookup"><span data-stu-id="91171-138">-Rights</span></span>
<span data-ttu-id="91171-139">Prawa, na przykład @ ("nasłuchuj", "Wyślij", "Zarządzaj")</span><span class="sxs-lookup"><span data-stu-id="91171-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="91171-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="91171-140">-WcfRelay</span></span>
<span data-ttu-id="91171-141">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="91171-141">WcfRelay Name.</span></span>

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

### <span data-ttu-id="91171-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="91171-142">-Confirm</span></span>
<span data-ttu-id="91171-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91171-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="91171-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="91171-144">-WhatIf</span></span>
<span data-ttu-id="91171-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="91171-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="91171-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="91171-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="91171-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="91171-147">CommonParameters</span></span>
<span data-ttu-id="91171-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="91171-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="91171-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="91171-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="91171-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="91171-150">INPUTS</span></span>

### <span data-ttu-id="91171-151">System. String</span><span class="sxs-lookup"><span data-stu-id="91171-151">System.String</span></span>

### <span data-ttu-id="91171-152">Microsoft. Azure. Commands. Relay. modele. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="91171-152">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="91171-153">System. String []</span><span class="sxs-lookup"><span data-stu-id="91171-153">System.String[]</span></span>

## <span data-ttu-id="91171-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="91171-154">OUTPUTS</span></span>

### <span data-ttu-id="91171-155">Microsoft. Azure. Commands. Relay. modele. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="91171-155">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="91171-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="91171-156">NOTES</span></span>

## <span data-ttu-id="91171-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="91171-157">RELATED LINKS</span></span>
