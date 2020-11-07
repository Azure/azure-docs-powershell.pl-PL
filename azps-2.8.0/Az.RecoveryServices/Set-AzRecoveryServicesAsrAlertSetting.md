---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 21106b2c5a8e36f58b6593049fccf28994b0af46
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872596"
---
# <span data-ttu-id="33a13-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="33a13-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="33a13-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="33a13-102">SYNOPSIS</span></span>
<span data-ttu-id="33a13-103">Skonfiguruj ustawienia powiadomień usługi Azure Site Recovery (powiadomienie e-mail) dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="33a13-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="33a13-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="33a13-104">SYNTAX</span></span>

### <span data-ttu-id="33a13-105">Set (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="33a13-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33a13-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="33a13-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33a13-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="33a13-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="33a13-108">Wyłącza</span><span class="sxs-lookup"><span data-stu-id="33a13-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33a13-109">Opis</span><span class="sxs-lookup"><span data-stu-id="33a13-109">DESCRIPTION</span></span>
<span data-ttu-id="33a13-110">Polecenie cmdlet **Set-AzRecoveryServicesAsrNotificationSetting** konfiguruje ustawienia powiadomień usługi Azure Site Recovery (powiadomienie e-mail) dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="33a13-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="33a13-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="33a13-111">EXAMPLES</span></span>

### <span data-ttu-id="33a13-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="33a13-112">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="33a13-113">Wyłącz powiadomienie.</span><span class="sxs-lookup"><span data-stu-id="33a13-113">Disable notification.</span></span>

### <span data-ttu-id="33a13-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="33a13-114">Example 2</span></span>
```
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="33a13-115">Ustaw powiadomienia dla niestandardowych adresów e-mail i właściciela subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="33a13-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="33a13-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="33a13-116">PARAMETERS</span></span>

### <span data-ttu-id="33a13-117">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="33a13-117">-CustomEmailAddress</span></span>
<span data-ttu-id="33a13-118">Alert/powiadomienie wysłane do wiadomości e-mail.</span><span class="sxs-lookup"><span data-stu-id="33a13-118">Alert / Notification sent to emails.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33a13-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33a13-119">-DefaultProfile</span></span>
<span data-ttu-id="33a13-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="33a13-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="33a13-121">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="33a13-121">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="33a13-122">Parametr Switch określa włączenie powiadomienia do właściciela subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="33a13-122">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableEmailToSubcriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33a13-123">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="33a13-123">-DisableNotification</span></span>
<span data-ttu-id="33a13-124">Flaga, aby wyłączyć wszystkie powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="33a13-124">Flag to disable all notification.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33a13-125">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="33a13-125">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="33a13-126">Parametr Switch określa włączenie powiadomienia do właściciela subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="33a13-126">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EmailToSubscriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33a13-127">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="33a13-127">-LocaleID</span></span>
<span data-ttu-id="33a13-128">Język poczty e-mail alertu/Notification użytkownikowi (obsługiwane kody kultur firmy Microsoft).</span><span class="sxs-lookup"><span data-stu-id="33a13-128">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

```yaml
Type: System.String
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33a13-129">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="33a13-129">-Confirm</span></span>
<span data-ttu-id="33a13-130">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33a13-130">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33a13-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33a13-131">-WhatIf</span></span>
<span data-ttu-id="33a13-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33a13-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="33a13-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="33a13-133">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33a13-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33a13-134">CommonParameters</span></span>
<span data-ttu-id="33a13-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33a13-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33a13-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="33a13-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33a13-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33a13-137">INPUTS</span></span>

### <span data-ttu-id="33a13-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="33a13-138">None</span></span>

## <span data-ttu-id="33a13-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="33a13-139">OUTPUTS</span></span>

### <span data-ttu-id="33a13-140">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="33a13-140">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="33a13-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="33a13-141">NOTES</span></span>

## <span data-ttu-id="33a13-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33a13-142">RELATED LINKS</span></span>
