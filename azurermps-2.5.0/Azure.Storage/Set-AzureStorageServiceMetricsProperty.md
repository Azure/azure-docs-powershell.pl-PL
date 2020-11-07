---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/set-azurestorageservicemetricsproperty
schema: 2.0.0
ms.openlocfilehash: 45192b6b24719bb793e3f443cf2a8cb42abd78ad
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899403"
---
# Set-AzureStorageServiceMetricsProperty

## STRESZCZENIe
Modyfikuje właściwości metryk dla usługi Azure Storage.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureStorageServiceMetricsProperty** modyfikuje właściwości metryk dla usługi Azure Storage.

## Przykłady

### Przykład 1: modyfikowanie właściwości metryk dla usługi BLOB
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

To polecenie modyfikuje metryki w wersji 1,0 dla magazynu obiektów BLOB na poziom usług.
Metryki usługi Azure Storage są zachowywanie wpisów przez 10 dni.
Ponieważ to polecenie określa parametr *PassThru* , polecenie wyświetla właściwości zmodyfikowano metryki.

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

### -MetricsLevel
Określa poziom metryk używany dla usługi Azure Storage.
Dopuszczalne wartości tego parametru to:
- Znaleziono
- Służby
- ServiceAndApi

```yaml
Type: System.Nullable`1[Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Metryki
Określa typ metryk.
Ten cmldet ustawia wartość typu metryki usługi Azure Storage na wartość określaną przez ten parametr.
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

### -PassThru
Wskazuje, że te polecenia cmdlet zwracają zaktualizowane właściwości metryk.
Jeśli nie podano tego parametru, to polecenie cmdlet nie zwraca wartości.

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

### -RetentionDays
Określa liczbę dni przechowywania informacji o metrykach w usłudze Azure Storage.

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

### -ServiceType
Określa typ usługi magazynu.
To polecenie cmdlet modyfikuje właściwości metryk dla typu usługi, którego ten parametr określa.
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

### -Version
Określa wersję metryk magazynu platformy Azure.
Wartość domyślna to 1,0.

```yaml
Type: System.Nullable`1[System.Double]
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

### Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext

## WYSYŁA

### Microsoft. platformy windowsazure. Storage. Shared. Protocol. MetricsProperties

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureStorageServiceMetricsProperty](./Get-AzureStorageServiceMetricsProperty.md)

[Nowe — AzureStorageContext](./New-AzureStorageContext.md)


