---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHub.md
ms.openlocfilehash: ad7d4a1cefaadf3f1c2f12b9ef3a1b516c3813fa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705422"
---
# <span data-ttu-id="4201b-101">Set-AzEventHub</span><span class="sxs-lookup"><span data-stu-id="4201b-101">Set-AzEventHub</span></span>

## <span data-ttu-id="4201b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4201b-102">SYNOPSIS</span></span>
<span data-ttu-id="4201b-103">Umożliwia zaktualizowanie określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="4201b-103">Updates the specified Event Hub.</span></span>

## <span data-ttu-id="4201b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4201b-104">SYNTAX</span></span>

### <span data-ttu-id="4201b-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="4201b-105">EventhubInputObjectSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4201b-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="4201b-106">EventhubPropertiesSet</span></span>
```
Set-AzEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-messageRetentionInDays <Int64>] [-partitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4201b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4201b-107">DESCRIPTION</span></span>
<span data-ttu-id="4201b-108">Polecenie cmdlet Set-AzEventHub aktualizuje właściwości określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="4201b-108">The Set-AzEventHub cmdlet updates the properties of the specified Event Hub.</span></span>

## <span data-ttu-id="4201b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4201b-109">EXAMPLES</span></span>

### <span data-ttu-id="4201b-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4201b-110">Example 1</span></span>
<span data-ttu-id="4201b-111">Aby zaktualizować centrum Eventhub za pomocą właściwości funkcji przechwytywania opisu, wykonaj poniższe czynności.</span><span class="sxs-lookup"><span data-stu-id="4201b-111">To update Eventhub with Capture description properties, please follow the below steps.</span></span> 

```
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

<span data-ttu-id="4201b-112">Aktualizuje MyEventHubName centrum zdarzeń \` \` reprezentowanego przez \` obiekt MyCreatedEventHub \` , ustawiając okres przechowywania wiadomości na 4 dni, liczbę partycji na 2 i właściwości CaptureDescription</span><span class="sxs-lookup"><span data-stu-id="4201b-112">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, the number of partitions to 2 and CaptureDescription properties</span></span>

### <span data-ttu-id="4201b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="4201b-113">Example 2</span></span>
```
PS C:\> Set-AzEventHub -ResourceGroupName MyResourceGroupName -Namespace MyNamespaceName -Name MyEventHubName -InputObject MyCreatedEventHub -messageRetentionInDays 4 -partitionCount 2
```

<span data-ttu-id="4201b-114">Aktualizuje MyEventHubName centrum zdarzeń \` \` reprezentowanego przez \` obiekt MyCreatedEventHub \` , ustawiając okres przechowywania wiadomości na 4 dni i liczbę partycji na 2.</span><span class="sxs-lookup"><span data-stu-id="4201b-114">Updates the Event Hub \`MyEventHubName\` represented by the \`MyCreatedEventHub\` object, setting the message retention period to 4 days, and the number of partitions to 2.</span></span>

## <span data-ttu-id="4201b-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4201b-115">PARAMETERS</span></span>

### <span data-ttu-id="4201b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4201b-116">-DefaultProfile</span></span>
<span data-ttu-id="4201b-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4201b-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4201b-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4201b-118">-InputObject</span></span>
<span data-ttu-id="4201b-119">Obiekt EventHub</span><span class="sxs-lookup"><span data-stu-id="4201b-119">EventHub object</span></span>

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

### <span data-ttu-id="4201b-120">-messageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="4201b-120">-messageRetentionInDays</span></span>
<span data-ttu-id="4201b-121">Przechowywanie wiadomości Eventhub w dniach</span><span class="sxs-lookup"><span data-stu-id="4201b-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="4201b-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4201b-122">-Name</span></span>
<span data-ttu-id="4201b-123">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="4201b-123">Namespace Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4201b-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4201b-124">-Namespace</span></span>
<span data-ttu-id="4201b-125">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="4201b-125">Namespace Name</span></span>

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

### <span data-ttu-id="4201b-126">-partitionCount</span><span class="sxs-lookup"><span data-stu-id="4201b-126">-partitionCount</span></span>
<span data-ttu-id="4201b-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="4201b-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="4201b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4201b-128">-ResourceGroupName</span></span>
<span data-ttu-id="4201b-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4201b-129">Resource Group Name</span></span>

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

### <span data-ttu-id="4201b-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4201b-130">-Confirm</span></span>
<span data-ttu-id="4201b-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4201b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4201b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4201b-132">-WhatIf</span></span>
<span data-ttu-id="4201b-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4201b-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4201b-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4201b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4201b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4201b-135">CommonParameters</span></span>
<span data-ttu-id="4201b-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4201b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4201b-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4201b-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4201b-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4201b-138">INPUTS</span></span>

### <span data-ttu-id="4201b-139">System. String</span><span class="sxs-lookup"><span data-stu-id="4201b-139">System.String</span></span>

### <span data-ttu-id="4201b-140">Microsoft. Azure. Commands. EventHub. modele. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="4201b-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

### <span data-ttu-id="4201b-141">System. Nullable ' 1 [[System. Int64; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="4201b-141">System.Nullable\`1[[System.Int64, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="4201b-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4201b-142">OUTPUTS</span></span>

### <span data-ttu-id="4201b-143">Microsoft. Azure. Commands. EventHub. modele. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="4201b-143">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>

## <span data-ttu-id="4201b-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4201b-144">NOTES</span></span>

## <span data-ttu-id="4201b-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4201b-145">RELATED LINKS</span></span>