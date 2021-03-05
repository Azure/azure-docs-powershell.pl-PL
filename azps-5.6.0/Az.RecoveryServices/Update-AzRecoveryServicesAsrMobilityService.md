---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 5c5c9509c7ae242f98c8474a2ab87635f94dd62d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101970369"
---
# <span data-ttu-id="06ef1-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="06ef1-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="06ef1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06ef1-102">SYNOPSIS</span></span>
<span data-ttu-id="06ef1-103">Aktualizacje agenta obsługi mobilności na komputerach chronionych.</span><span class="sxs-lookup"><span data-stu-id="06ef1-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="06ef1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="06ef1-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06ef1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="06ef1-105">DESCRIPTION</span></span>
<span data-ttu-id="06ef1-106">Polecenie **cmdlet Update-AzRecoveryServicesAsrServiceService** próbuje wypychać aktualizacje agenta usługi mobilności na komputerach chronionych (jeśli jest dostępna aktualizacja).</span><span class="sxs-lookup"><span data-stu-id="06ef1-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="06ef1-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="06ef1-107">EXAMPLES</span></span>

### <span data-ttu-id="06ef1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="06ef1-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="06ef1-109">Zadanie śledzenia agenta usługi mobilności chronionej replikacją aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="06ef1-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="06ef1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06ef1-110">PARAMETERS</span></span>

### <span data-ttu-id="06ef1-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="06ef1-111">-Account</span></span>
<span data-ttu-id="06ef1-112">The run as account ID to be used to push the update.</span><span class="sxs-lookup"><span data-stu-id="06ef1-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="06ef1-113">Musi znajdować się jedna z listy run as accounts in the ASR fabric odpowiadającej aktualizowanej maszynie.</span><span class="sxs-lookup"><span data-stu-id="06ef1-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

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

### <span data-ttu-id="06ef1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06ef1-114">-DefaultProfile</span></span>
<span data-ttu-id="06ef1-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="06ef1-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06ef1-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="06ef1-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="06ef1-117">Element chroniony replikacją odzyskiwania witryn platformy Azure do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="06ef1-117">Azure Site Recovery replication protected item to be updated.</span></span>

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

### <span data-ttu-id="06ef1-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="06ef1-118">-Confirm</span></span>
<span data-ttu-id="06ef1-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="06ef1-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06ef1-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06ef1-120">-WhatIf</span></span>
<span data-ttu-id="06ef1-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06ef1-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06ef1-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="06ef1-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06ef1-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06ef1-123">CommonParameters</span></span>
<span data-ttu-id="06ef1-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06ef1-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06ef1-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="06ef1-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06ef1-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06ef1-126">INPUTS</span></span>

### <span data-ttu-id="06ef1-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="06ef1-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="06ef1-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06ef1-128">OUTPUTS</span></span>

### <span data-ttu-id="06ef1-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="06ef1-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="06ef1-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="06ef1-130">NOTES</span></span>

## <span data-ttu-id="06ef1-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06ef1-131">RELATED LINKS</span></span>
