---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgridtopic
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridTopic.md
ms.openlocfilehash: 402d781c32b98362d504dd5167024932d82e64fb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188498"
---
# <span data-ttu-id="b7073-101">New-AzEventGridTopic</span><span class="sxs-lookup"><span data-stu-id="b7073-101">New-AzEventGridTopic</span></span>

## <span data-ttu-id="b7073-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7073-102">SYNOPSIS</span></span>
<span data-ttu-id="b7073-103">Tworzy nowy temat siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b7073-103">Creates a new Azure Event Grid Topic.</span></span>

## <span data-ttu-id="b7073-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b7073-104">SYNTAX</span></span>

```
New-AzEventGridTopic [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7073-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b7073-105">DESCRIPTION</span></span>
<span data-ttu-id="b7073-106">Tworzy nowy temat siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b7073-106">Creates a new Azure Event Grid Topic.</span></span> <span data-ttu-id="b7073-107">Po utworzeniu tematu aplikacja może publikować zdarzenia w punkcie końcowym tematu.</span><span class="sxs-lookup"><span data-stu-id="b7073-107">Once the topic is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="b7073-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b7073-108">EXAMPLES</span></span>

### <span data-ttu-id="b7073-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b7073-109">Example 1</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2
```

<span data-ttu-id="b7073-110">Tworzy temat Siatki zdarzeń , temat1 w określonej lokalizacji geograficznej zachódus2, w grupie zasobów \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="b7073-110">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="b7073-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b7073-111">Example 2</span></span>
```powershell
PS C:\> New-AzEventGridTopic -ResourceGroupName MyResourceGroupName -Name Topic1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }
```

<span data-ttu-id="b7073-112">Tworzy temat Siatki zdarzeń , temat1 w określonej lokalizacji geograficznej zachódus2, w grupie zasobów Nazwa_grupy Zasobów o określonych tagach \` \` "Dział" i \` \` \` \` "Środowisko".</span><span class="sxs-lookup"><span data-stu-id="b7073-112">Creates an Event Grid topic \`Topic1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

## <span data-ttu-id="b7073-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7073-113">PARAMETERS</span></span>

### <span data-ttu-id="b7073-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7073-114">-DefaultProfile</span></span>
<span data-ttu-id="b7073-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b7073-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b7073-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="b7073-116">-InboundIpRule</span></span>
<span data-ttu-id="b7073-117">Tabela skrótów reprezentująca listę reguł ip ruchu przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="b7073-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="b7073-118">Każda reguła określa adres IP w notacji CIDR, na przykład 10.0.0.0/8, wraz z odpowiadającą mu akcją do wykonania na podstawie dopasowania lub nie dopasowań maski IpMask.</span><span class="sxs-lookup"><span data-stu-id="b7073-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="b7073-119">Możliwe wartości akcji obejmują tylko zezwalanie</span><span class="sxs-lookup"><span data-stu-id="b7073-119">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="b7073-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="b7073-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="b7073-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span><span class="sxs-lookup"><span data-stu-id="b7073-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="b7073-122">Dozwolone nazwy kluczy to: temat, typ zdarzenia i dataversion.</span><span class="sxs-lookup"><span data-stu-id="b7073-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="b7073-123">Jest to używane, gdy inputSchemaHelp jest tylko customeventschema.</span><span class="sxs-lookup"><span data-stu-id="b7073-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="b7073-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="b7073-124">-InputMappingField</span></span>
<span data-ttu-id="b7073-125">Tabela skrótów reprezentująca pola mapowania danych wejściowych w formacie klawiszy oddzielonych spacjami = format wartości.</span><span class="sxs-lookup"><span data-stu-id="b7073-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="b7073-126">Dozwolone nazwy kluczy to: identyfikator, temat, czas zdarzenia, temat, typ zdarzenia i dataversion.</span><span class="sxs-lookup"><span data-stu-id="b7073-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="b7073-127">Jest to używane, gdy inputSchemaHelp jest tylko customeventschema.</span><span class="sxs-lookup"><span data-stu-id="b7073-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="b7073-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="b7073-128">-InputSchema</span></span>
<span data-ttu-id="b7073-129">Schemat zdarzeń wprowadzania dla tematu.</span><span class="sxs-lookup"><span data-stu-id="b7073-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="b7073-130">Dozwolone wartości to: eventgridschema, customeventschema lub cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="b7073-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="b7073-131">Wartość domyślna to eventgridschema.</span><span class="sxs-lookup"><span data-stu-id="b7073-131">Default value is eventgridschema.</span></span> <span data-ttu-id="b7073-132">Zwróć uwagę, że jeśli zostanie określony parametr customeventschema, należy również określić parametry InputMappingField lub/i InputMappingDefaultValue.</span><span class="sxs-lookup"><span data-stu-id="b7073-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

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

### <span data-ttu-id="b7073-133">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="b7073-133">-Location</span></span>
<span data-ttu-id="b7073-134">Lokalizacja tematu</span><span class="sxs-lookup"><span data-stu-id="b7073-134">The location of the topic</span></span>

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

### <span data-ttu-id="b7073-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b7073-135">-Name</span></span>
<span data-ttu-id="b7073-136">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="b7073-136">The name of the topic.</span></span>

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

### <span data-ttu-id="b7073-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="b7073-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="b7073-138">Pozwala to określić, czy ruch jest dozwolony za pośrednictwem sieci publicznej.</span><span class="sxs-lookup"><span data-stu-id="b7073-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="b7073-139">Domyślnie jest ona włączona.</span><span class="sxs-lookup"><span data-stu-id="b7073-139">By default it is enabled.</span></span> <span data-ttu-id="b7073-140">Możesz dodatkowo ograniczyć się do określonych wiadomości IP, konfigurując parametry przychodzącej pocztyiprule.</span><span class="sxs-lookup"><span data-stu-id="b7073-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="b7073-141">Dozwolone wartości są wyłączone i włączone.</span><span class="sxs-lookup"><span data-stu-id="b7073-141">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="b7073-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7073-142">-ResourceGroupName</span></span>
<span data-ttu-id="b7073-143">Grupa zasobów, w której należy utworzyć temat.</span><span class="sxs-lookup"><span data-stu-id="b7073-143">The resource group in which the topic should be created.</span></span>

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

### <span data-ttu-id="b7073-144">— Tag</span><span class="sxs-lookup"><span data-stu-id="b7073-144">-Tag</span></span>
<span data-ttu-id="b7073-145">Skróty reprezentujące tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7073-145">Hashtables which represents resource Tags.</span></span>

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

### <span data-ttu-id="b7073-146">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b7073-146">-Confirm</span></span>
<span data-ttu-id="b7073-147">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b7073-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7073-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7073-148">-WhatIf</span></span>
<span data-ttu-id="b7073-149">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b7073-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7073-150">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b7073-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7073-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7073-151">CommonParameters</span></span>
<span data-ttu-id="b7073-152">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7073-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7073-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7073-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7073-154">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7073-154">INPUTS</span></span>

### <span data-ttu-id="b7073-155">System.String</span><span class="sxs-lookup"><span data-stu-id="b7073-155">System.String</span></span>

### <span data-ttu-id="b7073-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b7073-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b7073-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b7073-157">OUTPUTS</span></span>

### <span data-ttu-id="b7073-158">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span><span class="sxs-lookup"><span data-stu-id="b7073-158">Microsoft.Azure.Commands.EventGrid.Models.PSTopic</span></span>

## <span data-ttu-id="b7073-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b7073-159">NOTES</span></span>

## <span data-ttu-id="b7073-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7073-160">RELATED LINKS</span></span>
