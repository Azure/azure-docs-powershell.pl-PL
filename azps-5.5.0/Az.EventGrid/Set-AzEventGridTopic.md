---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/set-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/Set-AzEventGridTopic.md
ms.openlocfilehash: 6a6b373fcbe38aac7e4e8d3972206955942eb18e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237920"
---
# <span data-ttu-id="c7e29-101">Set-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="c7e29-101">Set-AzEventGridTopic</span></span>

## <span data-ttu-id="c7e29-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7e29-102">SYNOPSIS</span></span>
<span data-ttu-id="c7e29-103">Ustawia właściwości tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c7e29-103">Sets the properties of an Event Grid topic.</span></span>

## <span data-ttu-id="c7e29-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c7e29-104">SYNTAX</span></span>

### <span data-ttu-id="c7e29-105">TopicNameParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c7e29-105">TopicNameParameterSet (Default)</span></span>
```
Set-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Tag] <Hashtable>
 [-InboundIpRule] <Hashtable> [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c7e29-106">ResourceIdEventSubscriptionParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7e29-106">ResourceIdEventSubscriptionParameterSet</span></span>
```
Set-AzEventGridTopic [-ResourceId] <String> [-Tag] <Hashtable> [-InboundIpRule] <Hashtable>
 [-PublicNetworkAccess] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c7e29-107">TopicInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c7e29-107">TopicInputObjectParameterSet</span></span>
```
Set-AzEventGridTopic [-InputObject] <PSTopic> [[-Tag] <Hashtable>] [[-InboundIpRule] <Hashtable>]
 [[-PublicNetworkAccess] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c7e29-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c7e29-108">DESCRIPTION</span></span>
<span data-ttu-id="c7e29-109">Ustawia właściwości tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c7e29-109">Sets the properties of an Event Grid topic.</span></span> <span data-ttu-id="c7e29-110">Za jego pomocą można zamienić tagi tematu siatki zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="c7e29-110">This can be used to replace the tags of an Event Grid topic.</span></span>

## <span data-ttu-id="c7e29-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c7e29-111">EXAMPLES</span></span>

### <span data-ttu-id="c7e29-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c7e29-112">Example 1</span></span>
```powershell
PS C:\> Set-AzEventGridTopic -ResourceGroup MyResourceGroupName -Name Topic1 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="c7e29-113">Ustawia właściwości tematu Siatka zdarzeń ( Temat1) w grupie zasobów Nazwa_grupy zasobów w celu zastąpienia tagów określonymi tagami \` \` \` \` "Dział" i "Środowisko".</span><span class="sxs-lookup"><span data-stu-id="c7e29-113">Sets the properties of the Event Grid topic \`Topic1\` in resource group \`MyResourceGroupName\` to replace the tags with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="c7e29-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c7e29-114">PARAMETERS</span></span>

### <span data-ttu-id="c7e29-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7e29-115">-DefaultProfile</span></span>
<span data-ttu-id="c7e29-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="c7e29-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7e29-117">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="c7e29-117">-InboundIpRule</span></span>
<span data-ttu-id="c7e29-118">Tabela skrótów reprezentująca listę reguł ip ruchu przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="c7e29-118">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="c7e29-119">Każda reguła określa adres IP w notacji CIDR, na przykład 10.0.0.0/8, wraz z odpowiadającą mu akcją do wykonania na podstawie dopasowania lub bez dopasowania maski IpMask.</span><span class="sxs-lookup"><span data-stu-id="c7e29-119">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="c7e29-120">Możliwe wartości akcji obejmują tylko zezwalanie</span><span class="sxs-lookup"><span data-stu-id="c7e29-120">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="c7e29-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c7e29-121">-InputObject</span></span>
<span data-ttu-id="c7e29-122">Obiekt tematu aplikacji EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c7e29-122">EventGrid Topic object.</span></span>

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

### <span data-ttu-id="c7e29-123">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="c7e29-123">-Name</span></span>
<span data-ttu-id="c7e29-124">Nazwa tematu w aplikacji EventGrid.</span><span class="sxs-lookup"><span data-stu-id="c7e29-124">EventGrid Topic Name.</span></span>

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

### <span data-ttu-id="c7e29-125">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="c7e29-125">-PublicNetworkAccess</span></span>
<span data-ttu-id="c7e29-126">Pozwala to określić, czy ruch jest dozwolony za pośrednictwem sieci publicznej.</span><span class="sxs-lookup"><span data-stu-id="c7e29-126">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="c7e29-127">Domyślnie jest ona włączona.</span><span class="sxs-lookup"><span data-stu-id="c7e29-127">By default it is enabled.</span></span> <span data-ttu-id="c7e29-128">Możesz dodatkowo ograniczyć się do określonych wiadomości IP, konfigurując parametry przychodzącej pocztyiprule.</span><span class="sxs-lookup"><span data-stu-id="c7e29-128">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="c7e29-129">Dozwolone wartości są wyłączone i włączone.</span><span class="sxs-lookup"><span data-stu-id="c7e29-129">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="c7e29-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7e29-130">-ResourceGroupName</span></span>
<span data-ttu-id="c7e29-131">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c7e29-131">Resource Group Name.</span></span>

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

### <span data-ttu-id="c7e29-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c7e29-132">-ResourceId</span></span>
<span data-ttu-id="c7e29-133">EventGrid Topic ResourceID.</span><span class="sxs-lookup"><span data-stu-id="c7e29-133">EventGrid Topic ResourceID.</span></span>

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

### <span data-ttu-id="c7e29-134">— Tag</span><span class="sxs-lookup"><span data-stu-id="c7e29-134">-Tag</span></span>
<span data-ttu-id="c7e29-135">Skróty reprezentujące tag zasobu.</span><span class="sxs-lookup"><span data-stu-id="c7e29-135">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="c7e29-136">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c7e29-136">-Confirm</span></span>
<span data-ttu-id="c7e29-137">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c7e29-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c7e29-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c7e29-138">-WhatIf</span></span>
<span data-ttu-id="c7e29-139">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c7e29-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c7e29-140">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c7e29-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c7e29-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7e29-141">CommonParameters</span></span>
<span data-ttu-id="c7e29-142">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7e29-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7e29-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c7e29-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7e29-144">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c7e29-144">INPUTS</span></span>

### <span data-ttu-id="c7e29-145">System.String</span><span class="sxs-lookup"><span data-stu-id="c7e29-145">System.String</span></span>

### <span data-ttu-id="c7e29-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="c7e29-146">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

### <span data-ttu-id="c7e29-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="c7e29-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="c7e29-148">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="c7e29-148">OUTPUTS</span></span>

### <span data-ttu-id="c7e29-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="c7e29-149">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="c7e29-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c7e29-150">NOTES</span></span>

## <span data-ttu-id="c7e29-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c7e29-151">RELATED LINKS</span></span>
