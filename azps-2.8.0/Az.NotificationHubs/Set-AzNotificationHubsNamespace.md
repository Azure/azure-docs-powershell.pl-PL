---
external help file: Microsoft.Azure.PowerShell.Cmdlets.NotificationHubs.dll-Help.xml
Module Name: Az.NotificationHubs
ms.assetid: 1B2AA717-ECD6-4CC0-AB6D-A199AF21A4A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.notificationhubs/set-aznotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/NotificationHubs/NotificationHubs/help/Set-AzNotificationHubsNamespace.md
ms.openlocfilehash: 9a17dfd649f35da3fa071eb7c6d2752d3a923398
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872500"
---
# Set-AzNotificationHubsNamespace

## STRESZCZENIe
Ustawia wartości właściwości dla obszaru nazw centrum powiadomień.

## POLECENIA

```
Set-AzNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-State] <NamespaceState>] [[-Critical] <Boolean>] [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzNotificationHubsNamespace** ustawia wartości właściwości istniejącej przestrzeni nazw centrum powiadomień.
Przestrzenie nazw są kontenerami logicznymi, które pomagają organizować Centra powiadomień i zarządzać nimi.
Musisz mieć co najmniej jeden obszar nazw centrum powiadomień.
Ponadto wszystkie Centra powiadomień muszą mieć przypisany obszar nazw.
To polecenie cmdlet służy głównie do włączania i wyłączania obszaru nazw.
Gdy obszar nazw jest wyłączony, użytkownicy nie mogą nawiązywać połączeń z żadnymi koncentratorami powiadomień w obszarze nazw ani Administratorzy mogą używać tych koncentratorów do wysyłania powiadomień wypychanych.
Aby ponownie włączyć wyłączony obszar nazw, użyj tego polecenia cmdlet w celu ustawienia właściwości **State** obszaru nazw na wartość aktywny.
Możesz również użyć tego polecenia cmdlet, aby oznaczyć obszar nazw jako krytyczny.
Uniemożliwia to usunięcie przestrzeni nazw.
Aby usunąć krytyczny obszar nazw, należy najpierw usunąć znacznik krytyczne.

## Przykłady

### Przykład 1. wyłączenie obszaru nazw
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Disabled"
```

To polecenie wyłącza obszar nazw o nazwie ContosoPartners, który znajduje się na zachodnim centrum danych w Stanach Zjednoczonych i jest przypisany do grupy zasobów ContosoNotificationsGroup.

### Przykład 2: Włączanie obszaru nazw
```
PS C:\>Set-AzNotificationHubsNamespace -Namespace "ContosoPartners" -Location "West US" -ResourceGroup "ContosoNotificationsGroup" -State "Active"
```

To polecenie umożliwia włączenie obszaru nazw o nazwie ContosoPartners, który znajduje się w zachodnim centrum danych w Stanach Zjednoczonych i przypisany do grupy zasobów ContosoNotificationsGroup.

## PARAMETRÓW

### — Krytyczne
Wskazuje, czy obszar nazw jest krytycznym obszarem nazw.
Nie można usuwać krytycznych obszarów nazw.
Aby usunąć krytyczny obszar nazw, należy ustawić wartość FAŁSZ dla tej właściwości w celu oznaczenia obszaru nazw jako niekrytycznego.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -Force
Nie pytaj o potwierdzenie.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Lokalizacja
Określa nazwę wyświetlaną centrum danych, w którym znajduje się obszar nazw.
Ten parametr można ustawić na dowolną prawidłową lokalizację platformy Azure, co zapewnia optymalną wydajność, dlatego należy korzystać z centrum danych w pobliżu większości użytkowników.
Aby uzyskać aktualną listę lokalizacji na platformie Azure, uruchom następujące polecenie: `Get-AzLocation | Select-Object DisplayName`

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Namespace
Określa obszar nazw, który jest modyfikowany przez to polecenie cmdlet.
Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceName
Określa grupę zasobów, do której przypisano obszar nazw.
Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób umożliwiający łatwe zarządzanie zapasami i administrowanie systemem Azure.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkuTier
Warstwa SKU obszaru nazw

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -State
Określa bieżący stan obszaru nazw.
Dopuszczalne wartości tego parametru to: aktywny i wyłączony.

```yaml
Type: Microsoft.Azure.Commands.NotificationHubs.Models.NamespaceState
Parameter Sets: (All)
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Tag
Określa pary nazwa-wartość, których można użyć do kategoryzowania i organizowania elementów platformy Azure.
Funkcja Tagi podobna do słów kluczowych i działa w ramach wdrożenia.
Jeśli na przykład wyszukiwane są wszystkie elementy z działem znaczników: funkcja wyszukiwania zwróci wszystkie elementy platformy Azure, które mają ten tag, niezależnie od tego, jakie elementy są takie jak typ elementu, lokalizacja lub Grupa zasobów.
Pojedynczy znacznik składa się z dwóch części: *nazwy* i (opcjonalnie) *wartości*.
Na przykład w dziale:, nazwa znacznika to dział, a jego wartość to znacznik.
Aby dodać znacznik, użyj składni tabeli skrótów podobnej do tego, co spowoduje utworzenie znacznika CalendarYear: 2016:-Tagi @ {Name = "CalendarYear"; Value = "2016"} aby dodać wiele tagów w tym samym poleceniu, oddziel poszczególne Tagi za pomocą przecinków:-tag @ {Name = "CalendarYear"; Value = "2016"}, @ {Name = "FiscalYear"; Wartość = "2017"}

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. NotificationHubs. models. NamespaceState

### System. Boolean

### System. Collections. Hashtable

## WYSYŁA

### Microsoft. Azure. Commands. NotificationHubs. models. NamespaceAttributes

## INFORMACYJN

## LINKI POKREWNE

[Get-AzNotificationHubsNamespace](./Get-AzNotificationHubsNamespace.md)

[Nowe — AzNotificationHubsNamespace](./New-AzNotificationHubsNamespace.md)

[Remove-AzNotificationHubsNamespace](./Remove-AzNotificationHubsNamespace.md)


