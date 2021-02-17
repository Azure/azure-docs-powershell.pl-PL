---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasralertsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrAlertSetting.md
ms.openlocfilehash: c7821ddfd07b17a77c482a770b28672ccd664cb4
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191323"
---
# <span data-ttu-id="9d384-101">Set-AzRecoveryServicesAsrAlertSetting</span><span class="sxs-lookup"><span data-stu-id="9d384-101">Set-AzRecoveryServicesAsrAlertSetting</span></span>

## <span data-ttu-id="9d384-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d384-102">SYNOPSIS</span></span>
<span data-ttu-id="9d384-103">Skonfiguruj ustawienia powiadomień usługi Azure Site Recovery (powiadomienie e-mail) dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="9d384-103">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="9d384-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9d384-104">SYNTAX</span></span>

### <span data-ttu-id="9d384-105">Ustaw (domyślne)</span><span class="sxs-lookup"><span data-stu-id="9d384-105">Set (Default)</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-CustomEmailAddress <String[]>] [-LocaleID <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d384-106">EmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="9d384-106">EmailToSubscriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-EnableEmailSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d384-107">DisableEmailToSubcriptionOwner</span><span class="sxs-lookup"><span data-stu-id="9d384-107">DisableEmailToSubcriptionOwner</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableEmailToSubscriptionOwner] [-CustomEmailAddress <String[]>]
 [-LocaleID <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d384-108">Wyłącz</span><span class="sxs-lookup"><span data-stu-id="9d384-108">Disable</span></span>
```
Set-AzRecoveryServicesAsrAlertSetting [-DisableNotification] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d384-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="9d384-109">DESCRIPTION</span></span>
<span data-ttu-id="9d384-110">Polecenie **cmdlet Set-AzRecoveryServicesAsrNotificationSetting** konfiguruje ustawienia powiadomień usługi Azure Site Recovery (powiadomienie e-mail) dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="9d384-110">The **Set-AzRecoveryServicesAsrNotificationSetting** cmdlet configures Azure Site Recovery notification settings (email notification) for the vault.</span></span>

## <span data-ttu-id="9d384-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9d384-111">EXAMPLES</span></span>

### <span data-ttu-id="9d384-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9d384-112">Example 1</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -DisableNotification

CustomEmailAddress EmailSubscriptionOwner Locale
------------------ ---------------------- ------
{}                 Off                    en-US
```

<span data-ttu-id="9d384-113">Wyłącz powiadomienie.</span><span class="sxs-lookup"><span data-stu-id="9d384-113">Disable notification.</span></span>

### <span data-ttu-id="9d384-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="9d384-114">Example 2</span></span>
```powershell
PS C:\> Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress "abcxxxx@xxxx.com" -EnableEmailSubscriptionOwner

CustomEmailAddress     EmailSubscriptionOwner Locale
------------------     ---------------------- ------
{abcxxxx@xxxx.com} On                     en-US
```

<span data-ttu-id="9d384-115">Ustaw powiadomienia dla niestandardowych adresów e-mail i dla właściciela subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9d384-115">Set notification for custom email address(s) and for subscription owner.</span></span>

### <span data-ttu-id="9d384-116">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="9d384-116">Example 3</span></span>

<span data-ttu-id="9d384-117">Skonfiguruj ustawienia powiadomień usługi Azure Site Recovery (powiadomienie e-mail) dla magazynu.</span><span class="sxs-lookup"><span data-stu-id="9d384-117">Configure Azure Site Recovery notification settings (email notification) for the vault.</span></span> <span data-ttu-id="9d384-118">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="9d384-118">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzRecoveryServicesAsrAlertSetting -CustomEmailAddress 'abcxxxx@xxxx.com' -DisableEmailToSubscriptionOwner
```

## <span data-ttu-id="9d384-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d384-119">PARAMETERS</span></span>

### <span data-ttu-id="9d384-120">-CustomEmailAddress</span><span class="sxs-lookup"><span data-stu-id="9d384-120">-CustomEmailAddress</span></span>
<span data-ttu-id="9d384-121">Alert / Powiadomienie wysłane do wiadomości e-mail.</span><span class="sxs-lookup"><span data-stu-id="9d384-121">Alert / Notification sent to emails.</span></span>

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

### <span data-ttu-id="9d384-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d384-122">-DefaultProfile</span></span>
<span data-ttu-id="9d384-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9d384-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9d384-124">-DisableEmailToSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="9d384-124">-DisableEmailToSubscriptionOwner</span></span>
<span data-ttu-id="9d384-125">Parametr przełącznika określa włącz powiadomienie dla właściciela subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9d384-125">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="9d384-126">-DisableNotification</span><span class="sxs-lookup"><span data-stu-id="9d384-126">-DisableNotification</span></span>
<span data-ttu-id="9d384-127">Oflaguj, aby wyłączyć wszystkie powiadomienia.</span><span class="sxs-lookup"><span data-stu-id="9d384-127">Flag to disable all notification.</span></span>

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

### <span data-ttu-id="9d384-128">-EnableEmailSubscriptionOwner</span><span class="sxs-lookup"><span data-stu-id="9d384-128">-EnableEmailSubscriptionOwner</span></span>
<span data-ttu-id="9d384-129">Parametr przełącznika określa włącz powiadomienie dla właściciela subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9d384-129">Switch parameter specifies enable notification to subscription owner.</span></span>

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

### <span data-ttu-id="9d384-130">- LocaleID</span><span class="sxs-lookup"><span data-stu-id="9d384-130">-LocaleID</span></span>
<span data-ttu-id="9d384-131">Język wiadomości e-mail alertu /powiadomienia dla użytkownika (obsługiwane kody kultury firmy microsoft).</span><span class="sxs-lookup"><span data-stu-id="9d384-131">Email language of alert /notification to user(supported culture codes from microsoft).</span></span> 

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

### <span data-ttu-id="9d384-132">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9d384-132">-Confirm</span></span>
<span data-ttu-id="9d384-133">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9d384-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d384-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9d384-134">-WhatIf</span></span>
<span data-ttu-id="9d384-135">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9d384-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d384-136">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9d384-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d384-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d384-137">CommonParameters</span></span>
<span data-ttu-id="9d384-138">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d384-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d384-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9d384-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d384-140">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d384-140">INPUTS</span></span>

### <span data-ttu-id="9d384-141">Brak</span><span class="sxs-lookup"><span data-stu-id="9d384-141">None</span></span>

## <span data-ttu-id="9d384-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9d384-142">OUTPUTS</span></span>

### <span data-ttu-id="9d384-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span><span class="sxs-lookup"><span data-stu-id="9d384-143">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAlertSetting</span></span>

## <span data-ttu-id="9d384-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9d384-144">NOTES</span></span>

## <span data-ttu-id="9d384-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9d384-145">RELATED LINKS</span></span>
