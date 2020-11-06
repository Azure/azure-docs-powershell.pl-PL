---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAlertRuleEmail.md
ms.openlocfilehash: 85479695efee536aac054751fdd5a48d4b5de5ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549171"
---
# <span data-ttu-id="375db-101">New-AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="375db-101">New-AzureRmAlertRuleEmail</span></span>

## <span data-ttu-id="375db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="375db-102">SYNOPSIS</span></span>
<span data-ttu-id="375db-103">Umożliwia utworzenie akcji poczty e-mail dla reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="375db-103">Creates an email action for an alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="375db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="375db-104">SYNTAX</span></span>

```
New-AzureRmAlertRuleEmail [[-CustomEmails] <String[]>] [-SendToServiceOwners]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="375db-105">Opis</span><span class="sxs-lookup"><span data-stu-id="375db-105">DESCRIPTION</span></span>
<span data-ttu-id="375db-106">Polecenie cmdlet **New-AzureRmAlertRuleEmail** umożliwia utworzenie akcji poczty e-mail dla reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="375db-106">The **New-AzureRmAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="375db-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="375db-107">EXAMPLES</span></span>

### <span data-ttu-id="375db-108">Przykład 1: Tworzenie akcji e-mail z regułą alertów dla właścicieli usługi</span><span class="sxs-lookup"><span data-stu-id="375db-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="375db-109">To polecenie umożliwia utworzenie akcji wiadomości e-mail z regułą alertu w celu wysłania jej właścicielom usług, gdy zostanie wygenerowane jej reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="375db-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="375db-110">Przykład 2: Tworzenie akcji e-mail z regułą alertów dla właścicieli niebędących usługami</span><span class="sxs-lookup"><span data-stu-id="375db-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="375db-111">To polecenie tworzy akcję e-mail dotyczącą reguły alertu dla określonych adresów e-mail, ale nie dla właścicieli usługi.</span><span class="sxs-lookup"><span data-stu-id="375db-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="375db-112">Przykład 3: Tworzenie reguły alertu e-mail dla właścicieli usługi i właścicieli niebędących usługami</span><span class="sxs-lookup"><span data-stu-id="375db-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzureRmAlertRuleEmail -CustomEmails "pattif@contoso.net" -SendToServiceOwners
```

<span data-ttu-id="375db-113">To polecenie umożliwia utworzenie akcji e-mail dotyczącej reguły alertu dla określonego adresu i jego właścicieli.</span><span class="sxs-lookup"><span data-stu-id="375db-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="375db-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="375db-114">PARAMETERS</span></span>

### <span data-ttu-id="375db-115">-CustomEmails</span><span class="sxs-lookup"><span data-stu-id="375db-115">-CustomEmails</span></span>
<span data-ttu-id="375db-116">Określa listę adresów e-mail rozdzielanych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="375db-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="375db-117">-SendToServiceOwners</span><span class="sxs-lookup"><span data-stu-id="375db-117">-SendToServiceOwners</span></span>
<span data-ttu-id="375db-118">Wskazuje, że ta operacja wysyła wiadomość e-mail do właścicieli usługi, gdy reguła jest uruchamiana.</span><span class="sxs-lookup"><span data-stu-id="375db-118">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="375db-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="375db-119">-DefaultProfile</span></span>
<span data-ttu-id="375db-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="375db-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="375db-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="375db-121">CommonParameters</span></span>
<span data-ttu-id="375db-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="375db-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="375db-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="375db-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="375db-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="375db-124">INPUTS</span></span>

## <span data-ttu-id="375db-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="375db-125">OUTPUTS</span></span>

### <span data-ttu-id="375db-126">Microsoft. Azure. Management. Monitor. Management. models. RuleEmailAction</span><span class="sxs-lookup"><span data-stu-id="375db-126">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="375db-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="375db-127">NOTES</span></span>

## <span data-ttu-id="375db-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="375db-128">RELATED LINKS</span></span>

[<span data-ttu-id="375db-129">Dodaj-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="375db-129">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="375db-130">Dodaj-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="375db-130">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="375db-131">Dodaj-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="375db-131">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="375db-132">Nowe — AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="375db-132">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


