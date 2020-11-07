---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 212281F0-9A3E-4652-919F-400455E3950E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMAEMExtension.md
ms.openlocfilehash: 3970d26199fc122f248ad8e41a5146222cad23e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718952"
---
# Get-AzureRmVMAEMExtension

## STRESZCZENIe
Pobiera informacje o rozszerzeniu AEM.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Get-AzureRmVMAEMExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Status]
 [[-OSType] <String>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmVMAEMExtension** pobiera informacje o rozszerzeniu usługi Azure enhanceing Monitoring (AEM).

## Przykłady

### Przykład 1: uzyskiwanie rozszerzenia AEM
```
PS C:\> Get-AzureRmVMAEMExtension -ResourceGroupName "ResourceGroup11" -VMName "contoso-server"
```

To polecenie pobiera informacje o rozszerzeniu AEM dla maszyny wirtualnej o nazwie contoso — Server.

## PARAMETRÓW

### -Name (nazwa)
Określa nazwę maszyny wirtualnej.
To polecenie cmdlet umożliwia pobieranie informacji dotyczących rozszerzenia AEM na maszynie wirtualnej, którą to polecenie cmdlet określa.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -OSType
Określa typ systemu operacyjnego dysku systemu operacyjnego.
Jeśli dysk systemu operacyjnego nie ma typu, należy określić ten parametr.
Dopuszczalne wartości tego parametru to: Windows i Linux.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów maszyny wirtualnej.
To polecenie cmdlet umożliwia pobieranie informacji dotyczących rozszerzenia AEM na tej maszynie wirtualnej.

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

### -Status
Wskazuje, że to polecenie cmdlet pobiera tylko widok wystąpienia rozszerzenia AEM.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Określa nazwę maszyny wirtualnej.
To polecenie cmdlet umożliwia pobieranie informacji o rozszerzeniu AEM dla maszyny wirtualnej, którą ten parametr określa.

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

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

## INFORMACYJN

## LINKI POKREWNE

[Remove-AzureRmVMAEMExtension](./Remove-AzureRmVMAEMExtension.md)

[Set-AzureRmVMAEMExtension](./Set-AzureRmVMAEMExtension.md)

[Test — AzureRmVMAEMExtension](./Test-AzureRmVMAEMExtension.md)


