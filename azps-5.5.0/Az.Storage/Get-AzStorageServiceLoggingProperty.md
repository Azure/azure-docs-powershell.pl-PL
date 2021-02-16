---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 6e4eced11a9de228f836e80e9f25350e3f09a8c0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176611"
---
# Get-AzStorageServiceLoggingProperty

## SYNOPSIS
Pobiera właściwości rejestrowania dla usług magazynu platformy Azure.

## SKŁADNIA

```
Get-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzStorageServiceLoggingProperty** pobiera właściwości rejestrowania dla usług magazynu platformy Azure.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie właściwości rejestrowania dla usługi obiektów blob
```
C:\PS>Get-AzStorageServiceLoggingProperty -ServiceType Blob
```

To polecenie pobiera właściwości rejestrowania dla magazynu obiektów blob.

## PARAMETERS

### — kontekst
Określa kontekst magazynu platformy Azure.
Aby uzyskać kontekst magazynowania, użyj New-AzStorageContext cmdlet.

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

### -ServiceType
Określa typ usługi magazynowania.
To polecenie cmdlet pobiera właściwości rejestrowania dla typu usługi, który określa ten parametr.
Dopuszczalne wartości dla tego parametru to:
- Obiekt blob 
- Tabela
- Kolejka
- Plik Wartość Pliku nie jest obecnie obsługiwana.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## OUTPUTS

### Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties

## NOTATKI

## LINKI POKREWNE

[New-AzStorageContext](./New-AzStorageContext.md)

[Set-AzStorageServiceLoggingProperty](./Set-AzStorageServiceLoggingProperty.md)


