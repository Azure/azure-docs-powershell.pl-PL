---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: e7b6e8139f201a69684d4236a5e84e89f6607c5c
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2020
ms.locfileid: "93888818"
---
# <span data-ttu-id="ea8c1-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="ea8c1-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="ea8c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ea8c1-102">SYNOPSIS</span></span>
<span data-ttu-id="ea8c1-103">Ustaw konfigurację kopii zapasowej w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="ea8c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ea8c1-104">SYNTAX</span></span>

### <span data-ttu-id="ea8c1-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="ea8c1-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionKey <SecureString>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ea8c1-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="ea8c1-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ea8c1-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="ea8c1-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ea8c1-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ea8c1-108">DESCRIPTION</span></span>
<span data-ttu-id="ea8c1-109">Ustaw konfigurację kopii zapasowej w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="ea8c1-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ea8c1-110">EXAMPLES</span></span>

### <span data-ttu-id="ea8c1-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="ea8c1-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionKey $encryptionKey
```

<span data-ttu-id="ea8c1-112">Ustaw konfigurację kopii zapasowej stosu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="ea8c1-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ea8c1-113">PARAMETERS</span></span>

### <span data-ttu-id="ea8c1-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ea8c1-114">-AsJob</span></span>
<span data-ttu-id="ea8c1-115">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-115">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8c1-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="ea8c1-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="ea8c1-117">Interwał, wyrażony w godzinach, dotyczący częstotliwości wykonywania kopii zapasowej przez harmonogram.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8c1-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="ea8c1-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="ea8c1-119">Okres przechowywania kopii zapasowych w lokalizacji przechowywania (w dniach).</span><span class="sxs-lookup"><span data-stu-id="ea8c1-119">The retention period, in days, for backups in the storage location.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: 0
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8c1-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="ea8c1-120">-EncryptionKey</span></span>
<span data-ttu-id="ea8c1-121">Klucz szyfrowania służący do szyfrowania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-121">Encryption key used to encrypt backups.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8c1-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ea8c1-122">-InputObject</span></span>
<span data-ttu-id="ea8c1-123">Konfiguracja lokalizacji kopii zapasowej zwrócona przez Get-AzsBackupConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

```yaml
Type: BackupLocation
Parameter Sets: InputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ea8c1-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="ea8c1-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="ea8c1-125">Czy ma być włączony Harmonogram kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-125">Whether the backup scheduler should be enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8c1-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ea8c1-126">-Location</span></span>
<span data-ttu-id="ea8c1-127">Lokalizacja do skonfigurowania.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-127">Location to configure.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8c1-128">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="ea8c1-128">-Password</span></span>
<span data-ttu-id="ea8c1-129">Hasło wymagane do uzyskania dostępu do lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-129">Password required to access backup location.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8c1-130">-Path</span><span class="sxs-lookup"><span data-stu-id="ea8c1-130">-Path</span></span>
<span data-ttu-id="ea8c1-131">Lokalizacja przechowywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-131">Location where backups will be stored.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: BackupShare

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8c1-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ea8c1-132">-ResourceGroupName</span></span>
<span data-ttu-id="ea8c1-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-133">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: Update
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8c1-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ea8c1-134">-ResourceId</span></span>
<span data-ttu-id="ea8c1-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-135">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ea8c1-136">-Username</span><span class="sxs-lookup"><span data-stu-id="ea8c1-136">-Username</span></span>
<span data-ttu-id="ea8c1-137">Nazwa użytkownika wymagana do uzyskania dostępu do lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-137">Username required to access backup location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8c1-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ea8c1-138">-Confirm</span></span>
<span data-ttu-id="ea8c1-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8c1-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ea8c1-140">-WhatIf</span></span>
<span data-ttu-id="ea8c1-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ea8c1-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ea8c1-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ea8c1-143">CommonParameters</span></span>
<span data-ttu-id="ea8c1-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ea8c1-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ea8c1-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ea8c1-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ea8c1-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ea8c1-146">INPUTS</span></span>

## <span data-ttu-id="ea8c1-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ea8c1-147">OUTPUTS</span></span>

### <span data-ttu-id="ea8c1-148">Microsoft. AzureStack. Management. Backup. admin. models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="ea8c1-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="ea8c1-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ea8c1-149">NOTES</span></span>

## <span data-ttu-id="ea8c1-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ea8c1-150">RELATED LINKS</span></span>

