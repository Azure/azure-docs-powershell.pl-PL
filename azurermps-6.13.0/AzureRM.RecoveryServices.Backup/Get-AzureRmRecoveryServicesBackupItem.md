---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: a1037f742fab47ae84edae6e1558e313e563c25a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718286"
---
# <span data-ttu-id="8cd3e-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8cd3e-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="8cd3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8cd3e-102">SYNOPSIS</span></span>
<span data-ttu-id="8cd3e-103">Pobiera elementy z kontenera w kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cd3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8cd3e-104">SYNTAX</span></span>

### <span data-ttu-id="8cd3e-105">GetItemsForContainer (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8cd3e-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8cd3e-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="8cd3e-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8cd3e-107">GetItemsForPolicy</span><span class="sxs-lookup"><span data-stu-id="8cd3e-107">GetItemsForPolicy</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Policy] <PolicyBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cd3e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8cd3e-108">DESCRIPTION</span></span>
<span data-ttu-id="8cd3e-109">Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupItem** Pobiera elementy w kontenerze lub wartość z usługi Kopia zapasowa Azure oraz stan ochrony elementów.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-109">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>
<span data-ttu-id="8cd3e-110">Kontener zarejestrowany w magazynie usług odzyskiwania Azure może zawierać jeden lub więcej elementów, które mogą być chronione.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-110">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="8cd3e-111">W przypadku maszyn wirtualnych platformy Azure w kontenerze maszyny wirtualnej może być tylko jedna pozycja kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-111">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>
<span data-ttu-id="8cd3e-112">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-112">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="8cd3e-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8cd3e-113">EXAMPLES</span></span>

### <span data-ttu-id="8cd3e-114">Przykład 1: pobieranie elementu z kontenera kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="8cd3e-114">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="8cd3e-115">Pierwsze polecenie uzyskuje kontener typu AzureVM, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-115">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>
<span data-ttu-id="8cd3e-116">Drugie polecenie pobiera element kopii zapasowej o nazwie V2VM w $Container, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-116">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="8cd3e-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8cd3e-117">PARAMETERS</span></span>

### <span data-ttu-id="8cd3e-118">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="8cd3e-118">-BackupManagementType</span></span>
<span data-ttu-id="8cd3e-119">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-119">Specifies the Backup management type.</span></span>
<span data-ttu-id="8cd3e-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8cd3e-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8cd3e-121">AzureVM</span><span class="sxs-lookup"><span data-stu-id="8cd3e-121">AzureVM</span></span> 
- <span data-ttu-id="8cd3e-122">OBSŁUGUJE</span><span class="sxs-lookup"><span data-stu-id="8cd3e-122">MARS</span></span> 
- <span data-ttu-id="8cd3e-123">SCDPM</span><span class="sxs-lookup"><span data-stu-id="8cd3e-123">SCDPM</span></span> 
- <span data-ttu-id="8cd3e-124">AzureBackupServer</span><span class="sxs-lookup"><span data-stu-id="8cd3e-124">AzureBackupServer</span></span> 
- <span data-ttu-id="8cd3e-125">AzureSQL</span><span class="sxs-lookup"><span data-stu-id="8cd3e-125">AzureSQL</span></span>
- <span data-ttu-id="8cd3e-126">AzureStorage</span><span class="sxs-lookup"><span data-stu-id="8cd3e-126">AzureStorage</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases:
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL, AzureStorage

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cd3e-127">-Kontener</span><span class="sxs-lookup"><span data-stu-id="8cd3e-127">-Container</span></span>
<span data-ttu-id="8cd3e-128">Określa obiekt kontenera, z którego ten polecenie cmdlet pobiera elementy kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-128">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="8cd3e-129">Aby uzyskać **AzureRmRecoveryServicesBackupContainer** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-129">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="8cd3e-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cd3e-130">-DefaultProfile</span></span>
<span data-ttu-id="8cd3e-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cd3e-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8cd3e-132">-Name</span></span>
<span data-ttu-id="8cd3e-133">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-133">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="8cd3e-134">-Policy</span><span class="sxs-lookup"><span data-stu-id="8cd3e-134">-Policy</span></span>
<span data-ttu-id="8cd3e-135">Obiekt zasad ochrony.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-135">Protection policy object.</span></span>

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

### <span data-ttu-id="8cd3e-136">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="8cd3e-136">-ProtectionState</span></span>
<span data-ttu-id="8cd3e-137">Określa stan ochrony.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-137">Specifies the state of protection.</span></span>
<span data-ttu-id="8cd3e-138">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8cd3e-138">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8cd3e-139">IRPending.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-139">IRPending.</span></span>
<span data-ttu-id="8cd3e-140">Początkowa synchronizacja nie została uruchomiona i nie ma jeszcze punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-140">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="8cd3e-141">Chroniony.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-141">Protected.</span></span>
<span data-ttu-id="8cd3e-142">Trwa ochrona.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-142">Protection is ongoing.</span></span> 
- <span data-ttu-id="8cd3e-143">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-143">ProtectionError.</span></span>
<span data-ttu-id="8cd3e-144">Wystąpił błąd ochrony.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-144">There is a protection error.</span></span>
- <span data-ttu-id="8cd3e-145">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-145">ProtectionStopped.</span></span>
<span data-ttu-id="8cd3e-146">Ochrona jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-146">Protection is disabled.</span></span>

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

### <span data-ttu-id="8cd3e-147">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="8cd3e-147">-ProtectionStatus</span></span>
<span data-ttu-id="8cd3e-148">Określa ogólny stan ochrony elementu w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-148">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="8cd3e-149">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8cd3e-149">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8cd3e-150">Dobrej kondycji</span><span class="sxs-lookup"><span data-stu-id="8cd3e-150">Healthy</span></span>
- <span data-ttu-id="8cd3e-151">Niezdrowy</span><span class="sxs-lookup"><span data-stu-id="8cd3e-151">Unhealthy</span></span>

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

### <span data-ttu-id="8cd3e-152">-VaultId</span><span class="sxs-lookup"><span data-stu-id="8cd3e-152">-VaultId</span></span>
<span data-ttu-id="8cd3e-153">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-153">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="8cd3e-154">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="8cd3e-154">-WorkloadType</span></span>
<span data-ttu-id="8cd3e-155">Określa typ obciążenia pracą.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-155">Specifies the workload type.</span></span> <span data-ttu-id="8cd3e-156">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="8cd3e-156">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="8cd3e-157">AzureVM</span><span class="sxs-lookup"><span data-stu-id="8cd3e-157">AzureVM</span></span> 
- <span data-ttu-id="8cd3e-158">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="8cd3e-158">AzureSQLDatabase</span></span>
- <span data-ttu-id="8cd3e-159">AzureFiles</span><span class="sxs-lookup"><span data-stu-id="8cd3e-159">AzureFiles</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: GetItemsForContainer, GetItemsForVault
Aliases:
Accepted values: AzureVM, AzureSQLDatabase, AzureFiles

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cd3e-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cd3e-160">CommonParameters</span></span>
<span data-ttu-id="8cd3e-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cd3e-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cd3e-162">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cd3e-162">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cd3e-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8cd3e-163">INPUTS</span></span>

### <span data-ttu-id="8cd3e-164">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ContainerBase</span><span class="sxs-lookup"><span data-stu-id="8cd3e-164">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase</span></span>

### <span data-ttu-id="8cd3e-165">System. String</span><span class="sxs-lookup"><span data-stu-id="8cd3e-165">System.String</span></span>
<span data-ttu-id="8cd3e-166">Parametry: VaultId (ByValue)</span><span class="sxs-lookup"><span data-stu-id="8cd3e-166">Parameters: VaultId (ByValue)</span></span>

## <span data-ttu-id="8cd3e-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8cd3e-167">OUTPUTS</span></span>

### <span data-ttu-id="8cd3e-168">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="8cd3e-168">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

## <span data-ttu-id="8cd3e-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8cd3e-169">NOTES</span></span>

## <span data-ttu-id="8cd3e-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8cd3e-170">RELATED LINKS</span></span>

[<span data-ttu-id="8cd3e-171">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8cd3e-171">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="8cd3e-172">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="8cd3e-172">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="8cd3e-173">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="8cd3e-173">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="8cd3e-174">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="8cd3e-174">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


