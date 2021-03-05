---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: 049e1667fec5aef4f12a9912a4b9669364095b0c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997473"
---
# <span data-ttu-id="a1716-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="a1716-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="a1716-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1716-102">SYNOPSIS</span></span>
<span data-ttu-id="a1716-103">Skonfiguruj ustawienia powiadomień usługi Azure Site Recovery (powiadomienie e-mail) dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="a1716-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="a1716-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a1716-104">SYNTAX</span></span>

### <span data-ttu-id="a1716-105">Ustaw (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a1716-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1716-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="a1716-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1716-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="a1716-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1716-108">Wyłącz</span><span class="sxs-lookup"><span data-stu-id="a1716-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a1716-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="a1716-109">DESCRIPTION</span></span>
<span data-ttu-id="a1716-110">Polecenie **cmdlet Set-AzRecoveryServicesAsrNotificationSetting** konfiguruje ustawienia powiadomień usługi Azure Site Recovery (powiadomienie e-mail) dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="a1716-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="a1716-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a1716-111">EXAMPLES</span></span>

### <span data-ttu-id="a1716-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a1716-112">Example 1</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="a1716-113">Wyłącz powiadomienie.</span><span class="sxs-lookup"><span data-stu-id="a1716-113">Disable notification.</span></span>

### <span data-ttu-id="a1716-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a1716-114">Example 2</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="a1716-115">Ustaw powiadomienia dla niestandardowych adresów e-mail i dla właściciela subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a1716-115">Set notification for custom email address(s) and for subscription owner.</span></span>

### <span data-ttu-id="a1716-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a1716-116">Example 3</span></span>

<span data-ttu-id="a1716-117">Skonfiguruj ustawienia powiadomień usługi Azure Site Recovery (powiadomienie e-mail) dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="a1716-117">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span> <span data-ttu-id="a1716-118">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="a1716-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress 'abcxxxx@xxxx.com' -DisableEmailToSubscriptionOwner
```

## <span data-ttu-id="a1716-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a1716-119">PARAMETERS</span></span>

### <span data-ttu-id="a1716-120">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="a1716-120">-CustomEmailAddress</span></span>
<span data-ttu-id="a1716-121">Alert / Powiadomienie wysłane do wiadomości e-mail.</span><span class="sxs-lookup"><span data-stu-id="a1716-121">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="a1716-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1716-122">-DefaultProfile</span></span>
<span data-ttu-id="a1716-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1716-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a1716-124">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="a1716-124">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="a1716-125">Parametr przełącznika określa włącz powiadomienie dla właściciela subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a1716-125">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="a1716-126">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="a1716-126">-DisableNotification</span></span>
<span data-ttu-id="a1716-127">Oflaguj, aby wyłączyć wszystkie powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="a1716-127">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="a1716-128">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="a1716-128">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="a1716-129">Parametr przełącznika określa włącz powiadomienie dla właściciela subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="a1716-129">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="a1716-130">- LocaleID</span><span class="sxs-lookup"><span data-stu-id="a1716-130">-LocaleID</span></span>
<span data-ttu-id="a1716-131">Język wiadomości e-mail alertu /powiadomienia dla użytkownika (obsługiwane kody kultury firmy microsoft).</span><span class="sxs-lookup"><span data-stu-id="a1716-131">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="a1716-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a1716-132">-Confirm</span></span>
<span data-ttu-id="a1716-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a1716-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a1716-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1716-134">-WhatIf</span></span>
<span data-ttu-id="a1716-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1716-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1716-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a1716-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a1716-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1716-137">CommonParameters</span></span>
<span data-ttu-id="a1716-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1716-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1716-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a1716-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1716-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1716-140">INPUTS</span></span>

### <span data-ttu-id="a1716-141">Brak</span><span class="sxs-lookup"><span data-stu-id="a1716-141">None</span></span>

## <span data-ttu-id="a1716-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1716-142">OUTPUTS</span></span>

### <span data-ttu-id="a1716-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="a1716-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="a1716-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a1716-144">NOTES</span></span>

## <span data-ttu-id="a1716-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1716-145">RELATED LINKS</span></span>
