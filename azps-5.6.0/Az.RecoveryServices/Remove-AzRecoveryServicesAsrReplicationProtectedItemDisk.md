---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: bee3d9ff2f3e13397afba0cc85ecbb148aedc0cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953153"
---
# <span data-ttu-id="a4dc7-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="a4dc7-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="a4dc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4dc7-102">SYNOPSIS</span></span>
<span data-ttu-id="a4dc7-103">Usuwa błędy dyskowe dla elementu chronionego replikacją.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="a4dc7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a4dc7-104">SYNTAX</span></span>

### <span data-ttu-id="a4dc7-105">AzureToAzure (domyślne)</span><span class="sxs-lookup"><span data-stu-id="a4dc7-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a4dc7-106">AzureToAzureManagedChat</span><span class="sxs-lookup"><span data-stu-id="a4dc7-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a4dc7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="a4dc7-107">DESCRIPTION</span></span>
<span data-ttu-id="a4dc7-108">Polecenie cmdlet **Remove-AzRecoveryServicesAsrReplicationProtectedItem Jednak** usuwa dysk z elementu chronionego replikacją asr.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="a4dc7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a4dc7-109">EXAMPLES</span></span>

### <span data-ttu-id="a4dc7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a4dc7-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="a4dc7-111">Uruchom operację, aby usunąć określony dysk z ochrony maszyny wirtualnej ochrony dla dysku niezamówień.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="a4dc7-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a4dc7-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="a4dc7-113">Uruchom operację, aby usunąć określony dysk z ochrony maszyny wirtualnej dla dysku zarządzanego.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="a4dc7-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="a4dc7-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="a4dc7-115">Rozpoczyna operację usunięcia określonego dysku i zwraca zadanie asr służące do śledzenia operacji usuwania dysku chronionego.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="a4dc7-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4dc7-116">PARAMETERS</span></span>

### <span data-ttu-id="a4dc7-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a4dc7-117">-Confirm</span></span>
<span data-ttu-id="a4dc7-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a4dc7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4dc7-119">-DefaultProfile</span></span>
<span data-ttu-id="a4dc7-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4dc7-121">- DiskId</span><span class="sxs-lookup"><span data-stu-id="a4dc7-121">-DiskId</span></span>
<span data-ttu-id="a4dc7-122">Określa listę identyfikatorów dysków zarządzanych.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-122">Specifies the list of managed disk Ids.</span></span>

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

### <span data-ttu-id="a4dc7-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a4dc7-123">-InputObject</span></span>
<span data-ttu-id="a4dc7-124">Obiekt wejściowy do polecenia cmdlet: obiekt elementu chronionego replikacją asr, odpowiadający dyskowi, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

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

### <span data-ttu-id="a4dc7-125">- VhdUri</span><span class="sxs-lookup"><span data-stu-id="a4dc7-125">-VhdUri</span></span>
<span data-ttu-id="a4dc7-126">Określa listę vhd Uri.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-126">Specifies the list of vhd Uri's.</span></span>

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

### <span data-ttu-id="a4dc7-127">- WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="a4dc7-127">-WaitForCompletion</span></span>
<span data-ttu-id="a4dc7-128">Poczekaj na ukończenie</span><span class="sxs-lookup"><span data-stu-id="a4dc7-128">Wait For Completion</span></span>

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

### <span data-ttu-id="a4dc7-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a4dc7-129">-WhatIf</span></span>
<span data-ttu-id="a4dc7-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a4dc7-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a4dc7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4dc7-132">CommonParameters</span></span>
<span data-ttu-id="a4dc7-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4dc7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4dc7-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a4dc7-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4dc7-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4dc7-135">INPUTS</span></span>

### <span data-ttu-id="a4dc7-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="a4dc7-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="a4dc7-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4dc7-137">OUTPUTS</span></span>

### <span data-ttu-id="a4dc7-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="a4dc7-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="a4dc7-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a4dc7-139">NOTES</span></span>

## <span data-ttu-id="a4dc7-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4dc7-140">RELATED LINKS</span></span>
