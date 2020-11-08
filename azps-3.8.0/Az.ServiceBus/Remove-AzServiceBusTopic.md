---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/remove-azservicebustopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Remove-AzServiceBusTopic.md
ms.openlocfilehash: 7cf379bbe7c68ebe381e473aa617595dfe2060f8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050057"
---
# <span data-ttu-id="f801e-101">Remove-AzServiceBusTopic</span><span class="sxs-lookup"><span data-stu-id="f801e-101">Remove-AzServiceBusTopic</span></span>

## <span data-ttu-id="f801e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f801e-102">SYNOPSIS</span></span>
<span data-ttu-id="f801e-103">Usuwa temat z określonego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="f801e-103">Removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f801e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f801e-104">SYNTAX</span></span>

### <span data-ttu-id="f801e-105">TopicPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f801e-105">TopicPropertiesSet (Default)</span></span>
```
Remove-AzServiceBusTopic [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f801e-106">TopicInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="f801e-106">TopicInputObjectSet</span></span>
```
Remove-AzServiceBusTopic [-InputObject] <PSTopicAttributes> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f801e-107">TopicResourceIdSet</span><span class="sxs-lookup"><span data-stu-id="f801e-107">TopicResourceIdSet</span></span>
```
Remove-AzServiceBusTopic [-ResourceId] <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f801e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="f801e-108">DESCRIPTION</span></span>
<span data-ttu-id="f801e-109">Polecenie cmdlet **Remove-AzServiceBusTopic** usuwa temat z określonego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="f801e-109">The **Remove-AzServiceBusTopic** cmdlet removes the topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="f801e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f801e-110">EXAMPLES</span></span>

### <span data-ttu-id="f801e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f801e-111">Example 1</span></span>
```
PS C:\> Remove-AzServiceBusTopic -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1
```

<span data-ttu-id="f801e-112">Usuwa temat `SB-Topic_exampl1` z obszaru nazw `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="f801e-112">Removes the topic `SB-Topic_exampl1` from the namespace `SB-Example1`.</span></span>

### <span data-ttu-id="f801e-113">Przykład 2,1-wejście-przy użyciu zmiennej:</span><span class="sxs-lookup"><span data-stu-id="f801e-113">Example 2.1 - InputObject - Using Variable:</span></span>
```
PS C:\> $inputobject = Get-AzServiceBusTopic <parmas>
PS C:\> Remove-AzServiceBusTopic -InputObject $inputobject
```

### <span data-ttu-id="f801e-114">Przykład 2,2-Inputobject-przy użyciu instalacji rurowej:</span><span class="sxs-lookup"><span data-stu-id="f801e-114">Example 2.2 - InputObject - Using Piping:</span></span>
```
PS C:\> Get-AzServiceBusTopic <parmas> | Remove-AzServiceBusTopic
```

### <span data-ttu-id="f801e-115">Przykład 3,1-ResourceId przy użyciu zmiennej:</span><span class="sxs-lookup"><span data-stu-id="f801e-115">Example 3.1 - ResourceId Using Variable:</span></span>
```
PS C:\> $resourceid = Get-AzServiceBusTopic <params>
PS C:\> Remove-AzServiceBusTopic -ResourceId $resourceid.Id
```

### <span data-ttu-id="f801e-116">Przykład 3,2-ResourceId przy użyciu wartości ciągu</span><span class="sxs-lookup"><span data-stu-id="f801e-116">Example 3.2 - ResourceId Using String value</span></span>
```
PS C:\> Remove-AzServiceBusTopic -ResourceId "/subscriptions/xxxx-xxxxx-xxxxxx-xxxxx/resourceGroups/ResourceGroupName/providers/Microsoft.ServiceBus/namespaces/NamespaceName/topics/TopicName"
```

## <span data-ttu-id="f801e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f801e-117">PARAMETERS</span></span>

### <span data-ttu-id="f801e-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f801e-118">-AsJob</span></span>
<span data-ttu-id="f801e-119">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="f801e-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f801e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f801e-120">-DefaultProfile</span></span>
<span data-ttu-id="f801e-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f801e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f801e-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f801e-122">-InputObject</span></span>
<span data-ttu-id="f801e-123">Obiekt temat magistrali usług</span><span class="sxs-lookup"><span data-stu-id="f801e-123">Service Bus Topic Object</span></span>

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

### <span data-ttu-id="f801e-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f801e-124">-Name</span></span>
<span data-ttu-id="f801e-125">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="f801e-125">Topic Name</span></span>

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

### <span data-ttu-id="f801e-126">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f801e-126">-Namespace</span></span>
<span data-ttu-id="f801e-127">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="f801e-127">Namespace Name</span></span>

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

### <span data-ttu-id="f801e-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f801e-128">-PassThru</span></span>
<span data-ttu-id="f801e-129">Określenie tej wartości zwróci wartość PRAWDA, jeśli polecenie zostało wykonane prawidłowo.</span><span class="sxs-lookup"><span data-stu-id="f801e-129">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="f801e-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f801e-130">-ResourceGroupName</span></span>
<span data-ttu-id="f801e-131">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f801e-131">The name of the resource group</span></span>

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

### <span data-ttu-id="f801e-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f801e-132">-ResourceId</span></span>
<span data-ttu-id="f801e-133">Identyfikator zasobu tematu magistrali usług</span><span class="sxs-lookup"><span data-stu-id="f801e-133">Service Bus Topic Resource Id</span></span>

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

### <span data-ttu-id="f801e-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f801e-134">-Confirm</span></span>
<span data-ttu-id="f801e-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f801e-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f801e-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f801e-136">-WhatIf</span></span>
<span data-ttu-id="f801e-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f801e-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f801e-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f801e-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f801e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f801e-139">CommonParameters</span></span>
<span data-ttu-id="f801e-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f801e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f801e-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f801e-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f801e-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f801e-142">INPUTS</span></span>

### <span data-ttu-id="f801e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="f801e-143">System.String</span></span>

### <span data-ttu-id="f801e-144">Microsoft. Azure. Commands. ServiceBus. models. PSTopicAttributes</span><span class="sxs-lookup"><span data-stu-id="f801e-144">Microsoft.Azure.Commands.ServiceBus.Models.PSTopicAttributes</span></span>

## <span data-ttu-id="f801e-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f801e-145">OUTPUTS</span></span>

### <span data-ttu-id="f801e-146">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f801e-146">System.Boolean</span></span>

## <span data-ttu-id="f801e-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f801e-147">NOTES</span></span>

## <span data-ttu-id="f801e-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f801e-148">RELATED LINKS</span></span>
