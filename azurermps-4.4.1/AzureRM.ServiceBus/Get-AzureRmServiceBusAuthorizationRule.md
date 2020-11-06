---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusAuthorizationRule.md
ms.openlocfilehash: fa7224654581a5c71cb4daafa5dbb96100d63705
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553759"
---
# <span data-ttu-id="a995b-101">Get-AzureRmServiceBusAuthorizationRule</span><span class="sxs-lookup"><span data-stu-id="a995b-101">Get-AzureRmServiceBusAuthorizationRule</span></span>

## <span data-ttu-id="a995b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a995b-102">SYNOPSIS</span></span>
<span data-ttu-id="a995b-103">Pobiera opis określonej reguły autoryzacji dla określonego obszaru nazw lub kolejki lub tematu.</span><span class="sxs-lookup"><span data-stu-id="a995b-103">Gets a description of the specified authorization rule for a given Namespace or Queue or Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a995b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a995b-104">SYNTAX</span></span>

### <span data-ttu-id="a995b-105">NamespaceAuthorizationRuleSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a995b-105">NamespaceAuthorizationRuleSet (Default)</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a995b-106">QueueAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a995b-106">QueueAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Queue] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a995b-107">TopicAuthorizationRuleSet</span><span class="sxs-lookup"><span data-stu-id="a995b-107">TopicAuthorizationRuleSet</span></span>
```
Get-AzureRmServiceBusAuthorizationRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a995b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a995b-108">DESCRIPTION</span></span>
<span data-ttu-id="a995b-109">Polecenie cmdlet **Get-AzureRmServiceBusAuthorizationRule** Pobiera opis określonej reguły autoryzacji w danym obszarze nazw lub kolejce lub temacie.</span><span class="sxs-lookup"><span data-stu-id="a995b-109">The **Get-AzureRmServiceBusAuthorizationRule** cmdlet gets the description of the specified authorization rule in the given Namespace or Queue or Topic.</span></span>

## <span data-ttu-id="a995b-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a995b-110">EXAMPLES</span></span>

### <span data-ttu-id="a995b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a995b-111">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Name AuthoRule1
```

<span data-ttu-id="a995b-112">Zwraca opis określonej reguły autoryzacji dla określonego obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="a995b-112">Returns the specified authorization rule description for a specified namespace.</span></span>

### <span data-ttu-id="a995b-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a995b-113">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Queue SBQueue -Name AuthoRule1
```

<span data-ttu-id="a995b-114">Zwraca opis reguły autoryzacji określonej kolejki.</span><span class="sxs-lookup"><span data-stu-id="a995b-114">Returns the specified authorization rule description for a specified queue.</span></span>

### <span data-ttu-id="a995b-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a995b-115">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusAuthorizationRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SB-Example1 -Topic SBTopic -Name AuthoRule1
```

<span data-ttu-id="a995b-116">Zwraca opis reguły autoryzacji określonego tematu.</span><span class="sxs-lookup"><span data-stu-id="a995b-116">Returns the specified authorization rule description for a specified topic.</span></span>

## <span data-ttu-id="a995b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a995b-117">PARAMETERS</span></span>

### <span data-ttu-id="a995b-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a995b-118">-Name</span></span>
<span data-ttu-id="a995b-119">Nazwa AuthorizationRule.</span><span class="sxs-lookup"><span data-stu-id="a995b-119">AuthorizationRule Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AuthorizationRuleName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a995b-120">-Namespace</span><span class="sxs-lookup"><span data-stu-id="a995b-120">-Namespace</span></span>
<span data-ttu-id="a995b-121">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="a995b-121">Namespace Name.</span></span>

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

### <span data-ttu-id="a995b-122">-Queue</span><span class="sxs-lookup"><span data-stu-id="a995b-122">-Queue</span></span>
<span data-ttu-id="a995b-123">Nazwa kolejki.</span><span class="sxs-lookup"><span data-stu-id="a995b-123">Queue Name.</span></span>

```yaml
Type: System.String
Parameter Sets: QueueAuthorizationRuleSet
Aliases: QueueName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a995b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a995b-124">-ResourceGroupName</span></span>
<span data-ttu-id="a995b-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a995b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="a995b-126">— Temat</span><span class="sxs-lookup"><span data-stu-id="a995b-126">-Topic</span></span>
<span data-ttu-id="a995b-127">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="a995b-127">Topic Name.</span></span>

```yaml
Type: System.String
Parameter Sets: TopicAuthorizationRuleSet
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a995b-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a995b-128">-DefaultProfile</span></span>
<span data-ttu-id="a995b-129">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a995b-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a995b-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a995b-130">CommonParameters</span></span>
<span data-ttu-id="a995b-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a995b-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a995b-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a995b-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a995b-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a995b-133">INPUTS</span></span>

### <span data-ttu-id="a995b-134">System. String</span><span class="sxs-lookup"><span data-stu-id="a995b-134">System.String</span></span>

## <span data-ttu-id="a995b-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a995b-135">OUTPUTS</span></span>

### <span data-ttu-id="a995b-136">System. Collections. Generic. list "1 [[Microsoft. Azure. Commands. ServiceBus. MODELES. SharedAccessAuthorizationRuleAttributes, Microsoft. Azure. Commands. ServiceBus, Version = 0.4.2.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="a995b-136">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.ServiceBus.Models.SharedAccessAuthorizationRuleAttributes, Microsoft.Azure.Commands.ServiceBus, Version=0.4.2.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="a995b-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a995b-137">NOTES</span></span>
## <span data-ttu-id="a995b-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a995b-138">RELATED LINKS</span></span>

## <span data-ttu-id="a995b-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a995b-139">RELATED LINKS</span></span>

