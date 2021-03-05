---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/powershell/module/az.digitaltwins/new-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 3c59099a2e4440e2c92836ab02b8396b5fc3b207
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984943"
---
# <span data-ttu-id="c1245-101">New-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1245-101">New-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="c1245-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1245-102">SYNOPSIS</span></span>
<span data-ttu-id="c1245-103">Utwórz lub zaktualizuj punkt końcowy DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c1245-103">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="c1245-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c1245-104">SYNTAX</span></span>

### <span data-ttu-id="c1245-105">EventHub (domyślne)</span><span class="sxs-lookup"><span data-stu-id="c1245-105">EventHub (Default)</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -ConnectionStringPrimaryKey <String> -EndpointType <EndpointType> [-SubscriptionId <String>]
 [-ConnectionStringSecondaryKey <String>] [-DeadLetterSecret <String>]
 [-EndpointDescription <IDigitalTwinsEndpointResource>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c1245-106">EventGrid</span><span class="sxs-lookup"><span data-stu-id="c1245-106">EventGrid</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -AccessKey1 <String> -EndpointType <EndpointType> -TopicEndpoint <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="c1245-107">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c1245-107">ServiceBus</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -EndpointType <EndpointType> -PrimaryConnectionString <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="c1245-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="c1245-108">DESCRIPTION</span></span>
<span data-ttu-id="c1245-109">Utwórz lub zaktualizuj punkt końcowy DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c1245-109">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="c1245-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c1245-110">EXAMPLES</span></span>

### <span data-ttu-id="c1245-111">Przykład 1. Tworzenie bazy danych AzDigitalTwinsEndpoint dla aplikacji Eventhub</span><span class="sxs-lookup"><span data-stu-id="c1245-111">Example 1: Create an AzDigitalTwinsEndpoint for Eventhub</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventHubEndPoint  -EndpointType EventHub -ResourceGroupName youritemp -ResourceName youriDigitalTwins -connectionStringPrimaryKey 'Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=youriEventhubPolicy;SharedAccessKey=********;EntityPath=yourieventhub'

Name                  Type
----                  ----
youriEventHubEndPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="c1245-112">Tworzenie witryny AzDigitalTwinsEndpoint dla aplikacji Eventhub przez connectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="c1245-112">Create an AzDigitalTwinsEndpoint for Eventhub by connectionStringPrimaryKey</span></span>

### <span data-ttu-id="c1245-113">Przykład 2. Tworzenie witryny AzDigitalTwinsEndpoint dla aplikacji EventGrid</span><span class="sxs-lookup"><span data-stu-id="c1245-113">Example 2: Create an AzDigitalTwinsEndpoint for EventGrid</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventGridPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -TopicEndpoint 'https://yourieventgrid.eastus-1.eventgrid.azure.net/api/events' -AccessKey1 'xxxxxxxxx='

Name                  Type
----                  ----
youriEventGridPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="c1245-114">Tworzenie witryny AzDigitalTwinsEndpoint dla aplikacji Eventhub według programu TopicEndpoint i uzyskiwanie dostępu do kluczaKey1</span><span class="sxs-lookup"><span data-stu-id="c1245-114">Create an AzDigitalTwinsEndpoint for Eventhub by TopicEndpoint and accessKey1</span></span>

### <span data-ttu-id="c1245-115">Przykład 3. Tworzenie bazy danych AzDigitalTwinsEndpoint dla usługi ServiceBus</span><span class="sxs-lookup"><span data-stu-id="c1245-115">Example 3: Create an AzDigitalTwinsEndpoint for ServiceBus</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriServiceBusPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -PrimaryConnectionString "Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=******;SharedAccessKey=********;EntityPath=yourieventhub"

Name                  Type
----                  ----
youriServiceBusPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="c1245-116">Tworzenie punktu azDigitalTwinsEndpoint dla usługi ServicBus przez PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="c1245-116">Create an AzDigitalTwinsEndpoint for ServicBus by PrimaryConnectionString</span></span>

## <span data-ttu-id="c1245-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1245-117">PARAMETERS</span></span>

### <span data-ttu-id="c1245-118">-AccessKey1</span><span class="sxs-lookup"><span data-stu-id="c1245-118">-AccessKey1</span></span>
<span data-ttu-id="c1245-119">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c1245-119">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1245-120">— AsJob</span><span class="sxs-lookup"><span data-stu-id="c1245-120">-AsJob</span></span>
<span data-ttu-id="c1245-121">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="c1245-121">Run the command as a job</span></span>

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

### <span data-ttu-id="c1245-122">-ConnectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="c1245-122">-ConnectionStringPrimaryKey</span></span>
<span data-ttu-id="c1245-123">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c1245-123">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1245-124">-ConnectionStringSecondaryKey</span><span class="sxs-lookup"><span data-stu-id="c1245-124">-ConnectionStringSecondaryKey</span></span>
<span data-ttu-id="c1245-125">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c1245-125">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventHub
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1245-126">-DeadLetterSecret</span><span class="sxs-lookup"><span data-stu-id="c1245-126">-DeadLetterSecret</span></span>
<span data-ttu-id="c1245-127">Tajny magazyn listów traconych.</span><span class="sxs-lookup"><span data-stu-id="c1245-127">Dead letter storage secret.</span></span>
<span data-ttu-id="c1245-128">Podczas czytania zostanie on obmyty.</span><span class="sxs-lookup"><span data-stu-id="c1245-128">Will be obfuscated during read.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1245-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1245-129">-DefaultProfile</span></span>
<span data-ttu-id="c1245-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c1245-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1245-131">-EndpointDescription</span><span class="sxs-lookup"><span data-stu-id="c1245-131">-EndpointDescription</span></span>
<span data-ttu-id="c1245-132">Zasób punktu końcowego DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c1245-132">DigitalTwinsInstance endpoint resource.</span></span>
<span data-ttu-id="c1245-133">Aby skonstruować, zobacz sekcję NOTATKI, aby uzyskać informacje o właściwościach parametru ENDPOINTDESCRIPTION i utworzyć tabelę skrótu.</span><span class="sxs-lookup"><span data-stu-id="c1245-133">To construct, see NOTES section for ENDPOINTDESCRIPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1245-134">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="c1245-134">-EndpointName</span></span>
<span data-ttu-id="c1245-135">Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="c1245-135">Name of Endpoint Resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1245-136">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="c1245-136">-EndpointType</span></span>
<span data-ttu-id="c1245-137">Typ punktu końcowego Firmy Digital</span><span class="sxs-lookup"><span data-stu-id="c1245-137">The type of Digital Twins endpoint</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Support.EndpointType
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1245-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="c1245-138">-NoWait</span></span>
<span data-ttu-id="c1245-139">Uruchamianie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="c1245-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="c1245-140">-PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="c1245-140">-PrimaryConnectionString</span></span>
<span data-ttu-id="c1245-141">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c1245-141">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceBus
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1245-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1245-142">-ResourceGroupName</span></span>
<span data-ttu-id="c1245-143">Nazwa grupy zasobów zawierającej nazwę DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c1245-143">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1245-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="c1245-144">-ResourceName</span></span>
<span data-ttu-id="c1245-145">Nazwa pliku DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c1245-145">The name of the DigitalTwinsInstance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1245-146">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="c1245-146">-SubscriptionId</span></span>
<span data-ttu-id="c1245-147">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c1245-147">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1245-148">-TopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="c1245-148">-TopicEndpoint</span></span>
<span data-ttu-id="c1245-149">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="c1245-149">The subscription identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: EventGrid
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c1245-150">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c1245-150">-Confirm</span></span>
<span data-ttu-id="c1245-151">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c1245-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1245-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c1245-152">-WhatIf</span></span>
<span data-ttu-id="c1245-153">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c1245-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c1245-154">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c1245-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1245-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1245-155">CommonParameters</span></span>
<span data-ttu-id="c1245-156">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1245-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1245-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1245-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1245-158">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1245-158">INPUTS</span></span>

### <span data-ttu-id="c1245-159">Microsoft.Azure.PowerShell.Cmdlet.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="c1245-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="c1245-160">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c1245-160">OUTPUTS</span></span>

### <span data-ttu-id="c1245-161">Microsoft.Azure.PowerShell.Cmdlet.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="c1245-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="c1245-162">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c1245-162">NOTES</span></span>

<span data-ttu-id="c1245-163">ALIASY</span><span class="sxs-lookup"><span data-stu-id="c1245-163">ALIASES</span></span>

<span data-ttu-id="c1245-164">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c1245-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="c1245-165">Aby utworzyć parametry opisane poniżej, skonstruuj tabelę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="c1245-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="c1245-166">Aby uzyskać informacje na temat skrótów tabel, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="c1245-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="c1245-167">ENDPOINTDESCRIPTION: zasób punktu końcowego <IDigitalTwinsEndpointResource> DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="c1245-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource>: DigitalTwinsInstance endpoint resource.</span></span>
  - <span data-ttu-id="c1245-168">`EndpointType <EndpointType>`: typ punktu końcowego firmy Digital Przednia</span><span class="sxs-lookup"><span data-stu-id="c1245-168">`EndpointType <EndpointType>`: The type of Digital Twins endpoint</span></span>
  - <span data-ttu-id="c1245-169">`[DeadLetterSecret <String>]`: Tajny magazyn listów traconych.</span><span class="sxs-lookup"><span data-stu-id="c1245-169">`[DeadLetterSecret <String>]`: Dead letter storage secret.</span></span> <span data-ttu-id="c1245-170">Podczas czytania zostanie on obmyty.</span><span class="sxs-lookup"><span data-stu-id="c1245-170">Will be obfuscated during read.</span></span>

## <span data-ttu-id="c1245-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c1245-171">RELATED LINKS</span></span>

