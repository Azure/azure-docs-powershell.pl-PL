---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 56C7B6F5-C2AC-4C5A-8930-645374694CC3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 053bb1bfb31b90a91d69e50b77ac6411321014f0
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054756"
---
# <span data-ttu-id="e33f2-101">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e33f2-101">Set-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="e33f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e33f2-102">SYNOPSIS</span></span>
<span data-ttu-id="e33f2-103">Ustawia rozszerzenie Azure SQL Server na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e33f2-103">Sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="e33f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e33f2-104">SYNTAX</span></span>

### <span data-ttu-id="e33f2-105">EnableSqlServerExtension (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e33f2-105">EnableSqlServerExtension (Default)</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>]
 [[-AutoPatchingSettings] <AutoPatchingSettings>] [[-AutoBackupSettings] <AutoBackupSettings>]
 [[-KeyVaultCredentialSettings] <KeyVaultCredentialSettings>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e33f2-106">DisableSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e33f2-106">DisableSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="e33f2-107">UninstallSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e33f2-107">UninstallSqlServerExtension</span></span>
```
Set-AzureVMSqlServerExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e33f2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e33f2-108">DESCRIPTION</span></span>
<span data-ttu-id="e33f2-109">Polecenie cmdlet **Set-AzureVMSqlServerExtension** ustawia rozszerzenie Azure SQL Server na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e33f2-109">The **Set-AzureVMSqlServerExtension** cmdlet sets the Azure SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="e33f2-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e33f2-110">EXAMPLES</span></span>

### <span data-ttu-id="e33f2-111">Przykład 1: ustawianie automatycznego poprawiania ustawień na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e33f2-111">Example 1: Set auto-patching settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoPatchingSettings $APS | Update-AzureVM
```

<span data-ttu-id="e33f2-112">To polecenie ustawia ustawienia automatycznej poprawki na maszynie wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e33f2-112">This command sets auto-patching settings on an Azure virtual machine.</span></span>

### <span data-ttu-id="e33f2-113">Przykład 2: Ustawianie ustawień funkcji autouzupełniania kopii zapasowych na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e33f2-113">Example 2: Set auto-backup settings on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "ServiceName" -Name "VMName" | Set-AzureVMSqlServerExtension -AutoBackupSettings $ABS | Update-AzureVM
```

<span data-ttu-id="e33f2-114">To polecenie ustawia ustawienia autokopii zapasowej na maszynie wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e33f2-114">This command sets auto-backup settings on Azure virtual machine.</span></span>

### <span data-ttu-id="e33f2-115">Przykład 3: wyłączanie rozszerzenia programu SQL Server na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e33f2-115">Example 3: Disable an SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Disable
```

<span data-ttu-id="e33f2-116">To polecenie wyłącza rozszerzenie maszyny wirtualnej programu SQL Server na danej maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e33f2-116">This command disables SQL Server virtual machine extension on a given virtual machine.</span></span>

### <span data-ttu-id="e33f2-117">Przykład 4: Odinstalowywanie rozszerzenia programu SQL Server na określonej maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="e33f2-117">Example 4: Uninstall an SQL Server extension on a specific virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Set-AzureVMSqlServerExtension -Uninstall
```

<span data-ttu-id="e33f2-118">To polecenie Odinstalowuje rozszerzenie maszyny wirtualnej programu SQL Server na maszynie wirtualnej o nazwie VMName.</span><span class="sxs-lookup"><span data-stu-id="e33f2-118">This command uninstalls a SQL Server virtual machine extension on the virtual machine named VMName.</span></span>

## <span data-ttu-id="e33f2-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e33f2-119">PARAMETERS</span></span>

### <span data-ttu-id="e33f2-120">-AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="e33f2-120">-AutoBackupSettings</span></span>
<span data-ttu-id="e33f2-121">Określa ustawienia automatycznej kopii zapasowej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e33f2-121">Specifies the automatic SQL Server backup settings.</span></span>

```yaml
Type: AutoBackupSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-122">-AutoPatchingSettings</span><span class="sxs-lookup"><span data-stu-id="e33f2-122">-AutoPatchingSettings</span></span>
<span data-ttu-id="e33f2-123">Określa ustawienia automatycznej poprawki programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e33f2-123">Specifies the automatic SQL Server patching settings.</span></span>

```yaml
Type: AutoPatchingSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-124">-Disable</span><span class="sxs-lookup"><span data-stu-id="e33f2-124">-Disable</span></span>
<span data-ttu-id="e33f2-125">Wskazuje, że to polecenie cmdlet wyłącza stan rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="e33f2-125">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-126">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e33f2-126">-InformationAction</span></span>
<span data-ttu-id="e33f2-127">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="e33f2-127">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="e33f2-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e33f2-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e33f2-129">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="e33f2-129">Continue</span></span>
- <span data-ttu-id="e33f2-130">Ignorować</span><span class="sxs-lookup"><span data-stu-id="e33f2-130">Ignore</span></span>
- <span data-ttu-id="e33f2-131">Inquire</span><span class="sxs-lookup"><span data-stu-id="e33f2-131">Inquire</span></span>
- <span data-ttu-id="e33f2-132">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e33f2-132">SilentlyContinue</span></span>
- <span data-ttu-id="e33f2-133">Przestaw</span><span class="sxs-lookup"><span data-stu-id="e33f2-133">Stop</span></span>
- <span data-ttu-id="e33f2-134">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="e33f2-134">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-135">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e33f2-135">-InformationVariable</span></span>
<span data-ttu-id="e33f2-136">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="e33f2-136">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-137">-KeyVaultCredentialSettings</span><span class="sxs-lookup"><span data-stu-id="e33f2-137">-KeyVaultCredentialSettings</span></span>
<span data-ttu-id="e33f2-138">Określa ustawienia poświadczeń magazynu kluczy.</span><span class="sxs-lookup"><span data-stu-id="e33f2-138">Specifies key vault credential settings.</span></span>

```yaml
Type: KeyVaultCredentialSettings
Parameter Sets: EnableSqlServerExtension
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-139">-Profile</span><span class="sxs-lookup"><span data-stu-id="e33f2-139">-Profile</span></span>
<span data-ttu-id="e33f2-140">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e33f2-140">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="e33f2-141">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="e33f2-141">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-142">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="e33f2-142">-ReferenceName</span></span>
<span data-ttu-id="e33f2-143">Określa nazwę referencyjną rozszerzenia programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="e33f2-143">Specifies the reference name of the SQL Server extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-144">— Odinstalowywanie</span><span class="sxs-lookup"><span data-stu-id="e33f2-144">-Uninstall</span></span>
<span data-ttu-id="e33f2-145">Wskazuje, że to polecenie cmdlet Odinstalowuje rozszerzenie programu SQL Server z maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e33f2-145">Indicates that this cmdlet uninstalls the SQL Server extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallSqlServerExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-146">-Version</span><span class="sxs-lookup"><span data-stu-id="e33f2-146">-Version</span></span>
<span data-ttu-id="e33f2-147">Określa wersję rozszerzenia SQL Server, z którego Get-AzureVMSqlServerExtension pobierane ustawienia.</span><span class="sxs-lookup"><span data-stu-id="e33f2-147">Specifies the version of the SQL Server extension that Get-AzureVMSqlServerExtension retrieves settings from.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-148">-VM</span><span class="sxs-lookup"><span data-stu-id="e33f2-148">-VM</span></span>
<span data-ttu-id="e33f2-149">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="e33f2-149">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e33f2-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e33f2-150">CommonParameters</span></span>
<span data-ttu-id="e33f2-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e33f2-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e33f2-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e33f2-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e33f2-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e33f2-153">INPUTS</span></span>

## <span data-ttu-id="e33f2-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e33f2-154">OUTPUTS</span></span>

## <span data-ttu-id="e33f2-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e33f2-155">NOTES</span></span>

## <span data-ttu-id="e33f2-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e33f2-156">RELATED LINKS</span></span>

[<span data-ttu-id="e33f2-157">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e33f2-157">Get-AzureVMSqlServerExtension</span></span>](./Get-AzureVMSqlServerExtension.md)

[<span data-ttu-id="e33f2-158">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="e33f2-158">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)


