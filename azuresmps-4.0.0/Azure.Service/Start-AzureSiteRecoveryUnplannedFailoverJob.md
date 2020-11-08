---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AC73119B-BB76-425B-AA44-44502028ECC4
online version: ''
schema: 2.0.0
ms.openlocfilehash: a74a02f219b5bb64957ab919168cb79ccf681869
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054772"
---
# <span data-ttu-id="7c321-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="7c321-101">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>

## <span data-ttu-id="7c321-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7c321-102">SYNOPSIS</span></span>
<span data-ttu-id="7c321-103">Rozpoczyna nieplanowaną pracę awaryjną dla jednostki ochrony odzyskiwania witryny lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="7c321-103">Starts the unplanned failover for a Site Recovery protection entity or recovery plan.</span></span>

## <span data-ttu-id="7c321-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7c321-104">SYNTAX</span></span>

### <span data-ttu-id="7c321-105">ByRPId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7c321-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RPId <String> -Direction <String> [-PrimaryAction <Boolean>]
 [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7c321-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="7c321-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 -Direction <String> [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="7c321-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="7c321-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -RecoveryPlan <ASRRecoveryPlan> -Direction <String>
 [-PrimaryAction <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="7c321-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="7c321-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity <ASRProtectionEntity> -Direction <String>
 [-PerformSourceSiteOperations <Boolean>] [-PerformSourceSideActions] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7c321-109">Opis</span><span class="sxs-lookup"><span data-stu-id="7c321-109">DESCRIPTION</span></span>
<span data-ttu-id="7c321-110">Polecenie cmdlet **Start-AzureSiteRecoveryUnplannedFailoverJob** uruchamia nieplanowaną pracę awaryjną w trybie failover jednostki ochrony usługi Azure Site Recovery lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="7c321-110">The **Start-AzureSiteRecoveryUnplannedFailoverJob** cmdlet starts the unplanned failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="7c321-111">Możesz sprawdzić, czy zadanie powiodło się przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryJob** .</span><span class="sxs-lookup"><span data-stu-id="7c321-111">You can check whether the job succeeds by using the **Get-AzureSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="7c321-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7c321-112">EXAMPLES</span></span>

### <span data-ttu-id="7c321-113">Przykład 1. uruchomienie niezaplanowanego zadania w trybie failover</span><span class="sxs-lookup"><span data-stu-id="7c321-113">Example 1: Start an unplanned failover job</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer 
PS C:\> Start-AzureSiteRecoveryUnplannedFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
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

<span data-ttu-id="7c321-114">Pierwsze polecenie uzyskuje chroniony kontener za pomocą polecenia cmdlet **Get-AzureSiteRecoveryProtectionContainer** , a następnie zapisuje go w zmiennej $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="7c321-114">The first command gets a protected container by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="7c321-115">Drugie polecenie pobiera chronione jednostki należące do kontenera chronionego przechowywanego w $ProtectionContainer przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="7c321-115">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="7c321-116">Polecenie zapisuje wyniki w zmiennej $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="7c321-116">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="7c321-117">Ostatnie polecenie uruchamia tryb failover dla chronionych obiektów przechowywanych w $ProtectionEntity i określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="7c321-117">The final command starts the failover for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

## <span data-ttu-id="7c321-118">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7c321-118">PARAMETERS</span></span>

### <span data-ttu-id="7c321-119">-Direction</span><span class="sxs-lookup"><span data-stu-id="7c321-119">-Direction</span></span>
<span data-ttu-id="7c321-120">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="7c321-120">Specifies the direction of the failover.</span></span>
<span data-ttu-id="7c321-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="7c321-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="7c321-122">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="7c321-122">PrimaryToRecovery</span></span>
- <span data-ttu-id="7c321-123">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="7c321-123">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="7c321-124">-PerformSourceSideActions</span><span class="sxs-lookup"><span data-stu-id="7c321-124">-PerformSourceSideActions</span></span>
<span data-ttu-id="7c321-125">Wskazuje, że akcja może wykonać akcje po stronie źródła.</span><span class="sxs-lookup"><span data-stu-id="7c321-125">Indicates that the action can perform source side actions.</span></span>

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

### <span data-ttu-id="7c321-126">-PerformSourceSiteOperations</span><span class="sxs-lookup"><span data-stu-id="7c321-126">-PerformSourceSiteOperations</span></span>
<span data-ttu-id="7c321-127">Wskazuje, że operacje witryny źródłowej mogą być wykonywane.</span><span class="sxs-lookup"><span data-stu-id="7c321-127">Indicates that source site operations can be performed.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByPEId, ByPEObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c321-128">-PrimaryAction</span><span class="sxs-lookup"><span data-stu-id="7c321-128">-PrimaryAction</span></span>
<span data-ttu-id="7c321-129">Wskazuje, że akcje witryny podstawowej są wymagane.</span><span class="sxs-lookup"><span data-stu-id="7c321-129">Indicates that  primary site actions are required.</span></span>

```yaml
Type: Boolean
Parameter Sets: ByRPId, ByRPObject
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7c321-130">-Profile</span><span class="sxs-lookup"><span data-stu-id="7c321-130">-Profile</span></span>
<span data-ttu-id="7c321-131">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7c321-131">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7c321-132">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="7c321-132">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7c321-133">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="7c321-133">-ProtectionContainerId</span></span>
<span data-ttu-id="7c321-134">Określa identyfikator chronionego kontenera.</span><span class="sxs-lookup"><span data-stu-id="7c321-134">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="7c321-135">To polecenie cmdlet uruchamia zadanie chronionej maszyny wirtualnej należącej do kontenera, które to polecenie cmdlet określa.</span><span class="sxs-lookup"><span data-stu-id="7c321-135">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="7c321-136">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7c321-136">-ProtectionEntity</span></span>
<span data-ttu-id="7c321-137">Określa obiekt jednostki ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="7c321-137">Specifies the Site Recovery protection entity object.</span></span>

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

### <span data-ttu-id="7c321-138">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="7c321-138">-ProtectionEntityId</span></span>
<span data-ttu-id="7c321-139">Określa identyfikator chronionej maszyny wirtualnej, dla której ma zostać uruchomione zadanie.</span><span class="sxs-lookup"><span data-stu-id="7c321-139">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

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

### <span data-ttu-id="7c321-140">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="7c321-140">-RecoveryPlan</span></span>
<span data-ttu-id="7c321-141">Określa obiekt planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="7c321-141">Specifies a recovery plan object.</span></span>

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

### <span data-ttu-id="7c321-142">-RPId</span><span class="sxs-lookup"><span data-stu-id="7c321-142">-RPId</span></span>
<span data-ttu-id="7c321-143">Określa identyfikator planu odzyskiwania, dla którego ma zostać uruchomione zadanie.</span><span class="sxs-lookup"><span data-stu-id="7c321-143">Specifies the ID of a recovery plan for which to start the job.</span></span>

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

### <span data-ttu-id="7c321-144">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="7c321-144">-WaitForCompletion</span></span>
<span data-ttu-id="7c321-145">Wskazuje, że polecenie cmdlet oczekuje na zakończenie operacji przed zwróceniem sterowania do konsoli programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="7c321-145">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="7c321-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c321-146">CommonParameters</span></span>
<span data-ttu-id="7c321-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c321-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c321-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c321-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c321-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7c321-149">INPUTS</span></span>

## <span data-ttu-id="7c321-150">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7c321-150">OUTPUTS</span></span>

## <span data-ttu-id="7c321-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7c321-151">NOTES</span></span>

## <span data-ttu-id="7c321-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7c321-152">RELATED LINKS</span></span>

[<span data-ttu-id="7c321-153">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="7c321-153">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="7c321-154">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="7c321-154">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="7c321-155">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="7c321-155">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="7c321-156">Start — AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="7c321-156">Start-AzureSiteRecoveryTestFailoverJob</span></span>](./Start-AzureSiteRecoveryTestFailoverJob.md)


