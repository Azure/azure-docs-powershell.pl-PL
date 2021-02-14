---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/update-azrecoveryservicesasrmobilityservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrMobilityService.md
ms.openlocfilehash: 3374ba9cbc1db05b80da6b0b6dd5c5d89212ad51
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183866"
---
# <span data-ttu-id="2bd5e-101">Update-AzRecoveryServicesAsrMobilityService</span><span class="sxs-lookup"><span data-stu-id="2bd5e-101">Update-AzRecoveryServicesAsrMobilityService</span></span>

## <span data-ttu-id="2bd5e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2bd5e-102">SYNOPSIS</span></span>
<span data-ttu-id="2bd5e-103">Aktualizacje agenta usługi wypychanej mobilności na komputerach chronionych.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-103">Push mobility service agent updates to protected machines.</span></span>

## <span data-ttu-id="2bd5e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2bd5e-104">SYNTAX</span></span>

```
Update-AzRecoveryServicesAsrMobilityService [-Account <ASRRunAsAccount>]
 -ReplicationProtectedItem <ASRReplicationProtectedItem> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2bd5e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2bd5e-105">DESCRIPTION</span></span>
<span data-ttu-id="2bd5e-106">Polecenie cmdlet **Update-AzRecoveryServicesAsrServiceService** próbuje wypychać aktualizacje agenta usługi mobilności na komputerach chronionych (jeśli jest dostępna aktualizacja).</span><span class="sxs-lookup"><span data-stu-id="2bd5e-106">The **Update-AzRecoveryServicesAsrMobilityService** cmdlet attempts to push mobility service agent updates to protected machines(if an update is available.)</span></span>

## <span data-ttu-id="2bd5e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2bd5e-107">EXAMPLES</span></span>

### <span data-ttu-id="2bd5e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2bd5e-108">Example 1</span></span>
```
PS C:\> Update-AzRecoveryServicesAsrMobilityService -ReplicationProtectedItem $rpi -Account $fabric.fabricSpecificDetails.RunAsAccounts[0]
```

<span data-ttu-id="2bd5e-109">Zadanie śledzenia agenta usługi mobilności chronionej replikacją aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-109">Job to track Update Replication Protected Item's Mobility Service Agent.</span></span>

## <span data-ttu-id="2bd5e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2bd5e-110">PARAMETERS</span></span>

### <span data-ttu-id="2bd5e-111">— Konto</span><span class="sxs-lookup"><span data-stu-id="2bd5e-111">-Account</span></span>
<span data-ttu-id="2bd5e-112">The run as account ID to be used to push the update.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-112">The run as account ID to be used to push the update.</span></span> <span data-ttu-id="2bd5e-113">Musi znajdować się jedna z listy run as accounts in the ASR fabric odpowiadającej aktualizowanej maszynie.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-113">Must be one from the list of run as accounts in the ASR fabric corresponding to machine being updated.</span></span>

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

### <span data-ttu-id="2bd5e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2bd5e-114">-DefaultProfile</span></span>
<span data-ttu-id="2bd5e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2bd5e-116">-ReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2bd5e-116">-ReplicationProtectedItem</span></span>
<span data-ttu-id="2bd5e-117">Element chroniony replikacją usługi Azure Site Recovery do zaktualizowania.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-117">Azure Site Recovery replication protected item to be updated.</span></span>

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

### <span data-ttu-id="2bd5e-118">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2bd5e-118">-Confirm</span></span>
<span data-ttu-id="2bd5e-119">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2bd5e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2bd5e-120">-WhatIf</span></span>
<span data-ttu-id="2bd5e-121">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2bd5e-122">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2bd5e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2bd5e-123">CommonParameters</span></span>
<span data-ttu-id="2bd5e-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2bd5e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2bd5e-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2bd5e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2bd5e-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2bd5e-126">INPUTS</span></span>

### <span data-ttu-id="2bd5e-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span><span class="sxs-lookup"><span data-stu-id="2bd5e-127">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRReplicationProtectedItem</span></span>

## <span data-ttu-id="2bd5e-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2bd5e-128">OUTPUTS</span></span>

### <span data-ttu-id="2bd5e-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="2bd5e-129">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="2bd5e-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2bd5e-130">NOTES</span></span>

## <span data-ttu-id="2bd5e-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2bd5e-131">RELATED LINKS</span></span>
