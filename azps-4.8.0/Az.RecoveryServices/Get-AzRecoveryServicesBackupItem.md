---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 358d3da36996c9b020db3a805889b7098b9c36ec
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94223668"
---
# <span data-ttu-id="e6504-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e6504-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="e6504-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e6504-102">SYNOPSIS</span></span>

<span data-ttu-id="e6504-103">Pobiera elementy z kontenera w kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="e6504-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="e6504-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e6504-104">SYNTAX</span></span>

### <span data-ttu-id="e6504-105">GetItemsForContainer (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e6504-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6504-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="e6504-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e6504-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="e6504-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e6504-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e6504-108">DESCRIPTION</span></span>

<span data-ttu-id="e6504-109">Polecenie cmdlet **Get-AzRecoveryServicesBackupItem** pobiera listę chronionych elementów w kontenerze oraz stan ochrony elementów.</span><span class="sxs-lookup"><span data-stu-id="e6504-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the list of protected items in a container and the protection status of the items.</span></span>
<span data-ttu-id="e6504-110">Kontener zarejestrowany w magazynie usług odzyskiwania Azure może zawierać jeden lub więcej elementów, które mogą być chronione.</span><span class="sxs-lookup"><span data-stu-id="e6504-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="e6504-111">W przypadku maszyn wirtualnych platformy Azure w kontenerze maszyny wirtualnej może być tylko jedna pozycja kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="e6504-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="e6504-112">Ustaw kontekst magazynu przy użyciu parametru-VaultId.</span><span class="sxs-lookup"><span data-stu-id="e6504-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="e6504-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e6504-113">EXAMPLES</span></span>

### <span data-ttu-id="e6504-114">Przykład 1: pobieranie elementu z kontenera kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="e6504-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="e6504-115">Pierwsze polecenie uzyskuje kontener typu AzureVM, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="e6504-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="e6504-116">Drugie polecenie pobiera element kopii zapasowej o nazwie V2VM w $Container, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="e6504-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="e6504-117">Przykład 2: pobieranie elementu udziału plików platformy Azure z programu FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e6504-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="e6504-118">Pierwsze polecenie uzyskuje kontener typu AzureStorage, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="e6504-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="e6504-119">Drugie polecenie pobiera element kopii zapasowej, którego przyjazna wartość jest zgodna z wartością przekazaną w parametrze FriendlyName, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="e6504-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="e6504-120">Użycie parametru FriendlyName może spowodować zwrócenie więcej niż jednego udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e6504-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="e6504-121">W takich przypadkach należy wykonać polecenie cmdlet, przekazując wartość parametru-name jako właściwość Name zwróconą w zestawie wyników $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="e6504-121">In such cases, execute the cmdlet by passing value for -Name parameter as the Name property returned in the result set of $BackupItem.</span></span>

## <span data-ttu-id="e6504-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e6504-122">PARAMETERS</span></span>

### <span data-ttu-id="e6504-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="e6504-123">-BackupManagementType</span></span>

<span data-ttu-id="e6504-124">Klasa zasobów chronionych.</span><span class="sxs-lookup"><span data-stu-id="e6504-124">The class of resources being protected.</span></span> <span data-ttu-id="e6504-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e6504-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e6504-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e6504-126">AzureVM</span></span>
- <span data-ttu-id="e6504-127">MAB</span><span class="sxs-lookup"><span data-stu-id="e6504-127">MAB</span></span>
- <span data-ttu-id="e6504-128">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="e6504-128">AzureStorage</span></span>
- <span data-ttu-id="e6504-129">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="e6504-129">AzureWorkload</span></span>

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

### <span data-ttu-id="e6504-130">-Kontener</span><span class="sxs-lookup"><span data-stu-id="e6504-130">-Container</span></span>

<span data-ttu-id="e6504-131">Określa obiekt kontenera, z którego ten polecenie cmdlet pobiera elementy kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="e6504-131">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="e6504-132">Aby uzyskać **AzureRmRecoveryServicesBackupContainer** , użyj polecenia cmdlet **Get-AzRecoveryServicesBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="e6504-132">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="e6504-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e6504-133">-DefaultProfile</span></span>

<span data-ttu-id="e6504-134">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e6504-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e6504-135">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="e6504-135">-DeleteState</span></span>
<span data-ttu-id="e6504-136">Określa deletestate elementu o wartościach dopuszczalnych dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="e6504-136">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e6504-137">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="e6504-137">ToBeDeleted</span></span>
- <span data-ttu-id="e6504-138">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="e6504-138">NotDeleted</span></span>

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

### <span data-ttu-id="e6504-139">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="e6504-139">-FriendlyName</span></span>
<span data-ttu-id="e6504-140">Przyjazna pozycja elementu kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="e6504-140">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="e6504-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e6504-141">-Name</span></span>

<span data-ttu-id="e6504-142">Określa nazwę elementu kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="e6504-142">Specifies the name of backup item.</span></span> <span data-ttu-id="e6504-143">W polu udział pliku Określ unikatowy identyfikator chronionego udziału plików.</span><span class="sxs-lookup"><span data-stu-id="e6504-143">For file share, specify the unique ID of protected file share.</span></span>

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

### <span data-ttu-id="e6504-144">-Policy</span><span class="sxs-lookup"><span data-stu-id="e6504-144">-Policy</span></span>

<span data-ttu-id="e6504-145">Obiekt zasad ochrony.</span><span class="sxs-lookup"><span data-stu-id="e6504-145">Protection policy object.</span></span>

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

### <span data-ttu-id="e6504-146">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="e6504-146">-ProtectionState</span></span>

<span data-ttu-id="e6504-147">Określa stan ochrony.</span><span class="sxs-lookup"><span data-stu-id="e6504-147">Specifies the state of protection.</span></span>
<span data-ttu-id="e6504-148">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e6504-148">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e6504-149">IRPending.</span><span class="sxs-lookup"><span data-stu-id="e6504-149">IRPending.</span></span>
<span data-ttu-id="e6504-150">Początkowa synchronizacja nie została uruchomiona i nie ma jeszcze punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="e6504-150">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="e6504-151">Chroniony.</span><span class="sxs-lookup"><span data-stu-id="e6504-151">Protected.</span></span>
<span data-ttu-id="e6504-152">Trwa ochrona.</span><span class="sxs-lookup"><span data-stu-id="e6504-152">Protection is ongoing.</span></span>
- <span data-ttu-id="e6504-153">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="e6504-153">ProtectionError.</span></span>
<span data-ttu-id="e6504-154">Wystąpił błąd ochrony.</span><span class="sxs-lookup"><span data-stu-id="e6504-154">There is a protection error.</span></span>
- <span data-ttu-id="e6504-155">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="e6504-155">ProtectionStopped.</span></span>
<span data-ttu-id="e6504-156">Ochrona jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="e6504-156">Protection is disabled.</span></span>

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

### <span data-ttu-id="e6504-157">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="e6504-157">-ProtectionStatus</span></span>

<span data-ttu-id="e6504-158">Określa ogólny stan ochrony elementu w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="e6504-158">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="e6504-159">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e6504-159">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e6504-160">Dobrej kondycji</span><span class="sxs-lookup"><span data-stu-id="e6504-160">Healthy</span></span>
- <span data-ttu-id="e6504-161">Niezdrowy</span><span class="sxs-lookup"><span data-stu-id="e6504-161">Unhealthy</span></span>

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

### <span data-ttu-id="e6504-162">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e6504-162">-VaultId</span></span>

<span data-ttu-id="e6504-163">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="e6504-163">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="e6504-164">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="e6504-164">-WorkloadType</span></span>

<span data-ttu-id="e6504-165">Typ obciążenia pracą zasobu.</span><span class="sxs-lookup"><span data-stu-id="e6504-165">Workload type of the resource.</span></span> <span data-ttu-id="e6504-166">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e6504-166">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e6504-167">AzureVM</span><span class="sxs-lookup"><span data-stu-id="e6504-167">AzureVM</span></span>
- <span data-ttu-id="e6504-168">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="e6504-168">AzureFiles</span></span>
- <span data-ttu-id="e6504-169">Usługa</span><span class="sxs-lookup"><span data-stu-id="e6504-169">MSSQL</span></span>

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

### <span data-ttu-id="e6504-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e6504-170">CommonParameters</span></span>
<span data-ttu-id="e6504-171">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e6504-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e6504-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="e6504-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e6504-173">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e6504-173">INPUTS</span></span>

### <span data-ttu-id="e6504-174">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="e6504-174">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="e6504-175">System. String</span><span class="sxs-lookup"><span data-stu-id="e6504-175">System.String</span></span>

## <span data-ttu-id="e6504-176">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e6504-176">OUTPUTS</span></span>

### <span data-ttu-id="e6504-177">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="e6504-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="e6504-178">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e6504-178">NOTES</span></span>

## <span data-ttu-id="e6504-179">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e6504-179">RELATED LINKS</span></span>

[<span data-ttu-id="e6504-180">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e6504-180">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="e6504-181">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="e6504-181">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="e6504-182">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="e6504-182">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="e6504-183">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="e6504-183">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
