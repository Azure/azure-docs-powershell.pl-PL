---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7C9470E5-21D2-4AF5-9F11-F66F94B133C0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 23f4511f8e0439c1581cc388843a37266092f4d0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055420"
---
# Remove-AzureVMImage

## STRESZCZENIe
Usuwa obraz systemu operacyjnego z repozytorium obrazów.

## POLECENIA

```
Remove-AzureVMImage [-ImageName] <String> [-DeleteVHD] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureVMImage** usuwa obraz systemu operacyjnego z repozytorium obrazów.
Domyślnie to polecenie cmdlet nie usuwa skojarzonego obiektu BLOB fizycznego obrazu z konta magazynu.
Aby usunąć skojarzony wirtualny dysk twardy (VHD), użyj parametru **DeleteVHD** .

## Przykłady

### Przykład 1. Usuwanie obrazu z repozytorium obrazów
```
PS C:\> Remove-AzureVMImage -ImageName "Image001"
```

To polecenie usuwa obraz o nazwie Image001 z repozytorium obrazów.

### Przykład 2: Usuwanie obrazu z repozytorium obrazów, a także wirtualnego dysku twardego
```
PS C:\> Remove-AzureVMImage -ImageName " Image001" -DeleteVHD
```

To polecenie powoduje usunięcie obrazu o nazwie Image001 z repozytorium obrazów, a także usunięcie fizycznego obrazu VHD z konta magazynu.

### Przykład 3: Ustawianie kontekstu subskrypcji, a następnie Usuwanie wszystkich obrazów
```
PS C:\> $SubsId = &amp;lt;MySubscriptionID&amp;gt;
PS C:\> $Cert = Get-AzureCertificate cert:\LocalMachine\MY\&amp;lt;CertificateThumbprint&amp;gt;
PS C:\> Get-AzureVMImage `
| Where-Object {$_.Label -match "Beta" }`
| Foreach-Object {Remove-AzureVMImage -ImageName $_.name }
```

To polecenie ustawia kontekst abonamentu, a następnie usuwa wszystkie obrazy z repozytorium obrazów, którego etykieta zawiera nazwę beta.

## PARAMETRÓW

### -DeleteVHD
Wskazuje, że to polecenie cmdlet usuwa obiekt BLOB obrazu fizycznego dysku VHD z konta magazynu.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ImageName
Określa obraz systemu operacyjnego lub maszyny wirtualnej do usunięcia z repozytorium obrazów.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Dodaj-AzureVMImage](./Add-AzureVMImage.md)

[Get-AzureVMImage](./Get-AzureVMImage.md)

[Zapisz — AzureVMImage](./Save-AzureVMImage.md)

[Update-AzureVMImage](./Update-AzureVMImage.md)


