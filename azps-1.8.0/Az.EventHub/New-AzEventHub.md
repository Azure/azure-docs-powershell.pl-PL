---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
ms.openlocfilehash: ac61b1f0bec6ea6b76fcc2b0ea4cf1438359197b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93709811"
---
# <span data-ttu-id="e4351-101">New-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="e4351-101">New-AzEventHub</span></span>

## <span data-ttu-id="e4351-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e4351-102">SYNOPSIS</span></span>
<span data-ttu-id="e4351-103">Tworzy nowy centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="e4351-103">Creates a new Event Hub.</span></span>

## <span data-ttu-id="e4351-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e4351-104">SYNTAX</span></span>

### <span data-ttu-id="e4351-105">EventhubPropertiesSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e4351-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4351-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="e4351-106">EventhubInputObjectSet</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e4351-107">Opis</span><span class="sxs-lookup"><span data-stu-id="e4351-107">DESCRIPTION</span></span>
<span data-ttu-id="e4351-108">Polecenie cmdlet New-AzEventHub tworzy nowy centrum zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e4351-108">The New-AzEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="e4351-109">Aby utworzyć centrum Eventhub za pomocą właściwości funkcji przechwytywania opisu, wykonaj poniższe czynności (przykłady 2).</span><span class="sxs-lookup"><span data-stu-id="e4351-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="e4351-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e4351-110">EXAMPLES</span></span>

### <span data-ttu-id="e4351-111">Przykład 1-Tworzenie nowego centrum EventHub</span><span class="sxs-lookup"><span data-stu-id="e4351-111">Example 1  - Create new EventHub</span></span>
```
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="e4351-112">Tworzy centrum zdarzeń o nazwie \` MyEventHubName \` z 3-dniowym okresem przechowywania wiadomości i dwiema partycjami w \` lokalizacji na zachód \` z grupą zasobów \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="e4351-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="e4351-113">Przykład 2 aktualizowanie centrum Eventhub za pomocą "CaptureDescription"</span><span class="sxs-lookup"><span data-stu-id="e4351-113">Example 2 Update Eventhub with 'CaptureDescription'</span></span>
```
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

PS C:\> $CreatedEventHub = Get-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName

PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.CaptureDescriptionAttributes

PS C:\> $createdEventHub.CaptureDescription.Enabled = $true
PS C:\> $createdEventHub.CaptureDescription.IntervalInSeconds  = 120
PS C:\> $createdEventHub.CaptureDescription.Encoding  = "Avro"
PS C:\> $createdEventHub.CaptureDescription.SizeLimitInBytes = 10485763
PS C:\> $createdEventHub.CaptureDescription.Destination.Name = "EventHubArchive.AzureBlockBlob"
PS C:\> $createdEventHub.CaptureDescription.Destination.BlobContainer = "container"
PS C:\> $createdEventHub.CaptureDescription.Destination.ArchiveNameFormat = "{Namespace}/{EventHub}/{PartitionId}/{Year}/{Month}/{Day}/{Hour}/{Minute}/{Second}"
PS C:\> $createdEventHub.CaptureDescription.Destination.StorageAccountResourceId = "/subscriptions/{SubscriptionId}/resourceGroups/MyResourceGroupName/providers/Microsoft.ClassicStorage/storageAccounts/arjunteststorage"
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="e4351-114">Tworzy centrum zdarzeń o nazwie \` MyEventHubName \` z 3-dniowym okresem przechowywania wiadomości, 2 partycje i właściwości CaptureDescription w \` lokalizacji zachodniej \` , z MyResourceGroupName grupą \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="e4351-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="e4351-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e4351-115">PARAMETERS</span></span>

### <span data-ttu-id="e4351-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4351-116">-DefaultProfile</span></span>
<span data-ttu-id="e4351-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e4351-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4351-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="e4351-118">-InputObject</span></span>
<span data-ttu-id="e4351-119">Obiekt wejściowy EventHub</span><span class="sxs-lookup"><span data-stu-id="e4351-119">EventHub Input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4351-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="e4351-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="e4351-121">Przechowywanie wiadomości Eventhub w dniach</span><span class="sxs-lookup"><span data-stu-id="e4351-121">Eventhub Message Retention In Days</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4351-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e4351-122">-Name</span></span>
<span data-ttu-id="e4351-123">Nazwa Eventhub</span><span class="sxs-lookup"><span data-stu-id="e4351-123">Eventhub Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4351-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e4351-124">-Namespace</span></span>
<span data-ttu-id="e4351-125">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="e4351-125">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4351-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="e4351-126">-PartitionCount</span></span>
<span data-ttu-id="e4351-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="e4351-127">Eventhub PartitionCount</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: EventhubPropertiesSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4351-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4351-128">-ResourceGroupName</span></span>
<span data-ttu-id="e4351-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e4351-129">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4351-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e4351-130">-Confirm</span></span>
<span data-ttu-id="e4351-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4351-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4351-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4351-132">-WhatIf</span></span>
<span data-ttu-id="e4351-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e4351-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4351-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e4351-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4351-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4351-135">CommonParameters</span></span>
<span data-ttu-id="e4351-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e4351-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4351-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4351-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4351-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e4351-138">INPUTS</span></span>

### <span data-ttu-id="e4351-139">System. String</span><span class="sxs-lookup"><span data-stu-id="e4351-139">System.String</span></span>

### <span data-ttu-id="e4351-140">Microsoft. Azure. Commands. EventHub. modele. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="e4351-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="e4351-141">System. Nullable ' 1 [[System. Int64; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e4351-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="e4351-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e4351-142">OUTPUTS</span></span>

### <span data-ttu-id="e4351-143">Microsoft. Azure. Commands. EventHub. modele. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="e4351-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="e4351-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e4351-144">NOTES</span></span>

## <span data-ttu-id="e4351-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e4351-145">RELATED LINKS</span></span>
