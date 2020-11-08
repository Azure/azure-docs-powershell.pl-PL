---
external help file: ''
Module Name: Az.TimeSeriesInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.timeseriesinsights/new-aztimeseriesinsightseventsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/TimeSeriesInsights/help/New-AzTimeSeriesInsightsEventSource.md
ms.openlocfilehash: 1c5e14fa71ded51d91792f462d01cb463ff36c61
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94234211"
---
# <span data-ttu-id="304e4-101">New-AzTimeSeriesInsightsEventSource</span><span class="sxs-lookup"><span data-stu-id="304e4-101">New-AzTimeSeriesInsightsEventSource</span></span>

## <span data-ttu-id="304e4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="304e4-102">SYNOPSIS</span></span>
<span data-ttu-id="304e4-103">Utwórz źródło zdarzenia w ramach określonego środowiska.</span><span class="sxs-lookup"><span data-stu-id="304e4-103">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="304e4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="304e4-104">SYNTAX</span></span>

### <span data-ttu-id="304e4-105">eventhub (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="304e4-105">eventhub (Default)</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventHubName <String> -EventSourceResourceId <String> -KeyName <String>
 -Kind <Kind> -Location <String> -ServiceBusNameSpace <String> -SharedAccessKey <SecureString>
 [-SubscriptionId <String>] [-Tag <Hashtable>] [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="304e4-106">iothub</span><span class="sxs-lookup"><span data-stu-id="304e4-106">iothub</span></span>
```
New-AzTimeSeriesInsightsEventSource -EnvironmentName <String> -Name <String> -ResourceGroupName <String>
 -ConsumerGroupName <String> -EventSourceResourceId <String> -IoTHubName <String> -KeyName <String>
 -Kind <Kind> -Location <String> -SharedAccessKey <SecureString> [-SubscriptionId <String>] [-Tag <Hashtable>]
 [-TimeStampPropertyName <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="304e4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="304e4-107">DESCRIPTION</span></span>
<span data-ttu-id="304e4-108">Utwórz źródło zdarzenia w ramach określonego środowiska.</span><span class="sxs-lookup"><span data-stu-id="304e4-108">Create an event source under the specified environment.</span></span>

## <span data-ttu-id="304e4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="304e4-109">EXAMPLES</span></span>

### <span data-ttu-id="304e4-110">Przykład 1. Tworzenie źródła zdarzeń eventhub w ramach określonego środowiska</span><span class="sxs-lookup"><span data-stu-id="304e4-110">Example 1: Create an eventhub event source under the specified environment</span></span>
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

<span data-ttu-id="304e4-111">To polecenie tworzy Źródło zdarzenia eventhub w ramach określonego środowiska.</span><span class="sxs-lookup"><span data-stu-id="304e4-111">This command creates an eventhub event source under the specified environment.</span></span>

### <span data-ttu-id="304e4-112">Przykład 2: tworzenie źródła zdarzenia iothub w ramach określonego środowiska</span><span class="sxs-lookup"><span data-stu-id="304e4-112">Example 2: Create an iothub event source under the specified environment</span></span>
```powershell
PS C:\> $ev = New-AzIotHub -ResourceGroupName testgroup -Location eastus -Name iotname001 -SkuName S1 -Units 100
PS C:\> $ks = Get-AzIotHubKey -ResourceGroupName testgroup -Name iotname001
PS C:\> $k  = $ks[0].PrimaryKey | ConvertTo-SecureString -AsPlainText -Force
PS C:\> New-AzTimeSeriesInsightsEventSource -ResourceGroupName testgroup -Name iots001 -EnvironmentName tsitest001 -Kind Microsoft.IoTHub -ConsumerGroupName testgroup -Location eastus -KeyName RootManageSharedAccessKey -IoTHubName iotname001 -EventSourceResourceId $ev.id -SharedAccessKey $k

Location Name    Type                                                   Kind
-------- ----    ----                                                   ----
eastus   iots001 Microsoft.TimeSeriesInsights/Environments/EventSources Microsoft.IoTHub
```

<span data-ttu-id="304e4-113">To polecenie tworzy Źródło zdarzenia iothub w ramach określonego środowiska.</span><span class="sxs-lookup"><span data-stu-id="304e4-113">This command creates an iothub event source under the specified environment.</span></span>

## <span data-ttu-id="304e4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="304e4-114">PARAMETERS</span></span>

### <span data-ttu-id="304e4-115">-ConsumerGroupName</span><span class="sxs-lookup"><span data-stu-id="304e4-115">-ConsumerGroupName</span></span>
<span data-ttu-id="304e4-116">Nazwa grupy konsumenckiej wydarzenia/Centrum IoT, która zawiera partycje, z których będą odczytywane zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="304e4-116">The name of the event/iot hub's consumer group that holds the partitions from which events will be read.</span></span>

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

### <span data-ttu-id="304e4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="304e4-117">-DefaultProfile</span></span>
<span data-ttu-id="304e4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="304e4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="304e4-119">-EnvironmentName</span><span class="sxs-lookup"><span data-stu-id="304e4-119">-EnvironmentName</span></span>
<span data-ttu-id="304e4-120">Nazwa środowiska informacji o serii czasowej skojarzonego z określoną grupą zasobów.</span><span class="sxs-lookup"><span data-stu-id="304e4-120">The name of the Time Series Insights environment associated with the specified resource group.</span></span>

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

### <span data-ttu-id="304e4-121">-EventHubName</span><span class="sxs-lookup"><span data-stu-id="304e4-121">-EventHubName</span></span>
<span data-ttu-id="304e4-122">Nazwa centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="304e4-122">The name of the event hub.</span></span>

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

### <span data-ttu-id="304e4-123">-EventSourceResourceId</span><span class="sxs-lookup"><span data-stu-id="304e4-123">-EventSourceResourceId</span></span>
<span data-ttu-id="304e4-124">Identyfikator zasobu źródła zdarzenia w Menedżerze zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="304e4-124">The resource id of the event source in Azure Resource Manager.</span></span>

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

### <span data-ttu-id="304e4-125">-IoTHubName</span><span class="sxs-lookup"><span data-stu-id="304e4-125">-IoTHubName</span></span>
<span data-ttu-id="304e4-126">Nazwa Centrum IoT.</span><span class="sxs-lookup"><span data-stu-id="304e4-126">The name of the iot hub.</span></span>

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

### <span data-ttu-id="304e4-127">-NazwaKlucza</span><span class="sxs-lookup"><span data-stu-id="304e4-127">-KeyName</span></span>
<span data-ttu-id="304e4-128">Nazwa klucza SAS, który przyznaje dostęp do usługi w ramach szeregu czasowego dostępu do centrum zdarzeń/usług IoT.</span><span class="sxs-lookup"><span data-stu-id="304e4-128">The name of the SAS key that grants the Time Series Insights service access to the event/iot hub.</span></span>

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

### <span data-ttu-id="304e4-129">-Kind</span><span class="sxs-lookup"><span data-stu-id="304e4-129">-Kind</span></span>
<span data-ttu-id="304e4-130">Rodzaj źródła zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="304e4-130">The kind of the event source.</span></span>

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

### <span data-ttu-id="304e4-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="304e4-131">-Location</span></span>
<span data-ttu-id="304e4-132">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="304e4-132">The location of the resource.</span></span>

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

### <span data-ttu-id="304e4-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="304e4-133">-Name</span></span>
<span data-ttu-id="304e4-134">Nazwa źródła zdarzenia.</span><span class="sxs-lookup"><span data-stu-id="304e4-134">Name of the event source.</span></span>

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

### <span data-ttu-id="304e4-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="304e4-135">-ResourceGroupName</span></span>
<span data-ttu-id="304e4-136">Nazwa grupy zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="304e4-136">Name of an Azure Resource group.</span></span>

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

### <span data-ttu-id="304e4-137">-ServiceBusNameSpace</span><span class="sxs-lookup"><span data-stu-id="304e4-137">-ServiceBusNameSpace</span></span>
<span data-ttu-id="304e4-138">Nazwa magistrali usług zawierającej centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="304e4-138">The name of the service bus that contains the event hub.</span></span>

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

### <span data-ttu-id="304e4-139">-SharedAccessKey</span><span class="sxs-lookup"><span data-stu-id="304e4-139">-SharedAccessKey</span></span>
<span data-ttu-id="304e4-140">Wartość klucza dostępu współdzielonego, który umożliwia usłudze informacji o seriach czasu dostęp do odczytu do centrum zdarzeń/usług IoT.</span><span class="sxs-lookup"><span data-stu-id="304e4-140">The value of the shared access key that grants the Time Series Insights service read access to the event/iot hub.</span></span>

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

### <span data-ttu-id="304e4-141">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="304e4-141">-SubscriptionId</span></span>
<span data-ttu-id="304e4-142">Identyfikator subskrypcji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="304e4-142">Azure Subscription ID.</span></span>

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

### <span data-ttu-id="304e4-143">-Tag</span><span class="sxs-lookup"><span data-stu-id="304e4-143">-Tag</span></span>
<span data-ttu-id="304e4-144">Pary klucz-wartość dodatkowych właściwości zasobu.</span><span class="sxs-lookup"><span data-stu-id="304e4-144">Key-value pairs of additional properties for the resource.</span></span>

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

### <span data-ttu-id="304e4-145">-TimeStampPropertyName</span><span class="sxs-lookup"><span data-stu-id="304e4-145">-TimeStampPropertyName</span></span>
<span data-ttu-id="304e4-146">Właściwość zdarzenia, która będzie używana jako sygnatura czasowa źródła zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="304e4-146">The event property that will be used as the event source's timestamp.</span></span>

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

### <span data-ttu-id="304e4-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="304e4-147">-Confirm</span></span>
<span data-ttu-id="304e4-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="304e4-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="304e4-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="304e4-149">-WhatIf</span></span>
<span data-ttu-id="304e4-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="304e4-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="304e4-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="304e4-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="304e4-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="304e4-152">CommonParameters</span></span>
<span data-ttu-id="304e4-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="304e4-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="304e4-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="304e4-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="304e4-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="304e4-155">INPUTS</span></span>

## <span data-ttu-id="304e4-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="304e4-156">OUTPUTS</span></span>

### <span data-ttu-id="304e4-157">Microsoft. Azure. PowerShell. polecenia. TimeSeriesInsights. models. Api20200515. IEventSourceResource</span><span class="sxs-lookup"><span data-stu-id="304e4-157">Microsoft.Azure.PowerShell.Cmdlets.TimeSeriesInsights.Models.Api20200515.IEventSourceResource</span></span>

## <span data-ttu-id="304e4-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="304e4-158">NOTES</span></span>

<span data-ttu-id="304e4-159">PISUJE</span><span class="sxs-lookup"><span data-stu-id="304e4-159">ALIASES</span></span>

## <span data-ttu-id="304e4-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="304e4-160">RELATED LINKS</span></span>

