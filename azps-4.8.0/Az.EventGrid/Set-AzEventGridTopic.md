---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: 6a6b373fcbe38aac7e4e8d3972206955942eb18e
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223942"
---
# <span data-ttu-id="76eeb-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="76eeb-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="76eeb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76eeb-102">SYNOPSIS</span></span>
<span data-ttu-id="76eeb-103">Ustawia właściwości tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="76eeb-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="76eeb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76eeb-104">SYNTAX</span></span>

### <span data-ttu-id="76eeb-105">TopicNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="76eeb-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-InboundIpRule] <Hashtable> [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76eeb-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="76eeb-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-InboundIpRule] <Hashtable>
 [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76eeb-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76eeb-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [[-InboundIpRule] <Hashtable>]
 [[-PublicNetworkAccess] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="76eeb-108">Opis</span><span class="sxs-lookup"><span data-stu-id="76eeb-108">DESCRIPTION</span></span>
<span data-ttu-id="76eeb-109">Ustawia właściwości tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="76eeb-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="76eeb-110">Za pomocą tej funkcji można zastępować znaczniki tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="76eeb-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="76eeb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76eeb-111">EXAMPLES</span></span>

### <span data-ttu-id="76eeb-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="76eeb-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="76eeb-113">Ustawia właściwości tematu siatki zdarzeń \` Temat1 \` w MyResourceGroupName grupy zasobów, \` \` Aby zamienić Tagi na określone znaczniki "Department" i "Environment".</span><span class="sxs-lookup"><span data-stu-id="76eeb-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="76eeb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76eeb-114">PARAMETERS</span></span>

### <span data-ttu-id="76eeb-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76eeb-115">-DefaultProfile</span></span>
<span data-ttu-id="76eeb-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="76eeb-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="76eeb-117">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="76eeb-117">-InboundIpRule</span></span>
<span data-ttu-id="76eeb-118">Obiekt Hashtable reprezentujący listę reguł przychodzącego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="76eeb-118">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="76eeb-119">Każda reguła określa adres IP w notacji CIDR, na przykład 10.0.0.0/8, wraz z odpowiednią akcją, którą należy wykonać na podstawie dopasowania lub braku dopasowania IpMask.</span><span class="sxs-lookup"><span data-stu-id="76eeb-119">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="76eeb-120">Możliwe wartości akcji obejmują tylko dozwolone</span><span class="sxs-lookup"><span data-stu-id="76eeb-120">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76eeb-121">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="76eeb-121">-InputObject</span></span>
<span data-ttu-id="76eeb-122">Obiekt tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="76eeb-122">EventGrid Topic object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventGrid.Models.PSTopic
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76eeb-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="76eeb-123">-Name</span></span>
<span data-ttu-id="76eeb-124">Nazwa tematu EventGrid.</span><span class="sxs-lookup"><span data-stu-id="76eeb-124">EventGrid Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76eeb-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="76eeb-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="76eeb-126">Określa, czy ruch jest dozwolony w sieci publicznej.</span><span class="sxs-lookup"><span data-stu-id="76eeb-126">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="76eeb-127">Domyślnie jest on włączony.</span><span class="sxs-lookup"><span data-stu-id="76eeb-127">By default it is enabled.</span></span> <span data-ttu-id="76eeb-128">Możesz dodatkowo ograniczyć do określonych adresów IP, konfigurując parametry InboundIpRule.</span><span class="sxs-lookup"><span data-stu-id="76eeb-128">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="76eeb-129">Dozwolone wartości są wyłączone i włączone.</span><span class="sxs-lookup"><span data-stu-id="76eeb-129">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:
Accepted values: enabled, disabled

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: TopicInputObjectParameterSet
Aliases:
Accepted values: enabled, disabled

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76eeb-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76eeb-130">-ResourceGroupName</span></span>
<span data-ttu-id="76eeb-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="76eeb-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicNameParameterSet
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76eeb-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76eeb-132">-ResourceId</span></span>
<span data-ttu-id="76eeb-133">EventGrid temat ResourceID.</span><span class="sxs-lookup"><span data-stu-id="76eeb-133">EventGrid Topic ResourceID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76eeb-134">-Tag</span><span class="sxs-lookup"><span data-stu-id="76eeb-134">-Tag</span></span>
<span data-ttu-id="76eeb-135">Hashtable, które reprezentują znacznik zasobu.</span><span class="sxs-lookup"><span data-stu-id="76eeb-135">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicNameParameterSet, ResourceIdEventSubscriptionParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: TopicInputObjectParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76eeb-136">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="76eeb-136">-Confirm</span></span>
<span data-ttu-id="76eeb-137">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76eeb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76eeb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76eeb-138">-WhatIf</span></span>
<span data-ttu-id="76eeb-139">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="76eeb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76eeb-140">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="76eeb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76eeb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76eeb-141">CommonParameters</span></span>
<span data-ttu-id="76eeb-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76eeb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76eeb-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="76eeb-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76eeb-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76eeb-144">INPUTS</span></span>

### <span data-ttu-id="76eeb-145">System. String</span><span class="sxs-lookup"><span data-stu-id="76eeb-145">System.String</span></span>

### <span data-ttu-id="76eeb-146">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="76eeb-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="76eeb-147">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="76eeb-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="76eeb-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76eeb-148">OUTPUTS</span></span>

### <span data-ttu-id="76eeb-149">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="76eeb-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="76eeb-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76eeb-150">NOTES</span></span>

## <span data-ttu-id="76eeb-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76eeb-151">RELATED LINKS</span></span>
