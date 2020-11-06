---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHub.md
gitcommit: https://github.com/Azure/azure-powershell/blob/28baa4a53a4efceb1197c032a8db08e199f0858d
ms.openlocfilehash: 2ff36708ba9b8303c8b8763146c81ee4e4d8b209
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549196"
---
# <span data-ttu-id="62ac0-101">Set-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="62ac0-101">Set-AzureRmEventHub</span></span>

## <span data-ttu-id="62ac0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62ac0-102">SYNOPSIS</span></span>
<span data-ttu-id="62ac0-103">Umożliwia zaktualizowanie określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="62ac0-103">Updates the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62ac0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62ac0-104">SYNTAX</span></span>

### <span data-ttu-id="62ac0-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="62ac0-105">EventhubInputObjectSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-InputObject <EventHubAttributes>] [-WhatIf] [-Confirm]
```

### <span data-ttu-id="62ac0-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="62ac0-106">EventhubPropertiesSet</span></span>
```
Set-AzureRmEventHub [-ResourceGroupName] <String> -Namespace <String> -Name <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="62ac0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="62ac0-107">DESCRIPTION</span></span>
<span data-ttu-id="62ac0-108">Polecenie cmdlet Set-AzureRmEventHub aktualizuje właściwości określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="62ac0-108">The Set-AzureRmEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="62ac0-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62ac0-109">EXAMPLES</span></span>

### <span data-ttu-id="62ac0-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="62ac0-110">Example 1</span></span>
<span data-ttu-id="62ac0-111">Aby zaktualizować centrum Eventhub za pomocą właściwości funkcji przechwytywania opisu, wykonaj poniższe czynności.</span><span class="sxs-lookup"><span data-stu-id="62ac0-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
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

<span data-ttu-id="62ac0-112">Aktualizuje MyEventHubName centrum zdarzeń \` \` reprezentowanego przez \` obiekt MyCreatedEventHub \` , ustawiając okres przechowywania wiadomości na 4 dni, liczbę partycji na 2 i właściwości CaptureDescription</span><span class="sxs-lookup"><span data-stu-id="62ac0-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="62ac0-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="62ac0-113">Example 2</span></span>

```
PS C:\> Set-AzureRmEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="62ac0-114">Aktualizuje MyEventHubName centrum zdarzeń \` \` reprezentowanego przez \` obiekt MyCreatedEventHub \` , ustawiając okres przechowywania wiadomości na 4 dni i liczbę partycji na 2.</span><span class="sxs-lookup"><span data-stu-id="62ac0-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="62ac0-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62ac0-115">PARAMETERS</span></span>

### <span data-ttu-id="62ac0-116">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="62ac0-116">-messageRetentionInDays</span></span>
<span data-ttu-id="62ac0-117">Okres przechowywania komunikatów centrum zdarzeń (w dniach).</span><span class="sxs-lookup"><span data-stu-id="62ac0-117">Event Hub message retention period, in days.</span></span>

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

### <span data-ttu-id="62ac0-118">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="62ac0-118">-partitionCount</span></span>
<span data-ttu-id="62ac0-119">Liczba partycji w tym centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="62ac0-119">Number of partitions on this Event Hub.</span></span>

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

### <span data-ttu-id="62ac0-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62ac0-120">-ResourceGroupName</span></span>
<span data-ttu-id="62ac0-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="62ac0-121">Resource group name.</span></span>

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

### <span data-ttu-id="62ac0-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62ac0-122">-Confirm</span></span>
<span data-ttu-id="62ac0-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62ac0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62ac0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62ac0-124">-WhatIf</span></span>
<span data-ttu-id="62ac0-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62ac0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62ac0-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="62ac0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62ac0-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="62ac0-127">-InputObject</span></span>
<span data-ttu-id="62ac0-128">Obiekt EventHub.</span><span class="sxs-lookup"><span data-stu-id="62ac0-128">EventHub object.</span></span>

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

### <span data-ttu-id="62ac0-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="62ac0-129">-Name</span></span>
<span data-ttu-id="62ac0-130">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="62ac0-130">Namespace Name.</span></span>

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

### <span data-ttu-id="62ac0-131">-Namespace</span><span class="sxs-lookup"><span data-stu-id="62ac0-131">-Namespace</span></span>
<span data-ttu-id="62ac0-132">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="62ac0-132">Namespace Name.</span></span>

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

## <span data-ttu-id="62ac0-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62ac0-133">INPUTS</span></span>

### <span data-ttu-id="62ac0-134">System. String</span><span class="sxs-lookup"><span data-stu-id="62ac0-134">System.String</span></span>

## <span data-ttu-id="62ac0-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62ac0-135">OUTPUTS</span></span>

### <span data-ttu-id="62ac0-136">Microsoft. Azure. Commands. EventHub. modele. EventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="62ac0-136">Microsoft.Azure.Commands.EventHub.Models.EventHubAttributes</span></span>

## <span data-ttu-id="62ac0-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62ac0-137">NOTES</span></span>

## <span data-ttu-id="62ac0-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62ac0-138">RELATED LINKS</span></span>

