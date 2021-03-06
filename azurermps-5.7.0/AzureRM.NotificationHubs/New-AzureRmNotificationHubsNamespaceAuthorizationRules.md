---
external help file: Microsoft.Azure.Commands.NotificationHubs.dll-Help.xml
Module Name: AzureRM.NotificationHubs
ms.assetid: 3F59F7E8-CD32-40CB-9DE0-3FB044439DD0
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.notificationhubs/new-azurermnotificationhubsnamespaceauthorizationrules
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/NotificationHubs/Commands.NotificationHubs/help/New-AzureRmNotificationHubsNamespaceAuthorizationRules.md
ms.openlocfilehash: 2530d4b0075856b6a172bdcf104474d320f657bf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550608"
---
# New-AzureRmNotificationHubsNamespaceAuthorizationRules

## STRESZCZENIe
Tworzy regułę autoryzacji i przypisuje tę regułę do obszaru nazw centrum powiadomień.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### InputFileParameterSet
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-InputFile] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### SASRuleParameterSet
```
New-AzureRmNotificationHubsNamespaceAuthorizationRules [-ResourceGroup] <String> [-Namespace] <String>
 [-SASRule] <SharedAccessAuthorizationRuleAttributes> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmNotificationHubsNamespaceAuthorizationRules** umożliwia utworzenie reguły autoryzacji współużytkowanego podpisu dostępu (SAS) i przypisanie jej do obszaru nazw centrum powiadomień.
Reguły autoryzacji zarządzają prawami użytkownika w obszarze nazw i z koncentratorami powiadomień zawartymi w tej przestrzeni nazw.

To polecenie cmdlet oferuje dwa sposoby tworzenia nowej reguły autoryzacji i przypisywania jej do obszaru nazw.
Możesz utworzyć wystąpienie obiektu **SharedAccessAuthorizationRuleAttributes** , a następnie skonfigurować ten obiekt z wartościami właściwości, które ma mieć Nowa reguła.
Można to zrobić za pomocą platformy .NET Framework.
Następnie można skopiować te wartości właściwości do nowej reguły za pomocą parametru *SASRule* .

Możesz również utworzyć plik JSON (notacja JavaScript) zawierający odpowiednie wartości konfiguracji, a następnie zastosować te wartości za pomocą parametru *plik_wejściowy* .
Plik JSON jest plikiem tekstowym używającym składni podobnej do następującej:

{  
    "Nazwa": "ContosoAuthorizationRule",  
    "Primaryke": "WE4qH0398AyXjlekt56gg1gMR3NHoMs29KkUnnpUk01Y =";  
    "Prawa": \[  
        "Odsłuchiwanie",  
        Przysła  
    \]  
}

W przypadku użycia w połączeniu z poleceniem cmdlet **New-AzureRmNotificationHubsNamespaceAuthorizationRules** Poprzednia przykładu JSON tworzy regułę autoryzacji o nazwie ContosoAuthorizationRule, która umożliwia użytkownikom odsłuchiwanie i wysyłanie praw do obszaru nazw.
Składnik *PrimaryKey* używany do uwierzytelniania może być generowany losowo za pomocą następującego polecenia programu Windows PowerShell:

\[Convert \] :: ToBase64String ((1.. 32 |% { \[ byte/] (Get-losowo-minimum 0-Maksymalna 255)})

## Przykłady

### Przykład 1: Tworzenie reguły autoryzacji i przypisywanie jej do obszaru nazw
```
PS C:\>New-AzureRmNotificationHubAuthorizationRules -Namespace "ContosoNamespace" -ResourceGroup "ContosoNotificationsGroup" -InputFile "C:\Configuration\NamespaceAuthorizationRules.json"
```

To polecenie powoduje utworzenie reguły autoryzacji i przypisanie tej reguły do obszaru nazw ContosoNamespace.
Podczas tworzenia tej reguły należy określić odpowiedni obszar nazw i grupę zasobów, do których jest przypisany obszar nazw.
Jednak nie musisz podawać żadnych informacji na temat samej reguły: informacje o regułach zostaną pobrane z pliku wejściowego C:\Configuration\NamespaceAuthorizationRules.jsw dniu.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

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

### -Plik_wejściowy
Określa ścieżkę do pliku JSON zawierającego informacje o konfiguracji dotyczące nowej reguły autoryzacji.

```yaml
Type: String
Parameter Sets: InputFileParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Namespace
Określa obszar nazw, do którego mają zostać przypisane reguły autoryzacji.

Obszary nazw umożliwiają grupowanie i kategoryzowanie koncentratorów powiadomień.
Nowe reguły muszą być przypisane do istniejącego obszaru nazw.
Polecenie cmdlet **New-AzureRmNotificationHubsNamespaceAuthorizationRules** nie może utworzyć nowego obszaru nazw.

```yaml
Type: String
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

Musisz użyć istniejącej grupy zasobów.
To polecenie cmdlet nie może utworzyć nowej grupy zasobów.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SASRule
Określa obiekt **SharedAccessAuthorizationRuleAttributes** zawierający informacje o konfiguracji dla nowych reguł.

```yaml
Type: SharedAccessAuthorizationRuleAttributes
Parameter Sets: SASRuleParameterSet
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

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

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. NotificationHubs. models. SharedAccessAuthorizationRuleAttributes

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmNotificationHubAuthorizationRules](./Get-AzureRmNotificationHubAuthorizationRules.md)

[Remove-AzureRmNotificationHubAuthorizationRules](./Remove-AzureRmNotificationHubAuthorizationRules.md)

[Set-AzureRmNotificationHubAuthorizationRules](./Set-AzureRmNotificationHubAuthorizationRules.md)


