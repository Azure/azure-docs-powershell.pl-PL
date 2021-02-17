---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalenotification
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleNotification.md
ms.openlocfilehash: 010698183dec206002c0966fb8f37d629d24794a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192186"
---
# <span data-ttu-id="d7340-101">New-AzAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="d7340-101">New-AzAutoscaleNotification</span></span>

## <span data-ttu-id="d7340-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d7340-102">SYNOPSIS</span></span>
<span data-ttu-id="d7340-103">Tworzy powiadomienie e-mail z automatycznym skalowaniem.</span><span class="sxs-lookup"><span data-stu-id="d7340-103">Creates an Autoscale email notification.</span></span>

## <span data-ttu-id="d7340-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d7340-104">SYNTAX</span></span>

```
New-AzAutoscaleNotification [[-Webhook] <WebhookNotification[]>] [[-CustomEmail] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrator]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d7340-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d7340-105">DESCRIPTION</span></span>
<span data-ttu-id="d7340-106">Polecenie **cmdlet New-AzAutoscaleNotification** tworzy powiadomienie e-mail dla skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="d7340-106">The **New-AzAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="d7340-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d7340-107">EXAMPLES</span></span>

### <span data-ttu-id="d7340-108">Przykład 1. Tworzenie powiadomienia e-mail z automatycznym skalowaniem</span><span class="sxs-lookup"><span data-stu-id="d7340-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzAutoscaleNotification -CustomEmail "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="d7340-109">To polecenie tworzy powiadomienie e-mail Autosacale dla dwóch określonych adresów.</span><span class="sxs-lookup"><span data-stu-id="d7340-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="d7340-110">Przykład 2. Tworzenie powiadomienia e-mail o automatycznym skalowania dla administratora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="d7340-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="d7340-111">To polecenie powoduje utworzenie powiadomienia e-mail Autosacale dla administratora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d7340-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="d7340-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d7340-112">PARAMETERS</span></span>

### <span data-ttu-id="d7340-113">- CustomEmail</span><span class="sxs-lookup"><span data-stu-id="d7340-113">-CustomEmail</span></span>
<span data-ttu-id="d7340-114">Określa rozdzieloną przecinkami listę adresów e-mail.</span><span class="sxs-lookup"><span data-stu-id="d7340-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="d7340-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d7340-115">-DefaultProfile</span></span>
<span data-ttu-id="d7340-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="d7340-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d7340-117">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="d7340-117">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="d7340-118">Oznacza, że ta operacja wysyła powiadomienie e-mail do administratora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d7340-118">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="d7340-119">-SendEmailToSubscriptionCoAdministrator</span><span class="sxs-lookup"><span data-stu-id="d7340-119">-SendEmailToSubscriptionCoAdministrator</span></span>
<span data-ttu-id="d7340-120">Oznacza, że ta operacja wysyła powiadomienie e-mail do współwłasnych administratorów subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="d7340-120">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="d7340-121">- Webhook</span><span class="sxs-lookup"><span data-stu-id="d7340-121">-Webhook</span></span>
<span data-ttu-id="d7340-122">Określa rozdzielaną przecinkami listę autoskalowania sieci Web.</span><span class="sxs-lookup"><span data-stu-id="d7340-122">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="d7340-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d7340-123">CommonParameters</span></span>
<span data-ttu-id="d7340-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d7340-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d7340-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d7340-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d7340-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7340-126">INPUTS</span></span>

### <span data-ttu-id="d7340-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span><span class="sxs-lookup"><span data-stu-id="d7340-127">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification[]</span></span>

### <span data-ttu-id="d7340-128">System.String[]</span><span class="sxs-lookup"><span data-stu-id="d7340-128">System.String[]</span></span>

### <span data-ttu-id="d7340-129">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="d7340-129">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d7340-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d7340-130">OUTPUTS</span></span>

### <span data-ttu-id="d7340-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="d7340-131">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="d7340-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d7340-132">NOTES</span></span>

## <span data-ttu-id="d7340-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d7340-133">RELATED LINKS</span></span>

[<span data-ttu-id="d7340-134">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="d7340-134">New-AzAutoscaleWebhook</span></span>](./New-AzAutoscaleWebhook.md)


