---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrJob.md
ms.openlocfilehash: 85479392a34e81395d3f00e3ef3891772a2dcbec
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872764"
---
# <span data-ttu-id="19079-101">Get-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="19079-101">Get-AzRecoveryServicesAsrJob</span></span>

## <span data-ttu-id="19079-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="19079-102">SYNOPSIS</span></span>
<span data-ttu-id="19079-103">Pobiera szczegóły określonego zadania ASR lub listę ostatnich zadań ASR w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="19079-103">Gets the details of the specified ASR job or the list of recent ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="19079-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="19079-104">SYNTAX</span></span>

### <span data-ttu-id="19079-105">ByParam (domyślny)</span><span class="sxs-lookup"><span data-stu-id="19079-105">ByParam (Default)</span></span>
```
Get-AzRecoveryServicesAsrJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19079-106">ByName</span><span class="sxs-lookup"><span data-stu-id="19079-106">ByName</span></span>
```
Get-AzRecoveryServicesAsrJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="19079-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="19079-107">ByObject</span></span>
```
Get-AzRecoveryServicesAsrJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19079-108">Opis</span><span class="sxs-lookup"><span data-stu-id="19079-108">DESCRIPTION</span></span>
<span data-ttu-id="19079-109">Polecenie cmdlet **Get-AzRecoveryServicesAsrJob** pobiera zadania odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="19079-109">The **Get-AzRecoveryServicesAsrJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="19079-110">Za pomocą tego polecenia cmdlet można wyświetlać zadania ASR w magazynie usług Recovery Services.</span><span class="sxs-lookup"><span data-stu-id="19079-110">You can use this cmdlet to view the ASR jobs in the Recovery Services vault.</span></span>

## <span data-ttu-id="19079-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="19079-111">EXAMPLES</span></span>

### <span data-ttu-id="19079-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="19079-112">Example 1</span></span>
```
PS C:\> $jobs = Get-AzRecoveryServicesAsrJob -TargetObjectId $ASRObjectId
```

<span data-ttu-id="19079-113">Zwraca wszystkie zadania określonego obiektu ASR (odwołanie do obiektu ASR, takiego jak replikowany element lub plan odzyskiwania) za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="19079-113">Returns all the jobs on a particular ASR object(reference the ASR object such as replicated item or recovery plan by its ID.)</span></span> 

## <span data-ttu-id="19079-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="19079-114">PARAMETERS</span></span>

### <span data-ttu-id="19079-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19079-115">-DefaultProfile</span></span>
<span data-ttu-id="19079-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="19079-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="19079-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="19079-117">-EndTime</span></span>
<span data-ttu-id="19079-118">Określa czas zakończenia zadań.</span><span class="sxs-lookup"><span data-stu-id="19079-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="19079-119">To polecenie cmdlet umożliwia pobieranie wszystkich zadań rozpoczętych przed określonym terminem.</span><span class="sxs-lookup"><span data-stu-id="19079-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="19079-120">Aby uzyskać obiekt **DateTime** dla tego parametru, użyj polecenia cmdlet Get-Date.</span><span class="sxs-lookup"><span data-stu-id="19079-120">To obtain a **DateTime** object for this parameter, use the Get-Date cmdlet.</span></span>
<span data-ttu-id="19079-121">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="19079-121">For more information, type `Get-Help Get-Date`.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19079-122">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="19079-122">-Job</span></span>
<span data-ttu-id="19079-123">Określa obiekt zadania ASR, dla którego mają zostać zaktualizowane szczegóły.</span><span class="sxs-lookup"><span data-stu-id="19079-123">Specifies the ASR job object to get updated details for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="19079-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="19079-124">-Name</span></span>
<span data-ttu-id="19079-125">Określ zadanie ASR według nazwy.</span><span class="sxs-lookup"><span data-stu-id="19079-125">Specify the ASR job by name.</span></span>

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

### <span data-ttu-id="19079-126">-StartTime</span><span class="sxs-lookup"><span data-stu-id="19079-126">-StartTime</span></span>
<span data-ttu-id="19079-127">Określa czas rozpoczęcia zadań.</span><span class="sxs-lookup"><span data-stu-id="19079-127">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="19079-128">To polecenie cmdlet umożliwia pobieranie wszystkich zadań uruchomionych po określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="19079-128">This cmdlet gets all jobs that started after the specified time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19079-129">-State</span><span class="sxs-lookup"><span data-stu-id="19079-129">-State</span></span>
<span data-ttu-id="19079-130">Określa stan zadania ASR.</span><span class="sxs-lookup"><span data-stu-id="19079-130">Specifies the state for a ASR job.</span></span>
<span data-ttu-id="19079-131">To polecenie cmdlet umożliwia pobieranie wszystkich zadań zgodnych z określonym stanem.</span><span class="sxs-lookup"><span data-stu-id="19079-131">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="19079-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="19079-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="19079-133">NotStarted</span><span class="sxs-lookup"><span data-stu-id="19079-133">NotStarted</span></span>
- <span data-ttu-id="19079-134">W trakcie</span><span class="sxs-lookup"><span data-stu-id="19079-134">InProgress</span></span>
- <span data-ttu-id="19079-135">Doszło</span><span class="sxs-lookup"><span data-stu-id="19079-135">Succeeded</span></span>
- <span data-ttu-id="19079-136">Pozostałe</span><span class="sxs-lookup"><span data-stu-id="19079-136">Other</span></span>
- <span data-ttu-id="19079-137">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="19079-137">Failed</span></span>
- <span data-ttu-id="19079-138">Anulowania</span><span class="sxs-lookup"><span data-stu-id="19079-138">Cancelled</span></span>
- <span data-ttu-id="19079-139">Zawiesin</span><span class="sxs-lookup"><span data-stu-id="19079-139">Suspended</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Other, Failed, Cancelled, Suspended

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19079-140">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="19079-140">-TargetObjectId</span></span>
<span data-ttu-id="19079-141">Określa identyfikator obiektu.</span><span class="sxs-lookup"><span data-stu-id="19079-141">Specifies the ID of the object.</span></span> <span data-ttu-id="19079-142">Umożliwia wyszukiwanie zadań na określonym obiekcie.</span><span class="sxs-lookup"><span data-stu-id="19079-142">Used to search for jobs on the specified object.</span></span>

```yaml
Type: System.String
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19079-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19079-143">CommonParameters</span></span>
<span data-ttu-id="19079-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="19079-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19079-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19079-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19079-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="19079-146">INPUTS</span></span>

### <span data-ttu-id="19079-147">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="19079-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="19079-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="19079-148">OUTPUTS</span></span>

### <span data-ttu-id="19079-149">Microsoft. Azure. Commands. RecoveryServices. SiteRecovery. ASRJob</span><span class="sxs-lookup"><span data-stu-id="19079-149">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="19079-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="19079-150">NOTES</span></span>

## <span data-ttu-id="19079-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="19079-151">RELATED LINKS</span></span>

[<span data-ttu-id="19079-152">Restart-AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="19079-152">Restart-AzRecoveryServicesAsrJob</span></span>](./Restart-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="19079-153">Życiorys — AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="19079-153">Resume-AzRecoveryServicesAsrJob</span></span>](./Resume-AzRecoveryServicesAsrJob.md)

[<span data-ttu-id="19079-154">Zatrzymaj — AzRecoveryServicesAsrJob</span><span class="sxs-lookup"><span data-stu-id="19079-154">Stop-AzRecoveryServicesAsrJob</span></span>](./Stop-AzRecoveryServicesAsrJob.md)
