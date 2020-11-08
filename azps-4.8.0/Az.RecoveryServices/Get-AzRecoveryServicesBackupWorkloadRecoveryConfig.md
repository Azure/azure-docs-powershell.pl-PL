---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 4209755de3475b21405fafd7f1e769bbbe3f7718
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221691"
---
# <span data-ttu-id="613b8-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="613b8-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="613b8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="613b8-102">SYNOPSIS</span></span>
<span data-ttu-id="613b8-103">To polecenie konstruuje konfigurację odzyskiwania elementu z kopią zapasową, na przykład SQL DB.</span><span class="sxs-lookup"><span data-stu-id="613b8-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="613b8-104">W obiekcie konfiguracji są przechowywane wszystkie szczegóły, takie jak tryb odzyskiwania, docelowe miejsca docelowe dla parametrów przywracania i aplikacji, takie jak docelowe ścieżki SQL.</span><span class="sxs-lookup"><span data-stu-id="613b8-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="613b8-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="613b8-105">SYNTAX</span></span>

### <span data-ttu-id="613b8-106">RpParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="613b8-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="613b8-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="613b8-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="613b8-108">Opis</span><span class="sxs-lookup"><span data-stu-id="613b8-108">DESCRIPTION</span></span>
<span data-ttu-id="613b8-109">Polecenie zwraca konfigurację odzyskiwania dla elementów AzureWorkload, które są przekazywane do polecenia cmdlet Restore.</span><span class="sxs-lookup"><span data-stu-id="613b8-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="613b8-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="613b8-110">EXAMPLES</span></span>

### <span data-ttu-id="613b8-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="613b8-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="613b8-112">Pierwsze polecenie cmdlet służy do pobierania obiektu punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="613b8-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="613b8-113">Drugie polecenie cmdlet tworzy plan odzyskiwania dla oryginalnej lokalizacji przywracania.</span><span class="sxs-lookup"><span data-stu-id="613b8-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="613b8-114">Trzecie polecenie cmdlet tworzy plan odzyskiwania dla alternatywnej lokalizacji przywracania.</span><span class="sxs-lookup"><span data-stu-id="613b8-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="613b8-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="613b8-115">Example 2</span></span>

<span data-ttu-id="613b8-116">To polecenie konstruuje konfigurację odzyskiwania elementu z kopią zapasową, na przykład SQL DB.</span><span class="sxs-lookup"><span data-stu-id="613b8-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="613b8-117">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="613b8-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="613b8-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="613b8-118">PARAMETERS</span></span>

### <span data-ttu-id="613b8-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="613b8-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="613b8-120">Określa, że kopia zapasowa bazy danych powinna zostać przywrócona na inny wybrany serwer.</span><span class="sxs-lookup"><span data-stu-id="613b8-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

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

### <span data-ttu-id="613b8-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="613b8-121">-DefaultProfile</span></span>
<span data-ttu-id="613b8-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="613b8-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="613b8-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="613b8-123">-FilePath</span></span>
<span data-ttu-id="613b8-124">Określa nazwę FilePath używaną podczas operacji przywracania.</span><span class="sxs-lookup"><span data-stu-id="613b8-124">Specifies the filepath which is used for restore operation.</span></span>

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

### <span data-ttu-id="613b8-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="613b8-125">-FromFull</span></span>
<span data-ttu-id="613b8-126">Określa pełne RecoveryPoint, do którego będą stosowane kopie zapasowe dziennika.</span><span class="sxs-lookup"><span data-stu-id="613b8-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

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

### <span data-ttu-id="613b8-127">-Item</span><span class="sxs-lookup"><span data-stu-id="613b8-127">-Item</span></span>
<span data-ttu-id="613b8-128">Określa element kopii zapasowej, na którym jest przeprowadzana operacja przywracania.</span><span class="sxs-lookup"><span data-stu-id="613b8-128">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="613b8-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="613b8-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="613b8-130">Określa, że kopia zapasowa bazy danych ma zostać zastąpiona informacjami o bazie danych w punkcie odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="613b8-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="613b8-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="613b8-131">-PointInTime</span></span>
<span data-ttu-id="613b8-132">Godzina zakończenia zakresu czasu, dla którego należy pobrać punkt odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="613b8-132">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="613b8-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="613b8-133">-RecoveryPoint</span></span>
<span data-ttu-id="613b8-134">Obiekt punktu odzyskiwania do przywrócenia</span><span class="sxs-lookup"><span data-stu-id="613b8-134">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="613b8-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="613b8-135">-RestoreAsFiles</span></span>
<span data-ttu-id="613b8-136">Określa, że należy przywrócić bazę danych jako pliki na komputerze.</span><span class="sxs-lookup"><span data-stu-id="613b8-136">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="613b8-137">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="613b8-137">-TargetContainer</span></span>
<span data-ttu-id="613b8-138">Określa docelowy komputer, na którym należy przywrócić pliki bazy danych.</span><span class="sxs-lookup"><span data-stu-id="613b8-138">Specifies the target machine on which DB Files need to be restored.</span></span>

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

### <span data-ttu-id="613b8-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="613b8-139">-TargetItem</span></span>
<span data-ttu-id="613b8-140">Określa cel, w którym należy przywrócić bazę danych.</span><span class="sxs-lookup"><span data-stu-id="613b8-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="613b8-141">W przypadku przywracania SQL wymagana jest ochrona elementu tylko typu SQLInstance.</span><span class="sxs-lookup"><span data-stu-id="613b8-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="613b8-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="613b8-142">-VaultId</span></span>
<span data-ttu-id="613b8-143">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="613b8-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="613b8-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="613b8-144">CommonParameters</span></span>
<span data-ttu-id="613b8-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="613b8-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="613b8-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="613b8-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="613b8-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="613b8-147">INPUTS</span></span>

### <span data-ttu-id="613b8-148">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="613b8-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="613b8-149">System. String</span><span class="sxs-lookup"><span data-stu-id="613b8-149">System.String</span></span>

## <span data-ttu-id="613b8-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="613b8-150">OUTPUTS</span></span>

### <span data-ttu-id="613b8-151">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="613b8-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="613b8-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="613b8-152">NOTES</span></span>

## <span data-ttu-id="613b8-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="613b8-153">RELATED LINKS</span></span>
