---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D6D54096-670D-43E4-93EB-24C8FBA199A4
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2db1d7a6bc87c694cf06ea1fef0a886c61734a75
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055131"
---
# Remove-AzureDeployment

## STRESZCZENIe
Umożliwia usunięcie wdrożenia usługi w chmurze.

## POLECENIA

```
Remove-AzureDeployment [-ServiceName] <String> [-Slot] <String> [-DeleteVHD] [-Force]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureDeployment** umożliwia usunięcie wdrożenia usługi w chmurze platformy Azure.
Aby usunąć wdrożenie, najpierw należy je wstrzymać.

## Przykłady

### Przykład 1: usunięcie wdrożenia
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService"
```

To polecenie umożliwia usunięcie wdrożenia usługi platformy Azure o nazwie ContosoService.
Ponieważ to polecenie nie określa gniazda, usuwa usługę ze środowiska produkcyjnego.

### Przykład 2: usuwanie wdrożenia i wirtualnych dysków twardych
```
PS C:\> Remove-AzureDeployment -ServiceName "ContosoService" -DeleteVHD
```

To polecenie usuwa wdrożenie usługi o nazwie ContosoService ze środowiska produkcyjnego.
Polecenie powoduje również usunięcie podstawowych wirtualnych dysków twardych.

## PARAMETRÓW

### -DeleteVHD
Określa, że to polecenie cmdlet spowoduje usunięcie wdrożenia i wirtualnych dysków twardych (VHD) z magazynu obiektów BLOB.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Force
Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationAction
Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.

Dopuszczalne wartości tego parametru to:

- Kontynuacj
- Ignorować
- Inquire
- SilentlyContinue
- Przestaw
- Wykonywanie

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InformationVariable
Określa zmienną informacyjną.

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.
Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceName
Określa nazwę usługi, dla której to polecenie cmdlet spowoduje usunięcie wdrożenia.

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

### -Slot
Określa środowisko wdrażania, w którym to polecenie cmdlet powoduje usunięcie wdrożenia.
Prawidłowe wartości to: przemieszczanie i produkcja.
Wartością domyślną jest produkcja.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### ManagementOperationContext

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureDeployment](./Get-AzureDeployment.md)

[Get-AzureDeploymentEvent](./Get-AzureDeploymentEvent.md)

[Przenieś — AzureDeployment](./Move-AzureDeployment.md)

[Nowe — AzureDeployment](./New-AzureDeployment.md)

[Set-AzureDeployment](./Set-AzureDeployment.md)


