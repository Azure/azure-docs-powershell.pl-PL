---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubAuthorizationRule.md
ms.openlocfilehash: 63da2be82f8af6339a68eab580c6871b05f2d884
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718601"
---
# <span data-ttu-id="ed7fe-101">New-AzureRmEventHubAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ed7fe-101">New-AzureRmEventHubAuthorizationRule</span></span>

## <span data-ttu-id="ed7fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed7fe-102">SYNOPSIS</span></span>
<span data-ttu-id="ed7fe-103">Umożliwia utworzenie nowej reguły autoryzacji koncentratora zdarzeń dla obszaru nazw lub centrum eventhub.</span><span class="sxs-lookup"><span data-stu-id="ed7fe-103">Creates a new Event Hubs authorization rule for namespace or eventhub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed7fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed7fe-104">SYNTAX</span></span>

### <span data-ttu-id="ed7fe-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ed7fe-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ed7fe-106">EventhubAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="ed7fe-106">EventhubAuthorizationRuleSet</span></span>
```
New-AzureRmEventHubAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ed7fe-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ed7fe-107">DESCRIPTION</span></span>
<span data-ttu-id="ed7fe-108">Polecenie cmdlet New-AzureRmEventHubAuthorizationRule powoduje utworzenie nowej reguły autoryzacji koncentratora zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="ed7fe-108">The New-AzureRmEventHubAuthorizationRule cmdlet creates a new Event Hubs authorization rule.</span></span>

## <span data-ttu-id="ed7fe-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed7fe-109">EXAMPLES</span></span>

### <span data-ttu-id="ed7fe-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ed7fe-110">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="ed7fe-111">Umożliwia utworzenie reguły autoryzacji \` MyAuthRuleName \` udzielenie uprawnień do przesłuchiwania i wysyłania do obszaru nazw obszar_nazwname \` \` z grupą zasobów \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="ed7fe-111">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="ed7fe-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ed7fe-112">Example 2</span></span>
```
PS C:\> New-AzureRmEventHubAuthorizationRule -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -AuthorizationRuleName MyAuthRuleName -Rights @("Listen","Send")
```

<span data-ttu-id="ed7fe-113">Tworzy regułę autoryzacji \` MyAuthRuleName \` udzielania praw do MyEventHubName centrum zdarzeń \` \` w przestrzeni nazw NamespaceName \` \` z MyResourceGroupName grupą zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="ed7fe-113">Creates an authorization rule \`MyAuthRuleName\` granting Listen and Send rights to the Event Hub \`MyEventHubName\` in namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="ed7fe-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed7fe-114">PARAMETERS</span></span>

### <span data-ttu-id="ed7fe-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed7fe-115">-DefaultProfile</span></span>
<span data-ttu-id="ed7fe-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed7fe-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed7fe-117">— EventHub</span><span class="sxs-lookup"><span data-stu-id="ed7fe-117">-EventHub</span></span>
<span data-ttu-id="ed7fe-118">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="ed7fe-118">EventHub Name</span></span>

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

### <span data-ttu-id="ed7fe-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ed7fe-119">-Name</span></span>
<span data-ttu-id="ed7fe-120">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="ed7fe-120">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="ed7fe-121">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ed7fe-121">-Namespace</span></span>
<span data-ttu-id="ed7fe-122">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="ed7fe-122">Namespace Name</span></span>

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

### <span data-ttu-id="ed7fe-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed7fe-123">-ResourceGroupName</span></span>
<span data-ttu-id="ed7fe-124">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ed7fe-124">Resource Group Name</span></span>

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

### <span data-ttu-id="ed7fe-125">-Prawa</span><span class="sxs-lookup"><span data-stu-id="ed7fe-125">-Rights</span></span>
<span data-ttu-id="ed7fe-126">Prawa, na przykład "odsłuchiwanie", "Wyślij", "Zarządzaj"</span><span class="sxs-lookup"><span data-stu-id="ed7fe-126">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="ed7fe-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ed7fe-127">-Confirm</span></span>
<span data-ttu-id="ed7fe-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed7fe-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed7fe-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed7fe-129">-WhatIf</span></span>
<span data-ttu-id="ed7fe-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ed7fe-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ed7fe-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ed7fe-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed7fe-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed7fe-132">CommonParameters</span></span>
<span data-ttu-id="ed7fe-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed7fe-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed7fe-134">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed7fe-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed7fe-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed7fe-135">INPUTS</span></span>

### <span data-ttu-id="ed7fe-136">System. String</span><span class="sxs-lookup"><span data-stu-id="ed7fe-136">System.String</span></span>

### <span data-ttu-id="ed7fe-137">System. String []</span><span class="sxs-lookup"><span data-stu-id="ed7fe-137">System.String[]</span></span>

## <span data-ttu-id="ed7fe-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed7fe-138">OUTPUTS</span></span>

### <span data-ttu-id="ed7fe-139">Microsoft. Azure. Commands. EventHub. modele. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="ed7fe-139">Microsoft.Azure.Commands.EventHub.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="ed7fe-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed7fe-140">NOTES</span></span>

## <span data-ttu-id="ed7fe-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed7fe-141">RELATED LINKS</span></span>