---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDF42420-3616-4A64-9562-1A896F828728
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragesharesastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareSASToken.md
ms.openlocfilehash: b55ab1d87fa63523b35077243d8b9b4f00ba5d2d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002353"
---
# New-AzStorageShareSASToken

## SYNOPSIS
Wygeneruj token podpisu dostępu udostępnionego dla udziału magazynu platformy Azure.

## SKŁADNIA

### SasPolicy
```
New-AzStorageShareSASToken [-ShareName] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### SasPermission
```
New-AzStorageShareSASToken [-ShareName] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzStorageShareSASToken** generuje token podpisu dostępu udostępnionego dla udziału magazynu platformy Azure.

## PRZYKŁADY

### Przykład 1. Generowanie tokenu podpisu dostępu udostępnionego dla udziału
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Permission "rwdl"
```

To polecenie tworzy token podpisu dostępu udostępnionego dla udziału o nazwie ContosoShare.

### Przykład 2. Generowanie wielu tokenów podpisu dostępu udostępnionego przy użyciu potoku
```
PS C:\>Get-AzStorageShare -Prefix "test" | New-AzStorageShareSASToken -Permission "rwdl"
```

To polecenie pobiera wszystkie udziały magazynu zgodne z testem prefiksu.
Polecenie przekazuje je do bieżącego polecenia cmdlet przy użyciu operatora potoku.
Bieżące polecenie cmdlet tworzy token dostępu udostępnionego dla każdego udziału magazynu, który ma określone uprawnienia.

### Przykład 3. Generowanie tokenu podpisu dostępu udostępnionego, który korzysta z zasad dostępu udostępnionego
```
PS C:\>New-AzStorageShareSASToken -ShareName "ContosoShare" -Policy "ContosoPolicy03"
```

To polecenie tworzy token podpisu dostępu udostępnionego dla udziału magazynu o nazwie ContosoShare, który ma zasady o nazwie ContosoPolicy03.

## PARAMETERS

### — kontekst
Określa kontekst magazynu platformy Azure.
Aby uzyskać kontekst, użyj polecenia cmdlet New-AzStorageContext cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ExpiryTime
Określa czas, w którym podpis dostępu udostępnionego staje się nieprawidłowy.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -FullUri
Wskazuje, że to polecenie cmdlet zwraca pełny adres URI obiektu blob i token podpisu dostępu udostępnionego.

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

### -IPAddressOrRange
Określa adres IP lub zakres adresów IP, z których mają być akceptowane żądania, na przykład 168.1.5.65 lub 168.1.5.60-168.1.5.70.
Zakres jest włącznie.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Uprawnienie
Określa uprawnienia w tokenie do uzyskiwania dostępu do udziału i plików w ramach udziału.
Należy pamiętać, że jest to ciąg, taki jak `rwd` (w przypadku odczytu, zapisu i usunięcia).

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Zasady
Określa przechowywane zasady dostępu dla udziału.

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Protokół
Określa protokół dozwolony dla żądania.
Dopuszczalne wartości dla tego parametru to:
* HttpsOnly
* HttpsOrHttp Wartość domyślna to httpsorhttp.

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.SharedAccessProtocol]
Parameter Sets: (All)
Aliases:
Accepted values: HttpsOnly, HttpsOrHttp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ShareName
Określa nazwę udziału magazynu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### — StartTime
Określa czas, w którym podpis dostępu udostępnionego stanie się prawidłowy.

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## DANE WYJŚCIOWE

### System.String

## NOTATKI
* Słowa kluczowe: common, azure, services, data, storage, blob, queue, table

## LINKI POKREWNE

[Get-AzstorageShare](./Get-AzStorageShare.md)

[New-azstorageFilesasToken](./New-AzStorageFileSASToken.md)
