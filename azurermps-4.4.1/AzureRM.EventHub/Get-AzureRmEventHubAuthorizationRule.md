---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Get-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 69bff610bdcb7795ed582fb6fe882a9e7cc27c8f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553912"
---
# <span data-ttu-id="c5bad-101">Get-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="c5bad-101">Get-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="c5bad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c5bad-102">SYNOPSIS</span></span>
<span data-ttu-id="c5bad-103">Pobiera szczegóły reguły autoryzacji lub pobiera listę reguł autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="c5bad-103">Gets the details of an authorization rule, or gets a list of authorization rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5bad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c5bad-104">SYNTAX</span></span>

### <span data-ttu-id="c5bad-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c5bad-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> [-Name <String>]
```

### <span data-ttu-id="c5bad-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="c5bad-106">EventhubAuthorizationRuleSet</span></span>
```
Get-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -Eventhub <String>
 [-Name <String>]
```

## <span data-ttu-id="c5bad-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c5bad-107">DESCRIPTION</span></span>
<span data-ttu-id="c5bad-108">Polecenie cmdlet Get-AzureRmEventHubAuthorizationRule pobiera szczegóły reguły autoryzacji lub listę wszystkich reguł autoryzacji określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c5bad-108">The Get-AzureRmEventHubAuthorizationRule cmdlet gets either the details of an authorization rule, or a list of all authorization rules for a specified Event Hub.</span></span>
<span data-ttu-id="c5bad-109">Jeśli jest podana nazwa reguły autoryzacji, zostaną zwrócone szczegóły dotyczące jednej reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="c5bad-109">If the name of an authorization rule is provided, the details of that single authorization rule are returned.</span></span>
<span data-ttu-id="c5bad-110">Jeśli nie podano nazwy reguły autoryzacji, zostanie zwrócona lista wszystkich reguł autoryzacji określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c5bad-110">If the name of an authorization rule is not provided, a list of all authorization rules for the specified Event Hub is returned.</span></span>

## <span data-ttu-id="c5bad-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c5bad-111">EXAMPLES</span></span>

### <span data-ttu-id="c5bad-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c5bad-112">Example 1</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRule MyAuthRuleName
```

<span data-ttu-id="c5bad-113">Pobiera regułę autoryzacji \` MyAuthRuleName \` w MyEventHubName centrum zdarzeń \` \` , która jest zakresem obszaru nazw \` \` obszar_nazwname.</span><span class="sxs-lookup"><span data-stu-id="c5bad-113">Gets the authorization rule \`MyAuthRuleName\` in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

### <span data-ttu-id="c5bad-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="c5bad-114">Example 2</span></span>
```
PS C:\> Get-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName
```

<span data-ttu-id="c5bad-115">Pobiera listę wszystkich reguł autoryzacji w MyEventHubName centrum zdarzeń \` \` , które są objęte zakresem przestrzeni nazw obszar_nazwname \` \` .</span><span class="sxs-lookup"><span data-stu-id="c5bad-115">Gets a list of all authorization rules in the Event Hub \`MyEventHubName\`, which is scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="c5bad-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c5bad-116">PARAMETERS</span></span>

### <span data-ttu-id="c5bad-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5bad-117">-ResourceGroupName</span></span>
<span data-ttu-id="c5bad-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c5bad-118">Resource group name.</span></span>

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

### <span data-ttu-id="c5bad-119">— Eventhub</span><span class="sxs-lookup"><span data-stu-id="c5bad-119">-Eventhub</span></span>
<span data-ttu-id="c5bad-120">Nazwa Eventhub.</span><span class="sxs-lookup"><span data-stu-id="c5bad-120">Eventhub Name.</span></span>

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bad-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c5bad-121">-Name</span></span>
<span data-ttu-id="c5bad-122">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="c5bad-122">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5bad-123">-Namespace</span><span class="sxs-lookup"><span data-stu-id="c5bad-123">-Namespace</span></span>
<span data-ttu-id="c5bad-124">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="c5bad-124">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="c5bad-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c5bad-125">INPUTS</span></span>

### <span data-ttu-id="c5bad-126">System. String</span><span class="sxs-lookup"><span data-stu-id="c5bad-126">System.String</span></span>

## <span data-ttu-id="c5bad-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c5bad-127">OUTPUTS</span></span>

### <span data-ttu-id="c5bad-128">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. EventHub. modele. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. EventHub, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="c5bad-128">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.EventHub, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="c5bad-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c5bad-129">NOTES</span></span>

## <span data-ttu-id="c5bad-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c5bad-130">RELATED LINKS</span></span>

