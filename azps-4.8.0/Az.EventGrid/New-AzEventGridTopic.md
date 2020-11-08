---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 402d781c32b98362d504dd5167024932d82e64fb
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223958"
---
# <span data-ttu-id="f7652-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="f7652-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="f7652-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f7652-102">SYNOPSIS</span></span>
<span data-ttu-id="f7652-103">Tworzy nowy temat siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f7652-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="f7652-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f7652-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f7652-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f7652-105">DESCRIPTION</span></span>
<span data-ttu-id="f7652-106">Tworzy nowy temat siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="f7652-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="f7652-107">Po utworzeniu tematu aplikacja może publikować zdarzenia w punkcie końcowym tematu.</span><span class="sxs-lookup"><span data-stu-id="f7652-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="f7652-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f7652-108">EXAMPLES</span></span>

### <span data-ttu-id="f7652-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f7652-109">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="f7652-110">Tworzy temat \` Temat1 w siatce zdarzeń \` w podanej lokalizacji geograficznej \` westus2 \` , w MyResourceGroupName grup zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="f7652-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="f7652-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="f7652-111">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="f7652-112">Tworzy temat \` Temat1 w siatce zdarzeń \` w określonej lokalizacji geograficznej \` westus2 \` , w MyResourceGroupName grup zasobów \` \` z określonymi znacznikami "Department" i "Environment".</span><span class="sxs-lookup"><span data-stu-id="f7652-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="f7652-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f7652-113">PARAMETERS</span></span>

### <span data-ttu-id="f7652-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7652-114">-DefaultProfile</span></span>
<span data-ttu-id="f7652-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f7652-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7652-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="f7652-116">-InboundIpRule</span></span>
<span data-ttu-id="f7652-117">Obiekt Hashtable reprezentujący listę reguł przychodzącego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="f7652-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="f7652-118">Każda reguła określa adres IP w notacji CIDR, na przykład 10.0.0.0/8, wraz z odpowiednią akcją, którą należy wykonać na podstawie dopasowania lub braku dopasowania IpMask.</span><span class="sxs-lookup"><span data-stu-id="f7652-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="f7652-119">Możliwe wartości akcji obejmują tylko dozwolone</span><span class="sxs-lookup"><span data-stu-id="f7652-119">Possible Action values include Allow only</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7652-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="f7652-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="f7652-121">Obiekt Hashtable, który reprezentuje pola mapowania wejściowego z wartością domyślną w kluczu oddzielonym spacją = format wartości.</span><span class="sxs-lookup"><span data-stu-id="f7652-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="f7652-122">Dozwolone nazwy kluczy: subject, EventType i wersja.</span><span class="sxs-lookup"><span data-stu-id="f7652-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="f7652-123">Ta funkcja jest używana, gdy InputSchemaHelp jest customeventschema tylko.</span><span class="sxs-lookup"><span data-stu-id="f7652-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7652-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="f7652-124">-InputMappingField</span></span>
<span data-ttu-id="f7652-125">Obiekt Hashtable, który reprezentuje pola mapowania wejściowego w polu rozdzielany spacjami = format wartości.</span><span class="sxs-lookup"><span data-stu-id="f7652-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="f7652-126">Dozwolone nazwy kluczy: identyfikator, temat, EventTime, temat, typ zdarzenia i wersja data.</span><span class="sxs-lookup"><span data-stu-id="f7652-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="f7652-127">Ta funkcja jest używana, gdy InputSchemaHelp jest customeventschema tylko.</span><span class="sxs-lookup"><span data-stu-id="f7652-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7652-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="f7652-128">-InputSchema</span></span>
<span data-ttu-id="f7652-129">Schemat zdarzeń wejściowych dla tematu.</span><span class="sxs-lookup"><span data-stu-id="f7652-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="f7652-130">Dozwolone wartości to: eventgridschema, customeventschema lub cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="f7652-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="f7652-131">Wartość domyślna to eventgridschema.</span><span class="sxs-lookup"><span data-stu-id="f7652-131">Default value is eventgridschema.</span></span> <span data-ttu-id="f7652-132">Uwaga: Jeśli customeventschema jest określony, należy również podać parametry InputMappingField lub/i InputMappingDefaultValue.</span><span class="sxs-lookup"><span data-stu-id="f7652-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: EventGridSchema, CustomEventSchema, CloudEventSchemaV1_0

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7652-133">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="f7652-133">-Location</span></span>
<span data-ttu-id="f7652-134">Lokalizacja tematu</span><span class="sxs-lookup"><span data-stu-id="f7652-134">The location of the topic</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7652-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f7652-135">-Name</span></span>
<span data-ttu-id="f7652-136">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="f7652-136">The name of the topic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7652-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="f7652-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="f7652-138">Określa, czy ruch jest dozwolony w sieci publicznej.</span><span class="sxs-lookup"><span data-stu-id="f7652-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="f7652-139">Domyślnie jest on włączony.</span><span class="sxs-lookup"><span data-stu-id="f7652-139">By default it is enabled.</span></span> <span data-ttu-id="f7652-140">Możesz dodatkowo ograniczyć do określonych adresów IP, konfigurując parametry InboundIpRule.</span><span class="sxs-lookup"><span data-stu-id="f7652-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="f7652-141">Dozwolone wartości są wyłączone i włączone.</span><span class="sxs-lookup"><span data-stu-id="f7652-141">Allowed values are disabled and enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7652-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7652-142">-ResourceGroupName</span></span>
<span data-ttu-id="f7652-143">Grupa zasobów, w której ma zostać utworzony temat.</span><span class="sxs-lookup"><span data-stu-id="f7652-143">The resource group in which the topic should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7652-144">-Tag</span><span class="sxs-lookup"><span data-stu-id="f7652-144">-Tag</span></span>
<span data-ttu-id="f7652-145">Hashtable, które reprezentują znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="f7652-145">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7652-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f7652-146">-Confirm</span></span>
<span data-ttu-id="f7652-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7652-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7652-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7652-148">-WhatIf</span></span>
<span data-ttu-id="f7652-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f7652-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7652-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f7652-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7652-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7652-151">CommonParameters</span></span>
<span data-ttu-id="f7652-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7652-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7652-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7652-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7652-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f7652-154">INPUTS</span></span>

### <span data-ttu-id="f7652-155">System. String</span><span class="sxs-lookup"><span data-stu-id="f7652-155">System.String</span></span>

### <span data-ttu-id="f7652-156">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f7652-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f7652-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f7652-157">OUTPUTS</span></span>

### <span data-ttu-id="f7652-158">Microsoft. Azure. Commands. EventGrid. models. PSTopic</span><span class="sxs-lookup"><span data-stu-id="f7652-158">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="f7652-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f7652-159">NOTES</span></span>

## <span data-ttu-id="f7652-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f7652-160">RELATED LINKS</span></span>
