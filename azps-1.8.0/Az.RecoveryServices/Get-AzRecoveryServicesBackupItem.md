---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupItem.md
ms.openlocfilehash: c861bbe3b422360f58f36cbe859343f7dcc7ed37
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708679"
---
# <span data-ttu-id="28ad7-101">Get-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="28ad7-101">Get-AzRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="28ad7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="28ad7-102">SYNOPSIS</span></span>
<span data-ttu-id="28ad7-103">Pobiera elementy z kontenera w kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="28ad7-103">Gets the items from a container in Backup.</span></span>

## <span data-ttu-id="28ad7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="28ad7-104">SYNTAX</span></span>

### <span data-ttu-id="28ad7-105">GetItemsForContainer (domyślny)</span><span class="sxs-lookup"><span data-stu-id="28ad7-105">GetItemsForContainer (Default)</span></span>
```
Get-AzRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28ad7-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="28ad7-106">GetItemsForVault</span></span>
```
Get-AzRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="28ad7-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="28ad7-107">GetItemsForPolicy</span></span>
```
Get-AzRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="28ad7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="28ad7-108">DESCRIPTION</span></span>
<span data-ttu-id="28ad7-109">Polecenie cmdlet **Get-AzRecoveryServicesBackupItem** Pobiera elementy w kontenerze lub wartość z usługi Kopia zapasowa Azure oraz stan ochrony elementów.</span><span class="sxs-lookup"><span data-stu-id="28ad7-109">The **Get-AzRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="28ad7-110">Kontener zarejestrowany w magazynie usług odzyskiwania Azure może zawierać jeden lub więcej elementów, które mogą być chronione.</span><span class="sxs-lookup"><span data-stu-id="28ad7-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="28ad7-111">W przypadku maszyn wirtualnych platformy Azure w kontenerze maszyny wirtualnej może być tylko jedna pozycja kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="28ad7-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="28ad7-112">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="28ad7-112">Set the vault context by using the Set-AzRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="28ad7-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="28ad7-113">EXAMPLES</span></span>

### <span data-ttu-id="28ad7-114">Przykład 1: pobieranie elementu z kontenera kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="28ad7-114">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="28ad7-115">Pierwsze polecenie uzyskuje kontener typu AzureVM, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="28ad7-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="28ad7-116">Drugie polecenie pobiera element kopii zapasowej o nazwie V2VM w $Container, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="28ad7-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="28ad7-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="28ad7-117">PARAMETERS</span></span>

### <span data-ttu-id="28ad7-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="28ad7-118">-BackupManagementType</span></span>
<span data-ttu-id="28ad7-119">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="28ad7-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="28ad7-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="28ad7-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="28ad7-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="28ad7-121">AzureVM</span></span> 
- <span data-ttu-id="28ad7-122">OBSŁUGUJE</span><span class="sxs-lookup"><span data-stu-id="28ad7-122">MARS</span></span> 
- <span data-ttu-id="28ad7-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="28ad7-123">SCDPM</span></span> 
- <span data-ttu-id="28ad7-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="28ad7-124">AzureBackupServer</span></span> 
- <span data-ttu-id="28ad7-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="28ad7-125">AzureSQL</span></span>
- <span data-ttu-id="28ad7-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="28ad7-126">AzureStorage</span></span>

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

### <span data-ttu-id="28ad7-127">-Kontener</span><span class="sxs-lookup"><span data-stu-id="28ad7-127">-Container</span></span>
<span data-ttu-id="28ad7-128">Określa obiekt kontenera, z którego ten polecenie cmdlet pobiera elementy kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="28ad7-128">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="28ad7-129">Aby uzyskać **AzureRmRecoveryServicesBackupContainer** , użyj polecenia cmdlet Get-AzRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="28ad7-129">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="28ad7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28ad7-130">-DefaultProfile</span></span>
<span data-ttu-id="28ad7-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="28ad7-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="28ad7-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="28ad7-132">-Name</span></span>
<span data-ttu-id="28ad7-133">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="28ad7-133">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="28ad7-134">-Policy</span><span class="sxs-lookup"><span data-stu-id="28ad7-134">-Policy</span></span>
<span data-ttu-id="28ad7-135">Obiekt zasad ochrony.</span><span class="sxs-lookup"><span data-stu-id="28ad7-135">Protection policy object.</span></span>

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

### <span data-ttu-id="28ad7-136">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="28ad7-136">-ProtectionState</span></span>
<span data-ttu-id="28ad7-137">Określa stan ochrony.</span><span class="sxs-lookup"><span data-stu-id="28ad7-137">Specifies the state of protection.</span></span>
<span data-ttu-id="28ad7-138">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="28ad7-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="28ad7-139">IRPending.</span><span class="sxs-lookup"><span data-stu-id="28ad7-139">IRPending.</span></span>
<span data-ttu-id="28ad7-140">Początkowa synchronizacja nie została uruchomiona i nie ma jeszcze punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="28ad7-140">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="28ad7-141">Chroniony.</span><span class="sxs-lookup"><span data-stu-id="28ad7-141">Protected.</span></span>
<span data-ttu-id="28ad7-142">Trwa ochrona.</span><span class="sxs-lookup"><span data-stu-id="28ad7-142">Protection is ongoing.</span></span> 
- <span data-ttu-id="28ad7-143">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="28ad7-143">ProtectionError.</span></span>
<span data-ttu-id="28ad7-144">Wystąpił błąd ochrony.</span><span class="sxs-lookup"><span data-stu-id="28ad7-144">There is a protection error.</span></span>
- <span data-ttu-id="28ad7-145">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="28ad7-145">ProtectionStopped.</span></span>
<span data-ttu-id="28ad7-146">Ochrona jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="28ad7-146">Protection is disabled.</span></span>

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

### <span data-ttu-id="28ad7-147">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="28ad7-147">-ProtectionStatus</span></span>
<span data-ttu-id="28ad7-148">Określa ogólny stan ochrony elementu w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="28ad7-148">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="28ad7-149">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="28ad7-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="28ad7-150">Dobrej kondycji</span><span class="sxs-lookup"><span data-stu-id="28ad7-150">Healthy</span></span>
- <span data-ttu-id="28ad7-151">Niezdrowy</span><span class="sxs-lookup"><span data-stu-id="28ad7-151">Unhealthy</span></span>

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

### <span data-ttu-id="28ad7-152">-VaultId</span><span class="sxs-lookup"><span data-stu-id="28ad7-152">-VaultId</span></span>
<span data-ttu-id="28ad7-153">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="28ad7-153">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="28ad7-154">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="28ad7-154">-WorkloadType</span></span>
<span data-ttu-id="28ad7-155">Określa typ obciążenia pracą.</span><span class="sxs-lookup"><span data-stu-id="28ad7-155">Specifies the workload type.</span></span> <span data-ttu-id="28ad7-156">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="28ad7-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="28ad7-157">AzureVM</span><span class="sxs-lookup"><span data-stu-id="28ad7-157">AzureVM</span></span> 
- <span data-ttu-id="28ad7-158">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="28ad7-158">AzureSQLDatabase</span></span>
- <span data-ttu-id="28ad7-159">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="28ad7-159">AzureFiles</span></span>

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

### <span data-ttu-id="28ad7-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28ad7-160">CommonParameters</span></span>
<span data-ttu-id="28ad7-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="28ad7-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28ad7-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28ad7-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28ad7-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="28ad7-163">INPUTS</span></span>

### <span data-ttu-id="28ad7-164">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="28ad7-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="28ad7-165">System. String</span><span class="sxs-lookup"><span data-stu-id="28ad7-165">System.String</span></span>

## <span data-ttu-id="28ad7-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="28ad7-166">OUTPUTS</span></span>

### <span data-ttu-id="28ad7-167">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="28ad7-167">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="28ad7-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="28ad7-168">NOTES</span></span>

## <span data-ttu-id="28ad7-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="28ad7-169">RELATED LINKS</span></span>

[<span data-ttu-id="28ad7-170">Backup-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="28ad7-170">Backup-AzRecoveryServicesBackupItem</span></span>](./Backup-AzRecoveryServicesBackupItem.md)

[<span data-ttu-id="28ad7-171">Disable-AzRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="28ad7-171">Disable-AzRecoveryServicesBackupProtection</span></span>](./Disable-AzRecoveryServicesBackupProtection.md)

[<span data-ttu-id="28ad7-172">Get-AzRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="28ad7-172">Get-AzRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="28ad7-173">Restore-AzRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="28ad7-173">Restore-AzRecoveryServicesBackupItem</span></span>](./Restore-AzRecoveryServicesBackupItem.md)


