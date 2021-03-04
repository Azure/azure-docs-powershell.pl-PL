---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/remove-azrecoveryservicesasrpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesAsrPolicy.md
ms.openlocfilehash: 5743d1d9288f0045755aab752274c24640b3c548
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953274"
---
# <span data-ttu-id="5e88d-101">Remove-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="5e88d-101">Remove-AzRecoveryServicesAsrPolicy</span></span>

## <span data-ttu-id="5e88d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e88d-102">SYNOPSIS</span></span>
<span data-ttu-id="5e88d-103">Usuwa określone zasady replikacji asr z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="5e88d-103">Deletes the specified ASR replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="5e88d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5e88d-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesAsrPolicy -InputObject <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e88d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="5e88d-105">DESCRIPTION</span></span>
<span data-ttu-id="5e88d-106">Polecenie **cmdlet Remove-AzRecoveryServicesAsrPolicy** usunąło określone zasady replikacji z magazynu usług odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="5e88d-106">The **Remove-AzRecoveryServicesAsrPolicy** cmdlet deleted the specified replication policy from the Recovery Services vault.</span></span>

## <span data-ttu-id="5e88d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5e88d-107">EXAMPLES</span></span>

### <span data-ttu-id="5e88d-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5e88d-108">Example 1</span></span>
```
PS C:\> $currentJob = Remove-AzRecoveryServicesAsrPolicy -Policy $Policy
```

<span data-ttu-id="5e88d-109">Rozpoczyna usuwanie określonych zasad replikacji i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="5e88d-109">Starts the deletion of the specified replication policy and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="5e88d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e88d-110">PARAMETERS</span></span>

### <span data-ttu-id="5e88d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e88d-111">-DefaultProfile</span></span>
<span data-ttu-id="5e88d-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e88d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="5e88d-113">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5e88d-113">-InputObject</span></span>
<span data-ttu-id="5e88d-114">Obiekt wejściowy do polecenia cmdlet: obiekt zasad replikacji asr odpowiadający zasadom replikacji, które mają zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="5e88d-114">The input object to the cmdlet: The ASR replication policy object corresponding to the replication policy to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: Policy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e88d-115">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e88d-115">-Confirm</span></span>
<span data-ttu-id="5e88d-116">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5e88d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e88d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e88d-117">-WhatIf</span></span>
<span data-ttu-id="5e88d-118">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e88d-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e88d-119">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5e88d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e88d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e88d-120">CommonParameters</span></span>
<span data-ttu-id="5e88d-121">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e88d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e88d-122">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e88d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e88d-123">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e88d-123">INPUTS</span></span>

### <span data-ttu-id="5e88d-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="5e88d-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRPolicy</span></span>

## <span data-ttu-id="5e88d-125">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e88d-125">OUTPUTS</span></span>

### <span data-ttu-id="5e88d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="5e88d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="5e88d-127">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5e88d-127">NOTES</span></span>

## <span data-ttu-id="5e88d-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e88d-128">RELATED LINKS</span></span>

[<span data-ttu-id="5e88d-129">Get-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="5e88d-129">Get-AzRecoveryServicesAsrPolicy</span></span>](./Get-AzRecoveryServicesAsrPolicy.md)

[<span data-ttu-id="5e88d-130">New-AzRecoveryServicesAsrPolicy</span><span class="sxs-lookup"><span data-stu-id="5e88d-130">New-AzRecoveryServicesAsrPolicy</span></span>](./New-AzRecoveryServicesAsrPolicy.md)
