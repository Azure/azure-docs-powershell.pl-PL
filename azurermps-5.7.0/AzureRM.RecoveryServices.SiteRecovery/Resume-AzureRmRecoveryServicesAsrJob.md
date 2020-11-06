---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/resume-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Resume-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: e6c384f56e7af9bacad40dfbc1fbf87d26dd8320
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544204"
---
# <span data-ttu-id="feee4-101">Resume-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="feee4-101">Resume-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="feee4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="feee4-102">SYNOPSIS</span></span>
<span data-ttu-id="feee4-103">Wznawia zawieszone zadanie odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="feee4-103">Resumes a suspended Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="feee4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="feee4-104">SYNTAX</span></span>

### <span data-ttu-id="feee4-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="feee4-105">ByObject (Default)</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feee4-106">ByName</span><span class="sxs-lookup"><span data-stu-id="feee4-106">ByName</span></span>
```
Resume-AzureRmRecoveryServicesAsrJob -Name <String> [-Comment <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="feee4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="feee4-107">DESCRIPTION</span></span>
<span data-ttu-id="feee4-108">Polecenie cmdlet **Resume-AzureRmRecoveryServicesAsrJob** Wznawia zawieszone zadanie odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="feee4-108">The **Resume-AzureRmRecoveryServicesAsrJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="feee4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="feee4-109">EXAMPLES</span></span>

### <span data-ttu-id="feee4-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="feee4-110">Example 1</span></span>
```
PS C:\> $currentJob = Resume-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="feee4-111">Wznowienie określonego zadania, jeśli jest ono w stanie oczekiwania lub wstrzymania i zwróci zaktualizowany obiekt zadania ASR odpowiadający temu zadaniu ASR.</span><span class="sxs-lookup"><span data-stu-id="feee4-111">Resume the specified job if it is in a waiting or suspended state and return the updated ASR job object corresponding to the ASR job.</span></span>

## <span data-ttu-id="feee4-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="feee4-112">PARAMETERS</span></span>

### <span data-ttu-id="feee4-113">-Komentarz</span><span class="sxs-lookup"><span data-stu-id="feee4-113">-Comment</span></span>
<span data-ttu-id="feee4-114">Komentarze dotyczące dziennika zadań.</span><span class="sxs-lookup"><span data-stu-id="feee4-114">Comments for the job log.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Comments

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feee4-115">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="feee4-115">-Confirm</span></span>
<span data-ttu-id="feee4-116">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="feee4-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feee4-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feee4-117">-DefaultProfile</span></span>
<span data-ttu-id="feee4-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="feee4-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feee4-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="feee4-119">-InputObject</span></span>
<span data-ttu-id="feee4-120">Obiekt wejściowy do polecenia cmdlet: obiekt zadania ASR odpowiadający zadanie, które ma zostać wznowione.</span><span class="sxs-lookup"><span data-stu-id="feee4-120">The input object to the cmdlet: The ASR Job object corresponding to the job to be resumed.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: Job

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="feee4-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="feee4-121">-Name</span></span>
<span data-ttu-id="feee4-122">Określ zadanie ASR według nazwy.</span><span class="sxs-lookup"><span data-stu-id="feee4-122">Specify the ASR job by name.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feee4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feee4-123">-WhatIf</span></span>
<span data-ttu-id="feee4-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="feee4-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="feee4-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="feee4-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="feee4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feee4-126">CommonParameters</span></span>
<span data-ttu-id="feee4-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feee4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feee4-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feee4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feee4-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="feee4-129">INPUTS</span></span>

### <span data-ttu-id="feee4-130">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="feee4-130">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="feee4-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="feee4-131">OUTPUTS</span></span>

### <span data-ttu-id="feee4-132">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="feee4-132">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="feee4-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="feee4-133">NOTES</span></span>

## <span data-ttu-id="feee4-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="feee4-134">RELATED LINKS</span></span>

[<span data-ttu-id="feee4-135">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="feee4-135">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="feee4-136">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="feee4-136">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="feee4-137">Zatrzymaj — AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="feee4-137">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
