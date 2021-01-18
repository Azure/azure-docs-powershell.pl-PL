---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 952a9160a20492fe49e7f79019ca68e3bc241e57
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98501864"
---
# <span data-ttu-id="fb738-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="fb738-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="fb738-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb738-102">SYNOPSIS</span></span>
<span data-ttu-id="fb738-103">Tworzy obiekt konfiguracji dla automatycznej kopii zapasowej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fb738-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="fb738-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb738-104">SYNTAX</span></span>

### <span data-ttu-id="fb738-105">StorageUriSqlServerAutoBackup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fb738-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb738-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="fb738-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb738-107">Opis</span><span class="sxs-lookup"><span data-stu-id="fb738-107">DESCRIPTION</span></span>
<span data-ttu-id="fb738-108">Polecenie cmdlet **New-AzVMSqlServerAutoBackupConfig** tworzy obiekt konfiguracji dla automatycznej kopii zapasowej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fb738-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="fb738-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb738-109">EXAMPLES</span></span>

### <span data-ttu-id="fb738-110">Przykład 1. Tworzenie automatycznej konfiguracji kopii zapasowej przy użyciu identyfikatora URI magazynu i klucza konta</span><span class="sxs-lookup"><span data-stu-id="fb738-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="fb738-111">To polecenie tworzy obiekt automatycznej konfiguracji kopii zapasowej przez określenie identyfikatora URI miejsca do magazynowania i klucza konta.</span><span class="sxs-lookup"><span data-stu-id="fb738-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="fb738-112">Automatyczna kopia zapasowa jest włączona, a automatyczne kopie zapasowe są zachowywane przez 10 dni.</span><span class="sxs-lookup"><span data-stu-id="fb738-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="fb738-113">Polecenie zapisuje wyniki w zmiennej $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="fb738-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="fb738-114">Możesz określić ten element konfiguracji dla innych poleceń cmdlet, takich jak polecenie cmdlet Set-AzVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="fb738-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="fb738-115">Przykład 2: Tworzenie automatycznej konfiguracji kopii zapasowej przy użyciu kontekstu magazynu</span><span class="sxs-lookup"><span data-stu-id="fb738-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="fb738-116">Pierwsze polecenie tworzy kontekst miejsca do magazynowania, a następnie zapisuje go w zmiennej $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="fb738-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="fb738-117">Aby uzyskać więcej informacji, zobacz Nowość-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="fb738-117">For more information, see New-AzStorageContext.</span></span>
<span data-ttu-id="fb738-118">Drugie polecenie tworzy obiekt konfiguracji automatycznej kopii zapasowej, określając kontekst miejsca do magazynowania w $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="fb738-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="fb738-119">Automatyczna kopia zapasowa jest włączona, a automatyczne kopie zapasowe są zachowywane przez 10 dni.</span><span class="sxs-lookup"><span data-stu-id="fb738-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="fb738-120">Przykład 3: Tworzenie automatycznej konfiguracji kopii zapasowej przy użyciu kontekstu magazynu z szyfrowaniem i hasłem</span><span class="sxs-lookup"><span data-stu-id="fb738-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="fb738-121">To polecenie umożliwia utworzenie obiektu konfiguracji automatycznej kopii zapasowej i zapisanie go.</span><span class="sxs-lookup"><span data-stu-id="fb738-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="fb738-122">Polecenie określa kontekst miejsca do magazynowania utworzony w poprzednim przykładzie.</span><span class="sxs-lookup"><span data-stu-id="fb738-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="fb738-123">Polecenie włącza szyfrowanie przy użyciu hasła.</span><span class="sxs-lookup"><span data-stu-id="fb738-123">The command enables encryption with password.</span></span>
<span data-ttu-id="fb738-124">W zmiennej $CertificatePassword hasło zostało wcześniej zapisane w postaci bezpiecznego ciągu.</span><span class="sxs-lookup"><span data-stu-id="fb738-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="fb738-125">Aby utworzyć bezpieczny ciąg, użyj polecenia cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="fb738-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="fb738-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb738-126">PARAMETERS</span></span>

### <span data-ttu-id="fb738-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="fb738-127">-BackupScheduleType</span></span>
<span data-ttu-id="fb738-128">Typ harmonogramu kopii zapasowych, ręczny lub zautomatyzowany</span><span class="sxs-lookup"><span data-stu-id="fb738-128">Backup schedule type, manual or automated</span></span>

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

### <span data-ttu-id="fb738-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="fb738-129">-BackupSystemDbs</span></span>
<span data-ttu-id="fb738-130">Tworzenie kopii zapasowych baz danych</span><span class="sxs-lookup"><span data-stu-id="fb738-130">Backup system databases</span></span>

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

### <span data-ttu-id="fb738-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="fb738-131">-CertificatePassword</span></span>
<span data-ttu-id="fb738-132">Określa hasło do szyfrowania certyfikatu używanego do wykonywania zaszyfrowanych kopii zapasowych programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fb738-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

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

### <span data-ttu-id="fb738-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb738-133">-DefaultProfile</span></span>
<span data-ttu-id="fb738-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb738-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb738-135">-Enable</span><span class="sxs-lookup"><span data-stu-id="fb738-135">-Enable</span></span>
<span data-ttu-id="fb738-136">Wskazuje, że jest włączona automatyczna kopia zapasowa maszyny wirtualnej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fb738-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="fb738-137">W przypadku określenia tego parametru funkcja automatycznego tworzenia kopii zapasowych ustawia Harmonogram kopii zapasowej dla wszystkich bieżących i nowych baz danych.</span><span class="sxs-lookup"><span data-stu-id="fb738-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="fb738-138">Spowoduje to zaktualizowanie ustawień zarządzanych kopii zapasowych w celu obserwowania tego harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="fb738-138">This updates your Managed Backup settings to follow this schedule.</span></span>

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

### <span data-ttu-id="fb738-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="fb738-139">-EnableEncryption</span></span>
<span data-ttu-id="fb738-140">Wskazuje, że to polecenie cmdlet włącza szyfrowanie.</span><span class="sxs-lookup"><span data-stu-id="fb738-140">Indicates that this cmdlet enables encryption.</span></span>

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

### <span data-ttu-id="fb738-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="fb738-141">-FullBackupFrequency</span></span>
<span data-ttu-id="fb738-142">Częstotliwość pełnej kopii zapasowej programu SQL Server, codziennie lub co tydzień</span><span class="sxs-lookup"><span data-stu-id="fb738-142">Sql Server Full Backup frequency, daily or weekly</span></span>

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

### <span data-ttu-id="fb738-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="fb738-143">-FullBackupStartHour</span></span>
<span data-ttu-id="fb738-144">Godzina dnia (0-23) po uruchomieniu pełnej kopii zapasowej programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="fb738-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="fb738-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="fb738-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="fb738-146">Okno pełnej kopii zapasowej programu SQL Server w godzinach</span><span class="sxs-lookup"><span data-stu-id="fb738-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="fb738-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="fb738-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="fb738-148">Częstotliwość wykonywania kopii zapasowych dziennika programu SQL Server, co 1-60 minut</span><span class="sxs-lookup"><span data-stu-id="fb738-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="fb738-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb738-149">-ResourceGroupName</span></span>
<span data-ttu-id="fb738-150">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="fb738-150">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="fb738-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="fb738-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="fb738-152">Określa liczbę dni przechowywania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="fb738-152">Specifies the number of days to retain a backup.</span></span>

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

### <span data-ttu-id="fb738-153">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="fb738-153">-StorageContext</span></span>
<span data-ttu-id="fb738-154">Określa konto magazynu, które będzie używane do przechowywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="fb738-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="fb738-155">Aby uzyskać obiekt **AzureStorageContext** , użyj polecenia cmdlet New-AzStorageContext.</span><span class="sxs-lookup"><span data-stu-id="fb738-155">To obtain an **AzureStorageContext** object, use the New-AzStorageContext cmdlet.</span></span>
<span data-ttu-id="fb738-156">Domyślnie jest to konto magazynu skojarzone z maszyną wirtualną programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="fb738-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

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

### <span data-ttu-id="fb738-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="fb738-157">-StorageKey</span></span>
<span data-ttu-id="fb738-158">Określa klucz magazynu konta magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="fb738-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="fb738-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="fb738-159">-StorageUri</span></span>
<span data-ttu-id="fb738-160">Określa identyfikator URI (Uniform Resource Identifier) konta magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="fb738-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="fb738-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb738-161">CommonParameters</span></span>
<span data-ttu-id="fb738-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb738-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb738-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb738-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb738-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb738-164">INPUTS</span></span>

### <span data-ttu-id="fb738-165">System. String</span><span class="sxs-lookup"><span data-stu-id="fb738-165">System.String</span></span>

### <span data-ttu-id="fb738-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fb738-166">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="fb738-167">System. Int32</span><span class="sxs-lookup"><span data-stu-id="fb738-167">System.Int32</span></span>

### <span data-ttu-id="fb738-168">Microsoft. Azure. Commands. Common. Authentication. Abstracts. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="fb738-168">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="fb738-169">System. URI</span><span class="sxs-lookup"><span data-stu-id="fb738-169">System.Uri</span></span>

### <span data-ttu-id="fb738-170">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="fb738-170">System.Security.SecureString</span></span>

### <span data-ttu-id="fb738-171">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fb738-171">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fb738-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb738-172">OUTPUTS</span></span>

### <span data-ttu-id="fb738-173">Microsoft. Azure. Commands. COMPUTE. AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="fb738-173">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="fb738-174">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb738-174">NOTES</span></span>

## <span data-ttu-id="fb738-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb738-175">RELATED LINKS</span></span>

[<span data-ttu-id="fb738-176">Nowe — AzVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="fb738-176">New-AzVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="fb738-177">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="fb738-177">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


