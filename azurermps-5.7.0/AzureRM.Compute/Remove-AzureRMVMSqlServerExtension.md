---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: B02CEAC8-C838-4890-8C21-9897CA39EF45
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: f074d61919098d6c23ab39424774d9ba18e457d6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526945"
---
# Remove-AzureRmVMSqlServerExtension

## STRESZCZENIe
Usuwa rozszerzenie programu SQL Server z maszyny wirtualnej.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

```
Remove-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name] <String>
 [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureRmVMSqlServerExtension** usuwa rozszerzenie serwera AzureSQL z maszyny wirtualnej.

## Przykłady

### Przykład 1: Usuwanie rozszerzenia programu SQL Server
```
PS C:\> Remove-AzureRMVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM22" -Name "SqlIaaSAgent"
```

To polecenie usuwa rozszerzenie programu SQL Server z maszyny wirtualnej o nazwie ContosoVM22.

## PARAMETRÓW

### -Name (nazwa)
Określa nazwę rozszerzenia programu SQL Server, które zostanie usunięte przez to polecenie cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów maszyny wirtualnej.

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

### -VMName
Określa nazwę maszyny wirtualnej, z której to polecenie cmdlet usuwa rozszerzenie programu SQL Server.

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

[Get-AzureRmVMSqlServerExtension](./Get-AzureRMVMSqlServerExtension.md)

[Set-AzureRmVMSqlServerExtension](./Set-AzureRMVMSqlServerExtension.md)


