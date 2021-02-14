---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/new-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHub.md
ms.openlocfilehash: eec7294a15217be85b4c2248dac6506d54c2e6aa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100237900"
---
# <span data-ttu-id="40bda-101">New-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="40bda-101">New-AzEventHub</span></span>

## <span data-ttu-id="40bda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40bda-102">SYNOPSIS</span></span>
<span data-ttu-id="40bda-103">Tworzy nowe Centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="40bda-103">Creates a new Event Hub.</span></span>

## <span data-ttu-id="40bda-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="40bda-104">SYNTAX</span></span>

### <span data-ttu-id="40bda-105">EventhubPropertiesSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="40bda-105">EventhubPropertiesSet (Default)</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40bda-106">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="40bda-106">EventhubInputObjectSet</span></span>
```
New-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="40bda-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="40bda-107">DESCRIPTION</span></span>
<span data-ttu-id="40bda-108">Polecenie New-AzEventHub cmdlet tworzy nowe centrum zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="40bda-108">The New-AzEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="40bda-109">Aby utworzyćhubę zdarzenia z właściwościami przechwytywania opisu, wykonaj poniższe czynności (przykłady 2).</span><span class="sxs-lookup"><span data-stu-id="40bda-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="40bda-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="40bda-110">EXAMPLES</span></span>

### <span data-ttu-id="40bda-111">Przykład 1. Tworzenie nowej aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="40bda-111">Example 1: - Create new EventHub</span></span>
```powershell
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName
```

<span data-ttu-id="40bda-112">Tworzy centrum zdarzeń o nazwie MyEventHubName z 3-dniowym okresem przechowywania wiadomości i dwoma partycjami w lokalizacji WestUS z grupą zasobów \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="40bda-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="40bda-113">Przykład 2. Aktualizowanie aplikacji Eventhub za pomocą funkcji CaptureDescription</span><span class="sxs-lookup"><span data-stu-id="40bda-113">Example 2: Update Eventhub with 'CaptureDescription'</span></span>
```powershell
PS C:\> New-AzEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Name MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2

PS C:\> $CreatedEventHub = Get-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName

PS C:\> $createdEventHub.CaptureDescription = New-Object -TypeName Microsoft.Azure.Commands.EventHub.Models.PSCaptureDescriptionAttributes

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

<span data-ttu-id="40bda-114">Tworzy centrum zdarzeń o nazwie MyEventHubName z 3-dniowym okresem przechowywania wiadomości, 2 partycjami i właściwościami CaptureDescription w lokalizacji WestUS z grupą zasobów \` \` \` \` \` MyResourceGroupName. \`</span><span class="sxs-lookup"><span data-stu-id="40bda-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="40bda-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="40bda-115">PARAMETERS</span></span>

### <span data-ttu-id="40bda-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40bda-116">-DefaultProfile</span></span>
<span data-ttu-id="40bda-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="40bda-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40bda-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="40bda-118">-InputObject</span></span>
<span data-ttu-id="40bda-119">Obiekt Wprowadzania w usłudze EventHub</span><span class="sxs-lookup"><span data-stu-id="40bda-119">EventHub Input object</span></span>

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

### <span data-ttu-id="40bda-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="40bda-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="40bda-121">Przechowywanie wiadomości w usłudze EventHub w dniach</span><span class="sxs-lookup"><span data-stu-id="40bda-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="40bda-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="40bda-122">-Name</span></span>
<span data-ttu-id="40bda-123">Nazwa aplikacji Eventhub</span><span class="sxs-lookup"><span data-stu-id="40bda-123">Eventhub Name</span></span>

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

### <span data-ttu-id="40bda-124">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="40bda-124">-Namespace</span></span>
<span data-ttu-id="40bda-125">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="40bda-125">Namespace Name</span></span>

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

### <span data-ttu-id="40bda-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="40bda-126">-PartitionCount</span></span>
<span data-ttu-id="40bda-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="40bda-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="40bda-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40bda-128">-ResourceGroupName</span></span>
<span data-ttu-id="40bda-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="40bda-129">Resource Group Name</span></span>

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

### <span data-ttu-id="40bda-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="40bda-130">-Confirm</span></span>
<span data-ttu-id="40bda-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="40bda-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40bda-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40bda-132">-WhatIf</span></span>
<span data-ttu-id="40bda-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="40bda-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40bda-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="40bda-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40bda-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40bda-135">CommonParameters</span></span>
<span data-ttu-id="40bda-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="40bda-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40bda-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="40bda-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40bda-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40bda-138">INPUTS</span></span>

### <span data-ttu-id="40bda-139">System.String</span><span class="sxs-lookup"><span data-stu-id="40bda-139">System.String</span></span>

### <span data-ttu-id="40bda-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="40bda-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="40bda-141">System.Nullable'1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="40bda-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="40bda-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="40bda-142">OUTPUTS</span></span>

### <span data-ttu-id="40bda-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="40bda-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="40bda-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="40bda-144">NOTES</span></span>

## <span data-ttu-id="40bda-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="40bda-145">RELATED LINKS</span></span>
