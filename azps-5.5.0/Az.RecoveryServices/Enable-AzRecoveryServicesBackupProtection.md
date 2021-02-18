---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 41ee67359d4545a5b69ec1f9c44ff8e37302837e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100193051"
---
# <span data-ttu-id="b397f-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="b397f-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="b397f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b397f-102">SYNOPSIS</span></span>
<span data-ttu-id="b397f-103">Umożliwia tworzenie kopii zapasowej elementu z określonymi zasadami ochrony kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b397f-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="b397f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b397f-104">SYNTAX</span></span>

### <span data-ttu-id="b397f-105">AzureVMComputeEnableProtection (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b397f-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b397f-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="b397f-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b397f-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="b397f-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b397f-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="b397f-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b397f-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="b397f-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b397f-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="b397f-110">DESCRIPTION</span></span>
<span data-ttu-id="b397f-111">Polecenie **cmdlet Enable-AzRecoveryServicesBackupProtection** umożliwia tworzenie kopii zapasowej przez skojarzenie zasad ochrony z elementem.</span><span class="sxs-lookup"><span data-stu-id="b397f-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="b397f-112">Jeśli nie ma identyfikatora zasad lub element kopii zapasowej nie jest skojarzony z żadnymi zasadami, to polecenie będzie oczekiwać identyfikatora zasad.</span><span class="sxs-lookup"><span data-stu-id="b397f-112">If policy ID is not present or the backup item is not associated with any policy, then this command will expect a policyID.</span></span>
<span data-ttu-id="b397f-113">Ustaw kontekst magazynu za pomocą Set-AzRecoveryServicesVaultContext cmdlet przed użyciem bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b397f-113">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="b397f-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b397f-114">EXAMPLES</span></span>

### <span data-ttu-id="b397f-115">Przykład 1. Włączanie ochrony kopii zapasowej elementu</span><span class="sxs-lookup"><span data-stu-id="b397f-115">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="b397f-116">Pierwsze polecenie cmdlet pobiera obiekt zasad domyślnych, a następnie przechowuje je w $Pol danych.</span><span class="sxs-lookup"><span data-stu-id="b397f-116">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="b397f-117">Drugie polecenie cmdlet określa nazwy LUN dysku, które mają zostać kopii zapasowej, i zapisuje je w $inclusionDiskLUNS zmienną.</span><span class="sxs-lookup"><span data-stu-id="b397f-117">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="b397f-118">Trzecie polecenie cmdlet ustawia zasady ochrony kopii zapasowej dla ARM wirtualnej o nazwie V2VM przy użyciu zasad w $Pol.</span><span class="sxs-lookup"><span data-stu-id="b397f-118">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="b397f-119">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b397f-119">Example 2</span></span>

<span data-ttu-id="b397f-120">Umożliwia tworzenie kopii zapasowej elementu z określonymi zasadami ochrony kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b397f-120">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="b397f-121">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="b397f-121">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="b397f-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b397f-122">PARAMETERS</span></span>

### <span data-ttu-id="b397f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b397f-123">-DefaultProfile</span></span>
<span data-ttu-id="b397f-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b397f-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b397f-125">-ExcludeAllDataDataS</span><span class="sxs-lookup"><span data-stu-id="b397f-125">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="b397f-126">Opcja określająca, aby utworzyć kopię zapasową tylko dysków systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="b397f-126">Option to specify to backup OS disks only</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b397f-127">-Exclusion Jednaklista</span><span class="sxs-lookup"><span data-stu-id="b397f-127">-ExclusionDisksList</span></span>
<span data-ttu-id="b397f-128">Lista telefonów LUN dysku do wykluczenia z kopii zapasowej, a pozostałe są automatycznie uwzględniane.</span><span class="sxs-lookup"><span data-stu-id="b397f-128">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b397f-129">-InclusionDrivesList</span><span class="sxs-lookup"><span data-stu-id="b397f-129">-InclusionDisksList</span></span>
<span data-ttu-id="b397f-130">Lista telefonów LUN dysku, które mają zostać uwzględnione w kopii zapasowej, a pozostałe są automatycznie wykluczone z wyjątkiem dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="b397f-130">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

```yaml
Type: System.String[]
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b397f-131">— element</span><span class="sxs-lookup"><span data-stu-id="b397f-131">-Item</span></span>
<span data-ttu-id="b397f-132">Określa element kopii zapasowej, dla którego to polecenie cmdlet zapewnia ochronę.</span><span class="sxs-lookup"><span data-stu-id="b397f-132">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="b397f-133">Aby uzyskać element **AzureRmRecoveryServicesBackupItem,** użyj Get-AzRecoveryServicesBackupItem cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b397f-133">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: ModifyProtection
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b397f-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b397f-134">-Name</span></span>
<span data-ttu-id="b397f-135">Określa nazwę elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b397f-135">Specifies the name of the Backup item.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection, AzureVMClassicComputeEnableProtection, AzureFileShareEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b397f-136">— Zasady</span><span class="sxs-lookup"><span data-stu-id="b397f-136">-Policy</span></span>
<span data-ttu-id="b397f-137">Określa zasady ochrony, które to polecenie cmdlet skojarzy z elementem.</span><span class="sxs-lookup"><span data-stu-id="b397f-137">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="b397f-138">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupProtectionPolicy,** użyj Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b397f-138">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b397f-139">- ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="b397f-139">-ProtectableItem</span></span>
<span data-ttu-id="b397f-140">Określa element, który ma być chroniony za pomocą danej zasady.</span><span class="sxs-lookup"><span data-stu-id="b397f-140">Specifies the item to be protected with the given policy.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: AzureWorkloadEnableProtection
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b397f-141">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="b397f-141">-ResetExclusionSettings</span></span>
<span data-ttu-id="b397f-142">Określa, jak zresetować ustawienie wykluczeń dysku skojarzone z elementem.</span><span class="sxs-lookup"><span data-stu-id="b397f-142">Specifies to reset disk exclusion setting associated with the item</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ModifyProtection
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b397f-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b397f-143">-ResourceGroupName</span></span>
<span data-ttu-id="b397f-144">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b397f-144">Specifies the name of the resource group.</span></span>
<span data-ttu-id="b397f-145">Określ ten parametr tylko dla ARM maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="b397f-145">Specify this parameter only for ARM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b397f-146">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b397f-146">-StorageAccountName</span></span>
<span data-ttu-id="b397f-147">Nazwa konta magazynu udziału plików platformy Azure</span><span class="sxs-lookup"><span data-stu-id="b397f-147">Azure file share storage account name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureFileShareEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b397f-148">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b397f-148">-VaultId</span></span>
<span data-ttu-id="b397f-149">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b397f-149">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b397f-150">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b397f-150">-Confirm</span></span>
<span data-ttu-id="b397f-151">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b397f-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b397f-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b397f-152">-WhatIf</span></span>
<span data-ttu-id="b397f-153">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b397f-153">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="b397f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b397f-154">CommonParameters</span></span>
<span data-ttu-id="b397f-155">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b397f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b397f-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b397f-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b397f-157">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b397f-157">INPUTS</span></span>

### <span data-ttu-id="b397f-158">System.String</span><span class="sxs-lookup"><span data-stu-id="b397f-158">System.String</span></span>

### <span data-ttu-id="b397f-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="b397f-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="b397f-160">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b397f-160">OUTPUTS</span></span>

### <span data-ttu-id="b397f-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.JobBase</span><span class="sxs-lookup"><span data-stu-id="b397f-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="b397f-162">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b397f-162">NOTES</span></span>

## <span data-ttu-id="b397f-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b397f-163">RELATED LINKS</span></span>

[<span data-ttu-id="b397f-164">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="b397f-164">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="b397f-165">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="b397f-165">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


