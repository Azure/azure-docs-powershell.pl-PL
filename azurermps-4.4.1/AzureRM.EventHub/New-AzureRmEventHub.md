---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 656e010a05ce1272355f689be8513ecadd330e7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553903"
---
# <span data-ttu-id="36b92-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="36b92-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="36b92-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36b92-102">SYNOPSIS</span></span>
<span data-ttu-id="36b92-103">Tworzy nowy centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="36b92-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36b92-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36b92-104">SYNTAX</span></span>

### <span data-ttu-id="36b92-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="36b92-105">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="36b92-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="36b92-106">EventhubPropertiesSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> [[-Location] <String>] -Name <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="36b92-107">Opis</span><span class="sxs-lookup"><span data-stu-id="36b92-107">DESCRIPTION</span></span>
<span data-ttu-id="36b92-108">Polecenie cmdlet New-AzureRmEventHub tworzy nowy centrum zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="36b92-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="36b92-109">Aby utworzyć centrum Eventhub za pomocą właściwości funkcji przechwytywania opisu, wykonaj poniższe czynności (przykłady 2).</span><span class="sxs-lookup"><span data-stu-id="36b92-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 


## <span data-ttu-id="36b92-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36b92-110">EXAMPLES</span></span>

### <span data-ttu-id="36b92-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="36b92-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2
```

<span data-ttu-id="36b92-112">Tworzy centrum zdarzeń o nazwie \` MyEventHubName \` z 3-dniowym okresem przechowywania wiadomości i dwiema partycjami w \` lokalizacji na zachód \` z grupą zasobów \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="36b92-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="36b92-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="36b92-113">Example 2</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

PS C:\> $CreatedEventHub = Get-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName

PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.CaptureDescriptionAttributes

PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="36b92-114">Tworzy centrum zdarzeń o nazwie \` MyEventHubName \` z 3-dniowym okresem przechowywania wiadomości, 2 partycje i właściwości CaptureDescription w \` lokalizacji zachodniej \` , z MyResourceGroupName grupą \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="36b92-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="36b92-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36b92-115">PARAMETERS</span></span>

### <span data-ttu-id="36b92-116">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="36b92-116">-Location</span></span>
<span data-ttu-id="36b92-117">Lokalizacja geograficzna obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="36b92-117">Namespace geographic location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b92-118">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="36b92-118">-MessageRetentionInDays</span></span>
<span data-ttu-id="36b92-119">Czas przechowywania komunikatów koncentratorów zdarzeń w dniach.</span><span class="sxs-lookup"><span data-stu-id="36b92-119">Event Hubs message retention time in days.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b92-120">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="36b92-120">-PartitionCount</span></span>
<span data-ttu-id="36b92-121">Liczba partycji w centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="36b92-121">Number of partitions in the Event Hub.</span></span>

```yaml
Type: Int64
Parameter Sets: EventhubPropertiesSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b92-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36b92-122">-ResourceGroupName</span></span>
<span data-ttu-id="36b92-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="36b92-123">Resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b92-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="36b92-124">-Confirm</span></span>
<span data-ttu-id="36b92-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36b92-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b92-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36b92-126">-WhatIf</span></span>
<span data-ttu-id="36b92-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="36b92-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="36b92-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="36b92-128">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36b92-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="36b92-129">-InputObject</span></span>
<span data-ttu-id="36b92-130">Obiekt wejściowy EventHub.</span><span class="sxs-lookup"><span data-stu-id="36b92-130">EventHub Input object.</span></span>

```yaml
Type: EventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b92-131">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="36b92-131">-Name</span></span>
<span data-ttu-id="36b92-132">Nazwa Eventhub.</span><span class="sxs-lookup"><span data-stu-id="36b92-132">Eventhub Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36b92-133">-Namespace</span><span class="sxs-lookup"><span data-stu-id="36b92-133">-Namespace</span></span>
<span data-ttu-id="36b92-134">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="36b92-134">Namespace Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

## <span data-ttu-id="36b92-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36b92-135">INPUTS</span></span>

### <span data-ttu-id="36b92-136">System. String</span><span class="sxs-lookup"><span data-stu-id="36b92-136">System.String</span></span>

## <span data-ttu-id="36b92-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36b92-137">OUTPUTS</span></span>

### <span data-ttu-id="36b92-138">Microsoft. Azure. Commands. EventHub. modele. EventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="36b92-138">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="36b92-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36b92-139">NOTES</span></span>

## <span data-ttu-id="36b92-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36b92-140">RELATED LINKS</span></span>

