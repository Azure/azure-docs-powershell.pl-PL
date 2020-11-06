---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 271426278c561ede4778e0ad69cf9ee4e6c0607e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523926"
---
# <span data-ttu-id="d8ec9-101">Set-AzsBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="d8ec9-101">Set-AzsBackupConfiguration</span></span>

## <span data-ttu-id="d8ec9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d8ec9-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ec9-103">Ustaw konfigurację kopii zapasowej w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d8ec9-103">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="d8ec9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d8ec9-104">SYNTAX</span></span>

### <span data-ttu-id="d8ec9-105">Aktualizuj (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d8ec9-105">Update (Default)</span></span>
```
Set-AzsBackupConfiguration [-ResourceGroupName <String>] [-Location <String>] [-Path <String>]
 [-Username <String>] [-Password <SecureString>] [-EncryptionKey <SecureString>]
 [-IsBackupSchedulerEnabled <Boolean>] [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>]
 [-AsJob] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d8ec9-106">Inputobject</span><span class="sxs-lookup"><span data-stu-id="d8ec9-106">InputObject</span></span>
```
Set-AzsBackupConfiguration -InputObject <BackupLocation> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d8ec9-107">Zasobów</span><span class="sxs-lookup"><span data-stu-id="d8ec9-107">ResourceId</span></span>
```
Set-AzsBackupConfiguration -ResourceId <String> [-Path <String>] [-Username <String>]
 [-Password <SecureString>] [-EncryptionKey <SecureString>] [-IsBackupSchedulerEnabled <Boolean>]
 [-BackupFrequencyInHours <Int32>] [-BackupRetentionPeriodInDays <Int32>] [-AsJob] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d8ec9-108">Opis</span><span class="sxs-lookup"><span data-stu-id="d8ec9-108">DESCRIPTION</span></span>
<span data-ttu-id="d8ec9-109">Ustaw konfigurację kopii zapasowej w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="d8ec9-109">Set the backup configuration at the specified location.</span></span>

## <span data-ttu-id="d8ec9-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d8ec9-110">EXAMPLES</span></span>

### <span data-ttu-id="d8ec9-111">--------------------------PRZYKŁAD 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="d8ec9-111">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Set-AzsBackupConfiguration -Path "\\***.***.***.***\Share" -Username "asdomain1\azurestackadmin" -Password $password  -EncryptionKey $encryptionKey
```

<span data-ttu-id="d8ec9-112">Ustaw konfigurację kopii zapasowej stosu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d8ec9-112">Set Azure Stack backup configuration.</span></span>

## <span data-ttu-id="d8ec9-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d8ec9-113">PARAMETERS</span></span>

### <span data-ttu-id="d8ec9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d8ec9-114">-AsJob</span></span>
<span data-ttu-id="d8ec9-115">Uruchamianie asynchronicznego jako zadania i zwracanie obiektu zadania.</span><span class="sxs-lookup"><span data-stu-id="d8ec9-115">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="d8ec9-116">-BackupFrequencyInHours</span><span class="sxs-lookup"><span data-stu-id="d8ec9-116">-BackupFrequencyInHours</span></span>
<span data-ttu-id="d8ec9-117">Interwał, wyrażony w godzinach, dotyczący częstotliwości wykonywania kopii zapasowej przez harmonogram.</span><span class="sxs-lookup"><span data-stu-id="d8ec9-117">The interval, in hours, for the frequency that the scheduler takes a backup.</span></span>

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

### <span data-ttu-id="d8ec9-118">-BackupRetentionPeriodInDays</span><span class="sxs-lookup"><span data-stu-id="d8ec9-118">-BackupRetentionPeriodInDays</span></span>
<span data-ttu-id="d8ec9-119">Okres przechowywania kopii zapasowych w lokalizacji przechowywania (w dniach).</span><span class="sxs-lookup"><span data-stu-id="d8ec9-119">The retention period, in days, for backups in the storage location.</span></span>

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

### <span data-ttu-id="d8ec9-120">-EncryptionKey</span><span class="sxs-lookup"><span data-stu-id="d8ec9-120">-EncryptionKey</span></span>
<span data-ttu-id="d8ec9-121">Klucz szyfrowania służący do szyfrowania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="d8ec9-121">Encryption key used to encrypt backups.</span></span>

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

### <span data-ttu-id="d8ec9-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="d8ec9-122">-InputObject</span></span>
<span data-ttu-id="d8ec9-123">Konfiguracja lokalizacji kopii zapasowej zwrócona przez Get-AzsBackupConfiguration.</span><span class="sxs-lookup"><span data-stu-id="d8ec9-123">Backup location configuration returned by Get-AzsBackupConfiguration.</span></span>

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

### <span data-ttu-id="d8ec9-124">-IsBackupSchedulerEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ec9-124">-IsBackupSchedulerEnabled</span></span>
<span data-ttu-id="d8ec9-125">Czy ma być włączony Harmonogram kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="d8ec9-125">Whether the backup scheduler should be enabled.</span></span>

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

### <span data-ttu-id="d8ec9-126">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="d8ec9-126">-Location</span></span>
<span data-ttu-id="d8ec9-127">Lokalizacja do skonfigurowania.</span><span class="sxs-lookup"><span data-stu-id="d8ec9-127">Location to configure.</span></span>

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

### <span data-ttu-id="d8ec9-128">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="d8ec9-128">-Password</span></span>
<span data-ttu-id="d8ec9-129">Hasło wymagane do uzyskania dostępu do lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="d8ec9-129">Password required to access backup location.</span></span>

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

### <span data-ttu-id="d8ec9-130">-Path</span><span class="sxs-lookup"><span data-stu-id="d8ec9-130">-Path</span></span>
<span data-ttu-id="d8ec9-131">Lokalizacja przechowywania kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="d8ec9-131">Location where backups will be stored.</span></span>

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

### <span data-ttu-id="d8ec9-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8ec9-132">-ResourceGroupName</span></span>
<span data-ttu-id="d8ec9-133">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d8ec9-133">Name of the resource group.</span></span>

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

### <span data-ttu-id="d8ec9-134">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d8ec9-134">-ResourceId</span></span>
<span data-ttu-id="d8ec9-135">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="d8ec9-135">The resource id.</span></span>

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

### <span data-ttu-id="d8ec9-136">-Username</span><span class="sxs-lookup"><span data-stu-id="d8ec9-136">-Username</span></span>
<span data-ttu-id="d8ec9-137">Nazwa użytkownika wymagana do uzyskania dostępu do lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="d8ec9-137">Username required to access backup location.</span></span>

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

### <span data-ttu-id="d8ec9-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8ec9-138">-Confirm</span></span>
<span data-ttu-id="d8ec9-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8ec9-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8ec9-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8ec9-140">-WhatIf</span></span>
<span data-ttu-id="d8ec9-141">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8ec9-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8ec9-142">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d8ec9-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8ec9-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ec9-143">CommonParameters</span></span>
<span data-ttu-id="d8ec9-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8ec9-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ec9-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d8ec9-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ec9-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8ec9-146">INPUTS</span></span>

## <span data-ttu-id="d8ec9-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d8ec9-147">OUTPUTS</span></span>

### <span data-ttu-id="d8ec9-148">Microsoft. AzureStack. Management. Backup. admin. models. BackupLocation</span><span class="sxs-lookup"><span data-stu-id="d8ec9-148">Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation</span></span>

## <span data-ttu-id="d8ec9-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d8ec9-149">NOTES</span></span>

## <span data-ttu-id="d8ec9-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8ec9-150">RELATED LINKS</span></span>

