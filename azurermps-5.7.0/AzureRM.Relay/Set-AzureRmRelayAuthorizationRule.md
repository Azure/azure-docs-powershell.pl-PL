---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/set-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Set-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 91f37ad2ed49b4c1bd39306be803776ddce9ecff
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551647"
---
# <span data-ttu-id="6056c-101">Set-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6056c-101">Set-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="6056c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6056c-102">SYNOPSIS</span></span>
<span data-ttu-id="6056c-103">Umożliwia zaktualizowanie określonego opisu reguły autoryzacji dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="6056c-103">Updates the specified authorization rule description for the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6056c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6056c-104">SYNTAX</span></span>

### <span data-ttu-id="6056c-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6056c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6056c-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6056c-106">WcfRelayAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6056c-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="6056c-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> [[-InputObject] <AuthorizationRuleAttributes>]
 [[-Rights] <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6056c-108">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="6056c-108">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <AuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6056c-109">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="6056c-109">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Name] <String> [-Rights] <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6056c-110">Opis</span><span class="sxs-lookup"><span data-stu-id="6056c-110">DESCRIPTION</span></span>
<span data-ttu-id="6056c-111">Polecenie cmdlet **Set-AzureRmRelayAuthorizationRule** aktualizuje opis określonej reguły autoryzacji dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="6056c-111">The **Set-AzureRmRelayAuthorizationRule** cmdlet updates the description for the specified authorization rule of the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="6056c-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6056c-112">EXAMPLES</span></span>

### <span data-ttu-id="6056c-113">Przykład 1,1-obszar nazw z funkcją Inputobject</span><span class="sxs-lookup"><span data-stu-id="6056c-113">Example 1.1 - Namespace with InputObject</span></span>
```
PS C:\>
PS C:\> $getAutoRule = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -NamespaceName TestNameSpace-Relay1 -AuthorizationRuleName
 AuthoRule1
PS C:\> $getAutoRule.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -InputObject $getAutoRule
```

<span data-ttu-id="6056c-114">Dodaje **nadawcę** z praw dostępu do reguły autoryzacji `AuthoRule1` w obszarze nazw `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="6056c-114">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="6056c-115">Przykład 1,2-obszar nazw z parametrem Rights</span><span class="sxs-lookup"><span data-stu-id="6056c-115">Example 1.2 - Namespace with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -AuthorizationRule AuthoRule1 -Rights "Send"
```

<span data-ttu-id="6056c-116">Dodaje **nadawcę** z praw dostępu do reguły autoryzacji `AuthoRule1` w obszarze nazw `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="6056c-116">Adds **Send** from the access rights of the authorization rule `AuthoRule1` in namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="6056c-117">Przykład 2,1-WcfRelay z funkcją Inputobject</span><span class="sxs-lookup"><span data-stu-id="6056c-117">Example 2.1 - WcfRelay with InputObject</span></span>
```
PS C:\> $getWcfRelayAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
PS C:\> $getWcfRelayAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -InputObject $getWcfRelayAutho
```

<span data-ttu-id="6056c-118">Dodaje **do** praw dostępu reguły autoryzacji `AuthoRule1` WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="6056c-118">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="6056c-119">Przykład 2,2-WcfRelay z parametrem Rights</span><span class="sxs-lookup"><span data-stu-id="6056c-119">Example 2.2 - WcfRelay with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="6056c-120">Dodaje **do** praw dostępu reguły autoryzacji `AuthoRule1` WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="6056c-120">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="6056c-121">Przykład 3,1-HybridConnection z funkcją Inputobject</span><span class="sxs-lookup"><span data-stu-id="6056c-121">Example 3.1 - HybridConnection with InputObject</span></span>
```
PS C:\> $GetHybirdAutho = Get-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1
PS C:\> $GetHybirdAutho.Rights.Add("Send")
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -InputObject $GetHybirdAutho
```

<span data-ttu-id="6056c-122">Dodaje **do** praw dostępu reguły autoryzacji `AuthoRule1` HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="6056c-122">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

### <span data-ttu-id="6056c-123">Przykład 3,2-HybridConnection z parametrem Rights</span><span class="sxs-lookup"><span data-stu-id="6056c-123">Example 3.2 - HybridConnection with Rights parameter</span></span>
```
PS C:\> Set-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Send"
```

<span data-ttu-id="6056c-124">Dodaje **do** praw dostępu reguły autoryzacji `AuthoRule1` HybridConnection `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="6056c-124">Adds **Send** to the access rights of the authorization rule `AuthoRule1` of the HybridConnection `TestHybridConnection`.</span></span>

## <span data-ttu-id="6056c-125">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6056c-125">PARAMETERS</span></span>

### <span data-ttu-id="6056c-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6056c-126">-DefaultProfile</span></span>
<span data-ttu-id="6056c-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6056c-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6056c-128">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="6056c-128">-HybridConnection</span></span>
<span data-ttu-id="6056c-129">Nazwa HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="6056c-129">HybridConnection Name.</span></span>

```yaml
Type: String
Parameter Sets: HybridConnectionAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6056c-130">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6056c-130">-InputObject</span></span>
<span data-ttu-id="6056c-131">Obiekt przekaźnika AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="6056c-131">Relay AuthorizationRule Object</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6056c-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6056c-132">-Name</span></span>
<span data-ttu-id="6056c-133">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="6056c-133">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6056c-134">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6056c-134">-Namespace</span></span>
<span data-ttu-id="6056c-135">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="6056c-135">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6056c-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6056c-136">-ResourceGroupName</span></span>
<span data-ttu-id="6056c-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6056c-137">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6056c-138">-Prawa</span><span class="sxs-lookup"><span data-stu-id="6056c-138">-Rights</span></span>
<span data-ttu-id="6056c-139">Prawa, na przykład @ ("nasłuchuj", "Wyślij", "Zarządzaj")</span><span class="sxs-lookup"><span data-stu-id="6056c-139">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, WcfRelayAuthorizationRuleSet, HybridConnectionAuthorizationRuleSet
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6056c-140">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="6056c-140">-WcfRelay</span></span>
<span data-ttu-id="6056c-141">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="6056c-141">WcfRelay Name.</span></span>

```yaml
Type: String
Parameter Sets: WcfRelayAuthorizationRuleSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6056c-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6056c-142">-Confirm</span></span>
<span data-ttu-id="6056c-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6056c-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6056c-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6056c-144">-WhatIf</span></span>
<span data-ttu-id="6056c-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6056c-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6056c-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6056c-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6056c-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6056c-147">CommonParameters</span></span>
<span data-ttu-id="6056c-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6056c-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6056c-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6056c-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6056c-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6056c-150">INPUTS</span></span>

### <span data-ttu-id="6056c-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6056c-151">-ResourceGroupName</span></span>
 <span data-ttu-id="6056c-152">System. String</span><span class="sxs-lookup"><span data-stu-id="6056c-152">System.String</span></span> 

### <span data-ttu-id="6056c-153">-Namespace</span><span class="sxs-lookup"><span data-stu-id="6056c-153">-Namespace</span></span>
 <span data-ttu-id="6056c-154">System. String</span><span class="sxs-lookup"><span data-stu-id="6056c-154">System.String</span></span> 
 

### <span data-ttu-id="6056c-155">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="6056c-155">-WcfRelay</span></span>
 <span data-ttu-id="6056c-156">System. String</span><span class="sxs-lookup"><span data-stu-id="6056c-156">System.String</span></span> 

### <span data-ttu-id="6056c-157">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="6056c-157">-HybridConnection</span></span>
 <span data-ttu-id="6056c-158">System. String</span><span class="sxs-lookup"><span data-stu-id="6056c-158">System.String</span></span> 
 

### <span data-ttu-id="6056c-159">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6056c-159">-Name</span></span>
 <span data-ttu-id="6056c-160">System. String</span><span class="sxs-lookup"><span data-stu-id="6056c-160">System.String</span></span>

### <span data-ttu-id="6056c-161">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6056c-161">-InputObject</span></span>
 <span data-ttu-id="6056c-162">Microsoft. Azure. Commands. Relay. modele. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="6056c-162">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>
 

### <span data-ttu-id="6056c-163">-Prawa</span><span class="sxs-lookup"><span data-stu-id="6056c-163">-Rights</span></span>
 <span data-ttu-id="6056c-164">System. String []</span><span class="sxs-lookup"><span data-stu-id="6056c-164">System.String []</span></span>

## <span data-ttu-id="6056c-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6056c-165">OUTPUTS</span></span>

### <span data-ttu-id="6056c-166">Microsoft. Azure. Commands. Relay. modele. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="6056c-166">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="6056c-167">Przykład 1-obszar nazw</span><span class="sxs-lookup"><span data-stu-id="6056c-167">Example 1 - Namespace</span></span>
<span data-ttu-id="6056c-168">Prawa: {Listen, Send} Name: AuthoRule1 typ: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="6056c-168">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="6056c-169">Przykład 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="6056c-169">Example 2 - WcfRelay</span></span>
<span data-ttu-id="6056c-170">Prawa: {Listen, Send} Name: AuthoRule1 typ: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="6056c-170">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="6056c-171">Przykład 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="6056c-171">Example 3 - HybridConnection</span></span>
<span data-ttu-id="6056c-172">Prawa: {Listen, Send} Name: AuthoRule1 typ: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="6056c-172">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="6056c-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6056c-173">NOTES</span></span>

## <span data-ttu-id="6056c-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6056c-174">RELATED LINKS</span></span>

