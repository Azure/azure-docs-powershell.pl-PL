---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
ms.openlocfilehash: c93f0d8a44a67195d2c901dd581505276b7ae2f0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201627"
---
# <span data-ttu-id="4c0eb-101">Remove-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="4c0eb-101">Remove-AzServiceBusQueue</span></span>

## <span data-ttu-id="4c0eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4c0eb-102">SYNOPSIS</span></span>
<span data-ttu-id="4c0eb-103">Usuwa kolejkę z określonej przestrzeni nazw autobusu usług.</span><span class="sxs-lookup"><span data-stu-id="4c0eb-103">Removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="4c0eb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4c0eb-104">SYNTAX</span></span>

### <span data-ttu-id="4c0eb-105">QueuePropertiesSet (Default)</span><span class="sxs-lookup"><span data-stu-id="4c0eb-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c0eb-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4c0eb-106">QueueInputObjectSet</span></span>
```
Remove-AzServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4c0eb-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="4c0eb-107">QueueResourceIdSet</span></span>
```
Remove-AzServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4c0eb-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="4c0eb-108">DESCRIPTION</span></span>
<span data-ttu-id="4c0eb-109">Polecenie **cmdlet Remove-AzServiceBusQueue** usuwa kolejkę z określonej przestrzeni nazw autobusu usług.</span><span class="sxs-lookup"><span data-stu-id="4c0eb-109">The **Remove-AzServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="4c0eb-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4c0eb-110">EXAMPLES</span></span>

### <span data-ttu-id="4c0eb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4c0eb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="4c0eb-112">Usuwa kolejkę usługi bus `SB-Queue_exampl1` z przestrzeni `SB-Example1` nazw.</span><span class="sxs-lookup"><span data-stu-id="4c0eb-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="4c0eb-113">Przykład 2. InputObject — używanie zmiennej:</span><span class="sxs-lookup"><span data-stu-id="4c0eb-113">Example 2: InputObject - Using variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="4c0eb-114">Usuwa kolejkę service bus podaną w parametrze $inputobject -InputObject</span><span class="sxs-lookup"><span data-stu-id="4c0eb-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="4c0eb-115">Przykład 3. InputObject — używanie funkcji rurowych:</span><span class="sxs-lookup"><span data-stu-id="4c0eb-115">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>  Get-AzServiceBusQueue <params> | Remove-AzServiceBusQueue
```

### <span data-ttu-id="4c0eb-116">Przykład 4. ResourceId — używanie zmiennej:</span><span class="sxs-lookup"><span data-stu-id="4c0eb-116">Example 4: ResourceId - Using variable:</span></span>
```powershell
PS c:\> $resourceid = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="4c0eb-117">Usuwa kolejkę service bus podaną w identyfikatorze ARM w ciągu $resourceid/string dla parametru -ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c0eb-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="4c0eb-118">Przykład 5. ResourceId — przechodząc jako ciąg:</span><span class="sxs-lookup"><span data-stu-id="4c0eb-118">Example 5: ResourceId - passing as string:</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="4c0eb-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4c0eb-119">PARAMETERS</span></span>

### <span data-ttu-id="4c0eb-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="4c0eb-120">-AsJob</span></span>
<span data-ttu-id="4c0eb-121">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="4c0eb-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="4c0eb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4c0eb-122">-DefaultProfile</span></span>
<span data-ttu-id="4c0eb-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4c0eb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4c0eb-124">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4c0eb-124">-InputObject</span></span>
<span data-ttu-id="4c0eb-125">Obiekt kolejki autobusu usługowego</span><span class="sxs-lookup"><span data-stu-id="4c0eb-125">Service Bus Queue Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes
Parameter Sets: QueueInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0eb-126">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="4c0eb-126">-Name</span></span>
<span data-ttu-id="4c0eb-127">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="4c0eb-127">Queue Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0eb-128">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="4c0eb-128">-Namespace</span></span>
<span data-ttu-id="4c0eb-129">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="4c0eb-129">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0eb-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4c0eb-130">-PassThru</span></span>
<span data-ttu-id="4c0eb-131">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="4c0eb-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="4c0eb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4c0eb-132">-ResourceGroupName</span></span>
<span data-ttu-id="4c0eb-133">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4c0eb-133">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: QueuePropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0eb-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4c0eb-134">-ResourceId</span></span>
<span data-ttu-id="4c0eb-135">Identyfikator zasobu kolejki serwisowej</span><span class="sxs-lookup"><span data-stu-id="4c0eb-135">Service Bus Queue Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: QueueResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4c0eb-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4c0eb-136">-Confirm</span></span>
<span data-ttu-id="4c0eb-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4c0eb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4c0eb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4c0eb-138">-WhatIf</span></span>
<span data-ttu-id="4c0eb-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4c0eb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4c0eb-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4c0eb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4c0eb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4c0eb-141">CommonParameters</span></span>
<span data-ttu-id="4c0eb-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4c0eb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4c0eb-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4c0eb-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4c0eb-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c0eb-144">INPUTS</span></span>

### <span data-ttu-id="4c0eb-145">System.String</span><span class="sxs-lookup"><span data-stu-id="4c0eb-145">System.String</span></span>

### <span data-ttu-id="4c0eb-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="4c0eb-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="4c0eb-147">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4c0eb-147">OUTPUTS</span></span>

### <span data-ttu-id="4c0eb-148">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4c0eb-148">System.Boolean</span></span>

## <span data-ttu-id="4c0eb-149">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4c0eb-149">NOTES</span></span>

## <span data-ttu-id="4c0eb-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4c0eb-150">RELATED LINKS</span></span>
