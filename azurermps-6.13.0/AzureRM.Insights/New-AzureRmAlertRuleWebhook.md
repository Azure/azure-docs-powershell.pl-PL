---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
ms.openlocfilehash: 619219a300bb1b7317ea4c8c5fce442d43b74ff1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543812"
---
# <span data-ttu-id="180af-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="180af-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="180af-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="180af-102">SYNOPSIS</span></span>
<span data-ttu-id="180af-103">Tworzy element webhook reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="180af-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="180af-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="180af-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="180af-105">Opis</span><span class="sxs-lookup"><span data-stu-id="180af-105">DESCRIPTION</span></span>
<span data-ttu-id="180af-106">Polecenie cmdlet **New-AzureRmAlertRuleWebhook** tworzy element webhook reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="180af-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="180af-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="180af-107">EXAMPLES</span></span>

### <span data-ttu-id="180af-108">Przykład 1: Tworzenie elementu webhook reguły alertu</span><span class="sxs-lookup"><span data-stu-id="180af-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="180af-109">To polecenie tworzy element webhook reguły alertu, określając tylko identyfikator URI usługi.</span><span class="sxs-lookup"><span data-stu-id="180af-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="180af-110">Przykład 2: Tworzenie elementu webhook o jednej właściwości</span><span class="sxs-lookup"><span data-stu-id="180af-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="180af-111">To polecenie tworzy element webhook reguły alertu dla Contoso.com o jednej właściwości, a następnie zapisuje go w zmiennej $Actual.</span><span class="sxs-lookup"><span data-stu-id="180af-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="180af-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="180af-112">PARAMETERS</span></span>

### <span data-ttu-id="180af-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="180af-113">-DefaultProfile</span></span>
<span data-ttu-id="180af-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="180af-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="180af-115">-Property</span><span class="sxs-lookup"><span data-stu-id="180af-115">-Property</span></span>
<span data-ttu-id="180af-116">Określa listę właściwości w formacie @ (Property1 = ' wartość1 ',....).</span><span class="sxs-lookup"><span data-stu-id="180af-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="180af-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="180af-117">-ServiceUri</span></span>
<span data-ttu-id="180af-118">Określa identyfikator URI usługi.</span><span class="sxs-lookup"><span data-stu-id="180af-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="180af-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="180af-119">CommonParameters</span></span>
<span data-ttu-id="180af-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="180af-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="180af-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="180af-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="180af-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="180af-122">INPUTS</span></span>

### <span data-ttu-id="180af-123">System. String</span><span class="sxs-lookup"><span data-stu-id="180af-123">System.String</span></span>

### <span data-ttu-id="180af-124">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="180af-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="180af-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="180af-125">OUTPUTS</span></span>

### <span data-ttu-id="180af-126">Microsoft. Azure. Management. Monitor. Management. models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="180af-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="180af-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="180af-127">NOTES</span></span>

## <span data-ttu-id="180af-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="180af-128">RELATED LINKS</span></span>

[<span data-ttu-id="180af-129">Dodaj-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="180af-129">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="180af-130">Dodaj-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="180af-130">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="180af-131">Dodaj-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="180af-131">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="180af-132">Nowe — AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="180af-132">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="180af-133">Nowe — AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="180af-133">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


