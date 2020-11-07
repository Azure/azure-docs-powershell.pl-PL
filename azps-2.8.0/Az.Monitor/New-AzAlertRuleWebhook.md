---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: aa287095405e48550153e58049f750d78a9ed877
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870412"
---
# <span data-ttu-id="5f668-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="5f668-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="5f668-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f668-102">SYNOPSIS</span></span>
<span data-ttu-id="5f668-103">Tworzy element webhook reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="5f668-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="5f668-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f668-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5f668-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5f668-105">DESCRIPTION</span></span>
<span data-ttu-id="5f668-106">Polecenie cmdlet **New-AzAlertRuleWebhook** tworzy element webhook reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="5f668-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="5f668-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f668-107">EXAMPLES</span></span>

### <span data-ttu-id="5f668-108">Przykład 1: Tworzenie elementu webhook reguły alertu</span><span class="sxs-lookup"><span data-stu-id="5f668-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="5f668-109">To polecenie tworzy element webhook reguły alertu, określając tylko identyfikator URI usługi.</span><span class="sxs-lookup"><span data-stu-id="5f668-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="5f668-110">Przykład 2: Tworzenie elementu webhook o jednej właściwości</span><span class="sxs-lookup"><span data-stu-id="5f668-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="5f668-111">To polecenie tworzy element webhook reguły alertu dla Contoso.com o jednej właściwości, a następnie zapisuje go w zmiennej $Actual.</span><span class="sxs-lookup"><span data-stu-id="5f668-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="5f668-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f668-112">PARAMETERS</span></span>

### <span data-ttu-id="5f668-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f668-113">-DefaultProfile</span></span>
<span data-ttu-id="5f668-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5f668-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5f668-115">-Property</span><span class="sxs-lookup"><span data-stu-id="5f668-115">-Property</span></span>
<span data-ttu-id="5f668-116">Określa listę właściwości w formacie @ (Property1 = ' wartość1 ',....).</span><span class="sxs-lookup"><span data-stu-id="5f668-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="5f668-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="5f668-117">-ServiceUri</span></span>
<span data-ttu-id="5f668-118">Określa identyfikator URI usługi.</span><span class="sxs-lookup"><span data-stu-id="5f668-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="5f668-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f668-119">CommonParameters</span></span>
<span data-ttu-id="5f668-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f668-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f668-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5f668-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f668-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f668-122">INPUTS</span></span>

### <span data-ttu-id="5f668-123">System. String</span><span class="sxs-lookup"><span data-stu-id="5f668-123">System.String</span></span>

### <span data-ttu-id="5f668-124">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="5f668-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5f668-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f668-125">OUTPUTS</span></span>

### <span data-ttu-id="5f668-126">Microsoft. Azure. Management. Monitor. Management. models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="5f668-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="5f668-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f668-127">NOTES</span></span>

## <span data-ttu-id="5f668-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f668-128">RELATED LINKS</span></span>

[<span data-ttu-id="5f668-129">Dodaj-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="5f668-129">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="5f668-130">Dodaj-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="5f668-130">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="5f668-131">Dodaj-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="5f668-131">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="5f668-132">Nowe — AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="5f668-132">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="5f668-133">Nowe — AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="5f668-133">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


