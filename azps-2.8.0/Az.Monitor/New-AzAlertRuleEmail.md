---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 30447992cd8159f56ae08d6cb2baf659c9ed7bb4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870420"
---
# <span data-ttu-id="36347-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="36347-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="36347-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="36347-102">SYNOPSIS</span></span>
<span data-ttu-id="36347-103">Umożliwia utworzenie akcji poczty e-mail dla reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="36347-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="36347-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="36347-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="36347-105">Opis</span><span class="sxs-lookup"><span data-stu-id="36347-105">DESCRIPTION</span></span>
<span data-ttu-id="36347-106">Polecenie cmdlet **New-AzAlertRuleEmail** umożliwia utworzenie akcji poczty e-mail dla reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="36347-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="36347-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="36347-107">EXAMPLES</span></span>

### <span data-ttu-id="36347-108">Przykład 1: Tworzenie akcji e-mail z regułą alertów dla właścicieli usługi</span><span class="sxs-lookup"><span data-stu-id="36347-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="36347-109">To polecenie umożliwia utworzenie akcji wiadomości e-mail z regułą alertu w celu wysłania jej właścicielom usług, gdy zostanie wygenerowane jej reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="36347-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="36347-110">Przykład 2: Tworzenie akcji e-mail z regułą alertów dla właścicieli niebędących usługami</span><span class="sxs-lookup"><span data-stu-id="36347-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="36347-111">To polecenie tworzy akcję e-mail dotyczącą reguły alertu dla określonych adresów e-mail, ale nie dla właścicieli usługi.</span><span class="sxs-lookup"><span data-stu-id="36347-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="36347-112">Przykład 3: Tworzenie reguły alertu e-mail dla właścicieli usługi i właścicieli niebędących usługami</span><span class="sxs-lookup"><span data-stu-id="36347-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="36347-113">To polecenie umożliwia utworzenie akcji e-mail dotyczącej reguły alertu dla określonego adresu i jego właścicieli.</span><span class="sxs-lookup"><span data-stu-id="36347-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="36347-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="36347-114">PARAMETERS</span></span>

### <span data-ttu-id="36347-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="36347-115">-CustomEmail</span></span>
<span data-ttu-id="36347-116">Określa listę adresów e-mail rozdzielanych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="36347-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="36347-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36347-117">-DefaultProfile</span></span>
<span data-ttu-id="36347-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="36347-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36347-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="36347-119">-SendToServiceOwner</span></span>
<span data-ttu-id="36347-120">Wskazuje, że ta operacja wysyła wiadomość e-mail do właścicieli usługi, gdy reguła jest uruchamiana.</span><span class="sxs-lookup"><span data-stu-id="36347-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="36347-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36347-121">CommonParameters</span></span>
<span data-ttu-id="36347-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36347-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36347-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="36347-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36347-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="36347-124">INPUTS</span></span>

### <span data-ttu-id="36347-125">System. String []</span><span class="sxs-lookup"><span data-stu-id="36347-125">System.String[]</span></span>

### <span data-ttu-id="36347-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="36347-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="36347-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="36347-127">OUTPUTS</span></span>

### <span data-ttu-id="36347-128">Microsoft. Azure. Management. Monitor. Management. models. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="36347-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="36347-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="36347-129">NOTES</span></span>

## <span data-ttu-id="36347-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="36347-130">RELATED LINKS</span></span>

[<span data-ttu-id="36347-131">Dodaj-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="36347-131">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="36347-132">Dodaj-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="36347-132">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="36347-133">Dodaj-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="36347-133">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="36347-134">Nowe — AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="36347-134">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


