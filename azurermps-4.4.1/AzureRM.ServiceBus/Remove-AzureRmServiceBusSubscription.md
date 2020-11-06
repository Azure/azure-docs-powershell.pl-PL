---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Remove-AzureRmServiceBusSubscription.md
ms.openlocfilehash: c3d4ca61f0bbdc5dcea2eb41a9da0f5de1112719
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542955"
---
# <span data-ttu-id="e9369-101">Remove-AzureRmServiceBusSubscription</span><span class="sxs-lookup"><span data-stu-id="e9369-101">Remove-AzureRmServiceBusSubscription</span></span>

## <span data-ttu-id="e9369-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e9369-102">SYNOPSIS</span></span>
<span data-ttu-id="e9369-103">Usuwa subskrypcję tematu z określonego obszaru nazw usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="e9369-103">Removes the subscription to a topic from the specified Service Bus namespace.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e9369-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e9369-104">SYNTAX</span></span>

```
Remove-AzureRmServiceBusSubscription -ResourceGroupName <String> -Namespace <String> -Topic <String>
 -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e9369-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e9369-105">DESCRIPTION</span></span>
<span data-ttu-id="e9369-106">Polecenie cmdlet **Remove-AzureRmServiceBusSubscription** usuwa abonament do tematu z określonego obszaru nazw magistrali usług.</span><span class="sxs-lookup"><span data-stu-id="e9369-106">The **Remove-AzureRmServiceBusSubscription** cmdlet removes the subscription to a topic from the specified Service Bus namespace.</span></span>

## <span data-ttu-id="e9369-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e9369-107">EXAMPLES</span></span>

### <span data-ttu-id="e9369-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e9369-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmServiceBusSubscription -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_exampl1 -SubscriptionName SB-TopicSubscription-Example1
```

<span data-ttu-id="e9369-109">Usuwa subskrypcję `SB-TopicSubscription-Example1` tematu `SB-Topic_exampl1` w określonym obszarze nazw magistrali usług `SB-Example1` .</span><span class="sxs-lookup"><span data-stu-id="e9369-109">Removes the subscription `SB-TopicSubscription-Example1` to the topic `SB-Topic_exampl1` in the specified Service Bus namespace `SB-Example1`.</span></span>

## <span data-ttu-id="e9369-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e9369-110">PARAMETERS</span></span>

### <span data-ttu-id="e9369-111">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e9369-111">-Confirm</span></span>
<span data-ttu-id="e9369-112">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9369-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e9369-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e9369-113">-WhatIf</span></span>
<span data-ttu-id="e9369-114">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e9369-114">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e9369-115">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e9369-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e9369-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e9369-116">-DefaultProfile</span></span>
<span data-ttu-id="e9369-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e9369-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e9369-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e9369-118">-Name</span></span>
<span data-ttu-id="e9369-119">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="e9369-119">Subscription Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9369-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="e9369-120">-Namespace</span></span>
<span data-ttu-id="e9369-121">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="e9369-121">Namespace Name.</span></span>

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

### <span data-ttu-id="e9369-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e9369-122">-ResourceGroupName</span></span>
<span data-ttu-id="e9369-123">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="e9369-123">The name of the resource group</span></span>

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

### <span data-ttu-id="e9369-124">— Temat</span><span class="sxs-lookup"><span data-stu-id="e9369-124">-Topic</span></span>
<span data-ttu-id="e9369-125">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="e9369-125">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e9369-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e9369-126">CommonParameters</span></span>
<span data-ttu-id="e9369-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e9369-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e9369-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e9369-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e9369-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e9369-129">INPUTS</span></span>

### <span data-ttu-id="e9369-130">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="e9369-130">-ResourceGroup</span></span>
 <span data-ttu-id="e9369-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e9369-131">System.String</span></span>

### <span data-ttu-id="e9369-132">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="e9369-132">-NamespaceName</span></span>
 <span data-ttu-id="e9369-133">System. String</span><span class="sxs-lookup"><span data-stu-id="e9369-133">System.String</span></span>

### <span data-ttu-id="e9369-134">-Tematname</span><span class="sxs-lookup"><span data-stu-id="e9369-134">-TopicName</span></span>
 <span data-ttu-id="e9369-135">System. String</span><span class="sxs-lookup"><span data-stu-id="e9369-135">System.String</span></span>

### <span data-ttu-id="e9369-136">-Subscriptionname</span><span class="sxs-lookup"><span data-stu-id="e9369-136">-SubscriptionName</span></span>
 <span data-ttu-id="e9369-137">System. String</span><span class="sxs-lookup"><span data-stu-id="e9369-137">System.String</span></span>

## <span data-ttu-id="e9369-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e9369-138">OUTPUTS</span></span>

### <span data-ttu-id="e9369-139">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="e9369-139">System.Boolean</span></span>

## <span data-ttu-id="e9369-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e9369-140">NOTES</span></span>

## <span data-ttu-id="e9369-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e9369-141">RELATED LINKS</span></span>

