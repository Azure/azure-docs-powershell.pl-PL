---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7b52c6064f7dd692b732558b682290e8612f383c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896141"
---
# <span data-ttu-id="9c553-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="9c553-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="9c553-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9c553-102">SYNOPSIS</span></span>
<span data-ttu-id="9c553-103">Umożliwia tworzenie kopii zapasowej elementu z określonymi zasadami ochrony kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="9c553-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="9c553-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9c553-104">SYNTAX</span></span>

### <span data-ttu-id="9c553-105">AzureVMComputeEnableProtection (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9c553-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c553-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="9c553-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c553-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="9c553-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c553-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="9c553-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c553-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="9c553-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9c553-110">Opis</span><span class="sxs-lookup"><span data-stu-id="9c553-110">DESCRIPTION</span></span>
<span data-ttu-id="9c553-111">Polecenie cmdlet **enable-AzRecoveryServicesBackupProtection** ustawia zasady ochrony kopii zapasowych Azure dla elementu.</span><span class="sxs-lookup"><span data-stu-id="9c553-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="9c553-112">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="9c553-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="9c553-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9c553-113">EXAMPLES</span></span>

### <span data-ttu-id="9c553-114">Przykład 1: Włączanie ochrony przed kopiami zapasowymi dla elementu</span><span class="sxs-lookup"><span data-stu-id="9c553-114">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="9c553-115">Pierwsze polecenie cmdlet Pobiera domyślny obiekt zasad, a następnie zapisuje go w zmiennej $Pol.</span><span class="sxs-lookup"><span data-stu-id="9c553-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="9c553-116">Drugie polecenie cmdlet określa dyski LUN, których kopie zapasowe mają być wykonywane, i przechowuje je w zmiennej $inclusionDiskLUNS.</span><span class="sxs-lookup"><span data-stu-id="9c553-116">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="9c553-117">Trzecie polecenie cmdlet ustawia zasady ochrony kopii zapasowych dla maszyny wirtualnej ARM o nazwie V2VM przy użyciu zasad w $Pol.</span><span class="sxs-lookup"><span data-stu-id="9c553-117">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="9c553-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9c553-118">PARAMETERS</span></span>

### <span data-ttu-id="9c553-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c553-119">-DefaultProfile</span></span>
<span data-ttu-id="9c553-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9c553-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c553-121">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="9c553-121">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="9c553-122">Opcja określająca tylko tworzenie kopii zapasowych dysków systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="9c553-122">Option to specify to backup OS disks only</span></span>

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

### <span data-ttu-id="9c553-123">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="9c553-123">-ExclusionDisksList</span></span>
<span data-ttu-id="9c553-124">Lista jednostek LUN dysku do wykluczenia z kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="9c553-124">List of Disk LUNs to exclude in backup</span></span>

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

### <span data-ttu-id="9c553-125">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="9c553-125">-InclusionDisksList</span></span>
<span data-ttu-id="9c553-126">Lista jednostek LUN dysku do uwzględnienia w kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="9c553-126">List of Disk LUNs to include in backup</span></span>

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

### <span data-ttu-id="9c553-127">-Item</span><span class="sxs-lookup"><span data-stu-id="9c553-127">-Item</span></span>
<span data-ttu-id="9c553-128">Określa element kopii zapasowej, dla którego to polecenie cmdlet włącza ochronę.</span><span class="sxs-lookup"><span data-stu-id="9c553-128">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="9c553-129">Aby uzyskać **AzureRmRecoveryServicesBackupItem** , użyj polecenia cmdlet Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="9c553-129">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="9c553-130">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9c553-130">-Name</span></span>
<span data-ttu-id="9c553-131">Określa nazwę elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="9c553-131">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="9c553-132">-Policy</span><span class="sxs-lookup"><span data-stu-id="9c553-132">-Policy</span></span>
<span data-ttu-id="9c553-133">Określa zasady ochrony, które to polecenie cmdlet kojarzy z elementem.</span><span class="sxs-lookup"><span data-stu-id="9c553-133">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="9c553-134">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupProtectionPolicy** , użyj polecenia cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="9c553-134">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="9c553-135">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="9c553-135">-ProtectableItem</span></span>
<span data-ttu-id="9c553-136">Wartość filtru określająca stan zadania.</span><span class="sxs-lookup"><span data-stu-id="9c553-136">Filter value for status of job.</span></span>

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

### <span data-ttu-id="9c553-137">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="9c553-137">-ResetExclusionSettings</span></span>
<span data-ttu-id="9c553-138">Określa, że Resetowanie ustawień wykluczania dysków skojarzonych z elementem</span><span class="sxs-lookup"><span data-stu-id="9c553-138">Specifies to reset disk exclusion setting associated with the item</span></span>

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

### <span data-ttu-id="9c553-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c553-139">-ResourceGroupName</span></span>
<span data-ttu-id="9c553-140">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9c553-140">Specifies the name of the resource group.</span></span>
<span data-ttu-id="9c553-141">Ten parametr należy określić tylko dla maszyn wirtualnych ARM.</span><span class="sxs-lookup"><span data-stu-id="9c553-141">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="9c553-142">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9c553-142">-ServiceName</span></span>
<span data-ttu-id="9c553-143">Określa nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="9c553-143">Specifies the service name.</span></span>
<span data-ttu-id="9c553-144">Ten parametr należy określić tylko dla maszyn wirtualnych ASM.</span><span class="sxs-lookup"><span data-stu-id="9c553-144">Specify this parameter only for ASM virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: AzureVMClassicComputeEnableProtection
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9c553-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9c553-145">-StorageAccountName</span></span>
<span data-ttu-id="9c553-146">Nazwa konta magazynu udziału plików w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="9c553-146">Azure file share storage account name</span></span>

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

### <span data-ttu-id="9c553-147">-VaultId</span><span class="sxs-lookup"><span data-stu-id="9c553-147">-VaultId</span></span>
<span data-ttu-id="9c553-148">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="9c553-148">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="9c553-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9c553-149">-Confirm</span></span>
<span data-ttu-id="9c553-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c553-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c553-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c553-151">-WhatIf</span></span>
<span data-ttu-id="9c553-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c553-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c553-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9c553-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c553-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c553-154">CommonParameters</span></span>
<span data-ttu-id="9c553-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c553-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c553-156">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="9c553-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c553-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c553-157">INPUTS</span></span>

### <span data-ttu-id="9c553-158">System. String</span><span class="sxs-lookup"><span data-stu-id="9c553-158">System.String</span></span>

### <span data-ttu-id="9c553-159">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="9c553-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="9c553-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9c553-160">OUTPUTS</span></span>

### <span data-ttu-id="9c553-161">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="9c553-161">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="9c553-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9c553-162">NOTES</span></span>

## <span data-ttu-id="9c553-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c553-163">RELATED LINKS</span></span>

[<span data-ttu-id="9c553-164">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="9c553-164">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="9c553-165">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="9c553-165">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


