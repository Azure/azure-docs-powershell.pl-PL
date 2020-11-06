---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 67AED9B8-AE3D-47E5-813C-9B46E11AE46C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Test-AzureRmVMAEMExtension.md
ms.openlocfilehash: d766102b0e87968e59bdd9bf63157dd62e977a25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525262"
---
# Test-AzureRmVMAEMExtension

## STRESZCZENIe
Sprawdza konfigurację rozszerzenia AEM.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Test-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-OSType] <String>]
 [[-WaitTimeInMinutes] <Int32>] [-SkipStorageCheck] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **test-AzureRmVMAEMExtension** sprawdza konfigurację rozszerzenia usługi Azure Enhanced Monitoring (AEM).
Rozszerzenie AEM gromadzi dane dotyczące wydajności.
To polecenie cmdlet sprawdza, czy dane wydajności są dostępne.

## Przykłady

### Przykład 1: Sprawdzanie konfiguracji rozszerzenia AEM
```
PS C:\> Test-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

To polecenie sprawdza konfigurację rozszerzenia AEM dla maszyny wirtualnej o nazwie contoso — Server.

## PARAMETRÓW

### -OSType
Określa typ systemu operacyjnego dysku systemu operacyjnego.
Jeśli dysk systemu operacyjnego nie ma typu, należy określić ten parametr.
Dopuszczalne wartości tego parametru to: Windows i Linux.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów maszyny wirtualnej, którą to polecenie cmdlet sprawdza.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -SkipStorageCheck
Wskazuje, że to polecenie cmdlet pomija Sprawdzanie konfiguracji magazynu.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -VMName
Określa nazwę maszyny wirtualnej.
To polecenie cmdlet testuje rozszerzenie AEM dla maszyny wirtualnej, którą ten parametr określa.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -WaitTimeInMinutes
Określa limit czasu (w minutach) sprawdzania konfiguracji magazynu.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureRmVMAEMExtension](./Get-AzureRmVMAEMExtension.md)

[Remove-AzureRmVMAEMExtension](./Remove-AzureRmVMAEMExtension.md)

[Set-AzureRmVMAEMExtension](./Set-AzureRmVMAEMExtension.md)


