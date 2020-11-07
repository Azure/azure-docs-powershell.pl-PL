---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalenotification
schema: 2.0.0
ms.openlocfilehash: 51a5c01c28471cf85617b8ab629c2f79b366d555
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899329"
---
# <span data-ttu-id="f6812-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="f6812-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="f6812-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f6812-102">SYNOPSIS</span></span>
<span data-ttu-id="f6812-103">Umożliwia utworzenie powiadomienia e-mail autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="f6812-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6812-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f6812-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6812-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f6812-105">DESCRIPTION</span></span>
<span data-ttu-id="f6812-106">Polecenie cmdlet **New-AzureRmAutoscaleNotification** umożliwia utworzenie powiadomienia e-mail w celu automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="f6812-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="f6812-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f6812-107">EXAMPLES</span></span>

### <span data-ttu-id="f6812-108">Przykład 1: Tworzenie powiadomienia e-mail autoskalowania</span><span class="sxs-lookup"><span data-stu-id="f6812-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="f6812-109">To polecenie tworzy powiadomienie o Autosacale e-mail dla dwóch określonych adresów.</span><span class="sxs-lookup"><span data-stu-id="f6812-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="f6812-110">Przykład 2: Tworzenie powiadomienia e-mail autoskalowania dla administratora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f6812-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="f6812-111">To polecenie tworzy powiadomienie o Autosacale pocztą e-mail dla administratora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f6812-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="f6812-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f6812-112">PARAMETERS</span></span>

### <span data-ttu-id="f6812-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="f6812-113">-CustomEmail</span></span>
<span data-ttu-id="f6812-114">Określa listę adresów e-mail rozdzielonych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="f6812-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="f6812-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6812-115">-DefaultProfile</span></span>
<span data-ttu-id="f6812-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f6812-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6812-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="f6812-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="f6812-118">Wskazuje, że ta operacja wysyła powiadomienie e-mail do administratora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f6812-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="f6812-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="f6812-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="f6812-120">Wskazuje, że ta operacja wysyła powiadomienie e-mail do współadministratora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f6812-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="f6812-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="f6812-121">-Webhook</span></span>
<span data-ttu-id="f6812-122">Określa listę rozdzielanych przecinkami punktów webhook.</span><span class="sxs-lookup"><span data-stu-id="f6812-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="f6812-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6812-123">CommonParameters</span></span>
<span data-ttu-id="f6812-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6812-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6812-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6812-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6812-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f6812-126">INPUTS</span></span>

### <span data-ttu-id="f6812-127">Microsoft. Azure. Management. Monitor. Management. models. WebhookNotification []</span><span class="sxs-lookup"><span data-stu-id="f6812-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="f6812-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="f6812-128">System.String[]</span></span>

### <span data-ttu-id="f6812-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f6812-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f6812-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f6812-130">OUTPUTS</span></span>

### <span data-ttu-id="f6812-131">Microsoft. Azure. Management. Monitor. Management. models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="f6812-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="f6812-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f6812-132">NOTES</span></span>

## <span data-ttu-id="f6812-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f6812-133">RELATED LINKS</span></span>

[<span data-ttu-id="f6812-134">Nowe — AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="f6812-134">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


