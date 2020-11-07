---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubAuthorizationRule.md
ms.openlocfilehash: 46f640eefcd429a7fec4d06397f394ef31831183
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705418"
---
# <span data-ttu-id="4abba-101">Set-AzEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4abba-101">Set-AzEventHubAuthorizationRule</span></span>

## <span data-ttu-id="4abba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4abba-102">SYNOPSIS</span></span>
<span data-ttu-id="4abba-103">Aktualizuje określoną regułę autoryzacji w centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="4abba-103">Updates the specified authorization rule on an Event Hub.</span></span>

## <span data-ttu-id="4abba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4abba-104">SYNTAX</span></span>

### <span data-ttu-id="4abba-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4abba-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4abba-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="4abba-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4abba-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4abba-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4abba-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4abba-108">DESCRIPTION</span></span>
<span data-ttu-id="4abba-109">Polecenie cmdlet Set-AzEventHubAuthorizationRule aktualizuje określoną regułę autoryzacji w danym centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="4abba-109">The Set-AzEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="4abba-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4abba-110">EXAMPLES</span></span>

### <span data-ttu-id="4abba-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4abba-111">Example 1</span></span>
```
PS C:\> Set-AzEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="4abba-112">Aktualizuje MyAuthRuleName reguły autoryzacji \` \` , aby udzielić praw do zarządzania MyEventHubName centrum zdarzeń \` \` , których zakresem jest obszar nazw \` \` obszar_nazwname.</span><span class="sxs-lookup"><span data-stu-id="4abba-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="4abba-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4abba-113">PARAMETERS</span></span>

### <span data-ttu-id="4abba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4abba-114">-DefaultProfile</span></span>
<span data-ttu-id="4abba-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4abba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4abba-116">— EventHub</span><span class="sxs-lookup"><span data-stu-id="4abba-116">-EventHub</span></span>
<span data-ttu-id="4abba-117">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="4abba-117">EventHub Name</span></span>

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

### <span data-ttu-id="4abba-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4abba-118">-InputObject</span></span>
<span data-ttu-id="4abba-119">Obiekt AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4abba-119">AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: AuthoRuleInputObjectSet
Aliases: AuthRuleObj

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4abba-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4abba-120">-Name</span></span>
<span data-ttu-id="4abba-121">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="4abba-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="4abba-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4abba-122">-Namespace</span></span>
<span data-ttu-id="4abba-123">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="4abba-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4abba-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4abba-124">-ResourceGroupName</span></span>
<span data-ttu-id="4abba-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4abba-125">Resource Group Name</span></span>

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

### <span data-ttu-id="4abba-126">-Prawa</span><span class="sxs-lookup"><span data-stu-id="4abba-126">-Rights</span></span>
<span data-ttu-id="4abba-127">Prawa, na przykład @ ("nasłuchuj", "Wyślij", "Zarządzaj")</span><span class="sxs-lookup"><span data-stu-id="4abba-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

```yaml
Type: System.String[]
Parameter Sets: NamespaceAuthorizationRuleSet, EventhubAuthorizationRuleSet
Aliases:
Accepted values: Listen, Send, Manage

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4abba-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4abba-128">-Confirm</span></span>
<span data-ttu-id="4abba-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4abba-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4abba-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4abba-130">-WhatIf</span></span>
<span data-ttu-id="4abba-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4abba-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4abba-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4abba-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4abba-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4abba-133">CommonParameters</span></span>
<span data-ttu-id="4abba-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4abba-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4abba-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4abba-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4abba-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4abba-136">INPUTS</span></span>

### <span data-ttu-id="4abba-137">System. String</span><span class="sxs-lookup"><span data-stu-id="4abba-137">System.String</span></span>

### <span data-ttu-id="4abba-138">Microsoft. Azure. Commands. EventHub. modele. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="4abba-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

### <span data-ttu-id="4abba-139">System. String []</span><span class="sxs-lookup"><span data-stu-id="4abba-139">System.String[]</span></span>

## <span data-ttu-id="4abba-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4abba-140">OUTPUTS</span></span>

### <span data-ttu-id="4abba-141">Microsoft. Azure. Commands. EventHub. modele. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="4abba-141">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="4abba-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4abba-142">NOTES</span></span>

## <span data-ttu-id="4abba-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4abba-143">RELATED LINKS</span></span>