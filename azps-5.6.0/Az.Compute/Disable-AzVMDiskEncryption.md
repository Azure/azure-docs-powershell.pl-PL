---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: bd96a26eda14770dcc7a5592e12e64e15eac02f6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101969434"
---
# Disable-AzVMDiskEncryption

## SYNOPSIS
Wyłącza szyfrowanie na komputerze wirtualnym IaaS.

## SKŁADNIA

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## OPIS
Polecenie cmdlet **Disable-AzVMBlockEncryption** wyłącza szyfrowanie na maszynie wirtualnej infrastruktury jako usługi (IaaS).
To polecenie cmdlet jest obsługiwane tylko w przypadku maszyn wirtualnych systemu Windows, a nie linux.
To polecenie cmdlet instaluje na komputerze wirtualnym rozszerzenie w celu wyłączenia szyfrowania.
Jeśli parametr *Name* nie zostanie określony, zostanie utworzone rozszerzenie o nazwie domyślnej "AzureCryption for Windows VMs".
Przestroga: To polecenie cmdlet ponownie uruchamia maszynę wirtualną.

## PRZYKŁADY

### Przykład 1. Wyłączenie szyfrowania dla wszystkich woluminów na maszyny wirtualnej systemu Windows
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

To polecenie wyłącza szyfrowanie woluminów typu dla maszyny wirtualnej o nazwie MASZYNY WIRTUALNEJ002, która należy do grupy zasobów o nazwie Group001.
Parametr *VolumeType* nie jest określony, dlatego polecenie cmdlet ustawia wartość All (Wszystko).

### Przykład 2. Wyłączenie szyfrowania woluminów danych na maszyny wirtualnej systemu Windows
```
PS C:\> $ResourceGroup = "Group002"
PS C:\> $VMName = "VM004"
PS C:\> $VolumeType = "Data"
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName $ResourceGroup -VMName $VMName -VolumeType $VolumeType
```

To polecenie wyłącza szyfrowanie dla woluminów danych typu dla maszyny wirtualnej o nazwie MASZYNY WIRTUALNEJ004, która należy do grupy zasobów o nazwie Group002.

## PARAMETERS

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

### -DisableAutoUpgradeMinorVersion
Wskazuje, że to polecenie cmdlet wyłącza automatyczne uaktualnianie wersji pomocniczej rozszerzenia.

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ExtensionPublisherName
Nazwa wydawcy rozszerzenia. Określ ten parametr, aby zastąpić wartość domyślną "Microsoft.Azure.Security".

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

### -ExtensionType
Typ rozszerzenia. Określ ten parametr, aby zastąpić jego wartość domyślną "AzureUxEncryption" dla maszyn wirtualnych systemu Windows i "AzureCryptionForLinux" dla maszyn wirtualnych systemu Linux.

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

### — Wymuszanie
Wymusza uruchomienie polecenia bez pytania o potwierdzenie użytkownika.

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

### — Nazwa
Określa nazwę zasobu Azure Resource Manager (ARM) reprezentującego to rozszerzenie.
Jeśli ten parametr nie zostanie określony, to polecenie cmdlet domyślnie ma wartość "AzureCryption for Windows VMs".

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów maszyny wirtualnej.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -TypeHandlerVersion
Określa wersję rozszerzenia szyfrowania.
Jeśli nie określisz wartości dla tego parametru, zostanie użyta najnowsza wersja rozszerzenia.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NAZWA.MASZYNY.WIRTUALNEJ
Określa nazwę maszyny wirtualnej, na podstawie których to polecenie cmdlet wyłącza szyfrowanie.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### - VolumeType
Określa typ woluminów maszyn wirtualnych do wykonania operacji szyfrowania.
W przypadku maszyn wirtualnych systemu Windows prawidłowe wartości: 
- Wszystkie
- System operacyjny
- Dane.
Jeśli nie określisz wartości dla tego parametru, wartość domyślna to Wszystko.
Wyłączenie szyfrowania nie jest obecnie obsługiwane w systemie Linux.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: OS, Data, All

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
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
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -WhatIf
Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.
Polecenie cmdlet nie zostanie uruchomione.

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
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)

## DANE WEJŚCIOWE

### System.String

### System.Management.Automation.SwitchParameters

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## NOTATKI

## LINKI POKREWNE

[Get-AzVM GdyszytEncryptionStatus](./Get-AzVMDiskEncryptionStatus.md)

[Remove-AzVMCryptionExtension](./Remove-AzVMDiskEncryptionExtension.md)

[Set-AzVMCryptionExtension](./Set-AzVMDiskEncryptionExtension.md)


