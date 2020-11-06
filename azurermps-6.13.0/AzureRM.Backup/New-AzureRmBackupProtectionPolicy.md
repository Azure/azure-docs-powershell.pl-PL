---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 3A7B0280-CE6E-4374-87AF-4C1015EB88FA
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/new-azurermbackupprotectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/New-AzureRmBackupProtectionPolicy.md
ms.openlocfilehash: ce4550d4b0b0206db3a28f11a58ac4384ecbac60
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526322"
---
# <span data-ttu-id="42e4b-101">New-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="42e4b-101">New-AzureRmBackupProtectionPolicy</span></span>

## <span data-ttu-id="42e4b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="42e4b-102">SYNOPSIS</span></span>
<span data-ttu-id="42e4b-103">Tworzy zasady tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="42e4b-103">Creates a Backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="42e4b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="42e4b-104">SYNTAX</span></span>

### <span data-ttu-id="42e4b-105">NoScheduleParamSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="42e4b-105">NoScheduleParamSet (Default)</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-BackupTime] <DateTime>
 [[-DaysOfWeek] <String[]>] [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42e4b-106">DailyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="42e4b-106">DailyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Daily] [-BackupTime] <DateTime>
 [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="42e4b-107">WeeklyScheduleParamSet</span><span class="sxs-lookup"><span data-stu-id="42e4b-107">WeeklyScheduleParamSet</span></span>
```
New-AzureRmBackupProtectionPolicy [-Name] <String> [-Type] <String> [-Weekly] [-BackupTime] <DateTime>
 [-DaysOfWeek] <String[]> [-RetentionPolicy] <AzureRMBackupRetentionPolicy[]> [-Vault] <AzureRMBackupVault>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="42e4b-108">Opis</span><span class="sxs-lookup"><span data-stu-id="42e4b-108">DESCRIPTION</span></span>
<span data-ttu-id="42e4b-109">Polecenie cmdlet **New-AzureRmBackupProtectionPolicy** tworzy zasady kopii zapasowej platformy Azure jako obiektu programu Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="42e4b-109">The **New-AzureRmBackupProtectionPolicy** cmdlet creates an Azure Backup policy as an Azure PowerShell object.</span></span>
<span data-ttu-id="42e4b-110">Zasady tworzenia kopii zapasowych określają, kiedy i jak często kopia zapasowa wykonuje kopię zapasową elementu.</span><span class="sxs-lookup"><span data-stu-id="42e4b-110">A backup policy defines when and how often Backup backs up an item.</span></span>
<span data-ttu-id="42e4b-111">Polecenie cmdlet Enable-AzureRmBackupProtection używa zasad tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="42e4b-111">The Enable-AzureRmBackupProtection cmdlet uses a backup policy.</span></span>

## <span data-ttu-id="42e4b-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="42e4b-112">EXAMPLES</span></span>

### <span data-ttu-id="42e4b-113">Przykład 1: tworzenie codziennych zasad tworzenia kopii zapasowych przy użyciu codziennego i comiesięcznego przechowywania</span><span class="sxs-lookup"><span data-stu-id="42e4b-113">Example 1: Create a daily backup policy with daily and monthly retention</span></span>
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> $Daily = New-AzureRmBackupRetentionPolicyObject -DailyRetention -Retention 30
PS C:\> $Monthly = New-AzureRmBackupRetentionPolicyObject -MonthlyRetentionInDailyFormat -DaysOfMonth (10, 20) -Retention 12
PS C:\> $ProtectionPolicy = New-AzureRmBackupProtectionPolicy -Name DailyBackup01 -Type AzureVM -Daily -BackupTime ([datetime]"3:30 PM") -RetentionPolicy ($Daily,$Monthly) -Vault $Vault
Name                      Type               ScheduleType       BackupTime
----                      ----               ------------       ----------
DailyBkp                  AzureVM            Daily              26-Aug-15 3:00:00 PM
```

<span data-ttu-id="42e4b-114">Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="42e4b-114">The first command gets the vault named Vault03 by using the Get-AzureRmBackupVault cmdlet.</span></span>
<span data-ttu-id="42e4b-115">Polecenie zapisuje ten obiekt w zmiennej $Vault.</span><span class="sxs-lookup"><span data-stu-id="42e4b-115">The command stores that object in the $Vault variable.</span></span>
<span data-ttu-id="42e4b-116">Drugie polecenie tworzy zasady przechowywania przez 30 dni codziennego przechowywania, a następnie zapisuje je w zmiennej $Daily.</span><span class="sxs-lookup"><span data-stu-id="42e4b-116">The second command creates a retention policy for 30 days of daily retention, and then stores it in the $Daily variable.</span></span>
<span data-ttu-id="42e4b-117">Trzecie polecenie tworzy zasady przechowywania, które przechowują kopię zapasową w dziesiątym i dwudziestym dniu każdego miesiąca przez dwanaście miesięcy.</span><span class="sxs-lookup"><span data-stu-id="42e4b-117">The third command creates a retention policy that keeps the backup on the tenth and the twentieth of each month for twelve months.</span></span>
<span data-ttu-id="42e4b-118">Polecenie przechowuje zasady przechowywania w zmiennej $Monthly.</span><span class="sxs-lookup"><span data-stu-id="42e4b-118">The command stores the retention policy in the $Monthly variable.</span></span>
<span data-ttu-id="42e4b-119">Ostatnie polecenie tworzy zasady tworzenia kopii zapasowych dla magazynu w $Vault o godzinie codziennej kopii zapasowej 3:00 PM.</span><span class="sxs-lookup"><span data-stu-id="42e4b-119">The final command creates a backup policy for the vault in $Vault that has a daily backup time of 3:00 PM.</span></span>
<span data-ttu-id="42e4b-120">Polecenie przypisuje zasady przechowywania przechowywane w $Daily i $Monthly.</span><span class="sxs-lookup"><span data-stu-id="42e4b-120">The command assigns the retention policies stored in $Daily and $Monthly.</span></span>
<span data-ttu-id="42e4b-121">Polecenie zapisuje wyniki w zmiennej $ProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="42e4b-121">The command stores the result in the $ProtectionPolicy variable.</span></span>

## <span data-ttu-id="42e4b-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="42e4b-122">PARAMETERS</span></span>

### <span data-ttu-id="42e4b-123">-Bez przestojów</span><span class="sxs-lookup"><span data-stu-id="42e4b-123">-BackupTime</span></span>
<span data-ttu-id="42e4b-124">Określa godzinę w postaci obiektu **DateTime** , dla operacji tworzenia kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="42e4b-124">Specifies the time of day, as a **DateTime** object, for the backup operation.</span></span>
<span data-ttu-id="42e4b-125">Aby uzyskać **wartość DateTime** , użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="42e4b-125">To obtain a **DateTime** , use the Get-Date cmdlet.</span></span>
<span data-ttu-id="42e4b-126">Aby uzyskać informacje o obiektach **DateTime** , wpisz `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="42e4b-126">For information about **DateTime** objects, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42e4b-127">-Codziennie</span><span class="sxs-lookup"><span data-stu-id="42e4b-127">-Daily</span></span>
<span data-ttu-id="42e4b-128">Wskazuje, że operacja tworzenia kopii zapasowej jest uruchamiana w harmonogramie dziennym.</span><span class="sxs-lookup"><span data-stu-id="42e4b-128">Indicates that the backup operation runs on a Daily schedule.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DailyScheduleParamSet
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e4b-129">-DaysOfWeek</span><span class="sxs-lookup"><span data-stu-id="42e4b-129">-DaysOfWeek</span></span>
<span data-ttu-id="42e4b-130">Określa tablicę dni tygodnia.</span><span class="sxs-lookup"><span data-stu-id="42e4b-130">Specifies an array of days of the week.</span></span>
<span data-ttu-id="42e4b-131">Te zasady uruchamiają kopie zapasowe w dniach określonych przez ten parametr.</span><span class="sxs-lookup"><span data-stu-id="42e4b-131">This policy runs backups on the days specified by this parameter.</span></span>
<span data-ttu-id="42e4b-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="42e4b-132">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="42e4b-133">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="42e4b-133">Monday</span></span> 
- <span data-ttu-id="42e4b-134">Wtorku</span><span class="sxs-lookup"><span data-stu-id="42e4b-134">Tuesday</span></span> 
- <span data-ttu-id="42e4b-135">Środa</span><span class="sxs-lookup"><span data-stu-id="42e4b-135">Wednesday</span></span> 
- <span data-ttu-id="42e4b-136">Czwartek</span><span class="sxs-lookup"><span data-stu-id="42e4b-136">Thursday</span></span> 
- <span data-ttu-id="42e4b-137">Poniedziałek</span><span class="sxs-lookup"><span data-stu-id="42e4b-137">Friday</span></span> 
- <span data-ttu-id="42e4b-138">Sobota</span><span class="sxs-lookup"><span data-stu-id="42e4b-138">Saturday</span></span> 
- <span data-ttu-id="42e4b-139">Niedziela Jeśli określisz parametr *tygodniowy* , określ ten parametr.</span><span class="sxs-lookup"><span data-stu-id="42e4b-139">Sunday If you specify the *Weekly* parameter, specify this parameter.</span></span>

```yaml
Type: System.String[]
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
Type: System.String[]
Parameter Sets: WeeklyScheduleParamSet
Aliases:
Accepted values: Monday, Tuesday, Wednesday, Thursday, Friday, Saturday, Sunday

Required: True
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42e4b-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42e4b-140">-DefaultProfile</span></span>
<span data-ttu-id="42e4b-141">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="42e4b-141">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="42e4b-142">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="42e4b-142">-Name</span></span>
<span data-ttu-id="42e4b-143">Określa nazwę zasad tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="42e4b-143">Specifies a name for the backup policy.</span></span>
<span data-ttu-id="42e4b-144">Wybierz nazwę, która jest unikatowa w magazynie.</span><span class="sxs-lookup"><span data-stu-id="42e4b-144">Select a name that is unique in the vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e4b-145">-RetentionPolicy</span><span class="sxs-lookup"><span data-stu-id="42e4b-145">-RetentionPolicy</span></span>
<span data-ttu-id="42e4b-146">Określa tablicę zasad przechowywania zasad tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="42e4b-146">Specifies an array of retention policies for the backup policy.</span></span>
<span data-ttu-id="42e4b-147">Aby uzyskać **AzureRmBackupRetentionPolicy** , użyj polecenia cmdlet New-AzureRmBackupRetentionPolicyObject.</span><span class="sxs-lookup"><span data-stu-id="42e4b-147">To obtain an **AzureRmBackupRetentionPolicy** , use the New-AzureRmBackupRetentionPolicyObject cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42e4b-148">-Type</span><span class="sxs-lookup"><span data-stu-id="42e4b-148">-Type</span></span>
<span data-ttu-id="42e4b-149">Określa typ elementu kopii zapasowej, którego dotyczą zasady.</span><span class="sxs-lookup"><span data-stu-id="42e4b-149">Specifies the type of backup item to which the policy applies.</span></span>
<span data-ttu-id="42e4b-150">Obecnie jedyną obsługiwaną wartością jest AzureVM.</span><span class="sxs-lookup"><span data-stu-id="42e4b-150">Currently, the only supported value is AzureVM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="42e4b-151">-Magazyn</span><span class="sxs-lookup"><span data-stu-id="42e4b-151">-Vault</span></span>
<span data-ttu-id="42e4b-152">Określa magazyn kopii zapasowych Azure, do którego należą zasady tworzenia kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="42e4b-152">Specifies the Azure Backup vault to which the backup policy belongs.</span></span>
<span data-ttu-id="42e4b-153">Aby uzyskać obiekt **AzureRmBackupVault** , użyj polecenia cmdlet Get-AzureRmBackupVault.</span><span class="sxs-lookup"><span data-stu-id="42e4b-153">To obtain an **AzureRmBackupVault** object, use the Get-AzureRmBackupVault cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="42e4b-154">-Co tydzień</span><span class="sxs-lookup"><span data-stu-id="42e4b-154">-Weekly</span></span>
<span data-ttu-id="42e4b-155">Wskazuje, że zasady tworzenia kopii zapasowych są wyzwalane co tydzień w co najmniej jednym dniu tygodnia.</span><span class="sxs-lookup"><span data-stu-id="42e4b-155">Indicates that the backup policy is triggered weekly on one or more days of the week.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: WeeklyScheduleParamSet
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="42e4b-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42e4b-156">CommonParameters</span></span>
<span data-ttu-id="42e4b-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42e4b-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42e4b-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="42e4b-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42e4b-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42e4b-159">INPUTS</span></span>

### <span data-ttu-id="42e4b-160">System. String</span><span class="sxs-lookup"><span data-stu-id="42e4b-160">System.String</span></span>

### <span data-ttu-id="42e4b-161">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="42e4b-161">System.DateTime</span></span>

### <span data-ttu-id="42e4b-162">System. String []</span><span class="sxs-lookup"><span data-stu-id="42e4b-162">System.String[]</span></span>

### <span data-ttu-id="42e4b-163">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupRetentionPolicy []</span><span class="sxs-lookup"><span data-stu-id="42e4b-163">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupRetentionPolicy[]</span></span>

### <span data-ttu-id="42e4b-164">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupVault</span><span class="sxs-lookup"><span data-stu-id="42e4b-164">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault</span></span>
<span data-ttu-id="42e4b-165">Parametry: Magazyn (ByValue)</span><span class="sxs-lookup"><span data-stu-id="42e4b-165">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="42e4b-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="42e4b-166">OUTPUTS</span></span>

### <span data-ttu-id="42e4b-167">Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="42e4b-167">Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupProtectionPolicy</span></span>

## <span data-ttu-id="42e4b-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="42e4b-168">NOTES</span></span>
* <span data-ttu-id="42e4b-169">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="42e4b-169">None</span></span>

## <span data-ttu-id="42e4b-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42e4b-170">RELATED LINKS</span></span>

[<span data-ttu-id="42e4b-171">Enable-AzureRmBackupProtection</span><span class="sxs-lookup"><span data-stu-id="42e4b-171">Enable-AzureRmBackupProtection</span></span>](./Enable-AzureRmBackupProtection.md)

[<span data-ttu-id="42e4b-172">Get-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="42e4b-172">Get-AzureRmBackupProtectionPolicy</span></span>](./Get-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="42e4b-173">Get-AzureRmBackupVault</span><span class="sxs-lookup"><span data-stu-id="42e4b-173">Get-AzureRmBackupVault</span></span>](./Get-AzureRmBackupVault.md)

[<span data-ttu-id="42e4b-174">Nowe — AzureRmBackupRetentionPolicyObject</span><span class="sxs-lookup"><span data-stu-id="42e4b-174">New-AzureRmBackupRetentionPolicyObject</span></span>](./New-AzureRmBackupRetentionPolicyObject.md)

[<span data-ttu-id="42e4b-175">Remove-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="42e4b-175">Remove-AzureRmBackupProtectionPolicy</span></span>](./Remove-AzureRmBackupProtectionPolicy.md)

[<span data-ttu-id="42e4b-176">Set-AzureRmBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="42e4b-176">Set-AzureRmBackupProtectionPolicy</span></span>](./Set-AzureRmBackupProtectionPolicy.md)


