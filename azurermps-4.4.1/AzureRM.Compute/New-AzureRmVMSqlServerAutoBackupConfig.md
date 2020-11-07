---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
Module Name: Azure
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/New-AzureRmVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: 2617ca54050f6a37fcc5714fe80e2f2d50e33e40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719368"
---
# <span data-ttu-id="31f17-101">New-AzureVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="31f17-101">New-AzureVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="31f17-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="31f17-102">SYNOPSIS</span></span>
<span data-ttu-id="31f17-103">Tworzy obiekt konfiguracji dla automatycznej kopii zapasowej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="31f17-103">Creates a configuration object for SQL Server automatic backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31f17-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="31f17-104">SYNTAX</span></span>

### <span data-ttu-id="31f17-105">StorageUriSqlServerAutoBackup (domyślny)</span><span class="sxs-lookup"><span data-stu-id="31f17-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>]
 [-BackupSystemDbs] [-BackupScheduleType <String>] [-FullBackupFrequency <String>]
 [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="31f17-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="31f17-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzureVMSqlServerAutoBackupConfig [-Enable] [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption]
 [[-CertificatePassword] <SecureString>] [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>]
 [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="31f17-107">Opis</span><span class="sxs-lookup"><span data-stu-id="31f17-107">DESCRIPTION</span></span>
<span data-ttu-id="31f17-108">Polecenie cmdlet **New-AzureVMSqlServerAutoBackupConfig** tworzy obiekt konfiguracji dla automatycznej kopii zapasowej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="31f17-108">The **New-AzureVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="31f17-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="31f17-109">EXAMPLES</span></span>

### <span data-ttu-id="31f17-110">Przykład 1. Tworzenie automatycznej konfiguracji kopii zapasowej przy użyciu identyfikatora URI magazynu i klucza konta</span><span class="sxs-lookup"><span data-stu-id="31f17-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="31f17-111">To polecenie tworzy obiekt automatycznej konfiguracji kopii zapasowej przez określenie identyfikatora URI miejsca do magazynowania i klucza konta.</span><span class="sxs-lookup"><span data-stu-id="31f17-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="31f17-112">Automatyczna kopia zapasowa jest włączona, a automatyczne kopie zapasowe są zachowywane przez 10 dni.</span><span class="sxs-lookup"><span data-stu-id="31f17-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="31f17-113">Polecenie zapisuje wyniki w zmiennej $AutoBackupConfig.</span><span class="sxs-lookup"><span data-stu-id="31f17-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="31f17-114">Możesz określić ten element konfiguracji dla innych poleceń cmdlet, takich jak polecenie cmdlet Set-AzureRmVMSqlServerExtension.</span><span class="sxs-lookup"><span data-stu-id="31f17-114">You can specify this configuration item for other cmdlets, such as the Set-AzureRmVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="31f17-115">Przykład 2: Tworzenie automatycznej konfiguracji kopii zapasowej przy użyciu kontekstu magazynu</span><span class="sxs-lookup"><span data-stu-id="31f17-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="31f17-116">Pierwsze polecenie tworzy kontekst miejsca do magazynowania, a następnie zapisuje go w zmiennej $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="31f17-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="31f17-117">Aby uzyskać więcej informacji, zobacz Nowość-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="31f17-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="31f17-118">Drugie polecenie tworzy obiekt konfiguracji automatycznej kopii zapasowej, określając kontekst miejsca do magazynowania w $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="31f17-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="31f17-119">Automatyczna kopia zapasowa jest włączona, a automatyczne kopie zapasowe są zachowywane przez 10 dni.</span><span class="sxs-lookup"><span data-stu-id="31f17-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="31f17-120">Przykład 3: Tworzenie automatycznej konfiguracji kopii zapasowej przy użyciu kontekstu magazynu z szyfrowaniem i hasłem</span><span class="sxs-lookup"><span data-stu-id="31f17-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzureVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="31f17-121">To polecenie umożliwia utworzenie obiektu konfiguracji automatycznej kopii zapasowej i zapisanie go.</span><span class="sxs-lookup"><span data-stu-id="31f17-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="31f17-122">Polecenie określa kontekst miejsca do magazynowania utworzony w poprzednim przykładzie.</span><span class="sxs-lookup"><span data-stu-id="31f17-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="31f17-123">Polecenie włącza szyfrowanie przy użyciu hasła.</span><span class="sxs-lookup"><span data-stu-id="31f17-123">The command enables encryption with password.</span></span>
<span data-ttu-id="31f17-124">W zmiennej $CertificatePassword hasło zostało wcześniej zapisane w postaci bezpiecznego ciągu.</span><span class="sxs-lookup"><span data-stu-id="31f17-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="31f17-125">Aby utworzyć bezpieczny ciąg, użyj polecenia cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="31f17-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="31f17-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="31f17-126">PARAMETERS</span></span>

### <span data-ttu-id="31f17-127">-Enable</span><span class="sxs-lookup"><span data-stu-id="31f17-127">-Enable</span></span>
<span data-ttu-id="31f17-128">Wskazuje, że jest włączona automatyczna kopia zapasowa maszyny wirtualnej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="31f17-128">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="31f17-129">W przypadku określenia tego parametru funkcja automatycznego tworzenia kopii zapasowych ustawia Harmonogram kopii zapasowej dla wszystkich bieżących i nowych baz danych.</span><span class="sxs-lookup"><span data-stu-id="31f17-129">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="31f17-130">Spowoduje to zaktualizowanie ustawień zarządzanych kopii zapasowych w celu obserwowania tego harmonogramu.</span><span class="sxs-lookup"><span data-stu-id="31f17-130">This updates your Managed Backup settings to follow this schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f17-131">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="31f17-131">-RetentionPeriodInDays</span></span>
<span data-ttu-id="31f17-132">Określa liczbę dni przechowywania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="31f17-132">Specifies the number of days to retain a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f17-133">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="31f17-133">-EnableEncryption</span></span>
<span data-ttu-id="31f17-134">Wskazuje, że to polecenie cmdlet włącza szyfrowanie.</span><span class="sxs-lookup"><span data-stu-id="31f17-134">Indicates that this cmdlet enables encryption.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f17-135">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="31f17-135">-CertificatePassword</span></span>
<span data-ttu-id="31f17-136">Określa hasło do szyfrowania certyfikatu używanego do wykonywania zaszyfrowanych kopii zapasowych programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="31f17-136">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f17-137">-StorageUri</span><span class="sxs-lookup"><span data-stu-id="31f17-137">-StorageUri</span></span>
<span data-ttu-id="31f17-138">Określa identyfikator URI (Uniform Resource Identifier) konta magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="31f17-138">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="31f17-139">-StorageKey</span><span class="sxs-lookup"><span data-stu-id="31f17-139">-StorageKey</span></span>
<span data-ttu-id="31f17-140">Określa klucz magazynu konta magazynu obiektów BLOB.</span><span class="sxs-lookup"><span data-stu-id="31f17-140">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="31f17-141">-Profile</span><span class="sxs-lookup"><span data-stu-id="31f17-141">-Profile</span></span>
<span data-ttu-id="31f17-142">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="31f17-142">Specifies the Azure profile from which this cmdlet reads.</span></span> <span data-ttu-id="31f17-143">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="31f17-143">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Utilities.Common.AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f17-144">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="31f17-144">-InformationAction</span></span>
<span data-ttu-id="31f17-145">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="31f17-145">@{Text=}</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f17-146">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="31f17-146">-InformationVariable</span></span>
<span data-ttu-id="31f17-147">@ {Text =}</span><span class="sxs-lookup"><span data-stu-id="31f17-147">@{Text=}</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31f17-148">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="31f17-148">-StorageContext</span></span>
<span data-ttu-id="31f17-149">Określa konto magazynu, które będzie używane do przechowywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="31f17-149">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="31f17-150">Aby uzyskać obiekt **AzureStorageContext** , użyj polecenia cmdlet New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="31f17-150">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="31f17-151">Domyślnie jest to konto magazynu skojarzone z maszyną wirtualną programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="31f17-151">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f17-152">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="31f17-152">-BackupScheduleType</span></span>
<span data-ttu-id="31f17-153">Typ harmonogramu kopii zapasowych, ręczny lub zautomatyzowany</span><span class="sxs-lookup"><span data-stu-id="31f17-153">Backup schedule type, manual or automated</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f17-154">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="31f17-154">-BackupSystemDbs</span></span>
<span data-ttu-id="31f17-155">Tworzenie kopii zapasowych baz danych</span><span class="sxs-lookup"><span data-stu-id="31f17-155">Backup system databases</span></span>

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

### <span data-ttu-id="31f17-156">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="31f17-156">-FullBackupFrequency</span></span>
<span data-ttu-id="31f17-157">Częstotliwość pełnej kopii zapasowej programu SQL Server, codziennie lub co tydzień</span><span class="sxs-lookup"><span data-stu-id="31f17-157">Sql Server Full Backup frequency, daily or week</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31f17-158">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="31f17-158">-FullBackupStartHour</span></span>
<span data-ttu-id="31f17-159">Godzina dnia (0-23) po uruchomieniu pełnej kopii zapasowej programu SQL Server</span><span class="sxs-lookup"><span data-stu-id="31f17-159">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="31f17-160">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="31f17-160">-FullBackupWindowInHours</span></span>
<span data-ttu-id="31f17-161">Okno pełnej kopii zapasowej programu SQL Server w godzinach</span><span class="sxs-lookup"><span data-stu-id="31f17-161">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="31f17-162">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="31f17-162">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="31f17-163">Częstotliwość wykonywania kopii zapasowych dziennika programu SQL Server, co 1-60 minut</span><span class="sxs-lookup"><span data-stu-id="31f17-163">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="31f17-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31f17-164">CommonParameters</span></span>
<span data-ttu-id="31f17-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31f17-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31f17-166">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31f17-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31f17-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="31f17-167">INPUTS</span></span>

## <span data-ttu-id="31f17-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="31f17-168">OUTPUTS</span></span>

## <span data-ttu-id="31f17-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="31f17-169">NOTES</span></span>

## <span data-ttu-id="31f17-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="31f17-170">RELATED LINKS</span></span>

[<span data-ttu-id="31f17-171">Nowe — AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="31f17-171">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzureVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="31f17-172">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="31f17-172">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)


