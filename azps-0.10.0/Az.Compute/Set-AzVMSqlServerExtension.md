---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 1795216cbc18da2d503a1e0056d614337cd12785
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398244"
---
# Set-AzVMSqlServerExtension

## SYNOPSIS
Ustawia rozszerzenie Azure SQL Server na komputerze wirtualnym.

## SKŁADNIA

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## OPIS
Polecenie **cmdlet Set-AzVMSqlServerExtension** ustawia rozszerzenie AzureSQL Server na komputerze wirtualnym.

## PRZYKŁADY

### Przykład 1. Ustawianie ustawień automatycznego poprawiania na komputerze wirtualnym
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

Pierwsze polecenie tworzy obiekt konfiguracji przy użyciu polecenia cmdlet **New-AzureVMSqlServerAutoPatchingConfig.**
Polecenie zapisuje konfigurację w $AutoPatchingConfig zmienną.

Drugie polecenie pobiera maszynę wirtualną o nazwie VirtualMachine11 w usłudze o nazwie Service02 za pomocą Get-AzVM cmdlet.
Polecenie przekazuje ten obiekt do bieżącego polecenia cmdlet przy użyciu operatora potoku.

Bieżące polecenie cmdlet ustawia ustawienia automatycznego poprawiania w $AutoPatchingConfig dla maszyny wirtualnej.
Polecenie przekazuje maszynę wirtualną do Update-AzVM cmdlet.

### Przykład 2. Ustawianie ustawień automatycznej kopii zapasowej na komputerze wirtualnym
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

Pierwsze polecenie tworzy obiekt konfiguracji przy użyciu polecenia cmdlet **New-AzureVMSqlServerAutoBackupConfig.**
Polecenie zapisuje konfigurację w $AutoBackupConfig zmienną.

Drugie polecenie pobiera maszynę wirtualną o nazwie VirtualMachine11 w usłudze o nazwie Service02, a następnie przekazuje ją do bieżącego polecenia cmdlet.

Bieżące polecenie cmdlet ustawia ustawienia automatycznej kopii zapasowej w $AutoBackupConfig maszyny wirtualnej.
Polecenie przekazuje maszynę wirtualną do Update-AzVM cmdlet.

### Przykład 3. Wyłączenie rozszerzenia programu SQL Server na komputerze wirtualnym
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

To polecenie pobiera maszynę wirtualną o nazwie VirtualMachine08 w usłudze Service03, a następnie przekazuje ją do bieżącego polecenia cmdlet.
To polecenie wyłącza rozszerzenie maszyny wirtualnej programu SQL Server na tej maszyny wirtualnej.

### Przykład 4. Odinstalowanie rozszerzenia programu SQL Server na określonej maszyny wirtualnej
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

To polecenie pobiera maszynę wirtualną o nazwie VirtualMachine08 w usłudze Service03, a następnie przekazuje ją do bieżącego polecenia cmdlet.
Polecenie odinstalowuje rozszerzenie maszyny wirtualnej programu SQL Server na tej maszyny wirtualnej.

## PARAMETERS

### -AutoBackupSettings
Określa ustawienia automatycznej kopii zapasowej programu SQL Server.
Aby utworzyć **obiekt AutoBackupSettings,** użyj New-AzureVMSqlServerAutoBackupConfig cmdlet.

```yaml
Type: AutoBackupSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutoPatchingSettings
Określa ustawienia automatycznego poprawiania poprawek w programie SQL Server.
Aby utworzyć **obiekt AutoPatchingSettings,** użyj New-AzureVMSqlServerAutoPatchingConfig cmdlet.

```yaml
Type: AutoPatchingSettings
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -KeyVaultCredentialSettings
```yaml
Type: KeyVaultCredentialSettings
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
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Nazwa
Określa nazwę rozszerzenia programu SQL Server.

```yaml
Type: String
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
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### — Wersja
Określa wersję rozszerzenia programu SQL Server.

```yaml
Type: String
Parameter Sets: (All)
Aliases: HandlerVersion

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -NAZWA.MASZYNY.WIRTUALNEJ
Określa nazwę maszyny wirtualnej, na której to polecenie cmdlet ustawia rozszerzenie programu SQL Server.

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .

## DANE WEJŚCIOWE

### Brak
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## DANE WYJŚCIOWE

### Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse

## NOTATKI

## LINKI POKREWNE

[Get-AzVM](./Get-AzVM.md)

[Get-AzVMSqlServerExtension](./Get-AzVMSqlServerExtension.md)

[New-AzureVMSqlServerAutoPatchingConfig](./New-AzVMSqlServerAutoPatchingConfig.md)

[New-AzureVMSqlServerAutoBackupConfig](./New-AzVMSqlServerAutoBackupConfig.md)

[Remove-AzVMSqlServerExtension](./Remove-AzVMSqlServerExtension.md)

[Update-AzVM](./Update-AzVM.md)


