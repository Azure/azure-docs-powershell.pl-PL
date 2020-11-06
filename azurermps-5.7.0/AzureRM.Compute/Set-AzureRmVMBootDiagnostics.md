---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 9A6F140C-9F1C-4701-9603-FC6107FCAF92
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMBootDiagnostics.md
ms.openlocfilehash: c02551e09fa0a5ce484883a4b2925c0c172e537f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542699"
---
# Set-AzureRmVMBootDiagnostics

## STRESZCZENIe
Modyfikowanie właściwości diagnostyki rozruchu maszyny wirtualnej.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### EnableBootDiagnostics
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Enable] [-ResourceGroupName] <String>
 [[-StorageAccountName] <String>] [<CommonParameters>]
```

### DisableBootDiagnostics
```
Set-AzureRmVMBootDiagnostics [-VM] <PSVirtualMachine> [-Disable] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzureRmVMBootDiagnostics** modyfikuje właściwości diagnostyki rozruchu maszyny wirtualnej.

## Przykłady

### Przykład 1: Włączanie diagnostyki rozruchu
```
PS C:\> $VM = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "ContosoVM07"
PS C:\> Set-AzureRmVMBootDiagnostics -VM $VM -Enable -ResourceGroupName "ResourceGroup11" -StorageAccountName "DiagnosticStorage"
PS C:\> Update-AzureRmVM -ResourceGroup "ResourceGroup11" -VM $VM
```

Pierwsze polecenie uzyskuje maszynę wirtualną o nazwie ContosoVM07 przy użyciu polecenia **Get-AzureRmVM**.
Polecenie zapisuje je w zmiennej $VM.

Drugie polecenie włącza diagnostykę rozruchu maszyny wirtualnej w $VM.
Dane diagnostyczne są przechowywane na określonym koncie.

## PARAMETRÓW

### -Disable
Wskazuje, że to polecenie cmdlet wyłącza diagnostykę rozruchu maszyny wirtualnej.

```yaml
Type: SwitchParameter
Parameter Sets: DisableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable
Wskazuje, że to polecenie cmdlet włącza diagnostykę rozruchu maszyny wirtualnej.

```yaml
Type: SwitchParameter
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów maszyny wirtualnej.

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageAccountName
Określa nazwę konta magazynu, w którym mają być zapisywane dane diagnostyczne rozruchu.

```yaml
Type: String
Parameter Sets: EnableBootDiagnostics
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Określa maszynę wirtualną, dla której to polecenie cmdlet zmienia narzędzie diagnostyczne rozruchu.
Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet Get-AzureRmVM.

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
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

[Get-AzureRmVM](./Get-AzureRmVM.md)

[Get-AzureRmVMBootDiagnosticsData](./Get-AzureRmVMBootDiagnosticsData.md)


