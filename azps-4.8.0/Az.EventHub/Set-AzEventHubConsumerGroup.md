---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
ms.openlocfilehash: cb898921b7fdfddddc95fc88d49dade4654c7ad2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062240"
---
# <span data-ttu-id="dd552-101">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="dd552-101">Set-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="dd552-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd552-102">SYNOPSIS</span></span>
<span data-ttu-id="dd552-103">Aktualizuje określoną grupę klientów koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="dd552-103">Updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="dd552-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd552-104">SYNTAX</span></span>

```
Set-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dd552-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dd552-105">DESCRIPTION</span></span>
<span data-ttu-id="dd552-106">Polecenie cmdlet Set-AzEventHubConsumerGroup aktualizuje określoną grupę klientów koncentratorów zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="dd552-106">The Set-AzEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="dd552-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd552-107">EXAMPLES</span></span>

### <span data-ttu-id="dd552-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dd552-108">Example 1</span></span>
```
PS C:\> Set-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="dd552-109">Ustawia metadane użytkownika grupy \` MyConsumerGroupName \` na "testowanie".</span><span class="sxs-lookup"><span data-stu-id="dd552-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="dd552-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd552-110">PARAMETERS</span></span>

### <span data-ttu-id="dd552-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd552-111">-DefaultProfile</span></span>
<span data-ttu-id="dd552-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd552-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd552-113">— EventHub</span><span class="sxs-lookup"><span data-stu-id="dd552-113">-EventHub</span></span>
<span data-ttu-id="dd552-114">Nazwa EventHub</span><span class="sxs-lookup"><span data-stu-id="dd552-114">EventHub Name</span></span>

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

### <span data-ttu-id="dd552-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dd552-115">-Name</span></span>
<span data-ttu-id="dd552-116">Nazwa odbiorcy</span><span class="sxs-lookup"><span data-stu-id="dd552-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="dd552-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="dd552-117">-Namespace</span></span>
<span data-ttu-id="dd552-118">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="dd552-118">Namespace Name</span></span>

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

### <span data-ttu-id="dd552-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd552-119">-ResourceGroupName</span></span>
<span data-ttu-id="dd552-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="dd552-120">Resource Group Name</span></span>

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

### <span data-ttu-id="dd552-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="dd552-121">-UserMetadata</span></span>
<span data-ttu-id="dd552-122">Metadane użytkownika dla usługi Konsumenckej</span><span class="sxs-lookup"><span data-stu-id="dd552-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="dd552-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd552-123">-Confirm</span></span>
<span data-ttu-id="dd552-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd552-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd552-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd552-125">-WhatIf</span></span>
<span data-ttu-id="dd552-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd552-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd552-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="dd552-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd552-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd552-128">CommonParameters</span></span>
<span data-ttu-id="dd552-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd552-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd552-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd552-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd552-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd552-131">INPUTS</span></span>

### <span data-ttu-id="dd552-132">System. String</span><span class="sxs-lookup"><span data-stu-id="dd552-132">System.String</span></span>

## <span data-ttu-id="dd552-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd552-133">OUTPUTS</span></span>

### <span data-ttu-id="dd552-134">Microsoft. Azure. Commands. EventHub. modele. PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="dd552-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="dd552-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd552-135">NOTES</span></span>

## <span data-ttu-id="dd552-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd552-136">RELATED LINKS</span></span>
