---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 6af467e5fd90a7d3028d67297b62f517f512b1b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100191330"
---
# <span data-ttu-id="ceda7-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ceda7-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="ceda7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ceda7-102">SYNOPSIS</span></span>
<span data-ttu-id="ceda7-103">Wznawia zawieszone zadanie odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ceda7-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="ceda7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ceda7-104">SYNTAX</span></span>

### <span data-ttu-id="ceda7-105">ByObject (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="ceda7-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ceda7-106">ByName</span><span class="sxs-lookup"><span data-stu-id="ceda7-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ceda7-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="ceda7-107">DESCRIPTION</span></span>
<span data-ttu-id="ceda7-108">Polecenie cmdlet **Resume-AzRecoveryServicesAsrJob** wznawia zawieszone zadanie odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ceda7-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="ceda7-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ceda7-109">EXAMPLES</span></span>

### <span data-ttu-id="ceda7-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ceda7-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="ceda7-111">Wznów określone zadanie, jeśli znajduje się w stanie oczekiwania lub zawieszenia, i zwróć zaktualizowany obiekt zadania asr odpowiadający zadaniu asr.</span><span class="sxs-lookup"><span data-stu-id="ceda7-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="ceda7-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ceda7-112">PARAMETERS</span></span>

### <span data-ttu-id="ceda7-113">— Komentarz</span><span class="sxs-lookup"><span data-stu-id="ceda7-113">-Comment</span></span>
<span data-ttu-id="ceda7-114">Komentarze dziennika zadań.</span><span class="sxs-lookup"><span data-stu-id="ceda7-114">Comments for the job log.</span></span>

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

### <span data-ttu-id="ceda7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ceda7-115">-DefaultProfile</span></span>
<span data-ttu-id="ceda7-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ceda7-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="ceda7-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ceda7-117">-InputObject</span></span>
<span data-ttu-id="ceda7-118">Obiekt wejściowy do polecenia cmdlet: Obiekt Zadania asr odpowiadający zadaniu do wznowienia.</span><span class="sxs-lookup"><span data-stu-id="ceda7-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="ceda7-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ceda7-119">-Name</span></span>
<span data-ttu-id="ceda7-120">Określanie zadania asr według nazwy.</span><span class="sxs-lookup"><span data-stu-id="ceda7-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="ceda7-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ceda7-121">-Confirm</span></span>
<span data-ttu-id="ceda7-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ceda7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ceda7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ceda7-123">-WhatIf</span></span>
<span data-ttu-id="ceda7-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ceda7-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ceda7-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ceda7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ceda7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ceda7-126">CommonParameters</span></span>
<span data-ttu-id="ceda7-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ceda7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ceda7-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ceda7-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ceda7-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ceda7-129">INPUTS</span></span>

### <span data-ttu-id="ceda7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="ceda7-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ceda7-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ceda7-131">OUTPUTS</span></span>

### <span data-ttu-id="ceda7-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span><span class="sxs-lookup"><span data-stu-id="ceda7-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="ceda7-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ceda7-133">NOTES</span></span>

## <span data-ttu-id="ceda7-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ceda7-134">RELATED LINKS</span></span>

[<span data-ttu-id="ceda7-135">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ceda7-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="ceda7-136">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ceda7-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="ceda7-137">Stop-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="ceda7-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
