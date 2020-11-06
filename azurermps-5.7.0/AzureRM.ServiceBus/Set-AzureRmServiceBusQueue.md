---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/set-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Set-AzureRmServiceBusQueue.md
ms.openlocfilehash: 785685981c38248fba944cc9e3809a2de1f32e71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544108"
---
# <span data-ttu-id="bf80e-101">Set-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="bf80e-101">Set-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="bf80e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bf80e-102">SYNOPSIS</span></span>
<span data-ttu-id="bf80e-103">Umożliwia zaktualizowanie opisu kolejki usługi Service Bus w określonym obszarze nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="bf80e-103">Updates the description of a Service Bus queue in the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf80e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bf80e-104">SYNTAX</span></span>

```
Set-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-InputObject] <QueueAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="bf80e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bf80e-105">DESCRIPTION</span></span>
<span data-ttu-id="bf80e-106">Polecenie cmdlet **Set-AzureRmServiceBusQueue** umożliwia zaktualizowanie opisu kolejki magistrali usług w określonym obszarze nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="bf80e-106">The **Set-AzureRmServiceBusQueue** cmdlet updates the description for the Service Bus queue in the specified Service Bus namespace.</span></span>

## <span data-ttu-id="bf80e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bf80e-107">EXAMPLES</span></span>

### <span data-ttu-id="bf80e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bf80e-108">Example 1</span></span>
```
PS C:\> $QueueObj = Get-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1

PS C:\> $QueueObj.DeadLetteringOnMessageExpiration = $True
PS C:\> $QueueObj.SupportOrdering = $True

PS C:\> Set-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -QueueObj $QueueObj

Name                                : SB-Queue_exampl1
LockDuration                        : 
AccessedAt                          : 1/1/0001 12:00:00 AM
AutoDeleteOnIdle                    : 10675199.02:48:05.4775807
CreatedAt                           : 1/20/2017 2:51:34 AM
DefaultMessageTimeToLive            : 10675199.02:48:05.4775807
DuplicateDetectionHistoryTimeWindow : 
DeadLetteringOnMessageExpiration    : False
EnableExpress                       : False
EnablePartitioning                  : True
MaxDeliveryCount                    : 
MaxSizeInMegabytes                  : 16384
MessageCount                        : 
CountDetails                        : Microsoft.Azure.Management.ServiceBus.Models.MessageCountDetails
RequiresDuplicateDetection          : False
RequiresSession                     : False
SizeInBytes                         : 
Status                              : Active
UpdatedAt                           : 1/20/2017 6:16:18 PM
```

<span data-ttu-id="bf80e-109">Aktualizuje określoną kolejkę o nowy opis w określonej przestrzeni nazw.</span><span class="sxs-lookup"><span data-stu-id="bf80e-109">Updates the specified queue with a new description in the specified namespace.</span></span> <span data-ttu-id="bf80e-110">W tym przykładzie jest aktualizowana Właściwość **DeadLetteringOnMessageExpiration** na wartość **true** i **SupportOrdering** na **wartość true**.</span><span class="sxs-lookup"><span data-stu-id="bf80e-110">This example updates the **DeadLetteringOnMessageExpiration** property to **true** and **SupportOrdering** to **true**.</span></span>

## <span data-ttu-id="bf80e-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bf80e-111">PARAMETERS</span></span>

### <span data-ttu-id="bf80e-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf80e-112">-DefaultProfile</span></span>
<span data-ttu-id="bf80e-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bf80e-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bf80e-114">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="bf80e-114">-InputObject</span></span>
<span data-ttu-id="bf80e-115">Definicja ServiceBus.</span><span class="sxs-lookup"><span data-stu-id="bf80e-115">ServiceBus definition.</span></span>

```yaml
Type: PSQueueAttributes
Parameter Sets: (All)
Aliases: QueueObj

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf80e-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bf80e-116">-Name</span></span>
<span data-ttu-id="bf80e-117">Nazwa kolejki.</span><span class="sxs-lookup"><span data-stu-id="bf80e-117">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf80e-118">-Namespace</span><span class="sxs-lookup"><span data-stu-id="bf80e-118">-Namespace</span></span>
<span data-ttu-id="bf80e-119">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="bf80e-119">Namespace Name.</span></span>

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

### <span data-ttu-id="bf80e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf80e-120">-ResourceGroupName</span></span>
<span data-ttu-id="bf80e-121">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bf80e-121">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf80e-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bf80e-122">-Confirm</span></span>
<span data-ttu-id="bf80e-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf80e-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf80e-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf80e-124">-WhatIf</span></span>
<span data-ttu-id="bf80e-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bf80e-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf80e-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bf80e-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf80e-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf80e-127">CommonParameters</span></span>
<span data-ttu-id="bf80e-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bf80e-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf80e-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf80e-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf80e-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bf80e-130">INPUTS</span></span>

### <span data-ttu-id="bf80e-131">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="bf80e-131">-ResourceGroup</span></span>
 <span data-ttu-id="bf80e-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bf80e-132">System.String</span></span>

### <span data-ttu-id="bf80e-133">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="bf80e-133">-NamespaceName</span></span>
 <span data-ttu-id="bf80e-134">System. String</span><span class="sxs-lookup"><span data-stu-id="bf80e-134">System.String</span></span>

### <span data-ttu-id="bf80e-135">-QueueName</span><span class="sxs-lookup"><span data-stu-id="bf80e-135">-QueueName</span></span>
 <span data-ttu-id="bf80e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="bf80e-136">System.String</span></span>

### <span data-ttu-id="bf80e-137">-QueueObj</span><span class="sxs-lookup"><span data-stu-id="bf80e-137">-QueueObj</span></span>
 <span data-ttu-id="bf80e-138">Microsoft. Azure. Commands. ServiceBus. models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="bf80e-138">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="bf80e-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bf80e-139">OUTPUTS</span></span>

### <span data-ttu-id="bf80e-140">Microsoft. Azure. Commands. ServiceBus. models. PSQueueAttributes</span><span class="sxs-lookup"><span data-stu-id="bf80e-140">Microsoft.Azure.Commands.ServiceBus.Models.PSQueueAttributes</span></span>

## <span data-ttu-id="bf80e-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bf80e-141">NOTES</span></span>

## <span data-ttu-id="bf80e-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bf80e-142">RELATED LINKS</span></span>

