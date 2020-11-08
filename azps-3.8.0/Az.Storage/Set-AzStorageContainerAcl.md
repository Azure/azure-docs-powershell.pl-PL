---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BDEEF1EA-A785-4E17-9887-C2000BDFCF57
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstoragecontaineracl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageContainerAcl.md
ms.openlocfilehash: a23df1d7f6af188557c8e949f116e3dd12351c49
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94050814"
---
# Set-AzStorageContainerAcl

## STRESZCZENIe
Ustawia uprawnienie dostępu publicznego do kontenera magazynu.

## POLECENIA

```
Set-AzStorageContainerAcl [-Name] <String> [-Permission] <BlobContainerPublicAccessType> [-PassThru]
 [-Context <IStorageContext>] [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzStorageContainerAcl** ustawia uprawnienie dostępu publicznego do określonego kontenera magazynu na platformie Azure.

## Przykłady

### Przykład 1: ustawianie listy ACL kontenera magazynu platformy Azure według nazwy
```
PS C:\>Set-AzStorageContainerAcl -Container "Container01" -Permission Off -PassThru
```

To polecenie tworzy kontener bez dostępu publicznego.

### Przykład 2: ustawianie listy ACL kontenera magazynu platformy Azure przy użyciu potoku
```
PS C:\>Get-AzStorageContainer container* | Set-AzStorageContainerAcl -Permission Blob -PassThru
```

To polecenie pobiera wszystkie kontenery magazynu, których nazwa zaczyna się od kontenera, a następnie przekazuje wynik w potoku, aby ustawić dla niego uprawnienie dostępu do obiektu BLOB.

## PARAMETRÓW

### -ClientTimeoutPerRequest
Określa interwał czasu po stronie klienta (w sekundach) dla jednego żądania usługi.
Jeśli poprzednie połączenie nie powiodło się w określonym interwale, to polecenie cmdlet ponawia próbę wykonania żądania.
Jeśli to polecenie cmdlet nie odbierze skutecznej odpowiedzi przed upływem interwału, to polecenie cmdlet zwróci błąd.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ClientTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ConcurrentTaskCount
Określa maksymalną liczbę współbieżnych połączeń sieciowych.
Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia lokalnego użycia procesora i przepustowości przez określenie maksymalnej liczby jednoczesnych połączeń sieciowych.
Określona wartość jest liczbą bezwzględną i nie jest mnożona przez liczność rdzeni.
Ten parametr może pomóc w zmniejszeniu problemów z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.
Wartość domyślna to 10.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Context
Określa kontekst usługi Azure Storage.
Możesz ją utworzyć przy użyciu polecenia cmdlet New-AzStorageContext.

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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

### -Name (nazwa)
Określa nazwę kontenera.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Container

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -PassThru
Zwraca obiekt reprezentujący element, z którym pracujesz.
Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.

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

### -Uprawnienie
Określa poziom dostępu publicznego do tego kontenera.
Domyślnie kontener i wszystkie obiekty blob są dostępne tylko dla właściciela konta magazynu.
Aby udzielić anonimowym użytkownikom uprawnień do odczytu kontenera i jego obiektów blob, możesz ustawić uprawnienia kontenera, aby umożliwić dostęp publiczny.
Anonimowi użytkownicy mogą czytać obiekty blob w publicznie dostępnym kontenerze bez uwierzytelniania żądania.
Dopuszczalne wartości tego parametru to:--kontener.
Zapewnia pełny dostęp do odczytu kontenera i jego obiektów BLOB.
Klienci mogą wyliczyć obiekty blob w kontenerze przez anonimowe żądanie, ale nie można wyliczyć kontenerów na koncie magazynu. --BLOB.
Zapewnia dostęp do odczytu do danych obiektu BLOB w kontenerze za pośrednictwem żądania anonimowego, ale nie umożliwia dostępu do danych kontenera.
Klienci nie mogą wyliczyć obiektów BLOB w kontenerze przy użyciu żądania anonimowego. --Wył.
Ogranicza dostęp tylko do właściciela konta magazynu.

```yaml
Type: Microsoft.Azure.Storage.Blob.BlobContainerPublicAccessType
Parameter Sets: (All)
Aliases: PublicAccess
Accepted values: Off, Container, Blob, Unknown

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Określa interwał limitu czasu po stronie usługi (w sekundach) dla żądania.
Jeśli upłynie określony interwał, zanim usługa przetworzy żądanie, usługa magazynu zwraca błąd.
Limit czasu po stronie serwera dla każdego żądania.

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: ServerTimeoutPerRequestInSeconds

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. Common. Storage. ResourceModel. AzureStorageContainer

## INFORMACYJN

## LINKI POKREWNE

[Get-AzStorageContainer](./Get-AzStorageContainer.md)

[Nowe — AzStorageContainer](./New-AzStorageContainer.md)

[Remove-AzStorageContainer](./Remove-AzStorageContainer.md)


