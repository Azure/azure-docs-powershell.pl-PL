---
external help file: Microsoft.Azure.Commands.Relay.dll-Help.xml
Module Name: AzureRM
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.relay/get-azurermrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Relay/Commands.Relay/help/Get-AzureRmRelayAuthorizationRule.md
ms.openlocfilehash: 333e3eeaaf7655c78d557eb104fa4a349a0c05e7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526622"
---
# <span data-ttu-id="8c6c2-101">Get-AzureRmRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="8c6c2-101">Get-AzureRmRelayAuthorizationRule</span></span>

## <span data-ttu-id="8c6c2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8c6c2-102">SYNOPSIS</span></span>
<span data-ttu-id="8c6c2-103">Pobiera opis określonej reguły autoryzacji dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="8c6c2-103">Gets the description of a specified authorization rule for a given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8c6c2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8c6c2-104">SYNTAX</span></span>

### <span data-ttu-id="8c6c2-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8c6c2-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c6c2-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8c6c2-106">WcfRelayAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8c6c2-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="8c6c2-107">HybridConnectionAuthorizationRuleSet</span></span>
```
Get-AzureRmRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-HybridConnection] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8c6c2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8c6c2-108">DESCRIPTION</span></span>
<span data-ttu-id="8c6c2-109">Polecenie cmdlet **Get-AzureRmRelayAuthorizationRule** Pobiera opis określonej reguły autoryzacji w określonych jednostkach przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="8c6c2-109">The **Get-AzureRmRelayAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="8c6c2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8c6c2-110">EXAMPLES</span></span>

### <span data-ttu-id="8c6c2-111">Przykład 1-obszar nazw</span><span class="sxs-lookup"><span data-stu-id="8c6c2-111">Example 1 - Namespace</span></span>
```
PS C:\> Get-AzureRmRelayNamespaceAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1
```

<span data-ttu-id="8c6c2-112">Zwraca opis określonej reguły autoryzacji dla określonego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="8c6c2-113">Przykład 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="8c6c2-113">Example 2 - WcfRelay</span></span>
```
PS C:\>Get-AzureRmWcfRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1
```

<span data-ttu-id="8c6c2-114">Zwraca określony opis reguły autoryzacji dla danego WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-114">Returns the specified authorization rule description for a given WcfRelay.</span></span>

### <span data-ttu-id="8c6c2-115">Przykład 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="8c6c2-115">Example 3 - HybridConnection</span></span>
```
PS C:\> Get-AzureRmRelayHybridConnectionAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnections TestHybridConnection -Name AuthoRule1
```

<span data-ttu-id="8c6c2-116">Zwraca określony opis reguły autoryzacji dla danego HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-116">Returns the specified authorization rule description for a given HybridConnection.</span></span>

## <span data-ttu-id="8c6c2-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8c6c2-117">PARAMETERS</span></span>

### <span data-ttu-id="8c6c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c6c2-118">-DefaultProfile</span></span>
<span data-ttu-id="8c6c2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8c6c2-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="8c6c2-120">-HybridConnection</span></span>
<span data-ttu-id="8c6c2-121">Nazwa HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="8c6c2-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8c6c2-122">-Name</span></span>
<span data-ttu-id="8c6c2-123">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-123">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8c6c2-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="8c6c2-124">-Namespace</span></span>
<span data-ttu-id="8c6c2-125">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-125">Namespace Name.</span></span>

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

### <span data-ttu-id="8c6c2-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c6c2-126">-ResourceGroupName</span></span>
<span data-ttu-id="8c6c2-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="8c6c2-128">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="8c6c2-128">-WcfRelay</span></span>
<span data-ttu-id="8c6c2-129">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-129">WcfRelay Name.</span></span>

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

### <span data-ttu-id="8c6c2-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c6c2-130">CommonParameters</span></span>
<span data-ttu-id="8c6c2-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c6c2-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c6c2-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8c6c2-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c6c2-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c6c2-133">INPUTS</span></span>

### <span data-ttu-id="8c6c2-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8c6c2-134">-ResourceGroupName</span></span>
 <span data-ttu-id="8c6c2-135">System. String</span><span class="sxs-lookup"><span data-stu-id="8c6c2-135">System.String</span></span> 

### <span data-ttu-id="8c6c2-136">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="8c6c2-136">-NamespaceName</span></span>
 <span data-ttu-id="8c6c2-137">System. String</span><span class="sxs-lookup"><span data-stu-id="8c6c2-137">System.String</span></span> 
 

### <span data-ttu-id="8c6c2-138">-HybridConnectionsName</span><span class="sxs-lookup"><span data-stu-id="8c6c2-138">-HybridConnectionsName</span></span>
 <span data-ttu-id="8c6c2-139">System. String</span><span class="sxs-lookup"><span data-stu-id="8c6c2-139">System.String</span></span> 

### <span data-ttu-id="8c6c2-140">-WcfRelayName</span><span class="sxs-lookup"><span data-stu-id="8c6c2-140">-WcfRelayName</span></span>
 <span data-ttu-id="8c6c2-141">System. String</span><span class="sxs-lookup"><span data-stu-id="8c6c2-141">System.String</span></span> 

### <span data-ttu-id="8c6c2-142">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8c6c2-142">-Name</span></span>
 <span data-ttu-id="8c6c2-143">System. String</span><span class="sxs-lookup"><span data-stu-id="8c6c2-143">System.String</span></span>

## <span data-ttu-id="8c6c2-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8c6c2-144">OUTPUTS</span></span>

### <span data-ttu-id="8c6c2-145">System. Collections. Generic. list ' 1 [[Microsoft. Azure. Commands. Relay. modele. AuthorizationRuleAttributes, Microsoft. Azure. Commands</span><span class="sxs-lookup"><span data-stu-id="8c6c2-145">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Relay.Models.AuthorizationRuleAttributes, Microsoft.Azure.Commands.Relay, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="8c6c2-146">Przykład 1-obszar nazw</span><span class="sxs-lookup"><span data-stu-id="8c6c2-146">Example 1 - Namespace</span></span>
<span data-ttu-id="8c6c2-147">Prawa: {Nasłuchuj, Wyślij} Nazwa: AuthoRule1 typ: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut hoRule1</span><span class="sxs-lookup"><span data-stu-id="8c6c2-147">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/Aut hoRule1</span></span>

### <span data-ttu-id="8c6c2-148">Przykład 2-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="8c6c2-148">Example 2 - WcfRelay</span></span>
<span data-ttu-id="8c6c2-149">Prawa: {Nasłuchuj, Wyślij} Nazwa: AuthoRule1 typ: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay 1/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="8c6c2-149">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay 1/authorizationRules/AuthoRule1</span></span>

### <span data-ttu-id="8c6c2-150">Przykład 3-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="8c6c2-150">Example 3 - HybridConnection</span></span>
<span data-ttu-id="8c6c2-151">Prawa: {Nasłuchuj, Wyślij} Nazwa: AuthoRule1 typ: Microsoft. Relay/AuthorizationRules ID:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test HybridConnection/authorizationRules/AuthoRule1</span><span class="sxs-lookup"><span data-stu-id="8c6c2-151">Rights : {Listen, Send} Name   : AuthoRule1 Type   : Microsoft.Relay/AuthorizationRules Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/Test HybridConnection/authorizationRules/AuthoRule1</span></span>

## <span data-ttu-id="8c6c2-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8c6c2-152">NOTES</span></span>

## <span data-ttu-id="8c6c2-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c6c2-153">RELATED LINKS</span></span>

