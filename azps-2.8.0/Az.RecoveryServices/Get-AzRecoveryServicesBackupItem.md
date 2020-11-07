---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 2dfc4b8fd0491a9f8c2200876609ab0a8cb00cce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872711"
---
# <span data-ttu-id="45092-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="45092-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="45092-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="45092-102">SYNOPSIS</span></span>

<span data-ttu-id="45092-103">Pobiera elementy z kontenera w kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="45092-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="45092-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="45092-104">SYNTAX</span></span>

### <span data-ttu-id="45092-105">GetItemsForContainer (domyślny)</span><span class="sxs-lookup"><span data-stu-id="45092-105">GetItemsForContainer (Default)</span></span>

```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45092-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="45092-106">GetItemsForVault</span></span>

```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45092-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="45092-107">GetItemsForPolicy</span></span>

```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [[-DeleteState] <ItemDeleteState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45092-108">Opis</span><span class="sxs-lookup"><span data-stu-id="45092-108">DESCRIPTION</span></span>

<span data-ttu-id="45092-109">Polecenie cmdlet **Get-AzRecoveryServicesBackupItem** Pobiera elementy w kontenerze lub wartość z usługi Kopia zapasowa Azure oraz stan ochrony elementów.</span><span class="sxs-lookup"><span data-stu-id="45092-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="45092-110">Kontener zarejestrowany w magazynie usług odzyskiwania Azure może zawierać jeden lub więcej elementów, które mogą być chronione.</span><span class="sxs-lookup"><span data-stu-id="45092-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="45092-111">W przypadku maszyn wirtualnych platformy Azure w kontenerze maszyny wirtualnej może być tylko jedna pozycja kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="45092-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="45092-112">Ustaw kontekst magazynu przy użyciu parametru-VaultId.</span><span class="sxs-lookup"><span data-stu-id="45092-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="45092-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="45092-113">EXAMPLES</span></span>

### <span data-ttu-id="45092-114">Przykład 1: pobieranie elementu z kontenera kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="45092-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="45092-115">Pierwsze polecenie uzyskuje kontener typu AzureVM, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="45092-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="45092-116">Drugie polecenie pobiera element kopii zapasowej o nazwie V2VM w $Container, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="45092-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="45092-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="45092-117">PARAMETERS</span></span>

### <span data-ttu-id="45092-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="45092-118">-BackupManagementType</span></span>

<span data-ttu-id="45092-119">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="45092-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="45092-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="45092-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45092-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="45092-121">AzureVM</span></span>
- <span data-ttu-id="45092-122">OBSŁUGUJE</span><span class="sxs-lookup"><span data-stu-id="45092-122">MARS</span></span>
- <span data-ttu-id="45092-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="45092-123">SCDPM</span></span>
- <span data-ttu-id="45092-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="45092-124">AzureBackupServer</span></span>
- <span data-ttu-id="45092-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="45092-125">AzureSQL</span></span>
- <span data-ttu-id="45092-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="45092-126">AzureStorage</span></span>
- <span data-ttu-id="45092-127">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="45092-127">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45092-128">-Kontener</span><span class="sxs-lookup"><span data-stu-id="45092-128">-Container</span></span>

<span data-ttu-id="45092-129">Określa obiekt kontenera, z którego ten polecenie cmdlet pobiera elementy kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="45092-129">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="45092-130">Aby uzyskać **AzureRmRecoveryServicesBackupContainer** , użyj polecenia cmdlet **Get-AzRecoveryServicesBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="45092-130">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: GetItemsForContainer
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45092-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45092-131">-DefaultProfile</span></span>

<span data-ttu-id="45092-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="45092-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45092-133">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="45092-133">-DeleteState</span></span>
<span data-ttu-id="45092-134">Określa deletestate elementu o wartościach dopuszczalnych dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="45092-134">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45092-135">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="45092-135">ToBeDeleted</span></span>
- <span data-ttu-id="45092-136">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="45092-136">NotDeleted</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemDeleteState
Parameter Sets: (All)
Aliases:
Accepted values: ToBeDeleted, NotDeleted

Required: False
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45092-137">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="45092-137">-Name</span></span>

<span data-ttu-id="45092-138">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="45092-138">Specifies the name of the container.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45092-139">-Policy</span><span class="sxs-lookup"><span data-stu-id="45092-139">-Policy</span></span>

<span data-ttu-id="45092-140">Obiekt zasad ochrony.</span><span class="sxs-lookup"><span data-stu-id="45092-140">Protection policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.PolicyBase
Parameter Sets: GetItemsForPolicy
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45092-141">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="45092-141">-ProtectionState</span></span>

<span data-ttu-id="45092-142">Określa stan ochrony.</span><span class="sxs-lookup"><span data-stu-id="45092-142">Specifies the state of protection.</span></span>
<span data-ttu-id="45092-143">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="45092-143">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45092-144">IRPending.</span><span class="sxs-lookup"><span data-stu-id="45092-144">IRPending.</span></span>
<span data-ttu-id="45092-145">Początkowa synchronizacja nie została uruchomiona i nie ma jeszcze punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="45092-145">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="45092-146">Chroniony.</span><span class="sxs-lookup"><span data-stu-id="45092-146">Protected.</span></span>
<span data-ttu-id="45092-147">Trwa ochrona.</span><span class="sxs-lookup"><span data-stu-id="45092-147">Protection is ongoing.</span></span>
- <span data-ttu-id="45092-148">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="45092-148">ProtectionError.</span></span>
<span data-ttu-id="45092-149">Wystąpił błąd ochrony.</span><span class="sxs-lookup"><span data-stu-id="45092-149">There is a protection error.</span></span>
- <span data-ttu-id="45092-150">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="45092-150">ProtectionStopped.</span></span>
<span data-ttu-id="45092-151">Ochrona jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="45092-151">Protection is disabled.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionState
Parameter Sets: (All)
Aliases:
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45092-152">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="45092-152">-ProtectionStatus</span></span>

<span data-ttu-id="45092-153">Określa ogólny stan ochrony elementu w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="45092-153">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="45092-154">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="45092-154">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45092-155">Dobrej kondycji</span><span class="sxs-lookup"><span data-stu-id="45092-155">Healthy</span></span>
- <span data-ttu-id="45092-156">Niezdrowy</span><span class="sxs-lookup"><span data-stu-id="45092-156">Unhealthy</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemProtectionStatus
Parameter Sets: (All)
Aliases:
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45092-157">-VaultId</span><span class="sxs-lookup"><span data-stu-id="45092-157">-VaultId</span></span>

<span data-ttu-id="45092-158">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="45092-158">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="45092-159">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="45092-159">-WorkloadType</span></span>

<span data-ttu-id="45092-160">Określa typ obciążenia pracą.</span><span class="sxs-lookup"><span data-stu-id="45092-160">Specifies the workload type.</span></span>
<span data-ttu-id="45092-161">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="45092-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="45092-162">AzureVM</span><span class="sxs-lookup"><span data-stu-id="45092-162">AzureVM</span></span>
- <span data-ttu-id="45092-163">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="45092-163">AzureSQLDatabase</span></span>
- <span data-ttu-id="45092-164">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="45092-164">AzureFiles</span></span>
- <span data-ttu-id="45092-165">Usługa</span><span class="sxs-lookup"><span data-stu-id="45092-165">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45092-166">-CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45092-166">-CommonParameters</span></span>

<span data-ttu-id="45092-167">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45092-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45092-168">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="45092-168">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45092-169">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45092-169">INPUTS</span></span>

### <span data-ttu-id="45092-170">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="45092-170">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="45092-171">System. String</span><span class="sxs-lookup"><span data-stu-id="45092-171">System.String</span></span>

## <span data-ttu-id="45092-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="45092-172">OUTPUTS</span></span>

### <span data-ttu-id="45092-173">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="45092-173">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="45092-174">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="45092-174">NOTES</span></span>

## <span data-ttu-id="45092-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45092-175">RELATED LINKS</span></span>

[<span data-ttu-id="45092-176">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="45092-176">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="45092-177">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="45092-177">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="45092-178">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="45092-178">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="45092-179">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="45092-179">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
