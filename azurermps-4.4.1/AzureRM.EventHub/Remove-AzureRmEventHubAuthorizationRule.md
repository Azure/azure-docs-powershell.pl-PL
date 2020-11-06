---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Remove-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 439d4ea871d70fa830bb5a0f327cbc0f75d137df
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553895"
---
# <span data-ttu-id="bd5a8-101">Remove-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="bd5a8-101">Remove-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="bd5a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd5a8-102">SYNOPSIS</span></span>
<span data-ttu-id="bd5a8-103">Usuwa określoną regułę autoryzacji centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="bd5a8-103">Removes the specified Event Hub authorization rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd5a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd5a8-104">SYNTAX</span></span>

### <span data-ttu-id="bd5a8-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bd5a8-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="bd5a8-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="bd5a8-106">EventhubAuthorizationRuleSet</span></span>
```
Remove-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="bd5a8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bd5a8-107">DESCRIPTION</span></span>
<span data-ttu-id="bd5a8-108">Polecenie cmdlet Remove-AzureRmEventHubAuthorizationRule powoduje usunięcie i usunięcie określonej reguły autoryzacji z danego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="bd5a8-108">The Remove-AzureRmEventHubAuthorizationRule cmdlet removes and deletes the specified authorization rule from the given Event Hub.</span></span>

## <span data-ttu-id="bd5a8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd5a8-109">EXAMPLES</span></span>

### <span data-ttu-id="bd5a8-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bd5a8-110">Example 1</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyAuthRuleName
```

### <span data-ttu-id="bd5a8-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="bd5a8-111">Example 2</span></span>
```
PS C:\> Remove-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -EventHub MyEventHubName -Name MyAuthRuleName
```

<span data-ttu-id="bd5a8-112">Usuwa regułę autoryzacji \` MyAuthRuleName \` z MyEventHubName centrum zdarzeń \` \` .</span><span class="sxs-lookup"><span data-stu-id="bd5a8-112">Removes the authorization rule \`MyAuthRuleName\` from the Event Hub \`MyEventHubName\`.</span></span>

## <span data-ttu-id="bd5a8-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd5a8-113">PARAMETERS</span></span>

### <span data-ttu-id="bd5a8-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd5a8-114">-ResourceGroupName</span></span>
<span data-ttu-id="bd5a8-115">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="bd5a8-115">Resource group name.</span></span>

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

### <span data-ttu-id="bd5a8-116">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bd5a8-116">-Confirm</span></span>
<span data-ttu-id="bd5a8-117">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd5a8-117">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd5a8-118">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd5a8-118">-WhatIf</span></span>
<span data-ttu-id="bd5a8-119">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bd5a8-119">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bd5a8-120">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bd5a8-120">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd5a8-121">— EventHub</span><span class="sxs-lookup"><span data-stu-id="bd5a8-121">-EventHub</span></span>
<span data-ttu-id="bd5a8-122">Nazwa EventHub.</span><span class="sxs-lookup"><span data-stu-id="bd5a8-122">EventHub Name.</span></span>

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

### <span data-ttu-id="bd5a8-123">-Force</span><span class="sxs-lookup"><span data-stu-id="bd5a8-123">-Force</span></span>
<span data-ttu-id="bd5a8-124">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="bd5a8-124">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd5a8-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bd5a8-125">-Name</span></span>
<span data-ttu-id="bd5a8-126">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="bd5a8-126">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="bd5a8-127">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bd5a8-127">-Namespace</span></span>
<span data-ttu-id="bd5a8-128">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="bd5a8-128">Namespace Name.</span></span>

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

### <span data-ttu-id="bd5a8-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd5a8-129">-PassThru</span></span>
<span data-ttu-id="bd5a8-130">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="bd5a8-130">{{Fill PassThru Description}}</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="bd5a8-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd5a8-131">INPUTS</span></span>

### <span data-ttu-id="bd5a8-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bd5a8-132">System.String</span></span>

## <span data-ttu-id="bd5a8-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd5a8-133">OUTPUTS</span></span>

### <span data-ttu-id="bd5a8-134">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="bd5a8-134">System.Boolean</span></span>

## <span data-ttu-id="bd5a8-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd5a8-135">NOTES</span></span>

## <span data-ttu-id="bd5a8-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd5a8-136">RELATED LINKS</span></span>

