---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 55E097F4-1F49-4196-9A8B-949FD5D9108A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4035487fa0363e6a7802966d9bc6422429723d94
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055165"
---
# <span data-ttu-id="c98eb-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="c98eb-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="c98eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c98eb-102">SYNOPSIS</span></span>
<span data-ttu-id="c98eb-103">Tworzy obiekt konfiguracji dla automatycznej kopii zapasowej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c98eb-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="c98eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c98eb-104">SYNTAX</span></span>

### <span data-ttu-id="c98eb-105">StorageUriSqlServerAutoBackup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c98eb-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="c98eb-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="c98eb-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <AzureStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c98eb-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c98eb-107">DESCRIPTION</span></span>
<span data-ttu-id="c98eb-108">Polecenie cmdlet **New-AzureVMSqlServerAutoBackupConfig** tworzy obiekt konfiguracji dla automatycznej kopii zapasowej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c98eb-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="c98eb-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c98eb-109">EXAMPLES</span></span>

### <span data-ttu-id="c98eb-110">Przykład 1: Tworzenie konfiguracji automatycznego tworzenia kopii zapasowej przy użyciu identyfikatora URI magazynu i klucza konta</span><span class="sxs-lookup"><span data-stu-id="c98eb-110">Example 1: Create an auto-backup configuration using storage URI and account key</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri $StorageUrl -StorageKey $StorageAccountKeySecure
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="c98eb-111">To polecenie tworzy obiekt konfiguracji automatycznego tworzenia kopii zapasowej, określając adres URL magazynu i klucz konta.</span><span class="sxs-lookup"><span data-stu-id="c98eb-111">This command creates an auto-backup configuration object by specifying storage URL and account key.</span></span>

### <span data-ttu-id="c98eb-112">Przykład 2: Tworzenie konfiguracji automatycznej kopii zapasowej przy użyciu kontekstu magazynu</span><span class="sxs-lookup"><span data-stu-id="c98eb-112">Example 2: Create an auto-backup configuration using storage context</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="c98eb-113">To polecenie tworzy obiekt konfiguracji autokopia zapasowa, określając kontekst miejsca do magazynowania.</span><span class="sxs-lookup"><span data-stu-id="c98eb-113">This command creates an auto-backup configuration object by specifying storage context.</span></span>

### <span data-ttu-id="c98eb-114">Przykład 3: Tworzenie konfiguracji automatycznej kopii zapasowej przy użyciu kontekstu magazynu z szyfrowaniem i hasłem</span><span class="sxs-lookup"><span data-stu-id="c98eb-114">Example 3: Create an auto-backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $ABS = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertPasswd
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="c98eb-115">To polecenie tworzy obiekt konfiguracji autokopia zapasowa, określając kontekst miejsca do magazynowania i włączając opcję szyfrowania z hasłami.</span><span class="sxs-lookup"><span data-stu-id="c98eb-115">This command creates an auto-backup configuration object by specifying Storage context and enabling encryption option with password.</span></span>
<span data-ttu-id="c98eb-116">CertificatePassword ist zapisana w zmiennej o nazwie $CertPasswd.</span><span class="sxs-lookup"><span data-stu-id="c98eb-116">The certificatepassword ist stored in the variable named $CertPasswd.</span></span>

## <span data-ttu-id="c98eb-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c98eb-117">PARAMETERS</span></span>

### <span data-ttu-id="c98eb-118">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="c98eb-118">-BackupScheduleType</span></span>
<span data-ttu-id="c98eb-119">Typ harmonogramu kopii zapasowych, ręczny lub zautomatyzowany</span><span class="sxs-lookup"><span data-stu-id="c98eb-119">Backup schedule type, manual or automated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c98eb-120">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="c98eb-120">-BackupSystemDbs</span></span>
<span data-ttu-id="c98eb-121">Tworzenie kopii zapasowych baz danych</span><span class="sxs-lookup"><span data-stu-id="c98eb-121">Backup system databases</span></span>

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

### <span data-ttu-id="c98eb-122">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="c98eb-122">-CertificatePassword</span></span>
<span data-ttu-id="c98eb-123">Określa hasło do szyfrowania certyfikatu używanego do wykonywania zaszyfrowanych kopii zapasowych programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c98eb-123">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c98eb-124">-Enable</span><span class="sxs-lookup"><span data-stu-id="c98eb-124">-Enable</span></span>
<span data-ttu-id="c98eb-125">Wskazuje, że jest włączona automatyczna kopia zapasowa maszyny wirtualnej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c98eb-125">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="c98eb-126">W przypadku użycia tego parametru funkcja automatycznego tworzenia kopii zapasowych ustawia Harmonogram kopii zapasowej dla wszystkich bieżących i nowych baz danych.</span><span class="sxs-lookup"><span data-stu-id="c98eb-126">If you use this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="c98eb-127">Spowoduje to zaktualizowanie ustawień zarządzanych kopii zapasowych w celu obserwowania tego harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="c98eb-127">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c98eb-128">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="c98eb-128">-EnableEncryption</span></span>
<span data-ttu-id="c98eb-129">Wskazuje, że szyfrowanie jest włączone.</span><span class="sxs-lookup"><span data-stu-id="c98eb-129">Indicates that encryption is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c98eb-130">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="c98eb-130">-FullBackupFrequency</span></span>
<span data-ttu-id="c98eb-131">Częstotliwość pełnej kopii zapasowej programu SQL Server, codziennie lub co tydzień</span><span class="sxs-lookup"><span data-stu-id="c98eb-131">Sql Server Full Backup frequency, daily or week</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c98eb-132">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="c98eb-132">-FullBackupStartHour</span></span>
<span data-ttu-id="c98eb-133">Godzina dnia (0-23) po uruchomieniu pełnej kopii zapasowej programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="c98eb-133">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="c98eb-134">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="c98eb-134">-FullBackupWindowInHours</span></span>
<span data-ttu-id="c98eb-135">Okno pełnej kopii zapasowej programu SQL Server w godzinach</span><span class="sxs-lookup"><span data-stu-id="c98eb-135">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="c98eb-136">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c98eb-136">-InformationAction</span></span>
<span data-ttu-id="c98eb-137">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="c98eb-137">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c98eb-138">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c98eb-138">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c98eb-139">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="c98eb-139">Continue</span></span>
- <span data-ttu-id="c98eb-140">Ignorować</span><span class="sxs-lookup"><span data-stu-id="c98eb-140">Ignore</span></span>
- <span data-ttu-id="c98eb-141">Inquire</span><span class="sxs-lookup"><span data-stu-id="c98eb-141">Inquire</span></span>
- <span data-ttu-id="c98eb-142">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c98eb-142">SilentlyContinue</span></span>
- <span data-ttu-id="c98eb-143">Przestaw</span><span class="sxs-lookup"><span data-stu-id="c98eb-143">Stop</span></span>
- <span data-ttu-id="c98eb-144">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="c98eb-144">Suspend</span></span>

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

### <span data-ttu-id="c98eb-145">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c98eb-145">-InformationVariable</span></span>
<span data-ttu-id="c98eb-146">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="c98eb-146">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c98eb-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="c98eb-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="c98eb-148">Częstotliwość wykonywania kopii zapasowych dziennika programu SQL Server, co 1-60 minut</span><span class="sxs-lookup"><span data-stu-id="c98eb-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="c98eb-149">-Profile</span><span class="sxs-lookup"><span data-stu-id="c98eb-149">-Profile</span></span>
<span data-ttu-id="c98eb-150">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c98eb-150">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c98eb-151">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="c98eb-151">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c98eb-152">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="c98eb-152">-RetentionPeriodInDays</span></span>
<span data-ttu-id="c98eb-153">Określa długość okresu przechowywania w dniach.</span><span class="sxs-lookup"><span data-stu-id="c98eb-153">Specifies the length of the retention period in days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c98eb-154">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="c98eb-154">-StorageContext</span></span>
<span data-ttu-id="c98eb-155">Określa konto magazynu, które ma być używane do przechowywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="c98eb-155">Specifies the storage account to be used to store backups.</span></span>
<span data-ttu-id="c98eb-156">Domyślnie jest to konto magazynu skojarzone z maszyną wirtualną programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="c98eb-156">Default is the storage account associated with the SQL Server virtual machine.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c98eb-157">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="c98eb-157">-StorageKey</span></span>
<span data-ttu-id="c98eb-158">Określa klucz magazynu konta magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="c98eb-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="c98eb-159">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="c98eb-159">-StorageUri</span></span>
<span data-ttu-id="c98eb-160">Określa identyfikator URI konta magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="c98eb-160">Specifies a URI to the blob storage account.</span></span>

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

### <span data-ttu-id="c98eb-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c98eb-161">CommonParameters</span></span>
<span data-ttu-id="c98eb-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c98eb-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c98eb-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c98eb-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c98eb-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c98eb-164">INPUTS</span></span>

## <span data-ttu-id="c98eb-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c98eb-165">OUTPUTS</span></span>

## <span data-ttu-id="c98eb-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c98eb-166">NOTES</span></span>

## <span data-ttu-id="c98eb-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c98eb-167">RELATED LINKS</span></span>

[<span data-ttu-id="c98eb-168">Nowe — AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="c98eb-168">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)


