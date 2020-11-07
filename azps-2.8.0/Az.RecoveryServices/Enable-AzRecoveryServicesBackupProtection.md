---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 44622461-E567-4A0A-8F18-2D7B1BF86DA2
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/enable-azrecoveryservicesbackupprotection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Enable-AzRecoveryServicesBackupProtection.md
ms.openlocfilehash: 7f29c0bef53d75be4f5b253e3a15bf78cbacd04b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872791"
---
# <span data-ttu-id="ad5c2-101">Enable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="ad5c2-101">Enable-AzRecoveryServicesBackupProtection</span></span>

## <span data-ttu-id="ad5c2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ad5c2-102">SYNOPSIS</span></span>
<span data-ttu-id="ad5c2-103">Umożliwia tworzenie kopii zapasowej elementu z określonymi zasadami ochrony kopii zapasowych.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-103">Enables backup for an item with a specified Backup protection policy.</span></span>

## <span data-ttu-id="ad5c2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ad5c2-104">SYNTAX</span></span>

### <span data-ttu-id="ad5c2-105">AzureVMComputeEnableProtection (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ad5c2-105">AzureVMComputeEnableProtection (Default)</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ResourceGroupName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad5c2-106">AzureVMClassicComputeEnableProtection</span><span class="sxs-lookup"><span data-stu-id="ad5c2-106">AzureVMClassicComputeEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String> [-ServiceName] <String>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad5c2-107">AzureFileShareEnableProtection</span><span class="sxs-lookup"><span data-stu-id="ad5c2-107">AzureFileShareEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Name] <String>
 [-StorageAccountName] <String> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad5c2-108">AzureWorkloadEnableProtection</span><span class="sxs-lookup"><span data-stu-id="ad5c2-108">AzureWorkloadEnableProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-ProtectableItem] <ProtectableItemBase>
 [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ad5c2-109">ModifyProtection</span><span class="sxs-lookup"><span data-stu-id="ad5c2-109">ModifyProtection</span></span>
```
Enable-AzRecoveryServicesBackupProtection [-Policy] <PolicyBase> [-Item] <ItemBase> [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad5c2-110">Opis</span><span class="sxs-lookup"><span data-stu-id="ad5c2-110">DESCRIPTION</span></span>
<span data-ttu-id="ad5c2-111">Polecenie cmdlet **enable-AzRecoveryServicesBackupProtection** ustawia zasady ochrony kopii zapasowych Azure dla elementu.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-111">The **Enable-AzRecoveryServicesBackupProtection** cmdlet sets Azure Backup protection policy on an item.</span></span>
<span data-ttu-id="ad5c2-112">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="ad5c2-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ad5c2-113">EXAMPLES</span></span>

### <span data-ttu-id="ad5c2-114">Przykład 1: Włączanie ochrony przed kopiami zapasowymi dla elementu</span><span class="sxs-lookup"><span data-stu-id="ad5c2-114">Example 1: Enable Backup protection for an item</span></span>
```
PS C:\> $Pol = Get-AzRecoveryServicesBackupProtectionPolicy -Name "DefaultPolicy"
PS C:\> Enable-AzRecoveryServicesBackupProtection -Policy $Pol -Name "V2VM" -ResourceGroupName "RGName1"
WorkloadName    Operation        Status          StartTime                  EndTime
------------    ---------        ------          ---------                  -------
co03-vm         ConfigureBackup  Completed       11-Apr-16 12:19:49 PM      11-Apr-16 12:19:54 PM
```

<span data-ttu-id="ad5c2-115">Pierwsze polecenie cmdlet Pobiera domyślny obiekt zasad, a następnie zapisuje go w zmiennej $Pol.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-115">The first cmdlet gets a default policy object, and then stores it in the $Pol variable.</span></span>
<span data-ttu-id="ad5c2-116">Drugie polecenie cmdlet ustawia zasady ochrony kopii zapasowych dla maszyny wirtualnej ARM o nazwie V2VM przy użyciu zasad w $Pol.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-116">The second cmdlet sets the Backup protection policy for the ARM virtual machine named V2VM using the policy in $Pol.</span></span>

## <span data-ttu-id="ad5c2-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ad5c2-117">PARAMETERS</span></span>

### <span data-ttu-id="ad5c2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad5c2-118">-DefaultProfile</span></span>
<span data-ttu-id="ad5c2-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad5c2-120">-Item</span><span class="sxs-lookup"><span data-stu-id="ad5c2-120">-Item</span></span>
<span data-ttu-id="ad5c2-121">Określa element kopii zapasowej, dla którego to polecenie cmdlet włącza ochronę.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-121">Specifies the Backup item for which this cmdlet enables protection.</span></span>
<span data-ttu-id="ad5c2-122">Aby uzyskać **AzureRmRecoveryServicesBackupItem** , użyj polecenia cmdlet Get-AzRecoveryServicesBackupItem.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-122">To obtain an **AzureRmRecoveryServicesBackupItem** , use the Get-AzRecoveryServicesBackupItem cmdlet.</span></span>

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

### <span data-ttu-id="ad5c2-123">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ad5c2-123">-Name</span></span>
<span data-ttu-id="ad5c2-124">Określa nazwę elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-124">Specifies the name of the Backup item.</span></span>

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

### <span data-ttu-id="ad5c2-125">-Policy</span><span class="sxs-lookup"><span data-stu-id="ad5c2-125">-Policy</span></span>
<span data-ttu-id="ad5c2-126">Określa zasady ochrony, które to polecenie cmdlet kojarzy z elementem.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-126">Specifies protection policy that this cmdlet associates with an item.</span></span>
<span data-ttu-id="ad5c2-127">Aby uzyskać obiekt **AzureRmRecoveryServicesBackupProtectionPolicy** , użyj polecenia cmdlet Get-AzRecoveryServicesBackupProtectionPolicy.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-127">To obtain an **AzureRmRecoveryServicesBackupProtectionPolicy** object, use the Get-AzRecoveryServicesBackupProtectionPolicy cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ad5c2-128">-ProtectableItem</span><span class="sxs-lookup"><span data-stu-id="ad5c2-128">-ProtectableItem</span></span>
<span data-ttu-id="ad5c2-129">Wartość filtru określająca stan zadania.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-129">Filter value for status of job.</span></span>

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

### <span data-ttu-id="ad5c2-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad5c2-130">-ResourceGroupName</span></span>
<span data-ttu-id="ad5c2-131">Określa nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-131">Specifies the name of the resource group.</span></span>
<span data-ttu-id="ad5c2-132">Ten parametr należy określić tylko dla maszyn wirtualnych ARM.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-132">Specify this parameter only for ARM virtual machines.</span></span>

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

### <span data-ttu-id="ad5c2-133">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ad5c2-133">-ServiceName</span></span>
<span data-ttu-id="ad5c2-134">Określa nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-134">Specifies the service name.</span></span>
<span data-ttu-id="ad5c2-135">Ten parametr należy określić tylko dla maszyn wirtualnych ASM.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-135">Specify this parameter only for ASM virtual machines.</span></span>

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

### <span data-ttu-id="ad5c2-136">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ad5c2-136">-StorageAccountName</span></span>
<span data-ttu-id="ad5c2-137">Nazwa konta magazynu udziału plików w usłudze Azure</span><span class="sxs-lookup"><span data-stu-id="ad5c2-137">Azure file share storage account name</span></span>

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

### <span data-ttu-id="ad5c2-138">-VaultId</span><span class="sxs-lookup"><span data-stu-id="ad5c2-138">-VaultId</span></span>
<span data-ttu-id="ad5c2-139">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-139">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="ad5c2-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad5c2-140">-Confirm</span></span>
<span data-ttu-id="ad5c2-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad5c2-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad5c2-142">-WhatIf</span></span>
<span data-ttu-id="ad5c2-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ad5c2-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad5c2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad5c2-145">CommonParameters</span></span>
<span data-ttu-id="ad5c2-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad5c2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad5c2-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad5c2-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad5c2-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad5c2-148">INPUTS</span></span>

### <span data-ttu-id="ad5c2-149">System. String</span><span class="sxs-lookup"><span data-stu-id="ad5c2-149">System.String</span></span>

### <span data-ttu-id="ad5c2-150">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="ad5c2-150">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="ad5c2-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ad5c2-151">OUTPUTS</span></span>

### <span data-ttu-id="ad5c2-152">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. JobBase</span><span class="sxs-lookup"><span data-stu-id="ad5c2-152">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.JobBase</span></span>

## <span data-ttu-id="ad5c2-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ad5c2-153">NOTES</span></span>

## <span data-ttu-id="ad5c2-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad5c2-154">RELATED LINKS</span></span>

[<span data-ttu-id="ad5c2-155">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="ad5c2-155">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="ad5c2-156">Get-AzRecoveryServicesBackupProtectionPolicy</span><span class="sxs-lookup"><span data-stu-id="ad5c2-156">Get-AzRecoveryServicesBackupProtectionPolicy</span></span>](./Get-AzRecoveryServicesBackupProtectionPolicy.md)


