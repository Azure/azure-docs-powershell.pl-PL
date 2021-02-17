---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 753c1de5b2f967ad321334231c77e379e11bc2ba
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196963"
---
# <span data-ttu-id="ebd07-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ebd07-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="ebd07-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ebd07-102">SYNOPSIS</span></span>
<span data-ttu-id="ebd07-103">Ustawia rozszerzenie Azure SQL Server na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="ebd07-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="ebd07-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ebd07-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ebd07-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ebd07-105">DESCRIPTION</span></span>
<span data-ttu-id="ebd07-106">Polecenie **cmdlet Set-AzVMSqlServerExtension** ustawia rozszerzenie AzureSQL Server na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="ebd07-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="ebd07-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ebd07-107">EXAMPLES</span></span>

### <span data-ttu-id="ebd07-108">Przykład 1. Ustawianie ustawień automatycznego poprawiania na komputerze wirtualnym</span><span class="sxs-lookup"><span data-stu-id="ebd07-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="ebd07-109">Pierwsze polecenie tworzy obiekt konfiguracji przy użyciu polecenia cmdlet **New-AzVMSqlServerAutoPatchingConfig.**</span><span class="sxs-lookup"><span data-stu-id="ebd07-109">The first command creates a configuration object by using the **New-AzVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="ebd07-110">Polecenie zapisuje konfigurację w $AutoPatchingConfig zmienną.</span><span class="sxs-lookup"><span data-stu-id="ebd07-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="ebd07-111">Drugie polecenie pobiera maszynę wirtualną o nazwie VirtualMachine11 w usłudze o nazwie Service02 za pomocą Get-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebd07-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="ebd07-112">Polecenie przekazuje ten obiekt do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="ebd07-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ebd07-113">Bieżące polecenie cmdlet ustawia ustawienia automatycznego poprawiania w $AutoPatchingConfig dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ebd07-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="ebd07-114">Polecenie przekazuje maszynę wirtualną do Update-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebd07-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="ebd07-115">Przykład 2. Ustawianie ustawień automatycznej kopii zapasowej na komputerze wirtualnym</span><span class="sxs-lookup"><span data-stu-id="ebd07-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="ebd07-116">Pierwsze polecenie tworzy obiekt konfiguracji przy użyciu polecenia cmdlet **New-AzVMSqlServerAutoBackupConfig.**</span><span class="sxs-lookup"><span data-stu-id="ebd07-116">The first command creates a configuration object by using the **New-AzVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="ebd07-117">Polecenie przechowuje konfigurację w $AutoBackupConfig zmienną.</span><span class="sxs-lookup"><span data-stu-id="ebd07-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="ebd07-118">Drugie polecenie pobiera maszynę wirtualną o nazwie VirtualMachine11 w usłudze o nazwie Service02, a następnie przekazuje ją do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebd07-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="ebd07-119">Bieżące polecenie cmdlet ustawia automatyczne ustawienia kopii zapasowej $AutoBackupConfig dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ebd07-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="ebd07-120">Polecenie przekazuje maszynę wirtualną do Update-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebd07-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="ebd07-121">Przykład 3. Wyłączenie rozszerzenia programu SQL Server na komputerze wirtualnym</span><span class="sxs-lookup"><span data-stu-id="ebd07-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="ebd07-122">To polecenie pobiera maszynę wirtualną o nazwie VirtualMachine08 w usłudze Service03, a następnie przekazuje ją do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebd07-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="ebd07-123">To polecenie wyłącza rozszerzenie maszyny wirtualnej programu SQL Server na tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ebd07-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="ebd07-124">Przykład 4. Odinstalowywanie rozszerzenia programu SQL Server na określonej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ebd07-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="ebd07-125">To polecenie pobiera maszynę wirtualną o nazwie VirtualMachine08 w usłudze Service03, a następnie przekazuje ją do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebd07-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="ebd07-126">Polecenie odinstalowuje rozszerzenie maszyny wirtualnej programu SQL Server na tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ebd07-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="ebd07-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ebd07-127">PARAMETERS</span></span>

### <span data-ttu-id="ebd07-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="ebd07-128">-AutoBackupSettings</span></span>
<span data-ttu-id="ebd07-129">Określa ustawienia automatycznej kopii zapasowej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ebd07-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="ebd07-130">Aby utworzyć **obiekt AutoBackupSettings,** użyj New-AzVMSqlServerAutoBackupConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebd07-130">To create an **AutoBackupSettings** object , use the New-AzVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="ebd07-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="ebd07-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="ebd07-132">Określa ustawienia automatycznego poprawiania poprawek w programie SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ebd07-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="ebd07-133">Aby utworzyć obiekt **AutoPatchingSettings,** użyj New-AzVMSqlServerAutoPatchingConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ebd07-133">To create an **AutoPatchingSettings** object , use the New-AzVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="ebd07-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ebd07-134">-DefaultProfile</span></span>
<span data-ttu-id="ebd07-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ebd07-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ebd07-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="ebd07-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="ebd07-137">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ebd07-137">-Location</span></span>
<span data-ttu-id="ebd07-138">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ebd07-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="ebd07-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ebd07-139">-Name</span></span>
<span data-ttu-id="ebd07-140">Określa nazwę rozszerzenia programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ebd07-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="ebd07-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ebd07-141">-ResourceGroupName</span></span>
<span data-ttu-id="ebd07-142">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ebd07-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ebd07-143">— Wersja</span><span class="sxs-lookup"><span data-stu-id="ebd07-143">-Version</span></span>
<span data-ttu-id="ebd07-144">Określa wersję rozszerzenia programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ebd07-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="ebd07-145">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="ebd07-145">-VMName</span></span>
<span data-ttu-id="ebd07-146">Określa nazwę maszyny wirtualnej, na której to polecenie cmdlet ustawia rozszerzenie programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ebd07-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="ebd07-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ebd07-147">CommonParameters</span></span>
<span data-ttu-id="ebd07-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ebd07-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ebd07-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ebd07-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ebd07-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ebd07-150">INPUTS</span></span>

### <span data-ttu-id="ebd07-151">System.String</span><span class="sxs-lookup"><span data-stu-id="ebd07-151">System.String</span></span>

### <span data-ttu-id="ebd07-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="ebd07-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="ebd07-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="ebd07-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="ebd07-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="ebd07-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="ebd07-155">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ebd07-155">OUTPUTS</span></span>

### <span data-ttu-id="ebd07-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="ebd07-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="ebd07-157">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ebd07-157">NOTES</span></span>

## <span data-ttu-id="ebd07-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ebd07-158">RELATED LINKS</span></span>

[<span data-ttu-id="ebd07-159">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="ebd07-159">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="ebd07-160">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ebd07-160">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="ebd07-161">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="ebd07-161">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="ebd07-162">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="ebd07-162">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="ebd07-163">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ebd07-163">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="ebd07-164">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="ebd07-164">Update-AzVM</span></span>](./Update-AzVM.md)


