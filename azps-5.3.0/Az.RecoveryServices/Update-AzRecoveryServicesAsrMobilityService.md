---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 3374ba9cbc1db05b80da6b0b6dd5c5d89212ad51
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498514"
---
# <span data-ttu-id="ef4d9-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="ef4d9-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="ef4d9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef4d9-102">SYNOPSIS</span></span>
<span data-ttu-id="ef4d9-103">Aktualizacje agenta usługi mobilności push na chronione komputery.</span><span class="sxs-lookup"><span data-stu-id="ef4d9-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="ef4d9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef4d9-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef4d9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ef4d9-105">DESCRIPTION</span></span>
<span data-ttu-id="ef4d9-106">Polecenie cmdlet **Update-AzRecoveryServicesAsrMobilityService** próbuje przepchnąć aktualizacje agenta usługi mobilności na chronione komputery (Jeśli aktualizacja jest dostępna).</span><span class="sxs-lookup"><span data-stu-id="ef4d9-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="ef4d9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef4d9-107">EXAMPLES</span></span>

### <span data-ttu-id="ef4d9-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ef4d9-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="ef4d9-109">Zadanie śledzenia agenta usługi ochrony przed mobilnością dla elementu chronionego replikacji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="ef4d9-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="ef4d9-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef4d9-110">PARAMETERS</span></span>

### <span data-ttu-id="ef4d9-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="ef4d9-111">-Account</span></span>
<span data-ttu-id="ef4d9-112">Identyfikator konta Uruchom jako, który ma być używany do wypychania aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="ef4d9-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="ef4d9-113">Musi znajdować się na liście kont Uruchom jako w sieci szkieletowej ASR odpowiadającej aktualizowanemu komputerowi.</span><span class="sxs-lookup"><span data-stu-id="ef4d9-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRunAsAccount
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef4d9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef4d9-114">-DefaultProfile</span></span>
<span data-ttu-id="ef4d9-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ef4d9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef4d9-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ef4d9-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="ef4d9-117">Element chroniony replikacji odzyskiwania witryny Azure do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="ef4d9-117">Azure Site Recovery replication protected item to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef4d9-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ef4d9-118">-Confirm</span></span>
<span data-ttu-id="ef4d9-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef4d9-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef4d9-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef4d9-120">-WhatIf</span></span>
<span data-ttu-id="ef4d9-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef4d9-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef4d9-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ef4d9-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef4d9-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef4d9-123">CommonParameters</span></span>
<span data-ttu-id="ef4d9-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef4d9-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef4d9-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ef4d9-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef4d9-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef4d9-126">INPUTS</span></span>

### <span data-ttu-id="ef4d9-127">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="ef4d9-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="ef4d9-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef4d9-128">OUTPUTS</span></span>

### <span data-ttu-id="ef4d9-129">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="ef4d9-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ef4d9-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef4d9-130">NOTES</span></span>

## <span data-ttu-id="ef4d9-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef4d9-131">RELATED LINKS</span></span>
