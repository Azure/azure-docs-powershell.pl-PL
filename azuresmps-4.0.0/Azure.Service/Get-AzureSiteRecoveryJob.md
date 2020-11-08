---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2957C0DE-3A2F-4337-A778-2B95654972E7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d0b272732cf6c1e1b2025c8e7f48b58e4807cdb3
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054561"
---
# <span data-ttu-id="63fe2-101">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="63fe2-101">Get-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="63fe2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="63fe2-102">SYNOPSIS</span></span>
<span data-ttu-id="63fe2-103">Pobiera informacje o operacji dla magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="63fe2-103">Gets the operation information for a Site Recovery vault.</span></span>

## <span data-ttu-id="63fe2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="63fe2-104">SYNTAX</span></span>

### <span data-ttu-id="63fe2-105">ByParam (domyślny)</span><span class="sxs-lookup"><span data-stu-id="63fe2-105">ByParam (Default)</span></span>
```
Get-AzureSiteRecoveryJob [-StartTime <DateTime>] [-EndTime <DateTime>] [-TargetObjectId <String>]
 [-State <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="63fe2-106">ById</span><span class="sxs-lookup"><span data-stu-id="63fe2-106">ById</span></span>
```
Get-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="63fe2-107">ByObject</span><span class="sxs-lookup"><span data-stu-id="63fe2-107">ByObject</span></span>
```
Get-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="63fe2-108">Opis</span><span class="sxs-lookup"><span data-stu-id="63fe2-108">DESCRIPTION</span></span>
<span data-ttu-id="63fe2-109">Polecenie cmdlet **Get-AzureSiteRecoveryJob** pobiera zadania odzyskiwania witryny Azure.</span><span class="sxs-lookup"><span data-stu-id="63fe2-109">The **Get-AzureSiteRecoveryJob** cmdlet gets Azure Site Recovery jobs.</span></span>
<span data-ttu-id="63fe2-110">Za pomocą tego polecenia cmdlet można wyświetlać informacje o operacjach dotyczących bieżącego magazynu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="63fe2-110">You can use this cmdlet to view the operation information for the current Site Recovery vault.</span></span>

## <span data-ttu-id="63fe2-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="63fe2-111">EXAMPLES</span></span>

### <span data-ttu-id="63fe2-112">Przykład 1. Pobieranie zadania przez określenie identyfikatora</span><span class="sxs-lookup"><span data-stu-id="63fe2-112">Example 1: Get a job by specifying an ID</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -Id "033785cc-9f72-4f07-8e78-e4d1e942a7ae" 
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="63fe2-113">To polecenie pobiera zadanie odzyskiwania witryny Azure z określonym IDENTYFIKATORem.</span><span class="sxs-lookup"><span data-stu-id="63fe2-113">This command gets the  Azure Site Recovery job that has the specified ID.</span></span>

### <span data-ttu-id="63fe2-114">Przykład 2: Pobiera zadanie na podstawie czasu</span><span class="sxs-lookup"><span data-stu-id="63fe2-114">Example 2: Gets a job based on time</span></span>
```
PS C:\> Get-AzureSiteRecoveryJob -StartTime "20-02-2015 01:00:00" -EndTime "21-02-2015 01:00:00"
Name             : SaveRecoveryPlan
ID               : 033785cc-9f72-4f07-8e78-e4d1e942a7ae
ClientRequestId  : d604206b-32e1-4d5b-9a23-32b118d14a1e-2015-02-20 07:20:42Z-P
State            : Succeeded
StateDescription : Completed
StartTime        : 20-02-2015 07:20:45 +05:30
EndTime          : 20-02-2015 07:20:46 +05:30
TargetObjectId   : cfb445bf-fd14-4b5d-b9ac-5154e1415ef2
TargetObjectType : RecoveryPlan
TargetObjectName : RP
AllowedActions   : {Cancel}
Tasks            : {Save a recovery plan task}
Errors           : {}
```

<span data-ttu-id="63fe2-115">To polecenie pobiera zadania odzyskiwania witryny przypadające pomiędzy określoną godziną rozpoczęcia a godziną zakończenia.</span><span class="sxs-lookup"><span data-stu-id="63fe2-115">This command gets Site Recovery jobs that fall between the specified start time and end time.</span></span>

## <span data-ttu-id="63fe2-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="63fe2-116">PARAMETERS</span></span>

### <span data-ttu-id="63fe2-117">-EndTime</span><span class="sxs-lookup"><span data-stu-id="63fe2-117">-EndTime</span></span>
<span data-ttu-id="63fe2-118">Określa czas zakończenia zadań.</span><span class="sxs-lookup"><span data-stu-id="63fe2-118">Specifies the end time for the jobs.</span></span>
<span data-ttu-id="63fe2-119">To polecenie cmdlet umożliwia pobieranie wszystkich zadań rozpoczętych przed określonym terminem.</span><span class="sxs-lookup"><span data-stu-id="63fe2-119">This cmdlet gets all jobs that started before the specified time.</span></span>
<span data-ttu-id="63fe2-120">Aby uzyskać obiekt **DateTime** , należy użyć polecenia cmdlet **Get-Date** .</span><span class="sxs-lookup"><span data-stu-id="63fe2-120">To obtain a **DateTime** object, use the **Get-Date** cmdlet.</span></span>
<span data-ttu-id="63fe2-121">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Date` .</span><span class="sxs-lookup"><span data-stu-id="63fe2-121">For more information, type `Get-Help Get-Date`.</span></span>

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

### <span data-ttu-id="63fe2-122">-ID</span><span class="sxs-lookup"><span data-stu-id="63fe2-122">-Id</span></span>
<span data-ttu-id="63fe2-123">Określa identyfikator zadania do pobrania.</span><span class="sxs-lookup"><span data-stu-id="63fe2-123">Specifies the ID of a job to get.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63fe2-124">— Zadanie</span><span class="sxs-lookup"><span data-stu-id="63fe2-124">-Job</span></span>
<span data-ttu-id="63fe2-125">Określa zadanie do pobrania.</span><span class="sxs-lookup"><span data-stu-id="63fe2-125">Specifies a job to get.</span></span>

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

### <span data-ttu-id="63fe2-126">-Profile</span><span class="sxs-lookup"><span data-stu-id="63fe2-126">-Profile</span></span>
<span data-ttu-id="63fe2-127">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="63fe2-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="63fe2-128">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="63fe2-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63fe2-129">-StartTime</span><span class="sxs-lookup"><span data-stu-id="63fe2-129">-StartTime</span></span>
<span data-ttu-id="63fe2-130">Określa czas rozpoczęcia zadań.</span><span class="sxs-lookup"><span data-stu-id="63fe2-130">Specifies the start time for the jobs.</span></span>
<span data-ttu-id="63fe2-131">To polecenie cmdlet umożliwia pobieranie wszystkich zadań uruchomionych po określonym czasie.</span><span class="sxs-lookup"><span data-stu-id="63fe2-131">This cmdlet gets all jobs that started after the specified time.</span></span>

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

### <span data-ttu-id="63fe2-132">-State</span><span class="sxs-lookup"><span data-stu-id="63fe2-132">-State</span></span>
<span data-ttu-id="63fe2-133">Określa stan wejścia zadania odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="63fe2-133">Specifies the input state for a Site Recovery job.</span></span>
<span data-ttu-id="63fe2-134">To polecenie cmdlet umożliwia pobieranie wszystkich zadań zgodnych z określonym stanem.</span><span class="sxs-lookup"><span data-stu-id="63fe2-134">This cmdlet gets all jobs that match the specified state.</span></span>
<span data-ttu-id="63fe2-135">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="63fe2-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="63fe2-136">NotStarted</span><span class="sxs-lookup"><span data-stu-id="63fe2-136">NotStarted</span></span>
- <span data-ttu-id="63fe2-137">W trakcie</span><span class="sxs-lookup"><span data-stu-id="63fe2-137">InProgress</span></span>
- <span data-ttu-id="63fe2-138">Doszło</span><span class="sxs-lookup"><span data-stu-id="63fe2-138">Succeeded</span></span>
- <span data-ttu-id="63fe2-139">Pozostałe</span><span class="sxs-lookup"><span data-stu-id="63fe2-139">Other</span></span>
- <span data-ttu-id="63fe2-140">Nie powiodło się</span><span class="sxs-lookup"><span data-stu-id="63fe2-140">Failed</span></span>
- <span data-ttu-id="63fe2-141">Anulowania</span><span class="sxs-lookup"><span data-stu-id="63fe2-141">Cancelled</span></span>
- <span data-ttu-id="63fe2-142">Zawiesin</span><span class="sxs-lookup"><span data-stu-id="63fe2-142">Suspended</span></span>

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

### <span data-ttu-id="63fe2-143">-TargetObjectId</span><span class="sxs-lookup"><span data-stu-id="63fe2-143">-TargetObjectId</span></span>
<span data-ttu-id="63fe2-144">Określa identyfikator obiektu wskazywanego przez zadanie.</span><span class="sxs-lookup"><span data-stu-id="63fe2-144">Specifies the ID of the object targeted by the job.</span></span>

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

### <span data-ttu-id="63fe2-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63fe2-145">CommonParameters</span></span>
<span data-ttu-id="63fe2-146">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="63fe2-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63fe2-147">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63fe2-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63fe2-148">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="63fe2-148">INPUTS</span></span>

## <span data-ttu-id="63fe2-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="63fe2-149">OUTPUTS</span></span>

## <span data-ttu-id="63fe2-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="63fe2-150">NOTES</span></span>

## <span data-ttu-id="63fe2-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="63fe2-151">RELATED LINKS</span></span>

[<span data-ttu-id="63fe2-152">Polecenia cmdlet usług Azure Site Recovery</span><span class="sxs-lookup"><span data-stu-id="63fe2-152">Azure Site Recovery Services Cmdlets</span></span>](./Azure.SiteRecoveryServices.md)

[<span data-ttu-id="63fe2-153">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="63fe2-153">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="63fe2-154">Życiorys — AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="63fe2-154">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="63fe2-155">Zatrzymaj — AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="63fe2-155">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


