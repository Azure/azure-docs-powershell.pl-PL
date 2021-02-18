---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupautoprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupAutoProtection.md
ms.openlocfilehash: e47ed3d2859a78837c57803789721005a5248204
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193066"
---
# <span data-ttu-id="666bc-101">Enable-AzRecoveryServicesBackupAutoProtection</span><span class="sxs-lookup"><span data-stu-id="666bc-101">Enable-AzRecoveryServicesBackupAutoProtection</span></span>

## <span data-ttu-id="666bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="666bc-102">SYNOPSIS</span></span>
<span data-ttu-id="666bc-103">Polecenie cmdlet **Enable-AzRecoveryServicesBackupAutoProtection** konfiguruje automatyczną ochronę bieżących i wszystkich przyszłych kodów DB języka SQL w danym wystąpieniu przy użyciu podanych zasad.</span><span class="sxs-lookup"><span data-stu-id="666bc-103">The **Enable-AzRecoveryServicesBackupAutoProtection** cmdlet sets up automatic protection of current and any future SQL DBs within the given instance with the supplied policy.</span></span>

## <span data-ttu-id="666bc-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="666bc-104">SYNTAX</span></span>

```
Enable-AzRecoveryServicesBackupAutoProtection [-InputItem] <ProtectableItemBase>
 [-BackupManagementType] <BackupManagementType> [-WorkloadType] <WorkloadType> [-Policy] <PolicyBase>
 [-PassThru] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="666bc-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="666bc-105">DESCRIPTION</span></span>
<span data-ttu-id="666bc-106">To polecenie umożliwia użytkownikom automatyczne chroninie wszystkich istniejących niechronionych baz danych SQL i wszelkich baz danych, które zostaną dodane później z danymi zasadami.</span><span class="sxs-lookup"><span data-stu-id="666bc-106">This command allows users to automatically protect all existing unprotected SQL DBs and any DB which will be added later with the given policy.</span></span>  <span data-ttu-id="666bc-107">Ponieważ instrukcje mają na celu tworzenie kopii zapasowej wszystkich przyszłych obiektów DB, operacja jest wykonywana na poziomie SQLInstance, dlatego usługa azure kopii zapasowej regularnie skanuje kontenery automatycznie chronione w poszukiwaniu nowych obiektów DB i automatycznie je chroni.</span><span class="sxs-lookup"><span data-stu-id="666bc-107">Since the instruction is to back up all future DBs, the operation is done at a SQLInstance level, Azure backup service will then regularly scan auto-protected containers for any new DBs and automatically protect them.</span></span>

## <span data-ttu-id="666bc-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="666bc-108">EXAMPLES</span></span>

### <span data-ttu-id="666bc-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="666bc-109">Example 1</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultSQLPolicy"
PS C:\> $SQLInstance = Get-AzRecoveryServicesBackupProtectableItem -workloadType MSSQL -ItemType SQLInstance -VaultId $targetVault.ID -Name "MSSQLInstance" -ServerName "TestSQLServer" 
PS C:\> Enable-AzRecoveryServicesBackupAutoProtection -InputItem $SQLInstance -BackupManagementType AzureWorkload -WorkloadType MSSQL -Policy $Pol -VaultId $targetvault.ID 
```

<span data-ttu-id="666bc-110">Pierwsze polecenie cmdlet pobiera obiekt zasad domyślnych, a następnie przechowuje je w $Pol danych.</span><span class="sxs-lookup"><span data-stu-id="666bc-110">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="666bc-111">Drugie polecenie cmdlet pobiera odpowiednią pozycję SQLInstance, która jest elementem, który można chronić.</span><span class="sxs-lookup"><span data-stu-id="666bc-111">The second cmdlet fetches the relevant SQLInstance which is a protectable item.</span></span> <span data-ttu-id="666bc-112">Trzecie polecenie konfiguruje automatyczną ochronę dla tego wystąpienia przy użyciu zasad w $Pol.</span><span class="sxs-lookup"><span data-stu-id="666bc-112">The 3rd command then sets up auto protection for this instance using the policy in $Pol.</span></span>

### <span data-ttu-id="666bc-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="666bc-113">Example 2</span></span>

<span data-ttu-id="666bc-114">To polecenia umożliwiają użytkownikom automatyczne chroninie wszystkich istniejących niechronionych baz danych i wszelkich baz danych, które zostaną dodane później z danymi zasadami.</span><span class="sxs-lookup"><span data-stu-id="666bc-114">This commands allows users to automatically protect all existing unprotected DBs and any DB which will be added later with the given policy.</span></span> <span data-ttu-id="666bc-115">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="666bc-115">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupAutoProtection -BackupManagementType AzureVM -InputItem <ProtectableItemBase> -Policy $Pol -VaultId $vault.ID -WorkloadType AzureVM
```

## <span data-ttu-id="666bc-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="666bc-116">PARAMETERS</span></span>

### <span data-ttu-id="666bc-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="666bc-117">-BackupManagementType</span></span>
<span data-ttu-id="666bc-118">Klasa zasobów, które są chronione.</span><span class="sxs-lookup"><span data-stu-id="666bc-118">The class of resources being protected.</span></span> <span data-ttu-id="666bc-119">Obecnie wartości obsługiwane dla tego polecenia cmdlet to: MAB, AzureWorkload, AzureVM</span><span class="sxs-lookup"><span data-stu-id="666bc-119">Currently the values supported for this cmdlet are MAB, AzureWorkload, AzureVM</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666bc-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="666bc-120">-DefaultProfile</span></span>
<span data-ttu-id="666bc-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="666bc-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666bc-122">-InputItem</span><span class="sxs-lookup"><span data-stu-id="666bc-122">-InputItem</span></span>
<span data-ttu-id="666bc-123">Określa obiekt elementu, który można chronić, który może być przekazywany jako dane wejściowe.</span><span class="sxs-lookup"><span data-stu-id="666bc-123">Specifies the protectable item object that can be passed as an input.</span></span> <span data-ttu-id="666bc-124">Bieżąca obsługiwana wartość jest obiektem protectableItem typu "SQLInstance".</span><span class="sxs-lookup"><span data-stu-id="666bc-124">The current supported value is a protectableItem object of type "SQLInstance".</span></span> 

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="666bc-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="666bc-125">-PassThru</span></span>
<span data-ttu-id="666bc-126">Zwraca wynik w celu ochrony automatycznej.</span><span class="sxs-lookup"><span data-stu-id="666bc-126">Return the result for auto protection.</span></span>

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

### <span data-ttu-id="666bc-127">— Zasady</span><span class="sxs-lookup"><span data-stu-id="666bc-127">-Policy</span></span>
<span data-ttu-id="666bc-128">Obiekt zasad ochrony.</span><span class="sxs-lookup"><span data-stu-id="666bc-128">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666bc-129">-VaultId</span><span class="sxs-lookup"><span data-stu-id="666bc-129">-VaultId</span></span>
<span data-ttu-id="666bc-130">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="666bc-130">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="666bc-131">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="666bc-131">-WorkloadType</span></span>
<span data-ttu-id="666bc-132">Typ obciążenia zasobu.</span><span class="sxs-lookup"><span data-stu-id="666bc-132">Workload type of the resource.</span></span> <span data-ttu-id="666bc-133">Aktualnie obsługiwane wartości to AzureVM, WindowsServer, MSSQL</span><span class="sxs-lookup"><span data-stu-id="666bc-133">The current supported values are AzureVM, WindowsServer, MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="666bc-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="666bc-134">-Confirm</span></span>
<span data-ttu-id="666bc-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="666bc-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="666bc-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="666bc-136">-WhatIf</span></span>
<span data-ttu-id="666bc-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="666bc-137">Shows what would happen if the cmdlet runs.</span></span>


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

### <span data-ttu-id="666bc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="666bc-138">CommonParameters</span></span>
<span data-ttu-id="666bc-139">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="666bc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="666bc-140">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="666bc-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="666bc-141">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="666bc-141">INPUTS</span></span>

### <span data-ttu-id="666bc-142">System.String</span><span class="sxs-lookup"><span data-stu-id="666bc-142">System.String</span></span>

## <span data-ttu-id="666bc-143">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="666bc-143">OUTPUTS</span></span>

### <span data-ttu-id="666bc-144">System.Object</span><span class="sxs-lookup"><span data-stu-id="666bc-144">System.Object</span></span>

## <span data-ttu-id="666bc-145">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="666bc-145">NOTES</span></span>

## <span data-ttu-id="666bc-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="666bc-146">RELATED LINKS</span></span>
