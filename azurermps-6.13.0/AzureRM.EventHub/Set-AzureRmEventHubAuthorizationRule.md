---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 4d77a0a31cdf9e7731346bd70a24533ce7a464c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545352"
---
# <span data-ttu-id="caa5d-101">Set-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="caa5d-101">Set-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="caa5d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="caa5d-102">SYNOPSIS</span></span>
<span data-ttu-id="caa5d-103">Aktualizuje określoną regułę autoryzacji w centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="caa5d-103">Updates the specified authorization rule on an Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="caa5d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="caa5d-104">SYNTAX</span></span>

### <span data-ttu-id="caa5d-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="caa5d-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caa5d-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="caa5d-106">EventhubAuthorizationRuleSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [[-Rights] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="caa5d-107">AuthoRuleInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="caa5d-107">AuthoRuleInputObjectSet</span></span>
```
Set-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Name] <String>
 [-InputObject] <PSSharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="caa5d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="caa5d-108">DESCRIPTION</span></span>
<span data-ttu-id="caa5d-109">Polecenie cmdlet Set-AzureRmEventHubAuthorizationRule aktualizuje określoną regułę autoryzacji w danym centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="caa5d-109">The Set-AzureRmEventHubAuthorizationRule cmdlet updates the specified authorization rule on the given Event Hub.</span></span>

## <span data-ttu-id="caa5d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="caa5d-110">EXAMPLES</span></span>

### <span data-ttu-id="caa5d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="caa5d-111">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Manage")
```

<span data-ttu-id="caa5d-112">Aktualizuje MyAuthRuleName reguły autoryzacji \` \` , aby udzielić praw do zarządzania MyEventHubName centrum zdarzeń \` \` , których zakresem jest obszar nazw \` \` obszar_nazwname.</span><span class="sxs-lookup"><span data-stu-id="caa5d-112">Updates the authorization rule \`MyAuthRuleName\` to grant Manage rights to the Event Hub \`MyEventHubName\`, scoped by the namespace \`MyNamespaceName\`.</span></span>

## <span data-ttu-id="caa5d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="caa5d-113">PARAMETERS</span></span>

### <span data-ttu-id="caa5d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="caa5d-114">-DefaultProfile</span></span>
<span data-ttu-id="caa5d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="caa5d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="caa5d-116">— EventHub</span><span class="sxs-lookup"><span data-stu-id="caa5d-116">-EventHub</span></span>
<span data-ttu-id="caa5d-117">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="caa5d-117">EventHub Name</span></span>

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

### <span data-ttu-id="caa5d-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="caa5d-118">-InputObject</span></span>
<span data-ttu-id="caa5d-119">Obiekt AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="caa5d-119">AuthorizationRule Object</span></span>

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

### <span data-ttu-id="caa5d-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="caa5d-120">-Name</span></span>
<span data-ttu-id="caa5d-121">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="caa5d-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="caa5d-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="caa5d-122">-Namespace</span></span>
<span data-ttu-id="caa5d-123">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="caa5d-123">Namespace Name</span></span>

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

### <span data-ttu-id="caa5d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="caa5d-124">-ResourceGroupName</span></span>
<span data-ttu-id="caa5d-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="caa5d-125">Resource Group Name</span></span>

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

### <span data-ttu-id="caa5d-126">-Prawa</span><span class="sxs-lookup"><span data-stu-id="caa5d-126">-Rights</span></span>
<span data-ttu-id="caa5d-127">Prawa, na przykład @ ("nasłuchuj", "Wyślij", "Zarządzaj")</span><span class="sxs-lookup"><span data-stu-id="caa5d-127">Rights, e.g. @("Listen","Send","Manage")</span></span>

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

### <span data-ttu-id="caa5d-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="caa5d-128">-Confirm</span></span>
<span data-ttu-id="caa5d-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="caa5d-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="caa5d-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="caa5d-130">-WhatIf</span></span>
<span data-ttu-id="caa5d-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="caa5d-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="caa5d-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="caa5d-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="caa5d-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="caa5d-133">CommonParameters</span></span>
<span data-ttu-id="caa5d-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="caa5d-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="caa5d-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="caa5d-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="caa5d-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="caa5d-136">INPUTS</span></span>

### <span data-ttu-id="caa5d-137">System. String</span><span class="sxs-lookup"><span data-stu-id="caa5d-137">System.String</span></span>

### <span data-ttu-id="caa5d-138">Microsoft. Azure. Commands. EventHub. modele. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="caa5d-138">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="caa5d-139">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="caa5d-139">Parameters: InputObject (ByValue)</span></span>

### <span data-ttu-id="caa5d-140">System. String []</span><span class="sxs-lookup"><span data-stu-id="caa5d-140">System.String[]</span></span>

## <span data-ttu-id="caa5d-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="caa5d-141">OUTPUTS</span></span>

### <span data-ttu-id="caa5d-142">Microsoft. Azure. Commands. EventHub. modele. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="caa5d-142">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="caa5d-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="caa5d-143">NOTES</span></span>

## <span data-ttu-id="caa5d-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="caa5d-144">RELATED LINKS</span></span>
