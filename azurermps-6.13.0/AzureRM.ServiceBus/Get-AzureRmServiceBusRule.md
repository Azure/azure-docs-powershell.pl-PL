---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: 2d249d8935b79c310e4ca0aa1270ee67bf33ece3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717369"
---
# <span data-ttu-id="7fad9-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="7fad9-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="7fad9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7fad9-102">SYNOPSIS</span></span>
<span data-ttu-id="7fad9-103">Tworzy nową regułę dla danej subskrypcji tematu.</span><span class="sxs-lookup"><span data-stu-id="7fad9-103">Creates a new rule for a given Subscription of Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fad9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7fad9-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7fad9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7fad9-105">DESCRIPTION</span></span>
<span data-ttu-id="7fad9-106">Polecenie cmdlet **Get-AzureRmServiceBusRule** Pobiera opis określonej reguły w podanej subskrypcji tematu.</span><span class="sxs-lookup"><span data-stu-id="7fad9-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="7fad9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7fad9-107">EXAMPLES</span></span>

### <span data-ttu-id="7fad9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7fad9-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="7fad9-109">Zwraca opis określonej reguły dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7fad9-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="7fad9-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="7fad9-110">Example 2</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="7fad9-111">Zwraca listę opisów reguł dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7fad9-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="7fad9-112">Domyślnie zostanie zwrócona reguła 100, a w przypadku zwrócenia więcej niż 100 reguły Użyj parametru-MaxCount.</span><span class="sxs-lookup"><span data-stu-id="7fad9-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="7fad9-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="7fad9-113">Example 3</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="7fad9-114">Zwraca listę pierwszych 150ych opisów reguł dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="7fad9-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="7fad9-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7fad9-115">PARAMETERS</span></span>

### <span data-ttu-id="7fad9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fad9-116">-DefaultProfile</span></span>
<span data-ttu-id="7fad9-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7fad9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7fad9-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="7fad9-118">-MaxCount</span></span>
<span data-ttu-id="7fad9-119">Określ maksymalną liczbę reguł, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="7fad9-119">Determine the maximum number of Rules to return.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fad9-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7fad9-120">-Name</span></span>
<span data-ttu-id="7fad9-121">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="7fad9-121">Rule Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fad9-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="7fad9-122">-Namespace</span></span>
<span data-ttu-id="7fad9-123">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="7fad9-123">Namespace Name</span></span>

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

### <span data-ttu-id="7fad9-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7fad9-124">-ResourceGroupName</span></span>
<span data-ttu-id="7fad9-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="7fad9-125">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fad9-126">-Subscription</span><span class="sxs-lookup"><span data-stu-id="7fad9-126">-Subscription</span></span>
<span data-ttu-id="7fad9-127">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7fad9-127">Subscription Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7fad9-128">— Temat</span><span class="sxs-lookup"><span data-stu-id="7fad9-128">-Topic</span></span>
<span data-ttu-id="7fad9-129">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="7fad9-129">Topic Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fad9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fad9-130">CommonParameters</span></span>
<span data-ttu-id="7fad9-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7fad9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fad9-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fad9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fad9-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7fad9-133">INPUTS</span></span>

### <span data-ttu-id="7fad9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="7fad9-134">System.String</span></span>

## <span data-ttu-id="7fad9-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7fad9-135">OUTPUTS</span></span>

### <span data-ttu-id="7fad9-136">Microsoft. Azure. Commands. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="7fad9-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="7fad9-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7fad9-137">NOTES</span></span>

## <span data-ttu-id="7fad9-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7fad9-138">RELATED LINKS</span></span>
