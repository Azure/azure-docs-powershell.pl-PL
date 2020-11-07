---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ServiceBus.dll-Help.xml
Module Name: Az.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/az.servicebus/get-azservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ServiceBus/ServiceBus/help/Get-AzServiceBusRule.md
ms.openlocfilehash: 0c23f4a46782e4ff30b48cde57706680c532e8f5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873147"
---
# <span data-ttu-id="ebf3c-101">Get-AzServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="ebf3c-101">Get-AzServiceBusRule</span></span>

## <span data-ttu-id="ebf3c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ebf3c-102">SYNOPSIS</span></span>
<span data-ttu-id="ebf3c-103">Tworzy nową regułę dla danej subskrypcji tematu.</span><span class="sxs-lookup"><span data-stu-id="ebf3c-103">Creates a new rule for a given Subscription of Topic.</span></span> 

## <span data-ttu-id="ebf3c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ebf3c-104">SYNTAX</span></span>

```
Get-AzServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-MaxCount <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ebf3c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ebf3c-105">DESCRIPTION</span></span>
<span data-ttu-id="ebf3c-106">Polecenie cmdlet **Get-AzServiceBusRule** Pobiera opis określonej reguły w podanej subskrypcji tematu.</span><span class="sxs-lookup"><span data-stu-id="ebf3c-106">The **Get-AzServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="ebf3c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ebf3c-107">EXAMPLES</span></span>

### <span data-ttu-id="ebf3c-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ebf3c-108">Example 1</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -Name SBRule
```

<span data-ttu-id="ebf3c-109">Zwraca opis określonej reguły dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ebf3c-109">Returns the specified rule description for a specified subscription.</span></span>

### <span data-ttu-id="ebf3c-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ebf3c-110">Example 2</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription
```

<span data-ttu-id="ebf3c-111">Zwraca listę opisów reguł dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ebf3c-111">Returns list of rule descriptions for a specified subscription.</span></span>  <span data-ttu-id="ebf3c-112">Domyślnie zostanie zwrócona reguła 100, a w przypadku zwrócenia więcej niż 100 reguły Użyj parametru-MaxCount.</span><span class="sxs-lookup"><span data-stu-id="ebf3c-112">By default 100 rule will be returned, if more than 100 rule to be returned, please use -MaxCount Parameter.</span></span>

### <span data-ttu-id="ebf3c-113">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="ebf3c-113">Example 3</span></span>
```
PS C:\> Get-AzServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -MaxCount 150
```

<span data-ttu-id="ebf3c-114">Zwraca listę pierwszych 150ych opisów reguł dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="ebf3c-114">Returns list of first 150 rules descriptions for a specified subscription.</span></span>

## <span data-ttu-id="ebf3c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ebf3c-115">PARAMETERS</span></span>

### <span data-ttu-id="ebf3c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebf3c-116">-DefaultProfile</span></span>
<span data-ttu-id="ebf3c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ebf3c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ebf3c-118">-MaxCount</span><span class="sxs-lookup"><span data-stu-id="ebf3c-118">-MaxCount</span></span>
<span data-ttu-id="ebf3c-119">Określ maksymalną liczbę reguł, które mają zostać zwrócone.</span><span class="sxs-lookup"><span data-stu-id="ebf3c-119">Determine the maximum number of Rules to return.</span></span>

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

### <span data-ttu-id="ebf3c-120">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ebf3c-120">-Name</span></span>
<span data-ttu-id="ebf3c-121">Nazwa reguły</span><span class="sxs-lookup"><span data-stu-id="ebf3c-121">Rule Name</span></span>

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

### <span data-ttu-id="ebf3c-122">-Namespace</span><span class="sxs-lookup"><span data-stu-id="ebf3c-122">-Namespace</span></span>
<span data-ttu-id="ebf3c-123">Nazwa obszaru nazw</span><span class="sxs-lookup"><span data-stu-id="ebf3c-123">Namespace Name</span></span>

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

### <span data-ttu-id="ebf3c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebf3c-124">-ResourceGroupName</span></span>
<span data-ttu-id="ebf3c-125">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="ebf3c-125">The name of the resource group</span></span>

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

### <span data-ttu-id="ebf3c-126">-Subscription</span><span class="sxs-lookup"><span data-stu-id="ebf3c-126">-Subscription</span></span>
<span data-ttu-id="ebf3c-127">Nazwa subskrypcji</span><span class="sxs-lookup"><span data-stu-id="ebf3c-127">Subscription Name</span></span>

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

### <span data-ttu-id="ebf3c-128">— Temat</span><span class="sxs-lookup"><span data-stu-id="ebf3c-128">-Topic</span></span>
<span data-ttu-id="ebf3c-129">Nazwa tematu</span><span class="sxs-lookup"><span data-stu-id="ebf3c-129">Topic Name</span></span>

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

### <span data-ttu-id="ebf3c-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebf3c-130">CommonParameters</span></span>
<span data-ttu-id="ebf3c-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebf3c-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebf3c-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ebf3c-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebf3c-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ebf3c-133">INPUTS</span></span>

### <span data-ttu-id="ebf3c-134">System. String</span><span class="sxs-lookup"><span data-stu-id="ebf3c-134">System.String</span></span>

## <span data-ttu-id="ebf3c-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ebf3c-135">OUTPUTS</span></span>

### <span data-ttu-id="ebf3c-136">Microsoft. Azure. Commands. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="ebf3c-136">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="ebf3c-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ebf3c-137">NOTES</span></span>

## <span data-ttu-id="ebf3c-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ebf3c-138">RELATED LINKS</span></span>
