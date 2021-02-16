---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/new-azvmsqlserverautobackupconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/New-AzVMSqlServerAutoBackupConfig.md
ms.openlocfilehash: ecff02643dd6d0e017d56af01792a06dc7b8d998
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398278"
---
# <span data-ttu-id="ff7ea-101">New-AzVMSqlServerAutoBackupConfig</span><span class="sxs-lookup"><span data-stu-id="ff7ea-101">New-AzVMSqlServerAutoBackupConfig</span></span>

## <span data-ttu-id="ff7ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff7ea-102">SYNOPSIS</span></span>
<span data-ttu-id="ff7ea-103">Tworzy obiekt konfiguracji dla automatycznej kopii zapasowej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-103">Creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="ff7ea-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ff7ea-104">SYNTAX</span></span>

### <span data-ttu-id="ff7ea-105">StorageUriSqlServerAutoBackup (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ff7ea-105">StorageUriSqlServerAutoBackup (Default)</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ff7ea-106">StorageContextSqlServerAutoBackup</span><span class="sxs-lookup"><span data-stu-id="ff7ea-106">StorageContextSqlServerAutoBackup</span></span>
```
New-AzVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ff7ea-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ff7ea-107">DESCRIPTION</span></span>
<span data-ttu-id="ff7ea-108">Polecenie **cmdlet New-AzVMSqlServerAutoBackupConfig** tworzy obiekt konfiguracji dla automatycznej kopii zapasowej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-108">The **New-AzVMSqlServerAutoBackupConfig** cmdlet creates a configuration object for SQL Server automatic backup.</span></span>

## <span data-ttu-id="ff7ea-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ff7ea-109">EXAMPLES</span></span>

### <span data-ttu-id="ff7ea-110">Przykład 1. Tworzenie automatycznej konfiguracji kopii zapasowej przy użyciu URI magazynu i klucza konta</span><span class="sxs-lookup"><span data-stu-id="ff7ea-110">Example 1: Create an automatic backup configuration using storage URI and account key</span></span>
```
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="ff7ea-111">To polecenie tworzy obiekt automatycznej konfiguracji kopii zapasowej, określając identyfikator URI magazynu i klucz konta.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-111">This command creates an automatic backup configuration object by specifying storage URI and account key.</span></span>
<span data-ttu-id="ff7ea-112">Automatyczne tworzenie kopii zapasowych jest włączone, a automatyczne kopie zapasowe są przechowywane przez 10 dni.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-112">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>
<span data-ttu-id="ff7ea-113">Polecenie przechowuje wynik w $AutoBackupConfig zmienną.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-113">The command stores the result in the $AutoBackupConfig variable.</span></span>
<span data-ttu-id="ff7ea-114">Ten element konfiguracji możesz określić dla innych pozycji cmdlet, takich jak polecenie cmdlet Set-AzVMSqlServerExtension cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-114">You can specify this configuration item for other cmdlets, such as the Set-AzVMSqlServerExtension cmdlet.</span></span>

### <span data-ttu-id="ff7ea-115">Przykład 2. Tworzenie automatycznej konfiguracji kopii zapasowej przy użyciu kontekstu magazynu</span><span class="sxs-lookup"><span data-stu-id="ff7ea-115">Example 2: Create an automatic backup configuration using storage context</span></span>
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

<span data-ttu-id="ff7ea-116">Pierwsze polecenie tworzy kontekst magazynu, a następnie zapisuje go w $StorageContext danych.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-116">The first command creates a storage context, and then stores it in the $StorageContext variable.</span></span>
<span data-ttu-id="ff7ea-117">Aby uzyskać więcej informacji, zobacz New-AzureStorageContext.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-117">For more information, see New-AzureStorageContext.</span></span>

<span data-ttu-id="ff7ea-118">Drugie polecenie tworzy obiekt automatycznej konfiguracji kopii zapasowej, określając kontekst magazynu w $StorageContext.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-118">The second command creates an automatic backup configuration object by specifying the storage context in $StorageContext.</span></span>
<span data-ttu-id="ff7ea-119">Automatyczne tworzenie kopii zapasowych jest włączone, a automatyczne kopie zapasowe są przechowywane przez 10 dni.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-119">Automatic backup is enabled and automatic backups are kept for 10 days.</span></span>

### <span data-ttu-id="ff7ea-120">Przykład 3. Tworzenie automatycznej konfiguracji kopii zapasowej przy użyciu kontekstu magazynu z szyfrowaniem i hasłem</span><span class="sxs-lookup"><span data-stu-id="ff7ea-120">Example 3: Create an automatic backup configuration using storage context with encryption and password</span></span>
```
PS C:\> $StorageContext = New-AzVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

<span data-ttu-id="ff7ea-121">To polecenie tworzy i przechowuje obiekt automatycznej konfiguracji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-121">This command creates and stores an automatic backup configuration object.</span></span>
<span data-ttu-id="ff7ea-122">To polecenie określa kontekst magazynowania utworzony w poprzednim przykładzie.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-122">The command specifies the storage context created in a previous example.</span></span>
<span data-ttu-id="ff7ea-123">To polecenie umożliwia szyfrowanie przy użyciu hasła.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-123">The command enables encryption with password.</span></span>
<span data-ttu-id="ff7ea-124">Hasło było wcześniej przechowywane jako bezpieczny ciąg w $CertificatePassword danych.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-124">The password was previously stored as a secure string in the $CertificatePassword variable.</span></span>
<span data-ttu-id="ff7ea-125">Aby utworzyć bezpieczny ciąg, użyj ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-125">To create a secure string, use the ConvertTo-SecureString cmdlet.</span></span>

## <span data-ttu-id="ff7ea-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ff7ea-126">PARAMETERS</span></span>

### <span data-ttu-id="ff7ea-127">-BackupScheduleType</span><span class="sxs-lookup"><span data-stu-id="ff7ea-127">-BackupScheduleType</span></span>
<span data-ttu-id="ff7ea-128">Typ harmonogramu kopii zapasowej, ręczny lub automatyczny</span><span class="sxs-lookup"><span data-stu-id="ff7ea-128">Backup schedule type, manual or automated</span></span>

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

### <span data-ttu-id="ff7ea-129">-BackupSystemDbs</span><span class="sxs-lookup"><span data-stu-id="ff7ea-129">-BackupSystemDbs</span></span>
<span data-ttu-id="ff7ea-130">Bazy danych systemu kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="ff7ea-130">Backup system databases</span></span>

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

### <span data-ttu-id="ff7ea-131">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="ff7ea-131">-CertificatePassword</span></span>
<span data-ttu-id="ff7ea-132">Określa hasło do szyfrowania certyfikatu używanego do wykonywania zaszyfrowanych kopii zapasowych programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-132">Specifies a password to encrypt the certificate that is used to perform SQL Server encrypted backups.</span></span>

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

### <span data-ttu-id="ff7ea-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff7ea-133">-DefaultProfile</span></span>
<span data-ttu-id="ff7ea-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ff7ea-135">— Włącz</span><span class="sxs-lookup"><span data-stu-id="ff7ea-135">-Enable</span></span>
<span data-ttu-id="ff7ea-136">Oznacza, że włączono automatyczną kopię zapasową maszyny wirtualnej programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-136">Indicates that automated backup for the SQL Server virtual machine is enabled.</span></span>
<span data-ttu-id="ff7ea-137">Jeśli określisz ten parametr, automatyczna kopia zapasowa ustawia harmonogram kopii zapasowej dla wszystkich bieżących i nowych baz danych.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-137">If you specify this parameter, automated backup sets a backup schedule for all current and new databases.</span></span>
<span data-ttu-id="ff7ea-138">To aktualizuje ustawienia zarządzanej kopii zapasowej, aby postępować zgodnie z tym harmonogramem.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-138">This updates your Managed Backup settings to follow this schedule.</span></span>

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

### <span data-ttu-id="ff7ea-139">-EnableEncryption</span><span class="sxs-lookup"><span data-stu-id="ff7ea-139">-EnableEncryption</span></span>
<span data-ttu-id="ff7ea-140">Wskazuje, że to polecenie cmdlet umożliwia szyfrowanie.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-140">Indicates that this cmdlet enables encryption.</span></span>

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

### <span data-ttu-id="ff7ea-141">-FullBackupFrequency</span><span class="sxs-lookup"><span data-stu-id="ff7ea-141">-FullBackupFrequency</span></span>
<span data-ttu-id="ff7ea-142">Częstotliwość wykonywania pełnej kopii zapasowej w programie Sql Server codziennie lub co tydzień</span><span class="sxs-lookup"><span data-stu-id="ff7ea-142">Sql Server Full Backup frequency, daily or weekly</span></span>

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

### <span data-ttu-id="ff7ea-143">-FullBackupStartHour</span><span class="sxs-lookup"><span data-stu-id="ff7ea-143">-FullBackupStartHour</span></span>
<span data-ttu-id="ff7ea-144">Godzina dnia (0–23), w którym powinna się rozpocząć pełna kopia zapasowa programu Sql Server</span><span class="sxs-lookup"><span data-stu-id="ff7ea-144">Hour of the day (0-23) when the Sql Server Full Backup should start</span></span>

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

### <span data-ttu-id="ff7ea-145">-FullBackupWindowInHours</span><span class="sxs-lookup"><span data-stu-id="ff7ea-145">-FullBackupWindowInHours</span></span>
<span data-ttu-id="ff7ea-146">Okno Pełnej kopii zapasowej w programie Sql Server w godzinach</span><span class="sxs-lookup"><span data-stu-id="ff7ea-146">Sql Server Full Backup window in hours</span></span>

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

### <span data-ttu-id="ff7ea-147">-LogBackupFrequencyInMinutes</span><span class="sxs-lookup"><span data-stu-id="ff7ea-147">-LogBackupFrequencyInMinutes</span></span>
<span data-ttu-id="ff7ea-148">Częstotliwość tworzenia kopii zapasowej dziennika programu Sql Server co 1–60 minut</span><span class="sxs-lookup"><span data-stu-id="ff7ea-148">Sql Server Log Backup frequency, once every 1-60 minutes</span></span>

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

### <span data-ttu-id="ff7ea-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff7ea-149">-ResourceGroupName</span></span>
<span data-ttu-id="ff7ea-150">Określa nazwę grupy zasobów maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-150">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="ff7ea-151">-RetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="ff7ea-151">-RetentionPeriodInDays</span></span>
<span data-ttu-id="ff7ea-152">Określa liczbę dni, przez które ma być zachowywana kopia zapasowa.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-152">Specifies the number of days to retain a backup.</span></span>

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

### <span data-ttu-id="ff7ea-153">- StorageContext</span><span class="sxs-lookup"><span data-stu-id="ff7ea-153">-StorageContext</span></span>
<span data-ttu-id="ff7ea-154">Określa konto magazynu, które będzie używane do przechowywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-154">Specifies the storage account that will be used to store backups.</span></span>
<span data-ttu-id="ff7ea-155">Aby uzyskać obiekt **AzureStorageContext,** użyj New-AzureStorageContext cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-155">To obtain an **AzureStorageContext** object, use the New-AzureStorageContext cmdlet.</span></span>
<span data-ttu-id="ff7ea-156">Domyślnie jest to konto magazynu skojarzone z maszyną wirtualną programu SQL Server.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-156">The default is the storage account that is associated with the SQL Server virtual machine.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ff7ea-157">- KluczDazydzydów</span><span class="sxs-lookup"><span data-stu-id="ff7ea-157">-StorageKey</span></span>
<span data-ttu-id="ff7ea-158">Określa klucz magazynu konta magazynu obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-158">Specifies the storage key of the blob storage account.</span></span>

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

### <span data-ttu-id="ff7ea-159">— StorageUri</span><span class="sxs-lookup"><span data-stu-id="ff7ea-159">-StorageUri</span></span>
<span data-ttu-id="ff7ea-160">Określa identyfikator URI konta magazynu obiektów blob.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-160">Specifies the Uniform Resource Identifier (URI) of the blob storage account.</span></span>

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

### <span data-ttu-id="ff7ea-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff7ea-161">CommonParameters</span></span>
<span data-ttu-id="ff7ea-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff7ea-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff7ea-163">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff7ea-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff7ea-164">INPUTS</span></span>

### <span data-ttu-id="ff7ea-165">Brak</span><span class="sxs-lookup"><span data-stu-id="ff7ea-165">None</span></span>
<span data-ttu-id="ff7ea-166">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="ff7ea-166">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ff7ea-167">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ff7ea-167">OUTPUTS</span></span>

### <span data-ttu-id="ff7ea-168">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span><span class="sxs-lookup"><span data-stu-id="ff7ea-168">Microsoft.Azure.Commands.Compute.AutoBackupSettings</span></span>

## <span data-ttu-id="ff7ea-169">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ff7ea-169">NOTES</span></span>

## <span data-ttu-id="ff7ea-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ff7ea-170">RELATED LINKS</span></span>

[<span data-ttu-id="ff7ea-171">New-AzureVMSqlServerAutoPatchingConfig</span><span class="sxs-lookup"><span data-stu-id="ff7ea-171">New-AzureVMSqlServerAutoPatchingConfig</span></span>](./New-AzVMSqlServerAutoPatchingConfig.md)

[<span data-ttu-id="ff7ea-172">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="ff7ea-172">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)


