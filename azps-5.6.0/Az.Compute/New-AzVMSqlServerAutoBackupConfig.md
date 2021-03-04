---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 6d9047679f4286e0e2212ca8e599237825326dd7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975921"
---
# <span data-ttu-id="f1352-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="f1352-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="f1352-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1352-102">SYNOPSIS</span></span>
<span data-ttu-id="f1352-103">Tworzy obiekt konfiguracji dla automatycznej kopii zapasowej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f1352-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="f1352-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f1352-104">SYNTAX</span></span>

### <span data-ttu-id="f1352-105">StorageUriSqlServerAutoBackup (domyślne)</span><span class="sxs-lookup"><span data-stu-id="f1352-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f1352-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="f1352-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f1352-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f1352-107">DESCRIPTION</span></span>
<span data-ttu-id="f1352-108">Polecenie **cmdlet New-AzVMSqlServerAutoBackupConfig** tworzy obiekt konfiguracji dla automatycznej kopii zapasowej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f1352-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="f1352-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f1352-109">EXAMPLES</span></span>

### <span data-ttu-id="f1352-110">Przykład 1. Tworzenie automatycznej konfiguracji kopii zapasowej przy użyciu URI magazynu i klucza konta</span><span class="sxs-lookup"><span data-stu-id="f1352-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="f1352-111">To polecenie tworzy obiekt automatycznej konfiguracji kopii zapasowej, określając identyfikator URI magazynu i klucz konta.</span><span class="sxs-lookup"><span data-stu-id="f1352-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="f1352-112">Automatyczne tworzenie kopii zapasowych jest włączone, a automatyczne kopie zapasowe są przechowywane przez 10 dni.</span><span class="sxs-lookup"><span data-stu-id="f1352-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="f1352-113">Polecenie przechowuje wynik w $AutoBackupConfig zmienną.</span><span class="sxs-lookup"><span data-stu-id="f1352-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="f1352-114">Ten element konfiguracji można określić dla innych pozycji cmdlet, takich jak polecenie cmdlet Set-AzVMSqlServerExtension cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1352-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="f1352-115">Przykład 2. Tworzenie automatycznej konfiguracji kopii zapasowej przy użyciu kontekstu magazynu</span><span class="sxs-lookup"><span data-stu-id="f1352-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="f1352-116">Pierwsze polecenie tworzy kontekst magazynu, a następnie zapisuje go w $StorageContext danych.</span><span class="sxs-lookup"><span data-stu-id="f1352-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="f1352-117">Aby uzyskać więcej informacji, zobacz New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="f1352-117">For more information, see New-AzStorageContext.</span></span>
<span data-ttu-id="f1352-118">Drugie polecenie tworzy obiekt automatycznej konfiguracji kopii zapasowej, określając kontekst magazynu w $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="f1352-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="f1352-119">Automatyczne tworzenie kopii zapasowych jest włączone, a automatyczne kopie zapasowe są przechowywane przez 10 dni.</span><span class="sxs-lookup"><span data-stu-id="f1352-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="f1352-120">Przykład 3. Tworzenie automatycznej konfiguracji kopii zapasowej przy użyciu kontekstu magazynu z szyfrowaniem i hasłem</span><span class="sxs-lookup"><span data-stu-id="f1352-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="f1352-121">To polecenie tworzy i przechowuje obiekt automatycznej konfiguracji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="f1352-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="f1352-122">To polecenie określa kontekst magazynowania utworzony w poprzednim przykładzie.</span><span class="sxs-lookup"><span data-stu-id="f1352-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="f1352-123">To polecenie umożliwia szyfrowanie przy użyciu hasła.</span><span class="sxs-lookup"><span data-stu-id="f1352-123">The command enables encryption with password.</span></span>
<span data-ttu-id="f1352-124">Hasło było wcześniej przechowywane jako bezpieczny ciąg w $CertificatePassword danych.</span><span class="sxs-lookup"><span data-stu-id="f1352-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="f1352-125">Aby utworzyć bezpieczny ciąg, użyj ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1352-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="f1352-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1352-126">PARAMETERS</span></span>

### <span data-ttu-id="f1352-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="f1352-127">-BackupScheduleType</span></span>
<span data-ttu-id="f1352-128">Typ harmonogramu kopii zapasowej, ręczny lub automatyczny</span><span class="sxs-lookup"><span data-stu-id="f1352-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1352-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="f1352-129">-BackupSystemDbs</span></span>
<span data-ttu-id="f1352-130">Bazy danych systemu kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="f1352-130">Backup system databases</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1352-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="f1352-131">-CertificatePassword</span></span>
<span data-ttu-id="f1352-132">Określa hasło do szyfrowania certyfikatu używanego do wykonywania zaszyfrowanych kopii zapasowych programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f1352-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1352-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1352-133">-DefaultProfile</span></span>
<span data-ttu-id="f1352-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1352-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1352-135">— Włącz</span><span class="sxs-lookup"><span data-stu-id="f1352-135">-Enable</span></span>
<span data-ttu-id="f1352-136">Oznacza, że włączono automatyczną kopię zapasową maszyny wirtualnej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f1352-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="f1352-137">Jeśli określisz ten parametr, automatyczna kopia zapasowa ustawia harmonogram kopii zapasowej dla wszystkich bieżących i nowych baz danych.</span><span class="sxs-lookup"><span data-stu-id="f1352-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="f1352-138">To aktualizuje ustawienia zarządzanej kopii zapasowej, aby postępować zgodnie z tym harmonogramem.</span><span class="sxs-lookup"><span data-stu-id="f1352-138">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1352-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="f1352-139">-EnableEncryption</span></span>
<span data-ttu-id="f1352-140">Wskazuje, że to polecenie cmdlet umożliwia szyfrowanie.</span><span class="sxs-lookup"><span data-stu-id="f1352-140">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1352-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="f1352-141">-FullBackupFrequency</span></span>
<span data-ttu-id="f1352-142">Częstotliwość wykonywania pełnej kopii zapasowej w programie Sql Server, codziennie lub co tydzień</span><span class="sxs-lookup"><span data-stu-id="f1352-142">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1352-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="f1352-143">-FullBackupStartHour</span></span>
<span data-ttu-id="f1352-144">Godzina dnia (0–23), w którym powinna się rozpocząć pełna kopia zapasowa programu Sql Server</span><span class="sxs-lookup"><span data-stu-id="f1352-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1352-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="f1352-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="f1352-146">Okno Pełnej kopii zapasowej w programie Sql Server w godzinach</span><span class="sxs-lookup"><span data-stu-id="f1352-146">Sql Server Full Backup window in hours</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1352-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="f1352-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="f1352-148">Częstotliwość tworzenia kopii zapasowej dziennika programu Sql Server co 1–60 minut</span><span class="sxs-lookup"><span data-stu-id="f1352-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1352-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1352-149">-ResourceGroupName</span></span>
<span data-ttu-id="f1352-150">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="f1352-150">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="f1352-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="f1352-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="f1352-152">Określa liczbę dni, przez które ma być zachowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="f1352-152">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1352-153">- StorageContext</span><span class="sxs-lookup"><span data-stu-id="f1352-153">-StorageContext</span></span>
<span data-ttu-id="f1352-154">Określa konto magazynu, które będzie używane do przechowywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="f1352-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="f1352-155">Aby uzyskać obiekt **AzureStorageContext,** użyj New-AzStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1352-155">To obtain an **AzureStorageContext** object, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="f1352-156">Wartością domyślną jest konto magazynu skojarzone z maszyną wirtualną programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="f1352-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1352-157">- KluczDazydzydów</span><span class="sxs-lookup"><span data-stu-id="f1352-157">-StorageKey</span></span>
<span data-ttu-id="f1352-158">Określa klucz magazynu konta magazynu obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="f1352-158">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1352-159">— StorageUri</span><span class="sxs-lookup"><span data-stu-id="f1352-159">-StorageUri</span></span>
<span data-ttu-id="f1352-160">Określa identyfikator URI konta magazynu obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="f1352-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1352-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1352-161">CommonParameters</span></span>
<span data-ttu-id="f1352-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1352-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1352-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f1352-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1352-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1352-164">INPUTS</span></span>

### <span data-ttu-id="f1352-165">System.String</span><span class="sxs-lookup"><span data-stu-id="f1352-165">System.String</span></span>

### <span data-ttu-id="f1352-166">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="f1352-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="f1352-167">System.Int32</span><span class="sxs-lookup"><span data-stu-id="f1352-167">System.Int32</span></span>

### <span data-ttu-id="f1352-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f1352-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="f1352-169">System.Uri</span><span class="sxs-lookup"><span data-stu-id="f1352-169">System.Uri</span></span>

### <span data-ttu-id="f1352-170">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="f1352-170">System.Security.SecureString</span></span>

### <span data-ttu-id="f1352-171">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f1352-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f1352-172">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1352-172">OUTPUTS</span></span>

### <span data-ttu-id="f1352-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="f1352-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="f1352-174">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f1352-174">NOTES</span></span>

## <span data-ttu-id="f1352-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1352-175">RELATED LINKS</span></span>

[<span data-ttu-id="f1352-176">New-AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="f1352-176">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="f1352-177">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="f1352-177">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


