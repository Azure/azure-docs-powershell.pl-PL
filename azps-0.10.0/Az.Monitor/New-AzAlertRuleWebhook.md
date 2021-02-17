---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 03a1ca397fb67daf4b7cf73700f54d6642dd9f2d
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399366"
---
# <span data-ttu-id="b603e-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="b603e-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="b603e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b603e-102">SYNOPSIS</span></span>
<span data-ttu-id="b603e-103">Tworzy webhook reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="b603e-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="b603e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b603e-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b603e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b603e-105">DESCRIPTION</span></span>
<span data-ttu-id="b603e-106">Polecenie **cmdlet New-AzAlertRuleWebhook** tworzy webhook reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="b603e-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="b603e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b603e-107">EXAMPLES</span></span>

### <span data-ttu-id="b603e-108">Przykład 1. Tworzenie webhook reguły alertu</span><span class="sxs-lookup"><span data-stu-id="b603e-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="b603e-109">To polecenie tworzy webhook reguły alertu przez określenie tylko URI usługi.</span><span class="sxs-lookup"><span data-stu-id="b603e-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="b603e-110">Przykład 2. Tworzenie witryny sieci Web z jedną właściwością</span><span class="sxs-lookup"><span data-stu-id="b603e-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="b603e-111">To polecenie tworzy webhook reguły alertu dla Contoso.com, który ma jedną właściwość, a następnie zapisuje go w zmiennej $Actual alertu.</span><span class="sxs-lookup"><span data-stu-id="b603e-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="b603e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b603e-112">PARAMETERS</span></span>

### <span data-ttu-id="b603e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b603e-113">-DefaultProfile</span></span>
<span data-ttu-id="b603e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b603e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b603e-115">- Właściwość</span><span class="sxs-lookup"><span data-stu-id="b603e-115">-Property</span></span>
<span data-ttu-id="b603e-116">Określa listę właściwości w formacie @(właściwość1 = 'wartość1',....).</span><span class="sxs-lookup"><span data-stu-id="b603e-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="b603e-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="b603e-117">-ServiceUri</span></span>
<span data-ttu-id="b603e-118">Określa URI usługi.</span><span class="sxs-lookup"><span data-stu-id="b603e-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="b603e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b603e-119">CommonParameters</span></span>
<span data-ttu-id="b603e-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b603e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b603e-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b603e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b603e-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b603e-122">INPUTS</span></span>

### <span data-ttu-id="b603e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="b603e-123">System.String</span></span>

### <span data-ttu-id="b603e-124">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="b603e-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="b603e-125">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b603e-125">OUTPUTS</span></span>

### <span data-ttu-id="b603e-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="b603e-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="b603e-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b603e-127">NOTES</span></span>

## <span data-ttu-id="b603e-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b603e-128">RELATED LINKS</span></span>


[<span data-ttu-id="b603e-129">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="b603e-129">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="b603e-130">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="b603e-130">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="b603e-131">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="b603e-131">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="b603e-132">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="b603e-132">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


