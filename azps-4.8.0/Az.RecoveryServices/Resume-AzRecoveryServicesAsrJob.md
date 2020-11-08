---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/resume-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Resume-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 6af467e5fd90a7d3028d67297b62f517f512b1b1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062153"
---
# <span data-ttu-id="af09a-101">Resume-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="af09a-101">Resume-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="af09a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="af09a-102">SYNOPSIS</span></span>
<span data-ttu-id="af09a-103">Wznawia zawieszone zadanie odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="af09a-103">Resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="af09a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="af09a-104">SYNTAX</span></span>

### <span data-ttu-id="af09a-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="af09a-105">ByObject (Default)</span></span>
```
Resume-AzRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="af09a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="af09a-106">ByName</span></span>
```
Resume-AzRecoveryServicesAsrJob -Name <String> [-Comment <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af09a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="af09a-107">DESCRIPTION</span></span>
<span data-ttu-id="af09a-108">Polecenie cmdlet **Resume-AzRecoveryServicesAsrJob** Wznawia zawieszone zadanie odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="af09a-108">The **Resume-AzRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="af09a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="af09a-109">EXAMPLES</span></span>

### <span data-ttu-id="af09a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="af09a-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="af09a-111">Wznowienie określonego zadania, jeśli jest ono w stanie oczekiwania lub wstrzymania i zwróci zaktualizowany obiekt zadania ASR odpowiadający temu zadaniu ASR.</span><span class="sxs-lookup"><span data-stu-id="af09a-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="af09a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="af09a-112">PARAMETERS</span></span>

### <span data-ttu-id="af09a-113">-Komentarz</span><span class="sxs-lookup"><span data-stu-id="af09a-113">-Comment</span></span>
<span data-ttu-id="af09a-114">Komentarze dotyczące dziennika zadań.</span><span class="sxs-lookup"><span data-stu-id="af09a-114">Comments for the job log.</span></span>

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

### <span data-ttu-id="af09a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af09a-115">-DefaultProfile</span></span>
<span data-ttu-id="af09a-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="af09a-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="af09a-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="af09a-117">-InputObject</span></span>
<span data-ttu-id="af09a-118">Obiekt wejściowy do polecenia cmdlet: obiekt zadania ASR odpowiadający zadanie, które ma zostać wznowione.</span><span class="sxs-lookup"><span data-stu-id="af09a-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="af09a-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="af09a-119">-Name</span></span>
<span data-ttu-id="af09a-120">Określ zadanie ASR według nazwy.</span><span class="sxs-lookup"><span data-stu-id="af09a-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="af09a-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="af09a-121">-Confirm</span></span>
<span data-ttu-id="af09a-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af09a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af09a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af09a-123">-WhatIf</span></span>
<span data-ttu-id="af09a-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="af09a-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="af09a-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="af09a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af09a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af09a-126">CommonParameters</span></span>
<span data-ttu-id="af09a-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="af09a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af09a-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="af09a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af09a-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="af09a-129">INPUTS</span></span>

### <span data-ttu-id="af09a-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="af09a-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="af09a-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="af09a-131">OUTPUTS</span></span>

### <span data-ttu-id="af09a-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="af09a-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="af09a-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="af09a-133">NOTES</span></span>

## <span data-ttu-id="af09a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="af09a-134">RELATED LINKS</span></span>

[<span data-ttu-id="af09a-135">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="af09a-135">Get-AzRecoveryServicesAsrJob</span></span>](./Get-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="af09a-136">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="af09a-136">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="af09a-137">Zatrzymaj — AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="af09a-137">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
