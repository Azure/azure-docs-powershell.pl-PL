---
external help file: Microsoft.WindowsAzure.Commands.RemoteApp.dll-Help.xml
ms.assetid: 58DABEB0-D3B6-478B-9B83-80E4C67A7792
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1d4717e795bcfea9728cbabb1b7c788713907aaa
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055536"
---
# Get-AzureRemoteAppVNet

## STRESZCZENIe
Pobiera informacje o wirtualnych sieciach Azure RemoteApp na platformie Azure.

## POLECENIA

```
Get-AzureRemoteAppVNet [[-VNetName] <String>] [-IncludeSharedKey] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRemoteAppVNet** pobiera informacje o wirtualnych sieciach funkcji Azure RemoteApp na platformie Microsoft Azure.
To polecenie cmdlet zwraca obiekt zawierający informacje o określonej sieci wirtualnej.
Jeśli nie określono sieci wirtualnej, to polecenie cmdlet zwraca informacje o wszystkich sieciach wirtualnych w bieżącej subskrypcji.

## Przykłady

### Przykład 1: pobieranie informacji o sieci wirtualnej
```
PS C:\> Get-AzureRemoteAppVNet -VNetName "ContosoVNet"
```

To polecenie pobiera informacje o sieci wirtualnej o nazwie ContosoVNet.

## PARAMETRÓW

### -IncludeSharedKey
Wskazuje, że w tym poleceniu cmdlet jest uwzględniana wartość klucza współdzielonego w informacjach pobieranych na temat sieci wirtualnej.

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

### -VNetName
Określa nazwę sieci wirtualnej usługi Azure RemoteApp.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: True
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Set-AzureRemoteAppVNet](./Set-AzureRemoteAppVNet.md)


