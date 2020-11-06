---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubNamespaceAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 52bf68f1105ea6aa6ec0a78fac1a75defa1d865a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554368"
---
# <span data-ttu-id="23731-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="23731-101">Set-AzureRmEventHubNamespaceAuthorizationRule</span></span>

## <span data-ttu-id="23731-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="23731-102">SYNOPSIS</span></span>
<span data-ttu-id="23731-103">Umożliwia zaktualizowanie reguły autoryzacji w określonym obszarze nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="23731-103">Updates the authorization rule on the specified Event Hubs namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="23731-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="23731-104">SYNTAX</span></span>

```
Set-AzureRmEventHubNamespaceAuthorizationRule [-ResourceGroupName] <String> [-NamespaceName] <String>
 [-AuthRuleObj] <AuthorizationRuleAttributes> [[-AuthorizationRuleName] <String>] [-Rights <String[]>]
 [-WhatIf] [-Confirm]
```

## <span data-ttu-id="23731-105">Opis</span><span class="sxs-lookup"><span data-stu-id="23731-105">DESCRIPTION</span></span>
<span data-ttu-id="23731-106">Polecenie cmdlet Set-AzureRmEventHubNamespaceAuthorizationRule aktualizuje regułę autoryzacji w określonym obszarze nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="23731-106">The Set-AzureRmEventHubNamespaceAuthorizationRule cmdlet updates the authorization rule on the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="23731-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="23731-107">EXAMPLES</span></span>

### <span data-ttu-id="23731-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="23731-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubNamespaceAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="23731-109">Aktualizuje MyAuthRuleName reguły autoryzacji \` \` , aby udzielić praw do zarządzania.</span><span class="sxs-lookup"><span data-stu-id="23731-109">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights.</span></span>

## <span data-ttu-id="23731-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="23731-110">PARAMETERS</span></span>

### <span data-ttu-id="23731-111">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="23731-111">-AuthorizationRuleName</span></span>
<span data-ttu-id="23731-112">Nazwa reguły autoryzacji.</span><span class="sxs-lookup"><span data-stu-id="23731-112">The authorization rule name.</span></span>
<span data-ttu-id="23731-113">Wymagane, jeśli nie podano parametru-AuthruleObj.</span><span class="sxs-lookup"><span data-stu-id="23731-113">Required if -AuthruleObj is not specified.</span></span>

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

### <span data-ttu-id="23731-114">-AuthRuleObj</span><span class="sxs-lookup"><span data-stu-id="23731-114">-AuthRuleObj</span></span>
<span data-ttu-id="23731-115">Obiekt reguły autoryzacji obszaru nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="23731-115">The Event Hubs namespace authorization rule object.</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="23731-116">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="23731-116">-NamespaceName</span></span>
<span data-ttu-id="23731-117">Nazwa obszaru nazw koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="23731-117">The Event Hubs namespace name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23731-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23731-118">-ResourceGroupName</span></span>
<span data-ttu-id="23731-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="23731-119">Resource group name.</span></span>

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

### <span data-ttu-id="23731-120">-Prawa</span><span class="sxs-lookup"><span data-stu-id="23731-120">-Rights</span></span>
<span data-ttu-id="23731-121">Wymagane, jeśli nie podano parametru-AuthruleObj.</span><span class="sxs-lookup"><span data-stu-id="23731-121">Required if -AuthruleObj is not specified.</span></span>
<span data-ttu-id="23731-122">Intelektualn na przykład @ ("nasłuchuj"; "Wyślij"; "Zarządzaj")</span><span class="sxs-lookup"><span data-stu-id="23731-122">Rights; for example,  @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23731-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="23731-123">-Confirm</span></span>
<span data-ttu-id="23731-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23731-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23731-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23731-125">-WhatIf</span></span>
<span data-ttu-id="23731-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="23731-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23731-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="23731-127">The cmdlet is not run.</span></span>

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

## <span data-ttu-id="23731-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="23731-128">INPUTS</span></span>

### <span data-ttu-id="23731-129">System. String</span><span class="sxs-lookup"><span data-stu-id="23731-129">System.String</span></span>

## <span data-ttu-id="23731-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="23731-130">OUTPUTS</span></span>

### <span data-ttu-id="23731-131">Microsoft. Azure. Commands. EventHub. modele. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="23731-131">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="23731-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="23731-132">NOTES</span></span>

## <span data-ttu-id="23731-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="23731-133">RELATED LINKS</span></span>

