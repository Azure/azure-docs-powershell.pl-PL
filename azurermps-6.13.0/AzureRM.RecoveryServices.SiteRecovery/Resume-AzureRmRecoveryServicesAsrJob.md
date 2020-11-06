---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/resume-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: c5efb6b9aa7d78ef5f8d50ef80c5155c7e731f11
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93552068"
---
# <span data-ttu-id="c3af3-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c3af3-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="c3af3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c3af3-102">SYNOPSIS</span></span>
<span data-ttu-id="c3af3-103">Wznawia zawieszone zadanie odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c3af3-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c3af3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c3af3-104">SYNTAX</span></span>

### <span data-ttu-id="c3af3-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c3af3-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c3af3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c3af3-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c3af3-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c3af3-107">DESCRIPTION</span></span>
<span data-ttu-id="c3af3-108">Polecenie cmdlet **Resume-AzureRmRecoveryServicesAsrJob** Wznawia zawieszone zadanie odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c3af3-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="c3af3-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c3af3-109">EXAMPLES</span></span>

### <span data-ttu-id="c3af3-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c3af3-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="c3af3-111">Wznowienie określonego zadania, jeśli jest ono w stanie oczekiwania lub wstrzymania i zwróci zaktualizowany obiekt zadania ASR odpowiadający temu zadaniu ASR.</span><span class="sxs-lookup"><span data-stu-id="c3af3-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="c3af3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c3af3-112">PARAMETERS</span></span>

### <span data-ttu-id="c3af3-113">-Komentarz</span><span class="sxs-lookup"><span data-stu-id="c3af3-113">-Comment</span></span>
<span data-ttu-id="c3af3-114">Komentarze dotyczące dziennika zadań.</span><span class="sxs-lookup"><span data-stu-id="c3af3-114">Comments for the job log.</span></span>

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

### <span data-ttu-id="c3af3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3af3-115">-DefaultProfile</span></span>
<span data-ttu-id="c3af3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c3af3-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c3af3-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c3af3-117">-InputObject</span></span>
<span data-ttu-id="c3af3-118">Obiekt wejściowy do polecenia cmdlet: obiekt zadania ASR odpowiadający zadanie, które ma zostać wznowione.</span><span class="sxs-lookup"><span data-stu-id="c3af3-118">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

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

### <span data-ttu-id="c3af3-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c3af3-119">-Name</span></span>
<span data-ttu-id="c3af3-120">Określ zadanie ASR według nazwy.</span><span class="sxs-lookup"><span data-stu-id="c3af3-120">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="c3af3-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c3af3-121">-Confirm</span></span>
<span data-ttu-id="c3af3-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3af3-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c3af3-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c3af3-123">-WhatIf</span></span>
<span data-ttu-id="c3af3-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c3af3-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c3af3-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c3af3-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c3af3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3af3-126">CommonParameters</span></span>
<span data-ttu-id="c3af3-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c3af3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3af3-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c3af3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3af3-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c3af3-129">INPUTS</span></span>

### <span data-ttu-id="c3af3-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c3af3-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c3af3-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c3af3-131">OUTPUTS</span></span>

### <span data-ttu-id="c3af3-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="c3af3-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c3af3-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c3af3-133">NOTES</span></span>

## <span data-ttu-id="c3af3-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c3af3-134">RELATED LINKS</span></span>

[<span data-ttu-id="c3af3-135">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c3af3-135">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="c3af3-136">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c3af3-136">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="c3af3-137">Zatrzymaj — AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="c3af3-137">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
