---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: fa9745703046ec835812d5fe477da938ef3fde48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543431"
---
# <span data-ttu-id="fc1a1-101">Remove-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-101">Remove-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="fc1a1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc1a1-102">SYNOPSIS</span></span>
<span data-ttu-id="fc1a1-103">Umożliwia usunięcie reguły autoryzacji obszaru nazw lub kolejki usługi, od określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc1a1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc1a1-104">SYNTAX</span></span>

### <span data-ttu-id="fc1a1-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fc1a1-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc1a1-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fc1a1-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc1a1-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="fc1a1-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc1a1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="fc1a1-108">DESCRIPTION</span></span>
<span data-ttu-id="fc1a1-109">Polecenie cmdlet **Remove-AzureRmServiceBusAuthorizationRule** usuwa regułę autoryzacji obszaru nazw lub kolejki usługi Service Bus dla określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-109">The **Remove-AzureRmServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="fc1a1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc1a1-110">EXAMPLES</span></span>

### <span data-ttu-id="fc1a1-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fc1a1-111">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="fc1a1-112">Usuwa regułę autoryzacji `SBAuthoRule1` obszaru nazw `SB-Example1` z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="fc1a1-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="fc1a1-113">Example 2</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="fc1a1-114">Usuwa regułę autoryzacji `SBAuthoRule1` kolejki `SBQueue` z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="fc1a1-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="fc1a1-115">Example 3</span></span>
```
PS C:\> Remove-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="fc1a1-116">Usuwa zasadę autoryzacji `SBAuthoRule1` tematu `SBTopic` z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="fc1a1-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc1a1-117">PARAMETERS</span></span>

### <span data-ttu-id="fc1a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc1a1-118">-DefaultProfile</span></span>
<span data-ttu-id="fc1a1-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc1a1-120">-Force</span><span class="sxs-lookup"><span data-stu-id="fc1a1-120">-Force</span></span>
<span data-ttu-id="fc1a1-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc1a1-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="fc1a1-122">-InputObject</span></span>
<span data-ttu-id="fc1a1-123">Obiekt AuthorizationRule ServiceBus</span><span class="sxs-lookup"><span data-stu-id="fc1a1-123">ServiceBus AuthorizationRule Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes
Parameter Sets: (All)
Aliases: AuthRuleObj

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc1a1-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fc1a1-124">-Name</span></span>
<span data-ttu-id="fc1a1-125">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="fc1a1-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="fc1a1-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="fc1a1-126">-Namespace</span></span>
<span data-ttu-id="fc1a1-127">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="fc1a1-127">Namespace Name</span></span>

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

### <span data-ttu-id="fc1a1-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fc1a1-128">-PassThru</span></span>
<span data-ttu-id="fc1a1-129">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fc1a1-130">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-130">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fc1a1-131">-Queue</span><span class="sxs-lookup"><span data-stu-id="fc1a1-131">-Queue</span></span>
<span data-ttu-id="fc1a1-132">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="fc1a1-132">Queue Name</span></span>

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

### <span data-ttu-id="fc1a1-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc1a1-133">-ResourceGroupName</span></span>
<span data-ttu-id="fc1a1-134">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="fc1a1-134">Resource Group Name</span></span>

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

### <span data-ttu-id="fc1a1-135">— Temat</span><span class="sxs-lookup"><span data-stu-id="fc1a1-135">-Topic</span></span>
<span data-ttu-id="fc1a1-136">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="fc1a1-136">Topic Name</span></span>

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

### <span data-ttu-id="fc1a1-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc1a1-137">-Confirm</span></span>
<span data-ttu-id="fc1a1-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc1a1-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc1a1-139">-WhatIf</span></span>
<span data-ttu-id="fc1a1-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc1a1-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc1a1-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc1a1-142">CommonParameters</span></span>
<span data-ttu-id="fc1a1-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc1a1-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc1a1-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc1a1-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc1a1-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc1a1-145">INPUTS</span></span>

### <span data-ttu-id="fc1a1-146">System. String</span><span class="sxs-lookup"><span data-stu-id="fc1a1-146">System.String</span></span>

### <span data-ttu-id="fc1a1-147">Microsoft. Azure. Commands. ServiceBus. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="fc1a1-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>
<span data-ttu-id="fc1a1-148">Parametry: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="fc1a1-148">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="fc1a1-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc1a1-149">OUTPUTS</span></span>

### <span data-ttu-id="fc1a1-150">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="fc1a1-150">System.Boolean</span></span>

## <span data-ttu-id="fc1a1-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc1a1-151">NOTES</span></span>

## <span data-ttu-id="fc1a1-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc1a1-152">RELATED LINKS</span></span>
