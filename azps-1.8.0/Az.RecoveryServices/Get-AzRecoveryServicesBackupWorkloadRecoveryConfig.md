---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupworkloadrecoveryconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupWorkloadRecoveryConfig.md
ms.openlocfilehash: 6b0f2e2c5b2e9579a92b2cee7387a19fda498fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708649"
---
# <span data-ttu-id="5236e-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span><span class="sxs-lookup"><span data-stu-id="5236e-101">Get-AzRecoveryServicesBackupWorkloadRecoveryConfig</span></span>

## <span data-ttu-id="5236e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5236e-102">SYNOPSIS</span></span>
<span data-ttu-id="5236e-103">To polecenie konstruuje konfigurację odzyskiwania elementu z kopią zapasową, na przykład SQL DB.</span><span class="sxs-lookup"><span data-stu-id="5236e-103">This command constructs the recovery configuration of a backed up item such as SQL DB.</span></span> <span data-ttu-id="5236e-104">W obiekcie konfiguracji są przechowywane wszystkie szczegóły, takie jak tryb odzyskiwania, docelowe miejsca docelowe dla parametrów przywracania i aplikacji, takie jak docelowe ścieżki SQL.</span><span class="sxs-lookup"><span data-stu-id="5236e-104">The configuration object stores all details such as the recovery mode, target destinations for the restore and application specific parameters like target physical paths for SQL.</span></span>

## <span data-ttu-id="5236e-105">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5236e-105">SYNTAX</span></span>

### <span data-ttu-id="5236e-106">RpParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5236e-106">RpParameterSet (Default)</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-RecoveryPoint] <RecoveryPointBase>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5236e-107">LogChainParameterSet</span><span class="sxs-lookup"><span data-stu-id="5236e-107">LogChainParameterSet</span></span>
```
Get-AzRecoveryServicesBackupWorkloadRecoveryConfig [[-PointInTime] <DateTime>]
 [[-TargetItem] <ProtectableItemBase>] [[-Item] <ItemBase>] [-OriginalWorkloadRestore]
 [-AlternateWorkloadRestore] [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5236e-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5236e-108">DESCRIPTION</span></span>
<span data-ttu-id="5236e-109">Polecenie zwraca konfigurację odzyskiwania dla elementów AzureWorkload, które są przekazywane do polecenia cmdlet Restore.</span><span class="sxs-lookup"><span data-stu-id="5236e-109">The command returns a recovery config for AzureWorkload items which is passed to the restore cmdlet.</span></span>

## <span data-ttu-id="5236e-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5236e-110">EXAMPLES</span></span>

### <span data-ttu-id="5236e-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5236e-111">Example 1</span></span>
```
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -OriginalWorkloadRestore
PS C:\> $SQLRecoveryObject = Get-AzRecoveryServicesBackupRecoveryPoint -Item $SQLBkpItem $startdate $enddate | Get-AzRecoveryServicesWorkloadRecoveryConfig -AlternateWorkloadRestore -TargetItem $SQLProtItem
```

<span data-ttu-id="5236e-112">Pierwsze polecenie cmdlet służy do pobierania obiektu punktu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="5236e-112">The first cmdlet is used to get the Recovery point object.</span></span>
<span data-ttu-id="5236e-113">Drugie polecenie cmdlet tworzy plan odzyskiwania dla oryginalnej lokalizacji przywracania.</span><span class="sxs-lookup"><span data-stu-id="5236e-113">The second cmdlet creates a recovery plan for a original location restore.</span></span>
<span data-ttu-id="5236e-114">Trzecie polecenie cmdlet crreats plan odzyskiwania dla alternatywnej lokalizacji przywracania.</span><span class="sxs-lookup"><span data-stu-id="5236e-114">THe third cmdlet crreats a recovery plan for a alternate location restore.</span></span>

## <span data-ttu-id="5236e-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5236e-115">PARAMETERS</span></span>

### <span data-ttu-id="5236e-116">-AlternateWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="5236e-116">-AlternateWorkloadRestore</span></span>
<span data-ttu-id="5236e-117">Określa, że kopia zapasowa bazy danych ma zostać zastąpiona informacjami o bazie danych w punkcie odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="5236e-117">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="5236e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5236e-118">-DefaultProfile</span></span>
<span data-ttu-id="5236e-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5236e-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5236e-120">-Item</span><span class="sxs-lookup"><span data-stu-id="5236e-120">-Item</span></span>
<span data-ttu-id="5236e-121">Określa element kopii zapasowej, na którym jest przeprowadzana operacja przywracania.</span><span class="sxs-lookup"><span data-stu-id="5236e-121">Specifies the backup item on which the restore operation is being performed.</span></span>

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

### <span data-ttu-id="5236e-122">-OriginalWorkloadRestore</span><span class="sxs-lookup"><span data-stu-id="5236e-122">-OriginalWorkloadRestore</span></span>
<span data-ttu-id="5236e-123">Określa, że kopia zapasowa bazy danych ma zostać zastąpiona informacjami o bazie danych w punkcie odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="5236e-123">Specifies that the backed up DB is to be overwritten with the DB information present in the recovery point.</span></span>

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

### <span data-ttu-id="5236e-124">-PointInTime</span><span class="sxs-lookup"><span data-stu-id="5236e-124">-PointInTime</span></span>
<span data-ttu-id="5236e-125">Godzina zakończenia zakresu czasu, dla którego należy pobrać punkt odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="5236e-125">End time of Time range for which recovery point need to be fetched</span></span>

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

### <span data-ttu-id="5236e-126">-RecoveryPoint</span><span class="sxs-lookup"><span data-stu-id="5236e-126">-RecoveryPoint</span></span>
<span data-ttu-id="5236e-127">Obiekt punktu odzyskiwania do przywrócenia</span><span class="sxs-lookup"><span data-stu-id="5236e-127">Recovery point object to be restored</span></span>

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

### <span data-ttu-id="5236e-128">-TargetItem</span><span class="sxs-lookup"><span data-stu-id="5236e-128">-TargetItem</span></span>
<span data-ttu-id="5236e-129">Określa cel, w którym należy przywrócić bazę danych.</span><span class="sxs-lookup"><span data-stu-id="5236e-129">Specifies the target on which the DB needs to be restored.</span></span> <span data-ttu-id="5236e-130">W przypadku przywracania SQL wymagana jest ochrona elementu tylko typu SQLInstance.</span><span class="sxs-lookup"><span data-stu-id="5236e-130">For SQL restores, it needs to be of protectable item type SQLInstance only.</span></span>

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

### <span data-ttu-id="5236e-131">-VaultId</span><span class="sxs-lookup"><span data-stu-id="5236e-131">-VaultId</span></span>
<span data-ttu-id="5236e-132">Identyfikator ARM magazynu usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="5236e-132">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="5236e-133">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5236e-133">-Confirm</span></span>
<span data-ttu-id="5236e-134">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5236e-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5236e-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5236e-135">-WhatIf</span></span>
<span data-ttu-id="5236e-136">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5236e-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5236e-137">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5236e-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5236e-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5236e-138">CommonParameters</span></span>
<span data-ttu-id="5236e-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5236e-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5236e-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5236e-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5236e-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5236e-141">INPUTS</span></span>

### <span data-ttu-id="5236e-142">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryPointBase</span><span class="sxs-lookup"><span data-stu-id="5236e-142">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryPointBase</span></span>
<span data-ttu-id="5236e-143">System. String</span><span class="sxs-lookup"><span data-stu-id="5236e-143">System.String</span></span>

## <span data-ttu-id="5236e-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5236e-144">OUTPUTS</span></span>

### <span data-ttu-id="5236e-145">Microsoft. Azure. Commands. RecoveryServices. Backup. cmdlets. models. RecoveryConfigBase</span><span class="sxs-lookup"><span data-stu-id="5236e-145">Microsoft.Azure.Commands.RecoveryServices.Backup.Cmdlets.Models.RecoveryConfigBase</span></span>

## <span data-ttu-id="5236e-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5236e-146">NOTES</span></span>

## <span data-ttu-id="5236e-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5236e-147">RELATED LINKS</span></span>