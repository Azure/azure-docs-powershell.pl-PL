---
external help file: Microsoft.Azure.Commands.EventHub.dll-Help.xml
Module Name: AzureRM.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.eventhub/set-azurermeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/EventHub/Commands.EventHub/help/Set-AzureRmEventHubConsumerGroup.md
ms.openlocfilehash: 743928771fdba7ed17fe2643cf9e92ae7c2d9860
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525129"
---
# <span data-ttu-id="9586f-101">Set-AzureRmEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="9586f-101">Set-AzureRmEventHubConsumerGroup</span></span>

## <span data-ttu-id="9586f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9586f-102">SYNOPSIS</span></span>
<span data-ttu-id="9586f-103">Aktualizuje określoną grupę klientów koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="9586f-103">Updates the specified Event Hubs consumer group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9586f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9586f-104">SYNTAX</span></span>

```
Set-AzureRmEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9586f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9586f-105">DESCRIPTION</span></span>
<span data-ttu-id="9586f-106">Polecenie cmdlet Set-AzureRmEventHubConsumerGroup aktualizuje określoną grupę klientów koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="9586f-106">The Set-AzureRmEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="9586f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9586f-107">EXAMPLES</span></span>

### <span data-ttu-id="9586f-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9586f-108">Example 1</span></span>
```
PS C:\> Set-AzureRmEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="9586f-109">Ustawia metadane użytkownika grupy \` MyConsumerGroupName \` na "testowanie".</span><span class="sxs-lookup"><span data-stu-id="9586f-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="9586f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9586f-110">PARAMETERS</span></span>

### <span data-ttu-id="9586f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9586f-111">-DefaultProfile</span></span>
<span data-ttu-id="9586f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9586f-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9586f-113">— EventHub</span><span class="sxs-lookup"><span data-stu-id="9586f-113">-EventHub</span></span>
<span data-ttu-id="9586f-114">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="9586f-114">EventHub Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: EventHubName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9586f-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9586f-115">-Name</span></span>
<span data-ttu-id="9586f-116">Nazwa odbiorcy</span><span class="sxs-lookup"><span data-stu-id="9586f-116">ConsumerGroup Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ConsumerGroupName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9586f-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9586f-117">-Namespace</span></span>
<span data-ttu-id="9586f-118">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="9586f-118">Namespace Name</span></span>

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

### <span data-ttu-id="9586f-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9586f-119">-ResourceGroupName</span></span>
<span data-ttu-id="9586f-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="9586f-120">Resource Group Name</span></span>

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

### <span data-ttu-id="9586f-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="9586f-121">-UserMetadata</span></span>
<span data-ttu-id="9586f-122">Metadane użytkownika dla usługi Konsumenckej</span><span class="sxs-lookup"><span data-stu-id="9586f-122">User Metadata for ConsumerGroup</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9586f-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9586f-123">-Confirm</span></span>
<span data-ttu-id="9586f-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9586f-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9586f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9586f-125">-WhatIf</span></span>
<span data-ttu-id="9586f-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9586f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9586f-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9586f-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9586f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9586f-128">CommonParameters</span></span>
<span data-ttu-id="9586f-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9586f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="9586f-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9586f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9586f-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9586f-131">INPUTS</span></span>

### <span data-ttu-id="9586f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9586f-132">System.String</span></span>


## <span data-ttu-id="9586f-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9586f-133">OUTPUTS</span></span>

### <span data-ttu-id="9586f-134">Microsoft. Azure. Commands. EventHub. modele. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="9586f-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>


## <span data-ttu-id="9586f-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9586f-135">NOTES</span></span>

## <span data-ttu-id="9586f-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9586f-136">RELATED LINKS</span></span>