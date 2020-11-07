---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: 35eeb7aa1482cb04c194f1a0674825bd3a72b187
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93867275"
---
# <span data-ttu-id="016e3-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="016e3-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="016e3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="016e3-102">SYNOPSIS</span></span>
<span data-ttu-id="016e3-103">Umożliwia utworzenie powiadomienia e-mail autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="016e3-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="016e3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="016e3-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="016e3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="016e3-105">DESCRIPTION</span></span>
<span data-ttu-id="016e3-106">Polecenie cmdlet **New-AzAutoscaleNotification** umożliwia utworzenie powiadomienia e-mail w celu automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="016e3-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="016e3-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="016e3-107">EXAMPLES</span></span>

### <span data-ttu-id="016e3-108">Przykład 1: Tworzenie powiadomienia e-mail autoskalowania</span><span class="sxs-lookup"><span data-stu-id="016e3-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="016e3-109">To polecenie tworzy powiadomienie o Autosacale e-mail dla dwóch określonych adresów.</span><span class="sxs-lookup"><span data-stu-id="016e3-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="016e3-110">Przykład 2: Tworzenie powiadomienia e-mail autoskalowania dla administratora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="016e3-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="016e3-111">To polecenie tworzy powiadomienie o Autosacale pocztą e-mail dla administratora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="016e3-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="016e3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="016e3-112">PARAMETERS</span></span>

### <span data-ttu-id="016e3-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="016e3-113">-CustomEmail</span></span>
<span data-ttu-id="016e3-114">Określa listę adresów e-mail rozdzielonych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="016e3-114">Specifies a comma-separated list of email addresses.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="016e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="016e3-115">-DefaultProfile</span></span>
<span data-ttu-id="016e3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="016e3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="016e3-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="016e3-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="016e3-118">Wskazuje, że ta operacja wysyła powiadomienie e-mail do administratora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="016e3-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="016e3-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="016e3-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="016e3-120">Wskazuje, że ta operacja wysyła powiadomienie e-mail do współadministratora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="016e3-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="016e3-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="016e3-121">-Webhook</span></span>
<span data-ttu-id="016e3-122">Określa listę rozdzielanych przecinkami punktów webhook.</span><span class="sxs-lookup"><span data-stu-id="016e3-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

```yaml
Type: Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="016e3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="016e3-123">CommonParameters</span></span>
<span data-ttu-id="016e3-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="016e3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="016e3-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="016e3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="016e3-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="016e3-126">INPUTS</span></span>

### <span data-ttu-id="016e3-127">Microsoft. Azure. Management. Monitor. Management. models. WebhookNotification []</span><span class="sxs-lookup"><span data-stu-id="016e3-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="016e3-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="016e3-128">System.String[]</span></span>

### <span data-ttu-id="016e3-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="016e3-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="016e3-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="016e3-130">OUTPUTS</span></span>

### <span data-ttu-id="016e3-131">Microsoft. Azure. Management. Monitor. Management. models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="016e3-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="016e3-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="016e3-132">NOTES</span></span>

## <span data-ttu-id="016e3-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="016e3-133">RELATED LINKS</span></span>

[<span data-ttu-id="016e3-134">Nowe — AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="016e3-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


