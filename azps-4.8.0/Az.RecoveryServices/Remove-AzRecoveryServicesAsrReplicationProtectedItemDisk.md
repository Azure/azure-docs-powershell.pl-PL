---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrreplicationprotecteditemDisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: a5ac137692c8945ba58e848ccca530bd4bc99ed2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221148"
---
# <span data-ttu-id="77e9f-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="77e9f-101">Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="77e9f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77e9f-102">SYNOPSIS</span></span>
<span data-ttu-id="77e9f-103">Usuwa dyski do chronionego elementu replikacji.</span><span class="sxs-lookup"><span data-stu-id="77e9f-103">Removes disks to replication protected item.</span></span>

## <span data-ttu-id="77e9f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77e9f-104">SYNTAX</span></span>

### <span data-ttu-id="77e9f-105">AzureToAzure (domyślny)</span><span class="sxs-lookup"><span data-stu-id="77e9f-105">AzureToAzure (Default)</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -VhdUri <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="77e9f-106">AzureToAzureManagedDisk</span><span class="sxs-lookup"><span data-stu-id="77e9f-106">AzureToAzureManagedDisk</span></span>
```
Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -DiskId <String[]> [-WaitForCompletion] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="77e9f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="77e9f-107">DESCRIPTION</span></span>
<span data-ttu-id="77e9f-108">Polecenie cmdlet **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** usuwa dysk z chronionego elementu replikacji funkcji ASR.</span><span class="sxs-lookup"><span data-stu-id="77e9f-108">The **Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet removes the disk from the ASR replication protected item.</span></span>

## <span data-ttu-id="77e9f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77e9f-109">EXAMPLES</span></span>

### <span data-ttu-id="77e9f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="77e9f-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -VhdUri $vhdUri
```

<span data-ttu-id="77e9f-111">Rozpocznij operację usuwania określonego dysku z chronionej maszyny wirtualnej na dysk niezarządzany.</span><span class="sxs-lookup"><span data-stu-id="77e9f-111">Start the operation to remove specified disk from protection VM for unManaged disk.</span></span>

### <span data-ttu-id="77e9f-112">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="77e9f-112">Example 2</span></span>
```powershell
PS C:\> Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
```

<span data-ttu-id="77e9f-113">Rozpocznij operację usuwania określonego dysku z chronionej maszyny wirtualnej na dysk zarządzany.</span><span class="sxs-lookup"><span data-stu-id="77e9f-113">Start the operation to remove specified disk from protection VM for Managed disk.</span></span>

### <span data-ttu-id="77e9f-114">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="77e9f-114">Example 3</span></span>
```
PS C:\>  $currentJob = Remove-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -DiskId $diskId
PS C:\>  Get-AzRecoveryServicesAsrJob -name $currentJob.id
```

<span data-ttu-id="77e9f-115">Rozpoczyna operację usuwania określonego dysku i zwraca zadanie ASR używane do śledzenia operacji usuwania chronionego dysku.</span><span class="sxs-lookup"><span data-stu-id="77e9f-115">Starts the operation to remove the specified disk and returns the ASR job used to track the remove protected disk operation.</span></span>

## <span data-ttu-id="77e9f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77e9f-116">PARAMETERS</span></span>

### <span data-ttu-id="77e9f-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="77e9f-117">-Confirm</span></span>
<span data-ttu-id="77e9f-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77e9f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77e9f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77e9f-119">-DefaultProfile</span></span>
<span data-ttu-id="77e9f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77e9f-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="77e9f-121">-DiskId</span><span class="sxs-lookup"><span data-stu-id="77e9f-121">-DiskId</span></span>
<span data-ttu-id="77e9f-122">Określa listę zarządzanych identyfikatorów dysków.</span><span class="sxs-lookup"><span data-stu-id="77e9f-122">Specifies the list of managed disk Ids.</span></span>

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

### <span data-ttu-id="77e9f-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="77e9f-123">-InputObject</span></span>
<span data-ttu-id="77e9f-124">Obiekt wejściowy do polecenia cmdlet: obiekt elementu chronionego replikacji ASR, odpowiadający dyskowi, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="77e9f-124">The input object to the cmdlet: The ASR replication protected item object corresponding to which disk is to be removed.</span></span>

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

### <span data-ttu-id="77e9f-125">-VhdUri</span><span class="sxs-lookup"><span data-stu-id="77e9f-125">-VhdUri</span></span>
<span data-ttu-id="77e9f-126">Określa listę identyfikatorów URI dysku VHD.</span><span class="sxs-lookup"><span data-stu-id="77e9f-126">Specifies the list of vhd Uri's.</span></span>

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

### <span data-ttu-id="77e9f-127">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="77e9f-127">-WaitForCompletion</span></span>
<span data-ttu-id="77e9f-128">Oczekiwanie na zakończenie</span><span class="sxs-lookup"><span data-stu-id="77e9f-128">Wait For Completion</span></span>

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

### <span data-ttu-id="77e9f-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77e9f-129">-WhatIf</span></span>
<span data-ttu-id="77e9f-130">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="77e9f-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="77e9f-131">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="77e9f-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77e9f-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77e9f-132">CommonParameters</span></span>
<span data-ttu-id="77e9f-133">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77e9f-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77e9f-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="77e9f-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77e9f-135">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77e9f-135">INPUTS</span></span>

### <span data-ttu-id="77e9f-136">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="77e9f-136">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="77e9f-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77e9f-137">OUTPUTS</span></span>

### <span data-ttu-id="77e9f-138">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="77e9f-138">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="77e9f-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77e9f-139">NOTES</span></span>

## <span data-ttu-id="77e9f-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77e9f-140">RELATED LINKS</span></span>
