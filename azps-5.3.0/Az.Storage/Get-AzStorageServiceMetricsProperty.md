---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 4d58b8e323476adda73f4a4827dc263c20bd4cc4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502736"
---
# Get-AzStorageServiceMetricsProperty

## STRESZCZENIe
Pobiera właściwości metryk dla usługi Azure Storage.

## POLECENIA

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzStorageServiceMetricsProperty** pobiera właściwości metryk dla usługi Azure Storage.

## Przykłady

### Przykład 1: uzyskiwanie właściwości metryk dla usługi BLOB
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

To polecenie pobiera właściwości metryk magazynu obiektów BLOB dla typu metryki godzinowych.

## PARAMETRÓW

### -Context
Określa kontekst usługi Azure Storage.
Aby uzyskać kontekst miejsca do magazynowania, użyj polecenia cmdlet New-AzStorageContext.

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

### -Metryki
Określa typ metryk.
To polecenie cmdlet umożliwia pobieranie właściwości metryki usługi Azure Storage dla typu metryki, który ten parametr określa.
Dopuszczalne wartości tego parametru to: godzina i minuta.

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServiceType
Określa typ usługi magazynu.
To polecenie cmdlet pobiera właściwości metryk dla typu, który określa ten parametr.
Dopuszczalne wartości tego parametru to:
- Obiektów BLOB 
- Tworząc
- Wykonany
- Plik wartość pliku nie jest obecnie obsługiwana.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext

## WYSYŁA

### Microsoft. Azure. Storage. Shared. Protocol. MetricsProperties

## INFORMACYJN

## LINKI POKREWNE

[Nowe — AzStorageContext](./New-AzStorageContext.md)

[Set-AzStorageServiceMetricsProperty](./Set-AzStorageServiceMetricsProperty.md)


