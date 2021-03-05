---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/get-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Get-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 842b48e1645bb141650c2a53dc86bbb5e79acb80
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969201"
---
# <span data-ttu-id="64ce1-101">Get-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="64ce1-101">Get-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="64ce1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="64ce1-102">SYNOPSIS</span></span>
<span data-ttu-id="64ce1-103">Pobiera szczegóły reguły autoryzacji lub pobiera listę reguł autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="64ce1-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

## <span data-ttu-id="64ce1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="64ce1-104">SYNTAX</span></span>

### <span data-ttu-id="64ce1-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="64ce1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64ce1-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="64ce1-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Eventhub] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="64ce1-107">AliasAuthoRuleSet</span><span class="sxs-lookup"><span data-stu-id="64ce1-107">AliasAuthoRuleSet</span></span>
```
Get-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-AliasName] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64ce1-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="64ce1-108">DESCRIPTION</span></span>
<span data-ttu-id="64ce1-109">Polecenie Get-AzEventHubAuthorizationRule pobiera szczegóły reguły autoryzacji lub listę wszystkich reguł autoryzacji dla określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="64ce1-109">The Get-AzEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="64ce1-110">Jeśli podano nazwę reguły autoryzacji, zostaną zwrócone szczegóły tej reguły pojedynczej autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="64ce1-110">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="64ce1-111">Jeśli nazwa reguły autoryzacji nie jest podana, jest zwracana lista wszystkich reguł autoryzacji dla określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="64ce1-111">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>
<span data-ttu-id="64ce1-112">Jeśli podano nazwę aliasu (odzyskiwanie po awarii), zwracane są szczegóły reguły autoryzacji skonfigurowanej przestrzeni nazw aliasu.</span><span class="sxs-lookup"><span data-stu-id="64ce1-112">If (Disaster Recovery) Alias name provided, the details of authorization rule of the Namespace for Alias configured is returned.</span></span>

## <span data-ttu-id="64ce1-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="64ce1-113">EXAMPLES</span></span>

### <span data-ttu-id="64ce1-114">Przykład 1. AuthorizationRule dla przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="64ce1-114">Example 1: AuthorizationRule for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyAuthRuleName
```

<span data-ttu-id="64ce1-115">Pobiera regułę \` autoryzacji MyAuthRuleName \` w przestrzeni nazw \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="64ce1-115">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="64ce1-116">Przykład 2. AuthorizationRules dla przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="64ce1-116">Example 2: AuthorizationRules for namespace</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="64ce1-117">Pobiera listę wszystkich reguł autoryzacji w przestrzeni nazw \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="64ce1-117">Gets a list of all authorization rules in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="64ce1-118">Przykład 3. AutoryzacjaBłędów dla usługi EventHub</span><span class="sxs-lookup"><span data-stu-id="64ce1-118">Example 3: AuthorizationRule for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="64ce1-119">Pobiera regułę autoryzacji MyAuthRuleName w centrum zdarzeń MyEventHubName , który jest ograniczony przez przestrzeń nazw \` \` \` \` \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="64ce1-119">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="64ce1-120">Przykład 4. AuthorizationRules dla usługi EventHub</span><span class="sxs-lookup"><span data-stu-id="64ce1-120">Example 4: AuthorizationRules for EventHub</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="64ce1-121">Pobiera reguły autoryzacji listy w witrynie MyEventHubName centrum zdarzeń, która jest podlega zakresowi przestrzeni nazw \` \` \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="64ce1-121">Gets list authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="64ce1-122">Przykład 5. Funkcja AuthorizationRule dla aliasu (konfiguracja funkcji GeoRecovery)</span><span class="sxs-lookup"><span data-stu-id="64ce1-122">Example 5: AuthorizationRule for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName -Name MyAuthRuleName
```

<span data-ttu-id="64ce1-123">Pobiera regułę \` autoryzacji MyAuthRuleName \` w przestrzeni nazw \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="64ce1-123">Gets the authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="64ce1-124">Przykład 6. AuthorizationRules for Alias (Konfiguracja funkcji GeoRecovery)</span><span class="sxs-lookup"><span data-stu-id="64ce1-124">Example 6: AuthorizationRules for Alias (GeoRecovery Configuration)</span></span>
```powershell
PS C:\> Get-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AliasName MyAliasNameName
```

<span data-ttu-id="64ce1-125">Pobiera listę wszystkich reguł autoryzacji \` MyAuthRuleName \` w przestrzeni nazw \` MyNamespaceName. \`</span><span class="sxs-lookup"><span data-stu-id="64ce1-125">Gets a list of all authorization rule \`MyAuthRuleName\` in the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="64ce1-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="64ce1-126">PARAMETERS</span></span>

### <span data-ttu-id="64ce1-127">-AliasName</span><span class="sxs-lookup"><span data-stu-id="64ce1-127">-AliasName</span></span>
<span data-ttu-id="64ce1-128">Nazwa aliasu</span><span class="sxs-lookup"><span data-stu-id="64ce1-128">Alias Name</span></span>

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

### <span data-ttu-id="64ce1-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64ce1-129">-DefaultProfile</span></span>
<span data-ttu-id="64ce1-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="64ce1-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="64ce1-131">-Eventhub</span><span class="sxs-lookup"><span data-stu-id="64ce1-131">-Eventhub</span></span>
<span data-ttu-id="64ce1-132">Nazwa aplikacji Eventhub</span><span class="sxs-lookup"><span data-stu-id="64ce1-132">Eventhub Name</span></span>

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

### <span data-ttu-id="64ce1-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="64ce1-133">-Name</span></span>
<span data-ttu-id="64ce1-134">Nazwa podmiotu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="64ce1-134">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="64ce1-135">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="64ce1-135">-Namespace</span></span>
<span data-ttu-id="64ce1-136">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="64ce1-136">Namespace Name</span></span>

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

### <span data-ttu-id="64ce1-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64ce1-137">-ResourceGroupName</span></span>
<span data-ttu-id="64ce1-138">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="64ce1-138">Resource Group Name</span></span>

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

### <span data-ttu-id="64ce1-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64ce1-139">CommonParameters</span></span>
<span data-ttu-id="64ce1-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64ce1-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64ce1-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64ce1-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64ce1-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64ce1-142">INPUTS</span></span>

### <span data-ttu-id="64ce1-143">System.String</span><span class="sxs-lookup"><span data-stu-id="64ce1-143">System.String</span></span>

## <span data-ttu-id="64ce1-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64ce1-144">OUTPUTS</span></span>

### <span data-ttu-id="64ce1-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="64ce1-145">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="64ce1-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="64ce1-146">NOTES</span></span>

## <span data-ttu-id="64ce1-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64ce1-147">RELATED LINKS</span></span>
