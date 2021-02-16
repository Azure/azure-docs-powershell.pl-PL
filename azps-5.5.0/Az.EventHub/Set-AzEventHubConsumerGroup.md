---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubconsumergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubConsumerGroup.md
ms.openlocfilehash: cb898921b7fdfddddc95fc88d49dade4654c7ad2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194371"
---
# <span data-ttu-id="74b81-101">Set-AzEventHubConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="74b81-101">Set-AzEventHubConsumerGroup</span></span>

## <span data-ttu-id="74b81-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74b81-102">SYNOPSIS</span></span>
<span data-ttu-id="74b81-103">Aktualizuje określoną grupę klientów z centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="74b81-103">Updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="74b81-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="74b81-104">SYNTAX</span></span>

```
Set-AzEventHubConsumerGroup [-ResourceGroupName] <String> [-Namespace] <String> [-EventHub] <String>
 [-Name] <String> [[-UserMetadata] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="74b81-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="74b81-105">DESCRIPTION</span></span>
<span data-ttu-id="74b81-106">Polecenie Set-AzEventHubConsumerGroup aktualizuje określoną grupę klientów centrum zdarzeń.</span><span class="sxs-lookup"><span data-stu-id="74b81-106">The Set-AzEventHubConsumerGroup cmdlet updates the specified Event Hubs consumer group.</span></span>

## <span data-ttu-id="74b81-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="74b81-107">EXAMPLES</span></span>

### <span data-ttu-id="74b81-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="74b81-108">Example 1</span></span>
```
PS C:\> Set-AzEventHubConsumerGroup -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -EventHubName MyEventHubName -ConsumerGroupName MyConsumerGroupName -UserMetadata "Testing"
```

<span data-ttu-id="74b81-109">Ustawia metadane użytkownika grupy klientów \` MyConsumerGroupName na \` "Testowanie".</span><span class="sxs-lookup"><span data-stu-id="74b81-109">Sets the user metadata of the consumer group \`MyConsumerGroupName\` to "Testing."</span></span>

## <span data-ttu-id="74b81-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74b81-110">PARAMETERS</span></span>

### <span data-ttu-id="74b81-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74b81-111">-DefaultProfile</span></span>
<span data-ttu-id="74b81-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="74b81-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="74b81-113">-EventHub</span><span class="sxs-lookup"><span data-stu-id="74b81-113">-EventHub</span></span>
<span data-ttu-id="74b81-114">Nazwa aplikacji EventHub</span><span class="sxs-lookup"><span data-stu-id="74b81-114">EventHub Name</span></span>

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

### <span data-ttu-id="74b81-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="74b81-115">-Name</span></span>
<span data-ttu-id="74b81-116">Nazwa grupy konsumenckiej</span><span class="sxs-lookup"><span data-stu-id="74b81-116">ConsumerGroup Name</span></span>

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

### <span data-ttu-id="74b81-117">—Przestrzeń nazw</span><span class="sxs-lookup"><span data-stu-id="74b81-117">-Namespace</span></span>
<span data-ttu-id="74b81-118">Nazwa przestrzeni nazw</span><span class="sxs-lookup"><span data-stu-id="74b81-118">Namespace Name</span></span>

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

### <span data-ttu-id="74b81-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74b81-119">-ResourceGroupName</span></span>
<span data-ttu-id="74b81-120">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="74b81-120">Resource Group Name</span></span>

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

### <span data-ttu-id="74b81-121">-UserMetadata</span><span class="sxs-lookup"><span data-stu-id="74b81-121">-UserMetadata</span></span>
<span data-ttu-id="74b81-122">Metadane użytkownika dla grupy ConsumerGroup</span><span class="sxs-lookup"><span data-stu-id="74b81-122">User Metadata for ConsumerGroup</span></span>

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

### <span data-ttu-id="74b81-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="74b81-123">-Confirm</span></span>
<span data-ttu-id="74b81-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="74b81-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74b81-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74b81-125">-WhatIf</span></span>
<span data-ttu-id="74b81-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="74b81-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="74b81-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="74b81-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74b81-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74b81-128">CommonParameters</span></span>
<span data-ttu-id="74b81-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74b81-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74b81-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74b81-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74b81-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74b81-131">INPUTS</span></span>

### <span data-ttu-id="74b81-132">System.String</span><span class="sxs-lookup"><span data-stu-id="74b81-132">System.String</span></span>

## <span data-ttu-id="74b81-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="74b81-133">OUTPUTS</span></span>

### <span data-ttu-id="74b81-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span><span class="sxs-lookup"><span data-stu-id="74b81-134">Microsoft.Azure.Commands.EventHub.Models.PSConsumerGroupAttributes</span></span>

## <span data-ttu-id="74b81-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="74b81-135">NOTES</span></span>

## <span data-ttu-id="74b81-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="74b81-136">RELATED LINKS</span></span>
