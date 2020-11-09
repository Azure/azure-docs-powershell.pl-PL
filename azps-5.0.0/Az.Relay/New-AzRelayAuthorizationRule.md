---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Relay.dll-Help.xml
Module Name: Az.Relay
online version: https://docs.microsoft.com/en-us/powershell/module/az.relay/new-azrelayauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Relay/Relay/help/New-AzRelayAuthorizationRule.md
ms.openlocfilehash: 39bba687e355b1742210fb0c37fc8f1a65d957a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94317778"
---
# <span data-ttu-id="f70e9-101">New-AzRelayAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f70e9-101">New-AzRelayAuthorizationRule</span></span>

## <span data-ttu-id="f70e9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f70e9-102">SYNOPSIS</span></span>
<span data-ttu-id="f70e9-103">Tworzy nową regułę autoryzacji dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="f70e9-103">Creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f70e9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f70e9-104">SYNTAX</span></span>

### <span data-ttu-id="f70e9-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f70e9-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f70e9-106">WcfRelayAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f70e9-106">WcfRelayAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-WcfRelay] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f70e9-107">HybridConnectionAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="f70e9-107">HybridConnectionAuthorizationRuleSet</span></span>
```
New-AzRelayAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>] [-HybridConnection] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f70e9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f70e9-108">DESCRIPTION</span></span>
<span data-ttu-id="f70e9-109">Polecenie cmdlet **New-AzRelayAuthorizationRule** tworzy nową regułę autoryzacji dla określonych jednostek przekazujących (Namespace/WcfRelay/HybridConnection).</span><span class="sxs-lookup"><span data-stu-id="f70e9-109">The **New-AzRelayAuthorizationRule** cmdlet creates a new authorization rule for the specified Relay entities (Namespace/WcfRelay/HybridConnection).</span></span>

## <span data-ttu-id="f70e9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f70e9-110">EXAMPLES</span></span>

### <span data-ttu-id="f70e9-111">Przykład 1: przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="f70e9-111">Example 1: Namespace</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/AuthorizationRules/AuthoRule1
```

<span data-ttu-id="f70e9-112">Tworzy `AuthoRule1` prawa **odsłuchiwania** dla obszaru nazw `TestNameSpace-Relay1` .</span><span class="sxs-lookup"><span data-stu-id="f70e9-112">Creates `AuthoRule1` with **Listen** rights for the namespace `TestNameSpace-Relay1`.</span></span>

### <span data-ttu-id="f70e9-113">Przykład 2: WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f70e9-113">Example 2: WcfRelay</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -WcfRelay TestWCFRelay1 -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/WcfRelays/TestWCFRelay1/authorizationRules/AuthoRule1
```

<span data-ttu-id="f70e9-114">Tworzy regułę autoryzacji `AuthoRule1` z prawami **odsłuchiwania** dla WcfRelay `TestWCFRelay1` .</span><span class="sxs-lookup"><span data-stu-id="f70e9-114">Creates authorization rule `AuthoRule1` with **Listen** rights for the WcfRelay `TestWCFRelay1`.</span></span>

### <span data-ttu-id="f70e9-115">Przykład 3: HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f70e9-115">Example 3: HybridConnection</span></span>
```powershell
PS C:\>New-AzRelayAuthorizationRule -ResourceGroupName Default-ServiceBus-WestUS -Namespace TestNameSpace-Relay1 -HybridConnection TestHybridConnection -Name AuthoRule1 -Rights "Listen"

Rights : {Listen}
Name   : AuthoRule1
Type   : Microsoft.Relay/AuthorizationRules
Id     : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.Relay/namespaces/TestNameSpace-Relay1/HybridConnections/TestHybridConnection/authorizationRules/AuthoRule1
```

<span data-ttu-id="f70e9-116">Tworzy `AuthoRule1` prawa do **odsłuchiwania** dla połączenia hybrydowego `TestHybridConnection` .</span><span class="sxs-lookup"><span data-stu-id="f70e9-116">Creates `AuthoRule1` with **Listen** rights for the Hybrid Connection `TestHybridConnection`.</span></span>

## <span data-ttu-id="f70e9-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f70e9-117">PARAMETERS</span></span>

### <span data-ttu-id="f70e9-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f70e9-118">-DefaultProfile</span></span>
<span data-ttu-id="f70e9-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f70e9-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f70e9-120">-HybridConnection</span><span class="sxs-lookup"><span data-stu-id="f70e9-120">-HybridConnection</span></span>
<span data-ttu-id="f70e9-121">Nazwa HybridConnection.</span><span class="sxs-lookup"><span data-stu-id="f70e9-121">HybridConnection Name.</span></span>

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

### <span data-ttu-id="f70e9-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f70e9-122">-Name</span></span>
<span data-ttu-id="f70e9-123">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="f70e9-123">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="f70e9-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f70e9-124">-Namespace</span></span>
<span data-ttu-id="f70e9-125">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="f70e9-125">Namespace Name.</span></span>

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

### <span data-ttu-id="f70e9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f70e9-126">-ResourceGroupName</span></span>
<span data-ttu-id="f70e9-127">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f70e9-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="f70e9-128">-Prawa</span><span class="sxs-lookup"><span data-stu-id="f70e9-128">-Rights</span></span>
<span data-ttu-id="f70e9-129">Prawa, na przykład "odsłuchiwanie", "Wyślij", "Zarządzaj"</span><span class="sxs-lookup"><span data-stu-id="f70e9-129">Rights, e.g. "Listen","Send","Manage"</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: Listen, Send, Manage

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f70e9-130">-WcfRelay</span><span class="sxs-lookup"><span data-stu-id="f70e9-130">-WcfRelay</span></span>
<span data-ttu-id="f70e9-131">Nazwa WcfRelay.</span><span class="sxs-lookup"><span data-stu-id="f70e9-131">WcfRelay Name.</span></span>

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

### <span data-ttu-id="f70e9-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f70e9-132">-Confirm</span></span>
<span data-ttu-id="f70e9-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f70e9-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f70e9-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f70e9-134">-WhatIf</span></span>
<span data-ttu-id="f70e9-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f70e9-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f70e9-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f70e9-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f70e9-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f70e9-137">CommonParameters</span></span>
<span data-ttu-id="f70e9-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f70e9-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f70e9-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f70e9-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f70e9-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f70e9-140">INPUTS</span></span>

### <span data-ttu-id="f70e9-141">System. String</span><span class="sxs-lookup"><span data-stu-id="f70e9-141">System.String</span></span>

### <span data-ttu-id="f70e9-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="f70e9-142">System.String[]</span></span>

## <span data-ttu-id="f70e9-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f70e9-143">OUTPUTS</span></span>

### <span data-ttu-id="f70e9-144">Microsoft. Azure. Commands. Relay. modele. PSAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="f70e9-144">Microsoft.Azure.Commands.Relay.Models.PSAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="f70e9-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f70e9-145">NOTES</span></span>

## <span data-ttu-id="f70e9-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f70e9-146">RELATED LINKS</span></span>
