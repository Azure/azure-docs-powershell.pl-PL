---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 15f26b611f90f8211e8f49c45c583d8953c028a8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525314"
---
# <span data-ttu-id="22692-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="22692-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="22692-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="22692-102">SYNOPSIS</span></span>
<span data-ttu-id="22692-103">Tworzy obiekt konfiguracji dla automatycznej kopii zapasowej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="22692-103">Creates a configuration object for SQL Server automatic backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="22692-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="22692-104">SYNTAX</span></span>

### <span data-ttu-id="22692-105">StorageUriSqlServerAutoBackup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="22692-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [<CommonParameters>]
```

### <span data-ttu-id="22692-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="22692-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable] [[-RetentionPeriodInDays] <Int32>]
 [-EnableEncryption] [[-CertificatePassword] <SecureString>] [[-StorageContext] <AzureStorageContext>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="22692-107">Opis</span><span class="sxs-lookup"><span data-stu-id="22692-107">DESCRIPTION</span></span>
<span data-ttu-id="22692-108">Polecenie cmdlet **New-AzureVMSqlServerAutoBackupConfig** tworzy obiekt konfiguracji dla automatycznej kopii zapasowej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="22692-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="22692-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="22692-109">EXAMPLES</span></span>

### <span data-ttu-id="22692-110">Przykład 1. Tworzenie automatycznej konfiguracji kopii zapasowej przy użyciu identyfikatora URI magazynu i klucza konta</span><span class="sxs-lookup"><span data-stu-id="22692-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="22692-111">To polecenie tworzy obiekt automatycznej konfiguracji kopii zapasowej przez określenie identyfikatora URI miejsca do magazynowania i klucza konta.</span><span class="sxs-lookup"><span data-stu-id="22692-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="22692-112">Automatyczna kopia zapasowa jest włączona, a automatyczne kopie zapasowe są zachowywane przez 10 dni.</span><span class="sxs-lookup"><span data-stu-id="22692-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="22692-113">Polecenie zapisuje wyniki w zmiennej $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="22692-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="22692-114">Możesz określić ten element konfiguracji dla innych poleceń cmdlet, takich jak polecenie cmdlet Set-AzureRmVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="22692-114">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="22692-115">Przykład 2: Tworzenie automatycznej konfiguracji kopii zapasowej przy użyciu kontekstu magazynu</span><span class="sxs-lookup"><span data-stu-id="22692-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="22692-116">Pierwsze polecenie tworzy kontekst miejsca do magazynowania, a następnie zapisuje go w zmiennej $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="22692-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="22692-117">Aby uzyskać więcej informacji, zobacz Nowość-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="22692-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="22692-118">Drugie polecenie tworzy obiekt konfiguracji automatycznej kopii zapasowej, określając kontekst miejsca do magazynowania w $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="22692-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="22692-119">Automatyczna kopia zapasowa jest włączona, a automatyczne kopie zapasowe są zachowywane przez 10 dni.</span><span class="sxs-lookup"><span data-stu-id="22692-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="22692-120">Przykład 3: Tworzenie automatycznej konfiguracji kopii zapasowej przy użyciu kontekstu magazynu z szyfrowaniem i hasłem</span><span class="sxs-lookup"><span data-stu-id="22692-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="22692-121">To polecenie umożliwia utworzenie obiektu konfiguracji automatycznej kopii zapasowej i zapisanie go.</span><span class="sxs-lookup"><span data-stu-id="22692-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="22692-122">Polecenie określa kontekst miejsca do magazynowania utworzony w poprzednim przykładzie.</span><span class="sxs-lookup"><span data-stu-id="22692-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="22692-123">Polecenie włącza szyfrowanie przy użyciu hasła.</span><span class="sxs-lookup"><span data-stu-id="22692-123">The command enables encryption with password.</span></span>
<span data-ttu-id="22692-124">W zmiennej $CertificatePassword hasło zostało wcześniej zapisane w postaci bezpiecznego ciągu.</span><span class="sxs-lookup"><span data-stu-id="22692-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="22692-125">Aby utworzyć bezpieczny ciąg, użyj polecenia cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="22692-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="22692-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="22692-126">PARAMETERS</span></span>

### <span data-ttu-id="22692-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="22692-127">-BackupScheduleType</span></span>
<span data-ttu-id="22692-128">Typ harmonogramu kopii zapasowych, ręczny lub zautomatyzowany</span><span class="sxs-lookup"><span data-stu-id="22692-128">Backup schedule type, manual or automated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22692-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="22692-129">-BackupSystemDbs</span></span>
<span data-ttu-id="22692-130">Tworzenie kopii zapasowych baz danych</span><span class="sxs-lookup"><span data-stu-id="22692-130">Backup system databases</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22692-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="22692-131">-CertificatePassword</span></span>
<span data-ttu-id="22692-132">Określa hasło do szyfrowania certyfikatu używanego do wykonywania zaszyfrowanych kopii zapasowych programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="22692-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="22692-133">-Enable</span><span class="sxs-lookup"><span data-stu-id="22692-133">-Enable</span></span>
<span data-ttu-id="22692-134">Wskazuje, że jest włączona automatyczna kopia zapasowa maszyny wirtualnej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="22692-134">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="22692-135">W przypadku określenia tego parametru funkcja automatycznego tworzenia kopii zapasowych ustawia Harmonogram kopii zapasowej dla wszystkich bieżących i nowych baz danych.</span><span class="sxs-lookup"><span data-stu-id="22692-135">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="22692-136">Spowoduje to zaktualizowanie ustawień zarządzanych kopii zapasowych w celu obserwowania tego harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="22692-136">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22692-137">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="22692-137">-EnableEncryption</span></span>
<span data-ttu-id="22692-138">Wskazuje, że to polecenie cmdlet włącza szyfrowanie.</span><span class="sxs-lookup"><span data-stu-id="22692-138">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22692-139">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="22692-139">-FullBackupFrequency</span></span>
<span data-ttu-id="22692-140">Częstotliwość pełnej kopii zapasowej programu SQL Server, codziennie lub co tydzień</span><span class="sxs-lookup"><span data-stu-id="22692-140">Sql Server Full Backup frequency, daily or weekly</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22692-141">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="22692-141">-FullBackupStartHour</span></span>
<span data-ttu-id="22692-142">Godzina dnia (0-23) po uruchomieniu pełnej kopii zapasowej programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="22692-142">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22692-143">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="22692-143">-FullBackupWindowInHours</span></span>
<span data-ttu-id="22692-144">Okno pełnej kopii zapasowej programu SQL Server w godzinach</span><span class="sxs-lookup"><span data-stu-id="22692-144">Sql Server Full Backup window in hours</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22692-145">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="22692-145">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="22692-146">Częstotliwość wykonywania kopii zapasowych dziennika programu SQL Server, co 1-60 minut</span><span class="sxs-lookup"><span data-stu-id="22692-146">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22692-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22692-147">-ResourceGroupName</span></span>
<span data-ttu-id="22692-148">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="22692-148">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22692-149">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="22692-149">-RetentionPeriodInDays</span></span>
<span data-ttu-id="22692-150">Określa liczbę dni przechowywania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="22692-150">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22692-151">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="22692-151">-StorageContext</span></span>
<span data-ttu-id="22692-152">Określa konto magazynu, które będzie używane do przechowywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="22692-152">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="22692-153">Aby uzyskać obiekt **AzureStorageContext** , użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="22692-153">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="22692-154">Domyślnie jest to konto magazynu skojarzone z maszyną wirtualną programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="22692-154">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22692-155">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="22692-155">-StorageKey</span></span>
<span data-ttu-id="22692-156">Określa klucz magazynu konta magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="22692-156">Specifies the storage key of the blob storage account.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22692-157">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="22692-157">-StorageUri</span></span>
<span data-ttu-id="22692-158">Określa identyfikator URI (Uniform Resource Identifier) konta magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="22692-158">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="22692-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22692-159">CommonParameters</span></span>
<span data-ttu-id="22692-160">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="22692-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22692-161">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22692-161">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22692-162">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="22692-162">INPUTS</span></span>

### <span data-ttu-id="22692-163">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="22692-163">None</span></span>
<span data-ttu-id="22692-164">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="22692-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="22692-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="22692-165">OUTPUTS</span></span>

## <span data-ttu-id="22692-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="22692-166">NOTES</span></span>

## <span data-ttu-id="22692-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="22692-167">RELATED LINKS</span></span>

[<span data-ttu-id="22692-168">Nowe — AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="22692-168">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="22692-169">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="22692-169">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


