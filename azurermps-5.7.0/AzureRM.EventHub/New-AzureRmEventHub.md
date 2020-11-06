---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHub.md
ms.openlocfilehash: 2c5bf49245da7ecac0f9d4351f5a66a39a663b98
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551727"
---
# <span data-ttu-id="2deab-101">New-AzureRmEventHub</span><span class="sxs-lookup"><span data-stu-id="2deab-101">New-AzureRmEventHub</span></span>

## <span data-ttu-id="2deab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2deab-102">SYNOPSIS</span></span>
<span data-ttu-id="2deab-103">Tworzy nowy centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="2deab-103">Creates a new Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2deab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2deab-104">SYNTAX</span></span>

### <span data-ttu-id="2deab-105">EventhubInputObjectSet</span><span class="sxs-lookup"><span data-stu-id="2deab-105">EventhubInputObjectSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject <PSEventHubAttributes>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2deab-106">EventhubPropertiesSet</span><span class="sxs-lookup"><span data-stu-id="2deab-106">EventhubPropertiesSet</span></span>
```
New-AzureRmEventHub [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-MessageRetentionInDays <Int64>] [-PartitionCount <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2deab-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2deab-107">DESCRIPTION</span></span>
<span data-ttu-id="2deab-108">Polecenie cmdlet New-AzureRmEventHub tworzy nowy centrum zdarzeń platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2deab-108">The New-AzureRmEventHub cmdlet creates a new Azure Event Hub.</span></span>
<span data-ttu-id="2deab-109">Aby utworzyć centrum Eventhub za pomocą właściwości funkcji przechwytywania opisu, wykonaj poniższe czynności (przykłady 2).</span><span class="sxs-lookup"><span data-stu-id="2deab-109">To create Eventhub with Capture description properties, please follow the below steps (Examples 2).</span></span> 

## <span data-ttu-id="2deab-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2deab-110">EXAMPLES</span></span>

### <span data-ttu-id="2deab-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2deab-111">Example 1</span></span>
```
PS C:\> New-AzureRmEventHub -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location WestUS -EventHubName MyEventHubName -MessageRetentionInDays 3 -PartitionCount 2
```

<span data-ttu-id="2deab-112">Tworzy centrum zdarzeń o nazwie \` MyEventHubName \` z 3-dniowym okresem przechowywania wiadomości i dwiema partycjami w \` lokalizacji na zachód \` z grupą zasobów \` MyResourceGroupName \` .</span><span class="sxs-lookup"><span data-stu-id="2deab-112">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period and two partitions, in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2deab-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2deab-113">Example 2</span></span>
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

<span data-ttu-id="2deab-114">Tworzy centrum zdarzeń o nazwie \` MyEventHubName \` z 3-dniowym okresem przechowywania wiadomości, 2 partycje i właściwości CaptureDescription w \` lokalizacji zachodniej \` , z MyResourceGroupName grupą \` zasobów \` .</span><span class="sxs-lookup"><span data-stu-id="2deab-114">Creates an Event Hub named \`MyEventHubName\` with a 3-day message retention period, 2 partitions and CaptureDescription properties in the \`WestUS\` location, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="2deab-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2deab-115">PARAMETERS</span></span>

### <span data-ttu-id="2deab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2deab-116">-DefaultProfile</span></span>
<span data-ttu-id="2deab-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2deab-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2deab-118">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2deab-118">-InputObject</span></span>
<span data-ttu-id="2deab-119">Obiekt wejściowy EventHub</span><span class="sxs-lookup"><span data-stu-id="2deab-119">EventHub Input object</span></span>

```yaml
Type: PSEventHubAttributes
Parameter Sets: EventhubInputObjectSet
Aliases: EventHubObj

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2deab-120">-MessageRetentionInDays</span><span class="sxs-lookup"><span data-stu-id="2deab-120">-MessageRetentionInDays</span></span>
<span data-ttu-id="2deab-121">Przechowywanie wiadomości Eventhub w dniach</span><span class="sxs-lookup"><span data-stu-id="2deab-121">Eventhub Message Retention In Days</span></span>

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

### <span data-ttu-id="2deab-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2deab-122">-Name</span></span>
<span data-ttu-id="2deab-123">Nazwa Eventhub</span><span class="sxs-lookup"><span data-stu-id="2deab-123">Eventhub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2deab-124">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2deab-124">-Namespace</span></span>
<span data-ttu-id="2deab-125">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="2deab-125">Namespace Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2deab-126">-PartitionCount</span><span class="sxs-lookup"><span data-stu-id="2deab-126">-PartitionCount</span></span>
<span data-ttu-id="2deab-127">Eventhub PartitionCount</span><span class="sxs-lookup"><span data-stu-id="2deab-127">Eventhub PartitionCount</span></span>

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

### <span data-ttu-id="2deab-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2deab-128">-ResourceGroupName</span></span>
<span data-ttu-id="2deab-129">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2deab-129">Resource Group Name</span></span>

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

### <span data-ttu-id="2deab-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2deab-130">-Confirm</span></span>
<span data-ttu-id="2deab-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2deab-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2deab-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2deab-132">-WhatIf</span></span>
<span data-ttu-id="2deab-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2deab-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2deab-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2deab-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2deab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2deab-135">CommonParameters</span></span>
<span data-ttu-id="2deab-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2deab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2deab-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2deab-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2deab-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2deab-138">INPUTS</span></span>

### <span data-ttu-id="2deab-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2deab-139">System.String</span></span>
<span data-ttu-id="2deab-140">Microsoft. Azure. Commands. EventHub. models. PSEventHubAttributes system. Nullable ' 1 [[System. Int64, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2deab-140">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes System.Nullable\`1[[System.Int64, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>


## <span data-ttu-id="2deab-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2deab-141">OUTPUTS</span></span>

### <span data-ttu-id="2deab-142">Microsoft. Azure. Commands. EventHub. modele. PSEventHubAttributes</span><span class="sxs-lookup"><span data-stu-id="2deab-142">Microsoft.Azure.Commands.EventHub.Models.PSEventHubAttributes</span></span>


## <span data-ttu-id="2deab-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2deab-143">NOTES</span></span>

## <span data-ttu-id="2deab-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2deab-144">RELATED LINKS</span></span>
