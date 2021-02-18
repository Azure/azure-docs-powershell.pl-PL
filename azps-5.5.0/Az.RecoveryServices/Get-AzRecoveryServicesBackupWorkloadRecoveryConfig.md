---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 4209755de3475b21405fafd7f1e769bbbe3f7718
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192946"
---
# <span data-ttu-id="46901-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="46901-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="46901-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46901-102">SYNOPSIS</span></span>
<span data-ttu-id="46901-103">To polecenie konstruuje konfigurację odzyskiwania elementu kopii zapasowej, takiego jak baza danych SQL.</span><span class="sxs-lookup"><span data-stu-id="46901-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="46901-104">Obiekt konfiguracji przechowuje wszystkie szczegóły, takie jak tryb odzyskiwania, docelowe miejsca docelowe przywracania i parametry specyficzne dla aplikacji, takie jak docelowe ścieżki fizyczne języka SQL.</span><span class="sxs-lookup"><span data-stu-id="46901-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="46901-105">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="46901-105">SYNTAX</span></span>

### <span data-ttu-id="46901-106">9ParameterSet (default)</span><span class="sxs-lookup"><span data-stu-id="46901-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46901-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="46901-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46901-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="46901-108">DESCRIPTION</span></span>
<span data-ttu-id="46901-109">To polecenie zwraca konfigurację odzyskiwania elementów azureWorkload, która jest przekazywana do polecenia cmdlet przywracania.</span><span class="sxs-lookup"><span data-stu-id="46901-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="46901-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="46901-110">EXAMPLES</span></span>

### <span data-ttu-id="46901-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="46901-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="46901-112">Pierwsze polecenie cmdlet jest używane do uzyskania obiektu Punkt odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="46901-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="46901-113">Drugie polecenie cmdlet tworzy plan odzyskiwania dla oryginalnego przywracania lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="46901-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="46901-114">Trzecie polecenie cmdlet tworzy plan odzyskiwania dla alternatywnego przywracania lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="46901-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="46901-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="46901-115">Example 2</span></span>

<span data-ttu-id="46901-116">To polecenie konstruuje konfigurację odzyskiwania elementu kopii zapasowej, takiego jak baza danych SQL.</span><span class="sxs-lookup"><span data-stu-id="46901-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="46901-117">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="46901-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="46901-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46901-118">PARAMETERS</span></span>

### <span data-ttu-id="46901-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="46901-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="46901-120">Określa, że należy przywrócić kopię zapasową bazy danych na innym wybranym serwerze.</span><span class="sxs-lookup"><span data-stu-id="46901-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46901-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46901-121">-DefaultProfile</span></span>
<span data-ttu-id="46901-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="46901-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46901-123">- FilePath</span><span class="sxs-lookup"><span data-stu-id="46901-123">-FilePath</span></span>
<span data-ttu-id="46901-124">Określa ścieżka pliku używana do operacji przywracania.</span><span class="sxs-lookup"><span data-stu-id="46901-124">Specifies the filepath which is used for restore operation.</span></span>

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

### <span data-ttu-id="46901-125">— FromFull</span><span class="sxs-lookup"><span data-stu-id="46901-125">-FromFull</span></span>
<span data-ttu-id="46901-126">Określa punkt pełnego odzyskiwania, do którego będą stosowane kopie zapasowe dziennika.</span><span class="sxs-lookup"><span data-stu-id="46901-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46901-127">— element</span><span class="sxs-lookup"><span data-stu-id="46901-127">-Item</span></span>
<span data-ttu-id="46901-128">Określa element kopii zapasowej, dla którego jest wykonywana operacja przywracania.</span><span class="sxs-lookup"><span data-stu-id="46901-128">Specifies the backup item on which the restore operation is being performed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46901-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="46901-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="46901-130">Określa, że zapasowa baza danych ma zostać zastąpiona informacjami bazy danych, które są obecne w punkcie odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="46901-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46901-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="46901-131">-PointInTime</span></span>
<span data-ttu-id="46901-132">Czas zakończenia zakresu czasu, dla którego należy pobrać punkt odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="46901-132">End time of Time range for which recovery point need to be fetched</span></span>

```yaml
Type: System.DateTime
Parameter Sets: LogChainParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46901-133">- RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="46901-133">-RecoveryPoint</span></span>
<span data-ttu-id="46901-134">Obiekt punktu odzyskiwania do przywrócenia</span><span class="sxs-lookup"><span data-stu-id="46901-134">Recovery point object to be restored</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase
Parameter Sets: RpParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="46901-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="46901-135">-RestoreAsFiles</span></span>
<span data-ttu-id="46901-136">Określa, jak przywrócić bazę danych jako pliki na komputerze.</span><span class="sxs-lookup"><span data-stu-id="46901-136">Specifies to restore Database as files in a machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46901-137">- TargetContainer</span><span class="sxs-lookup"><span data-stu-id="46901-137">-TargetContainer</span></span>
<span data-ttu-id="46901-138">Określa komputer docelowy, na którym należy przywrócić pliki DB.</span><span class="sxs-lookup"><span data-stu-id="46901-138">Specifies the target machine on which DB Files need to be restored.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ContainerBase
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46901-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="46901-139">-TargetItem</span></span>
<span data-ttu-id="46901-140">Określa element docelowy, na którym trzeba przywrócić db.</span><span class="sxs-lookup"><span data-stu-id="46901-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="46901-141">W przypadku przywracania języka SQL musi to być tylko element typu SQLInstance, który można chronić.</span><span class="sxs-lookup"><span data-stu-id="46901-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.ProtectableItemBase
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46901-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="46901-142">-VaultId</span></span>
<span data-ttu-id="46901-143">ARM identyfikatora magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="46901-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="46901-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46901-144">CommonParameters</span></span>
<span data-ttu-id="46901-145">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="46901-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46901-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="46901-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46901-147">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="46901-147">INPUTS</span></span>

### <span data-ttu-id="46901-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="46901-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="46901-149">System.String</span><span class="sxs-lookup"><span data-stu-id="46901-149">System.String</span></span>

## <span data-ttu-id="46901-150">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="46901-150">OUTPUTS</span></span>

### <span data-ttu-id="46901-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlet.Models.RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="46901-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="46901-152">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="46901-152">NOTES</span></span>

## <span data-ttu-id="46901-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="46901-153">RELATED LINKS</span></span>
