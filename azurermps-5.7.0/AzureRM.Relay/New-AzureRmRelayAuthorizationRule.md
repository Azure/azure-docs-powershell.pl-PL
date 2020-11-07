---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/new-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/New-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: daa2d1539a97b7aff7348fe8e603179c857c73db
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718479"
---
# <span data-ttu-id="63165-101">New-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="63165-101">New-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="63165-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63165-102">SYNOPSIS</span></span>
<span data-ttu-id="63165-103">Tworzy nową regułę autoryzacji dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="63165-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63165-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63165-104">SYNTAX</span></span>

### <span data-ttu-id="63165-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="63165-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="63165-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="63165-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="63165-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="63165-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63165-108">Opis</span><span class="sxs-lookup"><span data-stu-id="63165-108">DESCRIPTION</span></span>
<span data-ttu-id="63165-109">Polecenie cmdlet **New-AzureRmRelayAuthorizationRule** tworzy nową regułę autoryzacji dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="63165-109">The **New-AzureRmRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="63165-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63165-110">EXAMPLES</span></span>

### <span data-ttu-id="63165-111">Przykład 1-obszar nazw</span><span class="sxs-lookup"><span data-stu-id="63165-111">Example 1 - Namespace</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="63165-112">Tworzy `AuthoRule1` prawa **odsłuchiwania** dla obszaru nazw `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="63165-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="63165-113">Przykład 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="63165-113">Example 2 - WcfRelay</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="63165-114">Tworzy regułę autoryzacji `AuthoRule1` z prawami **odsłuchiwania** dla WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="63165-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="63165-115">Przykład 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="63165-115">Example 3 - HybridConnection</span></span>
```
PS C:\>New-AzureRmRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"
```

<span data-ttu-id="63165-116">Tworzy `AuthoRule1` prawa **odsłuchiwania** dla obszaru nazw `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="63165-116">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

## <span data-ttu-id="63165-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63165-117">PARAMETERS</span></span>

### <span data-ttu-id="63165-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="63165-118">-DefaultProfile</span></span>
<span data-ttu-id="63165-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="63165-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="63165-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="63165-120">-HybridConnection</span></span>
<span data-ttu-id="63165-121">Nazwa HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="63165-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="63165-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="63165-122">-Name</span></span>
<span data-ttu-id="63165-123">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="63165-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="63165-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="63165-124">-Namespace</span></span>
<span data-ttu-id="63165-125">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="63165-125">Namespace Name.</span></span>

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

### <span data-ttu-id="63165-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63165-126">-ResourceGroupName</span></span>
<span data-ttu-id="63165-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="63165-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="63165-128">-Prawa</span><span class="sxs-lookup"><span data-stu-id="63165-128">-Rights</span></span>
<span data-ttu-id="63165-129">Prawa, na przykład "odsłuchiwanie", "Wyślij", "Zarządzaj"</span><span class="sxs-lookup"><span data-stu-id="63165-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63165-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="63165-130">-WcfRelay</span></span>
<span data-ttu-id="63165-131">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="63165-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="63165-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="63165-132">-Confirm</span></span>
<span data-ttu-id="63165-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63165-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="63165-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63165-134">-WhatIf</span></span>
<span data-ttu-id="63165-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63165-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="63165-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="63165-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="63165-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63165-137">CommonParameters</span></span>
<span data-ttu-id="63165-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63165-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63165-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63165-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63165-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63165-140">INPUTS</span></span>

### <span data-ttu-id="63165-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63165-141">-ResourceGroupName</span></span>
 <span data-ttu-id="63165-142">System. String</span><span class="sxs-lookup"><span data-stu-id="63165-142">System.String</span></span> 

### <span data-ttu-id="63165-143">-Namespace</span><span class="sxs-lookup"><span data-stu-id="63165-143">-Namespace</span></span>
 <span data-ttu-id="63165-144">System. String</span><span class="sxs-lookup"><span data-stu-id="63165-144">System.String</span></span> 
 

### <span data-ttu-id="63165-145">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="63165-145">-WcfRelay</span></span>
 <span data-ttu-id="63165-146">System. String</span><span class="sxs-lookup"><span data-stu-id="63165-146">System.String</span></span> 

### <span data-ttu-id="63165-147">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="63165-147">-HybridConnection</span></span>
 <span data-ttu-id="63165-148">System. String</span><span class="sxs-lookup"><span data-stu-id="63165-148">System.String</span></span> 
 

### <span data-ttu-id="63165-149">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="63165-149">-Name</span></span>
 <span data-ttu-id="63165-150">System. String</span><span class="sxs-lookup"><span data-stu-id="63165-150">System.String</span></span>
 

### <span data-ttu-id="63165-151">-Prawa</span><span class="sxs-lookup"><span data-stu-id="63165-151">-Rights</span></span>
 <span data-ttu-id="63165-152">System. String []</span><span class="sxs-lookup"><span data-stu-id="63165-152">System.String []</span></span>

## <span data-ttu-id="63165-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63165-153">OUTPUTS</span></span>

### <span data-ttu-id="63165-154">Microsoft. Azure. Commands. Relay. modele. AuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="63165-154">Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes</span></span>

### <span data-ttu-id="63165-155">Przykład 1-obszar nazw</span><span class="sxs-lookup"><span data-stu-id="63165-155">Example 1 - Namespace</span></span>
<span data-ttu-id="63165-156">Prawa: {Listen} Name: AuthoRule1 typ: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="63165-156">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="63165-157">Przykład 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="63165-157">Example 2 - WcfRelay</span></span>
<span data-ttu-id="63165-158">Prawa: {Listen} Name: AuthoRule1 typ: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="63165-158">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="63165-159">Przykład 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="63165-159">Example 3 - HybridConnection</span></span>
<span data-ttu-id="63165-160">Prawa: {Listen} Name: AuthoRule1 typ: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="63165-160">Rights : {Listen} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="63165-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63165-161">NOTES</span></span>

## <span data-ttu-id="63165-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63165-162">RELATED LINKS</span></span>

