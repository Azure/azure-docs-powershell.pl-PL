---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 2575F5C4-A276-49CE-AB0C-726F359DA6F9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7f71138e47c851097fe36ca294784fc571b6369f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054717"
---
# <span data-ttu-id="5cd79-101">Start-AzureSiteRecoveryPlannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="5cd79-101">Start-AzureSiteRecoveryPlannedFailoverJob</span></span>

## <span data-ttu-id="5cd79-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5cd79-102">SYNOPSIS</span></span>
<span data-ttu-id="5cd79-103">Rozpoczyna operację planowanej pracy awaryjnej odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="5cd79-103">Starts a Site Recovery planned failover operation.</span></span>

## <span data-ttu-id="5cd79-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5cd79-104">SYNTAX</span></span>

### <span data-ttu-id="5cd79-105">ByRPId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5cd79-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RPId <String> -Direction <String> [-WaitForCompletion]
 [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5cd79-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="5cd79-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5cd79-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="5cd79-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="5cd79-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="5cd79-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryPlannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-WaitForCompletion] [-Optimize <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5cd79-109">Opis</span><span class="sxs-lookup"><span data-stu-id="5cd79-109">DESCRIPTION</span></span>
<span data-ttu-id="5cd79-110">Polecenie cmdlet **Start-AzureSiteRecoveryPlannedFailoverJob** rozpoczyna planowaną pracę w trybie failover dla jednostki ochrony usługi Azure Site Recovery lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="5cd79-110">The **Start-AzureSiteRecoveryPlannedFailoverJob** cmdlet starts a planned failover for an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="5cd79-111">Możesz sprawdzić, czy zadanie powiodło się przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryJob** .</span><span class="sxs-lookup"><span data-stu-id="5cd79-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="5cd79-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5cd79-112">EXAMPLES</span></span>

### <span data-ttu-id="5cd79-113">Przykład 1. uruchomienie planowanego zadania w trybie failover</span><span class="sxs-lookup"><span data-stu-id="5cd79-113">Example 1: Start a planned failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryPlannedFailoverJob -Direction PrimaryToRecovery -ProtectionEntity $Protected -Optimize ForDowntime
ID               : c38eecdc-731c-405b-a61c-08db99aae2fe
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : NotStarted
StateDescription : NotStarted
StartTime        : 
EndTime          : 
AllowedActions   : {}
Name             : 
Tasks            : {}
Errors           : {}
```

<span data-ttu-id="5cd79-114">Pierwsze polecenie pobiera wszystkie chronione kontenery w bieżącym magazynie usługi Azure Site Recovery, korzystając z polecenia cmdlet **Get-AzureSiteRecoveryProtectionContainer** , a następnie zapisuje wyniki w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="5cd79-114">The first command gets all protected containers in the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>
<span data-ttu-id="5cd79-115">W tym przykładzie istnieje jeden kontener.</span><span class="sxs-lookup"><span data-stu-id="5cd79-115">In this example, there is a single container.</span></span>

<span data-ttu-id="5cd79-116">Drugie polecenie pobiera chronione maszyny wirtualne należące do kontenera przechowywanego w $Container przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="5cd79-116">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="5cd79-117">Polecenie zapisuje wyniki w zmiennej $Protected.</span><span class="sxs-lookup"><span data-stu-id="5cd79-117">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="5cd79-118">Ostatnie polecenie uruchamia zadanie przejęcia awaryjnego w kierunku PrimaryToRecovery dla chronionych maszyn wirtualnych przechowywanych w $Protected.</span><span class="sxs-lookup"><span data-stu-id="5cd79-118">The final command starts the failover job in the direction PrimaryToRecovery for the protected virtual machines stored in $Protected.</span></span>

## <span data-ttu-id="5cd79-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5cd79-119">PARAMETERS</span></span>

### <span data-ttu-id="5cd79-120">-Direction</span><span class="sxs-lookup"><span data-stu-id="5cd79-120">-Direction</span></span>
<span data-ttu-id="5cd79-121">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="5cd79-121">Specifies the direction of the failover.</span></span>
<span data-ttu-id="5cd79-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5cd79-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5cd79-123">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="5cd79-123">PrimaryToRecovery</span></span>
- <span data-ttu-id="5cd79-124">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="5cd79-124">RecoveryToPrimary</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cd79-125">— Optymalizuj</span><span class="sxs-lookup"><span data-stu-id="5cd79-125">-Optimize</span></span>
<span data-ttu-id="5cd79-126">Określa, do czego należy zoptymalizować.</span><span class="sxs-lookup"><span data-stu-id="5cd79-126">Specifies what to optimize for.</span></span>
<span data-ttu-id="5cd79-127">Ten parametr dotyczy trybu failover z witryny platformy Azure w witrynie lokalnej, która wymaga znacznej synchronizacji danych.</span><span class="sxs-lookup"><span data-stu-id="5cd79-127">This parameter applies for failover from an Azure site to an on-premise site which requires a significant data synchronization.</span></span>
<span data-ttu-id="5cd79-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="5cd79-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5cd79-129">ForDowntime</span><span class="sxs-lookup"><span data-stu-id="5cd79-129">ForDowntime</span></span>
- <span data-ttu-id="5cd79-130">ForSynchronization</span><span class="sxs-lookup"><span data-stu-id="5cd79-130">ForSynchronization</span></span>

<span data-ttu-id="5cd79-131">Gdy jest określony **ForDowntime** , oznacza to, że dane są synchronizowane przed przejściem w tryb pracy awaryjnej w celu zminimalizowania przestojów.</span><span class="sxs-lookup"><span data-stu-id="5cd79-131">When **ForDowntime** is specified, this indicates that data is synchronized before failover to minimize downtime.</span></span>
<span data-ttu-id="5cd79-132">Synchronizacja jest przeprowadzana bez zamykania maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5cd79-132">Synchronization is performed without shutting down the virtual machine.</span></span>
<span data-ttu-id="5cd79-133">Po zakończeniu synchronizacji zadanie zostaje zawieszone.</span><span class="sxs-lookup"><span data-stu-id="5cd79-133">After synchronization is complete, the job is suspended.</span></span>
<span data-ttu-id="5cd79-134">Wznów zadanie, aby wykonać dodatkową operację synchronizacji, która zamyka maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="5cd79-134">Resume the job to do an additional synchronization operation that shuts down the virtual machine.</span></span>

<span data-ttu-id="5cd79-135">Gdy jest określony **ForSynchronization** , oznacza to, że dane są synchronizowane podczas pracy awaryjnej tylko wtedy, gdy synchronizacja danych jest zminimalizowana.</span><span class="sxs-lookup"><span data-stu-id="5cd79-135">When **ForSynchronization** is specified, this indicates that data is synchronized during failover only so data synchronization is minimized.</span></span>
<span data-ttu-id="5cd79-136">Ponieważ to ustawienie jest włączone, maszyna wirtualna jest natychmiast zamykana.</span><span class="sxs-lookup"><span data-stu-id="5cd79-136">Because this setting is enabled, the virtual machine is shut down immediately.</span></span>
<span data-ttu-id="5cd79-137">Synchronizacja rozpoczyna się po zamknięciu, aby ukończyć operację przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="5cd79-137">Synchronization starts after shutdown to complete the failover operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cd79-138">-Profile</span><span class="sxs-lookup"><span data-stu-id="5cd79-138">-Profile</span></span>
<span data-ttu-id="5cd79-139">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5cd79-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5cd79-140">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="5cd79-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5cd79-141">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="5cd79-141">-ProtectionContainerId</span></span>
<span data-ttu-id="5cd79-142">Określa identyfikator chronionego kontenera, dla którego ma zostać uruchomione zadanie.</span><span class="sxs-lookup"><span data-stu-id="5cd79-142">Specifies the ID of the protected container for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cd79-143">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5cd79-143">-ProtectionEntity</span></span>
<span data-ttu-id="5cd79-144">Określa obiekt jednostki ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="5cd79-144">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd79-145">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="5cd79-145">-ProtectionEntityId</span></span>
<span data-ttu-id="5cd79-146">Określa obiekt **ASRProtectionEntity** , dla którego ma zostać uruchomione zadanie.</span><span class="sxs-lookup"><span data-stu-id="5cd79-146">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="5cd79-147">Aby uzyskać obiekt **ASRProtectionEntity** , użyj polecenia cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="5cd79-147">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cd79-148">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="5cd79-148">-RecoveryPlan</span></span>
<span data-ttu-id="5cd79-149">Określa obiekt planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="5cd79-149">Specifies a recovery plan object.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5cd79-150">-RPId</span><span class="sxs-lookup"><span data-stu-id="5cd79-150">-RPId</span></span>
<span data-ttu-id="5cd79-151">Określa identyfikator planu odzyskiwania, dla którego ma zostać uruchomione zadanie.</span><span class="sxs-lookup"><span data-stu-id="5cd79-151">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cd79-152">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="5cd79-152">-WaitForCompletion</span></span>
<span data-ttu-id="5cd79-153">Wskazuje, że polecenie cmdlet oczekuje na zakończenie operacji przed zwróceniem sterowania do konsoli programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="5cd79-153">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5cd79-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5cd79-154">CommonParameters</span></span>
<span data-ttu-id="5cd79-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5cd79-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5cd79-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5cd79-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5cd79-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5cd79-157">INPUTS</span></span>

## <span data-ttu-id="5cd79-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5cd79-158">OUTPUTS</span></span>

## <span data-ttu-id="5cd79-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5cd79-159">NOTES</span></span>

## <span data-ttu-id="5cd79-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5cd79-160">RELATED LINKS</span></span>

[<span data-ttu-id="5cd79-161">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="5cd79-161">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="5cd79-162">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="5cd79-162">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


