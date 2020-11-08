---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B935B615-1200-4A83-95AF-4F17785793B4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a331f3e0ff2797b84c241e64872e3af0841cb106
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055210"
---
# Move-AzureDeployment

## STRESZCZENIe
Zamienia wdrożenia między produkcją a przemieszczaniem.

## POLECENIA

```
Move-AzureDeployment [-ServiceName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Move-AzureDeployment** umożliwia zamianę wirtualnych adresów IP wdrożeń w środowiskach produkcyjnych i przejściowych.
To polecenie cmdlet zamienia wdrożenie, które jest obecnie uruchamiane w środowisku roboczym w środowisku produkcyjnym, oraz wdrożenie uruchomione w środowisku produkcyjnym w środowisku roboczym.
W przypadku wdrożenia w środowisku przemieszczania i bez wdrożenia w środowisku produkcyjnym polecenie cmdlet przeniesie wdrożenie do produkcji.
Jeśli wdrożenie w środowisku produkcyjnym jest niezgodne z wdrożeniem w środowisku roboczym, wykonanie polecenia cmdlet nie powiodło się.

## Przykłady

### Przykład 1: wymiana wdrożeń dla usługi
```
PS C:\> Move-AzureDeployment -ServiceName "ContosoService"
```

To polecenie zamienia wdrożenia usługi o nazwie ContosoService między środowiska produkcyjne i robocze.

## PARAMETRÓW

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
Określa nazwę usługi, dla której to polecenie cmdlet zamienia wdrożenia produkcyjne i przemieszczające.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

### ManagementOperationContext

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureDeployment](./Get-AzureDeployment.md)

[Get-AzureDeploymentEvent](./Get-AzureDeploymentEvent.md)

[Nowe — AzureDeployment](./New-AzureDeployment.md)

[Remove-AzureDeployment](./Remove-AzureDeployment.md)

[Set-AzureDeployment](./Set-AzureDeployment.md)


