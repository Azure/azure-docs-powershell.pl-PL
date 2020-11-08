---
external help file: ''
Module Name: Azs.Backup.Admin
online version: https://docs.microsoft.com/powershell/module/azs.backup.admin/restore-azsbackup
schema: 2.0.0
ms.openlocfilehash: d441c74817ccaf1b32b7caf6fe811f6a5a4789da
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/08/2020
ms.locfileid: "94061509"
---
# <span data-ttu-id="1c31d-101">Restore-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="1c31d-101">Restore-AzsBackup</span></span>

## <span data-ttu-id="1c31d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c31d-102">SYNOPSIS</span></span>
<span data-ttu-id="1c31d-103">Przywracanie kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="1c31d-103">Restore a backup.</span></span>

## <span data-ttu-id="1c31d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c31d-104">SYNTAX</span></span>

### <span data-ttu-id="1c31d-105">RestoreExpanded (domyślny)</span><span class="sxs-lookup"><span data-stu-id="1c31d-105">RestoreExpanded (Default)</span></span>
```
Restore-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DecryptionCertPassword <SecureString>] [-DecryptionCertPath <String>] [-RoleName <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1c31d-106">Przywrócenie</span><span class="sxs-lookup"><span data-stu-id="1c31d-106">Restore</span></span>
```
Restore-AzsBackup -Name <String> -RestoreOption <IRestoreOptions> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="1c31d-107">RestoreViaIdentity</span><span class="sxs-lookup"><span data-stu-id="1c31d-107">RestoreViaIdentity</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> -RestoreOption <IRestoreOptions>
 [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait] [-PassThru] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="1c31d-108">RestoreViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="1c31d-108">RestoreViaIdentityExpanded</span></span>
```
Restore-AzsBackup -InputObject <IBackupAdminIdentity> [-DecryptionCertPassword <SecureString>]
 [-DecryptionCertPath <String>] [-RoleName <String>] [-DefaultProfile <PSObject>] [-AsJob] [-Force] [-NoWait]
 [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="1c31d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="1c31d-109">DESCRIPTION</span></span>
<span data-ttu-id="1c31d-110">Przywracanie kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="1c31d-110">Restore a backup.</span></span>

## <span data-ttu-id="1c31d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c31d-111">EXAMPLES</span></span>

### <span data-ttu-id="1c31d-112">Przykład 1: Przywracanie kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="1c31d-112">Example 1: Restore Backup</span></span>
```powershell
PS C:\> Restore-AzsBackup -Name $backupResourceName -DecryptionCertPath $decryptionCertPath -DecryptionCertPassword $decryptionCertPassword

```

<span data-ttu-id="1c31d-113">Przywracanie z kopii zapasowej stosu Azure.</span><span class="sxs-lookup"><span data-stu-id="1c31d-113">Restore from an Azure Stack backup.</span></span>

## <span data-ttu-id="1c31d-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c31d-114">PARAMETERS</span></span>

### <span data-ttu-id="1c31d-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1c31d-115">-AsJob</span></span>
<span data-ttu-id="1c31d-116">Uruchamianie polecenia jako zadania</span><span class="sxs-lookup"><span data-stu-id="1c31d-116">Run the command as a job</span></span>

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

### <span data-ttu-id="1c31d-117">-DecryptionCertPassword</span><span class="sxs-lookup"><span data-stu-id="1c31d-117">-DecryptionCertPassword</span></span>
<span data-ttu-id="1c31d-118">Hasło do certyfikatu deszyfrowania.</span><span class="sxs-lookup"><span data-stu-id="1c31d-118">The password for the decryption certificate.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1c31d-119">-DecryptionCertPath</span><span class="sxs-lookup"><span data-stu-id="1c31d-119">-DecryptionCertPath</span></span>
<span data-ttu-id="1c31d-120">Ścieżka do pliku certyfikatu deszyfrującego z kluczem prywatnym (pfx).</span><span class="sxs-lookup"><span data-stu-id="1c31d-120">Path to the decryption cert file with private key (.pfx).</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1c31d-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c31d-121">-DefaultProfile</span></span>
<span data-ttu-id="1c31d-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c31d-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c31d-123">-Force</span><span class="sxs-lookup"><span data-stu-id="1c31d-123">-Force</span></span>
<span data-ttu-id="1c31d-124">Nie pytaj o potwierdzenie</span><span class="sxs-lookup"><span data-stu-id="1c31d-124">Don't ask for confirmation</span></span>

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

### <span data-ttu-id="1c31d-125">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1c31d-125">-InputObject</span></span>
<span data-ttu-id="1c31d-126">Parametr Identity, aby skonstruować, zobacz sekcja notatki dla właściwości INPUTobject i tworzenie tabeli skrótów.</span><span class="sxs-lookup"><span data-stu-id="1c31d-126">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity
Parameter Sets: RestoreViaIdentity, RestoreViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="1c31d-127">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="1c31d-127">-Location</span></span>
<span data-ttu-id="1c31d-128">Nazwa lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="1c31d-128">Name of the backup location.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1c31d-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1c31d-129">-Name</span></span>
<span data-ttu-id="1c31d-130">Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="1c31d-130">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1c31d-131">-Nowait</span><span class="sxs-lookup"><span data-stu-id="1c31d-131">-NoWait</span></span>
<span data-ttu-id="1c31d-132">Wykonywanie polecenia asynchronicznie</span><span class="sxs-lookup"><span data-stu-id="1c31d-132">Run the command asynchronously</span></span>

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

### <span data-ttu-id="1c31d-133">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1c31d-133">-PassThru</span></span>
<span data-ttu-id="1c31d-134">Zwraca wartość PRAWDA, gdy wykonanie polecenia powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="1c31d-134">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="1c31d-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1c31d-135">-ResourceGroupName</span></span>
<span data-ttu-id="1c31d-136">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1c31d-136">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: "system.$((Get-AzLocation)[0].Location)"
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1c31d-137">-RestoreOption</span><span class="sxs-lookup"><span data-stu-id="1c31d-137">-RestoreOption</span></span>
<span data-ttu-id="1c31d-138">Właściwości opcji przywracania.</span><span class="sxs-lookup"><span data-stu-id="1c31d-138">Properties for restore options.</span></span>
<span data-ttu-id="1c31d-139">Aby skonstruować, zobacz sekcję notatki dla właściwości RESTOREOPTION i Utwórz tablicę skrótów.</span><span class="sxs-lookup"><span data-stu-id="1c31d-139">To construct, see NOTES section for RESTOREOPTION properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.Api20180901.IRestoreOptions
Parameter Sets: Restore, RestoreViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1c31d-140">-Rolename</span><span class="sxs-lookup"><span data-stu-id="1c31d-140">-RoleName</span></span>
<span data-ttu-id="1c31d-141">Nazwa roli stosu platformy Azure do przywrócenia, ustaw ją jako wartość pustą dla całej roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="1c31d-141">The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

```yaml
Type: System.String
Parameter Sets: RestoreExpanded, RestoreViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1c31d-142">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="1c31d-142">-SubscriptionId</span></span>
<span data-ttu-id="1c31d-143">Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1c31d-143">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="1c31d-144">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="1c31d-144">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Restore, RestoreExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="1c31d-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1c31d-145">-Confirm</span></span>
<span data-ttu-id="1c31d-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c31d-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c31d-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c31d-147">-WhatIf</span></span>
<span data-ttu-id="1c31d-148">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c31d-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c31d-149">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1c31d-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c31d-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c31d-150">CommonParameters</span></span>
<span data-ttu-id="1c31d-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c31d-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c31d-152">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c31d-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c31d-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c31d-153">INPUTS</span></span>

### <span data-ttu-id="1c31d-154">Microsoft. Azure. PowerShell. polecenia. BackupAdmin. models. IBackupAdminIdentity</span><span class="sxs-lookup"><span data-stu-id="1c31d-154">Microsoft.Azure.PowerShell.Cmdlets.BackupAdmin.Models.IBackupAdminIdentity</span></span>

## <span data-ttu-id="1c31d-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c31d-155">OUTPUTS</span></span>

### <span data-ttu-id="1c31d-156">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1c31d-156">System.Boolean</span></span>



## <span data-ttu-id="1c31d-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c31d-157">NOTES</span></span>

<span data-ttu-id="1c31d-158">ZŁOŻONE właściwości parametrów, które umożliwiają utworzenie parametrów opisanych poniżej, konstruowanie tabeli skrótów zawierającej odpowiednie właściwości.</span><span class="sxs-lookup"><span data-stu-id="1c31d-158">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="1c31d-159">Aby uzyskać informacje na temat tabel skrótów, uruchom Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="1c31d-159">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="1c31d-160">INPUTobject <IBackupAdminIdentity> : parametr Identity</span><span class="sxs-lookup"><span data-stu-id="1c31d-160">INPUTOBJECT <IBackupAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="1c31d-161">`[Backup <String>]`: Nazwa kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="1c31d-161">`[Backup <String>]`: Name of the backup.</span></span>
  - <span data-ttu-id="1c31d-162">`[Id <String>]`: Ścieżka tożsamości zasobu</span><span class="sxs-lookup"><span data-stu-id="1c31d-162">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="1c31d-163">`[Location <String>]`: Nazwa lokalizacji kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="1c31d-163">`[Location <String>]`: Name of the backup location.</span></span>
  - <span data-ttu-id="1c31d-164">`[ResourceGroupName <String>]`: Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1c31d-164">`[ResourceGroupName <String>]`: Name of the resource group.</span></span>
  - <span data-ttu-id="1c31d-165">`[SubscriptionId <String>]`: Poświadczenia subskrypcji, które jednoznacznie identyfikują abonament platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="1c31d-165">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="1c31d-166">Identyfikator subskrypcji stanowi część identyfikatora URI dla każdego połączenia z usługą.</span><span class="sxs-lookup"><span data-stu-id="1c31d-166">The subscription ID forms part of the URI for every service call.</span></span>

<span data-ttu-id="1c31d-167">RESTOREOPTION <IRestoreOptions> : właściwości opcji przywracania.</span><span class="sxs-lookup"><span data-stu-id="1c31d-167">RESTOREOPTION <IRestoreOptions>: Properties for restore options.</span></span>
  - <span data-ttu-id="1c31d-168">`[DecryptionCertBase64 <String>]`: Dane nieprzetworzone w postaci pliku certyfikatu w formacie base64.</span><span class="sxs-lookup"><span data-stu-id="1c31d-168">`[DecryptionCertBase64 <String>]`: The certificate file raw data in Base64 string.</span></span> <span data-ttu-id="1c31d-169">Powinna to być plik PFX z kluczem prywatnym.</span><span class="sxs-lookup"><span data-stu-id="1c31d-169">This should be the .pfx file with the private key.</span></span>
  - <span data-ttu-id="1c31d-170">`[DecryptionCertPassword <String>]`: Hasło do certyfikatu deszyfrowania.</span><span class="sxs-lookup"><span data-stu-id="1c31d-170">`[DecryptionCertPassword <String>]`: The password for the decryption certificate.</span></span>
  - <span data-ttu-id="1c31d-171">`[RoleName <String>]`: Nazwa roli stosu platformy Azure do przywracania, ustaw dla niej wartość Empty dla całej roli infrastruktury</span><span class="sxs-lookup"><span data-stu-id="1c31d-171">`[RoleName <String>]`: The Azure Stack role name for restore, set it to empty for all infrastructure role</span></span>

## <span data-ttu-id="1c31d-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c31d-172">RELATED LINKS</span></span>

