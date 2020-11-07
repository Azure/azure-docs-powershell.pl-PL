---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/set-azsbackupconfiguration
schema: 2.0.0
ms.openlocfilehash: c99e2c549cc865a5f7f9ad0d7c3252cbf6651e98
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93894049"
---
# <span data-ttu-id="08e4e-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="08e4e-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="08e4e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="08e4e-102">SYNOPSIS</span></span>
<span data-ttu-id="08e4e-103">Aktualizowanie lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="08e4e-103">Update a backup location.</span></span>

## <span data-ttu-id="08e4e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="08e4e-104">SYNTAX</span></span>

### <span data-ttu-id="08e4e-105">UpdateExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="08e4e-105">UpdateExpanded (Default)</span></span>
```
Set-AzsBackupConfiguration [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-EncryptionCertPath <String>]
 [-IsBackupSchedulerEnabled] [-Password <SecureString>] [-Path <String>] [-Tag <Hashtable>]
 [-UserName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="08e4e-106">Aktualizowane</span><span class="sxs-lookup"><span data-stu-id="08e4e-106">Update</span></span>
```
Set-AzsBackupConfiguration -Backup <IBackupLocation> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="08e4e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="08e4e-107">DESCRIPTION</span></span>
<span data-ttu-id="08e4e-108">Aktualizowanie lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="08e4e-108">Update a backup location.</span></span>

## <span data-ttu-id="08e4e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="08e4e-109">EXAMPLES</span></span>

### <span data-ttu-id="08e4e-110">Przykład 1: Ustawianie konfiguracji kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="08e4e-110">Example 1: Set backup configuration</span></span>
```powershell
PS C:\> Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionCertPath $encryptionCertPath

```

<span data-ttu-id="08e4e-111">Ustaw konfigurację kopii zapasowej stosu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="08e4e-111">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="08e4e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="08e4e-112">PARAMETERS</span></span>

### <span data-ttu-id="08e4e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="08e4e-113">-AsJob</span></span>
<span data-ttu-id="08e4e-114">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="08e4e-114">Run the command as a job</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08e4e-115">— Kopia zapasowa</span><span class="sxs-lookup"><span data-stu-id="08e4e-115">-Backup</span></span>
<span data-ttu-id="08e4e-116">Informacje o lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="08e4e-116">Information about the backup location.</span></span>
<span data-ttu-id="08e4e-117">Aby skonstruować, zobacz sekcję notatki dla właściwości kopii ZAPASowej i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="08e4e-117">To construct, see NOTES section for BACKUP properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation
Parameter Sets: Update
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="08e4e-118">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="08e4e-118">-BackupFrequencyInHours</span></span>
<span data-ttu-id="08e4e-119">Interwał, wyrażony w godzinach, dotyczący częstotliwości wykonywania kopii zapasowej przez harmonogram.</span><span class="sxs-lookup"><span data-stu-id="08e4e-119">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08e4e-120">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="08e4e-120">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="08e4e-121">Okres przechowywania (w dniach) dla kopii zapasowej w lokalizacji przechowywania.</span><span class="sxs-lookup"><span data-stu-id="08e4e-121">The retention period, in days, for backs in the storage location.</span></span>

```yaml
Type: System.Int32
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08e4e-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="08e4e-122">-DefaultProfile</span></span>
<span data-ttu-id="08e4e-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="08e4e-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08e4e-124">-EncryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="08e4e-124">-EncryptionCertPath</span></span>
<span data-ttu-id="08e4e-125">Ścieżka do pliku certyfikatu szyfrowania z kluczem publicznym (CER).</span><span class="sxs-lookup"><span data-stu-id="08e4e-125">Path to the encryption cert file with public key (.cer).</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08e4e-126">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="08e4e-126">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="08e4e-127">Prawda, jeśli jest włączony Harmonogram kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="08e4e-127">True if the backup scheduler is enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08e4e-128">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="08e4e-128">-Location</span></span>
<span data-ttu-id="08e4e-129">Nazwa lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="08e4e-129">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08e4e-130">-Nowait</span><span class="sxs-lookup"><span data-stu-id="08e4e-130">-NoWait</span></span>
<span data-ttu-id="08e4e-131">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="08e4e-131">Run the command asynchronously</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08e4e-132">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="08e4e-132">-Password</span></span>
<span data-ttu-id="08e4e-133">Hasło dostępu do lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="08e4e-133">Password to access the location.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08e4e-134">-Path</span><span class="sxs-lookup"><span data-stu-id="08e4e-134">-Path</span></span>
<span data-ttu-id="08e4e-135">Ścieżka do lokalizacji aktualizacji</span><span class="sxs-lookup"><span data-stu-id="08e4e-135">Path to the update location</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08e4e-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="08e4e-136">-ResourceGroupName</span></span>
<span data-ttu-id="08e4e-137">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="08e4e-137">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08e4e-138">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="08e4e-138">-SubscriptionId</span></span>
<span data-ttu-id="08e4e-139">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="08e4e-139">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="08e4e-140">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="08e4e-140">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08e4e-141">-Tag</span><span class="sxs-lookup"><span data-stu-id="08e4e-141">-Tag</span></span>
<span data-ttu-id="08e4e-142">Lista par kluczy wartości.</span><span class="sxs-lookup"><span data-stu-id="08e4e-142">List of key value pairs.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08e4e-143">-UserName</span><span class="sxs-lookup"><span data-stu-id="08e4e-143">-UserName</span></span>
<span data-ttu-id="08e4e-144">Nazwa_użytkownika, aby uzyskać dostęp do lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="08e4e-144">Username to access the location.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08e4e-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="08e4e-145">-Confirm</span></span>
<span data-ttu-id="08e4e-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08e4e-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08e4e-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="08e4e-147">-WhatIf</span></span>
<span data-ttu-id="08e4e-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="08e4e-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="08e4e-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="08e4e-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="08e4e-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="08e4e-150">CommonParameters</span></span>
<span data-ttu-id="08e4e-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="08e4e-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="08e4e-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="08e4e-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="08e4e-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="08e4e-153">INPUTS</span></span>

### <span data-ttu-id="08e4e-154">Microsoft. Azure. PowerShell. polecenia. BackupAdmin. models. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="08e4e-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>

## <span data-ttu-id="08e4e-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="08e4e-155">OUTPUTS</span></span>

### <span data-ttu-id="08e4e-156">Microsoft. Azure. PowerShell. polecenia. BackupAdmin. models. Api20180901. IBackupLocation</span><span class="sxs-lookup"><span data-stu-id="08e4e-156">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IBackupLocation</span></span>



## <span data-ttu-id="08e4e-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="08e4e-157">NOTES</span></span>

<span data-ttu-id="08e4e-158">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="08e4e-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="08e4e-159">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="08e4e-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="08e4e-160">BACKUP <IBackupLocation> : informacje o lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="08e4e-160">BACKUP <IBackupLocation>: Information about the backup location.</span></span>
  - <span data-ttu-id="08e4e-161">`[Location <String>]`: Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="08e4e-161">`[Location <String>]`: Location of the resource.</span></span>
  - <span data-ttu-id="08e4e-162">`[Tag <IResourceTags>]`: Lista par kluczy wartości.</span><span class="sxs-lookup"><span data-stu-id="08e4e-162">`[Tag <IResourceTags>]`: List of key value pairs.</span></span>
    - <span data-ttu-id="08e4e-163">`[(Any) <String>]`: Wskazuje, że do tego obiektu można dodać dowolną właściwość.</span><span class="sxs-lookup"><span data-stu-id="08e4e-163">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="08e4e-164">`[BackupFrequencyInHours <Int32?>]`: Interwał (w godzinach) częstotliwości wykonywania kopii zapasowej przez harmonogram.</span><span class="sxs-lookup"><span data-stu-id="08e4e-164">`[BackupFrequencyInHours <Int32?>]`: The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>
  - <span data-ttu-id="08e4e-165">`[BackupRetentionPeriodInDays <Int32?>]`: Okres przechowywania (w dniach) dla kopii zapasowej w lokalizacji przechowywania.</span><span class="sxs-lookup"><span data-stu-id="08e4e-165">`[BackupRetentionPeriodInDays <Int32?>]`: The retention period, in days, for backs in the storage location.</span></span>
  - <span data-ttu-id="08e4e-166">`[EncryptionCertBase64 <String>]`: Dane surowe Base64 dotyczące certyfikatu szyfrowania kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="08e4e-166">`[EncryptionCertBase64 <String>]`: The base64 raw data for the backup encryption certificate.</span></span>
  - <span data-ttu-id="08e4e-167">`[IsBackupSchedulerEnabled <Boolean?>]`Jeśli jest włączony Harmonogram kopii zapasowych, należy wykonać następujące czynności: prawda.</span><span class="sxs-lookup"><span data-stu-id="08e4e-167">`[IsBackupSchedulerEnabled <Boolean?>]`: True if the backup scheduler is enabled.</span></span>
  - <span data-ttu-id="08e4e-168">`[Password <String>]`: Hasło dostępu do lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="08e4e-168">`[Password <String>]`: Password to access the location.</span></span>
  - <span data-ttu-id="08e4e-169">`[Path <String>]`: Ścieżka do lokalizacji aktualizacji</span><span class="sxs-lookup"><span data-stu-id="08e4e-169">`[Path <String>]`: Path to the update location</span></span>
  - <span data-ttu-id="08e4e-170">`[UserName <String>]`: Nazwa użytkownika, aby uzyskać dostęp do lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="08e4e-170">`[UserName <String>]`: Username to access the location.</span></span>

## <span data-ttu-id="08e4e-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="08e4e-171">RELATED LINKS</span></span>

