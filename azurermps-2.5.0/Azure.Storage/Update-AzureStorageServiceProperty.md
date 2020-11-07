---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/update-azurestorageserviceproperty
schema: 2.0.0
ms.openlocfilehash: 2f0c59acba56fb80a12df0c5df6c8168ebc91000
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899149"
---
# Update-AzureStorageServiceProperty

## STRESZCZENIe
Modyfikuje właściwości usługi Azure Storage.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Update-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-DefaultServiceVersion <String>]
 [-PassThru] [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Update-AzureStorageServiceProperty** modyfikuje właściwości usługi Azure Storage.

## Przykłady

### Przykład 1: Ustawianie DefaultServiceVersion usługi BLOB na 2017-04-17
```
C:\PS>Update-AzureStorageServiceProperty -ServiceType Blob -DefaultServiceVersion 2017-04-17
```

To polecenie ustawia DefaultServiceVersion usługi BLOB równą 2017-04-17

## PARAMETRÓW

### -Context
Określa kontekst usługi Azure Storage.
Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzureStorageContext.

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
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultServiceVersion
DefaultServiceVersion wskazuje domyślną wersję, która ma być używana dla żądań w usłudze BLOB, jeśli nie została określona wersja żądania przychodzącego. Możliwe wartości to: wersja 2008-10-27 i wszystkie nowsze wersje. Zobacz więcej szczegółów w https://docs.microsoft.com/en-us/rest/api/storageservices/versioning-for-the-azure-storage-services

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

### -PassThru
Wyświetlanie właściwości serviceproperties

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

### -ServiceType
Określa typ usługi magazynu.
To polecenie cmdlet pobiera właściwości rejestrowania dla typu usługi, który ten parametr określa.
Dopuszczalne wartości tego parametru to:
- Obiektów BLOB 
- Tworząc
- Wykonany
- Plik

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Potwierdź
Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet. Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext

## WYSYŁA

### Microsoft. platformy windowsazure. Commands. Storage. model. ResourceModel. PSSeriviceProperties

## INFORMACYJN

## LINKI POKREWNE
