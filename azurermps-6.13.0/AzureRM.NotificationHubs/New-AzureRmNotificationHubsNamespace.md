---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3BA94976-DE88-4F07-9C06-41FEEDE1B829
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespace.md
ms.openlocfilehash: d4bba9d54dac21a8eb19a4b161bb2fdef29d4bb7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553460"
---
# New-AzureRmNotificationHubsNamespace

## STRESZCZENIe
Tworzy obszar nazw centrum powiadomień.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
New-AzureRmNotificationHubsNamespace [-ResourceGroup] <String> [-Namespace] <String> [-Location] <String>
 [[-Tag] <Hashtable>] [[-SkuTier] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmNotificationHubsNamespace** tworzy obszar nazw centrum powiadomień.
Przestrzenie nazw są kontenerami logicznymi, które pomagają organizować Centra powiadomień i zarządzać nimi.
Musisz mieć co najmniej jeden obszar nazw centrum powiadomień.
Jeden obszar nazw może być jednym z wielu koncentratorów.
Możesz mieć wiele obszarów nazw, aby zorganizować koncentratory lub przekazać konkretne osoby do zarządzania wybranym podzbiorem koncentratorów.
Aby utworzyć obszar nazw, upewnij się, że jest określana unikatowa nazwa obszaru nazw; Określ centrum danych, w którym znajduje się obszar nazw; i określ grupę zasobów, do której zostanie przypisany obszar nazw.
Po utworzeniu obszaru nazw możesz użyć polecenia cmdlet New-AzureRmNotificationHubsNamespaceAuthorizationRules, aby przypisać reguły autoryzacji do tego obszaru nazw.
Reguły autoryzacji są używane do zarządzania uprawnieniami do obszaru nazw.

## Przykłady

### Przykład 1. Tworzenie centrum powiadomień
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners"
```

To polecenie tworzy centrum powiadomień o nazwie ContosoPartners.
Obszar nazw znajdzie się na zachodnim centrum danych w Stanach Zjednoczonych i zostanie przypisany do grupy zasobów ContosoNotificationsGroup.

### Przykład 2: tworzenie centrum powiadomień ze znacznikami
```
PS C:\>New-AzureRmNotificationHubsNamespace -ResourceGroup "ContosoNotificationsGroup" -Location "West US" -Namespace "ContosoPartners" -Tags @{Name="Audience";Value="PartnerOrganizations"}
```

To polecenie tworzy centrum powiadomień o nazwie ContosoPartners.
Obszar nazw znajdzie się na zachodnim centrum danych w Stanach Zjednoczonych i zostanie przypisany do grupy zasobów ContosoNotificationsGroup.
Ponadto to polecenie tworzy znacznik o nazwie odbiorcy i wartości PartnerOrganizations oraz jest przypisany do obszaru nazw.
Zapewnia to, że obszar nazw będzie wyświetlany w dowolnym momencie filtrowania elementów, dla których znacznik odbiorców jest ustawiony na PartnerOrganizations.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### — Lokalizacja
Określa nazwę wyświetlaną centrum danych, które będzie hostem obszaru nazw.
Ten parametr można ustawić na dowolną prawidłową lokalizację, co zapewnia optymalną wydajność, które mogą być używane w pobliżu większości użytkowników.

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
Określa nazwę nowego obszaru nazw.
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
Określa grupę zasobów, do której zostanie przypisany obszar nazw.
Grupy zasobów organizują elementy, takie jak obszary nazw, Centra powiadomień i reguły autoryzacji, w sposób ułatwiający Zarządzanie zapasami i administrację.

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

### -Tag
Określa pary nazwa-wartość, których można użyć do kategoryzowania i organizowania elementów platformy Azure.
Funkcja Tagi podobna do słów kluczowych i działa w ramach wdrożenia.
Jeśli na przykład wyszukiwane są wszystkie elementy z działem znaczników: funkcja wyszukiwania zwróci wszystkie elementy platformy Azure, które mają ten tag, niezależnie od tego, jakie elementy są takie jak typ elementu, lokalizacja lub Grupa zasobów.
Pojedynczy znacznik składa się z dwóch części: *nazwy* i opcjonalnie *wartości*.
Na przykład w dziale: to nazwa znacznika to dział, a jego wartość to znacznik.
Aby dodać znacznik, użyj składni tabeli skrótów podobnej do tego, co spowoduje utworzenie znacznika CalendarYear: 2016:

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
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

### System. Collections. Hashtable

## WYSYŁA

### Microsoft. Azure. Commands. NotificationHubs. models. NamespaceAttributes

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmNotificationHubsNamespace](./Get-AzureRmNotificationHubsNamespace.md)

[Remove-AzureRmNotificationHubsNamespace](./Remove-AzureRmNotificationHubsNamespace.md)

[Set-AzureRmNotificationHubsNamespace](./Set-AzureRmNotificationHubsNamespace.md)


