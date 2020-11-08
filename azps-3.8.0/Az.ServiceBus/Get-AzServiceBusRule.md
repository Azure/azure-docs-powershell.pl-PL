---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: f4899d55919f8b3c08b36babc448f1594f4ac4c8
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052701"
---
# <span data-ttu-id="2329a-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="2329a-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="2329a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2329a-102">SYNOPSIS</span></span>
<span data-ttu-id="2329a-103">Tworzy nową regułę dla danej subskrypcji tematu.</span><span class="sxs-lookup"><span data-stu-id="2329a-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="2329a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2329a-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2329a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2329a-105">DESCRIPTION</span></span>
<span data-ttu-id="2329a-106">Polecenie cmdlet **Get-AzServiceBusRule** Pobiera opis określonej reguły w podanej subskrypcji tematu.</span><span class="sxs-lookup"><span data-stu-id="2329a-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="2329a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2329a-107">EXAMPLES</span></span>

### <span data-ttu-id="2329a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2329a-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="2329a-109">Zwraca opis określonej reguły dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2329a-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="2329a-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="2329a-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="2329a-111">Zwraca listę opisów reguł dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2329a-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="2329a-112">Domyślnie zostanie zwrócona reguła 100, a w przypadku zwrócenia więcej niż 100 reguły Użyj parametru-MaxCount.</span><span class="sxs-lookup"><span data-stu-id="2329a-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="2329a-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="2329a-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="2329a-114">Zwraca listę pierwszych 150ych opisów reguł dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="2329a-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="2329a-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2329a-115">PARAMETERS</span></span>

### <span data-ttu-id="2329a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2329a-116">-DefaultProfile</span></span>
<span data-ttu-id="2329a-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2329a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2329a-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="2329a-118">-MaxCount</span></span>
<span data-ttu-id="2329a-119">Określ maksymalną liczbę reguł, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="2329a-119">Determine the maximum number of Rules to return.</span></span>

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

### <span data-ttu-id="2329a-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2329a-120">-Name</span></span>
<span data-ttu-id="2329a-121">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="2329a-121">Rule Name</span></span>

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

### <span data-ttu-id="2329a-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="2329a-122">-Namespace</span></span>
<span data-ttu-id="2329a-123">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="2329a-123">Namespace Name</span></span>

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

### <span data-ttu-id="2329a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2329a-124">-ResourceGroupName</span></span>
<span data-ttu-id="2329a-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="2329a-125">The name of the resource group</span></span>

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

### <span data-ttu-id="2329a-126">-Subscription</span><span class="sxs-lookup"><span data-stu-id="2329a-126">-Subscription</span></span>
<span data-ttu-id="2329a-127">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="2329a-127">Subscription Name</span></span>

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

### <span data-ttu-id="2329a-128">— Temat</span><span class="sxs-lookup"><span data-stu-id="2329a-128">-Topic</span></span>
<span data-ttu-id="2329a-129">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="2329a-129">Topic Name</span></span>

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

### <span data-ttu-id="2329a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2329a-130">CommonParameters</span></span>
<span data-ttu-id="2329a-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2329a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2329a-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2329a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2329a-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2329a-133">INPUTS</span></span>

### <span data-ttu-id="2329a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="2329a-134">System.String</span></span>

## <span data-ttu-id="2329a-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2329a-135">OUTPUTS</span></span>

### <span data-ttu-id="2329a-136">Microsoft. Azure. Commands. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="2329a-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="2329a-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2329a-137">NOTES</span></span>

## <span data-ttu-id="2329a-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2329a-138">RELATED LINKS</span></span>
