---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMSqlServerExtension.md
ms.openlocfilehash: 753c1de5b2f967ad321334231c77e379e11bc2ba
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062860"
---
# <span data-ttu-id="5c5f8-101">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5c5f8-101">Set-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="5c5f8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5c5f8-102">SYNOPSIS</span></span>
<span data-ttu-id="5c5f8-103">Ustawia rozszerzenie Azure SQL Server na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="5c5f8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5c5f8-104">SYNTAX</span></span>

```
Set-AzVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5c5f8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5c5f8-105">DESCRIPTION</span></span>
<span data-ttu-id="5c5f8-106">Polecenie cmdlet **Set-AzVMSqlServerExtension** ustawia rozszerzenie serwera AzureSQL na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-106">The **Set-AzVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="5c5f8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5c5f8-107">EXAMPLES</span></span>

### <span data-ttu-id="5c5f8-108">Przykład 1: Ustawianie ustawień automatycznej poprawki na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5c5f8-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzVM
```

<span data-ttu-id="5c5f8-109">Pierwsze polecenie tworzy obiekt konfiguracji przy użyciu polecenia cmdlet **New-AzVMSqlServerAutoPatchingConfig** .</span><span class="sxs-lookup"><span data-stu-id="5c5f8-109">The first command creates a configuration object by using the **New-AzVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="5c5f8-110">Polecenie zapisuje konfigurację w zmiennej $AutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>
<span data-ttu-id="5c5f8-111">Drugie polecenie pobiera maszynę wirtualną o nazwie VirtualMachine11 w usłudze o nazwie Service02 przy użyciu polecenia cmdlet Get-AzVM.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="5c5f8-112">Polecenie przekazuje ten obiekt do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="5c5f8-113">Bieżące polecenie cmdlet ustawia ustawienia automatycznej poprawki w $AutoPatchingConfig maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="5c5f8-114">Polecenie przekazanie maszyny wirtualnej do Update-AzVM polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-114">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="5c5f8-115">Przykład 2: Ustawianie ustawień automatycznej kopii zapasowej na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5c5f8-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzVM
```

<span data-ttu-id="5c5f8-116">Pierwsze polecenie tworzy obiekt konfiguracji przy użyciu polecenia cmdlet **New-AzVMSqlServerAutoBackupConfig** .</span><span class="sxs-lookup"><span data-stu-id="5c5f8-116">The first command creates a configuration object by using the **New-AzVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="5c5f8-117">Polecenie zapisuje konfigurację w zmiennej $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="5c5f8-118">Drugie polecenie pobiera maszynę wirtualną o nazwie VirtualMachine11 w usłudze o nazwie Service02, a następnie przekazuje ją do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5c5f8-119">Bieżące polecenie cmdlet ustawia ustawienia automatycznej kopii zapasowej w $AutoBackupConfig dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="5c5f8-120">Polecenie przekazanie maszyny wirtualnej do Update-AzVM polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-120">The command passes the virtual machine to the Update-AzVM cmdlet.</span></span>

### <span data-ttu-id="5c5f8-121">Przykład 3: wyłączanie rozszerzenia programu SQL Server na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5c5f8-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Disable
```

<span data-ttu-id="5c5f8-122">To polecenie umożliwia pobieranie maszyny wirtualnej o nazwie VirtualMachine08 na Service03, a następnie przekazanie jej do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5c5f8-123">Polecenie wyłącza rozszerzenie maszyny wirtualnej programu SQL Server na tej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="5c5f8-124">Przykład 4: Odinstalowywanie rozszerzenia programu SQL Server na określonej maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5c5f8-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzVMSqlServerExtension -Uninstall
```

<span data-ttu-id="5c5f8-125">To polecenie umożliwia pobieranie maszyny wirtualnej o nazwie VirtualMachine08 na Service03, a następnie przekazanie jej do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5c5f8-126">Polecenie Odinstalowuje rozszerzenie maszyny wirtualnej programu SQL Server na tej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="5c5f8-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5c5f8-127">PARAMETERS</span></span>

### <span data-ttu-id="5c5f8-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="5c5f8-128">-AutoBackupSettings</span></span>
<span data-ttu-id="5c5f8-129">Określa ustawienia automatycznej kopii zapasowej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="5c5f8-130">Aby utworzyć obiekt **AutoBackupSettings** , użyj polecenia cmdlet New-AzVMSqlServerAutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-130">To create an **AutoBackupSettings** object , use the New-AzVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="5c5f8-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="5c5f8-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="5c5f8-132">Określa ustawienia automatycznej poprawki programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="5c5f8-133">Aby utworzyć obiekt **AutoPatchingSettings** , użyj polecenia cmdlet New-AzVMSqlServerAutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-133">To create an **AutoPatchingSettings** object , use the New-AzVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="5c5f8-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c5f8-134">-DefaultProfile</span></span>
<span data-ttu-id="5c5f8-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c5f8-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="5c5f8-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="5c5f8-137">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5c5f8-137">-Location</span></span>
<span data-ttu-id="5c5f8-138">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="5c5f8-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5c5f8-139">-Name</span></span>
<span data-ttu-id="5c5f8-140">Określa nazwę rozszerzenia programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="5c5f8-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c5f8-141">-ResourceGroupName</span></span>
<span data-ttu-id="5c5f8-142">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5c5f8-143">-Version</span><span class="sxs-lookup"><span data-stu-id="5c5f8-143">-Version</span></span>
<span data-ttu-id="5c5f8-144">Określa wersję rozszerzenia programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="5c5f8-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="5c5f8-145">-VMName</span></span>
<span data-ttu-id="5c5f8-146">Określa nazwę maszyny wirtualnej, na której to polecenie cmdlet ustawia rozszerzenie programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="5c5f8-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c5f8-147">CommonParameters</span></span>
<span data-ttu-id="5c5f8-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c5f8-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c5f8-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5c5f8-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c5f8-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5c5f8-150">INPUTS</span></span>

### <span data-ttu-id="5c5f8-151">System. String</span><span class="sxs-lookup"><span data-stu-id="5c5f8-151">System.String</span></span>

### <span data-ttu-id="5c5f8-152">Microsoft. Azure. Commands. COMPUTE. AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="5c5f8-152">Microsoft.Azure.Commands.Compute.AutoPatchingSettings</span></span>

### <span data-ttu-id="5c5f8-153">Microsoft. Azure. Commands. COMPUTE. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="5c5f8-153">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

### <span data-ttu-id="5c5f8-154">Microsoft. Azure. Commands. COMPUTE. KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="5c5f8-154">Microsoft.Azure.Commands.Compute.KeyVaultCredentialSettings</span></span>

## <span data-ttu-id="5c5f8-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5c5f8-155">OUTPUTS</span></span>

### <span data-ttu-id="5c5f8-156">Microsoft. Azure. Commands. COMPUTE. models. PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5c5f8-156">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5c5f8-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5c5f8-157">NOTES</span></span>

## <span data-ttu-id="5c5f8-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5c5f8-158">RELATED LINKS</span></span>

[<span data-ttu-id="5c5f8-159">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="5c5f8-159">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="5c5f8-160">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5c5f8-160">Get-AzVMSqlServerExtension</span></span>](./Get-AzVMSqlServerExtension.md)

[<span data-ttu-id="5c5f8-161">Nowe — AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="5c5f8-161">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="5c5f8-162">Nowe — AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="5c5f8-162">New-AzVMSqlServerAutoBackupConfig</span></span>](./New-AzVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="5c5f8-163">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5c5f8-163">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="5c5f8-164">Update-AzVM</span><span class="sxs-lookup"><span data-stu-id="5c5f8-164">Update-AzVM</span></span>](./Update-AzVM.md)


