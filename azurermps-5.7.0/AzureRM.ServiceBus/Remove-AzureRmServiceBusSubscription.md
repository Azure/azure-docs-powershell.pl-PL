---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/remove-azurermservicebussubscription
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: 80b3a5ce4cb38222993e69181519a864c578cf67
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551575"
---
# <span data-ttu-id="252ab-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="252ab-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="252ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="252ab-102">SYNOPSIS</span></span>
<span data-ttu-id="252ab-103">Usuwa subskrypcję tematu z określonego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="252ab-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="252ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="252ab-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusSubscription [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="252ab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="252ab-105">DESCRIPTION</span></span>
<span data-ttu-id="252ab-106">Polecenie cmdlet **Remove-AzureRmServiceBusSubscription** usuwa abonament do tematu z określonego obszaru nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="252ab-106">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="252ab-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="252ab-107">EXAMPLES</span></span>

### <span data-ttu-id="252ab-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="252ab-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="252ab-109">Usuwa subskrypcję `SB-TopicSubscription-Example1` tematu `SB-Topic_exampl1` w określonym obszarze nazw magistrali usług `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="252ab-109">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="252ab-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="252ab-110">PARAMETERS</span></span>

### <span data-ttu-id="252ab-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="252ab-111">-DefaultProfile</span></span>
<span data-ttu-id="252ab-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="252ab-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="252ab-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="252ab-113">-Name</span></span>
<span data-ttu-id="252ab-114">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="252ab-114">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="252ab-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="252ab-115">-Namespace</span></span>
<span data-ttu-id="252ab-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="252ab-116">Namespace Name.</span></span>

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

### <span data-ttu-id="252ab-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="252ab-117">-ResourceGroupName</span></span>
<span data-ttu-id="252ab-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="252ab-118">The name of the resource group</span></span>

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

### <span data-ttu-id="252ab-119">— Temat</span><span class="sxs-lookup"><span data-stu-id="252ab-119">-Topic</span></span>
<span data-ttu-id="252ab-120">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="252ab-120">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="252ab-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="252ab-121">-Confirm</span></span>
<span data-ttu-id="252ab-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="252ab-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="252ab-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="252ab-123">-WhatIf</span></span>
<span data-ttu-id="252ab-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="252ab-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="252ab-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="252ab-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="252ab-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="252ab-126">CommonParameters</span></span>
<span data-ttu-id="252ab-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="252ab-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="252ab-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="252ab-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="252ab-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="252ab-129">INPUTS</span></span>

### <span data-ttu-id="252ab-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="252ab-130">-ResourceGroup</span></span>
 <span data-ttu-id="252ab-131">System. String</span><span class="sxs-lookup"><span data-stu-id="252ab-131">System.String</span></span>

### <span data-ttu-id="252ab-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="252ab-132">-NamespaceName</span></span>
 <span data-ttu-id="252ab-133">System. String</span><span class="sxs-lookup"><span data-stu-id="252ab-133">System.String</span></span>

### <span data-ttu-id="252ab-134">-Tematname</span><span class="sxs-lookup"><span data-stu-id="252ab-134">-TopicName</span></span>
 <span data-ttu-id="252ab-135">System. String</span><span class="sxs-lookup"><span data-stu-id="252ab-135">System.String</span></span>

### <span data-ttu-id="252ab-136">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="252ab-136">-SubscriptionName</span></span>
 <span data-ttu-id="252ab-137">System. String</span><span class="sxs-lookup"><span data-stu-id="252ab-137">System.String</span></span>

## <span data-ttu-id="252ab-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="252ab-138">OUTPUTS</span></span>

### <span data-ttu-id="252ab-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="252ab-139">System.Boolean</span></span>

## <span data-ttu-id="252ab-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="252ab-140">NOTES</span></span>

## <span data-ttu-id="252ab-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="252ab-141">RELATED LINKS</span></span>

