---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: FB9ACBA2-081E-4876-A21A-F5BA11CBEDA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/publish-azvmdscconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Publish-AzVMDscConfiguration.md
ms.openlocfilehash: 3db80e92a7bcd61fc62adaafda0bb3887f532202
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706303"
---
# Publish-AzVMDscConfiguration

## STRESZCZENIe
Przekazywanie skryptu DSC do magazynu obiektów blob platformy Azure.

## POLECENIA

### UploadArchive (domyślny)
```
Publish-AzVMDscConfiguration [-ResourceGroupName] <String> [-ConfigurationPath] <String>
 [[-ContainerName] <String>] [-StorageAccountName] <String> [-StorageEndpointSuffix <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### Funkcja Zarchiwizuj
```
Publish-AzVMDscConfiguration [-ConfigurationPath] <String> [[-OutputArchivePath] <String>] [-Force]
 [-SkipDependencyDetection] [-ConfigurationDataPath <String>] [-AdditionalPath <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Publish-AzVMDscConfiguration** umożliwia przekazanie skryptu konfiguracji stanu (DSC) do magazynu obiektów blob platformy Azure, który później można zastosować do maszyn wirtualnych platformy Azure przy użyciu polecenia cmdlet Set-AzVMDscExtension.

## Przykłady

### Przykład 1: Tworzenie pakietu zip przekazywanie go do magazynu platformy Azure
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1"
```

To polecenie tworzy pakiet ZIP dla danego skryptu i wszystkich modułów zasobów zależnych, a następnie przekazuje go do magazynu platformy Azure.

### Przykład 2: Tworzenie pakietu zip i przechowywanie go w pliku lokalnym
```
PS C:\> Publish-AzVMDscConfiguration ".\MyConfiguration.ps1" -OutputArchivePath ".\MyConfiguration.ps1.zip"
```

To polecenie tworzy pakiet ZIP dla danego skryptu i wszystkich modułów zasobów zależnych i zapisuje go w pliku lokalnym o nazwie .\MyConfiguration.ps1.zip.

### Przykład 3: Dodawanie konfiguracji do archiwum, a następnie przekazywanie go do magazynu
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -SkipDependencyDetection
```

To polecenie dodaje konfigurację o nazwie Sample.ps1 do archiwum konfiguracji w celu przekazania do magazynu platformy Azure i pominięcie modułów zasobów zależnych.

### Przykład 4: Dodawanie danych konfiguracji i konfiguracji do archiwum, a następnie przekazywanie go do magazynu
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -ConfigurationDataPath "C:\SampleData.psd1"
```

To polecenie dodaje konfigurację o nazwie Sample.ps1 i dane konfiguracji o nazwie SampleData.psd1 do archiwum konfiguracji w celu przekazania do magazynu platformy Azure.

### Przykład 5: Dodawanie konfiguracji, danych konfiguracyjnych i dodatkowej zawartości do archiwum, a następnie przekazywanie go do miejsca do magazynowania
```
PS C:\> Publish-AzVMDscConfiguration -ConfigurationPath "C:\Sample.ps1" -AdditionalPath @("C:\ContentDir1", "C:\File.txt") -ConfigurationDataPath "C:\SampleData.psd1"
```

To polecenie umożliwia dodanie konfiguracji o nazwie Sample.ps1, danych konfiguracji SampleData.psd1 oraz dodatkowej zawartości do archiwum konfiguracji w celu przekazania do magazynu platformy Azure.

## PARAMETRÓW

### -AdditionalPath
Określa ścieżkę pliku lub katalogu, który ma zostać uwzględniony w archiwum konfiguracji.
Pobieranie zostanie pobrane na maszynie wirtualnej wraz z konfiguracją.

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationDataPath
Określa ścieżkę pliku psd1, który określa dane konfiguracji.
Zostanie ona dodana do archiwum konfiguracji, a następnie przekazana do funkcji konfiguracji.
Zostanie zastąpiona ścieżką danych konfiguracyjnych dostarczaną za pośrednictwem polecenia cmdlet Set-AzVMDscExtension

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationPath
Określa ścieżkę pliku zawierającego co najmniej jeden wariant.
Plik może być plikiem skryptu programu Windows PowerShell (. ps1) lub plikiem modułu programu Windows PowerShell (. PSM1).

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### -ContainerName
Określa nazwę kontenera magazynu platformy Azure, do którego jest przekazywana konfiguracja.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: 4
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

### -Force
Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.

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

### -OutputArchivePath
Określa ścieżkę lokalnego pliku. zip, w którym ma zostać napisana archiwum konfiguracji.
Gdy ten parametr jest wykorzystywany, skrypt konfiguracji nie jest przekazywany do magazynu obiektów blob platformy Azure.

```yaml
Type: System.String
Parameter Sets: CreateArchive
Aliases: ConfigurationArchivePath

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów zawierającej konto magazynu.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipDependencyDetection
Wskazuje, że to polecenie cmdlet wyklucza zależności zasobu DSC z archiwum konfiguracji.

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

### -StorageAccountName
Określa nazwę konta usługi Azure Storage, która jest używana do przekazania skryptu konfiguracji do kontenera określonego przez parametr *ContainerName* .

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageEndpointSuffix
Określa sufiks punktu końcowego magazynu.

```yaml
Type: System.String
Parameter Sets: UploadArchive
Aliases:

Required: False
Position: Named
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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### System. String []

## WYSYŁA

### System. String

## INFORMACYJN

## LINKI POKREWNE

[Get-AzVMDscExtension](./Get-AzVMDscExtension.md)

[Remove-AzVMDscExtension](./Remove-AzVMDscExtension.md)

[Set-AzVMDscExtension](./Set-AzVMDscExtension.md)


