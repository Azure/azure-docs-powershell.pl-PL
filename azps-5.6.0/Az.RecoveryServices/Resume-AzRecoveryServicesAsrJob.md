---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 5f76c9a1adabf69872b4d529df7e3289e4d6745b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997494"
---
# <span data-ttu-id="d057e-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d057e-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="d057e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d057e-102">SYNOPSIS</span></span>
<span data-ttu-id="d057e-103">Wznawia zawieszone zadanie odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d057e-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="d057e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d057e-104">SYNTAX</span></span>

### <span data-ttu-id="d057e-105">ByObject (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="d057e-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d057e-106">ByName</span><span class="sxs-lookup"><span data-stu-id="d057e-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d057e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d057e-107">DESCRIPTION</span></span>
<span data-ttu-id="d057e-108">Polecenie cmdlet **Resume-AzRecoveryServicesAsrJob** wznawia zawieszone zadanie odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d057e-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="d057e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d057e-109">EXAMPLES</span></span>

### <span data-ttu-id="d057e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d057e-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="d057e-111">Wznów określone zadanie, jeśli znajduje się w stanie oczekiwania lub zawieszenia, i zwróć zaktualizowany obiekt zadania asr odpowiadający zadaniu asr.</span><span class="sxs-lookup"><span data-stu-id="d057e-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="d057e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d057e-112">PARAMETERS</span></span>

### <span data-ttu-id="d057e-113">— Komentarz</span><span class="sxs-lookup"><span data-stu-id="d057e-113">-Comment</span></span>
<span data-ttu-id="d057e-114">Komentarze dziennika zadań.</span><span class="sxs-lookup"><span data-stu-id="d057e-114">Comments for the job log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d057e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d057e-115">-DefaultProfile</span></span>
<span data-ttu-id="d057e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d057e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="d057e-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d057e-117">-InputObject</span></span>
<span data-ttu-id="d057e-118">Obiekt wejściowy do polecenia cmdlet: Obiekt Zadania asr odpowiadający zadaniu do wznowienia.</span><span class="sxs-lookup"><span data-stu-id="d057e-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="d057e-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d057e-119">-Name</span></span>
<span data-ttu-id="d057e-120">Określanie zadania asr według nazwy.</span><span class="sxs-lookup"><span data-stu-id="d057e-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="d057e-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d057e-121">-Confirm</span></span>
<span data-ttu-id="d057e-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d057e-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d057e-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d057e-123">-WhatIf</span></span>
<span data-ttu-id="d057e-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d057e-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d057e-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d057e-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d057e-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d057e-126">CommonParameters</span></span>
<span data-ttu-id="d057e-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d057e-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d057e-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d057e-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d057e-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d057e-129">INPUTS</span></span>

### <span data-ttu-id="d057e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="d057e-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d057e-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d057e-131">OUTPUTS</span></span>

### <span data-ttu-id="d057e-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="d057e-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="d057e-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d057e-133">NOTES</span></span>

## <span data-ttu-id="d057e-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d057e-134">RELATED LINKS</span></span>

[<span data-ttu-id="d057e-135">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d057e-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="d057e-136">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d057e-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="d057e-137">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="d057e-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
