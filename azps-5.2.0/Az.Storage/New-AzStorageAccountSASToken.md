---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 3c79266c6f6e9b5200e2224f463ac12fe409bf0c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324856"
---
# New-AzStorageAccountSASToken

## STRESZCZENIe
Umożliwia utworzenie tokenu SAS na poziomie konta.

## POLECENIA

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzStorageSASToken** umożliwia utworzenie tokenu SAS (Shared Access Signature) na poziomie konta dla konta usługi Azure Storage.
Tokena SAS można używać do delegowania uprawnień dla wielu usług lub do delegowania uprawnień dla usług niedostępnych z tokenem SAS na poziomie obiektu.

## Przykłady

### Przykład 1. Tworzenie tokenu SAS na poziomie konta z pełnymi uprawnieniami
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

To polecenie tworzy token SAS na poziomie konta z pełnymi uprawnieniami.

### Przykład 2: Tworzenie tokenu SAS na poziomie konta dla zakresu adresów IP
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

To polecenie tworzy token SAS na poziomie konta dla żądań dotyczących tylko HTTPS z określonego zakresu adresów IP.

## PARAMETRÓW

### -Context
Określa kontekst usługi Azure Storage.
Możesz użyć polecenia cmdlet New-AzStorageContext, aby uzyskać obiekt **AzureStorageContext** .

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

### -ExpiryTime
Określa czas, po upływie którego podpis udostępniony jest nieprawidłowy.

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

### -IPAddressOrRange
Określa adres IP lub zakres adresów IP, od których należy akceptować żądania, takie jak 168.1.5.65 lub 168.1.5.60-168.1.5.70.
Zakresem jest włącznie.

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

### -Uprawnienie
Określa uprawnienia do konta magazynu.
Uprawnienia są ważne tylko wtedy, gdy pasują do określonego typu zasobu.
Ważne jest, aby zwrócić uwagę, że jest to ciąg, taki jak `rwd` (na przykład odczyt, zapis i usuwanie).
Aby uzyskać więcej informacji na temat dopuszczalnych wartości uprawnień, zobacz konstruowanie skojarzeń zabezpieczeń konta http://go.microsoft.com/fwlink/?LinkId=799514

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

### -Protocol (protokół)
Umożliwia określenie protokołu dozwolonego dla żądania wykonywanego za pomocą skojarzeń zabezpieczeń konta.
Dopuszczalne wartości tego parametru to:
- HttpsOnly
- HttpsOrHttp wartość domyślna to HttpsOrHttp.

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

### -ResourceType
Określa typy zasobów dostępne w tokenie SAS.
Dopuszczalne wartości tego parametru to:
- Znaleziono
- Służby
- Opakowaniu
- Stream

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountResourceTypes
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, Container, Object

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Service
Określa usługę.
Dopuszczalne wartości tego parametru to:
- Znaleziono
- Obiektów BLOB
- Plik
- Wykonany
- Tworząc

```yaml
Type: Microsoft.Azure.Storage.SharedAccessAccountServices
Parameter Sets: (All)
Aliases:
Accepted values: None, Blob, File, Queue, Table

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -StartTime
Określa czas (w postaci obiektu **DateTime** ), po upływie którego te skojarzenia będą obowiązywać.
Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.

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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext

## WYSYŁA

### System. String

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzStorageBlobSASToken](./New-AzStorageBlobSASToken.md)

[Nowe — AzStorageContainerSASToken](./New-AzStorageContainerSASToken.md)

[Nowe — AzStorageFileSASToken](./New-AzStorageFileSASToken.md)

[Nowe — AzStorageQueueSASToken](./New-AzStorageQueueSASToken.md)

[Nowe — AzStorageShareSASToken](./New-AzStorageShareSASToken.md)

[Nowe — AzStorageTableSASToken](./New-AzStorageTableSASToken.md)


