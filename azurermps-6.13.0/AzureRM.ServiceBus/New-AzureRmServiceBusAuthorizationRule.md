---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/new-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/New-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: ca9fc6d86617d5d4bc8af8a5b02b059178073e5d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717366"
---
# <span data-ttu-id="e1ef4-101">New-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e1ef4-101">New-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="e1ef4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1ef4-102">SYNOPSIS</span></span>
<span data-ttu-id="e1ef4-103">Tworzy nową regułę autoryzacji dla określonej magistrali usług dla danej przestrzeni nazw lub kolejki lub tematu.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1ef4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1ef4-104">SYNTAX</span></span>

### <span data-ttu-id="e1ef4-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e1ef4-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e1ef4-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e1ef4-106">QueueAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e1ef4-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="e1ef4-107">TopicAuthorizationRuleSet</span></span>
```
New-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e1ef4-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e1ef4-108">DESCRIPTION</span></span>
<span data-ttu-id="e1ef4-109">Polecenie cmdlet **New-AzureRmServiceBusAuthorizationRule** tworzy nową regułę autoryzacji dla określonej przestrzeni nazw lub kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-109">The **New-AzureRmServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="e1ef4-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1ef4-110">EXAMPLES</span></span>

### <span data-ttu-id="e1ef4-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e1ef4-111">Example 1</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="e1ef4-112">Tworzy `AuthoRule1` za pomocą **odsłuchiwania** i **wysyłania** praw do obszaru nazw `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="e1ef4-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="e1ef4-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e1ef4-113">Example 2</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="e1ef4-114">Tworzy `AuthoRule1` za pomocą **odsłuchiwania** i **wysyłania** praw do kolejki `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="e1ef4-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="e1ef4-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="e1ef4-115">Example 3</span></span>
```
PS C:\> New-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="e1ef4-116">Tworzy `AuthoRule1` z prawami do **nasłuchiwania** i **wysyłania** tematów `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="e1ef4-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="e1ef4-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1ef4-117">PARAMETERS</span></span>

### <span data-ttu-id="e1ef4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1ef4-118">-DefaultProfile</span></span>
<span data-ttu-id="e1ef4-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e1ef4-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e1ef4-120">-Name</span></span>
<span data-ttu-id="e1ef4-121">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="e1ef4-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="e1ef4-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e1ef4-122">-Namespace</span></span>
<span data-ttu-id="e1ef4-123">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="e1ef4-123">Namespace Name</span></span>

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

### <span data-ttu-id="e1ef4-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="e1ef4-124">-Queue</span></span>
<span data-ttu-id="e1ef4-125">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="e1ef4-125">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ef4-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e1ef4-126">-ResourceGroupName</span></span>
<span data-ttu-id="e1ef4-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e1ef4-127">Resource Group Name</span></span>

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

### <span data-ttu-id="e1ef4-128">-Prawa</span><span class="sxs-lookup"><span data-stu-id="e1ef4-128">-Rights</span></span>
<span data-ttu-id="e1ef4-129">Prawa, na przykład "odsłuchiwanie", "Wyślij", "Zarządzaj"</span><span class="sxs-lookup"><span data-stu-id="e1ef4-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="e1ef4-130">— Temat</span><span class="sxs-lookup"><span data-stu-id="e1ef4-130">-Topic</span></span>
<span data-ttu-id="e1ef4-131">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="e1ef4-131">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e1ef4-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e1ef4-132">-Confirm</span></span>
<span data-ttu-id="e1ef4-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e1ef4-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e1ef4-134">-WhatIf</span></span>
<span data-ttu-id="e1ef4-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e1ef4-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e1ef4-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1ef4-137">CommonParameters</span></span>
<span data-ttu-id="e1ef4-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1ef4-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1ef4-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1ef4-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1ef4-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1ef4-140">INPUTS</span></span>

### <span data-ttu-id="e1ef4-141">System. String</span><span class="sxs-lookup"><span data-stu-id="e1ef4-141">System.String</span></span>

### <span data-ttu-id="e1ef4-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="e1ef4-142">System.String[]</span></span>

## <span data-ttu-id="e1ef4-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1ef4-143">OUTPUTS</span></span>

### <span data-ttu-id="e1ef4-144">Microsoft. Azure. Commands. ServiceBus. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="e1ef4-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="e1ef4-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1ef4-145">NOTES</span></span>

## <span data-ttu-id="e1ef4-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1ef4-146">RELATED LINKS</span></span>
