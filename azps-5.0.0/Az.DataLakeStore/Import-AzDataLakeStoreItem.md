---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: 90630395-8747-4446-A879-323274811956
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/import-azdatalakestoreitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Import-AzDataLakeStoreItem.md
ms.openlocfilehash: bdad54f8d5615fe0e8c3a1a7d75077e9e6f34f80
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305569"
---
# Import-AzDataLakeStoreItem

## STRESZCZENIe
Umożliwia przekazywanie lokalnego pliku lub katalogu do usługi Data Lake Store.

## POLECENIA

### NoDiagnosticLogging (domyślny)
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### IncludeDiagnosticLogging
```
Import-AzDataLakeStoreItem [-Account] <String> [-Path] <String> [-Destination] <DataLakeStorePathInstance>
 [-Recurse] [-Resume] [-ForceBinary] [-Force] [-Concurrency <Int32>] [-DiagnosticLogLevel <LogLevel>]
 -DiagnosticLogPath <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Import-AzDataLakeStoreItem** umożliwia przekazanie lokalnego pliku lub katalogu do usługi Data Lake Store.

## Przykłady

### Przykład 1: przekazywanie pliku
```
PS C:\>Import-AzDataLakeStoreItem -AccountName "ContosoADL" -Path "C:\SrcFile.csv" -Destination "/MyFiles/File.csv" -Concurrency 4
```

To polecenie umożliwia przekazywanie pliku SrcFile.csv i dodanie go do folderu Moje pliki w usłudze Data Lake Store jako File.csv z współbieżnością równą 4.

## PARAMETRÓW

### — Konto
Określa nazwę konta usługi Data Lake Store.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Concurrency
Wskazuje liczbę plików lub fragmentów, które mają być przekazywane równolegle. Wartość domyślna będzie obliczana jako Najlepsza nakład pracy na podstawie specyfikacji systemowych.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
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

### -Miejsce docelowe
Określa ścieżkę usługi Data Lake Store, do której ma zostać przekazany plik lub folder, począwszy od katalogu głównego (/).

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiagnosticLogLevel
Opcjonalnie wskazuje poziom dziennika diagnostycznego, który ma być używany do rejestrowania zdarzeń podczas importowania pliku lub folderu. Błąd domyślny.

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.LogLevel
Parameter Sets: IncludeDiagnosticLogging
Aliases:
Accepted values: Debug, Information, Error, None

Required: False
Position: Named
Default value: Error
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DiagnosticLogPath
Określa ścieżkę dziennika diagnostycznego, do którego mają być rejestrowane zdarzenia podczas importowania pliku lub folderu.

```yaml
Type: System.String
Parameter Sets: IncludeDiagnosticLogging
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Force
Wskazuje, że ta operacja może spowodować zastąpienie pliku docelowego, jeśli już istnieje.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ForceBinary
Wskazuje, że kopiowane pliki powinny być kopiowane bez obawy o zachowanie nowych wierszy po dołączaniu.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Path
Określa ścieżkę lokalną pliku lub folderu, który ma zostać przekazany.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Rekursywowanie
Wskazuje, że ta operacja powinna przekazać wszystkie elementy we wszystkich podfolderach.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Życiorys
Wskazuje, że kopiowane pliki są kontynuacją wcześniejszego przekazania. Spowoduje to, że system będzie próbował wznowić pracę z ostatniego pliku, który nie został w pełni przekazany.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.
Polecenie cmdlet nie jest uruchamiane.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. DataLakeStore. models. DataLakeStorePathInstance

### System. Management. Automation. SwitchParameter

### System. Int32

### Microsoft. Azure. Commands. DataLakeStore. models. LogLevel

## WYSYŁA

### System. String

## INFORMACYJN

## LINKI POKREWNE

[Get-AzDataLakeStoreItem](./Get-AzDataLakeStoreItem.md)

[Eksportowanie — AzDataLakeStoreItem](./Export-AzDataLakeStoreItem.md)

[Dołącz do AzDataLakeStoreItem](./Join-AzDataLakeStoreItem.md)

[Przenieś — AzDataLakeStoreItem](./Move-AzDataLakeStoreItem.md)

[Nowe — AzDataLakeStoreItem](./New-AzDataLakeStoreItem.md)

[Remove-AzDataLakeStoreItem](./Remove-AzDataLakeStoreItem.md)

[Test — AzDataLakeStoreItem](./Test-AzDataLakeStoreItem.md)


