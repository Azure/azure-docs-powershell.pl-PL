---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: c3a146b99119ab94bf98176d202cda52e1dc5704
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93548176"
---
# <span data-ttu-id="a4459-101">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="a4459-101">Set-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="a4459-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4459-102">SYNOPSIS</span></span>
<span data-ttu-id="a4459-103">Ustawia rozszerzenie Azure SQL Server na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a4459-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4459-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4459-104">SYNTAX</span></span>

```
Set-AzureRmVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [<CommonParameters>]
```

## <span data-ttu-id="a4459-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a4459-105">DESCRIPTION</span></span>
<span data-ttu-id="a4459-106">Polecenie cmdlet **Set-AzureRmVMSqlServerExtension** ustawia rozszerzenie serwera AzureSQL na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a4459-106">The **Set-AzureRmVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="a4459-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4459-107">EXAMPLES</span></span>

### <span data-ttu-id="a4459-108">Przykład 1: Ustawianie ustawień automatycznej poprawki na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a4459-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzureRmVM
```

<span data-ttu-id="a4459-109">Pierwsze polecenie tworzy obiekt konfiguracji przy użyciu polecenia cmdlet **New-AzureVMSqlServerAutoPatchingConfig** .</span><span class="sxs-lookup"><span data-stu-id="a4459-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="a4459-110">Polecenie zapisuje konfigurację w zmiennej $AutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="a4459-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="a4459-111">Drugie polecenie pobiera maszynę wirtualną o nazwie VirtualMachine11 w usłudze o nazwie Service02 przy użyciu polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="a4459-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="a4459-112">Polecenie przekazuje ten obiekt do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="a4459-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="a4459-113">Bieżące polecenie cmdlet ustawia ustawienia automatycznej poprawki w $AutoPatchingConfig maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a4459-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="a4459-114">Polecenie przekazanie maszyny wirtualnej do Update-AzureRmVM polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4459-114">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="a4459-115">Przykład 2: Ustawianie ustawień automatycznej kopii zapasowej na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a4459-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzureRmVM
```

<span data-ttu-id="a4459-116">Pierwsze polecenie tworzy obiekt konfiguracji przy użyciu polecenia cmdlet **New-AzureVMSqlServerAutoBackupConfig** .</span><span class="sxs-lookup"><span data-stu-id="a4459-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="a4459-117">Polecenie zapisuje konfigurację w zmiennej $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="a4459-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="a4459-118">Drugie polecenie pobiera maszynę wirtualną o nazwie VirtualMachine11 w usłudze o nazwie Service02, a następnie przekazuje ją do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4459-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="a4459-119">Bieżące polecenie cmdlet ustawia ustawienia automatycznej kopii zapasowej w $AutoBackupConfig dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a4459-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="a4459-120">Polecenie przekazanie maszyny wirtualnej do Update-AzureRmVM polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4459-120">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="a4459-121">Przykład 3: wyłączanie rozszerzenia programu SQL Server na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a4459-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Disable
```

<span data-ttu-id="a4459-122">To polecenie umożliwia pobieranie maszyny wirtualnej o nazwie VirtualMachine08 na Service03, a następnie przekazanie jej do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4459-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="a4459-123">Polecenie wyłącza rozszerzenie maszyny wirtualnej programu SQL Server na tej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a4459-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="a4459-124">Przykład 4: Odinstalowywanie rozszerzenia programu SQL Server na określonej maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="a4459-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Uninstall
```

<span data-ttu-id="a4459-125">To polecenie umożliwia pobieranie maszyny wirtualnej o nazwie VirtualMachine08 na Service03, a następnie przekazanie jej do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4459-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="a4459-126">Polecenie Odinstalowuje rozszerzenie maszyny wirtualnej programu SQL Server na tej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a4459-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="a4459-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4459-127">PARAMETERS</span></span>

### <span data-ttu-id="a4459-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="a4459-128">-AutoBackupSettings</span></span>
<span data-ttu-id="a4459-129">Określa ustawienia automatycznej kopii zapasowej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a4459-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="a4459-130">Aby utworzyć obiekt **AutoBackupSettings** , użyj polecenia cmdlet New-AzureVMSqlServerAutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="a4459-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="a4459-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="a4459-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="a4459-132">Określa ustawienia automatycznej poprawki programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a4459-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="a4459-133">Aby utworzyć obiekt **AutoPatchingSettings** , użyj polecenia cmdlet New-AzureVMSqlServerAutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="a4459-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="a4459-134">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="a4459-134">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="a4459-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a4459-135">-Location</span></span>
<span data-ttu-id="a4459-136">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a4459-136">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="a4459-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a4459-137">-Name</span></span>
<span data-ttu-id="a4459-138">Określa nazwę rozszerzenia programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a4459-138">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="a4459-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a4459-139">-ResourceGroupName</span></span>
<span data-ttu-id="a4459-140">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="a4459-140">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="a4459-141">-Version</span><span class="sxs-lookup"><span data-stu-id="a4459-141">-Version</span></span>
<span data-ttu-id="a4459-142">Określa wersję rozszerzenia programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a4459-142">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="a4459-143">-VMName</span><span class="sxs-lookup"><span data-stu-id="a4459-143">-VMName</span></span>
<span data-ttu-id="a4459-144">Określa nazwę maszyny wirtualnej, na której to polecenie cmdlet ustawia rozszerzenie programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="a4459-144">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="a4459-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4459-145">CommonParameters</span></span>
<span data-ttu-id="a4459-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4459-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4459-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4459-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4459-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4459-148">INPUTS</span></span>

### <span data-ttu-id="a4459-149">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a4459-149">None</span></span>
<span data-ttu-id="a4459-150">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a4459-150">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a4459-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4459-151">OUTPUTS</span></span>

## <span data-ttu-id="a4459-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4459-152">NOTES</span></span>

## <span data-ttu-id="a4459-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4459-153">RELATED LINKS</span></span>

[<span data-ttu-id="a4459-154">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a4459-154">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="a4459-155">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="a4459-155">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="a4459-156">Nowe — AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="a4459-156">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="a4459-157">Nowe — AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="a4459-157">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="a4459-158">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="a4459-158">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="a4459-159">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="a4459-159">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


