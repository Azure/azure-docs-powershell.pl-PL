---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/update-azrecoveryservicesasrrecoveryplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Update-AzRecoveryServicesAsrRecoveryPlan.md
ms.openlocfilehash: b0780e4fb82a3e58e70f3a0bd64b5211ad07fd42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990837"
---
# <span data-ttu-id="1a6e3-101">Update-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1a6e3-101">Update-AzRecoveryServicesAsrRecoveryPlan</span></span>

## <span data-ttu-id="1a6e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a6e3-102">SYNOPSIS</span></span>
<span data-ttu-id="1a6e3-103">Aktualizuje zawartość planu odzyskiwania witryn platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-103">Updates the contents of an Azure Site recovery plan.</span></span>

## <span data-ttu-id="1a6e3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1a6e3-104">SYNTAX</span></span>

### <span data-ttu-id="1a6e3-105">ByRPObject (domyślne)</span><span class="sxs-lookup"><span data-stu-id="1a6e3-105">ByRPObject (Default)</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -InputObject <ASRRecoveryPlan>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a6e3-106">ByRPFile</span><span class="sxs-lookup"><span data-stu-id="1a6e3-106">ByRPFile</span></span>
```
Update-AzRecoveryServicesAsrRecoveryPlan -Path <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1a6e3-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="1a6e3-107">DESCRIPTION</span></span>
<span data-ttu-id="1a6e3-108">Polecenie cmdlet **Update-AzRecoveryServicesAsrRecoveryPlan** aktualizuje zawartość planu odzyskiwania przy użyciu zawartości określonego obiektu planu odzyskiwania asr lub pliku json planu odzyskiwania asr.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-108">The **Update-AzRecoveryServicesAsrRecoveryPlan** cmdlet updates the contents of a recovery plan using the contents of the specified ASR recovery plan object or ASR recovery plan definition json file.</span></span>

## <span data-ttu-id="1a6e3-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1a6e3-109">EXAMPLES</span></span>

### <span data-ttu-id="1a6e3-110">Przykład 1. Aktualizowanie planu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="1a6e3-110">Example 1: Update a recovery plan</span></span>
```
PS C:\> $currentJob = Update-AzRecoveryServicesAsrRecoveryPlan -RecoveryPlan $RP
```

<span data-ttu-id="1a6e3-111">Rozpocznij operację aktualizowania planu odzyskiwania przy użyciu zawartości określonego obiektu planu odzyskiwania funkcji ASR i zwraca zadanie asr służące do śledzenia operacji.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-111">Start the operation of updating a recovery plan using the contents of the specified ASR recovery plan object and returns the ASR job used to track the operation.</span></span>

## <span data-ttu-id="1a6e3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1a6e3-112">PARAMETERS</span></span>

### <span data-ttu-id="1a6e3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a6e3-113">-DefaultProfile</span></span>
<span data-ttu-id="1a6e3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="1a6e3-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1a6e3-115">-InputObject</span></span>
<span data-ttu-id="1a6e3-116">Obiekt input do polecenia cmdlet: Określa obiekt planu odzyskiwania asr, którego zawartość służy do aktualizowania planu odzyskiwania, do którego ten obiekt się odnosi.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-116">Input Object to the cmdlet: Specifies an ASR recovery plan object, the contents of which are used to update the recovery plan referred to by the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: RecoveryPlan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1a6e3-117">— Ścieżka</span><span class="sxs-lookup"><span data-stu-id="1a6e3-117">-Path</span></span>
<span data-ttu-id="1a6e3-118">Określa ścieżkę pliku json definicji planu odzyskiwania używanego do aktualizowania planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-118">Specifies the path of the recovery plan definition json file used to update the recovery plan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByRPFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1a6e3-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1a6e3-119">-Confirm</span></span>
<span data-ttu-id="1a6e3-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a6e3-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a6e3-121">-WhatIf</span></span>
<span data-ttu-id="1a6e3-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a6e3-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a6e3-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a6e3-124">CommonParameters</span></span>
<span data-ttu-id="1a6e3-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a6e3-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a6e3-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1a6e3-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a6e3-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a6e3-127">INPUTS</span></span>

### <span data-ttu-id="1a6e3-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1a6e3-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRRecoveryPlan</span></span>

## <span data-ttu-id="1a6e3-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1a6e3-129">OUTPUTS</span></span>

### <span data-ttu-id="1a6e3-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="1a6e3-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="1a6e3-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1a6e3-131">NOTES</span></span>

## <span data-ttu-id="1a6e3-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1a6e3-132">RELATED LINKS</span></span>

[<span data-ttu-id="1a6e3-133">Get-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1a6e3-133">Get-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Get-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="1a6e3-134">New-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1a6e3-134">New-AzRecoveryServicesAsrRecoveryPlan</span></span>](./New-AzRecoveryServicesAsrRecoveryPlan.md)

[<span data-ttu-id="1a6e3-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="1a6e3-135">Remove-AzRecoveryServicesAsrRecoveryPlan</span></span>](./Remove-AzRecoveryServicesAsrRecoveryPlan.md)
