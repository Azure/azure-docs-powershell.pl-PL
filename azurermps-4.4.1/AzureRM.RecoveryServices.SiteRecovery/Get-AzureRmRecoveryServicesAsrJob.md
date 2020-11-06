---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: afef81ad904ccd5bf53f0b2a09bb10511e71fca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553143"
---
# <span data-ttu-id="b2f64-101">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="b2f64-101">Get-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="b2f64-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2f64-102">SYNOPSIS</span></span>
<span data-ttu-id="b2f64-103">Pobiera szczegóły określonego zadania ASR lub listę ostatnich zadań ASR w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="b2f64-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2f64-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2f64-104">SYNTAX</span></span>

### <span data-ttu-id="b2f64-105">ByParam (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b2f64-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [<CommonParameters>]
```

### <span data-ttu-id="b2f64-106">ByName</span><span class="sxs-lookup"><span data-stu-id="b2f64-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [<CommonParameters>]
```

### <span data-ttu-id="b2f64-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="b2f64-107">ByObject</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [<CommonParameters>]
```

## <span data-ttu-id="b2f64-108">Opis</span><span class="sxs-lookup"><span data-stu-id="b2f64-108">DESCRIPTION</span></span>
<span data-ttu-id="b2f64-109">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrJob** pobiera zadania odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="b2f64-109">The **Get-AzureRmRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="b2f64-110">Za pomocą tego polecenia cmdlet można wyświetlać zadania ASR w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="b2f64-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="b2f64-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2f64-111">EXAMPLES</span></span>

### <span data-ttu-id="b2f64-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b2f64-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="b2f64-113">Zwraca wszystkie zadania określonego obiektu ASR (odwołanie do obiektu ASR, takiego jak replikowany element lub plan odzyskiwania) za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="b2f64-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="b2f64-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2f64-114">PARAMETERS</span></span>

### <span data-ttu-id="b2f64-115">-EndTime</span><span class="sxs-lookup"><span data-stu-id="b2f64-115">-EndTime</span></span>
<span data-ttu-id="b2f64-116">Określa czas zakończenia zadań.</span><span class="sxs-lookup"><span data-stu-id="b2f64-116">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="b2f64-117">To polecenie cmdlet umożliwia pobieranie wszystkich zadań rozpoczętych przed określonym terminem.</span><span class="sxs-lookup"><span data-stu-id="b2f64-117">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="b2f64-118">Aby uzyskać obiekt **DateTime** dla tego parametru, użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="b2f64-118">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="b2f64-119">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="b2f64-119">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2f64-120">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="b2f64-120">-Job</span></span>
<span data-ttu-id="b2f64-121">Określa obiekt zadania ASR, dla którego mają zostać zaktualizowane szczegóły.</span><span class="sxs-lookup"><span data-stu-id="b2f64-121">Specifies the ASR job object to get updated details for.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b2f64-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b2f64-122">-Name</span></span>
<span data-ttu-id="b2f64-123">Określ zadanie ASR według nazwy.</span><span class="sxs-lookup"><span data-stu-id="b2f64-123">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="b2f64-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="b2f64-124">-StartTime</span></span>
<span data-ttu-id="b2f64-125">Określa czas rozpoczęcia zadań.</span><span class="sxs-lookup"><span data-stu-id="b2f64-125">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="b2f64-126">To polecenie cmdlet umożliwia pobieranie wszystkich zadań uruchomionych po określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="b2f64-126">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2f64-127">-State</span><span class="sxs-lookup"><span data-stu-id="b2f64-127">-State</span></span>
<span data-ttu-id="b2f64-128">Określa stan zadania ASR.</span><span class="sxs-lookup"><span data-stu-id="b2f64-128">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="b2f64-129">To polecenie cmdlet umożliwia pobieranie wszystkich zadań zgodnych z określonym stanem.</span><span class="sxs-lookup"><span data-stu-id="b2f64-129">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="b2f64-130">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="b2f64-130">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b2f64-131">NotStarted</span><span class="sxs-lookup"><span data-stu-id="b2f64-131">NotStarted</span></span>
- <span data-ttu-id="b2f64-132">W trakcie</span><span class="sxs-lookup"><span data-stu-id="b2f64-132">InProgress</span></span>
- <span data-ttu-id="b2f64-133">Doszło</span><span class="sxs-lookup"><span data-stu-id="b2f64-133">Succeeded</span></span>
- <span data-ttu-id="b2f64-134">Pozostałe</span><span class="sxs-lookup"><span data-stu-id="b2f64-134">Other</span></span>
- <span data-ttu-id="b2f64-135">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="b2f64-135">Failed</span></span>
- <span data-ttu-id="b2f64-136">Anulowania</span><span class="sxs-lookup"><span data-stu-id="b2f64-136">Cancelled</span></span>
- <span data-ttu-id="b2f64-137">Zawiesin</span><span class="sxs-lookup"><span data-stu-id="b2f64-137">Suspended</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2f64-138">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="b2f64-138">-TargetObjectId</span></span>
<span data-ttu-id="b2f64-139">Określa identyfikator obiektu.</span><span class="sxs-lookup"><span data-stu-id="b2f64-139">Specifies the ID of the object.</span></span> <span data-ttu-id="b2f64-140">Umożliwia wyszukiwanie zadań na określonym obiekcie.</span><span class="sxs-lookup"><span data-stu-id="b2f64-140">Used to search for jobs on the specified object.</span></span>

```yaml
Type: String
Parameter Sets: ByParam
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b2f64-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2f64-141">CommonParameters</span></span>
<span data-ttu-id="b2f64-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2f64-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2f64-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2f64-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2f64-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2f64-144">INPUTS</span></span>

### <span data-ttu-id="b2f64-145">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="b2f64-145">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="b2f64-146">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2f64-146">OUTPUTS</span></span>

### <span data-ttu-id="b2f64-147">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="b2f64-147">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="b2f64-148">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2f64-148">NOTES</span></span>

## <span data-ttu-id="b2f64-149">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2f64-149">RELATED LINKS</span></span>

[<span data-ttu-id="b2f64-150">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="b2f64-150">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="b2f64-151">Życiorys — AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="b2f64-151">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="b2f64-152">Zatrzymaj — AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="b2f64-152">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
