---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 383402B2-6B7C-41AB-AFF9-36C86156B0A9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragecontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/New-AzStorageContext.md
ms.openlocfilehash: ae22e6923a03864b9371ccdf5379ef9b6bf5189d
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892162"
---
# New-AzStorageContext

## STRESZCZENIe
Tworzy kontekst usługi Azure Storage.

## POLECENIA

### AccountNameAndKey (domyślny)
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### AccountNameAndKeyEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-StorageAccountKey] <String> [-Protocol <String>]
 -Environment <String> [<CommonParameters>]
```

### AnonymousAccount
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] [-Endpoint <String>]
 [<CommonParameters>]
```

### AnonymousAccountEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> [-Anonymous] [-Protocol <String>] -Environment <String>
 [<CommonParameters>]
```

### SasToken
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> [-Protocol <String>]
 [-Endpoint <String>] [<CommonParameters>]
```

### SasTokenWithAzureEnvironment
```
New-AzStorageContext [-StorageAccountName] <String> -SasToken <String> -Environment <String>
 [<CommonParameters>]
```

### Elemencie
```
New-AzStorageContext -ConnectionString <String> [<CommonParameters>]
```

### LocalDevelopment
```
New-AzStorageContext [-Local] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzStorageContext** umożliwia utworzenie kontekstu usługi Azure Storage.

## Przykłady

### Przykład 1. Tworzenie kontekstu przez określenie nazwy i klucza konta magazynu
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
```

To polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza.

### Przykład 2: Tworzenie kontekstu przez określenie parametrów połączenia
```
C:\PS>New-AzStorageContext -ConnectionString "DefaultEndpointsProtocol=https;AccountName=ContosoGeneral;AccountKey=< Storage Key for ContosoGeneral ends with == >;"
```

To polecenie tworzy kontekst na podstawie określonych parametrów połączenia dla konta ContosoGeneral.

### Przykład 3: Tworzenie kontekstu dla konta magazynu anonimowego
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -Anonymous -Protocol "http"
```

To polecenie tworzy kontekst do anonimowego korzystania z konta o nazwie ContosoGeneral.
To polecenie określa HTTP jako protokół połączenia.

### Przykład 4: Tworzenie kontekstu za pomocą lokalnego konta magazynu opracowywania
```
C:\PS>New-AzStorageContext -Local
```

To polecenie tworzy kontekst za pomocą lokalnego konta magazynu dla deweloperów.
Polecenie określa parametr *Local* .

### Przykład 5: uzyskiwanie kontenera dla lokalnego konta magazynu dewelopera
```
C:\PS>New-AzStorageContext -Local | Get-AzStorageContainer
```

To polecenie tworzy kontekst przy użyciu lokalnego konta magazynu dla programistów, a następnie przekazuje nowy kontekst do polecenia cmdlet **Get-AzStorageContainer** przy użyciu operatora potoku.
Polecenie pobiera kontener magazynu platformy Azure dla konta magazynu lokalnego dla deweloperów.

### Przykład 6: uzyskiwanie wielu kontenerów
```
C:\PS>$Context01 = New-AzStorageContext -Local 
PS C:\> $Context02 = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >"
PS C:\> ($Context01, $Context02) | Get-AzStorageContainer
```

Pierwsze polecenie tworzy kontekst przy użyciu lokalnego konta magazynu dla programistów, a następnie przechowuje ten kontekst w zmiennej $Context 01.
Drugie polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza, a następnie zapisuje ten kontekst w zmiennej $Context 02.
Polecenie ostatnie uzyskuje kontenery dla kontekstów przechowywanych w $Context 01 i $Context 02 przy użyciu polecenia **Get-AzStorageContainer**.

### Przykład 7: Tworzenie kontekstu za pomocą punktu końcowego
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Endpoint "contosoaccount.core.windows.net"
```

To polecenie tworzy kontekst usługi Azure Storage o określonym punkcie końcowym magazynu.
Polecenie utworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza.

### Przykład 8: Tworzenie kontekstu za pomocą określonego środowiska
```
C:\PS>New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral ends with == >" -Environment "AzureChinaCloud"
```

To polecenie tworzy kontekst usługi Azure Storage z określonym środowiskiem platformy Azure.
Polecenie utworzy kontekst dla konta o nazwie ContosoGeneral, który używa określonego klucza.

### Przykład 9: Tworzenie kontekstu za pomocą tokenu SAS
```
C:\PS>$SasToken = New-AzStorageContainerSASToken -Name "ContosoMain" -Permission "rad"
PS C:\> $Context = New-AzStorageContext -StorageAccountName "ContosoGeneral" -SasToken $SasToken
PS C:\> $Context | Get-AzStorageBlob -Container "ContosoMain"
```

Pierwsze polecenie generuje token SAS przy użyciu polecenia cmdlet **New-AzStorageContainerSASToken** dla kontenera o nazwie ContosoMain, a następnie zapisuje ten token w zmiennej $SasToken.
Token ten jest przeznaczony dla uprawnień Odczyt, Dodawanie, aktualizowanie i usuwanie.
Drugie polecenie tworzy kontekst dla konta o nazwie ContosoGeneral, w którym jest używany token SAS przechowywany w $SasToken, a następnie przechowuje ten kontekst w zmiennej $Context.
W ostatnim poleceniu są wyświetlane wszystkie obiekty blob skojarzone z kontenerem o nazwie ContosoMain przy użyciu kontekstu przechowywanego w $Context.

## PARAMETRÓW

### -Anonymous
Wskazuje, że to polecenie cmdlet tworzy kontekst usługi Azure Storage do logowania anonimowego.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AnonymousAccount, AnonymousAccountEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConnectionString
Określa parametry połączenia dla kontekstu usługi Azure Storage.

```yaml
Type: System.String
Parameter Sets: ConnectionString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Endpoint
Określa punkt końcowy kontekstu usługi Azure Storage.

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AnonymousAccount, SasToken
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Środowisko
Określa środowisko Azure.
Dopuszczalne wartości tego parametru to: AzureCloud oraz AzureChinaCloud.
Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-AzureEnvironment` .

```yaml
Type: System.String
Parameter Sets: AccountNameAndKeyEnvironment, AnonymousAccountEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SasTokenWithAzureEnvironment
Aliases: Name, EnvironmentName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Local
Wskazuje, że to polecenie cmdlet tworzy kontekst przy użyciu lokalnego konta magazynu dla deweloperów.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: LocalDevelopment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Protocol (protokół)
Protokół transferu (https/http).

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken
Aliases:
Accepted values: Http, Https

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SasToken
Określa token funkcji dostępu współużytkowanego (SAS, Access Signature) dla kontekstu.

```yaml
Type: System.String
Parameter Sets: SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountKey
Określa klucz konta usługi Azure Storage.
To polecenie cmdlet tworzy kontekst dla klucza, który określa ten parametr.

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StorageAccountName
Określa nazwę konta magazynu platformy Azure.
To polecenie cmdlet tworzy kontekst dla konta, które określa ten parametr.

```yaml
Type: System.String
Parameter Sets: AccountNameAndKey, AccountNameAndKeyEnvironment, AnonymousAccount, AnonymousAccountEnvironment, SasToken, SasTokenWithAzureEnvironment
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. Storage. AzureStorageContext

## INFORMACYJN

## LINKI POKREWNE

[Get-AzStorageBlob](./Get-AzStorageBlob.md)

[Nowe — AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)


