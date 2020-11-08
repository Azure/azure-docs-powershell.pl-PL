---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2BDB255A-EFB3-4580-BE95-187008DB208C
online version: ''
schema: 2.0.0
ms.openlocfilehash: c21195f6d3ed938844717789f8a0df16f49fbd85
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054895"
---
# New-AzureDeployment

## STRESZCZENIe
Tworzy wdrożenie z usługi.

## POLECENIA

```
New-AzureDeployment [-ServiceName] <String> [-Package] <String> [-Configuration] <String> [-Slot] <String>
 [[-Label] <String>] [[-Name] <String>] [-DoNotStart] [-TreatWarningsAsError]
 [-ExtensionConfiguration <ExtensionConfigurationInput[]>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureDeployment** tworzy wdrożenie platformy Azure z usługi obejmującej role w sieci Web i role pracowników.
To polecenie cmdlet tworzy wdrożenie na podstawie pliku pakietu (. cspkg) oraz pliku konfiguracji usługi (cscfg).
Określ nazwę, która jest unikatowa w środowisku wdrażania.

Użyj polecenia cmdlet **New-AzureVM** w celu utworzenia wdrożenia opartego na maszynach wirtualnych platformy Azure.

## Przykłady

### Przykład 1: Tworzenie wdrożenia
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -Label "ContosoDeployment"
```

To polecenie tworzy wdrożenie produkcyjne na podstawie pakietu o nazwie ContosoPackage. cspkg i konfiguracji o nazwie ContosoConfiguration. cscfg.
Polecenie Określa etykietę wdrożenia.
Nazwa nie jest określana.
To polecenie cmdlet tworzy identyfikator GUID jako nazwę.

### Przykład 2: Tworzenie wdrożenia na podstawie konfiguracji rozszerzenia
```
PS C:\> New-AzureDeployment -ServiceName "ContosoService" -Slot "Production" -Package "https://contosostorage.blob.core.windows.net/container06/ContosoPackage.cspkg" -Configuration "C:\packages\ContosoConfiguration.cscfg" -ExtensionConfiguration "C:\packages\ContosoExtensionConfig.cscfg"
```

To polecenie tworzy wdrożenie produkcyjne na podstawie pakietu i konfiguracji.
To polecenie określa konfigurację rozszerzenia o nazwie ContosoExtensionConfig. cscfg.
To polecenie cmdlet tworzy identyfikatory GUID jako imię i nazwisko oraz etykietę.

## PARAMETRÓW

### — Konfiguracja
Określa pełną ścieżkę do pliku konfiguracji usługi.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DoNotStart
Określa, że to polecenie cmdlet nie rozpocznie wdrożenia.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExtensionConfiguration
Określa tablicę obiektów konfiguracji rozszerzenia.

```yaml
Type: ExtensionConfigurationInput[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
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

### -Label
Określa nazwę etykiety dla wdrożenia.
Jeśli nie określisz etykiety, to polecenie cmdlet użyje identyfikatora GUID.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę wdrożenia.
Jeśli nie określisz nazwy, to polecenie cmdlet użyje identyfikatora GUID.

```yaml
Type: String
Parameter Sets: (All)
Aliases: DeploymentName

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Package
Określa ścieżkę lub identyfikator URI pliku cspkg w magazynie w ramach tego samego abonamentu lub projektu.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
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
Określa nazwę usługi Azure dla wdrożenia.

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
Określa środowisko, w którym to polecenie cmdlet tworzy wdrożenie.
Prawidłowe wartości to: przemieszczanie i produkcja.
Wartością domyślną jest produkcja.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TreatWarningsAsError
Określa, że komunikaty ostrzegawcze są błędami.
W przypadku określenia tego parametru komunikat ostrzegawczy powoduje niepowodzenie wdrożenia.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureDeployment](./Get-AzureDeployment.md)

[Get-AzureDeploymentEvent](./Get-AzureDeploymentEvent.md)

[Przenieś — AzureDeployment](./Move-AzureDeployment.md)

[Nowe — AzureVM](./New-AzureVM.md)

[Remove-AzureDeployment](./Remove-AzureDeployment.md)

[Set-AzureDeployment](./Set-AzureDeployment.md)


