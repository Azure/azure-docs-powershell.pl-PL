---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: 534919a404ad415963408816b78e9bbf1f349965
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239330"
---
# Get-AzBatchNodeFileContent

## SYNOPSIS
Pobiera plik węzła Partia.

## SKŁADNIA

### Task_Id_Path
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationPath <String>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### Task_Id_Stream
```
Get-AzBatchNodeFileContent -JobId <String> -TaskId <String> [-Path] <String> -DestinationStream <Stream>
 [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Path
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationPath <String> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### ComputeNode_Id_Stream
```
Get-AzBatchNodeFileContent [-PoolId] <String> [-ComputeNodeId] <String> [-Path] <String>
 -DestinationStream <Stream> [-ByteRangeStart <Int64>] [-ByteRangeEnd <Int64>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### InputObject_Path
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationPath <String> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### InputObject_Stream
```
Get-AzBatchNodeFileContent [[-InputObject] <PSNodeFile>] -DestinationStream <Stream> [-ByteRangeStart <Int64>]
 [-ByteRangeEnd <Int64>] -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Get-AzBatchNodeFileContent** pobiera plik węzła usługi Azure Batch i zapisuje go jako plik lub w strumieniu.

## PRZYKŁADY

### Przykład 1. Uzyskiwanie pliku węzła wsadowego skojarzonego z zadaniem i zapisywanie pliku
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

To polecenie pobiera plik węzła o nazwie StdOut.txt i zapisuje go E:\PowerShell\StdOut.txt ścieżce pliku na komputerze lokalnym.
Plik StdOut.txt jest skojarzony z zadaniem o identyfikatorze Zadanie01 dla zadania, które ma zadanie o identyfikatorze Zadanie01.
Użyj Get-AzBatchAccountKey cmdlet, aby przypisać kontekst do zmiennej $Context danych.

### Przykład 2. Pobierz plik węzła wsadowy i zapisz go w określonej ścieżce pliku przy użyciu potoku
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

To polecenie pobiera plik węzła o nazwie StdErr.txt za pomocą Get-AzBatchNodeFile cmdlet.
Polecenie przekazuje ten plik do bieżącego polecenia cmdlet przy użyciu operatora potoku.
Bieżące polecenie cmdlet zapisuje ten plik w E:\PowerShell\StdOut.txt ścieżce pliku na komputerze lokalnym.
Plik StdOut.txt węzła jest skojarzony z zadaniem, które ma identyfikator Task02 dla zadania o identyfikatorze Zadanie02.

### Przykład 3. Pobierz plik węzła Batch skojarzony z zadaniem i przekieruj go do strumienia
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

Pierwsze polecenie tworzy strumień przy użyciu polecenia cmdlet New-Object, a następnie zapisuje go w $Stream danych.
Drugie polecenie pobiera plik węzła o nazwie StdOut.txt z zadania o identyfikatorze Zadanie11 dla zadania o identyfikatorze Zadanie03.
Polecenie kieruje zawartość pliku do strumienia w $Stream.

### Przykład 4. Pobierz plik węzła z węzła obliczeniowego i zapisz go
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

To polecenie pobiera plik węzła Startup\StdOut.txt z węzła obliczeniowego, który ma identyfikator ComputeNode01 w puli, która ma pulę identyfikatorów 01.
Polecenie zapisze plik w lokalizacji E:\PowerShell\StdOut.txt na komputerze lokalnym.

### Przykład 5. Pobierz plik węzła z węzła obliczeniowego i zapisz go przy użyciu potoku
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

To polecenie pobiera plik węzła Startup\StdOut.txt, używając Get-AzBatchNodeFile z węzła obliczeniowego, który ma identyfikator ComputeNode01.
Węzeł obliczeniowy znajduje się w puli, która ma pulę identyfikatorów 01.
Polecenie przekazuje ten plik węzła do bieżącego polecenia cmdlet.
To polecenie cmdlet zapisuje plik w E:\PowerShell\StdOut.txt ścieżce pliku na komputerze lokalnym.

### Przykład 6. Pobierz plik węzła z węzła obliczeniowego i przekieruj go do strumienia
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

Pierwsze polecenie tworzy strumień przy użyciu New-Object cmdlet, a następnie zapisuje go w $Stream zmienną.
Drugie polecenie pobiera plik węzła o nazwie StdOut.txt z węzła obliczeniowego o identyfikatorze ComputeNode01 w puli o identyfikatorze Pool01.
Polecenie kieruje zawartość pliku do strumienia w $Stream.

## PARAMETERS

### - BatchContext
Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.
Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory. Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu. Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany. Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ByteRangeEnd
Koniec zakresu bajtów do pobrania.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ByteRangeStart
Początek zakresu bajtów do pobrania.

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ComputeNodeId
Określa identyfikator węzła obliczeniowego zawierającego plik węzła zwracany przez to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationPath
Określa ścieżkę pliku, w której to polecenie cmdlet zapisuje plik węzła.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, ComputeNode_Id_Path, InputObject_Path
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DestinationStream
Określa strumień, do którego to polecenie cmdlet zapisuje zawartość pliku węzła.
To polecenie cmdlet nie zamyka ani nie przewija tego strumienia.

```yaml
Type: System.IO.Stream
Parameter Sets: Task_Id_Stream, ComputeNode_Id_Stream, InputObject_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -InputObject
Określa plik, który to polecenie cmdlet pobiera jako **obiekt PSNodeFile.**
Aby uzyskać obiekt pliku węzła, użyj Get-AzBatchNodeFile cmdlet.

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNodeFile
Parameter Sets: InputObject_Path, InputObject_Stream
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### - JobId
Określa identyfikator zadania zawierającego zadanie docelowe.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Ścieżka
Ścieżka pliku węzła do pobrania.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream, ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### - PoolId
Określa identyfikator puli zawierającej węzeł obliczeniowy zawierający plik węzła, który pobiera to polecenie cmdlet.

```yaml
Type: System.String
Parameter Sets: ComputeNode_Id_Path, ComputeNode_Id_Stream
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - TaskId
Określa identyfikator zadania.

```yaml
Type: System.String
Parameter Sets: Task_Id_Path, Task_Id_Stream
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### Microsoft.Azure.Commands.Batch. Models.PSNodeFile

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## DANE WYJŚCIOWE

### System.Void

## NOTATKI

## LINKI POKREWNE

[Get-AzBatchAccountKey](./Get-AzBatchAccountKey.md)

[Get-AzBatchNodeFile](./Get-AzBatchNodeFile.md)

[Polecenia cmdlet partii platformy Azure](/powershell/module/Az.Batch/)
