---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: 7722ee1a84aee6ef16642a84ac9f72f259d9772f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716878"
---
# <span data-ttu-id="36696-101">Remove-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="36696-101">Remove-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="36696-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36696-102">SYNOPSIS</span></span>
<span data-ttu-id="36696-103">Umożliwia usunięcie reguły autoryzacji obszaru nazw lub kolejki usługi, od określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="36696-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36696-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36696-104">SYNTAX</span></span>

### <span data-ttu-id="36696-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="36696-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="36696-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="36696-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Queue] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="36696-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="36696-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [[-Namespace] <String>]
 [-Topic] <String> [-Name] <String> [-Force] [-PassThru] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="36696-108">Opis</span><span class="sxs-lookup"><span data-stu-id="36696-108">DESCRIPTION</span></span>
<span data-ttu-id="36696-109">Polecenie cmdlet **Remove-AzureRmServiceBusAuthorizationRule** usuwa regułę autoryzacji obszaru nazw lub kolejki usługi Service Bus dla określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="36696-109">The **Remove-AzureRmServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="36696-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36696-110">EXAMPLES</span></span>

### <span data-ttu-id="36696-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="36696-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```
<span data-ttu-id="36696-112">Usuwa regułę autoryzacji `SBAuthoRule1` obszaru nazw `SB-Example1` z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="36696-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="36696-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="36696-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```
<span data-ttu-id="36696-114">Usuwa regułę autoryzacji `SBAuthoRule1` kolejki `SBQueue` z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="36696-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="36696-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="36696-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```
<span data-ttu-id="36696-116">Usuwa zasadę autoryzacji `SBAuthoRule1` tematu `SBTopic` z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="36696-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="36696-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36696-117">PARAMETERS</span></span>

### <span data-ttu-id="36696-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36696-118">-Confirm</span></span>
<span data-ttu-id="36696-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36696-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36696-120">-Force</span><span class="sxs-lookup"><span data-stu-id="36696-120">-Force</span></span>
<span data-ttu-id="36696-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="36696-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="36696-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36696-122">-Name</span></span>
<span data-ttu-id="36696-123">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="36696-123">AuthorizationRule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36696-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="36696-124">-Namespace</span></span>
<span data-ttu-id="36696-125">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="36696-125">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: NamespaceAuthorizationRuleSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet, TopicAuthorizationRuleSet
Aliases: NamespaceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36696-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="36696-126">-PassThru</span></span>
<span data-ttu-id="36696-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="36696-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="36696-128">-Queue</span><span class="sxs-lookup"><span data-stu-id="36696-128">-Queue</span></span>
<span data-ttu-id="36696-129">Nazwa kolejki.</span><span class="sxs-lookup"><span data-stu-id="36696-129">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36696-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36696-130">-ResourceGroupName</span></span>
<span data-ttu-id="36696-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="36696-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="36696-132">— Temat</span><span class="sxs-lookup"><span data-stu-id="36696-132">-Topic</span></span>
<span data-ttu-id="36696-133">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="36696-133">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36696-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36696-134">-WhatIf</span></span>
<span data-ttu-id="36696-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36696-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36696-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="36696-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="36696-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36696-137">INPUTS</span></span>

### <span data-ttu-id="36696-138">System. String</span><span class="sxs-lookup"><span data-stu-id="36696-138">System.String</span></span>


## <span data-ttu-id="36696-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36696-139">OUTPUTS</span></span>

### <span data-ttu-id="36696-140">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="36696-140">System.Boolean</span></span>


## <span data-ttu-id="36696-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36696-141">NOTES</span></span>

## <span data-ttu-id="36696-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36696-142">RELATED LINKS</span></span>

