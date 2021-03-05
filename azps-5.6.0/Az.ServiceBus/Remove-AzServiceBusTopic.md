---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 445108b2413673e2ce48dcbfac9f3fa0cdb45982
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993350"
---
# <span data-ttu-id="902ed-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="902ed-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="902ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="902ed-102">SYNOPSIS</span></span>
<span data-ttu-id="902ed-103">Usuwa temat z określonej przestrzeni nazw autobusu usług.</span><span class="sxs-lookup"><span data-stu-id="902ed-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="902ed-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="902ed-104">SYNTAX</span></span>

### <span data-ttu-id="902ed-105">TopicPropertiesSet (Default)</span><span class="sxs-lookup"><span data-stu-id="902ed-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="902ed-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="902ed-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="902ed-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="902ed-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="902ed-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="902ed-108">DESCRIPTION</span></span>
<span data-ttu-id="902ed-109">Polecenie **cmdlet Remove-AzServiceBusTopic** usuwa temat z określonej przestrzeni nazw bus usługi.</span><span class="sxs-lookup"><span data-stu-id="902ed-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="902ed-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="902ed-110">EXAMPLES</span></span>

### <span data-ttu-id="902ed-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="902ed-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="902ed-112">Usuwa temat z `SB-Topic_exampl1` przestrzeni `SB-Example1` nazw.</span><span class="sxs-lookup"><span data-stu-id="902ed-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="902ed-113">Przykład 2. InputObject — używanie zmiennej:</span><span class="sxs-lookup"><span data-stu-id="902ed-113">Example 2: InputObject - Using Variable:</span></span>
```powershell
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="902ed-114">Przykład 3. InputObject — używanie funkcji rurowych:</span><span class="sxs-lookup"><span data-stu-id="902ed-114">Example 3: InputObject - Using Piping:</span></span>
```powershell
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="902ed-115">Przykład 4. Użycie zmiennej ResourceId:</span><span class="sxs-lookup"><span data-stu-id="902ed-115">Example 4: ResourceId Using Variable:</span></span>
```powershell
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="902ed-116">Przykład 5. Użycie wartości ciągu ResourceId</span><span class="sxs-lookup"><span data-stu-id="902ed-116">Example 5: ResourceId Using String value</span></span>
```powershell
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="902ed-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="902ed-117">PARAMETERS</span></span>

### <span data-ttu-id="902ed-118">— AsJob</span><span class="sxs-lookup"><span data-stu-id="902ed-118">-AsJob</span></span>
<span data-ttu-id="902ed-119">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="902ed-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="902ed-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="902ed-120">-DefaultProfile</span></span>
<span data-ttu-id="902ed-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="902ed-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="902ed-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="902ed-122">-InputObject</span></span>
<span data-ttu-id="902ed-123">Obiekt tematu w usłudze Service Bus</span><span class="sxs-lookup"><span data-stu-id="902ed-123">Service Bus Topic Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes
Parameter Sets: TopicInputObjectSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="902ed-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="902ed-124">-Name</span></span>
<span data-ttu-id="902ed-125">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="902ed-125">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902ed-126">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="902ed-126">-Namespace</span></span>
<span data-ttu-id="902ed-127">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="902ed-127">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902ed-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="902ed-128">-PassThru</span></span>
<span data-ttu-id="902ed-129">Określenie tej wartości spowoduje zwrócenie wartości prawda, jeśli polecenie zostało pomyślnie określone.</span><span class="sxs-lookup"><span data-stu-id="902ed-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="902ed-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="902ed-130">-ResourceGroupName</span></span>
<span data-ttu-id="902ed-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="902ed-131">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: TopicPropertiesSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902ed-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="902ed-132">-ResourceId</span></span>
<span data-ttu-id="902ed-133">Identyfikator zasobu tematu w usłudze Service Bus</span><span class="sxs-lookup"><span data-stu-id="902ed-133">Service Bus Topic Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: TopicResourceIdSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="902ed-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="902ed-134">-Confirm</span></span>
<span data-ttu-id="902ed-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="902ed-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="902ed-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="902ed-136">-WhatIf</span></span>
<span data-ttu-id="902ed-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="902ed-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="902ed-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="902ed-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="902ed-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="902ed-139">CommonParameters</span></span>
<span data-ttu-id="902ed-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="902ed-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="902ed-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="902ed-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="902ed-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="902ed-142">INPUTS</span></span>

### <span data-ttu-id="902ed-143">System.String</span><span class="sxs-lookup"><span data-stu-id="902ed-143">System.String</span></span>

### <span data-ttu-id="902ed-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="902ed-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="902ed-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="902ed-145">OUTPUTS</span></span>

### <span data-ttu-id="902ed-146">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="902ed-146">System.Boolean</span></span>

## <span data-ttu-id="902ed-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="902ed-147">NOTES</span></span>

## <span data-ttu-id="902ed-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="902ed-148">RELATED LINKS</span></span>
