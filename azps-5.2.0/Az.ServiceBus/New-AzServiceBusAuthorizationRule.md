---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: beba9c457378949dfe82811186bde84522b46ae5
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338845"
---
# <span data-ttu-id="0b939-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0b939-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="0b939-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0b939-102">SYNOPSIS</span></span>
<span data-ttu-id="0b939-103">Tworzy nową regułę autoryzacji dla określonej magistrali usług dla danej przestrzeni nazw lub kolejki lub tematu.</span><span class="sxs-lookup"><span data-stu-id="0b939-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="0b939-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0b939-104">SYNTAX</span></span>

### <span data-ttu-id="0b939-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0b939-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b939-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="0b939-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b939-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="0b939-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0b939-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0b939-108">DESCRIPTION</span></span>
<span data-ttu-id="0b939-109">Polecenie cmdlet **New-AzServiceBusAuthorizationRule** tworzy nową regułę autoryzacji dla określonej przestrzeni nazw lub kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="0b939-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="0b939-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0b939-110">EXAMPLES</span></span>

### <span data-ttu-id="0b939-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0b939-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="0b939-112">Tworzy `AuthoRule1` za pomocą **odsłuchiwania** i **wysyłania** praw do obszaru nazw `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="0b939-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="0b939-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="0b939-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="0b939-114">Tworzy `AuthoRule1` za pomocą **odsłuchiwania** i **wysyłania** praw do kolejki `SBQueue` .</span><span class="sxs-lookup"><span data-stu-id="0b939-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="0b939-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="0b939-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="0b939-116">Tworzy `AuthoRule1` z prawami do **nasłuchiwania** i **wysyłania** tematów `SBTopic` .</span><span class="sxs-lookup"><span data-stu-id="0b939-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="0b939-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0b939-117">PARAMETERS</span></span>

### <span data-ttu-id="0b939-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b939-118">-DefaultProfile</span></span>
<span data-ttu-id="0b939-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0b939-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b939-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0b939-120">-Name</span></span>
<span data-ttu-id="0b939-121">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="0b939-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="0b939-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="0b939-122">-Namespace</span></span>
<span data-ttu-id="0b939-123">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="0b939-123">Namespace Name</span></span>

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

### <span data-ttu-id="0b939-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="0b939-124">-Queue</span></span>
<span data-ttu-id="0b939-125">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="0b939-125">Queue Name</span></span>

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

### <span data-ttu-id="0b939-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b939-126">-ResourceGroupName</span></span>
<span data-ttu-id="0b939-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="0b939-127">Resource Group Name</span></span>

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

### <span data-ttu-id="0b939-128">-Prawa</span><span class="sxs-lookup"><span data-stu-id="0b939-128">-Rights</span></span>
<span data-ttu-id="0b939-129">Prawa, na przykład "odsłuchiwanie", "Wyślij", "Zarządzaj"</span><span class="sxs-lookup"><span data-stu-id="0b939-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="0b939-130">— Temat</span><span class="sxs-lookup"><span data-stu-id="0b939-130">-Topic</span></span>
<span data-ttu-id="0b939-131">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="0b939-131">Topic Name</span></span>

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

### <span data-ttu-id="0b939-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0b939-132">-Confirm</span></span>
<span data-ttu-id="0b939-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b939-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b939-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b939-134">-WhatIf</span></span>
<span data-ttu-id="0b939-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0b939-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0b939-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0b939-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b939-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b939-137">CommonParameters</span></span>
<span data-ttu-id="0b939-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0b939-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b939-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0b939-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b939-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0b939-140">INPUTS</span></span>

### <span data-ttu-id="0b939-141">System. String</span><span class="sxs-lookup"><span data-stu-id="0b939-141">System.String</span></span>

### <span data-ttu-id="0b939-142">System. String []</span><span class="sxs-lookup"><span data-stu-id="0b939-142">System.String[]</span></span>

## <span data-ttu-id="0b939-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0b939-143">OUTPUTS</span></span>

### <span data-ttu-id="0b939-144">Microsoft. Azure. Commands. ServiceBus. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="0b939-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="0b939-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0b939-145">NOTES</span></span>

## <span data-ttu-id="0b939-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0b939-146">RELATED LINKS</span></span>
