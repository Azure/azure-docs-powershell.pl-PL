---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/new-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/New-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 34a59f0530ed036397523e3810d68175e7ee2d3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526186"
---
# <span data-ttu-id="65a99-101">New-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="65a99-101">New-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="65a99-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="65a99-102">SYNOPSIS</span></span>
<span data-ttu-id="65a99-103">Tworzy nową grupę użytkowników dla określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="65a99-103">Creates a new consumer group for the specified Event Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65a99-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="65a99-104">SYNTAX</span></span>

```
New-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="65a99-105">Opis</span><span class="sxs-lookup"><span data-stu-id="65a99-105">DESCRIPTION</span></span>
<span data-ttu-id="65a99-106">Tworzy nową grupę użytkowników dla określonego centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="65a99-106">Creates a new consumer group for the specified Event Hub.</span></span>

## <span data-ttu-id="65a99-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="65a99-107">EXAMPLES</span></span>

### <span data-ttu-id="65a99-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="65a99-108">Example 1</span></span>
```
PS C:\> New-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName
```

<span data-ttu-id="65a99-109">Tworzy MyConsumerGroupName grupy konsumenckiej \` \` w MyEventHubName centrum zdarzeń \` \` z zakresem nazw obszar_nazwname \` \` , z MyResourceGroupName grupą zasobów \` \` .</span><span class="sxs-lookup"><span data-stu-id="65a99-109">Creates the consumer group \`MyConsumerGroupName\` in the Event Hub \`MyEventHubName\`, scoped to the namespace \`MyNamespaceName\`, with resource group \`MyResourceGroupName\`.</span></span>

## <span data-ttu-id="65a99-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="65a99-110">PARAMETERS</span></span>

### <span data-ttu-id="65a99-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65a99-111">-DefaultProfile</span></span>
<span data-ttu-id="65a99-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="65a99-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="65a99-113">— EventHub</span><span class="sxs-lookup"><span data-stu-id="65a99-113">-EventHub</span></span>
<span data-ttu-id="65a99-114">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="65a99-114">EventHub Name</span></span>

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

### <span data-ttu-id="65a99-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="65a99-115">-Name</span></span>
<span data-ttu-id="65a99-116">Nazwa odbiorcy</span><span class="sxs-lookup"><span data-stu-id="65a99-116">ConsumerGroup Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65a99-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="65a99-117">-Namespace</span></span>
<span data-ttu-id="65a99-118">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="65a99-118">Namespace Name</span></span>

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

### <span data-ttu-id="65a99-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65a99-119">-ResourceGroupName</span></span>
<span data-ttu-id="65a99-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="65a99-120">Resource Group Name</span></span>

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

### <span data-ttu-id="65a99-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="65a99-121">-UserMetadata</span></span>
<span data-ttu-id="65a99-122">Metadane użytkownika dla usługi Konsumenckej</span><span class="sxs-lookup"><span data-stu-id="65a99-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65a99-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="65a99-123">-Confirm</span></span>
<span data-ttu-id="65a99-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65a99-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="65a99-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="65a99-125">-WhatIf</span></span>
<span data-ttu-id="65a99-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="65a99-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="65a99-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="65a99-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="65a99-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65a99-128">CommonParameters</span></span>
<span data-ttu-id="65a99-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="65a99-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65a99-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65a99-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65a99-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="65a99-131">INPUTS</span></span>

### <span data-ttu-id="65a99-132">System. String</span><span class="sxs-lookup"><span data-stu-id="65a99-132">System.String</span></span>

## <span data-ttu-id="65a99-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="65a99-133">OUTPUTS</span></span>

### <span data-ttu-id="65a99-134">Microsoft. Azure. Commands. EventHub. modele. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="65a99-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="65a99-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="65a99-135">NOTES</span></span>

## <span data-ttu-id="65a99-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="65a99-136">RELATED LINKS</span></span>
