---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/set-azurermrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 4e51cd90e490442c36b5864e53b4bb7a36e41e80
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544199"
---
# <span data-ttu-id="59bdb-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="59bdb-101">Set-AzureRmRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="59bdb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="59bdb-102">SYNOPSIS</span></span>
<span data-ttu-id="59bdb-103">Skonfiguruj ustawienia powiadomień usługi Azure Site Recovery (powiadomienie e-mail) dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="59bdb-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="59bdb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="59bdb-104">SYNTAX</span></span>

### <span data-ttu-id="59bdb-105">Set (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="59bdb-105">Set (Default)</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59bdb-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="59bdb-106">EmailToSubscriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59bdb-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="59bdb-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="59bdb-108">Wyłącza</span><span class="sxs-lookup"><span data-stu-id="59bdb-108">Disable</span></span>
```
Set-AzureRmRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59bdb-109">Opis</span><span class="sxs-lookup"><span data-stu-id="59bdb-109">DESCRIPTION</span></span>
<span data-ttu-id="59bdb-110">Polecenie cmdlet **Set-AzureRmRecoveryServicesAsrNotificationSetting** konfiguruje ustawienia powiadomień usługi Azure Site Recovery (powiadomienie e-mail) dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="59bdb-110">The **Set-AzureRmRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="59bdb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="59bdb-111">EXAMPLES</span></span>

### <span data-ttu-id="59bdb-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="59bdb-112">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="59bdb-113">Wyłącz powiadomienie.</span><span class="sxs-lookup"><span data-stu-id="59bdb-113">Disable notification.</span></span>

### <span data-ttu-id="59bdb-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="59bdb-114">Example 2</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="59bdb-115">Ustaw powiadomienia dla niestandardowych adresów e-mail i właściciela subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="59bdb-115">Set notification for custom email address(s) and for subscription owner.</span></span>

## <span data-ttu-id="59bdb-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="59bdb-116">PARAMETERS</span></span>

### <span data-ttu-id="59bdb-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="59bdb-117">-Confirm</span></span>
<span data-ttu-id="59bdb-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59bdb-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bdb-119">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="59bdb-119">-CustomEmailAddress</span></span>
<span data-ttu-id="59bdb-120">Alert/powiadomienie wysłane do wiadomości e-mail.</span><span class="sxs-lookup"><span data-stu-id="59bdb-120">Alert / Notification sent to emails.</span></span>

```yaml
Type: String[]
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bdb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59bdb-121">-DefaultProfile</span></span>
<span data-ttu-id="59bdb-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="59bdb-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bdb-123">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="59bdb-123">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="59bdb-124">Parametr Switch określa włączenie powiadomienia do właściciela subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="59bdb-124">Switch parameter specifies enable notification to subscription owner.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableEmailToSubcriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bdb-125">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="59bdb-125">-DisableNotification</span></span>
<span data-ttu-id="59bdb-126">Flaga, aby wyłączyć wszystkie powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="59bdb-126">Flag to disable all notification.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Disable
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bdb-127">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="59bdb-127">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="59bdb-128">Parametr Switch określa włączenie powiadomienia do właściciela subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="59bdb-128">Switch paramter specifies enable notification to subscription owner.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EmailToSubscriptionOwner
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bdb-129">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="59bdb-129">-LocaleID</span></span>
<span data-ttu-id="59bdb-130">Język poczty e-mail alertu/notifcation użytkownikowi (obsługiwane kody kultur firmy Microsoft).</span><span class="sxs-lookup"><span data-stu-id="59bdb-130">Email language of alert /notifcation to user(supported culture codes from microsoft).</span></span> 

```yaml
Type: String
Parameter Sets: Set, EmailToSubscriptionOwner, DisableEmailToSubcriptionOwner
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bdb-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59bdb-131">-WhatIf</span></span>
<span data-ttu-id="59bdb-132">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59bdb-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59bdb-133">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="59bdb-133">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59bdb-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59bdb-134">CommonParameters</span></span>
<span data-ttu-id="59bdb-135">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59bdb-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59bdb-136">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59bdb-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59bdb-137">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59bdb-137">INPUTS</span></span>

### <span data-ttu-id="59bdb-138">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="59bdb-138">None</span></span>

## <span data-ttu-id="59bdb-139">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="59bdb-139">OUTPUTS</span></span>

### <span data-ttu-id="59bdb-140">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 0.1.1.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="59bdb-140">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="59bdb-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="59bdb-141">NOTES</span></span>

## <span data-ttu-id="59bdb-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59bdb-142">RELATED LINKS</span></span>
