---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 6940e12f813cbc4292f02ab98f0b35774da67025
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94233169"
---
# <span data-ttu-id="4f061-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4f061-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="4f061-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4f061-102">SYNOPSIS</span></span>
<span data-ttu-id="4f061-103">Pobiera szczegóły reguły autoryzacji lub pobiera listę reguł autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="4f061-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="4f061-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4f061-104">SYNTAX</span></span>

### <span data-ttu-id="4f061-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4f061-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f061-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4f061-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f061-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="4f061-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f061-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4f061-108">DESCRIPTION</span></span>
<span data-ttu-id="4f061-109">Polecenie cmdlet Get-AzEventHubAuthorizationRule pobiera szczegóły reguły autoryzacji lub listę wszystkich reguł autoryzacji określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="4f061-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="4f061-110">Jeśli jest podana nazwa reguły autoryzacji, zostaną zwrócone szczegóły dotyczące jednej reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="4f061-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="4f061-111">Jeśli nie podano nazwy reguły autoryzacji, zostanie zwrócona lista wszystkich reguł autoryzacji określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="4f061-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="4f061-112">Jeśli zostanie podana nazwa aliasu (odzyskiwanie po awarii), zostanie zwrócona wartość szczegółów reguły autoryzacji obszaru nazw skonfigurowanego dla aliasu.</span><span class="sxs-lookup"><span data-stu-id="4f061-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="4f061-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4f061-113">EXAMPLES</span></span>

### <span data-ttu-id="4f061-114">Przykład 1: AuthorizationRule dla obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="4f061-114">Example 1: AuthorizationRule for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="4f061-115">Pobiera regułę autoryzacji \` MyAuthRuleName \` w obszarze nazw obszar_nazwname \` \` .</span><span class="sxs-lookup"><span data-stu-id="4f061-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="4f061-116">Przykład 2: AuthorizationRules dla obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="4f061-116">Example 2: AuthorizationRules for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="4f061-117">Pobiera listę wszystkich reguł autoryzacji w obszarze nazw obszar_nazw \` \` .</span><span class="sxs-lookup"><span data-stu-id="4f061-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="4f061-118">Przykład 3: AuthorizationRule dla EventHub</span><span class="sxs-lookup"><span data-stu-id="4f061-118">Example 3: AuthorizationRule for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="4f061-119">Pobiera regułę autoryzacji \` MyAuthRuleName \` w MyEventHubName centrum zdarzeń \` \` , która jest zakresem obszaru nazw \` \` obszar_nazwname.</span><span class="sxs-lookup"><span data-stu-id="4f061-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="4f061-120">Przykład 4: AuthorizationRules dla EventHub</span><span class="sxs-lookup"><span data-stu-id="4f061-120">Example 4: AuthorizationRules for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="4f061-121">Pobiera reguły autoryzacji listy w MyEventHubName centrum zdarzeń \` \` , która jest zakresem obszaru nazw obszar_nazwname \` \` .</span><span class="sxs-lookup"><span data-stu-id="4f061-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="4f061-122">Przykład 5: AuthorizationRule dla aliasu (Konfiguracja geoawaryjna)</span><span class="sxs-lookup"><span data-stu-id="4f061-122">Example 5: AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="4f061-123">Pobiera regułę autoryzacji \` MyAuthRuleName \` w obszarze nazw obszar_nazwname \` \` .</span><span class="sxs-lookup"><span data-stu-id="4f061-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="4f061-124">Przykład 6: AuthorizationRules dla aliasu (Konfiguracja geoawaryjna)</span><span class="sxs-lookup"><span data-stu-id="4f061-124">Example 6: AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="4f061-125">Pobiera listę wszystkich reguł autoryzacji \` MyAuthRuleName \` w obszarze nazw obszar_nazwname \` \` .</span><span class="sxs-lookup"><span data-stu-id="4f061-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="4f061-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4f061-126">PARAMETERS</span></span>

### <span data-ttu-id="4f061-127">-Aliasname</span><span class="sxs-lookup"><span data-stu-id="4f061-127">-AliasName</span></span>
<span data-ttu-id="4f061-128">Nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="4f061-128">Alias Name</span></span>

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

### <span data-ttu-id="4f061-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f061-129">-DefaultProfile</span></span>
<span data-ttu-id="4f061-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4f061-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f061-131">— Eventhub</span><span class="sxs-lookup"><span data-stu-id="4f061-131">-Eventhub</span></span>
<span data-ttu-id="4f061-132">Nazwa Eventhub</span><span class="sxs-lookup"><span data-stu-id="4f061-132">Eventhub Name</span></span>

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

### <span data-ttu-id="4f061-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4f061-133">-Name</span></span>
<span data-ttu-id="4f061-134">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4f061-134">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="4f061-135">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4f061-135">-Namespace</span></span>
<span data-ttu-id="4f061-136">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="4f061-136">Namespace Name</span></span>

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

### <span data-ttu-id="4f061-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f061-137">-ResourceGroupName</span></span>
<span data-ttu-id="4f061-138">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4f061-138">Resource Group Name</span></span>

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

### <span data-ttu-id="4f061-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f061-139">CommonParameters</span></span>
<span data-ttu-id="4f061-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4f061-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f061-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f061-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f061-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4f061-142">INPUTS</span></span>

### <span data-ttu-id="4f061-143">System. String</span><span class="sxs-lookup"><span data-stu-id="4f061-143">System.String</span></span>

## <span data-ttu-id="4f061-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4f061-144">OUTPUTS</span></span>

### <span data-ttu-id="4f061-145">Microsoft. Azure. Commands. EventHub. modele. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="4f061-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="4f061-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4f061-146">NOTES</span></span>

## <span data-ttu-id="4f061-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4f061-147">RELATED LINKS</span></span>
