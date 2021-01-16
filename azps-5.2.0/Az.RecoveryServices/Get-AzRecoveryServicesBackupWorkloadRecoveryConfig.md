---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 4209755de3475b21405fafd7f1e769bbbe3f7718
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333310"
---
# <span data-ttu-id="95240-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="95240-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="95240-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="95240-102">SYNOPSIS</span></span>
<span data-ttu-id="95240-103">To polecenie konstruuje konfigurację odzyskiwania elementu z kopią zapasową, na przykład SQL DB.</span><span class="sxs-lookup"><span data-stu-id="95240-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="95240-104">W obiekcie konfiguracji są przechowywane wszystkie szczegóły, takie jak tryb odzyskiwania, docelowe miejsca docelowe dla parametrów przywracania i aplikacji, takie jak docelowe ścieżki SQL.</span><span class="sxs-lookup"><span data-stu-id="95240-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="95240-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="95240-105">SYNTAX</span></span>

### <span data-ttu-id="95240-106">RpParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="95240-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="95240-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="95240-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="95240-108">Opis</span><span class="sxs-lookup"><span data-stu-id="95240-108">DESCRIPTION</span></span>
<span data-ttu-id="95240-109">Polecenie zwraca konfigurację odzyskiwania dla elementów AzureWorkload, które są przekazywane do polecenia cmdlet Restore.</span><span class="sxs-lookup"><span data-stu-id="95240-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="95240-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="95240-110">EXAMPLES</span></span>

### <span data-ttu-id="95240-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="95240-111">Example 1</span></span>
```powershell
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="95240-112">Pierwsze polecenie cmdlet służy do pobierania obiektu punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="95240-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="95240-113">Drugie polecenie cmdlet tworzy plan odzyskiwania dla oryginalnej lokalizacji przywracania.</span><span class="sxs-lookup"><span data-stu-id="95240-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="95240-114">Trzecie polecenie cmdlet tworzy plan odzyskiwania dla alternatywnej lokalizacji przywracania.</span><span class="sxs-lookup"><span data-stu-id="95240-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

### <span data-ttu-id="95240-115">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="95240-115">Example 2</span></span>

<span data-ttu-id="95240-116">To polecenie konstruuje konfigurację odzyskiwania elementu z kopią zapasową, na przykład SQL DB.</span><span class="sxs-lookup"><span data-stu-id="95240-116">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="95240-117">(autogenerowana)</span><span class="sxs-lookup"><span data-stu-id="95240-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig -AlternateWorkloadRestore -RecoveryPoint $rp[0] -TargetItem <ProtectableItemBase> -VaultId $vault.ID
```

## <span data-ttu-id="95240-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="95240-118">PARAMETERS</span></span>

### <span data-ttu-id="95240-119">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="95240-119">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="95240-120">Określa, że kopia zapasowa bazy danych powinna zostać przywrócona na inny wybrany serwer.</span><span class="sxs-lookup"><span data-stu-id="95240-120">Specifies that the backed up DB should be restored onto another selected server.</span></span>

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

### <span data-ttu-id="95240-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95240-121">-DefaultProfile</span></span>
<span data-ttu-id="95240-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="95240-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="95240-123">-FilePath</span><span class="sxs-lookup"><span data-stu-id="95240-123">-FilePath</span></span>
<span data-ttu-id="95240-124">Określa nazwę FilePath używaną podczas operacji przywracania.</span><span class="sxs-lookup"><span data-stu-id="95240-124">Specifies the filepath which is used for restore operation.</span></span>

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

### <span data-ttu-id="95240-125">-FromFull</span><span class="sxs-lookup"><span data-stu-id="95240-125">-FromFull</span></span>
<span data-ttu-id="95240-126">Określa pełne RecoveryPoint, do którego będą stosowane kopie zapasowe dziennika.</span><span class="sxs-lookup"><span data-stu-id="95240-126">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

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

### <span data-ttu-id="95240-127">-Item</span><span class="sxs-lookup"><span data-stu-id="95240-127">-Item</span></span>
<span data-ttu-id="95240-128">Określa element kopii zapasowej, na którym jest przeprowadzana operacja przywracania.</span><span class="sxs-lookup"><span data-stu-id="95240-128">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="95240-129">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="95240-129">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="95240-130">Określa, że kopia zapasowa bazy danych ma zostać zastąpiona informacjami o bazie danych w punkcie odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="95240-130">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="95240-131">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="95240-131">-PointInTime</span></span>
<span data-ttu-id="95240-132">Godzina zakończenia zakresu czasu, dla którego należy pobrać punkt odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="95240-132">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="95240-133">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="95240-133">-RecoveryPoint</span></span>
<span data-ttu-id="95240-134">Obiekt punktu odzyskiwania do przywrócenia</span><span class="sxs-lookup"><span data-stu-id="95240-134">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="95240-135">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="95240-135">-RestoreAsFiles</span></span>
<span data-ttu-id="95240-136">Określa, że należy przywrócić bazę danych jako pliki na komputerze.</span><span class="sxs-lookup"><span data-stu-id="95240-136">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="95240-137">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="95240-137">-TargetContainer</span></span>
<span data-ttu-id="95240-138">Określa docelowy komputer, na którym należy przywrócić pliki bazy danych.</span><span class="sxs-lookup"><span data-stu-id="95240-138">Specifies the target machine on which DB Files need to be restored.</span></span>

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

### <span data-ttu-id="95240-139">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="95240-139">-TargetItem</span></span>
<span data-ttu-id="95240-140">Określa cel, w którym należy przywrócić bazę danych.</span><span class="sxs-lookup"><span data-stu-id="95240-140">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="95240-141">W przypadku przywracania SQL wymagana jest ochrona elementu tylko typu SQLInstance.</span><span class="sxs-lookup"><span data-stu-id="95240-141">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="95240-142">-VaultId</span><span class="sxs-lookup"><span data-stu-id="95240-142">-VaultId</span></span>
<span data-ttu-id="95240-143">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="95240-143">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="95240-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95240-144">CommonParameters</span></span>
<span data-ttu-id="95240-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="95240-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95240-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="95240-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95240-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="95240-147">INPUTS</span></span>

### <span data-ttu-id="95240-148">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="95240-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="95240-149">System. String</span><span class="sxs-lookup"><span data-stu-id="95240-149">System.String</span></span>

## <span data-ttu-id="95240-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="95240-150">OUTPUTS</span></span>

### <span data-ttu-id="95240-151">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="95240-151">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="95240-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="95240-152">NOTES</span></span>

## <span data-ttu-id="95240-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="95240-153">RELATED LINKS</span></span>
