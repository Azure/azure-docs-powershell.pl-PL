---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 592329ff0793fc99f8e5b0e7031a2248342102f9
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051948"
---
# <span data-ttu-id="d5ffc-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="d5ffc-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="d5ffc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d5ffc-102">SYNOPSIS</span></span>
<span data-ttu-id="d5ffc-103">Umożliwia utworzenie akcji poczty e-mail dla reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="d5ffc-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="d5ffc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d5ffc-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d5ffc-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d5ffc-105">DESCRIPTION</span></span>
<span data-ttu-id="d5ffc-106">Polecenie cmdlet **New-AzAlertRuleEmail** umożliwia utworzenie akcji poczty e-mail dla reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="d5ffc-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="d5ffc-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d5ffc-107">EXAMPLES</span></span>

### <span data-ttu-id="d5ffc-108">Przykład 1: Tworzenie akcji e-mail z regułą alertów dla właścicieli usługi</span><span class="sxs-lookup"><span data-stu-id="d5ffc-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="d5ffc-109">To polecenie umożliwia utworzenie akcji wiadomości e-mail z regułą alertu w celu wysłania jej właścicielom usług, gdy zostanie wygenerowane jej reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="d5ffc-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="d5ffc-110">Przykład 2: Tworzenie akcji e-mail z regułą alertów dla właścicieli niebędących usługami</span><span class="sxs-lookup"><span data-stu-id="d5ffc-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="d5ffc-111">To polecenie tworzy akcję e-mail dotyczącą reguły alertu dla określonych adresów e-mail, ale nie dla właścicieli usługi.</span><span class="sxs-lookup"><span data-stu-id="d5ffc-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="d5ffc-112">Przykład 3: Tworzenie reguły alertu e-mail dla właścicieli usługi i właścicieli niebędących usługami</span><span class="sxs-lookup"><span data-stu-id="d5ffc-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="d5ffc-113">To polecenie umożliwia utworzenie akcji e-mail dotyczącej reguły alertu dla określonego adresu i jego właścicieli.</span><span class="sxs-lookup"><span data-stu-id="d5ffc-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="d5ffc-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d5ffc-114">PARAMETERS</span></span>

### <span data-ttu-id="d5ffc-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="d5ffc-115">-CustomEmail</span></span>
<span data-ttu-id="d5ffc-116">Określa listę adresów e-mail rozdzielanych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="d5ffc-116">Specifies a list of comma-separated e-mail addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5ffc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5ffc-117">-DefaultProfile</span></span>
<span data-ttu-id="d5ffc-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="d5ffc-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d5ffc-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="d5ffc-119">-SendToServiceOwner</span></span>
<span data-ttu-id="d5ffc-120">Wskazuje, że ta operacja wysyła wiadomość e-mail do właścicieli usługi, gdy reguła jest uruchamiana.</span><span class="sxs-lookup"><span data-stu-id="d5ffc-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d5ffc-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5ffc-121">CommonParameters</span></span>
<span data-ttu-id="d5ffc-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5ffc-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5ffc-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="d5ffc-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5ffc-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5ffc-124">INPUTS</span></span>

### <span data-ttu-id="d5ffc-125">System. String []</span><span class="sxs-lookup"><span data-stu-id="d5ffc-125">System.String[]</span></span>

### <span data-ttu-id="d5ffc-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="d5ffc-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d5ffc-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d5ffc-127">OUTPUTS</span></span>

### <span data-ttu-id="d5ffc-128">Microsoft. Azure. Management. Monitor. Management. models. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="d5ffc-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="d5ffc-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d5ffc-129">NOTES</span></span>

## <span data-ttu-id="d5ffc-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5ffc-130">RELATED LINKS</span></span>

[<span data-ttu-id="d5ffc-131">Dodaj-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="d5ffc-131">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="d5ffc-132">Dodaj-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="d5ffc-132">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="d5ffc-133">Dodaj-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="d5ffc-133">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="d5ffc-134">Nowe — AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="d5ffc-134">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


