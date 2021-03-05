---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusSubscription.md
ms.openlocfilehash: 1423c0c0c67b12b1cb2fcb6bf682d3ed60aae9c6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993357"
---
# <span data-ttu-id="1d1b3-101">Remove-AzServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="1d1b3-101">Remove-AzServiceBusSubscription</span></span>

## <span data-ttu-id="1d1b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d1b3-102">SYNOPSIS</span></span>
<span data-ttu-id="1d1b3-103">Usuwa subskrypcję do tematu z określonej przestrzeni nazw autobusu usług.</span><span class="sxs-lookup"><span data-stu-id="1d1b3-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="1d1b3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1d1b3-104">SYNTAX</span></span>

### <span data-ttu-id="1d1b3-105">SubscriptionPropertiesSet (Default)</span><span class="sxs-lookup"><span data-stu-id="1d1b3-105">SubscriptionPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1d1b3-106">SubscriptionInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="1d1b3-106">SubscriptionInputObjectSet</span></span>
```
Remove-AzServiceBusSubscription [-InputObject] <PSSubscriptionAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1d1b3-107">SubscriptionResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="1d1b3-107">SubscriptionResourceIdSet</span></span>
```
Remove-AzServiceBusSubscription [-ResourceId] <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d1b3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1d1b3-108">DESCRIPTION</span></span>
<span data-ttu-id="1d1b3-109">Polecenie **cmdlet Remove-AzServiceBusSubscription** usuwa subskrypcję do tematu z określonej przestrzeni nazw typu bus usługi.</span><span class="sxs-lookup"><span data-stu-id="1d1b3-109">The **Remove-AzServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="1d1b3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1d1b3-110">EXAMPLES</span></span>

### <span data-ttu-id="1d1b3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1d1b3-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="1d1b3-112">Usuwa subskrypcję do `SB-TopicSubscription-Example1` tematu w określonej przestrzeni nazw `SB-Topic_exampl1` autobusu `SB-Example1` usług.</span><span class="sxs-lookup"><span data-stu-id="1d1b3-112">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

### <span data-ttu-id="1d1b3-113">Przykład 2. InputObject — używanie zmiennej:</span><span class="sxs-lookup"><span data-stu-id="1d1b3-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -InputObject $inputobject
```

### <span data-ttu-id="1d1b3-114">Przykład 3. InputObject — używanie funkcji rurowych:</span><span class="sxs-lookup"><span data-stu-id="1d1b3-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>Get-AzServiceBusSubscription <params> |Remove-AzServiceBusSubscription
```

### <span data-ttu-id="1d1b3-115">Przykład 4. ResourceId — używanie zmiennej:</span><span class="sxs-lookup"><span data-stu-id="1d1b3-115">Example 4: ResourceId - Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusSubscription <params>
PS C:\> Remove-AzServiceBusSubscription -ResourceId $resourceid.Id
```

### <span data-ttu-id="1d1b3-116">Przykład 5. ResourceId — używanie wartości ciągu:</span><span class="sxs-lookup"><span data-stu-id="1d1b3-116">Example 5: ResourceId - Using string value:</span></span>
```powershell
PS C:\> Remove-AzServiceBusSubscription -ResourceId "/subscriptions/Subscriptionid/resourceGroups/ResourceGroup/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName/subscriptions/SubscriptionName"
```

<span data-ttu-id="1d1b3-117">Usuwa subskrypcję z identyfikatora ARM w ciągu $resourceid/string dla parametru -ResourceId.</span><span class="sxs-lookup"><span data-stu-id="1d1b3-117">Removes the subscription provided through ARM Id in $resourceid/string for -ResourceId parameter</span></span> 

## <span data-ttu-id="1d1b3-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1d1b3-118">PARAMETERS</span></span>

### <span data-ttu-id="1d1b3-119">— AsJob</span><span class="sxs-lookup"><span data-stu-id="1d1b3-119">-AsJob</span></span>
<span data-ttu-id="1d1b3-120">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="1d1b3-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1d1b3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d1b3-121">-DefaultProfile</span></span>
<span data-ttu-id="1d1b3-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d1b3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1d1b3-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1d1b3-123">-InputObject</span></span>
<span data-ttu-id="1d1b3-124">Obiekt subskrypcji usługi Service Bus</span><span class="sxs-lookup"><span data-stu-id="1d1b3-124">Service Bus Subscription Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes
Parameter Sets: SubscriptionInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1d1b3-125">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1d1b3-125">-Name</span></span>
<span data-ttu-id="1d1b3-126">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1d1b3-126">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d1b3-127">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="1d1b3-127">-Namespace</span></span>
<span data-ttu-id="1d1b3-128">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="1d1b3-128">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d1b3-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d1b3-129">-PassThru</span></span>
<span data-ttu-id="1d1b3-130">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="1d1b3-130">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="1d1b3-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d1b3-131">-ResourceGroupName</span></span>
<span data-ttu-id="1d1b3-132">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1d1b3-132">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d1b3-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1d1b3-133">-ResourceId</span></span>
<span data-ttu-id="1d1b3-134">Identyfikator zasobu subskrypcji usługi bus</span><span class="sxs-lookup"><span data-stu-id="1d1b3-134">Service Bus Subscription Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d1b3-135">— Temat</span><span class="sxs-lookup"><span data-stu-id="1d1b3-135">-Topic</span></span>
<span data-ttu-id="1d1b3-136">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="1d1b3-136">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d1b3-137">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1d1b3-137">-Confirm</span></span>
<span data-ttu-id="1d1b3-138">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1d1b3-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d1b3-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d1b3-139">-WhatIf</span></span>
<span data-ttu-id="1d1b3-140">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d1b3-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d1b3-141">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1d1b3-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d1b3-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d1b3-142">CommonParameters</span></span>
<span data-ttu-id="1d1b3-143">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d1b3-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d1b3-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d1b3-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d1b3-145">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d1b3-145">INPUTS</span></span>

### <span data-ttu-id="1d1b3-146">System.String</span><span class="sxs-lookup"><span data-stu-id="1d1b3-146">System.String</span></span>

### <span data-ttu-id="1d1b3-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span><span class="sxs-lookup"><span data-stu-id="1d1b3-147">Microsoft.Azure.Commands.ServiceBus.Models.PSSubscriptionAttributes</span></span>

## <span data-ttu-id="1d1b3-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d1b3-148">OUTPUTS</span></span>

### <span data-ttu-id="1d1b3-149">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1d1b3-149">System.Boolean</span></span>

## <span data-ttu-id="1d1b3-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1d1b3-150">NOTES</span></span>

## <span data-ttu-id="1d1b3-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d1b3-151">RELATED LINKS</span></span>
