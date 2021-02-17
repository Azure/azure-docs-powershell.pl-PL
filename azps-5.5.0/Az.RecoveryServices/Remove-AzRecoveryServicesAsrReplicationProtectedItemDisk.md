---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: a5ac137692c8945ba58e848ccca530bd4bc99ed2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186610"
---
# <span data-ttu-id="d6b8f-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="d6b8f-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="d6b8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="d6b8f-103">Usuwa błędy dyskowe dla elementu chronionego replikacją.</span><span class="sxs-lookup"><span data-stu-id="d6b8f-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="d6b8f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d6b8f-104">SYNTAX</span></span>

### <span data-ttu-id="d6b8f-105">AzureToAzure (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d6b8f-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d6b8f-106">AzureToAzureManagedChat</span><span class="sxs-lookup"><span data-stu-id="d6b8f-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d6b8f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d6b8f-107">DESCRIPTION</span></span>
<span data-ttu-id="d6b8f-108">Polecenie cmdlet **Remove-AzRecoveryServicesAsrReplicationProtectedItem Jednak** usuwa dysk z elementu chronionego replikacją asr.</span><span class="sxs-lookup"><span data-stu-id="d6b8f-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="d6b8f-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d6b8f-109">EXAMPLES</span></span>

### <span data-ttu-id="d6b8f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d6b8f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="d6b8f-111">Uruchom operację, aby usunąć określony dysk z maszyny wirtualnej ochrony dla dysku niezamówinego.</span><span class="sxs-lookup"><span data-stu-id="d6b8f-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="d6b8f-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d6b8f-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="d6b8f-113">Uruchom operację, aby usunąć określony dysk z maszyny wirtualnej ochrony dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="d6b8f-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="d6b8f-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="d6b8f-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="d6b8f-115">Rozpoczyna operację usunięcia określonego dysku i zwraca zadanie asr służące do śledzenia operacji usuwania dysku chronionego.</span><span class="sxs-lookup"><span data-stu-id="d6b8f-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="d6b8f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d6b8f-116">PARAMETERS</span></span>

### <span data-ttu-id="d6b8f-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d6b8f-117">-Confirm</span></span>
<span data-ttu-id="d6b8f-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d6b8f-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b8f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6b8f-119">-DefaultProfile</span></span>
<span data-ttu-id="d6b8f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d6b8f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b8f-121">- DiskId</span><span class="sxs-lookup"><span data-stu-id="d6b8f-121">-DiskId</span></span>
<span data-ttu-id="d6b8f-122">Określa listę identyfikatorów dysków zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="d6b8f-122">Specifies the list of managed disk Ids.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzureManagedDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b8f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d6b8f-123">-InputObject</span></span>
<span data-ttu-id="d6b8f-124">Obiekt wejściowy do polecenia cmdlet: obiekt elementu chronionego replikacją asr, odpowiadający dyskowi, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="d6b8f-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

```yaml
Type: ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6b8f-125">- VhdUri</span><span class="sxs-lookup"><span data-stu-id="d6b8f-125">-VhdUri</span></span>
<span data-ttu-id="d6b8f-126">Określa listę vhd Uri.</span><span class="sxs-lookup"><span data-stu-id="d6b8f-126">Specifies the list of vhd Uri's.</span></span>

```yaml
Type: String[]
Parameter Sets: AzureToAzure
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b8f-127">- WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="d6b8f-127">-WaitForCompletion</span></span>
<span data-ttu-id="d6b8f-128">Poczekaj na ukończenie</span><span class="sxs-lookup"><span data-stu-id="d6b8f-128">Wait For Completion</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b8f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d6b8f-129">-WhatIf</span></span>
<span data-ttu-id="d6b8f-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d6b8f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d6b8f-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d6b8f-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6b8f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6b8f-132">CommonParameters</span></span>
<span data-ttu-id="d6b8f-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d6b8f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6b8f-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d6b8f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6b8f-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d6b8f-135">INPUTS</span></span>

### <span data-ttu-id="d6b8f-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="d6b8f-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="d6b8f-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d6b8f-137">OUTPUTS</span></span>

### <span data-ttu-id="d6b8f-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="d6b8f-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d6b8f-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d6b8f-139">NOTES</span></span>

## <span data-ttu-id="d6b8f-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d6b8f-140">RELATED LINKS</span></span>
