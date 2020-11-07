---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: fd5f27a942a33082b9488f74cac2779107f7371f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888713"
---
# <span data-ttu-id="2f41d-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="2f41d-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="2f41d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2f41d-102">SYNOPSIS</span></span>
<span data-ttu-id="2f41d-103">Ustaw konfigurację kopii zapasowej w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="2f41d-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="2f41d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2f41d-104">SYNTAX</span></span>

### <span data-ttu-id="2f41d-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="2f41d-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionCertPath <String>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2f41d-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="2f41d-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionCertPath <String>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2f41d-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="2f41d-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionCertPath <String>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2f41d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2f41d-108">DESCRIPTION</span></span>
<span data-ttu-id="2f41d-109">Ustaw konfigurację kopii zapasowej w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="2f41d-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="2f41d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2f41d-110">EXAMPLES</span></span>

### <span data-ttu-id="2f41d-111">PRZYKŁAD 1</span><span class="sxs-lookup"><span data-stu-id="2f41d-111">EXAMPLE 1</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionCertPath $encryptionCertPath
```

<span data-ttu-id="2f41d-112">Ustaw konfigurację kopii zapasowej stosu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2f41d-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="2f41d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2f41d-113">PARAMETERS</span></span>

### <span data-ttu-id="2f41d-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2f41d-114">-AsJob</span></span>
<span data-ttu-id="2f41d-115">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="2f41d-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f41d-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="2f41d-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="2f41d-117">Interwał, wyrażony w godzinach, dotyczący częstotliwości wykonywania kopii zapasowej przez harmonogram.</span><span class="sxs-lookup"><span data-stu-id="2f41d-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f41d-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="2f41d-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="2f41d-119">Okres przechowywania kopii zapasowych w lokalizacji przechowywania (w dniach).</span><span class="sxs-lookup"><span data-stu-id="2f41d-119">The retention period, in days, for backups in the storage location.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f41d-120">-EncryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="2f41d-120">-EncryptionCertPath</span></span>
<span data-ttu-id="2f41d-121">Ścieżka do pliku certyfikatu szyfrowania z kluczem publicznym (CER).</span><span class="sxs-lookup"><span data-stu-id="2f41d-121">Path to the encryption cert file with public key (.cer).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f41d-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2f41d-122">-InputObject</span></span>
<span data-ttu-id="2f41d-123">Konfiguracja lokalizacji kopii zapasowej zwrócona przez Get-AzsBackupConfiguration.</span><span class="sxs-lookup"><span data-stu-id="2f41d-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

```yaml
Type: Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2f41d-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="2f41d-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="2f41d-125">Czy ma być włączony Harmonogram kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="2f41d-125">Whether the backup scheduler should be enabled.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f41d-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2f41d-126">-Location</span></span>
<span data-ttu-id="2f41d-127">Lokalizacja do skonfigurowania.</span><span class="sxs-lookup"><span data-stu-id="2f41d-127">Location to configure.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f41d-128">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="2f41d-128">-Password</span></span>
<span data-ttu-id="2f41d-129">Hasło wymagane do uzyskania dostępu do lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="2f41d-129">Password required to access backup location.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f41d-130">-Path</span><span class="sxs-lookup"><span data-stu-id="2f41d-130">-Path</span></span>
<span data-ttu-id="2f41d-131">Lokalizacja przechowywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="2f41d-131">Location where backups will be stored.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: BackupShare

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f41d-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f41d-132">-ResourceGroupName</span></span>
<span data-ttu-id="2f41d-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2f41d-133">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Update
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f41d-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2f41d-134">-ResourceId</span></span>
<span data-ttu-id="2f41d-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="2f41d-135">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2f41d-136">-Username</span><span class="sxs-lookup"><span data-stu-id="2f41d-136">-Username</span></span>
<span data-ttu-id="2f41d-137">Nazwa użytkownika wymagana do uzyskania dostępu do lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="2f41d-137">Username required to access backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2f41d-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f41d-138">-Confirm</span></span>
<span data-ttu-id="2f41d-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f41d-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f41d-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f41d-140">-WhatIf</span></span>
<span data-ttu-id="2f41d-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f41d-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f41d-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2f41d-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f41d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f41d-143">CommonParameters</span></span>
<span data-ttu-id="2f41d-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f41d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f41d-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2f41d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f41d-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f41d-146">INPUTS</span></span>

## <span data-ttu-id="2f41d-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2f41d-147">OUTPUTS</span></span>

### <span data-ttu-id="2f41d-148">Microsoft. AzureStack. Management. Backup. admin. models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="2f41d-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="2f41d-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2f41d-149">NOTES</span></span>

## <span data-ttu-id="2f41d-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f41d-150">RELATED LINKS</span></span>
