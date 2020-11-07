---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: c23a13cbb50e6826d865e24abda52a9fc049b949
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706163"
---
# Set-AzVMSqlServerExtension

## STRESZCZENIe
Ustawia rozszerzenie Azure SQL Server na maszynie wirtualnej.

## POLECENIA

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Set-AzVMSqlServerExtension** ustawia rozszerzenie serwera AzureSQL na maszynie wirtualnej.

## Przykłady

### Przykład 1: Ustawianie ustawień automatycznej poprawki na maszynie wirtualnej
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

Pierwsze polecenie tworzy obiekt konfiguracji przy użyciu polecenia cmdlet **New-AzVMSqlServerAutoPatchingConfig** .
Polecenie zapisuje konfigurację w zmiennej $AutoPatchingConfig.
Drugie polecenie pobiera maszynę wirtualną o nazwie VirtualMachine11 w usłudze o nazwie Service02 przy użyciu polecenia cmdlet Get-AzVM.
Polecenie przekazuje ten obiekt do bieżącego polecenia cmdlet za pomocą operatora potoku.
Bieżące polecenie cmdlet ustawia ustawienia automatycznej poprawki w $AutoPatchingConfig maszyny wirtualnej.
Polecenie przekazanie maszyny wirtualnej do Update-AzVM polecenia cmdlet.

### Przykład 2: Ustawianie ustawień automatycznej kopii zapasowej na maszynie wirtualnej
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

Pierwsze polecenie tworzy obiekt konfiguracji przy użyciu polecenia cmdlet **New-AzVMSqlServerAutoBackupConfig** .
Polecenie zapisuje konfigurację w zmiennej $AutoBackupConfig.
Drugie polecenie pobiera maszynę wirtualną o nazwie VirtualMachine11 w usłudze o nazwie Service02, a następnie przekazuje ją do bieżącego polecenia cmdlet.
Bieżące polecenie cmdlet ustawia ustawienia automatycznej kopii zapasowej w $AutoBackupConfig dla maszyny wirtualnej.
Polecenie przekazanie maszyny wirtualnej do Update-AzVM polecenia cmdlet.

### Przykład 3: wyłączanie rozszerzenia programu SQL Server na maszynie wirtualnej
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

To polecenie umożliwia pobieranie maszyny wirtualnej o nazwie VirtualMachine08 na Service03, a następnie przekazanie jej do bieżącego polecenia cmdlet.
Polecenie wyłącza rozszerzenie maszyny wirtualnej programu SQL Server na tej maszynie wirtualnej.

### Przykład 4: Odinstalowywanie rozszerzenia programu SQL Server na określonej maszynie wirtualnej
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

To polecenie umożliwia pobieranie maszyny wirtualnej o nazwie VirtualMachine08 na Service03, a następnie przekazanie jej do bieżącego polecenia cmdlet.
Polecenie Odinstalowuje rozszerzenie maszyny wirtualnej programu SQL Server na tej maszynie wirtualnej.

## PARAMETRÓW

### -AutoBackupSettings
Określa ustawienia automatycznej kopii zapasowej programu SQL Server.
Aby utworzyć obiekt **AutoBackupSettings** , użyj polecenia cmdlet New-AzVMSqlServerAutoBackupConfig.

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoPatchingSettings
Określa ustawienia automatycznej poprawki programu SQL Server.
Aby utworzyć obiekt **AutoPatchingSettings** , użyj polecenia cmdlet New-AzVMSqlServerAutoPatchingConfig.

```yaml
Type: Microsoft.Azure.Commands.Compute.AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
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

### -KeyVaultCredentialSettings
```yaml
Type: Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Lokalizacja
Określa lokalizację maszyny wirtualnej.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Name (nazwa)
Określa nazwę rozszerzenia programu SQL Server.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
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
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Version
Określa wersję rozszerzenia programu SQL Server.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VMName
Określa nazwę maszyny wirtualnej, na której to polecenie cmdlet ustawia rozszerzenie programu SQL Server.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).

## WEJŚCIOWE

### System. String

### Microsoft. Azure. Commands. COMPUTE. AutoPatchingSettings

### Microsoft. Azure. Commands. COMPUTE. AutoBackupSettings

### Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse

## INFORMACYJN

## LINKI POKREWNE

[Get-AzVM](./Get-AzVM.md)

[Get-AzVMSqlServerExtension](./Get-AzVMSqlServerExtension.md)

[Nowe — AzVMSqlServerAutoPatchingConfig](./New-AzVMSqlServerAutoPatchingConfig.md)

[Nowe — AzVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Remove-AzVMSqlServerExtension](./Remove-AzVMSqlServerExtension.md)

[Update-AzVM](./Update-AzVM.md)


