---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: ab8c2bb74f381be898dc243ddd010462f8158ed2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100179003"
---
# <span data-ttu-id="b73de-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="b73de-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="b73de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b73de-102">SYNOPSIS</span></span>
<span data-ttu-id="b73de-103">Dodaj dysk w celu ochrony już chronionej maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b73de-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="b73de-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b73de-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b73de-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b73de-105">DESCRIPTION</span></span>
<span data-ttu-id="b73de-106">Polecenie cmdlet **Add-AzRecoveryServicesAsrReplicationProtectedItem Jak** dodać dysk w celu ochrony już chronionej maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b73de-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="b73de-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b73de-107">EXAMPLES</span></span>

### <span data-ttu-id="b73de-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b73de-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="b73de-109">Uruchom operację, aby dodać określoną konfigurację dysku w celu ochrony.</span><span class="sxs-lookup"><span data-stu-id="b73de-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="b73de-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="b73de-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="b73de-111">Uruchom operację, aby dodać określoną konfigurację dysku w celu ochrony. Element chroniony replikacją danych wejściowych rurowych.</span><span class="sxs-lookup"><span data-stu-id="b73de-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="b73de-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b73de-112">PARAMETERS</span></span>

### <span data-ttu-id="b73de-113">-AzureToAzureChatReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="b73de-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="b73de-114">Określa konfigurację dysku, która ma być używana na wypadek ochrony dysku platformy Azure do scenariusza odzyskiwania po awarii platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b73de-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRAzuretoAzureDiskReplicationConfig[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b73de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b73de-115">-DefaultProfile</span></span>
<span data-ttu-id="b73de-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b73de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b73de-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b73de-117">-InputObject</span></span>
<span data-ttu-id="b73de-118">Obiekt wejściowy do polecenia cmdlet: obiekt elementu chronionego replikacją asr, odpowiadający noweowi dyskowi, który ma być chroniony.</span><span class="sxs-lookup"><span data-stu-id="b73de-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases: ReplicationProtectedItem

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b73de-119">- WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="b73de-119">-WaitForCompletion</span></span>
<span data-ttu-id="b73de-120">Poczekaj na ukończenie</span><span class="sxs-lookup"><span data-stu-id="b73de-120">Wait For Completion</span></span>

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

### <span data-ttu-id="b73de-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b73de-121">-Confirm</span></span>
<span data-ttu-id="b73de-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b73de-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b73de-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b73de-123">-WhatIf</span></span>
<span data-ttu-id="b73de-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b73de-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b73de-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b73de-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b73de-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b73de-126">CommonParameters</span></span>
<span data-ttu-id="b73de-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b73de-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b73de-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b73de-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b73de-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b73de-129">INPUTS</span></span>

### <span data-ttu-id="b73de-130">Brak</span><span class="sxs-lookup"><span data-stu-id="b73de-130">None</span></span>

## <span data-ttu-id="b73de-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b73de-131">OUTPUTS</span></span>

### <span data-ttu-id="b73de-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="b73de-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b73de-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b73de-133">NOTES</span></span>

## <span data-ttu-id="b73de-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b73de-134">RELATED LINKS</span></span>
