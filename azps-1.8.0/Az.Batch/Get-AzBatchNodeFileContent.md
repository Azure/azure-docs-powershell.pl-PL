---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C9E2D9EC-3B6A-492D-B183-9856185548CD
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchnodefilecontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchNodeFileContent.md
ms.openlocfilehash: b04461caa9b3f10438706a5a2a2017eef3e71cb3
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/13/2020
ms.locfileid: "93710844"
---
# Get-AzBatchNodeFileContent

## STRESZCZENIe
Pobiera plik węzła wsadowego.

## POLECENIA

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

## Opis
Polecenie cmdlet **Get-AzBatchNodeFileContent** pobiera plik węzła usługi Azure Batch i zapisuje go jako plik lub strumień.

## Przykłady

### Przykład 1: uzyskiwanie pliku węzła partii skojarzonego z zadaniem i zapisywanie pliku
```
PS C:\>Get-AzBatchNodeFileContent -JobId "Job01" -TaskId "Task01" -Path "StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

To polecenie powoduje wyświetlenie pliku węzła o nazwie StdOut.txt i zapisanie go w E:\PowerShell\StdOut.txt ścieżki pliku na komputerze lokalnym.
Plik węzła StdOut.txt jest skojarzony z zadaniem o IDENTYFIKATORze Task01 dla zadania o IDENTYFIKATORze Job01.
Użyj polecenia cmdlet Get-AzBatchAccountKeys, aby przypisać kontekst do zmiennej $Context.

### Przykład 2: pobranie pliku węzła partii i zapisanie go w określonej ścieżce pliku za pomocą potoku
```
PS C:\>Get-AzBatchNodeFile -JobId "Job02" -TaskId "Task02" -Path "StdErr.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

To polecenie pobiera plik węzła o nazwie StdErr.txt przy użyciu polecenia cmdlet Get-AzBatchNodeFile.
Polecenie przekazuje ten plik do bieżącego polecenia cmdlet za pomocą operatora potoku.
Bieżące polecenie cmdlet zapisuje ten plik w ścieżce pliku E:\PowerShell\StdOut.txt na komputerze lokalnym.
Plik węzła StdOut.txt jest skojarzony z zadaniem zawierającym identyfikator Task02 dla zadania o IDENTYFIKATORze Job02.

### Przykład 3: uzyskiwanie pliku węzła partii skojarzonego z zadaniem i kierowanie go do strumienia
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -JobId "Job03" -TaskId "Task11" -Path "StdOut.txt" -DestinationStream $Stream -BatchContext $Context
```

Pierwsze polecenie tworzy strumień za pomocą polecenia cmdlet New-Object, a następnie zapisuje go w zmiennej $Stream.
Drugie polecenie pobiera plik węzła o nazwie StdOut.txt z zadania o IDENTYFIKATORze Task11 dla zadania o IDENTYFIKATORze Job03.
Polecenie kieruje zawartość pliku do strumienia w $Stream.

### Przykład 4: Pobieranie pliku węzła z węzła compute i zapisywanie go
```
PS C:\>Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

To polecenie pobiera plik węzła Startup\StdOut.txt z węzła obliczeniowego zawierającego identyfikator ComputeNode01 w puli, która ma identyfikator Pool01.
Polecenie zapisuje plik w ścieżce pliku E:\PowerShell\StdOut.txt na komputerze lokalnym.

### Przykład 5: Pobieranie pliku węzła z węzła compute i zapisywanie go za pomocą potoku
```
PS C:\>Get-AzBatchNodeFile -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "Startup\StdOut.txt" -BatchContext $Context | Get-AzBatchNodeFileContent -DestinationPath "E:\PowerShell\StdOut.txt" -BatchContext $Context
```

To polecenie pobiera plik węzła Startup\StdOut.txt przy użyciu Get-AzBatchNodeFile z węzła obliczeniowego o IDENTYFIKATORze ComputeNode01.
Węzeł obliczeniowy znajduje się w puli o IDENTYFIKATORze Pool01.
Polecenie przekazuje ten plik węzła do bieżącego polecenia cmdlet.
Polecenie cmdlet zapisuje plik w ścieżce pliku E:\PowerShell\StdOut.txt na komputerze lokalnym.

### Przykład 6: Pobieranie pliku węzła z węzła obliczeniowego i kierowanie go do strumienia
```
PS C:\>$Stream = New-Object -TypeName "System.IO.MemoryStream"
PS C:\> Get-AzBatchNodeFileContent -PoolId "Pool01" -ComputeNodeId "ComputeNode01" -Path "startup\stdout.txt" -DestinationStream $Stream -BatchContext $Context
```

Pierwsze polecenie tworzy strumień za pomocą polecenia cmdlet New-Object, a następnie zapisuje go w zmiennej $Stream.
Drugie polecenie pobiera plik węzła o nazwie StdOut.txt z węzła obliczeniowego o IDENTYFIKATORze ComputeNode01 w puli o IDENTYFIKATORze Pool01.
Polecenie kieruje zawartość pliku do strumienia w $Stream.

## PARAMETRÓW

### -BatchContext
Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.
Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego. Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu. W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu. Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.

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
Koniec zakresu bajtów, który ma zostać pobrany.

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
Początek zakresu bajtów, który ma zostać pobrany.

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
Określa identyfikator węzła obliczeniowego zawierającego plik węzła, który zostanie zwrócony przez to polecenie cmdlet.

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
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

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
Określa ścieżkę pliku, w którym to polecenie cmdlet zapisuje plik węzła.

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
Określa strumień, w którym polecenie cmdlet zapisuje zawartość pliku węzła.
To polecenie cmdlet nie zamyka ani nie Przewija tego strumienia.

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

### -Inputobject
Określa plik, który jest pobierany przez to polecenie cmdlet, jako obiekt **PSNodeFile** .
Aby uzyskać obiekt pliku węzła, użyj polecenia cmdlet Get-AzBatchNodeFile.

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

### -JobId
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

### -Path
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

### -PoolId
Określa identyfikator puli zawierającej węzeł obliczeniowy, który zawiera plik węzła, który jest pobierany przez to polecenie cmdlet.

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

### -TaskId
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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### Microsoft.Azure.Commands.Batch. Modele. PSNodeFile

### Microsoft.Azure.Commands.Batch.BatchAccountContext

## WYSYŁA

### System. void

## INFORMACYJN

## LINKI POKREWNE

[Get-AzBatchAccountKeys](./Get-AzBatchAccountKey.md)

[Get-AzBatchNodeFile](./Get-AzBatchNodeFile.md)

[Polecenia cmdlet usługi Azure Batch](/powershell/module/az.batch)


