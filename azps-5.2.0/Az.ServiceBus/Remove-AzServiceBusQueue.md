---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusQueue.md
ms.openlocfilehash: c93f0d8a44a67195d2c901dd581505276b7ae2f0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98331054"
---
# <span data-ttu-id="37dbb-101">Remove-AzServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="37dbb-101">Remove-AzServiceBusQueue</span></span>

## <span data-ttu-id="37dbb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="37dbb-102">SYNOPSIS</span></span>
<span data-ttu-id="37dbb-103">Usuwa kolejkę z określonego obszaru nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="37dbb-103">Removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="37dbb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="37dbb-104">SYNTAX</span></span>

### <span data-ttu-id="37dbb-105">QueuePropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="37dbb-105">QueuePropertiesSet (Default)</span></span>
```
Remove-AzServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37dbb-106">QueueInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="37dbb-106">QueueInputObjectSet</span></span>
```
Remove-AzServiceBusQueue [-InputObject] <PSQueueAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="37dbb-107">QueueResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="37dbb-107">QueueResourceIdSet</span></span>
```
Remove-AzServiceBusQueue [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="37dbb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="37dbb-108">DESCRIPTION</span></span>
<span data-ttu-id="37dbb-109">Polecenie cmdlet **Remove-AzServiceBusQueue** Usuwa kolejkę z określonego obszaru nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="37dbb-109">The **Remove-AzServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="37dbb-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="37dbb-110">EXAMPLES</span></span>

### <span data-ttu-id="37dbb-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="37dbb-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="37dbb-112">Usuwa kolejkę usługi Service Bus `SB-Queue_exampl1` z obszaru nazw `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="37dbb-112">Removes the Service Bus queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="37dbb-113">Przykład 2: wejście-przy użyciu zmiennej:</span><span class="sxs-lookup"><span data-stu-id="37dbb-113">Example 2: InputObject - Using variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -InputObject $inputobject
```

<span data-ttu-id="37dbb-114">Usuwa kolejkę usługi Service Bus określoną w parametrze $inputobject for Inputobject</span><span class="sxs-lookup"><span data-stu-id="37dbb-114">Removes the Service Bus queue provided in the $inputobject for -InputObject parameter</span></span>

### <span data-ttu-id="37dbb-115">Przykład 3: wejście-korzystanie z połączeń rurowych:</span><span class="sxs-lookup"><span data-stu-id="37dbb-115">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\>  Get-AzServiceBusQueue <params> | Remove-AzServiceBusQueue
```

### <span data-ttu-id="37dbb-116">Przykład 4: Identyfikator ResourceId używający zmiennej:</span><span class="sxs-lookup"><span data-stu-id="37dbb-116">Example 4: ResourceId - Using variable:</span></span>
```powershell
PS c:\> $resourceid = Get-AzServiceBusQueue <params>
PS C:\> Remove-AzServiceBusQueue -ResourceId $resourceid.Id
```

<span data-ttu-id="37dbb-117">Usuwa kolejkę usługi Service Bus określoną w polu Identyfikator ARM w $resourceid parametr/String dla-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37dbb-117">Removes the Service Bus queue provided in the ARM id in $resourceid/string for -ResourceId parameter</span></span>

### <span data-ttu-id="37dbb-118">Przykład 5: ResourceId-przekazanie jako ciąg:</span><span class="sxs-lookup"><span data-stu-id="37dbb-118">Example 5: ResourceId - passing as string:</span></span>
```powershell
PS C:\> Remove-AzServiceBusQueue -ResourceId "/subscriptions/xxxx-xxxxx-xxxxx-xxxxxx-xxxxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/queues/QueueName"
```

## <span data-ttu-id="37dbb-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="37dbb-119">PARAMETERS</span></span>

### <span data-ttu-id="37dbb-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="37dbb-120">-AsJob</span></span>
<span data-ttu-id="37dbb-121">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="37dbb-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="37dbb-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37dbb-122">-DefaultProfile</span></span>
<span data-ttu-id="37dbb-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="37dbb-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="37dbb-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="37dbb-124">-InputObject</span></span>
<span data-ttu-id="37dbb-125">Obiekt kolejki usługi Service Bus</span><span class="sxs-lookup"><span data-stu-id="37dbb-125">Service Bus Queue Object</span></span>

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

### <span data-ttu-id="37dbb-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="37dbb-126">-Name</span></span>
<span data-ttu-id="37dbb-127">Nazwa kolejki</span><span class="sxs-lookup"><span data-stu-id="37dbb-127">Queue Name</span></span>

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

### <span data-ttu-id="37dbb-128">-Namespace</span><span class="sxs-lookup"><span data-stu-id="37dbb-128">-Namespace</span></span>
<span data-ttu-id="37dbb-129">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="37dbb-129">Namespace Name</span></span>

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

### <span data-ttu-id="37dbb-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="37dbb-130">-PassThru</span></span>
<span data-ttu-id="37dbb-131">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="37dbb-131">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="37dbb-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="37dbb-132">-ResourceGroupName</span></span>
<span data-ttu-id="37dbb-133">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="37dbb-133">The name of the resource group</span></span>

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

### <span data-ttu-id="37dbb-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="37dbb-134">-ResourceId</span></span>
<span data-ttu-id="37dbb-135">Identyfikator zasobu kolejki usługi Service Bus</span><span class="sxs-lookup"><span data-stu-id="37dbb-135">Service Bus Queue Resource Id</span></span>

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

### <span data-ttu-id="37dbb-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="37dbb-136">-Confirm</span></span>
<span data-ttu-id="37dbb-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37dbb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="37dbb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="37dbb-138">-WhatIf</span></span>
<span data-ttu-id="37dbb-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="37dbb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="37dbb-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="37dbb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="37dbb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37dbb-141">CommonParameters</span></span>
<span data-ttu-id="37dbb-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37dbb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37dbb-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37dbb-143">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37dbb-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="37dbb-144">INPUTS</span></span>

### <span data-ttu-id="37dbb-145">System. String</span><span class="sxs-lookup"><span data-stu-id="37dbb-145">System.String</span></span>

### <span data-ttu-id="37dbb-146">Microsoft. Azure. Commands. ServiceBus. models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="37dbb-146">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="37dbb-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="37dbb-147">OUTPUTS</span></span>

### <span data-ttu-id="37dbb-148">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="37dbb-148">System.Boolean</span></span>

## <span data-ttu-id="37dbb-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="37dbb-149">NOTES</span></span>

## <span data-ttu-id="37dbb-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="37dbb-150">RELATED LINKS</span></span>
