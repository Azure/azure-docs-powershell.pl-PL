---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 8124122b59dcee8a654d52c6f1d9382cb90e2a10
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240282"
---
# <span data-ttu-id="b2dec-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b2dec-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="b2dec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2dec-102">SYNOPSIS</span></span>

<span data-ttu-id="b2dec-103">Pobiera elementy z kontenera w kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b2dec-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="b2dec-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b2dec-104">SYNTAX</span></span>

### <span data-ttu-id="b2dec-105">GetItemsForContainer (domyślne)</span><span class="sxs-lookup"><span data-stu-id="b2dec-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>]  [-UseSecondaryRegion] [<CommonParameters>]
```

### <span data-ttu-id="b2dec-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="b2dec-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>]  [-UseSecondaryRegion] [<CommonParameters>]
```

### <span data-ttu-id="b2dec-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="b2dec-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>]  [-UseSecondaryRegion] [<CommonParameters>]
```

## <span data-ttu-id="b2dec-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b2dec-108">DESCRIPTION</span></span>

<span data-ttu-id="b2dec-109">Polecenie **cmdlet Get-AzRecoveryServicesBackupItem** pobiera listę elementów chronionych w kontenerze oraz stan ochrony elementów.</span><span class="sxs-lookup"><span data-stu-id="b2dec-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the list of protected items in a container and the protection status of the items.</span></span>
<span data-ttu-id="b2dec-110">Kontener zarejestrowany w magazynie usług Azure Recovery Services może mieć co najmniej jeden element, który może być chroniony.</span><span class="sxs-lookup"><span data-stu-id="b2dec-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="b2dec-111">W przypadku maszyn wirtualnych platformy Azure w kontenerze maszyn wirtualnych może być tylko jeden element kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b2dec-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="b2dec-112">Ustaw kontekst magazynu przy użyciu parametru -VaultId.</span><span class="sxs-lookup"><span data-stu-id="b2dec-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="b2dec-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b2dec-113">EXAMPLES</span></span>

### <span data-ttu-id="b2dec-114">Przykład 1. Uzyskiwanie elementu z kontenera kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="b2dec-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -FriendlyName "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="b2dec-115">Pierwsze polecenie pobiera kontener typu AzureVM, a następnie przechowuje go w $Container zmienną.</span><span class="sxs-lookup"><span data-stu-id="b2dec-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="b2dec-116">Drugie polecenie pobiera element kopii zapasowej o nazwie V2VM $Container, a następnie przechowuje go w $BackupItem zmienną.</span><span class="sxs-lookup"><span data-stu-id="b2dec-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="b2dec-117">Przykład 2. Uzyskiwanie elementu Azure File Share item from FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b2dec-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -FriendlyName "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="b2dec-118">Pierwsze polecenie pobiera kontener typu AzureStorage, a następnie przechowuje go w $Container zmienną.</span><span class="sxs-lookup"><span data-stu-id="b2dec-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="b2dec-119">Drugie polecenie pobiera element kopii zapasowej, którego przyjazna nazwa odpowiada wartości przekazywanej w parametrze FriendlyName, a następnie przechowuje ją w $BackupItem danych.</span><span class="sxs-lookup"><span data-stu-id="b2dec-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="b2dec-120">Użycie parametru FriendlyName może spowodować zwrócenie więcej niż jednego udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b2dec-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="b2dec-121">W takich przypadkach należy wykonać polecenie cmdlet, przekazując wartość parametru -Name jako właściwość Name zwróconą w zestawie wyników $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="b2dec-121">In such cases, execute the cmdlet by passing value for -Name parameter as the Name property returned in the result set of $BackupItem.</span></span>

## <span data-ttu-id="b2dec-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b2dec-122">PARAMETERS</span></span>

### <span data-ttu-id="b2dec-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="b2dec-123">-BackupManagementType</span></span>

<span data-ttu-id="b2dec-124">Klasa zasobów, które są chronione.</span><span class="sxs-lookup"><span data-stu-id="b2dec-124">The class of resources being protected.</span></span> <span data-ttu-id="b2dec-125">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b2dec-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b2dec-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b2dec-126">AzureVM</span></span>
- <span data-ttu-id="b2dec-127">MAB</span><span class="sxs-lookup"><span data-stu-id="b2dec-127">MAB</span></span>
- <span data-ttu-id="b2dec-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="b2dec-128">AzureStorage</span></span>
- <span data-ttu-id="b2dec-129">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="b2dec-129">AzureWorkload</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, AzureStorage, AzureWorkload

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2dec-130">— Kontener</span><span class="sxs-lookup"><span data-stu-id="b2dec-130">-Container</span></span>

<span data-ttu-id="b2dec-131">Określa obiekt kontenera, z którego to polecenie cmdlet pobiera elementy kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b2dec-131">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="b2dec-132">Aby uzyskać element **cmdlet AzureRmRecoveryServicesBackupContainer,** użyj polecenia cmdlet **Get-AzRecoveryServicesBackupContainer.**</span><span class="sxs-lookup"><span data-stu-id="b2dec-132">To obtain an **AzureRmRecoveryServicesBackupContainer**, use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="b2dec-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2dec-133">-DefaultProfile</span></span>

<span data-ttu-id="b2dec-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2dec-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2dec-135">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="b2dec-135">-DeleteState</span></span>
<span data-ttu-id="b2dec-136">Określa stan usuwania elementu Dopuszczalne wartości dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="b2dec-136">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b2dec-137">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="b2dec-137">ToBeDeleted</span></span>
- <span data-ttu-id="b2dec-138">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="b2dec-138">NotDeleted</span></span>

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

### <span data-ttu-id="b2dec-139">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b2dec-139">-FriendlyName</span></span>
<span data-ttu-id="b2dec-140">Przyjazna nazwa elementu kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="b2dec-140">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="b2dec-141">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b2dec-141">-Name</span></span>

<span data-ttu-id="b2dec-142">Określa nazwę elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b2dec-142">Specifies the name of backup item.</span></span> <span data-ttu-id="b2dec-143">W przypadku udziału plików określ unikatowy identyfikator chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="b2dec-143">For file share, specify the unique ID of protected file share.</span></span>

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

### <span data-ttu-id="b2dec-144">— Zasady</span><span class="sxs-lookup"><span data-stu-id="b2dec-144">-Policy</span></span>

<span data-ttu-id="b2dec-145">Obiekt zasad ochrony.</span><span class="sxs-lookup"><span data-stu-id="b2dec-145">Protection policy object.</span></span>

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

### <span data-ttu-id="b2dec-146">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="b2dec-146">-ProtectionState</span></span>

<span data-ttu-id="b2dec-147">Określa stan ochrony.</span><span class="sxs-lookup"><span data-stu-id="b2dec-147">Specifies the state of protection.</span></span>
<span data-ttu-id="b2dec-148">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b2dec-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b2dec-149">IRPending.</span><span class="sxs-lookup"><span data-stu-id="b2dec-149">IRPending.</span></span>
<span data-ttu-id="b2dec-150">Początkowa synchronizacja nie została uruchomiona i nie ma jeszcze punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b2dec-150">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="b2dec-151">Chroniony.</span><span class="sxs-lookup"><span data-stu-id="b2dec-151">Protected.</span></span>
<span data-ttu-id="b2dec-152">Ochrona jest w toku.</span><span class="sxs-lookup"><span data-stu-id="b2dec-152">Protection is ongoing.</span></span>
- <span data-ttu-id="b2dec-153">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="b2dec-153">ProtectionError.</span></span>
<span data-ttu-id="b2dec-154">Wystąpił błąd ochrony.</span><span class="sxs-lookup"><span data-stu-id="b2dec-154">There is a protection error.</span></span>
- <span data-ttu-id="b2dec-155">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="b2dec-155">ProtectionStopped.</span></span>
<span data-ttu-id="b2dec-156">Ochrona jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="b2dec-156">Protection is disabled.</span></span>

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

### <span data-ttu-id="b2dec-157">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="b2dec-157">-ProtectionStatus</span></span>

<span data-ttu-id="b2dec-158">Określa ogólny stan ochrony elementu w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="b2dec-158">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="b2dec-159">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b2dec-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b2dec-160">Zdrowe</span><span class="sxs-lookup"><span data-stu-id="b2dec-160">Healthy</span></span>
- <span data-ttu-id="b2dec-161">Zła kondycja</span><span class="sxs-lookup"><span data-stu-id="b2dec-161">Unhealthy</span></span>

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

### <span data-ttu-id="b2dec-162">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b2dec-162">-VaultId</span></span>

<span data-ttu-id="b2dec-163">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b2dec-163">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b2dec-164">-WorkloadType</span><span class="sxs-lookup"><span data-stu-id="b2dec-164">-WorkloadType</span></span>

<span data-ttu-id="b2dec-165">Typ obciążenia zasobu.</span><span class="sxs-lookup"><span data-stu-id="b2dec-165">Workload type of the resource.</span></span> <span data-ttu-id="b2dec-166">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b2dec-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b2dec-167">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b2dec-167">AzureVM</span></span>
- <span data-ttu-id="b2dec-168">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="b2dec-168">AzureFiles</span></span>
- <span data-ttu-id="b2dec-169">MSSQL</span><span class="sxs-lookup"><span data-stu-id="b2dec-169">MSSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureFiles, MSSQL

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2dec-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2dec-170">CommonParameters</span></span>
<span data-ttu-id="b2dec-171">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2dec-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2dec-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b2dec-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2dec-173">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2dec-173">INPUTS</span></span>

### <span data-ttu-id="b2dec-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.ContainerBase</span><span class="sxs-lookup"><span data-stu-id="b2dec-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="b2dec-175">System.String</span><span class="sxs-lookup"><span data-stu-id="b2dec-175">System.String</span></span>

## <span data-ttu-id="b2dec-176">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2dec-176">OUTPUTS</span></span>

### <span data-ttu-id="b2dec-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.ItemBase</span><span class="sxs-lookup"><span data-stu-id="b2dec-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="b2dec-178">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b2dec-178">NOTES</span></span>

## <span data-ttu-id="b2dec-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2dec-179">RELATED LINKS</span></span>

[<span data-ttu-id="b2dec-180">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b2dec-180">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="b2dec-181">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="b2dec-181">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="b2dec-182">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b2dec-182">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="b2dec-183">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b2dec-183">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
