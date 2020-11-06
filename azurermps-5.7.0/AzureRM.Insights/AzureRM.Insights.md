---
Module Name: AzureRM.Insights
Module Guid: 698c387c-bd6b-41c6-82ce-721f1ef39548
Download Help Link:
  object Object: 
Help Version:
  object Object: 
Locale: en-US
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/AzureRM.Insights.md
ms.openlocfilehash: d4f7819a3ddbf49f4a3c4ed56cd8273b1f2e1848
ms.sourcegitcommit: 43f4bdf2a59dd82fd881512aa9761bf72eb5703c
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/23/2019
ms.locfileid: "93522817"
---
# Moduł AzureRM. Insights
## Opis
Ten temat zawiera tematy pomocy dotyczące apletów poleceń usługi Azure Insights.

## AzureRM. Informacje o poleceniach cmdlet
### [Dodaj-AzureRmAutoscaleSetting](Add-AzureRmAutoscaleSetting.md)
Umożliwia utworzenie ustawienia skalowania automatycznego.

### [Dodaj-AzureRmLogAlertRule](Add-AzureRmLogAlertRule.md)
Dodanie lub zastąpienie reguły alertu dziennika.

### [Dodaj-AzureRmLogProfile](Add-AzureRmLogProfile.md)
Tworzy nowy profil dziennika aktywności. Ten profil służy do archiwizowania dziennika aktywności na koncie usługi Azure Storage lub przesyłania strumieniowego do centrum zdarzeń platformy Azure w ramach tej samej subskrypcji. 

- **Konto magazynu** — obsługiwane jest tylko standardowe konto magazynu (konto magazynu Premium jest nieobsługiwane). Być może jest to typ ARM lub klasyczny. Jeśli jest on zarejestrowany na koncie magazynu, koszty przechowywania dziennika aktywności są rozliczane według zwykłych standardowych stawek za składowanie. Tylko jeden profil dziennika dla jednej subskrypcji może zawierać tylko jedno konto magazynu na jedną subskrypcję, aby wyeksportować dziennik aktywności. 

- **Centrum zdarzeń** — tylko jeden profil dziennika dla jednej subskrypcji może mieć tylko jeden centrum zdarzeń na subskrypcję, aby wyeksportować dziennik aktywności. Jeśli dziennik aktywności jest przesyłany strumieniowo do centrum zdarzeń, będą obowiązywać standardowe ceny centrum zdarzeń. 

Zdarzenia w dzienniku aktywności mogą dotyczyć regionu lub mogą być "globalnymi". Globalnym względnie oznacza, że te zdarzenia są regionem agnostics i są niezależne od regionu, w rzeczywistości większość wydarzeń należy do tej kategorii. Jeśli profil dziennika aktywności jest ustawiony na podstawie portalu, domyślnie dodawany jest komunikat "globalny" wraz z dowolnym innym regionem wybranym w interfejsie użytkownika. W przypadku korzystania z polecenia cmdlet lokalizacja "Global" musi być jawnie wymieniona poza dowolnym innym regionem. 

**Uwaga** : w **przypadku niepowodzenia ustawienia "globalne" w lokalizacjach nie będzie można eksportować dziennika aktywności.** 

### [Dodaj-AzureRmMetricAlertRule](Add-AzureRmMetricAlertRule.md)
Umożliwia dodanie lub zaktualizowanie reguły alertu opartego na metrykach.

### [Dodaj-AzureRmWebtestAlertRule](Add-AzureRmWebtestAlertRule.md)
Umożliwia dodanie lub zaktualizowanie reguły alertu WebTest.

### [Disable-AzureRmActivityLogAlert](Disable-AzureRmActivityLogAlert.md)
Wyłącza alert dziennika aktywności i ustawia jego Tagi.

### [Enable-AzureRmActivityLogAlert](Enable-AzureRmActivityLogAlert.md)
Włącza alert dziennika aktywności i ustawia jego Tagi.

### [Get-AzureRmActionGroup](Get-AzureRmActionGroup.md)
Pobiera grupy akcji.

### [Get-AzureRmActivityLogAlert](Get-AzureRmActivityLogAlert.md)
Pobiera jeden lub więcej zasobów alertów dziennika aktywności.

### [Get-AzureRmAlertHistory](Get-AzureRmAlertHistory.md)
Pobiera historię alertów.

### [Get-AzureRmAlertRule](Get-AzureRmAlertRule.md)
Pobiera reguły alertów.

### [Get-AzureRmAutoscaleHistory](Get-AzureRmAutoscaleHistory.md)
Pobiera historię autoskalowania.

### [Get-AzureRmAutoscaleSetting](Get-AzureRmAutoscaleSetting.md)
Pobiera ustawienia autoskalowania.

### [Get-AzureRmDiagnosticSetting](Get-AzureRmDiagnosticSetting.md)
Pobiera zarejestrowane kategorie i ziarno czasu.

### [Get-AzureRmLog](Get-AzureRmLog.md)
Pobiera dziennik zdarzeń.

### [Get-AzureRmLogProfile](Get-AzureRmLogProfile.md)
Pobiera profil dziennika.

### [Get-AzureRmMetric](Get-AzureRmMetric.md)
Pobiera wartości metryki zasobu.

### [Get-AzureRmMetricDefinition](Get-AzureRmMetricDefinition.md)
Pobiera definicje metryk.

### [Get-AzureRmUsage](Get-AzureRmUsage.md)
Pobiera metryki użycia zasobu.

### [Nowe — AzureRmActionGroup](New-AzureRmActionGroup.md)
Tworzy obiekt odwołania do obiektu Actions w pamięci.

### [Nowe — AzureRmActionGroupReceiver](New-AzureRmActionGroupReceiver.md)
Tworzy nowy odbiorcę grupy akcji.

### [Nowe — AzureRmActivityLogAlertCondition](New-AzureRmActivityLogAlertCondition.md)
Umożliwia utworzenie nowego obiektu warunkowego alertu dziennika aktywności w pamięci.

### [Nowe — AzureRmAlertRuleEmail](New-AzureRmAlertRuleEmail.md)
Umożliwia utworzenie akcji poczty e-mail dla reguły alertu.

### [Nowe — AzureRmAlertRuleWebhook](New-AzureRmAlertRuleWebhook.md)
Tworzy element webhook reguły alertu.

### [Nowe — AzureRmAutoscaleNotification](New-AzureRmAutoscaleNotification.md)
Umożliwia utworzenie powiadomienia e-mail autoskalowania.

### [Nowe — AzureRmAutoscaleProfile](New-AzureRmAutoscaleProfile.md)
Tworzy profil autoskalowania.

### [Nowe — AzureRmAutoscaleRule](New-AzureRmAutoscaleRule.md)
Umożliwia utworzenie reguły skalowania automatycznego.

### [Nowe — AzureRmAutoscaleWebhook](New-AzureRmAutoscaleWebhook.md)
Umożliwia utworzenie elementu webhook autoskalowania.

### [Remove-AzureRmActionGroup](Remove-AzureRmActionGroup.md)
Usuwa grupę akcji.

### [Remove-AzureRmActivityLogAlert](Remove-AzureRmActivityLogAlert.md)
Usuwa alert dziennika aktywności.

### [Remove-AzureRmAlertRule](Remove-AzureRmAlertRule.md)
Usuwa regułę alertu.

### [Remove-AzureRmAutoscaleSetting](Remove-AzureRmAutoscaleSetting.md)
Usuwa ustawienie skalowania automatycznego.

### [Remove-AzureRmLogProfile](Remove-AzureRmLogProfile.md)
Usuwa profil dziennika.

### [Set-AzureRmActionGroup](Set-AzureRmActionGroup.md)
Umożliwia utworzenie nowej lub zaktualizowanie istniejącej grupy akcji.

### [Set-AzureRmActivityLogAlert](Set-AzureRmActivityLogAlert.md)
Tworzy nowy lub ustawia istniejący alert dziennika aktywności.

### [Set-AzureRmDiagnosticSetting](Set-AzureRmDiagnosticSetting.md)
Ustawia ustawienia dzienników i metryk dla zasobu.

