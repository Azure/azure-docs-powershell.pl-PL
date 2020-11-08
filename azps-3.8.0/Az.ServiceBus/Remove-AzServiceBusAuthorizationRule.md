---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusauthorizationrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusAuthorizationRule.md
ms.openlocfilehash: e6e3fb3c1998a009b10599c3ea059a147ab7f9ce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050267"
---
# <span data-ttu-id="a4c23-101">Remove-AzServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a4c23-101">Remove-AzServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="a4c23-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4c23-102">SYNOPSIS</span></span>
<span data-ttu-id="a4c23-103">Umożliwia usunięcie reguły autoryzacji obszaru nazw lub kolejki usługi, od określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4c23-103">Removes the authorization rule of a Service Bus namespace or queue or topic from the specified resource group.</span></span>

## <span data-ttu-id="a4c23-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4c23-104">SYNTAX</span></span>

### <span data-ttu-id="a4c23-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a4c23-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4c23-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a4c23-106">QueueAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a4c23-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a4c23-107">TopicAuthorizationRuleSet</span></span>
```
Remove-AzServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [[-InputObject] <PSSharedAccessAuthorizationRuleAttributes>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a4c23-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a4c23-108">DESCRIPTION</span></span>
<span data-ttu-id="a4c23-109">Polecenie cmdlet **Remove-AzServiceBusAuthorizationRule** usuwa regułę autoryzacji obszaru nazw lub kolejki usługi Service Bus dla określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4c23-109">The **Remove-AzServiceBusAuthorizationRule** cmdlet removes the authorization rule of a Service Bus namespace or queue or topic for the specified resource group.</span></span>

## <span data-ttu-id="a4c23-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4c23-110">EXAMPLES</span></span>

### <span data-ttu-id="a4c23-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4c23-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="a4c23-112">Usuwa regułę autoryzacji `SBAuthoRule1` obszaru nazw `SB-Example1` z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4c23-112">Removes the authorization rule `SBAuthoRule1` of namespace `SB-Example1` from the specified resource group.</span></span>

### <span data-ttu-id="a4c23-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a4c23-113">Example 2</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="a4c23-114">Usuwa regułę autoryzacji `SBAuthoRule1` kolejki `SBQueue` z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4c23-114">Removes the authorization rule `SBAuthoRule1` of queue `SBQueue` from the specified resource group.</span></span>

### <span data-ttu-id="a4c23-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a4c23-115">Example 3</span></span>
```
PS C:\> Remove-AzServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="a4c23-116">Usuwa zasadę autoryzacji `SBAuthoRule1` tematu `SBTopic` z określonej grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a4c23-116">Removes the authorization rule `SBAuthoRule1` of topic `SBTopic` from the specified resource group.</span></span>

## <span data-ttu-id="a4c23-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4c23-117">PARAMETERS</span></span>

### <span data-ttu-id="a4c23-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4c23-118">-DefaultProfile</span></span>
<span data-ttu-id="a4c23-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4c23-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4c23-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a4c23-120">-Force</span></span>
<span data-ttu-id="a4c23-121">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a4c23-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a4c23-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="a4c23-122">-InputObject</span></span>
<span data-ttu-id="a4c23-123">Obiekt AuthorizationRule ServiceBus</span><span class="sxs-lookup"><span data-stu-id="a4c23-123">ServiceBus AuthorizationRule Object</span></span>

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

### <span data-ttu-id="a4c23-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a4c23-124">-Name</span></span>
<span data-ttu-id="a4c23-125">Nazwa AuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a4c23-125">AuthorizationRule Name</span></span>

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

### <span data-ttu-id="a4c23-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a4c23-126">-Namespace</span></span>
<span data-ttu-id="a4c23-127">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="a4c23-127">Namespace Name</span></span>

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

### <span data-ttu-id="a4c23-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4c23-128">-PassThru</span></span>
<span data-ttu-id="a4c23-129">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="a4c23-129">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a4c23-130">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="a4c23-130">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a4c23-131">-Queue</span><span class="sxs-lookup"><span data-stu-id="a4c23-131">-Queue</span></span>
<span data-ttu-id="a4c23-132">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="a4c23-132">Queue Name</span></span>

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

### <span data-ttu-id="a4c23-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4c23-133">-ResourceGroupName</span></span>
<span data-ttu-id="a4c23-134">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a4c23-134">Resource Group Name</span></span>

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

### <span data-ttu-id="a4c23-135">— Temat</span><span class="sxs-lookup"><span data-stu-id="a4c23-135">-Topic</span></span>
<span data-ttu-id="a4c23-136">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="a4c23-136">Topic Name</span></span>

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

### <span data-ttu-id="a4c23-137">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4c23-137">-Confirm</span></span>
<span data-ttu-id="a4c23-138">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4c23-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4c23-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4c23-139">-WhatIf</span></span>
<span data-ttu-id="a4c23-140">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4c23-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4c23-141">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a4c23-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4c23-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4c23-142">CommonParameters</span></span>
<span data-ttu-id="a4c23-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4c23-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4c23-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4c23-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4c23-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4c23-145">INPUTS</span></span>

### <span data-ttu-id="a4c23-146">System. String</span><span class="sxs-lookup"><span data-stu-id="a4c23-146">System.String</span></span>

### <span data-ttu-id="a4c23-147">Microsoft. Azure. Commands. ServiceBus. models. PSSharedAccessAuthorizationRuleAttributes</span><span class="sxs-lookup"><span data-stu-id="a4c23-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSharedAccessAuthorizationRuleAttributes</span></span>

## <span data-ttu-id="a4c23-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4c23-148">OUTPUTS</span></span>

### <span data-ttu-id="a4c23-149">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a4c23-149">System.Boolean</span></span>

## <span data-ttu-id="a4c23-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4c23-150">NOTES</span></span>

## <span data-ttu-id="a4c23-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4c23-151">RELATED LINKS</span></span>
