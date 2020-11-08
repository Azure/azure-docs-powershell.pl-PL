---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 6033421b9a78e7cb531d2a33eabba1e97010c4f6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053686"
---
# <span data-ttu-id="0f976-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="0f976-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="0f976-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f976-102">SYNOPSIS</span></span>
<span data-ttu-id="0f976-103">To polecenie konstruuje konfigurację odzyskiwania elementu z kopią zapasową, na przykład SQL DB.</span><span class="sxs-lookup"><span data-stu-id="0f976-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="0f976-104">W obiekcie konfiguracji są przechowywane wszystkie szczegóły, takie jak tryb odzyskiwania, docelowe miejsca docelowe dla parametrów przywracania i aplikacji, takie jak docelowe ścieżki SQL.</span><span class="sxs-lookup"><span data-stu-id="0f976-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="0f976-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f976-105">SYNTAX</span></span>

### <span data-ttu-id="0f976-106">RpParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="0f976-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0f976-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="0f976-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-TargetContainer <ContainerBase>] [-RestoreAsFiles]
 [-FromFull <RecoveryPointBase>] [-FilePath <String>] [-VaultId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0f976-108">Opis</span><span class="sxs-lookup"><span data-stu-id="0f976-108">DESCRIPTION</span></span>
<span data-ttu-id="0f976-109">Polecenie zwraca konfigurację odzyskiwania dla elementów AzureWorkload, które są przekazywane do polecenia cmdlet Restore.</span><span class="sxs-lookup"><span data-stu-id="0f976-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="0f976-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f976-110">EXAMPLES</span></span>

### <span data-ttu-id="0f976-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="0f976-111">Example 1</span></span>
```
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="0f976-112">Pierwsze polecenie cmdlet służy do pobierania obiektu punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="0f976-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="0f976-113">Drugie polecenie cmdlet tworzy plan odzyskiwania dla oryginalnej lokalizacji przywracania.</span><span class="sxs-lookup"><span data-stu-id="0f976-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="0f976-114">Trzecie polecenie cmdlet tworzy plan odzyskiwania dla alternatywnej lokalizacji przywracania.</span><span class="sxs-lookup"><span data-stu-id="0f976-114">THe third cmdlet creates a recovery plan for a alternate location restore.</span></span>

## <span data-ttu-id="0f976-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f976-115">PARAMETERS</span></span>

### <span data-ttu-id="0f976-116">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="0f976-116">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="0f976-117">Określa, że kopia zapasowa bazy danych ma zostać zastąpiona informacjami o bazie danych w punkcie odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="0f976-117">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="0f976-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f976-118">-DefaultProfile</span></span>
<span data-ttu-id="0f976-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0f976-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0f976-120">-FilePath</span><span class="sxs-lookup"><span data-stu-id="0f976-120">-FilePath</span></span>
<span data-ttu-id="0f976-121">Określa nazwę FilePath dla operacji przywracania.</span><span class="sxs-lookup"><span data-stu-id="0f976-121">Specifies the filepath for restore operation.</span></span>

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

### <span data-ttu-id="0f976-122">-FromFull</span><span class="sxs-lookup"><span data-stu-id="0f976-122">-FromFull</span></span>
<span data-ttu-id="0f976-123">Określa pełne RecoveryPoint, do którego będą stosowane kopie zapasowe dziennika.</span><span class="sxs-lookup"><span data-stu-id="0f976-123">Specifies the Full RecoveryPoint to which Log backups will be applied.</span></span>

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

### <span data-ttu-id="0f976-124">-Item</span><span class="sxs-lookup"><span data-stu-id="0f976-124">-Item</span></span>
<span data-ttu-id="0f976-125">Określa element kopii zapasowej, na którym jest przeprowadzana operacja przywracania.</span><span class="sxs-lookup"><span data-stu-id="0f976-125">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="0f976-126">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="0f976-126">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="0f976-127">Określa, że kopia zapasowa bazy danych ma zostać zastąpiona informacjami o bazie danych w punkcie odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="0f976-127">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="0f976-128">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="0f976-128">-PointInTime</span></span>
<span data-ttu-id="0f976-129">Godzina zakończenia zakresu czasu, dla którego należy pobrać punkt odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="0f976-129">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="0f976-130">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="0f976-130">-RecoveryPoint</span></span>
<span data-ttu-id="0f976-131">Obiekt punktu odzyskiwania do przywrócenia</span><span class="sxs-lookup"><span data-stu-id="0f976-131">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="0f976-132">-RestoreAsFiles</span><span class="sxs-lookup"><span data-stu-id="0f976-132">-RestoreAsFiles</span></span>
<span data-ttu-id="0f976-133">Określa, że należy przywrócić bazę danych jako pliki na komputerze.</span><span class="sxs-lookup"><span data-stu-id="0f976-133">Specifies to restore Database as files in a machine.</span></span>

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

### <span data-ttu-id="0f976-134">-TargetContainer</span><span class="sxs-lookup"><span data-stu-id="0f976-134">-TargetContainer</span></span>
<span data-ttu-id="0f976-135">Określa docelowy komputer, na którym należy przywrócić pliki bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0f976-135">Specifies the target machine on which DB Files need to be restored.</span></span>

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

### <span data-ttu-id="0f976-136">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="0f976-136">-TargetItem</span></span>
<span data-ttu-id="0f976-137">Określa cel, w którym należy przywrócić bazę danych.</span><span class="sxs-lookup"><span data-stu-id="0f976-137">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="0f976-138">W przypadku przywracania SQL wymagana jest ochrona elementu tylko typu SQLInstance.</span><span class="sxs-lookup"><span data-stu-id="0f976-138">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="0f976-139">-VaultId</span><span class="sxs-lookup"><span data-stu-id="0f976-139">-VaultId</span></span>
<span data-ttu-id="0f976-140">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="0f976-140">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="0f976-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f976-141">CommonParameters</span></span>
<span data-ttu-id="0f976-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f976-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f976-143">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="0f976-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f976-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f976-144">INPUTS</span></span>

### <span data-ttu-id="0f976-145">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="0f976-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="0f976-146">System. String</span><span class="sxs-lookup"><span data-stu-id="0f976-146">System.String</span></span>

## <span data-ttu-id="0f976-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f976-147">OUTPUTS</span></span>

### <span data-ttu-id="0f976-148">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="0f976-148">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="0f976-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f976-149">NOTES</span></span>

## <span data-ttu-id="0f976-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f976-150">RELATED LINKS</span></span>
