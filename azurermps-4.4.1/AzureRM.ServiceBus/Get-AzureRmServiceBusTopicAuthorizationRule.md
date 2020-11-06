---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusTopicAuthorizationRule.md
ms.openlocfilehash: e8bcb3688aec6d718c192e4dac4b6b4632eba059
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552359"
---
# <span data-ttu-id="f56c4-101">Get-AzureRmServiceBusTopicAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="f56c4-101">Get-AzureRmServiceBusTopicAuthorizationRule</span></span>

## <span data-ttu-id="f56c4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f56c4-102">SYNOPSIS</span></span>
<span data-ttu-id="f56c4-103">Zwraca opis określonego opisu reguły autoryzacji dla danego tematu.</span><span class="sxs-lookup"><span data-stu-id="f56c4-103">Returns the description of the specified authorization rule description for the given topic.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f56c4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f56c4-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusTopicAuthorizationRule [-ResourceGroup] <String> -Namespace <String> -Topic <String>
 [-Name <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f56c4-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f56c4-105">DESCRIPTION</span></span>
<span data-ttu-id="f56c4-106">Polecenie cmdlet **Get-AzureRmServiceBusTopicAuthorizationRule** Pobiera opis określonej reguły autoryzacji w danym temacie Magistrala usług.</span><span class="sxs-lookup"><span data-stu-id="f56c4-106">The **Get-AzureRmServiceBusTopicAuthorizationRule** cmdlet gets the description of the specified authorization rule on the given Service Bus topic.</span></span>

## <span data-ttu-id="f56c4-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f56c4-107">EXAMPLES</span></span>

### <span data-ttu-id="f56c4-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f56c4-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusTopicAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -NamespaceName SB-Example1 -TopicName SB-Topic_example1 -AuthorizationRuleName SBTopicAuthoRule1
```

<span data-ttu-id="f56c4-109">Zwraca opis określonej reguły autoryzacji dla danego tematu.</span><span class="sxs-lookup"><span data-stu-id="f56c4-109">Returns the description of the specified authorization rule for the given topic.</span></span>

## <span data-ttu-id="f56c4-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f56c4-110">PARAMETERS</span></span>

### <span data-ttu-id="f56c4-111">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f56c4-111">-ResourceGroup</span></span>
<span data-ttu-id="f56c4-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="f56c4-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="f56c4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f56c4-113">-DefaultProfile</span></span>
<span data-ttu-id="f56c4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f56c4-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f56c4-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f56c4-115">-Name</span></span>
<span data-ttu-id="f56c4-116">Temat AuthorizationRule nazwa.</span><span class="sxs-lookup"><span data-stu-id="f56c4-116">Topic AuthorizationRule Name.</span></span>

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

### <span data-ttu-id="f56c4-117">-Namespace</span><span class="sxs-lookup"><span data-stu-id="f56c4-117">-Namespace</span></span>
<span data-ttu-id="f56c4-118">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="f56c4-118">Namespace Name.</span></span>

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

### <span data-ttu-id="f56c4-119">— Temat</span><span class="sxs-lookup"><span data-stu-id="f56c4-119">-Topic</span></span>
<span data-ttu-id="f56c4-120">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="f56c4-120">Topic Name.</span></span>

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

### <span data-ttu-id="f56c4-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f56c4-121">CommonParameters</span></span>
<span data-ttu-id="f56c4-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f56c4-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f56c4-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f56c4-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f56c4-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f56c4-124">INPUTS</span></span>

### <span data-ttu-id="f56c4-125">-ResourceName</span><span class="sxs-lookup"><span data-stu-id="f56c4-125">-ResourceGroup</span></span>
 <span data-ttu-id="f56c4-126">System. String</span><span class="sxs-lookup"><span data-stu-id="f56c4-126">System.String</span></span>
 

### <span data-ttu-id="f56c4-127">-NamespaceName</span><span class="sxs-lookup"><span data-stu-id="f56c4-127">-NamespaceName</span></span>
 <span data-ttu-id="f56c4-128">System. String</span><span class="sxs-lookup"><span data-stu-id="f56c4-128">System.String</span></span>
 

### <span data-ttu-id="f56c4-129">-Tematname</span><span class="sxs-lookup"><span data-stu-id="f56c4-129">-TopicName</span></span>
 <span data-ttu-id="f56c4-130">System. String</span><span class="sxs-lookup"><span data-stu-id="f56c4-130">System.String</span></span>
 

### <span data-ttu-id="f56c4-131">-AuthorizationRuleName</span><span class="sxs-lookup"><span data-stu-id="f56c4-131">-AuthorizationRuleName</span></span>
 <span data-ttu-id="f56c4-132">System. String</span><span class="sxs-lookup"><span data-stu-id="f56c4-132">System.String</span></span>

## <span data-ttu-id="f56c4-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f56c4-133">OUTPUTS</span></span>

### <span data-ttu-id="f56c4-134">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. ServiceBus. MODELES. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.0.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f56c4-134">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.0.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="f56c4-135">Identyfikator:/subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1/authorizati onrules/SBTopicAuthoRule1 typ: Microsoft. ServiceBus/AuthorizationRules Name: SBTopicAuthoRule1 Location: zachód AMERYKAŃSKIe znaczniki: prawa: {Listen, Send}</span><span class="sxs-lookup"><span data-stu-id="f56c4-135">Id       : /subscriptions/854d368f-1828-428f-8f3c-f2affa9b2f7d/resourceGroups/Default-ServiceBus-WestUS/providers/Microsoft.ServiceBus/namespaces/SB-Example1/topics/SB-Topic_example1/authorizati onRules/SBTopicAuthoRule1 Type     : Microsoft.ServiceBus/AuthorizationRules Name     : SBTopicAuthoRule1 Location : West US Tags     : Rights   : {Listen, Send}</span></span>

## <span data-ttu-id="f56c4-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f56c4-136">NOTES</span></span>

## <span data-ttu-id="f56c4-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f56c4-137">RELATED LINKS</span></span>

