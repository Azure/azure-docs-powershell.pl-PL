---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubAuthorizationRule.md
ms.openlocfilehash: fde71fed26c074efa705d0b1dc181dfb46bae44e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957153"
---
# <span data-ttu-id="19c1c-101">New-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="19c1c-101">New-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="19c1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19c1c-102">SYNOPSIS</span></span>
<span data-ttu-id="19c1c-103">Tworzy nową regułę autoryzacji centrum zdarzeń dla przestrzeni nazw lub aplikacji EventHub.</span><span class="sxs-lookup"><span data-stu-id="19c1c-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

## <span data-ttu-id="19c1c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="19c1c-104">SYNTAX</span></span>

### <span data-ttu-id="19c1c-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="19c1c-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19c1c-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="19c1c-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="19c1c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="19c1c-107">DESCRIPTION</span></span>
<span data-ttu-id="19c1c-108">Polecenie New-AzEventHubAuthorizationRule cmdlet tworzy nową regułę autoryzacji centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="19c1c-108">The New-AzEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="19c1c-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="19c1c-109">EXAMPLES</span></span>

### <span data-ttu-id="19c1c-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="19c1c-110">Example 1</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="19c1c-111">Tworzy regułę autoryzacji MyAuthRuleName, która udziela praw Dosłuchiwanie i Wysyłanie do przestrzeni nazw MyNamespaceName z grupą zasobów \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="19c1c-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="19c1c-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="19c1c-112">Example 2</span></span>
```
PS C:\> New-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="19c1c-113">Tworzy regułę autoryzacji MyAuthRuleName, która udziela uprawnień Dosłuchiwanie i Wysyłanie do centrum zdarzeń MyEventHubName w przestrzeni nazw MyNamespaceName z grupą zasobów \` \` \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="19c1c-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="19c1c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="19c1c-114">PARAMETERS</span></span>

### <span data-ttu-id="19c1c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c1c-115">-DefaultProfile</span></span>
<span data-ttu-id="19c1c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="19c1c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19c1c-117">-EventHub</span><span class="sxs-lookup"><span data-stu-id="19c1c-117">-EventHub</span></span>
<span data-ttu-id="19c1c-118">Nazwa aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="19c1c-118">EventHub Name</span></span>

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

### <span data-ttu-id="19c1c-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="19c1c-119">-Name</span></span>
<span data-ttu-id="19c1c-120">Nazwa podmiotu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="19c1c-120">AuthorizationRule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19c1c-121">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="19c1c-121">-Namespace</span></span>
<span data-ttu-id="19c1c-122">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="19c1c-122">Namespace Name</span></span>

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

### <span data-ttu-id="19c1c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19c1c-123">-ResourceGroupName</span></span>
<span data-ttu-id="19c1c-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="19c1c-124">Resource Group Name</span></span>

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

### <span data-ttu-id="19c1c-125">— Prawa</span><span class="sxs-lookup"><span data-stu-id="19c1c-125">-Rights</span></span>
<span data-ttu-id="19c1c-126">Prawa, np. "Posłuchaj", "Wyślij", "Zarządzaj"</span><span class="sxs-lookup"><span data-stu-id="19c1c-126">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="19c1c-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="19c1c-127">-Confirm</span></span>
<span data-ttu-id="19c1c-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="19c1c-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19c1c-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19c1c-129">-WhatIf</span></span>
<span data-ttu-id="19c1c-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="19c1c-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19c1c-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="19c1c-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19c1c-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c1c-132">CommonParameters</span></span>
<span data-ttu-id="19c1c-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19c1c-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c1c-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c1c-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c1c-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19c1c-135">INPUTS</span></span>

### <span data-ttu-id="19c1c-136">System.String</span><span class="sxs-lookup"><span data-stu-id="19c1c-136">System.String</span></span>

### <span data-ttu-id="19c1c-137">System.String[]</span><span class="sxs-lookup"><span data-stu-id="19c1c-137">System.String[]</span></span>

## <span data-ttu-id="19c1c-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19c1c-138">OUTPUTS</span></span>

### <span data-ttu-id="19c1c-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="19c1c-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="19c1c-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="19c1c-140">NOTES</span></span>

## <span data-ttu-id="19c1c-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19c1c-141">RELATED LINKS</span></span>
