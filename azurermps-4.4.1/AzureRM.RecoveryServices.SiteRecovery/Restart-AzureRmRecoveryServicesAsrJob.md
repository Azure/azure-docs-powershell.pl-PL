---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Restart-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 2f219882199010b2765ebd4386691451d74a182d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718124"
---
# <span data-ttu-id="103a9-101">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="103a9-101">Restart-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="103a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="103a9-102">SYNOPSIS</span></span>
<span data-ttu-id="103a9-103">Ponowne uruchamianie zadania odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="103a9-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="103a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="103a9-104">SYNTAX</span></span>

### <span data-ttu-id="103a9-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="103a9-105">ByObject (Default)</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="103a9-106">ByName</span><span class="sxs-lookup"><span data-stu-id="103a9-106">ByName</span></span>
```
Restart-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="103a9-107">Opis</span><span class="sxs-lookup"><span data-stu-id="103a9-107">DESCRIPTION</span></span>
<span data-ttu-id="103a9-108">Polecenie cmdlet **restart-AzureRmRecoveryServicesAsrJob** powoduje ponowne uruchomienie zadania odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="103a9-108">The **Restart-AzureRmRecoveryServicesAsrJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="103a9-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="103a9-109">EXAMPLES</span></span>

### <span data-ttu-id="103a9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="103a9-110">Example 1</span></span>
```
PS C:\> $currentJob = Restart-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="103a9-111">Powoduje ponowne uruchomienie określonego zadania ASR i zwraca zaktualizowany obiekt zadania ASR zadania ASR.</span><span class="sxs-lookup"><span data-stu-id="103a9-111">Restarts the specified ASR job and returns the updated ASR job object of the ASR job.</span></span>

## <span data-ttu-id="103a9-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="103a9-112">PARAMETERS</span></span>

### <span data-ttu-id="103a9-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="103a9-113">-InputObject</span></span>
<span data-ttu-id="103a9-114">Obiekt wejściowy do polecenia cmdlet: obiekt zadania ASR odpowiadający zadaniu ASR do ponownego uruchomienia</span><span class="sxs-lookup"><span data-stu-id="103a9-114">The input object to the cmdlet: The ASR job object corresponding to the ASR job to be restarted</span></span>
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

### <span data-ttu-id="103a9-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="103a9-115">-Name</span></span>
<span data-ttu-id="103a9-116">Określ zadanie według nazwy.</span><span class="sxs-lookup"><span data-stu-id="103a9-116">Specify the job by name.</span></span>

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

### <span data-ttu-id="103a9-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="103a9-117">-Confirm</span></span>
<span data-ttu-id="103a9-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="103a9-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="103a9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="103a9-119">-WhatIf</span></span>
<span data-ttu-id="103a9-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="103a9-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="103a9-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="103a9-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="103a9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="103a9-122">CommonParameters</span></span>
<span data-ttu-id="103a9-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="103a9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="103a9-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="103a9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="103a9-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="103a9-125">INPUTS</span></span>

### <span data-ttu-id="103a9-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="103a9-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="103a9-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="103a9-127">OUTPUTS</span></span>

### <span data-ttu-id="103a9-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="103a9-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="103a9-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="103a9-129">NOTES</span></span>

## <span data-ttu-id="103a9-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="103a9-130">RELATED LINKS</span></span>

[<span data-ttu-id="103a9-131">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="103a9-131">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="103a9-132">Życiorys — AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="103a9-132">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="103a9-133">Zatrzymaj — AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="103a9-133">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
