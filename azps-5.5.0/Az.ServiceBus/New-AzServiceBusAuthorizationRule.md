---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/new-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/New-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: beba9c457378949dfe82811186bde84522b46ae5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201666"
---
# <span data-ttu-id="385ce-101">New-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="385ce-101">New-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="385ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="385ce-102">SYNOPSIS</span></span>
<span data-ttu-id="385ce-103">Tworzy nową regułę autoryzacji dla określonego autobusu usług o podanej przestrzeni nazw, kolejce lub temacie.</span><span class="sxs-lookup"><span data-stu-id="385ce-103">Creates a new authorization rule for the specified Service Bus given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="385ce-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="385ce-104">SYNTAX</span></span>

### <span data-ttu-id="385ce-105">NamespaceAuthorizationRuleSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="385ce-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="385ce-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="385ce-106">QueueAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="385ce-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="385ce-107">TopicAuthorizationRuleSet</span></span>
```
New-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> -Rights <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="385ce-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="385ce-108">DESCRIPTION</span></span>
<span data-ttu-id="385ce-109">Polecenie **cmdlet New-AzServiceBusAuthorizationRule** tworzy nową regułę autoryzacji dla określonej przestrzeni nazw, kolejki lub tematu autobusu usługi.</span><span class="sxs-lookup"><span data-stu-id="385ce-109">The **New-AzServiceBusAuthorizationRule** cmdlet creates a new authorization rule for the specified Service Bus namespace or queue or topic.</span></span>

## <span data-ttu-id="385ce-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="385ce-110">EXAMPLES</span></span>

### <span data-ttu-id="385ce-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="385ce-111">Example 1</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="385ce-112">Tworzy `AuthoRule1` za pomocą praw do **odsłuchiwać** i wysyłania dla przestrzeni  `SB-Example1` nazw.</span><span class="sxs-lookup"><span data-stu-id="385ce-112">Creates `AuthoRule1` with **Listen** and **Send** rights for the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="385ce-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="385ce-113">Example 2</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="385ce-114">Tworzy `AuthoRule1` z prawami do **odsłuchiwać** i wysyłania dla  `SBQueue` kolejki.</span><span class="sxs-lookup"><span data-stu-id="385ce-114">Creates `AuthoRule1` with **Listen** and **Send** rights for the queue `SBQueue`.</span></span>

### <span data-ttu-id="385ce-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="385ce-115">Example 3</span></span>
```
PS C:\> New-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1 -Rights @("Listen","Send")
```

<span data-ttu-id="385ce-116">Tworzy `AuthoRule1` z prawami do **odsłuchiwać** i wysyłania dla tematu.  `SBTopic`</span><span class="sxs-lookup"><span data-stu-id="385ce-116">Creates `AuthoRule1` with **Listen** and **Send** rights for the topic `SBTopic`.</span></span>

## <span data-ttu-id="385ce-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="385ce-117">PARAMETERS</span></span>

### <span data-ttu-id="385ce-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="385ce-118">-DefaultProfile</span></span>
<span data-ttu-id="385ce-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="385ce-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="385ce-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="385ce-120">-Name</span></span>
<span data-ttu-id="385ce-121">Nazwa podmiotu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="385ce-121">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="385ce-122">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="385ce-122">-Namespace</span></span>
<span data-ttu-id="385ce-123">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="385ce-123">Namespace Name</span></span>

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

### <span data-ttu-id="385ce-124">— Kolejka</span><span class="sxs-lookup"><span data-stu-id="385ce-124">-Queue</span></span>
<span data-ttu-id="385ce-125">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="385ce-125">Queue Name</span></span>

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

### <span data-ttu-id="385ce-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="385ce-126">-ResourceGroupName</span></span>
<span data-ttu-id="385ce-127">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="385ce-127">Resource Group Name</span></span>

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

### <span data-ttu-id="385ce-128">— Prawa</span><span class="sxs-lookup"><span data-stu-id="385ce-128">-Rights</span></span>
<span data-ttu-id="385ce-129">Prawa, np. "Posłuchaj", "Wyślij", "Zarządzaj"</span><span class="sxs-lookup"><span data-stu-id="385ce-129">Rights, e.g. "Listen","Send","Manage"</span></span>

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

### <span data-ttu-id="385ce-130">— Temat</span><span class="sxs-lookup"><span data-stu-id="385ce-130">-Topic</span></span>
<span data-ttu-id="385ce-131">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="385ce-131">Topic Name</span></span>

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

### <span data-ttu-id="385ce-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="385ce-132">-Confirm</span></span>
<span data-ttu-id="385ce-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="385ce-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="385ce-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="385ce-134">-WhatIf</span></span>
<span data-ttu-id="385ce-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="385ce-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="385ce-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="385ce-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="385ce-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="385ce-137">CommonParameters</span></span>
<span data-ttu-id="385ce-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="385ce-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="385ce-139">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="385ce-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="385ce-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="385ce-140">INPUTS</span></span>

### <span data-ttu-id="385ce-141">System.String</span><span class="sxs-lookup"><span data-stu-id="385ce-141">System.String</span></span>

### <span data-ttu-id="385ce-142">System.String[]</span><span class="sxs-lookup"><span data-stu-id="385ce-142">System.String[]</span></span>

## <span data-ttu-id="385ce-143">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="385ce-143">OUTPUTS</span></span>

### <span data-ttu-id="385ce-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="385ce-144">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="385ce-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="385ce-145">NOTES</span></span>

## <span data-ttu-id="385ce-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="385ce-146">RELATED LINKS</span></span>
