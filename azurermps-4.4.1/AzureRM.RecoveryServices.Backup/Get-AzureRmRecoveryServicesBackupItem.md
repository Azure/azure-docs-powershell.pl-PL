---
external help file: Microsoft.Azure.Commands.RecoveryServices.Backup.dll-Help.xml
Module Name: AzureRM.RecoveryServices.Backup
ms.assetid: DEB3D7B5-D974-472B-B8B4-9A19CA6AECCC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.Backup/Commands.RecoveryServices.Backup/help/Get-AzureRmRecoveryServicesBackupItem.md
ms.openlocfilehash: 03da361f8dd68d345782568dc243d4438cad1d77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719004"
---
# <span data-ttu-id="0a1a0-101">Get-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0a1a0-101">Get-AzureRmRecoveryServicesBackupItem</span></span>

## <span data-ttu-id="0a1a0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0a1a0-102">SYNOPSIS</span></span>
<span data-ttu-id="0a1a0-103">Pobiera elementy z kontenera w kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-103">Gets the items from a container in Backup.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0a1a0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0a1a0-104">SYNTAX</span></span>

### <span data-ttu-id="0a1a0-105">GetItemsForContainer (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0a1a0-105">GetItemsForContainer (Default)</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-Container] <ContainerBase> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0a1a0-106">GetItemsForVault</span><span class="sxs-lookup"><span data-stu-id="0a1a0-106">GetItemsForVault</span></span>
```
Get-AzureRmRecoveryServicesBackupItem [-BackupManagementType] <BackupManagementType> [[-Name] <String>]
 [[-ProtectionStatus] <ItemProtectionStatus>] [[-ProtectionState] <ItemProtectionState>]
 [-WorkloadType] <WorkloadType> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a1a0-107">Opis</span><span class="sxs-lookup"><span data-stu-id="0a1a0-107">DESCRIPTION</span></span>
<span data-ttu-id="0a1a0-108">Polecenie cmdlet **Get-AzureRmRecoveryServicesBackupItem** Pobiera elementy w kontenerze lub wartość z usługi Kopia zapasowa Azure oraz stan ochrony elementów.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-108">The **Get-AzureRmRecoveryServicesBackupItem** cmdlet gets the items in a container or a value in Azure Backup and the protection status of the items.</span></span>

<span data-ttu-id="0a1a0-109">Kontener zarejestrowany w magazynie usług odzyskiwania Azure może zawierać jeden lub więcej elementów, które mogą być chronione.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-109">A container that is registered to an Azure Recovery Services vault can have one or more items that can be protected.</span></span>
<span data-ttu-id="0a1a0-110">W przypadku maszyn wirtualnych platformy Azure w kontenerze maszyny wirtualnej może być tylko jedna pozycja kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-110">For Azure virtual machines, there can be only one backup item in the virtual machine container.</span></span>

<span data-ttu-id="0a1a0-111">Przed użyciem bieżącego polecenia cmdlet Ustaw kontekst magazynu przy użyciu polecenia cmdlet Set-AzureRmRecoveryServicesVaultContext.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-111">Set the vault context by using the Set-AzureRmRecoveryServicesVaultContext cmdlet before you use the current cmdlet.</span></span>

## <span data-ttu-id="0a1a0-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0a1a0-112">EXAMPLES</span></span>

### <span data-ttu-id="0a1a0-113">Przykład 1: pobieranie elementu z kontenera kopii zapasowej</span><span class="sxs-lookup"><span data-stu-id="0a1a0-113">Example 1: Get an item from a Backup container</span></span>
```
PS C:\>$Container = Get-AzureRmRecoveryServicesBackupContainer -ContainerType AzureVM -Status Registered -Name "V2VM"
PS C:\> $BackupItem = Get-AzureRmRecoveryServicesBackupItem -Container $Container -WorkloadType AzureVM
```

<span data-ttu-id="0a1a0-114">Pierwsze polecenie uzyskuje kontener typu AzureVM, a następnie zapisuje go w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-114">The first command gets the container of type AzureVM, and then stores it in the $Container variable.</span></span>

<span data-ttu-id="0a1a0-115">Drugie polecenie pobiera element kopii zapasowej o nazwie V2VM w $Container, a następnie zapisuje go w zmiennej $BackupItem.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-115">The second command gets the Backup item named V2VM in $Container, and then stores it in the $BackupItem variable.</span></span>

## <span data-ttu-id="0a1a0-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0a1a0-116">PARAMETERS</span></span>

### <span data-ttu-id="0a1a0-117">-BackupManagementType</span><span class="sxs-lookup"><span data-stu-id="0a1a0-117">-BackupManagementType</span></span>
<span data-ttu-id="0a1a0-118">Określa typ zarządzania kopią zapasową.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-118">Specifies the Backup management type.</span></span>
<span data-ttu-id="0a1a0-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0a1a0-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a1a0-120">AzureVM</span><span class="sxs-lookup"><span data-stu-id="0a1a0-120">AzureVM</span></span> 
- <span data-ttu-id="0a1a0-121">OBSŁUGUJE</span><span class="sxs-lookup"><span data-stu-id="0a1a0-121">MARS</span></span> 
- <span data-ttu-id="0a1a0-122">SCDPM</span><span class="sxs-lookup"><span data-stu-id="0a1a0-122">SCDPM</span></span> 
- <span data-ttu-id="0a1a0-123">AzureBackupServer AzureSQL</span><span class="sxs-lookup"><span data-stu-id="0a1a0-123">AzureBackupServer AzureSQL</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.BackupManagementType
Parameter Sets: GetItemsForVault
Aliases: 
Accepted values: AzureVM, MARS, SCDPM, AzureBackupServer, AzureSQL

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a1a0-124">-Kontener</span><span class="sxs-lookup"><span data-stu-id="0a1a0-124">-Container</span></span>
<span data-ttu-id="0a1a0-125">Określa obiekt kontenera, z którego ten polecenie cmdlet pobiera elementy kopii zapasowej.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-125">Specifies a container object from which this cmdlet gets backup items.</span></span>
<span data-ttu-id="0a1a0-126">Aby uzyskać **AzureRmRecoveryServicesBackupContainer** , użyj polecenia cmdlet Get-AzureRmRecoveryServicesBackupContainer.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-126">To obtain an **AzureRmRecoveryServicesBackupContainer** , use the Get-AzureRmRecoveryServicesBackupContainer cmdlet.</span></span>

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

### <span data-ttu-id="0a1a0-127">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="0a1a0-127">-Name</span></span>
<span data-ttu-id="0a1a0-128">Określa nazwę kontenera.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-128">Specifies the name of the container.</span></span>

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

### <span data-ttu-id="0a1a0-129">-ProtectionState</span><span class="sxs-lookup"><span data-stu-id="0a1a0-129">-ProtectionState</span></span>
<span data-ttu-id="0a1a0-130">Określa stan ochrony.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-130">Specifies the state of protection.</span></span>
<span data-ttu-id="0a1a0-131">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0a1a0-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a1a0-132">IRPending.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-132">IRPending.</span></span>
<span data-ttu-id="0a1a0-133">Początkowa synchronizacja nie została uruchomiona i nie ma jeszcze punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-133">Initial synchronization has not started and there is no recovery point yet.</span></span> 
- <span data-ttu-id="0a1a0-134">Chroniony.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-134">Protected.</span></span>
<span data-ttu-id="0a1a0-135">Trwa ochrona.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-135">Protection is ongoing.</span></span> 
- <span data-ttu-id="0a1a0-136">ProtectionError.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-136">ProtectionError.</span></span>
<span data-ttu-id="0a1a0-137">Wystąpił błąd ochrony.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-137">There is a protection error.</span></span>
- <span data-ttu-id="0a1a0-138">ProtectionStopped.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-138">ProtectionStopped.</span></span>
<span data-ttu-id="0a1a0-139">Ochrona jest wyłączona.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-139">Protection is disabled.</span></span>

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

### <span data-ttu-id="0a1a0-140">-ProtectionStatus</span><span class="sxs-lookup"><span data-stu-id="0a1a0-140">-ProtectionStatus</span></span>
<span data-ttu-id="0a1a0-141">Określa ogólny stan ochrony elementu w kontenerze.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-141">Specifies the overall protection status of an item in the container.</span></span>
<span data-ttu-id="0a1a0-142">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0a1a0-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a1a0-143">Dobrej kondycji</span><span class="sxs-lookup"><span data-stu-id="0a1a0-143">Healthy</span></span>
- <span data-ttu-id="0a1a0-144">Niezdrowy</span><span class="sxs-lookup"><span data-stu-id="0a1a0-144">Unhealthy</span></span>

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

### <span data-ttu-id="0a1a0-145">-Obciążenia</span><span class="sxs-lookup"><span data-stu-id="0a1a0-145">-WorkloadType</span></span>
<span data-ttu-id="0a1a0-146">Określa typ obciążenia pracą.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-146">Specifies the workload type.</span></span> <span data-ttu-id="0a1a0-147">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0a1a0-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0a1a0-148">AzureVM</span><span class="sxs-lookup"><span data-stu-id="0a1a0-148">AzureVM</span></span> 
- <span data-ttu-id="0a1a0-149">AzureSQLDatabase</span><span class="sxs-lookup"><span data-stu-id="0a1a0-149">AzureSQLDatabase</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.WorkloadType
Parameter Sets: (All)
Aliases: 
Accepted values: AzureVM, AzureSQLDatabase

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a1a0-150">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a1a0-150">-DefaultProfile</span></span>
<span data-ttu-id="0a1a0-151">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-151">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0a1a0-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a1a0-152">CommonParameters</span></span>
<span data-ttu-id="0a1a0-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0a1a0-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a1a0-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a1a0-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a1a0-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0a1a0-155">INPUTS</span></span>

## <span data-ttu-id="0a1a0-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0a1a0-156">OUTPUTS</span></span>

### <span data-ttu-id="0a1a0-157">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. ItemBase</span><span class="sxs-lookup"><span data-stu-id="0a1a0-157">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase</span></span>

### <span data-ttu-id="0a1a0-158">System. Collections. Generic. IList ' 1 [Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. modele. ItemBase]</span><span class="sxs-lookup"><span data-stu-id="0a1a0-158">System.Collections.Generic.IList\`1[Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase]</span></span>

## <span data-ttu-id="0a1a0-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0a1a0-159">NOTES</span></span>

## <span data-ttu-id="0a1a0-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0a1a0-160">RELATED LINKS</span></span>

[<span data-ttu-id="0a1a0-161">Backup-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0a1a0-161">Backup-AzureRmRecoveryServicesBackupItem</span></span>](./Backup-AzureRmRecoveryServicesBackupItem.md)

[<span data-ttu-id="0a1a0-162">Disable-AzureRmRecoveryServicesBackupProtection</span><span class="sxs-lookup"><span data-stu-id="0a1a0-162">Disable-AzureRmRecoveryServicesBackupProtection</span></span>](./Disable-AzureRmRecoveryServicesBackupProtection.md)

[<span data-ttu-id="0a1a0-163">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="0a1a0-163">Get-AzureRmRecoveryServicesBackupRecoveryPoint</span></span>](./Get-AzureRmRecoveryServicesBackupRecoveryPoint.md)

[<span data-ttu-id="0a1a0-164">Restore-AzureRmRecoveryServicesBackupItem</span><span class="sxs-lookup"><span data-stu-id="0a1a0-164">Restore-AzureRmRecoveryServicesBackupItem</span></span>](./Restore-AzureRmRecoveryServicesBackupItem.md)


