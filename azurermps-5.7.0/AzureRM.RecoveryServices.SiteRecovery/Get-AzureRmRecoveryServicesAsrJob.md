---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrJob.md
ms.openlocfilehash: 233a6a7c7fd7b2bfe96ed9cc0df6a88bdb9d8747
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526657"
---
# <span data-ttu-id="e224c-101">Get-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e224c-101">Get-AzureRmRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="e224c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e224c-102">SYNOPSIS</span></span>
<span data-ttu-id="e224c-103">Pobiera szczegóły określonego zadania ASR lub listę ostatnich zadań ASR w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="e224c-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e224c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e224c-104">SYNTAX</span></span>

### <span data-ttu-id="e224c-105">ByParam (domyślny)</span><span class="sxs-lookup"><span data-stu-id="e224c-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e224c-106">ByName</span><span class="sxs-lookup"><span data-stu-id="e224c-106">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e224c-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="e224c-107">ByObject</span></span>
```
Get-AzureRmRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e224c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="e224c-108">DESCRIPTION</span></span>
<span data-ttu-id="e224c-109">Polecenie cmdlet **Get-AzureRmRecoveryServicesAsrJob** pobiera zadania odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="e224c-109">The **Get-AzureRmRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="e224c-110">Za pomocą tego polecenia cmdlet można wyświetlać zadania ASR w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="e224c-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="e224c-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e224c-111">EXAMPLES</span></span>

### <span data-ttu-id="e224c-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e224c-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzureRmRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="e224c-113">Zwraca wszystkie zadania określonego obiektu ASR (odwołanie do obiektu ASR, takiego jak replikowany element lub plan odzyskiwania) za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="e224c-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="e224c-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e224c-114">PARAMETERS</span></span>

### <span data-ttu-id="e224c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e224c-115">-DefaultProfile</span></span>
<span data-ttu-id="e224c-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e224c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>
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

### <span data-ttu-id="e224c-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="e224c-117">-EndTime</span></span>
<span data-ttu-id="e224c-118">Określa czas zakończenia zadań.</span><span class="sxs-lookup"><span data-stu-id="e224c-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="e224c-119">To polecenie cmdlet umożliwia pobieranie wszystkich zadań rozpoczętych przed określonym terminem.</span><span class="sxs-lookup"><span data-stu-id="e224c-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="e224c-120">Aby uzyskać obiekt **DateTime** dla tego parametru, użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="e224c-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="e224c-121">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="e224c-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="e224c-122">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="e224c-122">-Job</span></span>
<span data-ttu-id="e224c-123">Określa obiekt zadania ASR, dla którego mają zostać zaktualizowane szczegóły.</span><span class="sxs-lookup"><span data-stu-id="e224c-123">Specifies the ASR job object to get updated details for.</span></span>

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

### <span data-ttu-id="e224c-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e224c-124">-Name</span></span>
<span data-ttu-id="e224c-125">Określ zadanie ASR według nazwy.</span><span class="sxs-lookup"><span data-stu-id="e224c-125">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="e224c-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e224c-126">-StartTime</span></span>
<span data-ttu-id="e224c-127">Określa czas rozpoczęcia zadań.</span><span class="sxs-lookup"><span data-stu-id="e224c-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="e224c-128">To polecenie cmdlet umożliwia pobieranie wszystkich zadań uruchomionych po określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="e224c-128">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="e224c-129">-State</span><span class="sxs-lookup"><span data-stu-id="e224c-129">-State</span></span>
<span data-ttu-id="e224c-130">Określa stan zadania ASR.</span><span class="sxs-lookup"><span data-stu-id="e224c-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="e224c-131">To polecenie cmdlet umożliwia pobieranie wszystkich zadań zgodnych z określonym stanem.</span><span class="sxs-lookup"><span data-stu-id="e224c-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="e224c-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="e224c-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="e224c-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="e224c-133">NotStarted</span></span>
- <span data-ttu-id="e224c-134">W trakcie</span><span class="sxs-lookup"><span data-stu-id="e224c-134">InProgress</span></span>
- <span data-ttu-id="e224c-135">Doszło</span><span class="sxs-lookup"><span data-stu-id="e224c-135">Succeeded</span></span>
- <span data-ttu-id="e224c-136">Pozostałe</span><span class="sxs-lookup"><span data-stu-id="e224c-136">Other</span></span>
- <span data-ttu-id="e224c-137">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="e224c-137">Failed</span></span>
- <span data-ttu-id="e224c-138">Anulowania</span><span class="sxs-lookup"><span data-stu-id="e224c-138">Cancelled</span></span>
- <span data-ttu-id="e224c-139">Zawiesin</span><span class="sxs-lookup"><span data-stu-id="e224c-139">Suspended</span></span>

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

### <span data-ttu-id="e224c-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="e224c-140">-TargetObjectId</span></span>
<span data-ttu-id="e224c-141">Określa identyfikator obiektu.</span><span class="sxs-lookup"><span data-stu-id="e224c-141">Specifies the ID of the object.</span></span> <span data-ttu-id="e224c-142">Umożliwia wyszukiwanie zadań na określonym obiekcie.</span><span class="sxs-lookup"><span data-stu-id="e224c-142">Used to search for jobs on the specified object.</span></span>

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

### <span data-ttu-id="e224c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e224c-143">CommonParameters</span></span>
<span data-ttu-id="e224c-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e224c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e224c-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e224c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e224c-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e224c-146">INPUTS</span></span>

### <span data-ttu-id="e224c-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="e224c-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="e224c-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e224c-148">OUTPUTS</span></span>

### <span data-ttu-id="e224c-149">System. Collections. Generic. IEnumerable ' 1 [[Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob, Microsoft. Azure. Commands. RecoveryServices. SiteRecovery, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="e224c-149">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=4.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e224c-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e224c-150">NOTES</span></span>

## <span data-ttu-id="e224c-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e224c-151">RELATED LINKS</span></span>

[<span data-ttu-id="e224c-152">Restart-AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e224c-152">Restart-AzureRmRecoveryServicesAsrJob</span></span>](./Restart-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="e224c-153">Życiorys — AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e224c-153">Resume-AzureRmRecoveryServicesAsrJob</span></span>](./Resume-AzureRmRecoveryServicesAsrJob.md)

[<span data-ttu-id="e224c-154">Zatrzymaj — AzureRmRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="e224c-154">Stop-AzureRmRecoveryServicesAsrJob</span></span>](./Stop-AzureRmRecoveryServicesAsrJob.md)
