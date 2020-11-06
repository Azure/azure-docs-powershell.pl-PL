---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusQueueAuthorizationRule.md
ms.openlocfilehash: 5d3f9212fcaf55d6506723b6c29ed1da0d676bb1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542984"
---
# <span data-ttu-id="9bf5d-101">Get-AzureRmServiceBusQueueAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="9bf5d-101">Get-AzureRmServiceBusQueueAuthorizationRule</span></span>

## <span data-ttu-id="9bf5d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9bf5d-102">SYNOPSIS</span></span>
<span data-ttu-id="9bf5d-103">Pobiera opis określonej reguły autoryzacji dla danej kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="9bf5d-103">Gets the description of a specified authorization rule for a given Service Bus queue.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9bf5d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9bf5d-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusQueueAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Queue <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9bf5d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9bf5d-105">DESCRIPTION</span></span>
<span data-ttu-id="9bf5d-106">Polecenie cmdlet **Get-AzureRmServiceBusQueueAuthorizationRule** Pobiera opis określonej reguły autoryzacji w danej kolejce usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="9bf5d-106">The **Get-AzureRmServiceBusQueueAuthorizationRule** cmdlet gets the description of a specified authorization rule on the given Service Bus queue.</span></span>

## <span data-ttu-id="9bf5d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9bf5d-107">EXAMPLES</span></span>

### <span data-ttu-id="9bf5d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9bf5d-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusQueueAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -QueueName SB-Queue_exampl1 -AuthorizationRuleName SBAuthoRule1
```

<span data-ttu-id="9bf5d-109">Zwraca opis określonej reguły autoryzacji danej kolejki usługi Service Bus.</span><span class="sxs-lookup"><span data-stu-id="9bf5d-109">Returns the specified authorization rule description for a given Service Bus queue.</span></span>

## <span data-ttu-id="9bf5d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9bf5d-110">PARAMETERS</span></span>

### <span data-ttu-id="9bf5d-111">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9bf5d-111">-ResourceGroup</span></span>
<span data-ttu-id="9bf5d-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9bf5d-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="9bf5d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9bf5d-113">-DefaultProfile</span></span>
<span data-ttu-id="9bf5d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9bf5d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9bf5d-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9bf5d-115">-Name</span></span>
<span data-ttu-id="9bf5d-116">Nazwa AuthorizationRule EventHub.</span><span class="sxs-lookup"><span data-stu-id="9bf5d-116">EventHub AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9bf5d-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="9bf5d-117">-Namespace</span></span>
<span data-ttu-id="9bf5d-118">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="9bf5d-118">Namespace Name.</span></span>

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

### <span data-ttu-id="9bf5d-119">-Queue</span><span class="sxs-lookup"><span data-stu-id="9bf5d-119">-Queue</span></span>
<span data-ttu-id="9bf5d-120">Nazwa kolejki.</span><span class="sxs-lookup"><span data-stu-id="9bf5d-120">Queue Name.</span></span>

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

### <span data-ttu-id="9bf5d-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9bf5d-121">CommonParameters</span></span>
<span data-ttu-id="9bf5d-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9bf5d-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9bf5d-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9bf5d-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9bf5d-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9bf5d-124">INPUTS</span></span>

### <span data-ttu-id="9bf5d-125">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="9bf5d-125">-ResourceGroup</span></span>
 <span data-ttu-id="9bf5d-126">System. String</span><span class="sxs-lookup"><span data-stu-id="9bf5d-126">System.String</span></span>
 

### <span data-ttu-id="9bf5d-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="9bf5d-127">-NamespaceName</span></span>
 <span data-ttu-id="9bf5d-128">System. String</span><span class="sxs-lookup"><span data-stu-id="9bf5d-128">System.String</span></span>
 

### <span data-ttu-id="9bf5d-129">-QueueName</span><span class="sxs-lookup"><span data-stu-id="9bf5d-129">-QueueName</span></span>
 <span data-ttu-id="9bf5d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="9bf5d-130">System.String</span></span>
 

### <span data-ttu-id="9bf5d-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="9bf5d-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="9bf5d-132">System. String</span><span class="sxs-lookup"><span data-stu-id="9bf5d-132">System.String</span></span>

## <span data-ttu-id="9bf5d-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9bf5d-133">OUTPUTS</span></span>

### <span data-ttu-id="9bf5d-134">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. ServiceBus. MODELES. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9bf5d-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="9bf5d-135">Identyfikator:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onrules/SBAuthoRule1 typ: Microsoft. ServiceBus/AuthorizationRules Name: SBAuthoRule1 Location: zachód AMERYKAŃSKIe znaczniki: prawa: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="9bf5d-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/queues/SB-Queue_exampl1/authorizati onRules/SBAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="9bf5d-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9bf5d-136">NOTES</span></span>

## <span data-ttu-id="9bf5d-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9bf5d-137">RELATED LINKS</span></span>

