---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 2de23408aef9d9af4ebd23eb520261760883cf3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994785"
---
# Get-AzStorageTableStoredAccessPolicy

## SYNOPSIS
Pobiera zasady lub zasady dostępu przechowywane dla tabeli magazynu platformy Azure.

## SKŁADNIA

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzStorageTableStoredAccessPolicy** zawiera listę przechowywanych zasad dostępu dla tabeli magazynu platformy Azure.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie przechowywanych zasad dostępu w tabeli magazynu
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

To polecenie pobiera zasady dostępu o nazwie Zasady50 w tabeli magazynu o nazwie Tabela02.

### Przykład 2. Uzyskiwanie wszystkich przechowywanych zasad dostępu w tabeli magazynu
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

To polecenie pobiera wszystkie zasady dostępu w tabeli o nazwie Tabela02.

## PARAMETERS

### — kontekst
Określa kontekst magazynu platformy Azure.
Aby uzyskać kontekst magazynu, użyj New-AzStorageContext cmdlet.

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

### — Zasady
Określa zasady przechowywanego dostępu, które zawierają uprawnienia do tego tokenu SAS (Shared Access Signature).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Tabela
Określa nazwę tabeli magazynu platformy Azure.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## DANE WYJŚCIOWE

### Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy

## NOTATKI

## LINKI POKREWNE

[New-AzStorageTableStoredAccessPolicy](./New-AzStorageTableStoredAccessPolicy.md)

[Remove-AzStorageTableStoredAccessPolicy](./Remove-AzStorageTableStoredAccessPolicy.md)

[Set-AzStorageTableStoredAccessPolicy](./Set-AzStorageTableStoredAccessPolicy.md)

[New-AzStorageContext](./New-AzStorageContext.md)


