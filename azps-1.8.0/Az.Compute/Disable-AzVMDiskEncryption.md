---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 979E956B-4C74-426E-A617-E50C4EBC8A20
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/disable-azvmdiskencryption
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Disable-AzVMDiskEncryption.md
ms.openlocfilehash: 6720f4eb323d0050cacd9656fc14559da24ecf81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710333"
---
# Disable-AzVMDiskEncryption

## STRESZCZENIe
Wyłącza szyfrowanie na maszynie wirtualnej IaaS.

## POLECENIA

```
Disable-AzVMDiskEncryption [-ResourceGroupName] <String> [-VMName] <String> [[-VolumeType] <String>]
 [[-Name] <String>] [[-TypeHandlerVersion] <String>] [-Force] [-DisableAutoUpgradeMinorVersion]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **disable-AzVMDiskEncryption** wyłącza szyfrowanie infrastruktury jako maszynę wirtualną usługi (IaaS).
To polecenie cmdlet jest obsługiwane tylko na maszynach wirtualnych systemu Windows, a nie na maszynach wirtualnych Linux.
To polecenie cmdlet powoduje zainstalowanie rozszerzenia na maszynie wirtualnej w celu wyłączenia szyfrowania.
Jeśli parametr *name* nie jest określony, zostanie utworzona rozszerzenie z nazwą domyślną "AzureDiskEncryption for Windows VMS".
Uwaga: to polecenie cmdlet powoduje ponowne uruchomienie maszyny wirtualnej.

## Przykłady

### Przykład 1: wyłączanie szyfrowania dla wszystkich woluminów na maszynie wirtualnej systemu Windows
```
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group001" -VMName "VM002"
```

To polecenie wyłącza szyfrowanie woluminów typu all dla maszyny wirtualnej o nazwie VM002 należącej do grupy zasobów o nazwie Group001.
Ponieważ parametr *volumetype* nie jest określony, polecenie cmdlet ustawia wartość All (wszystko).

### Przykład 2: wyłączanie szyfrowania dla woluminów danych na maszynie wirtualnej systemu Windows
```
PS C:\> $ResourceGroup = "Group002";
PS C:\> $VMName = "VM004";
PS C:\> Disable-AzVMDiskEncryption -ResourceGroupName "Group002" -VMName "VM004" -VolumeType "Data"
```

To polecenie wyłącza szyfrowanie woluminów typu dane dla maszyny wirtualnej o nazwie VM004 należącej do grupy zasobów o nazwie Group002.

## PARAMETRÓW

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

### -DisableAutoUpgradeMinorVersion
Wskazuje, że to polecenie cmdlet wyłącza automatyczne uaktualnianie pomocniczej wersji rozszerzenia.

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
Nazwa wydawcy rozszerzenia. Ten parametr można określić tylko w celu zastąpienia wartości domyślnej "Microsoft. Azure. Security".

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
Typ rozszerzenia. Określ ten parametr, aby zastąpić swoją domyślną wartość "AzureDiskEncryption" dla maszyn wirtualnych systemu Windows i "AzureDiskEncryptionForLinux" dla maszyn wirtualnych Linux.

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

### -Name (nazwa)
Specifes nazwę zasobu Menedżera zasobów platformy Azure (ARM), który reprezentuje rozszerzenie.
Jeśli ten parametr nie jest określony, to polecenie cmdlet domyślnie przyjmuje wartość "AzureDiskEncryption for Windows VMs".

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
Jeśli nie określisz wartości dla tego parametru, zostanie wykorzystana Najnowsza wersja rozszerzenia.

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

### -VMName
Określa nazwę maszyny wirtualnej, w której to polecenie cmdlet wyłącza szyfrowanie.

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

### -Volumetype
Określa typ woluminów maszyny wirtualnej, które mają wykonać operację szyfrowania.
W przypadku maszyn wirtualnych systemu Windows prawidłowymi wartościami są: 
- Cały
- OPERACYJNYM
- Danymi.
Jeśli nie określisz wartości dla tego parametru, wartość domyślna to All (wszystko).
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
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### System. String

### System. Management. Automation. SwitchParameter

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse

## INFORMACYJN

## LINKI POKREWNE

[Get-AzVMDiskEncryptionStatus](./Get-AzVMDiskEncryptionStatus.md)

[Remove-AzVMDiskEncryptionExtension](./Remove-AzVMDiskEncryptionExtension.md)

[Set-AzVMDiskEncryptionExtension](./Set-AzVMDiskEncryptionExtension.md)


