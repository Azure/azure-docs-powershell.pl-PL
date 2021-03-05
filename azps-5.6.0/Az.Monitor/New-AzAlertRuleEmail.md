---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B1000C10-265E-4465-B167-F1251470BE3E
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azalertruleemail
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAlertRuleEmail.md
ms.openlocfilehash: 481105ca99a2bdc797a7a539f54ab69fd9935ebb
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979889"
---
# <span data-ttu-id="ed6d9-101">New-AzAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="ed6d9-101">New-AzAlertRuleEmail</span></span>

## <span data-ttu-id="ed6d9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed6d9-102">SYNOPSIS</span></span>
<span data-ttu-id="ed6d9-103">Tworzy akcję wiadomości e-mail dla reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="ed6d9-103">Creates an email action for an alert rule.</span></span>

## <span data-ttu-id="ed6d9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ed6d9-104">SYNTAX</span></span>

```
New-AzAlertRuleEmail [[-CustomEmail] <String[]>] [-SendToServiceOwner]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ed6d9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ed6d9-105">DESCRIPTION</span></span>
<span data-ttu-id="ed6d9-106">Polecenie **cmdlet New-AzAlertRuleEmail** tworzy akcję poczty e-mail dla reguły alertu.</span><span class="sxs-lookup"><span data-stu-id="ed6d9-106">The **New-AzAlertRuleEmail** cmdlet creates an e-mail action for an alert rule.</span></span>

## <span data-ttu-id="ed6d9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ed6d9-107">EXAMPLES</span></span>

### <span data-ttu-id="ed6d9-108">Przykład 1. Tworzenie akcji wiadomości e-mail reguły alertu dla właścicieli usług</span><span class="sxs-lookup"><span data-stu-id="ed6d9-108">Example 1: Create an alert rule email action for service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -SendToServiceOwners
```

<span data-ttu-id="ed6d9-109">To polecenie tworzy akcję poczty e-mail reguły alertu w celu wysłania jej właścicielom usługi w przypadku jej działania alertu.</span><span class="sxs-lookup"><span data-stu-id="ed6d9-109">This command creates an alert rule email action to send for its service owners when an alert rule is fired.</span></span>

### <span data-ttu-id="ed6d9-110">Przykład 2. Tworzenie akcji wiadomości e-mail reguły alertu dla właścicieli niebędące usługami</span><span class="sxs-lookup"><span data-stu-id="ed6d9-110">Example 2: Create an alert rule email action for non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.com,davidchew@contoso.net
```

<span data-ttu-id="ed6d9-111">To polecenie tworzy akcję poczty e-mail reguły alertu dla określonych adresów e-mail, ale nie dla właścicieli usługi.</span><span class="sxs-lookup"><span data-stu-id="ed6d9-111">This command creates an alert rule email action for the specified email addresses, but not for the service owners.</span></span>

### <span data-ttu-id="ed6d9-112">Przykład 3. Tworzenie akcji wiadomości e-mail reguły alertu dla właścicieli usług i osób niebędących usługami</span><span class="sxs-lookup"><span data-stu-id="ed6d9-112">Example 3: Create an alert rule email action for service owners and non-service owners</span></span>
```
PS C:\>New-AzAlertRuleEmail -CustomEmail pattif@contoso.net -SendToServiceOwners
```

<span data-ttu-id="ed6d9-113">To polecenie tworzy akcję poczty e-mail reguły alertu dla określonego adresu i dla jej właścicieli usługi.</span><span class="sxs-lookup"><span data-stu-id="ed6d9-113">This command creates an alert rule email action for the specified address and for its service owners.</span></span>

## <span data-ttu-id="ed6d9-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ed6d9-114">PARAMETERS</span></span>

### <span data-ttu-id="ed6d9-115">- CustomEmail</span><span class="sxs-lookup"><span data-stu-id="ed6d9-115">-CustomEmail</span></span>
<span data-ttu-id="ed6d9-116">Określa listę adresów e-mail rozdzielanych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="ed6d9-116">Specifies a list of comma-separated e-mail addresses.</span></span>

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

### <span data-ttu-id="ed6d9-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed6d9-117">-DefaultProfile</span></span>
<span data-ttu-id="ed6d9-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="ed6d9-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ed6d9-119">-SendToServiceOwner</span><span class="sxs-lookup"><span data-stu-id="ed6d9-119">-SendToServiceOwner</span></span>
<span data-ttu-id="ed6d9-120">Wskazuje, że ta operacja wysyła wiadomość e-mail do właścicieli usług w momencie jej odpalowania.</span><span class="sxs-lookup"><span data-stu-id="ed6d9-120">Indicates that this operation sends an e-mail to the service owners when the rule fires.</span></span>

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

### <span data-ttu-id="ed6d9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed6d9-121">CommonParameters</span></span>
<span data-ttu-id="ed6d9-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed6d9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed6d9-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ed6d9-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed6d9-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed6d9-124">INPUTS</span></span>

### <span data-ttu-id="ed6d9-125">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ed6d9-125">System.String[]</span></span>

### <span data-ttu-id="ed6d9-126">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="ed6d9-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ed6d9-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed6d9-127">OUTPUTS</span></span>

### <span data-ttu-id="ed6d9-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleemailAction</span><span class="sxs-lookup"><span data-stu-id="ed6d9-128">Microsoft.Azure.Management.Monitor.Management.Models.RuleEmailAction</span></span>

## <span data-ttu-id="ed6d9-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ed6d9-129">NOTES</span></span>

## <span data-ttu-id="ed6d9-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed6d9-130">RELATED LINKS</span></span>

[<span data-ttu-id="ed6d9-131">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="ed6d9-131">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="ed6d9-132">Add-AzMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="ed6d9-132">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="ed6d9-133">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="ed6d9-133">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="ed6d9-134">New-AzAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="ed6d9-134">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)


