---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.backup/get-azurermrecoveryservicesbackupitem
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 9b836a4c4c056699e2c74bcb4d5b373f5bfe170e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526718"
---
# <span data-ttu-id="903aa-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="903aa-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="903aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="903aa-102">SYNOPSIS</span></span>
<span data-ttu-id="903aa-103">Pobiera elementy z kontenera w kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="903aa-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="903aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="903aa-104">SYNTAX</span></span>

### <span data-ttu-id="903aa-105">GetItemsForContainer (domyślny)</span><span class="sxs-lookup"><span data-stu-id="903aa-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="903aa-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="903aa-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="903aa-107">Opis</span><span class="sxs-lookup"><span data-stu-id="903aa-107">DESCRIPTION</span></span>
<span data-ttu-id="903aa-108">Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupItem** Pobiera elementy w kontenerze lub wartość z usługi Kopia zapasowa Azure oraz stan ochrony elementów.</span><span class="sxs-lookup"><span data-stu-id="903aa-108">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>

<span data-ttu-id="903aa-109">Kontener zarejestrowany w magazynie usług odzyskiwania Azure może zawierać jeden lub więcej elementów, które mogą być chronione.</span><span class="sxs-lookup"><span data-stu-id="903aa-109">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="903aa-110">W przypadku maszyn wirtualnych platformy Azure w kontenerze maszyny wirtualnej może być tylko jedna pozycja kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="903aa-110">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>

<span data-ttu-id="903aa-111">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="903aa-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="903aa-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="903aa-112">EXAMPLES</span></span>

### <span data-ttu-id="903aa-113">Przykład 1: pobieranie elementu z kontenera kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="903aa-113">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="903aa-114">Pierwsze polecenie uzyskuje kontener typu AzureVM, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="903aa-114">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="903aa-115">Drugie polecenie pobiera element kopii zapasowej o nazwie V2VM w $Container, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="903aa-115">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="903aa-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="903aa-116">PARAMETERS</span></span>

### <span data-ttu-id="903aa-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="903aa-117">-BackupManagementType</span></span>
<span data-ttu-id="903aa-118">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="903aa-118">Specifies the Backup management type.</span></span>
<span data-ttu-id="903aa-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="903aa-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="903aa-120">AzureVM</span><span class="sxs-lookup"><span data-stu-id="903aa-120">AzureVM</span></span> 
- <span data-ttu-id="903aa-121">OBSŁUGUJE</span><span class="sxs-lookup"><span data-stu-id="903aa-121">MARS</span></span> 
- <span data-ttu-id="903aa-122">SCDPM</span><span class="sxs-lookup"><span data-stu-id="903aa-122">SCDPM</span></span> 
- <span data-ttu-id="903aa-123">AzureBackupServer AzureSQL</span><span class="sxs-lookup"><span data-stu-id="903aa-123">AzureBackupServer AzureSQL</span></span>

```yaml
Type: BackupManagementType
Parameter Sets: GetItemsForVault
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903aa-124">-Kontener</span><span class="sxs-lookup"><span data-stu-id="903aa-124">-Container</span></span>
<span data-ttu-id="903aa-125">Określa obiekt kontenera, z którego ten polecenie cmdlet pobiera elementy kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="903aa-125">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="903aa-126">Aby uzyskać **AzureRmRecoveryServicesBackupContainer** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="903aa-126">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

```yaml
Type: ContainerBase
Parameter Sets: GetItemsForContainer
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="903aa-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="903aa-127">-DefaultProfile</span></span>
<span data-ttu-id="903aa-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="903aa-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903aa-129">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="903aa-129">-Name</span></span>
<span data-ttu-id="903aa-130">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="903aa-130">Specifies the name of the container.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903aa-131">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="903aa-131">-ProtectionState</span></span>
<span data-ttu-id="903aa-132">Określa stan ochrony.</span><span class="sxs-lookup"><span data-stu-id="903aa-132">Specifies the state of protection.</span></span>
<span data-ttu-id="903aa-133">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="903aa-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="903aa-134">IRPending.</span><span class="sxs-lookup"><span data-stu-id="903aa-134">IRPending.</span></span>
<span data-ttu-id="903aa-135">Początkowa synchronizacja nie została uruchomiona i nie ma jeszcze punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="903aa-135">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="903aa-136">Chroniony.</span><span class="sxs-lookup"><span data-stu-id="903aa-136">Protected.</span></span>
<span data-ttu-id="903aa-137">Trwa ochrona.</span><span class="sxs-lookup"><span data-stu-id="903aa-137">Protection is ongoing.</span></span> 
- <span data-ttu-id="903aa-138">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="903aa-138">ProtectionError.</span></span>
<span data-ttu-id="903aa-139">Wystąpił błąd ochrony.</span><span class="sxs-lookup"><span data-stu-id="903aa-139">There is a protection error.</span></span>
- <span data-ttu-id="903aa-140">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="903aa-140">ProtectionStopped.</span></span>
<span data-ttu-id="903aa-141">Ochrona jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="903aa-141">Protection is disabled.</span></span>

```yaml
Type: ItemProtectionState
Parameter Sets: (All)
Aliases: 
Accepted values: IRPending, ProtectionError, Protected, ProtectionStopped

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903aa-142">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="903aa-142">-ProtectionStatus</span></span>
<span data-ttu-id="903aa-143">Określa ogólny stan ochrony elementu w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="903aa-143">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="903aa-144">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="903aa-144">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="903aa-145">Dobrej kondycji</span><span class="sxs-lookup"><span data-stu-id="903aa-145">Healthy</span></span>
- <span data-ttu-id="903aa-146">Niezdrowy</span><span class="sxs-lookup"><span data-stu-id="903aa-146">Unhealthy</span></span>

```yaml
Type: ItemProtectionStatus
Parameter Sets: (All)
Aliases: 
Accepted values: Healthy, Unhealthy

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903aa-147">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="903aa-147">-WorkloadType</span></span>
<span data-ttu-id="903aa-148">Określa typ obciążenia pracą.</span><span class="sxs-lookup"><span data-stu-id="903aa-148">Specifies the workload type.</span></span> <span data-ttu-id="903aa-149">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="903aa-149">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="903aa-150">AzureVM</span><span class="sxs-lookup"><span data-stu-id="903aa-150">AzureVM</span></span> 
- <span data-ttu-id="903aa-151">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="903aa-151">AzureSQLDatabase</span></span>

```yaml
Type: WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="903aa-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="903aa-152">CommonParameters</span></span>
<span data-ttu-id="903aa-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="903aa-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="903aa-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="903aa-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="903aa-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="903aa-155">INPUTS</span></span>

### <span data-ttu-id="903aa-156">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="903aa-156">None</span></span>
<span data-ttu-id="903aa-157">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="903aa-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="903aa-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="903aa-158">OUTPUTS</span></span>

### <span data-ttu-id="903aa-159">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="903aa-159">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="903aa-160">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. modele. ItemBase]</span><span class="sxs-lookup"><span data-stu-id="903aa-160">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase]</span></span>

## <span data-ttu-id="903aa-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="903aa-161">NOTES</span></span>

## <span data-ttu-id="903aa-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="903aa-162">RELATED LINKS</span></span>

[<span data-ttu-id="903aa-163">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="903aa-163">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="903aa-164">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="903aa-164">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="903aa-165">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="903aa-165">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="903aa-166">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="903aa-166">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


