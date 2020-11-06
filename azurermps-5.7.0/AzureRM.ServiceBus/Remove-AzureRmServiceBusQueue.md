---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebusqueue
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: 28c6bf4d463331755121e8a1ea14bf7f93407017
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547963"
---
# <span data-ttu-id="31e24-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="31e24-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="31e24-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31e24-102">SYNOPSIS</span></span>
<span data-ttu-id="31e24-103">Usuwa kolejkę z określonego obszaru nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="31e24-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31e24-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31e24-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueue [-ResourceGroupName] <String> [-Namespace] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31e24-105">Opis</span><span class="sxs-lookup"><span data-stu-id="31e24-105">DESCRIPTION</span></span>
<span data-ttu-id="31e24-106">Polecenie cmdlet **Remove-AzureRmServiceBusQueue** Usuwa kolejkę z określonego obszaru nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="31e24-106">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="31e24-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31e24-107">EXAMPLES</span></span>

### <span data-ttu-id="31e24-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="31e24-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="31e24-109">Usuwa kolejkę `SB-Queue_exampl1` z obszaru nazw `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="31e24-109">Removes the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="31e24-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31e24-110">PARAMETERS</span></span>

### <span data-ttu-id="31e24-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31e24-111">-DefaultProfile</span></span>
<span data-ttu-id="31e24-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="31e24-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31e24-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="31e24-113">-Name</span></span>
<span data-ttu-id="31e24-114">Nazwa kolejki.</span><span class="sxs-lookup"><span data-stu-id="31e24-114">Queue Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31e24-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="31e24-115">-Namespace</span></span>
<span data-ttu-id="31e24-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="31e24-116">Namespace Name.</span></span>

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

### <span data-ttu-id="31e24-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="31e24-117">-ResourceGroupName</span></span>
<span data-ttu-id="31e24-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="31e24-118">The name of the resource group</span></span>

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

### <span data-ttu-id="31e24-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="31e24-119">-Confirm</span></span>
<span data-ttu-id="31e24-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31e24-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="31e24-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31e24-121">-WhatIf</span></span>
<span data-ttu-id="31e24-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31e24-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31e24-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="31e24-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="31e24-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31e24-124">CommonParameters</span></span>
<span data-ttu-id="31e24-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31e24-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31e24-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31e24-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31e24-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31e24-127">INPUTS</span></span>

### <span data-ttu-id="31e24-128">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="31e24-128">-ResourceGroup</span></span>
 <span data-ttu-id="31e24-129">System. String</span><span class="sxs-lookup"><span data-stu-id="31e24-129">System.String</span></span>

### <span data-ttu-id="31e24-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="31e24-130">-NamespaceName</span></span>
 <span data-ttu-id="31e24-131">System. String</span><span class="sxs-lookup"><span data-stu-id="31e24-131">System.String</span></span>

### <span data-ttu-id="31e24-132">-QueueName</span><span class="sxs-lookup"><span data-stu-id="31e24-132">-QueueName</span></span>
 <span data-ttu-id="31e24-133">System. String</span><span class="sxs-lookup"><span data-stu-id="31e24-133">System.String</span></span>

## <span data-ttu-id="31e24-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31e24-134">OUTPUTS</span></span>

### <span data-ttu-id="31e24-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="31e24-135">System.Object</span></span>

## <span data-ttu-id="31e24-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31e24-136">NOTES</span></span>

## <span data-ttu-id="31e24-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31e24-137">RELATED LINKS</span></span>

