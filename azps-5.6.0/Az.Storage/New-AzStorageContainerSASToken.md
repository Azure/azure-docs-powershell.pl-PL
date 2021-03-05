---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 6FF04E82-4921-4F7B-83D0-6997316BC5FD
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragecontainersastoken
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageContainerSASToken.md
ms.openlocfilehash: 09cbfb953118e5d6e29f2af25cd4653939135f07
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102002506"
---
# New-AzStorageContainerSASToken

## SYNOPSIS
Generuje token SAS dla kontenera magazynu platformy Azure.

## SKŁADNIA

### SasPolicy
```
New-AzStorageContainerSASToken [-Name] <String> -Policy <String> [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### SasPermission
```
New-AzStorageContainerSASToken [-Name] <String> [-Permission <String>] [-Protocol <SharedAccessProtocol>]
 [-IPAddressOrRange <String>] [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-FullUri]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **New-AzStorageContainerSASToken** generuje token SAS (Shared Access Signature) dla kontenera magazynu platformy Azure.

## PRZYKŁADY

### Przykład 1. Generowanie tokenu SAS kontenera z pełnym uprawnieniem kontenera
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Permission rwdl
```

W tym przykładzie jest generowany token SAS kontenera z pełnym uprawnieniem kontenera.

### Przykład 2. Generowanie tokenu SAS wielu kontenerów według potoku
```
PS C:\>Get-AzStorageContainer -Container test* | New-AzStorageContainerSASToken -Permission rwdl
```

W tym przykładzie jest generowanych wiele tokenów SAS kontenera przy użyciu potoku.

### Przykład 3. Generowanie tokenu SAS kontenera za pomocą zasad dostępu udostępnionego
```
PS C:\>New-AzStorageContainerSASToken -Name "Test" -Policy "PolicyName"
```

W tym przykładzie jest generowany token SAS kontenera z zasadami dostępu udostępnionego.

### Przykład 3. Generowanie tokenu SAS kontenera tożsamości użytkownika z kontekstem magazynowania na podstawie uwierzytelniania OAuth
```
PS C:\> $ctx = New-AzStorageContext -StorageAccountName $accountName -UseConnectedAccount
PS C:\> $StartTime = Get-Date
PS C:\> $EndTime = $startTime.AddDays(6)
PS C:\> New-AzStorageContainerSASToken -Name "ContainerName" -Permission rwd -StartTime $StartTime -ExpiryTime $EndTime -context $ctx
```

W tym przykładzie jest generowany token SAS kontenera tożsamości użytkownika z kontekstem magazynowania na podstawie uwierzytelniania OAuth

## PARAMETERS

### — kontekst
Określa kontekst magazynu platformy Azure.
Możesz go utworzyć za pomocą polecenia cmdlet New-AzStorageContext cmdlet.
Gdy kontekst magazynu jest oparty na uwierzytelnieniu OAuth, wygeneruje token SAS kontenera tożsamości użytkownika.

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
Jeśli użytkownik ustawi godzinę rozpoczęcia, ale nie czas wygaśnięcia, czas wygaśnięcia zostanie ustawiony na godzinę rozpoczęcia plus godzina.
Jeśli ani godzina rozpoczęcia, ani czas wygaśnięcia nie są określone, czas wygaśnięcia jest ustawiany na bieżący czas plus godzina.
Jeśli kontekst magazynu jest oparty na uwierzytelnianiu OAuth, czas wygaśnięcia musi upłynąć 7 dni od bieżącej godziny i nie może być wcześniejszy niż bieżący czas.

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

### -FullUri
Wskazuje, że to polecenie cmdlet zwraca pełny adres URI obiektu blob i token podpisu dostępu udostępnionego.

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

### — Nazwa
Określa nazwę kontenera magazynu platformy Azure.

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

### — Uprawnienie
Określa uprawnienia dla kontenera magazynu.
Należy pamiętać, że jest to ciąg, taki jak `rwd` (w przypadku odczytu, zapisu i usunięcia).

```yaml
Type: System.String
Parameter Sets: SasPermission
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Zasady
Określa zasady przechowywanego dostępu platformy Azure.

```yaml
Type: System.String
Parameter Sets: SasPolicy
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Protokół
Określa protokół dozwolony dla żądania.
Dopuszczalne wartości dla tego parametru to:
* HttpsOnly
* HttpsOrHttp Wartość domyślna to httpsorhttp.

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

### — StartTime
Określa czas, w którym podpis dostępu udostępnionego stanie się prawidłowy.

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

### — Potwierdź
Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.

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
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet. Polecenie cmdlet nie zostanie uruchomione.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### System.String

### Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext

## DANE WYJŚCIOWE

### System.String

## NOTATKI

## LINKI POKREWNE

[New-AzstorageBlobSASToken](./New-AzStorageBlobSASToken.md)
