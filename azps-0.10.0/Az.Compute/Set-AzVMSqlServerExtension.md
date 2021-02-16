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
# <span data-ttu-id="8ec9f-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8ec9f-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="8ec9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ec9f-102">SYNOPSIS</span></span>
<span data-ttu-id="8ec9f-103">Ustawia rozszerzenie Azure SQL Server na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="8ec9f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8ec9f-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8ec9f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8ec9f-105">DESCRIPTION</span></span>
<span data-ttu-id="8ec9f-106">Polecenie **cmdlet Set-AzVMSqlServerExtension** ustawia rozszerzenie AzureSQL Server na komputerze wirtualnym.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="8ec9f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8ec9f-107">EXAMPLES</span></span>

### <span data-ttu-id="8ec9f-108">Przykład 1. Ustawianie ustawień automatycznego poprawiania na komputerze wirtualnym</span><span class="sxs-lookup"><span data-stu-id="8ec9f-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="8ec9f-109">Pierwsze polecenie tworzy obiekt konfiguracji przy użyciu polecenia cmdlet **New-AzureVMSqlServerAutoPatchingConfig.**</span><span class="sxs-lookup"><span data-stu-id="8ec9f-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="8ec9f-110">Polecenie zapisuje konfigurację w $AutoPatchingConfig zmienną.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="8ec9f-111">Drugie polecenie pobiera maszynę wirtualną o nazwie VirtualMachine11 w usłudze o nazwie Service02 za pomocą Get-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="8ec9f-112">Polecenie przekazuje ten obiekt do bieżącego polecenia cmdlet przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="8ec9f-113">Bieżące polecenie cmdlet ustawia ustawienia automatycznego poprawiania w $AutoPatchingConfig dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="8ec9f-114">Polecenie przekazuje maszynę wirtualną do Update-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="8ec9f-115">Przykład 2. Ustawianie ustawień automatycznej kopii zapasowej na komputerze wirtualnym</span><span class="sxs-lookup"><span data-stu-id="8ec9f-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="8ec9f-116">Pierwsze polecenie tworzy obiekt konfiguracji przy użyciu polecenia cmdlet **New-AzureVMSqlServerAutoBackupConfig.**</span><span class="sxs-lookup"><span data-stu-id="8ec9f-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="8ec9f-117">Polecenie zapisuje konfigurację w $AutoBackupConfig zmienną.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="8ec9f-118">Drugie polecenie pobiera maszynę wirtualną o nazwie VirtualMachine11 w usłudze o nazwie Service02, a następnie przekazuje ją do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="8ec9f-119">Bieżące polecenie cmdlet ustawia ustawienia automatycznej kopii zapasowej w $AutoBackupConfig maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="8ec9f-120">Polecenie przekazuje maszynę wirtualną do Update-AzVM cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="8ec9f-121">Przykład 3. Wyłączenie rozszerzenia programu SQL Server na komputerze wirtualnym</span><span class="sxs-lookup"><span data-stu-id="8ec9f-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="8ec9f-122">To polecenie pobiera maszynę wirtualną o nazwie VirtualMachine08 w usłudze Service03, a następnie przekazuje ją do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="8ec9f-123">To polecenie wyłącza rozszerzenie maszyny wirtualnej programu SQL Server na tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="8ec9f-124">Przykład 4. Odinstalowanie rozszerzenia programu SQL Server na określonej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="8ec9f-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="8ec9f-125">To polecenie pobiera maszynę wirtualną o nazwie VirtualMachine08 w usłudze Service03, a następnie przekazuje ją do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="8ec9f-126">Polecenie odinstalowuje rozszerzenie maszyny wirtualnej programu SQL Server na tej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="8ec9f-127">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ec9f-127">PARAMETERS</span></span>

### <span data-ttu-id="8ec9f-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="8ec9f-128">-AutoBackupSettings</span></span>
<span data-ttu-id="8ec9f-129">Określa ustawienia automatycznej kopii zapasowej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="8ec9f-130">Aby utworzyć **obiekt AutoBackupSettings,** użyj New-AzureVMSqlServerAutoBackupConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="8ec9f-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="8ec9f-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="8ec9f-132">Określa ustawienia automatycznego poprawiania poprawek w programie SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="8ec9f-133">Aby utworzyć **obiekt AutoPatchingSettings,** użyj New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="8ec9f-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ec9f-134">-DefaultProfile</span></span>
<span data-ttu-id="8ec9f-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8ec9f-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="8ec9f-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="8ec9f-137">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="8ec9f-137">-Location</span></span>
<span data-ttu-id="8ec9f-138">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="8ec9f-139">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8ec9f-139">-Name</span></span>
<span data-ttu-id="8ec9f-140">Określa nazwę rozszerzenia programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="8ec9f-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ec9f-141">-ResourceGroupName</span></span>
<span data-ttu-id="8ec9f-142">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8ec9f-143">— Wersja</span><span class="sxs-lookup"><span data-stu-id="8ec9f-143">-Version</span></span>
<span data-ttu-id="8ec9f-144">Określa wersję rozszerzenia programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="8ec9f-145">-NAZWA.MASZYNY.WIRTUALNEJ</span><span class="sxs-lookup"><span data-stu-id="8ec9f-145">-VMName</span></span>
<span data-ttu-id="8ec9f-146">Określa nazwę maszyny wirtualnej, na której to polecenie cmdlet ustawia rozszerzenie programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="8ec9f-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ec9f-147">CommonParameters</span></span>
<span data-ttu-id="8ec9f-148">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ec9f-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ec9f-149">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ec9f-150">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ec9f-150">INPUTS</span></span>

### <span data-ttu-id="8ec9f-151">Brak</span><span class="sxs-lookup"><span data-stu-id="8ec9f-151">None</span></span>
<span data-ttu-id="8ec9f-152">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="8ec9f-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="8ec9f-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ec9f-153">OUTPUTS</span></span>

### <span data-ttu-id="8ec9f-154">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="8ec9f-154">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="8ec9f-155">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8ec9f-155">NOTES</span></span>

## <span data-ttu-id="8ec9f-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ec9f-156">RELATED LINKS</span></span>

[<span data-ttu-id="8ec9f-157">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="8ec9f-157">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="8ec9f-158">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8ec9f-158">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="8ec9f-159">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="8ec9f-159">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="8ec9f-160">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="8ec9f-160">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="8ec9f-161">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="8ec9f-161">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="8ec9f-162">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="8ec9f-162">Update-AzVM</span></span>](./Update-AzVM.md)


