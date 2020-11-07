---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 66e32c19001586972cb408e61397545fb1c25d44
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705464"
---
# <span data-ttu-id="03445-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="03445-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="03445-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="03445-102">SYNOPSIS</span></span>
<span data-ttu-id="03445-103">Pobiera szczegóły reguły autoryzacji lub pobiera listę reguł autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="03445-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="03445-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="03445-104">SYNTAX</span></span>

### <span data-ttu-id="03445-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="03445-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03445-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="03445-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="03445-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="03445-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="03445-108">Opis</span><span class="sxs-lookup"><span data-stu-id="03445-108">DESCRIPTION</span></span>
<span data-ttu-id="03445-109">Polecenie cmdlet Get-AzEventHubAuthorizationRule pobiera szczegóły reguły autoryzacji lub listę wszystkich reguł autoryzacji określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="03445-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="03445-110">Jeśli jest podana nazwa reguły autoryzacji, zostaną zwrócone szczegóły dotyczące jednej reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="03445-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="03445-111">Jeśli nie podano nazwy reguły autoryzacji, zostanie zwrócona lista wszystkich reguł autoryzacji określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="03445-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="03445-112">Jeśli zostanie podana nazwa aliasu (odzyskiwanie po awarii), zostanie zwrócona wartość szczegółów reguły autoryzacji obszaru nazw skonfigurowanego dla aliasu.</span><span class="sxs-lookup"><span data-stu-id="03445-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="03445-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="03445-113">EXAMPLES</span></span>

### <span data-ttu-id="03445-114">Przykład 1,0-AuthorizationRule dla obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="03445-114">Example 1.0 - AuthorizationRule for namespace</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="03445-115">Pobiera regułę autoryzacji \` MyAuthRuleName \` w obszarze nazw obszar_nazwname \` \` .</span><span class="sxs-lookup"><span data-stu-id="03445-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="03445-116">Przykład 1,1-AuthorizationRules dla obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="03445-116">Example 1.1 - AuthorizationRules for namespace</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="03445-117">Pobiera listę wszystkich reguł autoryzacji w obszarze nazw obszar_nazw \` \` .</span><span class="sxs-lookup"><span data-stu-id="03445-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="03445-118">Przykład 2,0-AuthorizationRule dla EventHub</span><span class="sxs-lookup"><span data-stu-id="03445-118">Example 2.0 - AuthorizationRule for EventHub</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="03445-119">Pobiera regułę autoryzacji \` MyAuthRuleName \` w MyEventHubName centrum zdarzeń \` \` , która jest zakresem obszaru nazw \` \` obszar_nazwname.</span><span class="sxs-lookup"><span data-stu-id="03445-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="03445-120">Przykład 2,1-AuthorizationRules dla EventHub</span><span class="sxs-lookup"><span data-stu-id="03445-120">Example 2.1 - AuthorizationRules for EventHub</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="03445-121">Pobiera reguły autoryzacji listy w MyEventHubName centrum zdarzeń \` \` , która jest zakresem obszaru nazw obszar_nazwname \` \` .</span><span class="sxs-lookup"><span data-stu-id="03445-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="03445-122">Przykład 3,0-AuthorizationRule dla aliasu (Konfiguracja geoawaryjna)</span><span class="sxs-lookup"><span data-stu-id="03445-122">Example 3.0 - AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="03445-123">Pobiera regułę autoryzacji \` MyAuthRuleName \` w obszarze nazw obszar_nazwname \` \` .</span><span class="sxs-lookup"><span data-stu-id="03445-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="03445-124">Przykład 3,1-AuthorizationRules dla aliasu (Konfiguracja geoawaryjna)</span><span class="sxs-lookup"><span data-stu-id="03445-124">Example 3.1 -AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="03445-125">Pobiera listę wszystkich reguł autoryzacji \` MyAuthRuleName \` w obszarze nazw obszar_nazwname \` \` .</span><span class="sxs-lookup"><span data-stu-id="03445-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="03445-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="03445-126">PARAMETERS</span></span>

### <span data-ttu-id="03445-127">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="03445-127">-AliasName</span></span>
<span data-ttu-id="03445-128">Nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="03445-128">Alias Name</span></span>

```yaml
Type: System.String
Parameter Sets: AliasAuthoRuleSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03445-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="03445-129">-DefaultProfile</span></span>
<span data-ttu-id="03445-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="03445-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="03445-131">— Eventhub</span><span class="sxs-lookup"><span data-stu-id="03445-131">-Eventhub</span></span>
<span data-ttu-id="03445-132">Nazwa Eventhub</span><span class="sxs-lookup"><span data-stu-id="03445-132">Eventhub Name</span></span>

```yaml
Type: System.String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03445-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="03445-133">-Name</span></span>
<span data-ttu-id="03445-134">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="03445-134">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03445-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="03445-135">-Namespace</span></span>
<span data-ttu-id="03445-136">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="03445-136">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="03445-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="03445-137">-ResourceGroupName</span></span>
<span data-ttu-id="03445-138">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="03445-138">Resource Group Name</span></span>

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

### <span data-ttu-id="03445-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="03445-139">CommonParameters</span></span>
<span data-ttu-id="03445-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="03445-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="03445-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="03445-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="03445-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="03445-142">INPUTS</span></span>

### <span data-ttu-id="03445-143">System. String</span><span class="sxs-lookup"><span data-stu-id="03445-143">System.String</span></span>

## <span data-ttu-id="03445-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="03445-144">OUTPUTS</span></span>

### <span data-ttu-id="03445-145">Microsoft. Azure. Commands. EventHub. modele. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="03445-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="03445-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="03445-146">NOTES</span></span>

## <span data-ttu-id="03445-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="03445-147">RELATED LINKS</span></span>
