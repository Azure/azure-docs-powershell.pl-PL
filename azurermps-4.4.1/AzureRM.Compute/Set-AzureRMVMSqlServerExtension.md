---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: C650E465-7CDE-47F8-B85A-8FA3E1756FAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: a89a2fc342bf1a3ed6e311057f55bb83c80be210
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528242"
---
# <span data-ttu-id="5a4f7-101">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5a4f7-101">Set-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="5a4f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5a4f7-102">SYNOPSIS</span></span>
<span data-ttu-id="5a4f7-103">Ustawia rozszerzenie Azure SQL Server na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5a4f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5a4f7-104">SYNTAX</span></span>

```
Set-AzureRmVMSqlServerExtension [[-Version] <String>] [-ResourceGroupName] <String> [-VMName] <String>
 [[-Name] <String>] [[-AutoPatchingSettings] <AutoPatchingSettings>]
 [[-AutoBackupSettings] <AutoBackupSettings>] [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>]
 [[-Location] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a4f7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5a4f7-105">DESCRIPTION</span></span>
<span data-ttu-id="5a4f7-106">Polecenie cmdlet **Set-AzureRmVMSqlServerExtension** ustawia rozszerzenie serwera AzureSQL na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-106">The **Set-AzureRmVMSqlServerExtension** cmdlet sets the AzureSQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="5a4f7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5a4f7-107">EXAMPLES</span></span>

### <span data-ttu-id="5a4f7-108">Przykład 1: Ustawianie ustawień automatycznej poprawki na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5a4f7-108">Example 1: Set automatic patching settings on a virtual machine</span></span>
```
PS C:\> $AutoPatchingConfig = New-AzureVMSqlServerAutoPatchingConfig -Enable -DayOfWeek "Thursday" -MaintenanceWindowStartingHour 11 -MaintenanceWindowDuration 120 -PatchCategory "Important"
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoPatchingSettings $AutoPatchingConfig | Update-AzureRmVM
```

<span data-ttu-id="5a4f7-109">Pierwsze polecenie tworzy obiekt konfiguracji przy użyciu polecenia cmdlet **New-AzureVMSqlServerAutoPatchingConfig** .</span><span class="sxs-lookup"><span data-stu-id="5a4f7-109">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoPatchingConfig** cmdlet.</span></span>
<span data-ttu-id="5a4f7-110">Polecenie zapisuje konfigurację w zmiennej $AutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-110">The command stores the configuration in the $AutoPatchingConfig variable.</span></span>

<span data-ttu-id="5a4f7-111">Drugie polecenie pobiera maszynę wirtualną o nazwie VirtualMachine11 w usłudze o nazwie Service02 przy użyciu polecenia cmdlet Get-AzureRmVM.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-111">The second command gets the virtual machine named VirtualMachine11 on the service named Service02 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="5a4f7-112">Polecenie przekazuje ten obiekt do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-112">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="5a4f7-113">Bieżące polecenie cmdlet ustawia ustawienia automatycznej poprawki w $AutoPatchingConfig maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-113">The current cmdlet sets the automatic patching settings in $AutoPatchingConfig for the virtual machine.</span></span>
<span data-ttu-id="5a4f7-114">Polecenie przekazanie maszyny wirtualnej do Update-AzureRmVM polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-114">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="5a4f7-115">Przykład 2: Ustawianie ustawień automatycznej kopii zapasowej na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5a4f7-115">Example 2: Set automatic backup settings on a virtual machine</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
PS C:\> Get-AzureRmVM -ServiceName "Service02" -Name "VirtualMachine11" | Set-AzureRmVMSqlServerExtension -AutoBackupSettings $AutoBackupConfig | Update-AzureRmVM
```

<span data-ttu-id="5a4f7-116">Pierwsze polecenie tworzy obiekt konfiguracji przy użyciu polecenia cmdlet **New-AzureVMSqlServerAutoBackupConfig** .</span><span class="sxs-lookup"><span data-stu-id="5a4f7-116">The first command creates a configuration object by using the **New-AzureVMSqlServerAutoBackupConfig** cmdlet.</span></span>
<span data-ttu-id="5a4f7-117">Polecenie zapisuje konfigurację w zmiennej $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-117">The command stores the configuration in the $AutoBackupConfig variable.</span></span>

<span data-ttu-id="5a4f7-118">Drugie polecenie pobiera maszynę wirtualną o nazwie VirtualMachine11 w usłudze o nazwie Service02, a następnie przekazuje ją do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-118">The second command gets the virtual machine named VirtualMachine11 on the service named Service02, and then passes it to the current cmdlet.</span></span>

<span data-ttu-id="5a4f7-119">Bieżące polecenie cmdlet ustawia ustawienia automatycznej kopii zapasowej w $AutoBackupConfig dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-119">The current cmdlet sets the automatic backup settings in $AutoBackupConfig for the virtual machine.</span></span>
<span data-ttu-id="5a4f7-120">Polecenie przekazanie maszyny wirtualnej do Update-AzureRmVM polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-120">The command passes the virtual machine to the Update-AzureRmVM cmdlet.</span></span>

### <span data-ttu-id="5a4f7-121">Przykład 3: wyłączanie rozszerzenia programu SQL Server na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5a4f7-121">Example 3: Disable a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Disable
```

<span data-ttu-id="5a4f7-122">To polecenie umożliwia pobieranie maszyny wirtualnej o nazwie VirtualMachine08 na Service03, a następnie przekazanie jej do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-122">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5a4f7-123">Polecenie wyłącza rozszerzenie maszyny wirtualnej programu SQL Server na tej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-123">The command disables SQL Server virtual machine extension on that virtual machine.</span></span>

### <span data-ttu-id="5a4f7-124">Przykład 4: Odinstalowywanie rozszerzenia programu SQL Server na określonej maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="5a4f7-124">Example 4: Uninstall a SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service03" -Name "VirtualMachine08" | Set-AzureRmVMSqlServerExtension -Uninstall
```

<span data-ttu-id="5a4f7-125">To polecenie umożliwia pobieranie maszyny wirtualnej o nazwie VirtualMachine08 na Service03, a następnie przekazanie jej do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-125">This command gets a virtual machine named VirtualMachine08 on Service03, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="5a4f7-126">Polecenie Odinstalowuje rozszerzenie maszyny wirtualnej programu SQL Server na tej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-126">The command uninstalls a SQL Server virtual machine extension on that virtual machine.</span></span>

## <span data-ttu-id="5a4f7-127">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5a4f7-127">PARAMETERS</span></span>

### <span data-ttu-id="5a4f7-128">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="5a4f7-128">-AutoBackupSettings</span></span>
<span data-ttu-id="5a4f7-129">Określa ustawienia automatycznej kopii zapasowej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-129">Specifies the automatic SQL Server backup settings.</span></span>
<span data-ttu-id="5a4f7-130">Aby utworzyć obiekt **AutoBackupSettings** , użyj polecenia cmdlet New-AzureVMSqlServerAutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-130">To create an **AutoBackupSettings** object , use the New-AzureVMSqlServerAutoBackupConfig cmdlet.</span></span>

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

### <span data-ttu-id="5a4f7-131">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="5a4f7-131">-AutoPatchingSettings</span></span>
<span data-ttu-id="5a4f7-132">Określa ustawienia automatycznej poprawki programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-132">Specifies the automatic SQL Server patching settings.</span></span>
<span data-ttu-id="5a4f7-133">Aby utworzyć obiekt **AutoPatchingSettings** , użyj polecenia cmdlet New-AzureVMSqlServerAutoPatchingConfig.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-133">To create an **AutoPatchingSettings** object , use the New-AzureVMSqlServerAutoPatchingConfig cmdlet.</span></span>

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

### <span data-ttu-id="5a4f7-134">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a4f7-134">-DefaultProfile</span></span>
<span data-ttu-id="5a4f7-135">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-135">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a4f7-136">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="5a4f7-136">-KeyVaultCredentialSettings</span></span>
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

### <span data-ttu-id="5a4f7-137">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5a4f7-137">-Location</span></span>
<span data-ttu-id="5a4f7-138">Określa lokalizację maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-138">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="5a4f7-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5a4f7-139">-Name</span></span>
<span data-ttu-id="5a4f7-140">Określa nazwę rozszerzenia programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-140">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="5a4f7-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a4f7-141">-ResourceGroupName</span></span>
<span data-ttu-id="5a4f7-142">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-142">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="5a4f7-143">-Version</span><span class="sxs-lookup"><span data-stu-id="5a4f7-143">-Version</span></span>
<span data-ttu-id="5a4f7-144">Określa wersję rozszerzenia programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-144">Specifies the version of the SQL Server extension.</span></span>

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

### <span data-ttu-id="5a4f7-145">-VMName</span><span class="sxs-lookup"><span data-stu-id="5a4f7-145">-VMName</span></span>
<span data-ttu-id="5a4f7-146">Określa nazwę maszyny wirtualnej, na której to polecenie cmdlet ustawia rozszerzenie programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-146">Specifies the name of the virtual machine on which this cmdlet sets the SQL Server extension.</span></span>

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

### <span data-ttu-id="5a4f7-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a4f7-147">CommonParameters</span></span>
<span data-ttu-id="5a4f7-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5a4f7-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a4f7-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5a4f7-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a4f7-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5a4f7-150">INPUTS</span></span>

## <span data-ttu-id="5a4f7-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5a4f7-151">OUTPUTS</span></span>

## <span data-ttu-id="5a4f7-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5a4f7-152">NOTES</span></span>

## <span data-ttu-id="5a4f7-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5a4f7-153">RELATED LINKS</span></span>

[<span data-ttu-id="5a4f7-154">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5a4f7-154">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="5a4f7-155">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5a4f7-155">Get-AzureRmVMSqlServerExtension</span></span>](./Get-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="5a4f7-156">Nowe — AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="5a4f7-156">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="5a4f7-157">Nowe — AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="5a4f7-157">New-AzureVMSqlServerAutoBackupConfig</span></span>](./New-AzureVMSqlServerAutoBackupConfig.md)

[<span data-ttu-id="5a4f7-158">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5a4f7-158">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="5a4f7-159">Update-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="5a4f7-159">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


