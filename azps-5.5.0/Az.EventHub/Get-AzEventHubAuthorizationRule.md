---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 6940e12f813cbc4292f02ab98f0b35774da67025
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237909"
---
# <span data-ttu-id="bb3e8-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bb3e8-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="bb3e8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bb3e8-102">SYNOPSIS</span></span>
<span data-ttu-id="bb3e8-103">Pobiera szczegóły reguły autoryzacji lub pobiera listę reguł autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="bb3e8-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="bb3e8-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bb3e8-104">SYNTAX</span></span>

### <span data-ttu-id="bb3e8-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="bb3e8-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb3e8-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="bb3e8-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bb3e8-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="bb3e8-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bb3e8-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="bb3e8-108">DESCRIPTION</span></span>
<span data-ttu-id="bb3e8-109">Polecenie Get-AzEventHubAuthorizationRule pobiera szczegóły reguły autoryzacji lub listę wszystkich reguł autoryzacji dla określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="bb3e8-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="bb3e8-110">Jeśli podano nazwę reguły autoryzacji, zostaną zwrócone szczegóły tej reguły pojedynczej autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="bb3e8-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="bb3e8-111">Jeśli nazwa reguły autoryzacji nie jest podana, jest zwracana lista wszystkich reguł autoryzacji dla określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="bb3e8-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="bb3e8-112">Jeśli podano nazwę aliasu (odzyskiwanie po awarii), zwracane są szczegóły reguły autoryzacji skonfigurowanej przestrzeni nazw aliasu.</span><span class="sxs-lookup"><span data-stu-id="bb3e8-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="bb3e8-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bb3e8-113">EXAMPLES</span></span>

### <span data-ttu-id="bb3e8-114">Przykład 1. AuthorizationRule dla przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="bb3e8-114">Example 1: AuthorizationRule for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="bb3e8-115">Pobiera regułę \` autoryzacji MyAuthRuleName \` w przestrzeni nazw \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="bb3e8-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="bb3e8-116">Przykład 2. AuthorizationRules dla przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="bb3e8-116">Example 2: AuthorizationRules for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="bb3e8-117">Pobiera listę wszystkich reguł autoryzacji w przestrzeni nazw \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="bb3e8-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="bb3e8-118">Przykład 3. AutoryzacjaBłędów dla usługi EventHub</span><span class="sxs-lookup"><span data-stu-id="bb3e8-118">Example 3: AuthorizationRule for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="bb3e8-119">Pobiera regułę autoryzacji MyAuthRuleName w centrum zdarzeń MyEventHubName , który jest ograniczony przez przestrzeń nazw \` \` \` \` \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="bb3e8-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="bb3e8-120">Przykład 4. AuthorizationRules dla usługi EventHub</span><span class="sxs-lookup"><span data-stu-id="bb3e8-120">Example 4: AuthorizationRules for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="bb3e8-121">Pobiera reguły autoryzacji listy w witrynie MyEventHubName centrum zdarzeń, która jest podlega zakresowi przestrzeni nazw \` \` \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="bb3e8-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="bb3e8-122">Przykład 5. Funkcja AuthorizationRule dla aliasu (konfiguracja funkcji GeoRecovery)</span><span class="sxs-lookup"><span data-stu-id="bb3e8-122">Example 5: AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="bb3e8-123">Pobiera regułę \` autoryzacji MyAuthRuleName \` w przestrzeni nazw \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="bb3e8-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="bb3e8-124">Przykład 6. AuthorizationRules for Alias (GeoRecovery Configuration)</span><span class="sxs-lookup"><span data-stu-id="bb3e8-124">Example 6: AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="bb3e8-125">Pobiera listę wszystkich reguł autoryzacji \` MyAuthRuleName \` w przestrzeni nazw \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="bb3e8-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="bb3e8-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bb3e8-126">PARAMETERS</span></span>

### <span data-ttu-id="bb3e8-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="bb3e8-127">-AliasName</span></span>
<span data-ttu-id="bb3e8-128">Nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="bb3e8-128">Alias Name</span></span>

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

### <span data-ttu-id="bb3e8-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bb3e8-129">-DefaultProfile</span></span>
<span data-ttu-id="bb3e8-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bb3e8-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bb3e8-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="bb3e8-131">-Eventhub</span></span>
<span data-ttu-id="bb3e8-132">Nazwa aplikacji Eventhub</span><span class="sxs-lookup"><span data-stu-id="bb3e8-132">Eventhub Name</span></span>

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

### <span data-ttu-id="bb3e8-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="bb3e8-133">-Name</span></span>
<span data-ttu-id="bb3e8-134">Nazwa podmiotu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="bb3e8-134">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="bb3e8-135">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="bb3e8-135">-Namespace</span></span>
<span data-ttu-id="bb3e8-136">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="bb3e8-136">Namespace Name</span></span>

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

### <span data-ttu-id="bb3e8-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bb3e8-137">-ResourceGroupName</span></span>
<span data-ttu-id="bb3e8-138">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bb3e8-138">Resource Group Name</span></span>

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

### <span data-ttu-id="bb3e8-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bb3e8-139">CommonParameters</span></span>
<span data-ttu-id="bb3e8-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bb3e8-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bb3e8-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bb3e8-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bb3e8-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb3e8-142">INPUTS</span></span>

### <span data-ttu-id="bb3e8-143">System.String</span><span class="sxs-lookup"><span data-stu-id="bb3e8-143">System.String</span></span>

## <span data-ttu-id="bb3e8-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bb3e8-144">OUTPUTS</span></span>

### <span data-ttu-id="bb3e8-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="bb3e8-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="bb3e8-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bb3e8-146">NOTES</span></span>

## <span data-ttu-id="bb3e8-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bb3e8-147">RELATED LINKS</span></span>
