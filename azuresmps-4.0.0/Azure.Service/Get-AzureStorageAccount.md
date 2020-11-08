---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7D7D1FAE-5360-428B-AAE9-9D1109A7B67F
online version: ''
schema: 2.0.0
ms.openlocfilehash: faccd241929beca1f2423fa9c23f35793233205b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054515"
---
# Get-AzureStorageAccount

## STRESZCZENIe
Pobiera konta magazynu dla bieżącej subskrypcji platformy Azure.

## POLECENIA

```
Get-AzureStorageAccount [[-StorageAccountName] <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureStorageAccount** zwraca obiekt zawierający informacje o kontach magazynu dla bieżącej subskrypcji.
Jeśli parametr *StorageAccountName* jest określony, zwracane są tylko informacje dotyczące określonego konta magazynu.

## Przykłady

### Przykład 1. zwraca wszystkie konta magazynu
```
PS C:\> Get-AzureStorageAccount
```

To polecenie zwraca obiekt z wszystkimi kontami magazynu skojarzonymi z bieżącą subskrypcją.

### Przykład 2: informacje o koncie zwrotnym dla określonego konta
```
PS C:\> Get-AzureStorageAccount -StorageAccountName "ContosoStore01"
```

To polecenie zwraca obiekt zawierający tylko informacje o koncie ContosoStore01.

### Przykład 3: wyświetlanie tabeli kont magazynu
```
PS C:\> Get-AzureStorageAccount | Format-Table -AutoSize -Property @{Label="Name";Expression={$_.StorageAccountName}},"Label","Location"
```

To polecenie zwraca obiekt z wszystkimi kontami magazynu skojarzonymi z bieżącą subskrypcją i wyświetla go jako tabelę zawierającą nazwę konta, etykietę konta i lokalizację magazynu.

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

### -StorageAccountName
Określa nazwę konta magazynu.
Jeśli ta funkcja jest określona, to polecenie cmdlet zwróci tylko określony obiekt konta magazynu.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
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
* Wpisz `help node-dev` , aby uzyskać pomoc dotyczącą Node.js poleceń cmdlet związanych z programowaniem. Wpisz `help php-dev` , aby uzyskać pomoc dotyczącą poleceń cmdlet związanych z projektowaniem w programie php.

## LINKI POKREWNE

[Nowe — AzureStorageAccount](./New-AzureStorageAccount.md)

[Set-AzureStorageAccount](./Set-AzureStorageAccount.md)


