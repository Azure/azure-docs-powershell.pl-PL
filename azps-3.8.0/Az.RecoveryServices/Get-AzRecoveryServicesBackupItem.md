---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: 75eb9975a578e1114e994b08949eda8d3dafda0e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049856"
---
# <span data-ttu-id="b44d0-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b44d0-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="b44d0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b44d0-102">SYNOPSIS</span></span>

<span data-ttu-id="b44d0-103">Pobiera elementy z kontenera w kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b44d0-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="b44d0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b44d0-104">SYNTAX</span></span>

### <span data-ttu-id="b44d0-105">GetItemsForContainer (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b44d0-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b44d0-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="b44d0-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b44d0-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="b44d0-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [[-DeleteState] <ItemDeleteState>] [-FriendlyName <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b44d0-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b44d0-108">DESCRIPTION</span></span>

<span data-ttu-id="b44d0-109">Polecenie cmdlet **Get-AzRecoveryServicesBackupItem** Pobiera elementy w kontenerze lub wartość z usługi Kopia zapasowa Azure oraz stan ochrony elementów.</span><span class="sxs-lookup"><span data-stu-id="b44d0-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="b44d0-110">Kontener zarejestrowany w magazynie usług odzyskiwania Azure może zawierać jeden lub więcej elementów, które mogą być chronione.</span><span class="sxs-lookup"><span data-stu-id="b44d0-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="b44d0-111">W przypadku maszyn wirtualnych platformy Azure w kontenerze maszyny wirtualnej może być tylko jedna pozycja kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b44d0-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="b44d0-112">Ustaw kontekst magazynu przy użyciu parametru-VaultId.</span><span class="sxs-lookup"><span data-stu-id="b44d0-112">Set the vault context by using the -VaultId parameter.</span></span>

## <span data-ttu-id="b44d0-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b44d0-113">EXAMPLES</span></span>

### <span data-ttu-id="b44d0-114">Przykład 1: pobieranie elementu z kontenera kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="b44d0-114">Example 1: Get an item from a Backup container</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM -VaultId $vault.ID
```

<span data-ttu-id="b44d0-115">Pierwsze polecenie uzyskuje kontener typu AzureVM, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="b44d0-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="b44d0-116">Drugie polecenie pobiera element kopii zapasowej o nazwie V2VM w $Container, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="b44d0-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

### <span data-ttu-id="b44d0-117">Przykład 2: pobieranie elementu udziału plików platformy Azure z programu FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b44d0-117">Example 2: Get an Azure File Share Item from FriendlyName</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureStorage -Status Registered -Name "StorageAccount1" -VaultId $vault.ID
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureFiles -VaultId $vault.ID -FriendlyName "FileShareName"
```

<span data-ttu-id="b44d0-118">Pierwsze polecenie uzyskuje kontener typu AzureStorage, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="b44d0-118">The first command gets the container of type AzureStorage, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="b44d0-119">Drugie polecenie pobiera element kopii zapasowej, którego przyjazna wartość jest zgodna z wartością przekazaną w parametrze FriendlyName, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="b44d0-119">The second command gets the Backup item whose friendlyName matches the value passed in FriendlyName Parameter, and then stores it in the $BackupItem variable.</span></span>
<span data-ttu-id="b44d0-120">Użycie parametru FriendlyName może spowodować zwrócenie więcej niż jednego udziału plików platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b44d0-120">Using FriendlyName parameter can result in returning more than one Azure File Share.</span></span> <span data-ttu-id="b44d0-121">W takich przypadkach należy użyć parametru-name z wartością Parameter jako właściwości Name zwróconej w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="b44d0-121">In such cases use -Name parameter with parameter value as the Name property returned in $BackupItem variable.</span></span>

## <span data-ttu-id="b44d0-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b44d0-122">PARAMETERS</span></span>

### <span data-ttu-id="b44d0-123">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="b44d0-123">-BackupManagementType</span></span>

<span data-ttu-id="b44d0-124">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="b44d0-124">Specifies the Backup management type.</span></span>
<span data-ttu-id="b44d0-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b44d0-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b44d0-126">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b44d0-126">AzureVM</span></span>
- <span data-ttu-id="b44d0-127">OBSŁUGUJE</span><span class="sxs-lookup"><span data-stu-id="b44d0-127">MARS</span></span>
- <span data-ttu-id="b44d0-128">SCDPM</span><span class="sxs-lookup"><span data-stu-id="b44d0-128">SCDPM</span></span>
- <span data-ttu-id="b44d0-129">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="b44d0-129">AzureBackupServer</span></span>
- <span data-ttu-id="b44d0-130">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="b44d0-130">AzureSQL</span></span>
- <span data-ttu-id="b44d0-131">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="b44d0-131">AzureStorage</span></span>
- <span data-ttu-id="b44d0-132">AzureWorkload</span><span class="sxs-lookup"><span data-stu-id="b44d0-132">AzureWorkload</span></span>

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

### <span data-ttu-id="b44d0-133">-Kontener</span><span class="sxs-lookup"><span data-stu-id="b44d0-133">-Container</span></span>

<span data-ttu-id="b44d0-134">Określa obiekt kontenera, z którego ten polecenie cmdlet pobiera elementy kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="b44d0-134">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="b44d0-135">Aby uzyskać **AzureRmRecoveryServicesBackupContainer** , użyj polecenia cmdlet **Get-AzRecoveryServicesBackupContainer** .</span><span class="sxs-lookup"><span data-stu-id="b44d0-135">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the **Get-AzRecoveryServicesBackupContainer** cmdlet.</span></span>

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

### <span data-ttu-id="b44d0-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b44d0-136">-DefaultProfile</span></span>

<span data-ttu-id="b44d0-137">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b44d0-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b44d0-138">-DeleteState</span><span class="sxs-lookup"><span data-stu-id="b44d0-138">-DeleteState</span></span>
<span data-ttu-id="b44d0-139">Określa deletestate elementu o wartościach dopuszczalnych dla tego parametru:</span><span class="sxs-lookup"><span data-stu-id="b44d0-139">Specifies the deletestate of the item The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b44d0-140">ToBeDeleted</span><span class="sxs-lookup"><span data-stu-id="b44d0-140">ToBeDeleted</span></span>
- <span data-ttu-id="b44d0-141">NotDeleted</span><span class="sxs-lookup"><span data-stu-id="b44d0-141">NotDeleted</span></span>

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

### <span data-ttu-id="b44d0-142">-FriendlyName</span><span class="sxs-lookup"><span data-stu-id="b44d0-142">-FriendlyName</span></span>
<span data-ttu-id="b44d0-143">Przyjazna pozycja elementu kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="b44d0-143">FriendlyName of the backed up item</span></span>

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

### <span data-ttu-id="b44d0-144">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b44d0-144">-Name</span></span>

<span data-ttu-id="b44d0-145">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="b44d0-145">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="b44d0-146">-Policy</span><span class="sxs-lookup"><span data-stu-id="b44d0-146">-Policy</span></span>

<span data-ttu-id="b44d0-147">Obiekt zasad ochrony.</span><span class="sxs-lookup"><span data-stu-id="b44d0-147">Protection policy object.</span></span>

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

### <span data-ttu-id="b44d0-148">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="b44d0-148">-ProtectionState</span></span>

<span data-ttu-id="b44d0-149">Określa stan ochrony.</span><span class="sxs-lookup"><span data-stu-id="b44d0-149">Specifies the state of protection.</span></span>
<span data-ttu-id="b44d0-150">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b44d0-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b44d0-151">IRPending.</span><span class="sxs-lookup"><span data-stu-id="b44d0-151">IRPending.</span></span>
<span data-ttu-id="b44d0-152">Początkowa synchronizacja nie została uruchomiona i nie ma jeszcze punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="b44d0-152">Initial synchronization has not started and there is no recovery point yet.</span></span>
- <span data-ttu-id="b44d0-153">Chroniony.</span><span class="sxs-lookup"><span data-stu-id="b44d0-153">Protected.</span></span>
<span data-ttu-id="b44d0-154">Trwa ochrona.</span><span class="sxs-lookup"><span data-stu-id="b44d0-154">Protection is ongoing.</span></span>
- <span data-ttu-id="b44d0-155">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="b44d0-155">ProtectionError.</span></span>
<span data-ttu-id="b44d0-156">Wystąpił błąd ochrony.</span><span class="sxs-lookup"><span data-stu-id="b44d0-156">There is a protection error.</span></span>
- <span data-ttu-id="b44d0-157">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="b44d0-157">ProtectionStopped.</span></span>
<span data-ttu-id="b44d0-158">Ochrona jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="b44d0-158">Protection is disabled.</span></span>

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

### <span data-ttu-id="b44d0-159">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="b44d0-159">-ProtectionStatus</span></span>

<span data-ttu-id="b44d0-160">Określa ogólny stan ochrony elementu w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="b44d0-160">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="b44d0-161">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b44d0-161">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b44d0-162">Dobrej kondycji</span><span class="sxs-lookup"><span data-stu-id="b44d0-162">Healthy</span></span>
- <span data-ttu-id="b44d0-163">Niezdrowy</span><span class="sxs-lookup"><span data-stu-id="b44d0-163">Unhealthy</span></span>

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

### <span data-ttu-id="b44d0-164">-VaultId</span><span class="sxs-lookup"><span data-stu-id="b44d0-164">-VaultId</span></span>

<span data-ttu-id="b44d0-165">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="b44d0-165">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="b44d0-166">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="b44d0-166">-WorkloadType</span></span>

<span data-ttu-id="b44d0-167">Określa typ obciążenia pracą.</span><span class="sxs-lookup"><span data-stu-id="b44d0-167">Specifies the workload type.</span></span>
<span data-ttu-id="b44d0-168">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b44d0-168">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b44d0-169">AzureVM</span><span class="sxs-lookup"><span data-stu-id="b44d0-169">AzureVM</span></span>
- <span data-ttu-id="b44d0-170">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="b44d0-170">AzureSQLDatabase</span></span>
- <span data-ttu-id="b44d0-171">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="b44d0-171">AzureFiles</span></span>
- <span data-ttu-id="b44d0-172">Usługa</span><span class="sxs-lookup"><span data-stu-id="b44d0-172">MSSQL</span></span>

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

### <span data-ttu-id="b44d0-173">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b44d0-173">CommonParameters</span></span>
<span data-ttu-id="b44d0-174">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b44d0-174">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b44d0-175">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="b44d0-175">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b44d0-176">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b44d0-176">INPUTS</span></span>

### <span data-ttu-id="b44d0-177">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="b44d0-177">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="b44d0-178">System. String</span><span class="sxs-lookup"><span data-stu-id="b44d0-178">System.String</span></span>

## <span data-ttu-id="b44d0-179">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b44d0-179">OUTPUTS</span></span>

### <span data-ttu-id="b44d0-180">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="b44d0-180">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="b44d0-181">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b44d0-181">NOTES</span></span>

## <span data-ttu-id="b44d0-182">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b44d0-182">RELATED LINKS</span></span>

[<span data-ttu-id="b44d0-183">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b44d0-183">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="b44d0-184">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="b44d0-184">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="b44d0-185">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="b44d0-185">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="b44d0-186">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="b44d0-186">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)
