---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueue.md
ms.openlocfilehash: 8c5c614a041ff0e4ab9bc4fdc0aea944901d1efc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542960"
---
# <span data-ttu-id="439cf-101">Remove-AzureRmServiceBusQueue</span><span class="sxs-lookup"><span data-stu-id="439cf-101">Remove-AzureRmServiceBusQueue</span></span>

## <span data-ttu-id="439cf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="439cf-102">SYNOPSIS</span></span>
<span data-ttu-id="439cf-103">Usuwa kolejkę z określonego obszaru nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="439cf-103">Removes the queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="439cf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="439cf-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueue -ResourceGroupName <String> -Namespace <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="439cf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="439cf-105">DESCRIPTION</span></span>
<span data-ttu-id="439cf-106">Polecenie cmdlet **Remove-AzureRmServiceBusQueue** Usuwa kolejkę z określonego obszaru nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="439cf-106">The **Remove-AzureRmServiceBusQueue** cmdlet removes the queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="439cf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="439cf-107">EXAMPLES</span></span>

### <span data-ttu-id="439cf-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="439cf-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueue -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1
```

<span data-ttu-id="439cf-109">Usuwa kolejkę `SB-Queue_exampl1` z obszaru nazw `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="439cf-109">Removes the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="439cf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="439cf-110">PARAMETERS</span></span>

### <span data-ttu-id="439cf-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="439cf-111">-Confirm</span></span>
<span data-ttu-id="439cf-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="439cf-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439cf-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="439cf-113">-WhatIf</span></span>
<span data-ttu-id="439cf-114">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="439cf-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="439cf-115">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="439cf-115">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="439cf-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="439cf-116">-DefaultProfile</span></span>
<span data-ttu-id="439cf-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="439cf-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="439cf-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="439cf-118">-Name</span></span>
<span data-ttu-id="439cf-119">Nazwa kolejki.</span><span class="sxs-lookup"><span data-stu-id="439cf-119">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: QueueName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="439cf-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="439cf-120">-Namespace</span></span>
<span data-ttu-id="439cf-121">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="439cf-121">Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="439cf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="439cf-122">-ResourceGroupName</span></span>
<span data-ttu-id="439cf-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="439cf-123">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="439cf-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="439cf-124">CommonParameters</span></span>
<span data-ttu-id="439cf-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="439cf-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="439cf-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="439cf-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="439cf-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="439cf-127">INPUTS</span></span>

### <span data-ttu-id="439cf-128">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="439cf-128">-ResourceGroup</span></span>
 <span data-ttu-id="439cf-129">System. String</span><span class="sxs-lookup"><span data-stu-id="439cf-129">System.String</span></span>

### <span data-ttu-id="439cf-130">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="439cf-130">-NamespaceName</span></span>
 <span data-ttu-id="439cf-131">System. String</span><span class="sxs-lookup"><span data-stu-id="439cf-131">System.String</span></span>

### <span data-ttu-id="439cf-132">-QueueName</span><span class="sxs-lookup"><span data-stu-id="439cf-132">-QueueName</span></span>
 <span data-ttu-id="439cf-133">System. String</span><span class="sxs-lookup"><span data-stu-id="439cf-133">System.String</span></span>

## <span data-ttu-id="439cf-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="439cf-134">OUTPUTS</span></span>

### <span data-ttu-id="439cf-135">System. Object</span><span class="sxs-lookup"><span data-stu-id="439cf-135">System.Object</span></span>

## <span data-ttu-id="439cf-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="439cf-136">NOTES</span></span>

## <span data-ttu-id="439cf-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="439cf-137">RELATED LINKS</span></span>

