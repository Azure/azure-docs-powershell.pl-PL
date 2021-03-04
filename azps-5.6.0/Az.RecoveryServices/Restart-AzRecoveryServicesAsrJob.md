---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/restart-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Restart-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 2609ed7483499445dbdd093d0059b76b7e781ef8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101953105"
---
# <span data-ttu-id="79c6d-101">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="79c6d-101">Restart-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="79c6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79c6d-102">SYNOPSIS</span></span>
<span data-ttu-id="79c6d-103">Powoduje ponowne uruchomienie zadania odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="79c6d-103">Restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="79c6d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="79c6d-104">SYNTAX</span></span>

### <span data-ttu-id="79c6d-105">ByObject (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="79c6d-105">ByObject (Default)</span></span>
```
Restart-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79c6d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="79c6d-106">ByName</span></span>
```
Restart-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79c6d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="79c6d-107">DESCRIPTION</span></span>
<span data-ttu-id="79c6d-108">Polecenie **cmdlet Restart-AzRecoveryServicesAsrJob** powoduje ponowne uruchomienie zadania odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="79c6d-108">The **Restart-AzRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="79c6d-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="79c6d-109">EXAMPLES</span></span>

### <span data-ttu-id="79c6d-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79c6d-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="79c6d-111">Powoduje ponowne uruchomienie określonego zadania asr i zwraca zaktualizowany obiekt zadania asr zadania asr.</span><span class="sxs-lookup"><span data-stu-id="79c6d-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="79c6d-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="79c6d-112">PARAMETERS</span></span>

### <span data-ttu-id="79c6d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79c6d-113">-DefaultProfile</span></span>
<span data-ttu-id="79c6d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="79c6d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="79c6d-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79c6d-115">-InputObject</span></span>
<span data-ttu-id="79c6d-116">Obiekt wejściowy do polecenia cmdlet: Obiekt zadania asr odpowiadający zadaniu asr do ponownego uruchomienia</span><span class="sxs-lookup"><span data-stu-id="79c6d-116">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>


```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79c6d-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="79c6d-117">-Name</span></span>
<span data-ttu-id="79c6d-118">Określanie zadania według nazwy.</span><span class="sxs-lookup"><span data-stu-id="79c6d-118">Specify the job by name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79c6d-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79c6d-119">-Confirm</span></span>
<span data-ttu-id="79c6d-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="79c6d-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79c6d-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79c6d-121">-WhatIf</span></span>
<span data-ttu-id="79c6d-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79c6d-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79c6d-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="79c6d-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79c6d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79c6d-124">CommonParameters</span></span>
<span data-ttu-id="79c6d-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79c6d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79c6d-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79c6d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79c6d-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79c6d-127">INPUTS</span></span>

### <span data-ttu-id="79c6d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="79c6d-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="79c6d-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79c6d-129">OUTPUTS</span></span>

### <span data-ttu-id="79c6d-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="79c6d-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="79c6d-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="79c6d-131">NOTES</span></span>

## <span data-ttu-id="79c6d-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79c6d-132">RELATED LINKS</span></span>

[<span data-ttu-id="79c6d-133">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="79c6d-133">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="79c6d-134">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="79c6d-134">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="79c6d-135">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="79c6d-135">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
