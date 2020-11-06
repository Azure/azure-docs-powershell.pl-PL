---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5B5F494-D912-40D0-99E2-A62FAACA3EC9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleNotification.md
ms.openlocfilehash: f6791d2cc962f0bb0db038ad8c5391425c09bfbe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553308"
---
# <span data-ttu-id="41a4f-101">New-AzureRmAutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="41a4f-101">New-AzureRmAutoscaleNotification</span></span>

## <span data-ttu-id="41a4f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="41a4f-102">SYNOPSIS</span></span>
<span data-ttu-id="41a4f-103">Umożliwia utworzenie powiadomienia e-mail autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="41a4f-103">Creates an Autoscale email notification.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="41a4f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="41a4f-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleNotification [[-Webhooks] <WebhookNotification[]>] [[-CustomEmails] <String[]>]
 [-SendEmailToSubscriptionAdministrator] [-SendEmailToSubscriptionCoAdministrators]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="41a4f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="41a4f-105">DESCRIPTION</span></span>
<span data-ttu-id="41a4f-106">Polecenie cmdlet **New-AzureRmAutoscaleNotification** umożliwia utworzenie powiadomienia e-mail w celu automatycznego skalowania.</span><span class="sxs-lookup"><span data-stu-id="41a4f-106">The **New-AzureRmAutoscaleNotification** cmdlet creates an email notification for Autoscale.</span></span>

## <span data-ttu-id="41a4f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="41a4f-107">EXAMPLES</span></span>

### <span data-ttu-id="41a4f-108">Przykład 1: Tworzenie powiadomienia e-mail autoskalowania</span><span class="sxs-lookup"><span data-stu-id="41a4f-108">Example 1: Create an Autoscale email notification</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -CustomEmails "pattif@contoso.com, davidchew@contoso.net"
```

<span data-ttu-id="41a4f-109">To polecenie tworzy powiadomienie o Autosacale e-mail dla dwóch określonych adresów.</span><span class="sxs-lookup"><span data-stu-id="41a4f-109">This command creates an Autosacale email notification for two specified addresses.</span></span>

### <span data-ttu-id="41a4f-110">Przykład 2: Tworzenie powiadomienia e-mail autoskalowania dla administratora subskrypcji</span><span class="sxs-lookup"><span data-stu-id="41a4f-110">Example 2: Create an Autoscale email notification for the subscription administrator</span></span>
```
PS C:\>New-AzureRmAutoscaleNotification -SendEmailToSubscriptionAdministrator
```

<span data-ttu-id="41a4f-111">To polecenie tworzy powiadomienie o Autosacale pocztą e-mail dla administratora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="41a4f-111">This command creates an Autosacale email notification for the subscription administrator.</span></span>

## <span data-ttu-id="41a4f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="41a4f-112">PARAMETERS</span></span>

### <span data-ttu-id="41a4f-113">-CustomEmails</span><span class="sxs-lookup"><span data-stu-id="41a4f-113">-CustomEmails</span></span>
<span data-ttu-id="41a4f-114">Określa listę adresów e-mail rozdzielonych przecinkami.</span><span class="sxs-lookup"><span data-stu-id="41a4f-114">Specifies a comma-separated list of email addresses.</span></span>

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

### <span data-ttu-id="41a4f-115">-SendEmailToSubscriptionAdministrator</span><span class="sxs-lookup"><span data-stu-id="41a4f-115">-SendEmailToSubscriptionAdministrator</span></span>
<span data-ttu-id="41a4f-116">Wskazuje, że ta operacja wysyła powiadomienie e-mail do administratora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="41a4f-116">Indicates that this operation sends an email notification to the subscription administrator.</span></span>

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

### <span data-ttu-id="41a4f-117">-SendEmailToSubscriptionCoAdministrators</span><span class="sxs-lookup"><span data-stu-id="41a4f-117">-SendEmailToSubscriptionCoAdministrators</span></span>
<span data-ttu-id="41a4f-118">Wskazuje, że ta operacja wysyła powiadomienie e-mail do współadministratora subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="41a4f-118">Indicates that this operation sends an email notification to the subscription co-administrators.</span></span>

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

### <span data-ttu-id="41a4f-119">-Haki internetowe</span><span class="sxs-lookup"><span data-stu-id="41a4f-119">-Webhooks</span></span>
<span data-ttu-id="41a4f-120">Określa listę rozdzielanych przecinkami punktów webhook.</span><span class="sxs-lookup"><span data-stu-id="41a4f-120">Specifies a comma-separated list of Autoscale webhooks.</span></span>

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

### <span data-ttu-id="41a4f-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="41a4f-121">-DefaultProfile</span></span>
<span data-ttu-id="41a4f-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="41a4f-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="41a4f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="41a4f-123">CommonParameters</span></span>
<span data-ttu-id="41a4f-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="41a4f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="41a4f-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="41a4f-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="41a4f-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="41a4f-126">INPUTS</span></span>

## <span data-ttu-id="41a4f-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="41a4f-127">OUTPUTS</span></span>

### <span data-ttu-id="41a4f-128">Microsoft. Azure. Management. Monitor. Management. models. AutoscaleNotification</span><span class="sxs-lookup"><span data-stu-id="41a4f-128">Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification</span></span>

## <span data-ttu-id="41a4f-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="41a4f-129">NOTES</span></span>

## <span data-ttu-id="41a4f-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="41a4f-130">RELATED LINKS</span></span>

[<span data-ttu-id="41a4f-131">Nowe — AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="41a4f-131">New-AzureRmAutoscaleWebhook</span></span>](./New-AzureRmAutoscaleWebhook.md)


