---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Stop-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: e639e6fc42e440b5088a34ee29e21d324ed7d235
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718120"
---
# <span data-ttu-id="9169a-101">Stop-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9169a-101">Stop-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="9169a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9169a-102">SYNOPSIS</span></span>
<span data-ttu-id="9169a-103">Zatrzymuje zadanie odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="9169a-103">Stops an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9169a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9169a-104">SYNTAX</span></span>

### <span data-ttu-id="9169a-105">ByObject (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9169a-105">ByObject (Default)</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -InputObject <ASRJob> [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9169a-106">ByName</span><span class="sxs-lookup"><span data-stu-id="9169a-106">ByName</span></span>
```
Stop-AzureRmRecoveryServicesAsrJob -Name <String> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9169a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9169a-107">DESCRIPTION</span></span>
<span data-ttu-id="9169a-108">Polecenie cmdlet **stop-AzureRmRecoveryServicesAsrJob** zatrzymuje określone zadanie odzyskiwania witryny platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9169a-108">The **Stop-AzureRmRecoveryServicesAsrJob** cmdlet stops the specified Azure Site Recovery job.</span></span>

## <span data-ttu-id="9169a-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9169a-109">EXAMPLES</span></span>

### <span data-ttu-id="9169a-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9169a-110">Example 1</span></span>
```
PS C:\> $currentJob = Stop-AzureRmRecoveryServicesAsrJob -Job $Job
```

<span data-ttu-id="9169a-111">Próbuje zatrzymać określone zadanie i zwraca zaktualizowany obiekt zadania ASR.</span><span class="sxs-lookup"><span data-stu-id="9169a-111">Attempts to stop the specified job and returns an updated ASR job object.</span></span>

## <span data-ttu-id="9169a-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9169a-112">PARAMETERS</span></span>

### <span data-ttu-id="9169a-113">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9169a-113">-InputObject</span></span>
<span data-ttu-id="9169a-114">Obiekt wejściowy: Określ obiekt zadania ASR odpowiadający zadaniu funkcji ASR, który ma zostać zatrzymany</span><span class="sxs-lookup"><span data-stu-id="9169a-114">Input Object: Specify the ASR job object corresponding to the ASR job to be stopped</span></span>

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

### <span data-ttu-id="9169a-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9169a-115">-Name</span></span>
<span data-ttu-id="9169a-116">Określ zadanie ASR, które ma zostać zatrzymane przez nazwę zadania ASR.</span><span class="sxs-lookup"><span data-stu-id="9169a-116">Specify the ASR Job to be stopped by the ASR job name.</span></span>

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

### <span data-ttu-id="9169a-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9169a-117">-Confirm</span></span>
<span data-ttu-id="9169a-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9169a-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9169a-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9169a-119">-WhatIf</span></span>
<span data-ttu-id="9169a-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9169a-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9169a-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9169a-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9169a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9169a-122">CommonParameters</span></span>
<span data-ttu-id="9169a-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9169a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9169a-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9169a-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9169a-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9169a-125">INPUTS</span></span>

### <span data-ttu-id="9169a-126">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9169a-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9169a-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9169a-127">OUTPUTS</span></span>

### <span data-ttu-id="9169a-128">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="9169a-128">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="9169a-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9169a-129">NOTES</span></span>

## <span data-ttu-id="9169a-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9169a-130">RELATED LINKS</span></span>

[<span data-ttu-id="9169a-131">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9169a-131">Get-AzureRmRecoveryServicesAsrJob</span></span>](./Get-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="9169a-132">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9169a-132">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="9169a-133">Życiorys — AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="9169a-133">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)
