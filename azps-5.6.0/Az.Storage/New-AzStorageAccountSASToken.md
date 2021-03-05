---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BCCBB05B-A5D7-4796-BE55-6BE5E18E07FC
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstorageaccountsastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageAccountSASToken.md
ms.openlocfilehash: 6d399c7ed7c074cd5adaf0579097c0706f46192d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002609"
---
# New-AzStorageAccountSASToken

## SYNOPSIS
Tworzy token SAS na poziomie konta.

## SKŁADNIA

```
New-AzStorageAccountSASToken -Service <SharedAccessAccountServices>
 -ResourceType <SharedAccessAccountResourceTypes> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **New-AzStorageSASToken** tworzy token SAS (Shared Access Signature) na poziomie konta dla konta usługi Azure Storage.
Tokenu SAS można użyć do delegowania uprawnień do wielu usług lub do delegowania uprawnień do usług, które nie są dostępne za pomocą tokenu SAS na poziomie obiektu.

## PRZYKŁADY

### Przykład 1. Tworzenie tokenu SAS na poziomie konta z pełnymi uprawnieniami
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup"
```

To polecenie tworzy token SAS na poziomie konta z pełnymi uprawnieniami.

### Przykład 2. Tworzenie tokenu SAS na poziomie konta dla zakresu adresów IP
```
PS C:\> New-AzStorageAccountSASToken -Service Blob,File,Table,Queue -ResourceType Service,Container,Object -Permission "racwdlup" -Protocol HttpsOnly -IPAddressOrRange 168.1.5.60-168.1.5.70
```

To polecenie tworzy token SAS na poziomie konta dla żądań HTTPS z określonego zakresu adresów IP.

## PARAMETERS

### — kontekst
Określa kontekst magazynu platformy Azure.
Aby uzyskać obiekt **AzureStorageContext,** możesz użyć New-AzStorageContext cmdlet.

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
Określa uprawnienia dla konta magazynu.
Uprawnienia są prawidłowe tylko wtedy, gdy są zgodne z określonym typem zasobu.
Należy pamiętać, że jest to ciąg, taki jak `rwd` (w przypadku odczytu, zapisu i usunięcia).
Aby uzyskać więcej informacji na temat akceptowalnych wartości uprawnień, zobacz Tworzenie sygnatury SAS konta http://go.microsoft.com/fwlink/?LinkId=799514

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

### — Protokół
Określa protokół dozwolony dla żądania dokonanego za pomocą sygnatury SAS konta.
Dopuszczalne wartości dla tego parametru to:
- HttpsOnly
- HttpsOrHttp Wartość domyślna to httpsorhttp.

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
Dopuszczalne wartości dla tego parametru to:
- Brak
- Usługa
- Kontener
- Obiekt

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

### — Usługa
Określa usługę.
Dopuszczalne wartości dla tego parametru to:
- Brak
- Obiekt blob
- Plik
- Kolejka
- Tabela

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

### — StartTime
Określa czas (jako obiekt **DateTime),** w którym sygnatura SAS jest prawidłowa.
Aby uzyskać obiekt **DateTime,** użyj Get-Date cmdlet.

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

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## DANE WYJŚCIOWE

### System.String

## NOTATKI

## LINKI POKREWNE

[New-AzstorageBlobSASToken](./New-AzStorageBlobSASToken.md)

[New-AzstorageContainerSASToken](./New-AzStorageContainerSASToken.md)

[New-azstorageFilesasToken](./New-AzStorageFileSASToken.md)

[New-AzStorageQueueSASToken](./New-AzStorageQueueSASToken.md)

[New-AzstorageSharesasToken](./New-AzStorageShareSASToken.md)

[New-azstorageTableSASToken](./New-AzStorageTableSASToken.md)


