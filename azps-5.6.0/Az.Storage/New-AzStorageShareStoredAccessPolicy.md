---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 37E76360-B683-407C-9AEF-7138374562D8
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragesharestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageShareStoredAccessPolicy.md
ms.openlocfilehash: 3604d6e8d3c9394a53c59e220bdef31662a75f88
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002337"
---
# New-AzStorageShareStoredAccessPolicy

## SYNOPSIS
Tworzy przechowywane zasady dostępu dla udziału magazynu.

## SKŁADNIA

```
New-AzStorageShareStoredAccessPolicy [-ShareName] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-ServerTimeoutPerRequest <Int32>] [-ClientTimeoutPerRequest <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-ConcurrentTaskCount <Int32>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet New-AzStorageShareStoredAccessPolicy** tworzy zasady dostępu przechowywanego w magazynie platformy Azure.

## PRZYKŁADY

### Przykład 1. Tworzenie przechowywanych zasad dostępu w udziałach
```
PS C:\>New-AzStorageShareStoredAccessPolicy -ShareName "ContosoShare" -Policy "GeneralPolicy" -Permission "rwdl"
```

To polecenie tworzy przechowywane zasady dostępu, które mają pełne uprawnienia w udostępniniu.

## PARAMETERS

### -ClientTimeoutPerRequest
Określa przedział czasu po stronie klienta (w sekundach) dla jednego żądania usługi.
Jeśli poprzednie połączenie nie powiedzie się w określonym interwale, to polecenie cmdlet podejmie ponowne próbę żądania.
Jeśli to polecenie cmdlet nie otrzyma pomyślnej odpowiedzi przed upływem interwału, to polecenie cmdlet zwraca błąd.

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
Określa maksymalną liczbę jednoczesnych połączeń sieciowych.
Za pomocą tego parametru można ograniczyć współbieżność w celu ograniczenia użycia lokalnego procesora i przepustowości, określając maksymalną liczbę jednoczesnych połączeń sieciowych.
Określona wartość jest wartością bezwzględną i nie jest mnożona przez liczbę podstawową.
Ten parametr może pomóc zmniejszyć problemy z połączeniem sieciowym w środowiskach o niskiej przepustowości, takich jak 100 kilobitów na sekundę.
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

### — kontekst
Określa kontekst magazynu platformy Azure.
Aby uzyskać kontekst przechowywania, użyj polecenia cmdlet [New-AzStorageContext.](./New-AzStorageContext.md)

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
Określa czas, w którym przechowywane zasady dostępu stają się nieprawidłowe.

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

### — Uprawnienie
Określa uprawnienia w zasadach dostępu przechowywanego do uzyskiwania dostępu do udziału magazynu lub plików w tej chmurze.
Należy pamiętać, że jest to ciąg, taki jak `rwd` (w przypadku odczytu, zapisu i usunięcia).

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

### — Zasady
Określa nazwę przechowywanych zasad dostępu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ServerTimeoutPerRequest
Określa długość okresu przeoencji dla części żądania na serwerze.

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
Określa czas, w którym przechowywane zasady dostępu stają się prawidłowe.

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

## LINKI POKREWNE

[Get-AzStorageShareStoredAccessPolicy](./Get-AzStorageShareStoredAccessPolicy.md)

[New-AzStorageContext](./New-AzStorageContext.md)

[Remove-AzStorageShareStoredAccessPolicy](./Remove-AzStorageShareStoredAccessPolicy.md)

[Set-AzStorageShareStoredAccessPolicy](./Set-AzStorageShareStoredAccessPolicy.md)
