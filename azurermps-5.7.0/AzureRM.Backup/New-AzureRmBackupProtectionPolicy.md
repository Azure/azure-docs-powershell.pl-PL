---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3A7B0280-CE6E-4374-87AF-4C1015EB88FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: 4ea286ae6e3aec7f3eca961b5dc1452c717f3c59
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550668"
---
# <span data-ttu-id="c792e-101">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c792e-101">New-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="c792e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c792e-102">SYNOPSIS</span></span>
<span data-ttu-id="c792e-103">Tworzy zasady tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="c792e-103">Creates a Backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c792e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c792e-104">SYNTAX</span></span>

### <span data-ttu-id="c792e-105">NoScheduleParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c792e-105">NoScheduleParamSet (Default)</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-BackupTime] <DateTime>
 [[-DaysOfWeek] <String[]>] [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c792e-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="c792e-106">DailyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Daily] [-BackupTime] <DateTime>
 [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c792e-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="c792e-107">WeeklyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Weekly] [-BackupTime] <DateTime>
 [-DaysOfWeek] <String[]> [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c792e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c792e-108">DESCRIPTION</span></span>
<span data-ttu-id="c792e-109">Polecenie cmdlet **New-AzureRmBackupProtectionPolicy** tworzy zasady kopii zapasowej platformy Azure jako obiektu programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="c792e-109">The **New-AzureRmBackupProtectionPolicy** cmdlet creates an Azure Backup policy as an Azure PowerShell object.</span></span>

<span data-ttu-id="c792e-110">Zasady tworzenia kopii zapasowych określają, kiedy i jak często kopia zapasowa wykonuje kopię zapasową elementu.</span><span class="sxs-lookup"><span data-stu-id="c792e-110">A backup policy defines when and how often Backup backs up an item.</span></span>
<span data-ttu-id="c792e-111">Polecenie cmdlet Enable-AzureRmBackupProtection używa zasad tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="c792e-111">The Enable-AzureRmBackupProtection cmdlet uses a backup policy.</span></span>

## <span data-ttu-id="c792e-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c792e-112">EXAMPLES</span></span>

### <span data-ttu-id="c792e-113">Przykład 1: tworzenie codziennych zasad tworzenia kopii zapasowych przy użyciu codziennego i comiesięcznego przechowywania</span><span class="sxs-lookup"><span data-stu-id="c792e-113">Example 1: Create a daily backup policy with daily and monthly retention</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $ProtectionPolicy = New-AzureRmBackupProtectionPolicy -Name DailyBackup01 -Type AzureVM -Daily -BackupTime ([datetime]"3:30 PM") -RetentionPolicy ($Daily,$Monthly) -Vault $Vault
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="c792e-114">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="c792e-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="c792e-115">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="c792e-115">The command stores that object in the $Vault variable.</span></span>

<span data-ttu-id="c792e-116">Drugie polecenie tworzy zasady przechowywania przez 30 dni codziennego przechowywania, a następnie zapisuje je w zmiennej $Daily.</span><span class="sxs-lookup"><span data-stu-id="c792e-116">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>

<span data-ttu-id="c792e-117">Trzecie polecenie tworzy zasady przechowywania, które przechowują kopię zapasową w dziesiątym i dwudziestym dniu każdego miesiąca przez dwanaście miesięcy.</span><span class="sxs-lookup"><span data-stu-id="c792e-117">The third command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="c792e-118">Polecenie przechowuje zasady przechowywania w zmiennej $Monthly.</span><span class="sxs-lookup"><span data-stu-id="c792e-118">The command stores the retention policy in the $Monthly variable.</span></span>

<span data-ttu-id="c792e-119">Ostatnie polecenie tworzy zasady tworzenia kopii zapasowych dla magazynu w $Vault o godzinie codziennej kopii zapasowej 3:00 PM.</span><span class="sxs-lookup"><span data-stu-id="c792e-119">The final command creates a backup policy for the vault in $Vault that has a daily backup time of 3:00 PM.</span></span>
<span data-ttu-id="c792e-120">Polecenie przypisuje zasady przechowywania przechowywane w $Daily i $Monthly.</span><span class="sxs-lookup"><span data-stu-id="c792e-120">The command assigns the retention policies stored in $Daily and $Monthly.</span></span>
<span data-ttu-id="c792e-121">Polecenie zapisuje wyniki w zmiennej $ProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="c792e-121">The command stores the result in the $ProtectionPolicy variable.</span></span>

## <span data-ttu-id="c792e-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c792e-122">PARAMETERS</span></span>

### <span data-ttu-id="c792e-123">-Bez przestojów</span><span class="sxs-lookup"><span data-stu-id="c792e-123">-BackupTime</span></span>
<span data-ttu-id="c792e-124">Określa godzinę w postaci obiektu **DateTime** , dla operacji tworzenia kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="c792e-124">Specifies the time of day, as a **DateTime** object, for the backup operation.</span></span>
<span data-ttu-id="c792e-125">Aby uzyskać **wartość DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="c792e-125">To obtain a **DateTime** , use the Get-Date cmdlet.</span></span>
<span data-ttu-id="c792e-126">Aby uzyskać informacje o obiektach **DateTime** , wpisz `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="c792e-126">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c792e-127">-Codziennie</span><span class="sxs-lookup"><span data-stu-id="c792e-127">-Daily</span></span>
<span data-ttu-id="c792e-128">Wskazuje, że operacja tworzenia kopii zapasowej jest uruchamiana w harmonogramie dziennym.</span><span class="sxs-lookup"><span data-stu-id="c792e-128">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c792e-129">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="c792e-129">-DaysOfWeek</span></span>
<span data-ttu-id="c792e-130">Określa tablicę dni tygodnia.</span><span class="sxs-lookup"><span data-stu-id="c792e-130">Specifies an array of days of the week.</span></span>
<span data-ttu-id="c792e-131">Te zasady uruchamiają kopie zapasowe w dniach określonych przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c792e-131">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="c792e-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c792e-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c792e-133">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="c792e-133">Monday</span></span> 
- <span data-ttu-id="c792e-134">Wtorku</span><span class="sxs-lookup"><span data-stu-id="c792e-134">Tuesday</span></span> 
- <span data-ttu-id="c792e-135">Środa</span><span class="sxs-lookup"><span data-stu-id="c792e-135">Wednesday</span></span> 
- <span data-ttu-id="c792e-136">Czwartek</span><span class="sxs-lookup"><span data-stu-id="c792e-136">Thursday</span></span> 
- <span data-ttu-id="c792e-137">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="c792e-137">Friday</span></span> 
- <span data-ttu-id="c792e-138">Sobota</span><span class="sxs-lookup"><span data-stu-id="c792e-138">Saturday</span></span> 
- <span data-ttu-id="c792e-139">Niedziele</span><span class="sxs-lookup"><span data-stu-id="c792e-139">Sunday</span></span>

<span data-ttu-id="c792e-140">Jeśli określisz parametr *Weekly* , określ ten parametr.</span><span class="sxs-lookup"><span data-stu-id="c792e-140">If you specify the *Weekly* parameter, specify this parameter.</span></span>

```yaml
Type: String[]
Parameter Sets: NoScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases: 
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c792e-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c792e-141">-DefaultProfile</span></span>
<span data-ttu-id="c792e-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c792e-142">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c792e-143">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c792e-143">-Name</span></span>
<span data-ttu-id="c792e-144">Określa nazwę zasad tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="c792e-144">Specifies a name for the backup policy.</span></span>
<span data-ttu-id="c792e-145">Wybierz nazwę, która jest unikatowa w magazynie.</span><span class="sxs-lookup"><span data-stu-id="c792e-145">Select a name that is unique in the vault.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c792e-146">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="c792e-146">-RetentionPolicy</span></span>
<span data-ttu-id="c792e-147">Określa tablicę zasad przechowywania zasad tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="c792e-147">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="c792e-148">Aby uzyskać **AzureRmBackupRetentionPolicy** , użyj polecenia cmdlet New-AzureRmBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="c792e-148">To obtain an **AzureRmBackupRetentionPolicy** , use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c792e-149">-Type</span><span class="sxs-lookup"><span data-stu-id="c792e-149">-Type</span></span>
<span data-ttu-id="c792e-150">Określa typ elementu kopii zapasowej, którego dotyczą zasady.</span><span class="sxs-lookup"><span data-stu-id="c792e-150">Specifies the type of backup item to which the policy applies.</span></span>
<span data-ttu-id="c792e-151">Obecnie jedyną obsługiwaną wartością jest AzureVM.</span><span class="sxs-lookup"><span data-stu-id="c792e-151">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c792e-152">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="c792e-152">-Vault</span></span>
<span data-ttu-id="c792e-153">Określa magazyn kopii zapasowych Azure, do którego należą zasady tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="c792e-153">Specifies the Azure Backup vault to which the backup policy belongs.</span></span>
<span data-ttu-id="c792e-154">Aby uzyskać obiekt **AzureRmBackupVault** , użyj polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="c792e-154">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: AzureRMBackupVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c792e-155">-Co tydzień</span><span class="sxs-lookup"><span data-stu-id="c792e-155">-Weekly</span></span>
<span data-ttu-id="c792e-156">Wskazuje, że zasady tworzenia kopii zapasowych są wyzwalane co tydzień w co najmniej jednym dniu tygodnia.</span><span class="sxs-lookup"><span data-stu-id="c792e-156">Indicates that the backup policy is triggered weekly on one or more days of the week.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c792e-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c792e-157">CommonParameters</span></span>
<span data-ttu-id="c792e-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c792e-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c792e-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c792e-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c792e-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c792e-160">INPUTS</span></span>

### <span data-ttu-id="c792e-161">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c792e-161">None</span></span>

## <span data-ttu-id="c792e-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c792e-162">OUTPUTS</span></span>

### <span data-ttu-id="c792e-163">AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c792e-163">AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="c792e-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c792e-164">NOTES</span></span>
* <span data-ttu-id="c792e-165">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="c792e-165">None</span></span>

## <span data-ttu-id="c792e-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c792e-166">RELATED LINKS</span></span>

[<span data-ttu-id="c792e-167">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="c792e-167">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="c792e-168">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c792e-168">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="c792e-169">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="c792e-169">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="c792e-170">Nowe — AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="c792e-170">New-AzureRmBackupRetentionPolicyObject</span></span>](./New-AzureRmBackupRetentionPolicyObject.md)

[<span data-ttu-id="c792e-171">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c792e-171">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="c792e-172">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="c792e-172">Set-AzureRmBackupProtectionPolicy</span></span>](./Set-AzureRmBackupProtectionPolicy.md)


