---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
ms.openlocfilehash: f5936bcbbf12308830fd158baa2c2d20f295694b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543819"
---
# <span data-ttu-id="c2f0c-101">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="c2f0c-101">New-AzureRmAlertRuleEmail</span></span>

## <span data-ttu-id="c2f0c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c2f0c-102">SYNOPSIS</span></span>
<span data-ttu-id="c2f0c-103">Umożliwia utworzenie akcji poczty e-mail dla reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="c2f0c-103">Creates an email action for an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2f0c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c2f0c-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2f0c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c2f0c-105">DESCRIPTION</span></span>
<span data-ttu-id="c2f0c-106">Polecenie cmdlet **New-AzureRmAlertRuleEmail** umożliwia utworzenie akcji poczty e-mail dla reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="c2f0c-106">The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="c2f0c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c2f0c-107">EXAMPLES</span></span>

### <span data-ttu-id="c2f0c-108">Przykład 1: Tworzenie akcji e-mail z regułą alertów dla właścicieli usługi</span><span class="sxs-lookup"><span data-stu-id="c2f0c-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="c2f0c-109">To polecenie umożliwia utworzenie akcji wiadomości e-mail z regułą alertu w celu wysłania jej właścicielom usług, gdy zostanie wygenerowane jej reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="c2f0c-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="c2f0c-110">Przykład 2: Tworzenie akcji e-mail z regułą alertów dla właścicieli niebędących usługami</span><span class="sxs-lookup"><span data-stu-id="c2f0c-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="c2f0c-111">To polecenie tworzy akcję e-mail dotyczącą reguły alertu dla określonych adresów e-mail, ale nie dla właścicieli usługi.</span><span class="sxs-lookup"><span data-stu-id="c2f0c-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="c2f0c-112">Przykład 3: Tworzenie reguły alertu e-mail dla właścicieli usługi i właścicieli niebędących usługami</span><span class="sxs-lookup"><span data-stu-id="c2f0c-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="c2f0c-113">To polecenie umożliwia utworzenie akcji e-mail dotyczącej reguły alertu dla określonego adresu i jego właścicieli.</span><span class="sxs-lookup"><span data-stu-id="c2f0c-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="c2f0c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c2f0c-114">PARAMETERS</span></span>

### <span data-ttu-id="c2f0c-115">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="c2f0c-115">-CustomEmail</span></span>
<span data-ttu-id="c2f0c-116">Określa listę adresów e-mail rozdzielanych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="c2f0c-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="c2f0c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2f0c-117">-DefaultProfile</span></span>
<span data-ttu-id="c2f0c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c2f0c-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c2f0c-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="c2f0c-119">-SendToServiceOwner</span></span>
<span data-ttu-id="c2f0c-120">Wskazuje, że ta operacja wysyła wiadomość e-mail do właścicieli usługi, gdy reguła jest uruchamiana.</span><span class="sxs-lookup"><span data-stu-id="c2f0c-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="c2f0c-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2f0c-121">CommonParameters</span></span>
<span data-ttu-id="c2f0c-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c2f0c-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2f0c-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2f0c-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2f0c-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c2f0c-124">INPUTS</span></span>

### <span data-ttu-id="c2f0c-125">System. String []</span><span class="sxs-lookup"><span data-stu-id="c2f0c-125">System.String[]</span></span>

### <span data-ttu-id="c2f0c-126">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="c2f0c-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="c2f0c-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c2f0c-127">OUTPUTS</span></span>

### <span data-ttu-id="c2f0c-128">Microsoft. Azure. Management. Monitor. Management. models. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="c2f0c-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="c2f0c-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c2f0c-129">NOTES</span></span>

## <span data-ttu-id="c2f0c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c2f0c-130">RELATED LINKS</span></span>

[<span data-ttu-id="c2f0c-131">Dodaj-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="c2f0c-131">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="c2f0c-132">Dodaj-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="c2f0c-132">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="c2f0c-133">Dodaj-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="c2f0c-133">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="c2f0c-134">Nowe — AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="c2f0c-134">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


