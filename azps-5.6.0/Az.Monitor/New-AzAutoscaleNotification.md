---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: c537908d2249ca5ec8a33adffa4e655b0a9ec6e6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982666"
---
# <span data-ttu-id="88524-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="88524-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="88524-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88524-102">SYNOPSIS</span></span>
<span data-ttu-id="88524-103">Tworzy powiadomienie e-mail o automatycznym skalowaniach.</span><span class="sxs-lookup"><span data-stu-id="88524-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="88524-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="88524-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88524-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="88524-105">DESCRIPTION</span></span>
<span data-ttu-id="88524-106">Polecenie **cmdlet New-AzAutoscaleNotification** tworzy powiadomienie e-mail dla skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="88524-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="88524-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="88524-107">EXAMPLES</span></span>

### <span data-ttu-id="88524-108">Przykład 1. Tworzenie powiadomienia e-mail z automatycznym skalowaniem</span><span class="sxs-lookup"><span data-stu-id="88524-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="88524-109">To polecenie tworzy powiadomienie e-mail Autosacale dla dwóch określonych adresów.</span><span class="sxs-lookup"><span data-stu-id="88524-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="88524-110">Przykład 2. Tworzenie powiadomienia e-mail o automatycznym skalowania dla administratora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="88524-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="88524-111">To polecenie tworzy powiadomienie e-mail Autosacale dla administratora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="88524-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="88524-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88524-112">PARAMETERS</span></span>

### <span data-ttu-id="88524-113">- CustomEmail</span><span class="sxs-lookup"><span data-stu-id="88524-113">-CustomEmail</span></span>
<span data-ttu-id="88524-114">Określa rozdzieloną przecinkami listę adresów e-mail.</span><span class="sxs-lookup"><span data-stu-id="88524-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="88524-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88524-115">-DefaultProfile</span></span>
<span data-ttu-id="88524-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="88524-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="88524-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="88524-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="88524-118">Oznacza, że ta operacja wysyła powiadomienie e-mail do administratora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="88524-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="88524-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="88524-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="88524-120">Oznacza, że ta operacja wysyła powiadomienie e-mail do współwłasnych administratorów subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="88524-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="88524-121">- Webhook</span><span class="sxs-lookup"><span data-stu-id="88524-121">-Webhook</span></span>
<span data-ttu-id="88524-122">Określa rozdzielaną przecinkami listę autoskalowania sieci Web.</span><span class="sxs-lookup"><span data-stu-id="88524-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="88524-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88524-123">CommonParameters</span></span>
<span data-ttu-id="88524-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88524-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88524-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="88524-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88524-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88524-126">INPUTS</span></span>

### <span data-ttu-id="88524-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span><span class="sxs-lookup"><span data-stu-id="88524-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="88524-128">System.String[]</span><span class="sxs-lookup"><span data-stu-id="88524-128">System.String[]</span></span>

### <span data-ttu-id="88524-129">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="88524-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="88524-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88524-130">OUTPUTS</span></span>

### <span data-ttu-id="88524-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="88524-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="88524-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="88524-132">NOTES</span></span>

## <span data-ttu-id="88524-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88524-133">RELATED LINKS</span></span>

[<span data-ttu-id="88524-134">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="88524-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


