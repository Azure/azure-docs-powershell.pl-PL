---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: fa2573a774df86ee96563e90b617db43aed0b1c3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995842"
---
# <span data-ttu-id="7a6ae-101">New-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="7a6ae-101">New-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="7a6ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a6ae-102">SYNOPSIS</span></span>
<span data-ttu-id="7a6ae-103">Tworzenie źródła zdarzeń w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-103">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="7a6ae-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7a6ae-104">SYNTAX</span></span>

### <span data-ttu-id="7a6ae-105">eventhub (domyślne)</span><span class="sxs-lookup"><span data-stu-id="7a6ae-105">eventhub (Default)</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventHubName <String> -EventSourceResourceId <String> -KeyName <String>
 -Kind <Kind> -Location <String> -ServiceBusNameSpace <String> -SharedAccessKey <SecureString>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="7a6ae-106">iothub</span><span class="sxs-lookup"><span data-stu-id="7a6ae-106">iothub</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventSourceResourceId <String> -IoTHubName <String> -KeyName <String>
 -Kind <Kind> -Location <String> -SharedAccessKey <SecureString> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="7a6ae-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="7a6ae-107">DESCRIPTION</span></span>
<span data-ttu-id="7a6ae-108">Tworzenie źródła zdarzeń w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-108">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="7a6ae-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7a6ae-109">EXAMPLES</span></span>

### <span data-ttu-id="7a6ae-110">Przykład 1. Tworzenie źródła zdarzeń aplikacji EventHub w określonym środowisku</span><span class="sxs-lookup"><span data-stu-id="7a6ae-110">Example 1: Create an eventhub event source under the specified environment</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -Name spacename002 -ResourceGroupName testgroup -Location eastus
PS C:\> $ev = New-AzEventHub -ResourceGroupName testgroup -NamespaceName spacename002 -Name hubname001 -MessageRetentionInDays 3 -PartitionCount 2
PS C:\> $ks = Get-AzEventHubKey -ResourceGroupName testgroup -NamespaceName spacename002 -AuthorizationRuleName RootManageSharedAccessKey
PS C:\> $k  = $ks.PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name estest001 -EnvironmentName tsitest001 -Kind Microsoft.EventHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -ServiceBusNameSpace spacename002 -EventHubName hubname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Kind               Location Name      Type
----               -------- ----      ----
Microsoft.EventHub eastus   estest001 Microsoft.TimeSeriesInsights/Environments/EventSources
```

<span data-ttu-id="7a6ae-111">To polecenie tworzy źródło zdarzeń aplikacji EventHub w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-111">This command creates an eventhub event source under the specified environment.</span></span>

### <span data-ttu-id="7a6ae-112">Przykład 2. Tworzenie źródła zdarzeń aplikacji iothub w określonym środowisku</span><span class="sxs-lookup"><span data-stu-id="7a6ae-112">Example 2: Create an iothub event source under the specified environment</span></span>
```powershell
PS C:\> $ev = New-AzIotHub -ResourceGroupName testgroup -Location eastus -Name iotname001 -SkuName S1 -Units 100
PS C:\> $ks = Get-AzIotHubKey -ResourceGroupName testgroup -Name iotname001
PS C:\> $k  = $ks[0].PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name iots001 -EnvironmentName tsitest001 -Kind Microsoft.IoTHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -IoTHubName iotname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Location Name    Type                                                   Kind
-------- ----    ----                                                   ----
eastus   iots001 Microsoft.TimeSeriesInsights/Environments/EventSources Microsoft.IoTHub
```

<span data-ttu-id="7a6ae-113">To polecenie tworzy źródło zdarzeń aplikacji iothub w określonym środowisku.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-113">This command creates an iothub event source under the specified environment.</span></span>

## <span data-ttu-id="7a6ae-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a6ae-114">PARAMETERS</span></span>

### <span data-ttu-id="7a6ae-115">- ConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="7a6ae-115">-ConsumerGroupName</span></span>
<span data-ttu-id="7a6ae-116">Nazwa grupy konsumenckiej centrum zdarzeń/iot, która zawiera partycje, z których będą odczytywane zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-116">The name of the event/iot hub's consumer group that holds the partitions from which events will be read.</span></span>

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

### <span data-ttu-id="7a6ae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a6ae-117">-DefaultProfile</span></span>
<span data-ttu-id="7a6ae-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a6ae-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="7a6ae-119">-EnvironmentName</span></span>
<span data-ttu-id="7a6ae-120">Nazwa środowiska szczegółowych informacji szeregu czasowego skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="7a6ae-121">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="7a6ae-121">-EventHubName</span></span>
<span data-ttu-id="7a6ae-122">Nazwa centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-122">The name of the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a6ae-123">-EventSourceResourceId</span><span class="sxs-lookup"><span data-stu-id="7a6ae-123">-EventSourceResourceId</span></span>
<span data-ttu-id="7a6ae-124">Identyfikator zasobu źródła zdarzeń w usłudze Azure Resource Manager.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-124">The resource id of the event source in Azure Resource Manager.</span></span>

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

### <span data-ttu-id="7a6ae-125">-IoTHubName</span><span class="sxs-lookup"><span data-stu-id="7a6ae-125">-IoTHubName</span></span>
<span data-ttu-id="7a6ae-126">Nazwa centrum iot.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-126">The name of the iot hub.</span></span>

```yaml
Type: System.String
Parameter Sets: iothub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a6ae-127">-KeyName</span><span class="sxs-lookup"><span data-stu-id="7a6ae-127">-KeyName</span></span>
<span data-ttu-id="7a6ae-128">Nazwa klucza SAS, który udziela usłudze Time Series Insights dostępu do centrum zdarzeń/iot.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-128">The name of the SAS key that grants the Time Series Insights service access to the event/iot hub.</span></span>

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

### <span data-ttu-id="7a6ae-129">— Rodzaj</span><span class="sxs-lookup"><span data-stu-id="7a6ae-129">-Kind</span></span>
<span data-ttu-id="7a6ae-130">Rodzaj źródła zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-130">The kind of the event source.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Support.Kind
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a6ae-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="7a6ae-131">-Location</span></span>
<span data-ttu-id="7a6ae-132">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-132">The location of the resource.</span></span>

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

### <span data-ttu-id="7a6ae-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="7a6ae-133">-Name</span></span>
<span data-ttu-id="7a6ae-134">Nazwa źródła zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-134">Name of the event source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventSourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a6ae-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7a6ae-135">-ResourceGroupName</span></span>
<span data-ttu-id="7a6ae-136">Nazwa grupy usługi Azure Resource.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="7a6ae-137">-ServiceBusNameSpace</span><span class="sxs-lookup"><span data-stu-id="7a6ae-137">-ServiceBusNameSpace</span></span>
<span data-ttu-id="7a6ae-138">Nazwa autobusu usługi zawierającego centrum wydarzeń.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-138">The name of the service bus that contains the event hub.</span></span>

```yaml
Type: System.String
Parameter Sets: eventhub
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a6ae-139">-SharedAccessKey</span><span class="sxs-lookup"><span data-stu-id="7a6ae-139">-SharedAccessKey</span></span>
<span data-ttu-id="7a6ae-140">Wartość klucza dostępu udostępnionego, który udziela usłudze Time Series Insights dostępu do odczytu centrum zdarzeń/iot.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-140">The value of the shared access key that grants the Time Series Insights service read access to the event/iot hub.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a6ae-141">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="7a6ae-141">-SubscriptionId</span></span>
<span data-ttu-id="7a6ae-142">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-142">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="7a6ae-143">— Tag</span><span class="sxs-lookup"><span data-stu-id="7a6ae-143">-Tag</span></span>
<span data-ttu-id="7a6ae-144">Pary klucz-wartość dodatkowych właściwości zasobu.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-144">Key-value pairs of additional properties for the resource.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7a6ae-145">-TimeStampPropertyName</span><span class="sxs-lookup"><span data-stu-id="7a6ae-145">-TimeStampPropertyName</span></span>
<span data-ttu-id="7a6ae-146">Właściwość zdarzenia, która będzie używana jako sygnatura czasowa źródła zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-146">The event property that will be used as the event source's timestamp.</span></span>

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

### <span data-ttu-id="7a6ae-147">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a6ae-147">-Confirm</span></span>
<span data-ttu-id="7a6ae-148">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a6ae-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a6ae-149">-WhatIf</span></span>
<span data-ttu-id="7a6ae-150">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a6ae-151">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a6ae-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a6ae-152">CommonParameters</span></span>
<span data-ttu-id="7a6ae-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a6ae-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a6ae-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7a6ae-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a6ae-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a6ae-155">INPUTS</span></span>

## <span data-ttu-id="7a6ae-156">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a6ae-156">OUTPUTS</span></span>

### <span data-ttu-id="7a6ae-157">Microsoft.Azure.PowerShell.Cmdlet.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="7a6ae-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="7a6ae-158">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7a6ae-158">NOTES</span></span>

<span data-ttu-id="7a6ae-159">ALIASY</span><span class="sxs-lookup"><span data-stu-id="7a6ae-159">ALIASES</span></span>

## <span data-ttu-id="7a6ae-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a6ae-160">RELATED LINKS</span></span>

