---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: e4600b44943170256d2c8ef999496d2160e369ab
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549195"
---
# <span data-ttu-id="4888d-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4888d-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="4888d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4888d-102">SYNOPSIS</span></span>
<span data-ttu-id="4888d-103">Aktualizuje określoną regułę autoryzacji w centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="4888d-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4888d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4888d-104">SYNTAX</span></span>

### <span data-ttu-id="4888d-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4888d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4888d-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4888d-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace <String>] -EventHub <String>
 -Name <String> [-InputObject <AuthorizationRuleAttributes>] [-Rights <String[]>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4888d-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4888d-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String>
 -InputObject <AuthorizationRuleAttributes> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="4888d-108">AuthoRulePropertiesSet</span><span class="sxs-lookup"><span data-stu-id="4888d-108">AuthoRulePropertiesSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> -Name <String> -Rights <String[]> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="4888d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="4888d-109">DESCRIPTION</span></span>
<span data-ttu-id="4888d-110">Polecenie cmdlet Set-AzureRmEventHubAuthorizationRule aktualizuje określoną regułę autoryzacji w danym centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="4888d-110">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="4888d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4888d-111">EXAMPLES</span></span>

### <span data-ttu-id="4888d-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4888d-112">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="4888d-113">Aktualizuje MyAuthRuleName reguły autoryzacji \` \` , aby udzielić praw do zarządzania MyEventHubName centrum zdarzeń \` \` , których zakresem jest obszar nazw \` \` obszar_nazwname.</span><span class="sxs-lookup"><span data-stu-id="4888d-113">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="4888d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4888d-114">PARAMETERS</span></span>

### <span data-ttu-id="4888d-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4888d-115">-ResourceGroupName</span></span>
<span data-ttu-id="4888d-116">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4888d-116">Resource group name.</span></span>

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

### <span data-ttu-id="4888d-117">-Prawa</span><span class="sxs-lookup"><span data-stu-id="4888d-117">-Rights</span></span>
<span data-ttu-id="4888d-118">Wymagany, jeśli nie podano parametru "AuthruleObj".</span><span class="sxs-lookup"><span data-stu-id="4888d-118">Required if 'AuthruleObj' not specified.</span></span>
<span data-ttu-id="4888d-119">Intelektualn na przykład @ ("nasłuchuj"; "Wyślij"; "Zarządzaj")</span><span class="sxs-lookup"><span data-stu-id="4888d-119">Rights; for example, @("Listen","Send","Manage")</span></span>

```yaml
Type: String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: AuthoRulePropertiesSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4888d-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4888d-120">-Confirm</span></span>
<span data-ttu-id="4888d-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4888d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4888d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4888d-122">-WhatIf</span></span>
<span data-ttu-id="4888d-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4888d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4888d-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4888d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4888d-125">— EventHub</span><span class="sxs-lookup"><span data-stu-id="4888d-125">-EventHub</span></span>
<span data-ttu-id="4888d-126">Nazwa EventHub.</span><span class="sxs-lookup"><span data-stu-id="4888d-126">EventHub Name.</span></span>

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

### <span data-ttu-id="4888d-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4888d-127">-InputObject</span></span>
<span data-ttu-id="4888d-128">{{Fillobject opis}}</span><span class="sxs-lookup"><span data-stu-id="4888d-128">{{Fill InputObject Description}}</span></span>

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: AuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4888d-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4888d-129">-Name</span></span>
<span data-ttu-id="4888d-130">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="4888d-130">AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="4888d-131">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4888d-131">-Namespace</span></span>
<span data-ttu-id="4888d-132">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="4888d-132">Namespace Name.</span></span>

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

## <span data-ttu-id="4888d-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4888d-133">INPUTS</span></span>

### <span data-ttu-id="4888d-134">System. String</span><span class="sxs-lookup"><span data-stu-id="4888d-134">System.String</span></span>

## <span data-ttu-id="4888d-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4888d-135">OUTPUTS</span></span>

### <span data-ttu-id="4888d-136">Microsoft. Azure. Commands. EventHub. modele. SharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="4888d-136">Microsoft.Azure.Commands.EventHub.Models.SharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="4888d-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4888d-137">NOTES</span></span>

## <span data-ttu-id="4888d-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4888d-138">RELATED LINKS</span></span>

