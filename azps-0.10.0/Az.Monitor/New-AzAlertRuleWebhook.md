---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 0137ECA3-37E1-4064-8A65-A582519E9017
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertrulewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/New-AzAlertRuleWebhook.md
ms.openlocfilehash: 420bfd3536c9bbf8bcfe075eb7ed56320788d3b3
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891158"
---
# <span data-ttu-id="0ced1-101">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="0ced1-101">New-AzAlertRuleWebhook</span></span>

## <span data-ttu-id="0ced1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0ced1-102">SYNOPSIS</span></span>
<span data-ttu-id="0ced1-103">Tworzy element webhook reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="0ced1-103">Creates an alert rule webhook.</span></span>

## <span data-ttu-id="0ced1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0ced1-104">SYNTAX</span></span>

```
New-AzAlertRuleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0ced1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0ced1-105">DESCRIPTION</span></span>
<span data-ttu-id="0ced1-106">Polecenie cmdlet **New-AzAlertRuleWebhook** tworzy element webhook reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="0ced1-106">The **New-AzAlertRuleWebhook** cmdlet creates an alert rule webhook.</span></span>

## <span data-ttu-id="0ced1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0ced1-107">EXAMPLES</span></span>

### <span data-ttu-id="0ced1-108">Przykład 1: Tworzenie elementu webhook reguły alertu</span><span class="sxs-lookup"><span data-stu-id="0ced1-108">Example 1: Create an alert rule webhook</span></span>
```
PS C:\>New-AzAlertRuleWebhook -ServiceUri "http://contoso.com"
```

<span data-ttu-id="0ced1-109">To polecenie tworzy element webhook reguły alertu, określając tylko identyfikator URI usługi.</span><span class="sxs-lookup"><span data-stu-id="0ced1-109">This command creates an alert rule webhook by specifying only the service URI.</span></span>

### <span data-ttu-id="0ced1-110">Przykład 2: Tworzenie elementu webhook o jednej właściwości</span><span class="sxs-lookup"><span data-stu-id="0ced1-110">Example 2: Create a webhook with one property</span></span>
```
PS C:\>$Actual = New-AzAlertRuleWebhook -ServiceUri "http://contoso.com" -Property @{prop1 = 'value1'}
```

<span data-ttu-id="0ced1-111">To polecenie tworzy element webhook reguły alertu dla Contoso.com o jednej właściwości, a następnie zapisuje go w zmiennej $Actual.</span><span class="sxs-lookup"><span data-stu-id="0ced1-111">This command creates an alert rule webhook for Contoso.com that has one property, and then stores it in the $Actual variable.</span></span>

## <span data-ttu-id="0ced1-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0ced1-112">PARAMETERS</span></span>

### <span data-ttu-id="0ced1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ced1-113">-DefaultProfile</span></span>
<span data-ttu-id="0ced1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0ced1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0ced1-115">-Property</span><span class="sxs-lookup"><span data-stu-id="0ced1-115">-Property</span></span>
<span data-ttu-id="0ced1-116">Określa listę właściwości w formacie @ (Property1 = ' wartość1 ',....).</span><span class="sxs-lookup"><span data-stu-id="0ced1-116">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="0ced1-117">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="0ced1-117">-ServiceUri</span></span>
<span data-ttu-id="0ced1-118">Określa identyfikator URI usługi.</span><span class="sxs-lookup"><span data-stu-id="0ced1-118">Specifies the service URI.</span></span>

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

### <span data-ttu-id="0ced1-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ced1-119">CommonParameters</span></span>
<span data-ttu-id="0ced1-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0ced1-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ced1-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0ced1-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ced1-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0ced1-122">INPUTS</span></span>

### <span data-ttu-id="0ced1-123">System. String</span><span class="sxs-lookup"><span data-stu-id="0ced1-123">System.String</span></span>

### <span data-ttu-id="0ced1-124">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="0ced1-124">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0ced1-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0ced1-125">OUTPUTS</span></span>

### <span data-ttu-id="0ced1-126">Microsoft. Azure. Management. Monitor. Management. models. RuleWebhookAction</span><span class="sxs-lookup"><span data-stu-id="0ced1-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleWebhookAction</span></span>

## <span data-ttu-id="0ced1-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0ced1-127">NOTES</span></span>

## <span data-ttu-id="0ced1-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0ced1-128">RELATED LINKS</span></span>

[<span data-ttu-id="0ced1-129">Dodaj-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="0ced1-129">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="0ced1-130">Dodaj-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="0ced1-130">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="0ced1-131">Dodaj-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="0ced1-131">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="0ced1-132">Nowe — AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="0ced1-132">New-AzAlertRuleEmail</span></span>](./New-AzAlertRuleEmail.md)

[<span data-ttu-id="0ced1-133">Nowe — AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="0ced1-133">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


