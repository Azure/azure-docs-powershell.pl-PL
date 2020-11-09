---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: 010698183dec206002c0966fb8f37d629d24794a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304561"
---
# <span data-ttu-id="88340-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="88340-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="88340-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88340-102">SYNOPSIS</span></span>
<span data-ttu-id="88340-103">Umożliwia utworzenie powiadomienia e-mail autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="88340-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="88340-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88340-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88340-105">Opis</span><span class="sxs-lookup"><span data-stu-id="88340-105">DESCRIPTION</span></span>
<span data-ttu-id="88340-106">Polecenie cmdlet **New-AzAutoscaleNotification** umożliwia utworzenie powiadomienia e-mail w celu automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="88340-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="88340-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88340-107">EXAMPLES</span></span>

### <span data-ttu-id="88340-108">Przykład 1: Tworzenie powiadomienia e-mail autoskalowania</span><span class="sxs-lookup"><span data-stu-id="88340-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="88340-109">To polecenie tworzy powiadomienie o Autosacale e-mail dla dwóch określonych adresów.</span><span class="sxs-lookup"><span data-stu-id="88340-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="88340-110">Przykład 2: Tworzenie powiadomienia e-mail autoskalowania dla administratora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="88340-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="88340-111">To polecenie tworzy powiadomienie o Autosacale pocztą e-mail dla administratora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="88340-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="88340-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88340-112">PARAMETERS</span></span>

### <span data-ttu-id="88340-113">-CustomEmail</span><span class="sxs-lookup"><span data-stu-id="88340-113">-CustomEmail</span></span>
<span data-ttu-id="88340-114">Określa listę adresów e-mail rozdzielonych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="88340-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="88340-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88340-115">-DefaultProfile</span></span>
<span data-ttu-id="88340-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="88340-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88340-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="88340-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="88340-118">Wskazuje, że ta operacja wysyła powiadomienie e-mail do administratora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="88340-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="88340-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="88340-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="88340-120">Wskazuje, że ta operacja wysyła powiadomienie e-mail do współadministratora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="88340-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="88340-121">-Webhook</span><span class="sxs-lookup"><span data-stu-id="88340-121">-Webhook</span></span>
<span data-ttu-id="88340-122">Określa listę rozdzielanych przecinkami punktów webhook.</span><span class="sxs-lookup"><span data-stu-id="88340-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="88340-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88340-123">CommonParameters</span></span>
<span data-ttu-id="88340-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88340-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88340-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="88340-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88340-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88340-126">INPUTS</span></span>

### <span data-ttu-id="88340-127">Microsoft. Azure. Management. Monitor. Management. models. WebhookNotification []</span><span class="sxs-lookup"><span data-stu-id="88340-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="88340-128">System. String []</span><span class="sxs-lookup"><span data-stu-id="88340-128">System.String[]</span></span>

### <span data-ttu-id="88340-129">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="88340-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="88340-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88340-130">OUTPUTS</span></span>

### <span data-ttu-id="88340-131">Microsoft. Azure. Management. Monitor. Management. models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="88340-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="88340-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88340-132">NOTES</span></span>

## <span data-ttu-id="88340-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88340-133">RELATED LINKS</span></span>

[<span data-ttu-id="88340-134">Nowe — AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="88340-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


