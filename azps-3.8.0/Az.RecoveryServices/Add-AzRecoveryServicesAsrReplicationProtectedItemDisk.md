---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/add-azrecoveryservicesasrreplicationprotecteditemdisk
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Add-AzRecoveryServicesAsrReplicationProtectedItemDisk.md
ms.openlocfilehash: ab8c2bb74f381be898dc243ddd010462f8158ed2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049967"
---
# <span data-ttu-id="1c0ca-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span><span class="sxs-lookup"><span data-stu-id="1c0ca-101">Add-AzRecoveryServicesAsrReplicationProtectedItemDisk</span></span>

## <span data-ttu-id="1c0ca-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1c0ca-102">SYNOPSIS</span></span>
<span data-ttu-id="1c0ca-103">Dodaj dysk do ochrony już chronionej maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-103">Add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="1c0ca-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1c0ca-104">SYNTAX</span></span>

```
Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -InputObject <ASRReplicationProtectedItem>
 -AzureToAzureDiskReplicationConfiguration <ASRAzuretoAzureDiskReplicationConfig[]> [-WaitForCompletion]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1c0ca-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1c0ca-105">DESCRIPTION</span></span>
<span data-ttu-id="1c0ca-106">Polecenie cmdlet **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** umożliwia dodanie dysku do ochrony już chronionej maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-106">The **Add-AzRecoveryServicesAsrReplicationProtectedItemDisk** cmdlet add the disk for protection for already protected azure virtual machine.</span></span>

## <span data-ttu-id="1c0ca-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1c0ca-107">EXAMPLES</span></span>

### <span data-ttu-id="1c0ca-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1c0ca-108">Example 1</span></span>
```powershell
PS C:> Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -ReplicationProtectedItem $rpi -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="1c0ca-109">Rozpocznij operację, aby dodać określoną konfigurację dysku do ochrony.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-109">Start the operation to add specified disk configuration for protection.</span></span>

### <span data-ttu-id="1c0ca-110">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="1c0ca-110">Example 2</span></span>
```powershell
PS C:> $ReplicationProtectedItem |Add-AzRecoveryServicesAsrReplicationProtectedItemDisk -AzureToAzureDiskReplicationConfiguration $disk1,$disk2
```

<span data-ttu-id="1c0ca-111">Rozpocznij operację, aby dodać określoną konfigurację dysku do ochrony. Natoku wprowadzanie chronione replikacji elementu.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-111">Start the operation to add specified disk configuration for protection.Piping input replication protected item.</span></span>

## <span data-ttu-id="1c0ca-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1c0ca-112">PARAMETERS</span></span>

### <span data-ttu-id="1c0ca-113">-AzureToAzureDiskReplicationConfiguration</span><span class="sxs-lookup"><span data-stu-id="1c0ca-113">-AzureToAzureDiskReplicationConfiguration</span></span>
<span data-ttu-id="1c0ca-114">Określa konfigurację dysków używaną w celu ochrony dysków na platformie odzyskiwania po awarii usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-114">Specifies the disk configuration to used for disk protection for Azure to Azure disaster recovery scenario.</span></span>

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

### <span data-ttu-id="1c0ca-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1c0ca-115">-DefaultProfile</span></span>
<span data-ttu-id="1c0ca-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1c0ca-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1c0ca-117">-InputObject</span></span>
<span data-ttu-id="1c0ca-118">Obiekt wejściowy do polecenia cmdlet: obiekt elementu chronionego replikacji ASR, dla którego powinien być chroniony nowy dysk.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-118">The input object to the cmdlet: The ASR replication protected item object corresponding to which new disk should be protected.</span></span>

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

### <span data-ttu-id="1c0ca-119">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="1c0ca-119">-WaitForCompletion</span></span>
<span data-ttu-id="1c0ca-120">Oczekiwanie na zakończenie</span><span class="sxs-lookup"><span data-stu-id="1c0ca-120">Wait For Completion</span></span>

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

### <span data-ttu-id="1c0ca-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1c0ca-121">-Confirm</span></span>
<span data-ttu-id="1c0ca-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1c0ca-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1c0ca-123">-WhatIf</span></span>
<span data-ttu-id="1c0ca-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1c0ca-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1c0ca-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1c0ca-126">CommonParameters</span></span>
<span data-ttu-id="1c0ca-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1c0ca-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1c0ca-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1c0ca-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1c0ca-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1c0ca-129">INPUTS</span></span>

### <span data-ttu-id="1c0ca-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="1c0ca-130">None</span></span>

## <span data-ttu-id="1c0ca-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1c0ca-131">OUTPUTS</span></span>

### <span data-ttu-id="1c0ca-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="1c0ca-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1c0ca-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1c0ca-133">NOTES</span></span>

## <span data-ttu-id="1c0ca-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1c0ca-134">RELATED LINKS</span></span>
