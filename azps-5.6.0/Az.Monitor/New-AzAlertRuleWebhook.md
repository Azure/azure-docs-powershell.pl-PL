---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 22afc323e827c543150bffb317f1b5db5275d82c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979882"
---
# <span data-ttu-id="fbb3a-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="fbb3a-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="fbb3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fbb3a-102">SYNOPSIS</span></span>
<span data-ttu-id="fbb3a-103">Tworzy webhook reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="fbb3a-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="fbb3a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fbb3a-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fbb3a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="fbb3a-105">DESCRIPTION</span></span>
<span data-ttu-id="fbb3a-106">Polecenie **cmdlet New-AzAlertRuleWebhook** tworzy webhook reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="fbb3a-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="fbb3a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fbb3a-107">EXAMPLES</span></span>

### <span data-ttu-id="fbb3a-108">Przykład 1. Tworzenie webhook reguły alertu</span><span class="sxs-lookup"><span data-stu-id="fbb3a-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="fbb3a-109">To polecenie tworzy webhook reguły alertu przez określenie tylko URI usługi.</span><span class="sxs-lookup"><span data-stu-id="fbb3a-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="fbb3a-110">Przykład 2. Tworzenie webhook za pomocą jednej właściwości</span><span class="sxs-lookup"><span data-stu-id="fbb3a-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="fbb3a-111">To polecenie tworzy webhook reguły alertu dla Contoso.com, który ma jedną właściwość, a następnie zapisuje go w zmiennej $Actual alertu.</span><span class="sxs-lookup"><span data-stu-id="fbb3a-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="fbb3a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fbb3a-112">PARAMETERS</span></span>

### <span data-ttu-id="fbb3a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fbb3a-113">-DefaultProfile</span></span>
<span data-ttu-id="fbb3a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="fbb3a-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fbb3a-115">- Właściwość</span><span class="sxs-lookup"><span data-stu-id="fbb3a-115">-Property</span></span>
<span data-ttu-id="fbb3a-116">Określa listę właściwości w formacie @(właściwość1 = 'wartość1',....).</span><span class="sxs-lookup"><span data-stu-id="fbb3a-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="fbb3a-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="fbb3a-117">-ServiceUri</span></span>
<span data-ttu-id="fbb3a-118">Określa URI usługi.</span><span class="sxs-lookup"><span data-stu-id="fbb3a-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="fbb3a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fbb3a-119">CommonParameters</span></span>
<span data-ttu-id="fbb3a-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fbb3a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fbb3a-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fbb3a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fbb3a-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbb3a-122">INPUTS</span></span>

### <span data-ttu-id="fbb3a-123">System.String</span><span class="sxs-lookup"><span data-stu-id="fbb3a-123">System.String</span></span>

### <span data-ttu-id="fbb3a-124">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fbb3a-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fbb3a-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fbb3a-125">OUTPUTS</span></span>

### <span data-ttu-id="fbb3a-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="fbb3a-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="fbb3a-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fbb3a-127">NOTES</span></span>

## <span data-ttu-id="fbb3a-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fbb3a-128">RELATED LINKS</span></span>

[<span data-ttu-id="fbb3a-129">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="fbb3a-129">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="fbb3a-130">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="fbb3a-130">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="fbb3a-131">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="fbb3a-131">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="fbb3a-132">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="fbb3a-132">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="fbb3a-133">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="fbb3a-133">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


