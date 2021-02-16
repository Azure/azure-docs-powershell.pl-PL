---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventGrid.dll-Help.xml
Module Name: Az.EventGrid
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventgrid/new-azeventgriddomain
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventGrid/EventGrid/help/New-AzEventGridDomain.md
ms.openlocfilehash: 6340db7446671660df08449529b6678cf79a2af9
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194410"
---
# <span data-ttu-id="032b9-101">New-AzEventGridDomain</span><span class="sxs-lookup"><span data-stu-id="032b9-101">New-AzEventGridDomain</span></span>

## <span data-ttu-id="032b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="032b9-102">SYNOPSIS</span></span>
<span data-ttu-id="032b9-103">Tworzy nową domenę siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="032b9-103">Creates a new Azure Event Grid Domain.</span></span>

## <span data-ttu-id="032b9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="032b9-104">SYNTAX</span></span>

```
New-AzEventGridDomain [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-InputSchema <String>] [-InputMappingField <Hashtable>] [-InputMappingDefaultValue <Hashtable>]
 [-InboundIpRule <Hashtable>] [-PublicNetworkAccess <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="032b9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="032b9-105">DESCRIPTION</span></span>
<span data-ttu-id="032b9-106">Tworzy nową domenę siatki zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="032b9-106">Creates a new Azure Event Grid Domain.</span></span> <span data-ttu-id="032b9-107">Po utworzeniu domeny aplikacja może publikować zdarzenia w punkcie końcowym tematu.</span><span class="sxs-lookup"><span data-stu-id="032b9-107">Once the domain is created, an application can publish events to the topic endpoint.</span></span>

## <span data-ttu-id="032b9-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="032b9-108">EXAMPLES</span></span>

### <span data-ttu-id="032b9-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="032b9-109">Example 1</span></span>

<span data-ttu-id="032b9-110">Tworzy domenę siatki zdarzeń (Domain1) w określonej lokalizacji geograficznej westus2 w grupie zasobów \` \` \` \` \` MyResourceGroupName (Nazwa_grupy \` zasobów).</span><span class="sxs-lookup"><span data-stu-id="032b9-110">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\`.</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              :
```

### <span data-ttu-id="032b9-111">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="032b9-111">Example 2</span></span>

<span data-ttu-id="032b9-112">Tworzy domenę siatki zdarzeń (Domain1) w określonej lokalizacji geograficznej westus2, w grupie zasobów MyResourceGroupName z określonymi tagami \` \` \` \` "Department" (Dział) i \` \` "Environment" (Środowisko).</span><span class="sxs-lookup"><span data-stu-id="032b9-112">Creates an Event Grid domain \`Domain1\` in the specified geographic location \`westus2\`, in resource group \`MyResourceGroupName\` with the specified tags "Department" and "Environment".</span></span>

```powershell
PS C:\> New-AzEventGridDomain -ResourceGroupName MyResourceGroupName -Name Domain1 -Location westus2 -Tag @{ Department="Finance"; Environment="Test" }

ResourceGroupName : MyResourceGroupName
DomainName        : Domain1
Id                : /subscriptions/<Azure Subscription Id>/resourceGroups/MyResourceGroupName/providers/Microsoft.EventGrid/domains/domain1
Type              : Microsoft.EventGrid/domains
Location          : westus2
Endpoint          : https://domain1.westus2-1.eventgrid.azure.net/api/events
ProvisioningState : Succeeded
Tags              : {[Department, Finance], [Environment, Test]}
```

## <span data-ttu-id="032b9-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="032b9-113">PARAMETERS</span></span>

### <span data-ttu-id="032b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="032b9-114">-DefaultProfile</span></span>
<span data-ttu-id="032b9-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="032b9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="032b9-116">-InboundIpRule</span><span class="sxs-lookup"><span data-stu-id="032b9-116">-InboundIpRule</span></span>
<span data-ttu-id="032b9-117">Tabela skrótów reprezentująca listę reguł ip ruchu przychodzącego.</span><span class="sxs-lookup"><span data-stu-id="032b9-117">Hashtable which represents list of inbound IP rules.</span></span> <span data-ttu-id="032b9-118">Każda reguła określa adres IP w notacji CIDR, na przykład 10.0.0.0/8, wraz z odpowiadającą mu akcją do wykonania na podstawie dopasowania lub bez dopasowania maski IpMask.</span><span class="sxs-lookup"><span data-stu-id="032b9-118">Each rule specifies the IP Address in CIDR notation e.g., 10.0.0.0/8 along with the corresponding Action to be performed based on the match or no match of the IpMask.</span></span> <span data-ttu-id="032b9-119">Możliwe wartości akcji obejmują tylko zezwalanie</span><span class="sxs-lookup"><span data-stu-id="032b9-119">Possible Action values include Allow only</span></span>

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

### <span data-ttu-id="032b9-120">-InputMappingDefaultValue</span><span class="sxs-lookup"><span data-stu-id="032b9-120">-InputMappingDefaultValue</span></span>
<span data-ttu-id="032b9-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span><span class="sxs-lookup"><span data-stu-id="032b9-121">Hashtable which represents the input mapping fields with default value in space separated key = value format.</span></span> <span data-ttu-id="032b9-122">Dozwolone nazwy kluczy to: temat, typ zdarzenia i dataversion.</span><span class="sxs-lookup"><span data-stu-id="032b9-122">Allowed key names are: subject, eventtype, and dataversion.</span></span> <span data-ttu-id="032b9-123">Jest to używane, gdy inputSchemaHelp jest tylko customeventschema.</span><span class="sxs-lookup"><span data-stu-id="032b9-123">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="032b9-124">-InputMappingField</span><span class="sxs-lookup"><span data-stu-id="032b9-124">-InputMappingField</span></span>
<span data-ttu-id="032b9-125">Tabela skrótów reprezentująca pola mapowania danych wejściowych w formacie klawiszy oddzielonych spacjami = format wartości.</span><span class="sxs-lookup"><span data-stu-id="032b9-125">Hashtable which represents the input mapping fields in space separated key = value format.</span></span> <span data-ttu-id="032b9-126">Dozwolone nazwy kluczy to: identyfikator, temat, czas zdarzenia, temat, typ zdarzenia i dataversion.</span><span class="sxs-lookup"><span data-stu-id="032b9-126">Allowed key names are: id, topic, eventtime, subject, eventtype, and dataversion.</span></span> <span data-ttu-id="032b9-127">Jest to używane, gdy inputSchemaHelp jest tylko customeventschema.</span><span class="sxs-lookup"><span data-stu-id="032b9-127">This is used when InputSchemaHelp is customeventschema only.</span></span>

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

### <span data-ttu-id="032b9-128">-InputSchema</span><span class="sxs-lookup"><span data-stu-id="032b9-128">-InputSchema</span></span>
<span data-ttu-id="032b9-129">Schemat zdarzeń wprowadzania dla tematu.</span><span class="sxs-lookup"><span data-stu-id="032b9-129">The schema of the input events for the topic.</span></span> <span data-ttu-id="032b9-130">Dozwolone wartości to: eventgridschema, customeventschema lub cloudeventv01Schema.</span><span class="sxs-lookup"><span data-stu-id="032b9-130">Allowed values are: eventgridschema, customeventschema, or cloudeventv01Schema.</span></span> <span data-ttu-id="032b9-131">Wartość domyślna to eventgridschema.</span><span class="sxs-lookup"><span data-stu-id="032b9-131">Default value is eventgridschema.</span></span> <span data-ttu-id="032b9-132">Zwróć uwagę, że jeśli zostanie określony parametr customeventschema, należy również określić parametry InputMappingField lub/i InputMappingDefaultValue.</span><span class="sxs-lookup"><span data-stu-id="032b9-132">Note that if customeventschema is specified, then InputMappingField or/and InputMappingDefaultValue parameters need to be specified as well.</span></span>

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

### <span data-ttu-id="032b9-133">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="032b9-133">-Location</span></span>
<span data-ttu-id="032b9-134">Lokalizacja domeny.</span><span class="sxs-lookup"><span data-stu-id="032b9-134">The location of the domain.</span></span>

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

### <span data-ttu-id="032b9-135">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="032b9-135">-Name</span></span>
<span data-ttu-id="032b9-136">Nazwa domeny EventGrid.</span><span class="sxs-lookup"><span data-stu-id="032b9-136">EventGrid domain name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DomainName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="032b9-137">-PublicNetworkAccess</span><span class="sxs-lookup"><span data-stu-id="032b9-137">-PublicNetworkAccess</span></span>
<span data-ttu-id="032b9-138">Pozwala to określić, czy ruch jest dozwolony za pośrednictwem sieci publicznej.</span><span class="sxs-lookup"><span data-stu-id="032b9-138">This determines if traffic is allowed over public network.</span></span> <span data-ttu-id="032b9-139">Domyślnie jest ona włączona.</span><span class="sxs-lookup"><span data-stu-id="032b9-139">By default it is enabled.</span></span> <span data-ttu-id="032b9-140">Możesz dodatkowo ograniczyć się do określonych wiadomości IP, konfigurując parametry przychodzącej pocztyiprule.</span><span class="sxs-lookup"><span data-stu-id="032b9-140">You can further restrict to specific IPs by configuring InboundIpRule parameters.</span></span> <span data-ttu-id="032b9-141">Dozwolone wartości są wyłączone i włączone.</span><span class="sxs-lookup"><span data-stu-id="032b9-141">Allowed values are disabled and enabled.</span></span>

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

### <span data-ttu-id="032b9-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="032b9-142">-ResourceGroupName</span></span>
<span data-ttu-id="032b9-143">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="032b9-143">The name of the resource group.</span></span>

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

### <span data-ttu-id="032b9-144">— Tag</span><span class="sxs-lookup"><span data-stu-id="032b9-144">-Tag</span></span>
<span data-ttu-id="032b9-145">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="032b9-145">Hashtable which represents resource Tags.</span></span>

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

### <span data-ttu-id="032b9-146">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="032b9-146">-Confirm</span></span>
<span data-ttu-id="032b9-147">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="032b9-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="032b9-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="032b9-148">-WhatIf</span></span>
<span data-ttu-id="032b9-149">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="032b9-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="032b9-150">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="032b9-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="032b9-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="032b9-151">CommonParameters</span></span>
<span data-ttu-id="032b9-152">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="032b9-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="032b9-153">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="032b9-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="032b9-154">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="032b9-154">INPUTS</span></span>

### <span data-ttu-id="032b9-155">System.String</span><span class="sxs-lookup"><span data-stu-id="032b9-155">System.String</span></span>

### <span data-ttu-id="032b9-156">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="032b9-156">System.Collections.Hashtable</span></span>

## <span data-ttu-id="032b9-157">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="032b9-157">OUTPUTS</span></span>

### <span data-ttu-id="032b9-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span><span class="sxs-lookup"><span data-stu-id="032b9-158">Microsoft.Azure.Commands.EventGrid.Models.PSDomain</span></span>

## <span data-ttu-id="032b9-159">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="032b9-159">NOTES</span></span>

## <span data-ttu-id="032b9-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="032b9-160">RELATED LINKS</span></span>
