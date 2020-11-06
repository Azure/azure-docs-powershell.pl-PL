---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 93efa23e802c3470d1bd1470cadd0f070cc34422
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542963"
---
# <span data-ttu-id="a9929-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a9929-101">Remove-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="a9929-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a9929-102">SYNOPSIS</span></span>
<span data-ttu-id="a9929-103">Usuwa regułę autoryzacji kolejki z określonego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="a9929-103">Removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9929-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a9929-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a9929-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a9929-105">DESCRIPTION</span></span>
<span data-ttu-id="a9929-106">Polecenie cmdlet **Remove-AzureRmServiceBusQueueAuthorizationRule** usuwa regułę autoryzacji kolejki z określonego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="a9929-106">The **Remove-AzureRmServiceBusQueueAuthorizationRule** cmdlet removes the authorization rule of a queue from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="a9929-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a9929-107">EXAMPLES</span></span>

### <span data-ttu-id="a9929-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a9929-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="a9929-109">Usuwa `SBAuthoRule1` z obszaru nazw regułę autoryzacji kolejki `SB-Queue_exampl1` `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="a9929-109">Removes the authorization rule `SBAuthoRule1` of the queue `SB-Queue_exampl1` from the namespace `SB-Example1`.</span></span>

## <span data-ttu-id="a9929-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a9929-110">PARAMETERS</span></span>

### <span data-ttu-id="a9929-111">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a9929-111">-ResourceGroup</span></span>
<span data-ttu-id="a9929-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a9929-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="a9929-113">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a9929-113">-Confirm</span></span>
<span data-ttu-id="a9929-114">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9929-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9929-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9929-115">-WhatIf</span></span>
<span data-ttu-id="a9929-116">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a9929-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9929-117">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a9929-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9929-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9929-118">-DefaultProfile</span></span>
<span data-ttu-id="a9929-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a9929-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a9929-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a9929-120">-Name</span></span>
<span data-ttu-id="a9929-121">Nazwa AuthorizationRule kolejki.</span><span class="sxs-lookup"><span data-stu-id="a9929-121">Queue AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9929-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a9929-122">-Namespace</span></span>
<span data-ttu-id="a9929-123">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="a9929-123">Namespace Name.</span></span>

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

### <span data-ttu-id="a9929-124">-Queue</span><span class="sxs-lookup"><span data-stu-id="a9929-124">-Queue</span></span>
<span data-ttu-id="a9929-125">Nazwa kolejki.</span><span class="sxs-lookup"><span data-stu-id="a9929-125">Queue Name.</span></span>

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

### <span data-ttu-id="a9929-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9929-126">CommonParameters</span></span>
<span data-ttu-id="a9929-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9929-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9929-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9929-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9929-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a9929-129">INPUTS</span></span>

### <span data-ttu-id="a9929-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="a9929-130">-ResourceGroup</span></span>
 <span data-ttu-id="a9929-131">System. String</span><span class="sxs-lookup"><span data-stu-id="a9929-131">System.String</span></span>

### <span data-ttu-id="a9929-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="a9929-132">-NamespaceName</span></span>
 <span data-ttu-id="a9929-133">System. String</span><span class="sxs-lookup"><span data-stu-id="a9929-133">System.String</span></span>

### <span data-ttu-id="a9929-134">-QueueName</span><span class="sxs-lookup"><span data-stu-id="a9929-134">-QueueName</span></span>
 <span data-ttu-id="a9929-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a9929-135">System.String</span></span>

### <span data-ttu-id="a9929-136">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="a9929-136">-AuthorizationRuleName</span></span>
 <span data-ttu-id="a9929-137">System. String</span><span class="sxs-lookup"><span data-stu-id="a9929-137">System.String</span></span>

## <span data-ttu-id="a9929-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a9929-138">OUTPUTS</span></span>

### <span data-ttu-id="a9929-139">System. Object</span><span class="sxs-lookup"><span data-stu-id="a9929-139">System.Object</span></span>

## <span data-ttu-id="a9929-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a9929-140">NOTES</span></span>

## <span data-ttu-id="a9929-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a9929-141">RELATED LINKS</span></span>

