---
external help file: Microsoft.Azure.Commands.ServiceBus.dll-Help.xml
Module Name: AzureRM.ServiceBus
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.servicebus/get-azurermservicebusrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ServiceBus/Commands.ServiceBus/help/Get-AzureRmServiceBusRule.md
ms.openlocfilehash: 3eb629665f8bc4ed030b5c616410fb47455136e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551587"
---
# <span data-ttu-id="4498b-101">Get-AzureRmServiceBusRule</span><span class="sxs-lookup"><span data-stu-id="4498b-101">Get-AzureRmServiceBusRule</span></span>

## <span data-ttu-id="4498b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4498b-102">SYNOPSIS</span></span>
<span data-ttu-id="4498b-103">Pobiera opis określonej reguły dla danej subskrypcji tematu.</span><span class="sxs-lookup"><span data-stu-id="4498b-103">Gets a description of the specified rule for a given Subscription of  Topic.</span></span> 

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4498b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4498b-104">SYNTAX</span></span>

```
Get-AzureRmServiceBusRule [-ResourceGroupName] <String> [-Namespace] <String> [-Topic] <String>
 [-Subscription] <String> [[-Name] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4498b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="4498b-105">DESCRIPTION</span></span>
<span data-ttu-id="4498b-106">Polecenie cmdlet **Get-AzureRmServiceBusRule** Pobiera opis określonej reguły w podanej subskrypcji tematu.</span><span class="sxs-lookup"><span data-stu-id="4498b-106">The **Get-AzureRmServiceBusRule** cmdlet gets the description of the specified rule in the given subscription of topic.</span></span>

## <span data-ttu-id="4498b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4498b-107">EXAMPLES</span></span>

### <span data-ttu-id="4498b-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="4498b-108">Example 1</span></span>
```
PS C:\> Get-AzureRmServiceBusRule -ResourceGroup Default-ServiceBus-WestUS -Namespace SBExample1 -Topic SBTopic -Subscription SBSubscription -NAme SBRule
```

<span data-ttu-id="4498b-109">Zwraca opis określonej reguły dla określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4498b-109">Returns the specified rule description for a specified subscription.</span></span>

## <span data-ttu-id="4498b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4498b-110">PARAMETERS</span></span>

### <span data-ttu-id="4498b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4498b-111">-DefaultProfile</span></span>
<span data-ttu-id="4498b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4498b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4498b-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4498b-113">-Name</span></span>
<span data-ttu-id="4498b-114">Nazwa reguły.</span><span class="sxs-lookup"><span data-stu-id="4498b-114">Rule Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4498b-115">-Namespace</span><span class="sxs-lookup"><span data-stu-id="4498b-115">-Namespace</span></span>
<span data-ttu-id="4498b-116">Nazwa obszaru nazw.</span><span class="sxs-lookup"><span data-stu-id="4498b-116">Namespace Name.</span></span>

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

### <span data-ttu-id="4498b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4498b-117">-ResourceGroupName</span></span>
<span data-ttu-id="4498b-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="4498b-118">The name of the resource group</span></span>

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

### <span data-ttu-id="4498b-119">-Subscription</span><span class="sxs-lookup"><span data-stu-id="4498b-119">-Subscription</span></span>
<span data-ttu-id="4498b-120">Nazwa subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="4498b-120">Subscription Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubscriptionName

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4498b-121">— Temat</span><span class="sxs-lookup"><span data-stu-id="4498b-121">-Topic</span></span>
<span data-ttu-id="4498b-122">Nazwa tematu.</span><span class="sxs-lookup"><span data-stu-id="4498b-122">Topic Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TopicName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4498b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4498b-123">CommonParameters</span></span>
<span data-ttu-id="4498b-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4498b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4498b-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4498b-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4498b-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4498b-126">INPUTS</span></span>

### <span data-ttu-id="4498b-127">System. String</span><span class="sxs-lookup"><span data-stu-id="4498b-127">System.String</span></span>

## <span data-ttu-id="4498b-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4498b-128">OUTPUTS</span></span>

### <span data-ttu-id="4498b-129">Microsoft. Azure. Commands. ServiceBus. models. PSRulesAttributes</span><span class="sxs-lookup"><span data-stu-id="4498b-129">Microsoft.Azure.Commands.ServiceBus.Models.PSRulesAttributes</span></span>

## <span data-ttu-id="4498b-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4498b-130">NOTES</span></span>

## <span data-ttu-id="4498b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4498b-131">RELATED LINKS</span></span>

