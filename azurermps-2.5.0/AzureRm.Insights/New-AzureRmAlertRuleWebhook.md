---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertrulewebhook
schema: 2.0.0
ms.openlocfilehash: d45624da172ecafba48354968d5a3ac5531be693
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899328"
---
# <span data-ttu-id="18417-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="18417-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="18417-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="18417-102">SYNOPSIS</span></span>
<span data-ttu-id="18417-103">Tworzy element webhook reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="18417-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="18417-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="18417-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="18417-105">Opis</span><span class="sxs-lookup"><span data-stu-id="18417-105">DESCRIPTION</span></span>
<span data-ttu-id="18417-106">Polecenie cmdlet **New-AzureRmAlertRuleWebhook** tworzy element webhook reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="18417-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="18417-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="18417-107">EXAMPLES</span></span>

### <span data-ttu-id="18417-108">Przykład 1: Tworzenie elementu webhook reguły alertu</span><span class="sxs-lookup"><span data-stu-id="18417-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="18417-109">To polecenie tworzy element webhook reguły alertu, określając tylko identyfikator URI usługi.</span><span class="sxs-lookup"><span data-stu-id="18417-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="18417-110">Przykład 2: Tworzenie elementu webhook o jednej właściwości</span><span class="sxs-lookup"><span data-stu-id="18417-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="18417-111">To polecenie tworzy element webhook reguły alertu dla Contoso.com o jednej właściwości, a następnie zapisuje go w zmiennej $Actual.</span><span class="sxs-lookup"><span data-stu-id="18417-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="18417-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="18417-112">PARAMETERS</span></span>

### <span data-ttu-id="18417-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="18417-113">-DefaultProfile</span></span>
<span data-ttu-id="18417-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="18417-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="18417-115">-Property</span><span class="sxs-lookup"><span data-stu-id="18417-115">-Property</span></span>
<span data-ttu-id="18417-116">Określa listę właściwości w formacie @ (Property1 = ' wartość1 ',....).</span><span class="sxs-lookup"><span data-stu-id="18417-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="18417-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="18417-117">-ServiceUri</span></span>
<span data-ttu-id="18417-118">Określa identyfikator URI usługi.</span><span class="sxs-lookup"><span data-stu-id="18417-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="18417-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="18417-119">CommonParameters</span></span>
<span data-ttu-id="18417-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="18417-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="18417-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="18417-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="18417-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="18417-122">INPUTS</span></span>

### <span data-ttu-id="18417-123">System. String</span><span class="sxs-lookup"><span data-stu-id="18417-123">System.String</span></span>

### <span data-ttu-id="18417-124">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="18417-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="18417-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="18417-125">OUTPUTS</span></span>

### <span data-ttu-id="18417-126">Microsoft. Azure. Management. Monitor. Management. models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="18417-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="18417-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="18417-127">NOTES</span></span>

## <span data-ttu-id="18417-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="18417-128">RELATED LINKS</span></span>



[<span data-ttu-id="18417-129">Dodaj-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="18417-129">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="18417-130">Dodaj-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="18417-130">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="18417-131">Nowe — AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="18417-131">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="18417-132">Nowe — AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="18417-132">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


