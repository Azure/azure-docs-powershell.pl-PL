---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 3085479125219450368322ddb64fee4c06cdce2a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717847"
---
# <span data-ttu-id="7de02-101">New-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="7de02-101">New-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="7de02-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7de02-102">SYNOPSIS</span></span>
<span data-ttu-id="7de02-103">Umożliwia utworzenie nowej reguły autoryzacji koncentratora zdarzeń dla obszaru nazw lub centrum eventhub.</span><span class="sxs-lookup"><span data-stu-id="7de02-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7de02-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7de02-104">SYNTAX</span></span>

### <span data-ttu-id="7de02-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7de02-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 -Rights <String[]> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="7de02-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="7de02-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> -Rights <String[]> [-WhatIf] [-Confirm]
```

## <span data-ttu-id="7de02-107">Opis</span><span class="sxs-lookup"><span data-stu-id="7de02-107">DESCRIPTION</span></span>
<span data-ttu-id="7de02-108">Polecenie cmdlet New-AzureRmEventHubAuthorizationRule powoduje utworzenie nowej reguły autoryzacji koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="7de02-108">The New-AzureRmEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="7de02-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7de02-109">EXAMPLES</span></span>

### <span data-ttu-id="7de02-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7de02-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="7de02-111">Umożliwia utworzenie reguły autoryzacji \` MyAuthRuleName \` udzielenie uprawnień do przesłuchiwania i wysyłania do obszaru nazw obszar_nazwname \` \` z grupą zasobów \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="7de02-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="7de02-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7de02-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="7de02-113">Tworzy regułę autoryzacji \` MyAuthRuleName \` udzielania praw do MyEventHubName centrum zdarzeń \` \` w przestrzeni nazw NamespaceName \` \` z MyResourceGroupName grupą zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="7de02-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="7de02-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7de02-114">PARAMETERS</span></span>

### <span data-ttu-id="7de02-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7de02-115">-ResourceGroupName</span></span>
<span data-ttu-id="7de02-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7de02-116">Resource group name.</span></span>

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

### <span data-ttu-id="7de02-117">-Prawa</span><span class="sxs-lookup"><span data-stu-id="7de02-117">-Rights</span></span>
<span data-ttu-id="7de02-118">Intelektualn na przykład @ ("nasłuchuj", "Wyślij", "Zarządzaj").</span><span class="sxs-lookup"><span data-stu-id="7de02-118">Rights; for example @("Listen","Send","Manage").</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de02-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7de02-119">-Confirm</span></span>
<span data-ttu-id="7de02-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7de02-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de02-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7de02-121">-WhatIf</span></span>
<span data-ttu-id="7de02-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7de02-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7de02-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7de02-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7de02-124">— EventHub</span><span class="sxs-lookup"><span data-stu-id="7de02-124">-EventHub</span></span>
<span data-ttu-id="7de02-125">Nazwa EventHub.</span><span class="sxs-lookup"><span data-stu-id="7de02-125">EventHub Name.</span></span>

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

### <span data-ttu-id="7de02-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7de02-126">-Name</span></span>
<span data-ttu-id="7de02-127">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="7de02-127">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7de02-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7de02-128">-Namespace</span></span>
<span data-ttu-id="7de02-129">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="7de02-129">Namespace Name.</span></span>

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

## <span data-ttu-id="7de02-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7de02-130">INPUTS</span></span>

### <span data-ttu-id="7de02-131">System. String</span><span class="sxs-lookup"><span data-stu-id="7de02-131">System.String</span></span>

## <span data-ttu-id="7de02-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7de02-132">OUTPUTS</span></span>

### <span data-ttu-id="7de02-133">Microsoft. Azure. Commands. EventHub. modele. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="7de02-133">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="7de02-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7de02-134">NOTES</span></span>

## <span data-ttu-id="7de02-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7de02-135">RELATED LINKS</span></span>

