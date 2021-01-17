---
external help file: ''
Module Name: Az.DigitalTwins
online version: https://docs.microsoft.com/en-us/powershell/module/az.digitaltwins/new-azdigitaltwinsendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DigitalTwins/help/New-AzDigitalTwinsEndpoint.md
ms.openlocfilehash: 6b2c51d21b40745d3dd4dd2db71604fa01a5a6cc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489874"
---
# <span data-ttu-id="02472-101">New-AzDigitalTwinsEndpoint</span><span class="sxs-lookup"><span data-stu-id="02472-101">New-AzDigitalTwinsEndpoint</span></span>

## <span data-ttu-id="02472-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02472-102">SYNOPSIS</span></span>
<span data-ttu-id="02472-103">Tworzenie lub aktualizowanie punktu końcowego DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="02472-103">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="02472-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02472-104">SYNTAX</span></span>

### <span data-ttu-id="02472-105">EventHub (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="02472-105">EventHub (Default)</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -ConnectionStringPrimaryKey <String> -EndpointType <EndpointType> [-SubscriptionId <String>]
 [-ConnectionStringSecondaryKey <String>] [-DeadLetterSecret <String>]
 [-EndpointDescription <IDigitalTwinsEndpointResource>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="02472-106">EventGrid</span><span class="sxs-lookup"><span data-stu-id="02472-106">EventGrid</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -AccessKey1 <String> -EndpointType <EndpointType> -TopicEndpoint <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="02472-107">ServiceBus</span><span class="sxs-lookup"><span data-stu-id="02472-107">ServiceBus</span></span>
```
New-AzDigitalTwinsEndpoint -EndpointName <String> -ResourceGroupName <String> -ResourceName <String>
 -EndpointType <EndpointType> -PrimaryConnectionString <String> [-SubscriptionId <String>]
 [-DeadLetterSecret <String>] [-EndpointDescription <IDigitalTwinsEndpointResource>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="02472-108">Opis</span><span class="sxs-lookup"><span data-stu-id="02472-108">DESCRIPTION</span></span>
<span data-ttu-id="02472-109">Tworzenie lub aktualizowanie punktu końcowego DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="02472-109">Create or update DigitalTwinsInstance endpoint.</span></span>

## <span data-ttu-id="02472-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02472-110">EXAMPLES</span></span>

### <span data-ttu-id="02472-111">Przykład 1. Tworzenie AzDigitalTwinsEndpoint dla centrum Eventhub</span><span class="sxs-lookup"><span data-stu-id="02472-111">Example 1: Create an AzDigitalTwinsEndpoint for Eventhub</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventHubEndPoint  -EndpointType EventHub -ResourceGroupName youritemp -ResourceName youriDigitalTwins -connectionStringPrimaryKey 'Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=youriEventhubPolicy;SharedAccessKey=********;EntityPath=yourieventhub'

Name                  Type
----                  ----
youriEventHubEndPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="02472-112">Tworzenie AzDigitalTwinsEndpoint dla centrum Eventhub według connectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="02472-112">Create an AzDigitalTwinsEndpoint for Eventhub by connectionStringPrimaryKey</span></span>

### <span data-ttu-id="02472-113">Przykład 2: Tworzenie AzDigitalTwinsEndpoint dla EventGrid</span><span class="sxs-lookup"><span data-stu-id="02472-113">Example 2: Create an AzDigitalTwinsEndpoint for EventGrid</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriEventGridPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -TopicEndpoint 'https://yourieventgrid.eastus-1.eventgrid.azure.net/api/events' -AccessKey1 'xxxxxxxxx='

Name                  Type
----                  ----
youriEventGridPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="02472-114">Tworzenie AzDigitalTwinsEndpoint dla centrum Eventhub według TopicEndpoint i accessKey1</span><span class="sxs-lookup"><span data-stu-id="02472-114">Create an AzDigitalTwinsEndpoint for Eventhub by TopicEndpoint and accessKey1</span></span>

### <span data-ttu-id="02472-115">Przykład 3: Tworzenie AzDigitalTwinsEndpoint dla ServiceBus</span><span class="sxs-lookup"><span data-stu-id="02472-115">Example 3: Create an AzDigitalTwinsEndpoint for ServiceBus</span></span>
```powershell
PS C:\> New-AzDigitalTwinsEndpoint -EndpointName youriServiceBusPoint  -EndpointType EventGrid -ResourceGroupName youritemp -ResourceName youriDigitalTwins -PrimaryConnectionString "Endpoint=sb://yourieventhubnp.servicebus.windows.net/;SharedAccessKeyName=******;SharedAccessKey=********;EntityPath=yourieventhub"

Name                  Type
----                  ----
youriServiceBusPoint Microsoft.DigitalTwins/digitalTwinsInstances/endpoints
```

<span data-ttu-id="02472-116">Tworzenie AzDigitalTwinsEndpoint dla ServicBus przez PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="02472-116">Create an AzDigitalTwinsEndpoint for ServicBus by PrimaryConnectionString</span></span>

## <span data-ttu-id="02472-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02472-117">PARAMETERS</span></span>

### <span data-ttu-id="02472-118">-AccessKey1</span><span class="sxs-lookup"><span data-stu-id="02472-118">-AccessKey1</span></span>
<span data-ttu-id="02472-119">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="02472-119">The subscription identifier.</span></span>

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

### <span data-ttu-id="02472-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="02472-120">-AsJob</span></span>
<span data-ttu-id="02472-121">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="02472-121">Run the command as a job</span></span>

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

### <span data-ttu-id="02472-122">-ConnectionStringPrimaryKey</span><span class="sxs-lookup"><span data-stu-id="02472-122">-ConnectionStringPrimaryKey</span></span>
<span data-ttu-id="02472-123">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="02472-123">The subscription identifier.</span></span>

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

### <span data-ttu-id="02472-124">-ConnectionStringSecondaryKey</span><span class="sxs-lookup"><span data-stu-id="02472-124">-ConnectionStringSecondaryKey</span></span>
<span data-ttu-id="02472-125">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="02472-125">The subscription identifier.</span></span>

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

### <span data-ttu-id="02472-126">-DeadLetterSecret</span><span class="sxs-lookup"><span data-stu-id="02472-126">-DeadLetterSecret</span></span>
<span data-ttu-id="02472-127">Tajemnica miejsca do magazynowania wiadomości utraconych.</span><span class="sxs-lookup"><span data-stu-id="02472-127">Dead letter storage secret.</span></span>
<span data-ttu-id="02472-128">Zostaną zaciemniane podczas czytania.</span><span class="sxs-lookup"><span data-stu-id="02472-128">Will be obfuscated during read.</span></span>

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

### <span data-ttu-id="02472-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02472-129">-DefaultProfile</span></span>
<span data-ttu-id="02472-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02472-130">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02472-131">-EndpointDescription</span><span class="sxs-lookup"><span data-stu-id="02472-131">-EndpointDescription</span></span>
<span data-ttu-id="02472-132">Zasób punktu końcowego DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="02472-132">DigitalTwinsInstance endpoint resource.</span></span>
<span data-ttu-id="02472-133">Aby skonstruować, zobacz sekcję notatki dla właściwości ENDPOINTDESCRIPTION i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="02472-133">To construct, see NOTES section for ENDPOINTDESCRIPTION properties and create a hash table.</span></span>

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

### <span data-ttu-id="02472-134">-EndpointName</span><span class="sxs-lookup"><span data-stu-id="02472-134">-EndpointName</span></span>
<span data-ttu-id="02472-135">Nazwa zasobu punktu końcowego.</span><span class="sxs-lookup"><span data-stu-id="02472-135">Name of Endpoint Resource.</span></span>

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

### <span data-ttu-id="02472-136">-EndpointType</span><span class="sxs-lookup"><span data-stu-id="02472-136">-EndpointType</span></span>
<span data-ttu-id="02472-137">Typ cyfrowego punktu końcowego Twins</span><span class="sxs-lookup"><span data-stu-id="02472-137">The type of Digital Twins endpoint</span></span>

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

### <span data-ttu-id="02472-138">-Nowait</span><span class="sxs-lookup"><span data-stu-id="02472-138">-NoWait</span></span>
<span data-ttu-id="02472-139">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="02472-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="02472-140">-PrimaryConnectionString</span><span class="sxs-lookup"><span data-stu-id="02472-140">-PrimaryConnectionString</span></span>
<span data-ttu-id="02472-141">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="02472-141">The subscription identifier.</span></span>

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

### <span data-ttu-id="02472-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02472-142">-ResourceGroupName</span></span>
<span data-ttu-id="02472-143">Nazwa grupy zasobów zawierającej DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="02472-143">The name of the resource group that contains the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="02472-144">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="02472-144">-ResourceName</span></span>
<span data-ttu-id="02472-145">Nazwa DigitalTwinsInstance.</span><span class="sxs-lookup"><span data-stu-id="02472-145">The name of the DigitalTwinsInstance.</span></span>

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

### <span data-ttu-id="02472-146">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="02472-146">-SubscriptionId</span></span>
<span data-ttu-id="02472-147">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="02472-147">The subscription identifier.</span></span>

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

### <span data-ttu-id="02472-148">-TopicEndpoint</span><span class="sxs-lookup"><span data-stu-id="02472-148">-TopicEndpoint</span></span>
<span data-ttu-id="02472-149">Identyfikator subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="02472-149">The subscription identifier.</span></span>

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

### <span data-ttu-id="02472-150">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="02472-150">-Confirm</span></span>
<span data-ttu-id="02472-151">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02472-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02472-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02472-152">-WhatIf</span></span>
<span data-ttu-id="02472-153">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="02472-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02472-154">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="02472-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02472-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02472-155">CommonParameters</span></span>
<span data-ttu-id="02472-156">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02472-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02472-157">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="02472-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02472-158">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02472-158">INPUTS</span></span>

### <span data-ttu-id="02472-159">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. Api20201031. IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="02472-159">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="02472-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02472-160">OUTPUTS</span></span>

### <span data-ttu-id="02472-161">Microsoft. Azure. PowerShell. polecenia. DigitalTwins. models. Api20201031. IDigitalTwinsEndpointResource</span><span class="sxs-lookup"><span data-stu-id="02472-161">Microsoft.Azure.PowerShell.Cmdlets.DigitalTwins.Models.Api20201031.IDigitalTwinsEndpointResource</span></span>

## <span data-ttu-id="02472-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02472-162">NOTES</span></span>

<span data-ttu-id="02472-163">PISUJE</span><span class="sxs-lookup"><span data-stu-id="02472-163">ALIASES</span></span>

<span data-ttu-id="02472-164">ZŁOŻONE WŁAŚCIWOŚCI PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02472-164">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="02472-165">Aby utworzyć opisane poniżej parametry, Skonstruuj tablicę skrótów zawierającą odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="02472-165">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="02472-166">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="02472-166">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="02472-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource> : DigitalTwinsInstance w punkcie końcowym.</span><span class="sxs-lookup"><span data-stu-id="02472-167">ENDPOINTDESCRIPTION <IDigitalTwinsEndpointResource>: DigitalTwinsInstance endpoint resource.</span></span>
  - <span data-ttu-id="02472-168">`EndpointType <EndpointType>`: Typ punktu końcowego Twins cyfrowego</span><span class="sxs-lookup"><span data-stu-id="02472-168">`EndpointType <EndpointType>`: The type of Digital Twins endpoint</span></span>
  - <span data-ttu-id="02472-169">`[DeadLetterSecret <String>]`: Tajemnica miejsca na przechowywanie listów utraconych.</span><span class="sxs-lookup"><span data-stu-id="02472-169">`[DeadLetterSecret <String>]`: Dead letter storage secret.</span></span> <span data-ttu-id="02472-170">Zostaną zaciemniane podczas czytania.</span><span class="sxs-lookup"><span data-stu-id="02472-170">Will be obfuscated during read.</span></span>

## <span data-ttu-id="02472-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02472-171">RELATED LINKS</span></span>

