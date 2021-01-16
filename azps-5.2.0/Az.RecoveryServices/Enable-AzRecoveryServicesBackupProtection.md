---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: f0147cea03d4b535102efd53af1a4d5f88338530
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345118"
---
# <span data-ttu-id="53bc3-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="53bc3-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="53bc3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53bc3-102">SYNOPSIS</span></span>
<span data-ttu-id="53bc3-103">Umożliwia tworzenie kopii zapasowej elementu z określonymi zasadami ochrony kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="53bc3-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="53bc3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53bc3-104">SYNTAX</span></span>

### <span data-ttu-id="53bc3-105">AzureVMComputeEnableProtection (domyślny)</span><span class="sxs-lookup"><span data-stu-id="53bc3-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-ResourceGroupName] <String> [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="53bc3-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="53bc3-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String> [-ServiceName] <String>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ExcludeAllDataDisks] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53bc3-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="53bc3-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53bc3-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="53bc3-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="53bc3-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="53bc3-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [[-Policy] <PolicyBase>] [-Item] <ItemBase>
 [-InclusionDisksList <String[]>] [-ExclusionDisksList <String[]>] [-ResetExclusionSettings]
 [-ExcludeAllDataDisks] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="53bc3-110">Opis</span><span class="sxs-lookup"><span data-stu-id="53bc3-110">DESCRIPTION</span></span>
<span data-ttu-id="53bc3-111">Polecenie cmdlet **enable-AzRecoveryServicesBackupProtection** włącza wykonywanie kopii zapasowej, kojarząc zasady ochrony z elementem.</span><span class="sxs-lookup"><span data-stu-id="53bc3-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet enables the backup by associating a protection policy with the item.</span></span>
<span data-ttu-id="53bc3-112">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="53bc3-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="53bc3-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53bc3-113">EXAMPLES</span></span>

### <span data-ttu-id="53bc3-114">Przykład 1: Włączanie ochrony przed kopiami zapasowymi dla elementu</span><span class="sxs-lookup"><span data-stu-id="53bc3-114">Example 1: Enable Backup protection for an item</span></span>
```powershell
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> $inclusionDiskLUNS = ("1", "2")
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1" -InclusionDisksList $inclusionDiskLUNS
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="53bc3-115">Pierwsze polecenie cmdlet Pobiera domyślny obiekt zasad, a następnie zapisuje go w zmiennej $Pol.</span><span class="sxs-lookup"><span data-stu-id="53bc3-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="53bc3-116">Drugie polecenie cmdlet określa dyski LUN, których kopie zapasowe mają być wykonywane, i przechowuje je w zmiennej $inclusionDiskLUNS.</span><span class="sxs-lookup"><span data-stu-id="53bc3-116">The second cmdlet specifies the disk LUNs which are to be backed up and stores it in $inclusionDiskLUNS variable.</span></span>
<span data-ttu-id="53bc3-117">Trzecie polecenie cmdlet ustawia zasady ochrony kopii zapasowych dla maszyny wirtualnej ARM o nazwie V2VM przy użyciu zasad w $Pol.</span><span class="sxs-lookup"><span data-stu-id="53bc3-117">The third cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

### <span data-ttu-id="53bc3-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="53bc3-118">Example 2</span></span>

<span data-ttu-id="53bc3-119">Umożliwia tworzenie kopii zapasowej elementu z określonymi zasadami ochrony kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="53bc3-119">Enables backup for an item with a specified Backup protection policy.</span></span> <span data-ttu-id="53bc3-120">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="53bc3-120">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Enable-AzRecoveryServicesBackupProtection -Item $Item -Policy $Pol -VaultId $vault
```

## <span data-ttu-id="53bc3-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53bc3-121">PARAMETERS</span></span>

### <span data-ttu-id="53bc3-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53bc3-122">-DefaultProfile</span></span>
<span data-ttu-id="53bc3-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="53bc3-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="53bc3-124">-ExcludeAllDataDisks</span><span class="sxs-lookup"><span data-stu-id="53bc3-124">-ExcludeAllDataDisks</span></span>
<span data-ttu-id="53bc3-125">Opcja określająca tylko tworzenie kopii zapasowych dysków systemu operacyjnego</span><span class="sxs-lookup"><span data-stu-id="53bc3-125">Option to specify to backup OS disks only</span></span>

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

### <span data-ttu-id="53bc3-126">-ExclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="53bc3-126">-ExclusionDisksList</span></span>
<span data-ttu-id="53bc3-127">Lista jednostek LUN dysku do wykluczenia w kopii zapasowej, a pozostałe są automatycznie dołączane.</span><span class="sxs-lookup"><span data-stu-id="53bc3-127">List of Disk LUNs to be excluded in backup and the rest are automatically included.</span></span>

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

### <span data-ttu-id="53bc3-128">-InclusionDisksList</span><span class="sxs-lookup"><span data-stu-id="53bc3-128">-InclusionDisksList</span></span>
<span data-ttu-id="53bc3-129">Lista numerów LUN dysków, które mają zostać uwzględnione w kopii zapasowej, a pozostałe są automatycznie wykluczane z wyjątkiem dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="53bc3-129">List of Disk LUNs to be included in backup and the rest are automatically excluded except OS disk.</span></span>

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

### <span data-ttu-id="53bc3-130">-Item</span><span class="sxs-lookup"><span data-stu-id="53bc3-130">-Item</span></span>
<span data-ttu-id="53bc3-131">Określa element kopii zapasowej, dla którego to polecenie cmdlet włącza ochronę.</span><span class="sxs-lookup"><span data-stu-id="53bc3-131">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="53bc3-132">Aby uzyskać **AzureRmRecoveryServicesBackupItem**, użyj polecenia cmdlet Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="53bc3-132">To obtain an **AzureRmRecoveryServicesBackupItem**, use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="53bc3-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="53bc3-133">-Name</span></span>
<span data-ttu-id="53bc3-134">Określa nazwę elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="53bc3-134">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="53bc3-135">-Policy</span><span class="sxs-lookup"><span data-stu-id="53bc3-135">-Policy</span></span>
<span data-ttu-id="53bc3-136">Określa zasady ochrony, które to polecenie cmdlet kojarzy z elementem.</span><span class="sxs-lookup"><span data-stu-id="53bc3-136">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="53bc3-137">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupProtectionPolicy** , użyj polecenia cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="53bc3-137">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

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

### <span data-ttu-id="53bc3-138">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="53bc3-138">-ProtectableItem</span></span>
<span data-ttu-id="53bc3-139">Określa element, który ma być chroniony za pomocą danej zasady.</span><span class="sxs-lookup"><span data-stu-id="53bc3-139">Specifies the item to be protected with the given policy.</span></span>

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

### <span data-ttu-id="53bc3-140">-ResetExclusionSettings</span><span class="sxs-lookup"><span data-stu-id="53bc3-140">-ResetExclusionSettings</span></span>
<span data-ttu-id="53bc3-141">Określa, że Resetowanie ustawień wykluczania dysków skojarzonych z elementem</span><span class="sxs-lookup"><span data-stu-id="53bc3-141">Specifies to reset disk exclusion setting associated with the item</span></span>

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

### <span data-ttu-id="53bc3-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53bc3-142">-ResourceGroupName</span></span>
<span data-ttu-id="53bc3-143">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="53bc3-143">Specifies the name of the resource group.</span></span>
<span data-ttu-id="53bc3-144">Ten parametr należy określić tylko dla maszyn wirtualnych ARM.</span><span class="sxs-lookup"><span data-stu-id="53bc3-144">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="53bc3-145">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="53bc3-145">-StorageAccountName</span></span>
<span data-ttu-id="53bc3-146">Nazwa konta magazynu udziału plików w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="53bc3-146">Azure file share storage account name</span></span>

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

### <span data-ttu-id="53bc3-147">-VaultId</span><span class="sxs-lookup"><span data-stu-id="53bc3-147">-VaultId</span></span>
<span data-ttu-id="53bc3-148">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="53bc3-148">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="53bc3-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="53bc3-149">-Confirm</span></span>
<span data-ttu-id="53bc3-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53bc3-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="53bc3-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="53bc3-151">-WhatIf</span></span>
<span data-ttu-id="53bc3-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="53bc3-152">Shows what would happen if the cmdlet runs.</span></span> 

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

### <span data-ttu-id="53bc3-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53bc3-153">CommonParameters</span></span>
<span data-ttu-id="53bc3-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53bc3-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53bc3-155">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="53bc3-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53bc3-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53bc3-156">INPUTS</span></span>

### <span data-ttu-id="53bc3-157">System. String</span><span class="sxs-lookup"><span data-stu-id="53bc3-157">System.String</span></span>

### <span data-ttu-id="53bc3-158">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="53bc3-158">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="53bc3-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53bc3-159">OUTPUTS</span></span>

### <span data-ttu-id="53bc3-160">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="53bc3-160">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="53bc3-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53bc3-161">NOTES</span></span>

## <span data-ttu-id="53bc3-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53bc3-162">RELATED LINKS</span></span>

[<span data-ttu-id="53bc3-163">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="53bc3-163">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="53bc3-164">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="53bc3-164">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


