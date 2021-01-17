---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: c7821ddfd07b17a77c482a770b28672ccd664cb4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490785"
---
# <span data-ttu-id="8f511-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="8f511-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="8f511-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8f511-102">SYNOPSIS</span></span>
<span data-ttu-id="8f511-103">Skonfiguruj ustawienia powiadomień usługi Azure Site Recovery (powiadomienie e-mail) dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="8f511-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="8f511-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8f511-104">SYNTAX</span></span>

### <span data-ttu-id="8f511-105">Set (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="8f511-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f511-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="8f511-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f511-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="8f511-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f511-108">Wyłącza</span><span class="sxs-lookup"><span data-stu-id="8f511-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f511-109">Opis</span><span class="sxs-lookup"><span data-stu-id="8f511-109">DESCRIPTION</span></span>
<span data-ttu-id="8f511-110">Polecenie cmdlet **Set-AzRecoveryServicesAsrNotificationSetting** konfiguruje ustawienia powiadomień usługi Azure Site Recovery (powiadomienie e-mail) dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="8f511-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="8f511-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8f511-111">EXAMPLES</span></span>

### <span data-ttu-id="8f511-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8f511-112">Example 1</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="8f511-113">Wyłącz powiadomienie.</span><span class="sxs-lookup"><span data-stu-id="8f511-113">Disable notification.</span></span>

### <span data-ttu-id="8f511-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="8f511-114">Example 2</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="8f511-115">Ustaw powiadomienia dla niestandardowych adresów e-mail i właściciela subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8f511-115">Set notification for custom email address(s) and for subscription owner.</span></span>

### <span data-ttu-id="8f511-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="8f511-116">Example 3</span></span>

<span data-ttu-id="8f511-117">Skonfiguruj ustawienia powiadomień usługi Azure Site Recovery (powiadomienie e-mail) dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="8f511-117">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span> <span data-ttu-id="8f511-118">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="8f511-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress 'abcxxxx@xxxx.com' -DisableEmailToSubscriptionOwner
```

## <span data-ttu-id="8f511-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8f511-119">PARAMETERS</span></span>

### <span data-ttu-id="8f511-120">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="8f511-120">-CustomEmailAddress</span></span>
<span data-ttu-id="8f511-121">Alert/powiadomienie wysłane do wiadomości e-mail.</span><span class="sxs-lookup"><span data-stu-id="8f511-121">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="8f511-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f511-122">-DefaultProfile</span></span>
<span data-ttu-id="8f511-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8f511-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8f511-124">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="8f511-124">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="8f511-125">Parametr Switch określa włączenie powiadomienia do właściciela subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8f511-125">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="8f511-126">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="8f511-126">-DisableNotification</span></span>
<span data-ttu-id="8f511-127">Flaga, aby wyłączyć wszystkie powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="8f511-127">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="8f511-128">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="8f511-128">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="8f511-129">Parametr Switch określa włączenie powiadomienia do właściciela subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="8f511-129">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="8f511-130">-LocaleID</span><span class="sxs-lookup"><span data-stu-id="8f511-130">-LocaleID</span></span>
<span data-ttu-id="8f511-131">Język poczty e-mail alertu/Notification użytkownikowi (obsługiwane kody kultur firmy Microsoft).</span><span class="sxs-lookup"><span data-stu-id="8f511-131">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="8f511-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8f511-132">-Confirm</span></span>
<span data-ttu-id="8f511-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f511-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f511-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f511-134">-WhatIf</span></span>
<span data-ttu-id="8f511-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8f511-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8f511-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8f511-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f511-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f511-137">CommonParameters</span></span>
<span data-ttu-id="8f511-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8f511-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f511-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8f511-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f511-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8f511-140">INPUTS</span></span>

### <span data-ttu-id="8f511-141">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="8f511-141">None</span></span>

## <span data-ttu-id="8f511-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8f511-142">OUTPUTS</span></span>

### <span data-ttu-id="8f511-143">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="8f511-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="8f511-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8f511-144">NOTES</span></span>

## <span data-ttu-id="8f511-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8f511-145">RELATED LINKS</span></span>
