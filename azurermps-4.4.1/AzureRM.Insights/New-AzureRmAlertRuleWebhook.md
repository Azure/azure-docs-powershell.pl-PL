---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleWebhook.md
ms.openlocfilehash: ed8b8fe18e6320a297635b09089ff95bd52fe1e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553312"
---
# <span data-ttu-id="e1745-101">New-AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="e1745-101">New-AzureRmAlertRuleWebhook</span></span>

## <span data-ttu-id="e1745-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e1745-102">SYNOPSIS</span></span>
<span data-ttu-id="e1745-103">Tworzy element webhook reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="e1745-103">Creates an alert rule webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e1745-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e1745-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleWebhook [-ServiceUri] <String> [[-Properties] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e1745-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e1745-105">DESCRIPTION</span></span>
<span data-ttu-id="e1745-106">Polecenie cmdlet **New-AzureRmAlertRuleWebhook** tworzy element webhook reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="e1745-106">The **New-AzureRmAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="e1745-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e1745-107">EXAMPLES</span></span>

### <span data-ttu-id="e1745-108">Przykład 1: Tworzenie elementu webhook reguły alertu</span><span class="sxs-lookup"><span data-stu-id="e1745-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="e1745-109">To polecenie tworzy element webhook reguły alertu, określając tylko identyfikator URI usługi.</span><span class="sxs-lookup"><span data-stu-id="e1745-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="e1745-110">Przykład 2: Tworzenie elementu webhook o jednej właściwości</span><span class="sxs-lookup"><span data-stu-id="e1745-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzureRmAlertRuleWebhook -ServiceUri "http://contoso.com" -Properties @{prop1 = 'value1'}
```

<span data-ttu-id="e1745-111">To polecenie tworzy element webhook reguły alertu dla Contoso.com o jednej właściwości, a następnie zapisuje go w zmiennej $Actual.</span><span class="sxs-lookup"><span data-stu-id="e1745-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="e1745-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e1745-112">PARAMETERS</span></span>

### <span data-ttu-id="e1745-113">-Properties</span><span class="sxs-lookup"><span data-stu-id="e1745-113">-Properties</span></span>
<span data-ttu-id="e1745-114">Określa listę właściwości w formacie @ (Property1 = ' wartość1 ',....).</span><span class="sxs-lookup"><span data-stu-id="e1745-114">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="e1745-115">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="e1745-115">-ServiceUri</span></span>
<span data-ttu-id="e1745-116">Określa identyfikator URI usługi.</span><span class="sxs-lookup"><span data-stu-id="e1745-116">Specifies the service URI.</span></span>

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

### <span data-ttu-id="e1745-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e1745-117">-DefaultProfile</span></span>
<span data-ttu-id="e1745-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e1745-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e1745-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e1745-119">CommonParameters</span></span>
<span data-ttu-id="e1745-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e1745-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e1745-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e1745-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e1745-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e1745-122">INPUTS</span></span>

## <span data-ttu-id="e1745-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e1745-123">OUTPUTS</span></span>

### <span data-ttu-id="e1745-124">Microsoft. Azure. Management. Monitor. Management. models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="e1745-124">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="e1745-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e1745-125">NOTES</span></span>

## <span data-ttu-id="e1745-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e1745-126">RELATED LINKS</span></span>

[<span data-ttu-id="e1745-127">Dodaj-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="e1745-127">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="e1745-128">Dodaj-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="e1745-128">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="e1745-129">Dodaj-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="e1745-129">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="e1745-130">Nowe — AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="e1745-130">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="e1745-131">Nowe — AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="e1745-131">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


