---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 44A22B6C-5FD4-43B0-9726-71E28AE53E9D
online version: ''
schema: 2.0.0
ms.openlocfilehash: de1b7a24c1af362297319d0297ce356b00ef9d49
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054744"
---
# <span data-ttu-id="9ff2b-101">Start-AzureSiteRecoveryCommitFailoverJob</span><span class="sxs-lookup"><span data-stu-id="9ff2b-101">Start-AzureSiteRecoveryCommitFailoverJob</span></span>

## <span data-ttu-id="9ff2b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9ff2b-102">SYNOPSIS</span></span>
<span data-ttu-id="9ff2b-103">Rozpoczyna akcję zatwierdzania trybu failover dla obiektu odzyskiwania witryny.</span><span class="sxs-lookup"><span data-stu-id="9ff2b-103">Starts the commit failover action for a Site Recovery object.</span></span>

## <span data-ttu-id="9ff2b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9ff2b-104">SYNTAX</span></span>

### <span data-ttu-id="9ff2b-105">ByRPId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="9ff2b-105">ByRPId (Default)</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RPId <String> [-Direction <String>] [-WaitForCompletion]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9ff2b-106">ByPEId</span><span class="sxs-lookup"><span data-stu-id="9ff2b-106">ByPEId</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntityId <String> -ProtectionContainerId <String>
 [-Direction <String>] [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9ff2b-107">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="9ff2b-107">ByRPObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -RecoveryPlan <ASRRecoveryPlan> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="9ff2b-108">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="9ff2b-108">ByPEObject</span></span>
```
Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity <ASRProtectionEntity> [-Direction <String>]
 [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9ff2b-109">Opis</span><span class="sxs-lookup"><span data-stu-id="9ff2b-109">DESCRIPTION</span></span>
<span data-ttu-id="9ff2b-110">Polecenie cmdlet **Start-AzureSiteRecoveryCommitFailoverJob** uruchamia proces zatwierdzania trybu failover dla obiektu odzyskiwania witryny Azure po wykonaniu operacji przełączania awaryjnego.</span><span class="sxs-lookup"><span data-stu-id="9ff2b-110">The **Start-AzureSiteRecoveryCommitFailoverJob** cmdlet starts the commit failover process for an Azure Site Recovery object after a failover operation.</span></span>

## <span data-ttu-id="9ff2b-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9ff2b-111">EXAMPLES</span></span>

### <span data-ttu-id="9ff2b-112">Przykład 1. Rozpocznij zadanie zatwierdzania pracy w trybie failover</span><span class="sxs-lookup"><span data-stu-id="9ff2b-112">Example 1: Start a commit failover job</span></span>
```
PS C:\> $Container = Get-AzureSiteRecoveryProtectionContainer 
PS C:\> $Protected = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $Container 
PS C:\> Start-AzureSiteRecoveryCommitFailoverJob -ProtectionEntity $Protected
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

<span data-ttu-id="9ff2b-113">Pierwsze polecenie pobiera wszystkie chronione kontenery dla bieżącego magazynu usługi Azure Site Recovery, korzystając z polecenia cmdlet **Get-AzureSiteRecoveryProtectionContainer** , a następnie zapisuje wyniki w zmiennej $Container.</span><span class="sxs-lookup"><span data-stu-id="9ff2b-113">The first command gets all protected containers for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryProtectionContainer** cmdlet, and then stores the results in the $Container variable.</span></span>

<span data-ttu-id="9ff2b-114">Drugie polecenie pobiera chronione maszyny wirtualne należące do kontenera przechowywanego w $Container przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="9ff2b-114">The second command gets the protected virtual machines that belong to the container stored in $Container by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="9ff2b-115">Polecenie zapisuje wyniki w zmiennej $Protected.</span><span class="sxs-lookup"><span data-stu-id="9ff2b-115">The command stores the results in the $Protected variable.</span></span>

<span data-ttu-id="9ff2b-116">Ostatnie polecenie uruchamia zadanie przejęcia awaryjnego dla chronionych obiektów przechowywanych w $Protected.</span><span class="sxs-lookup"><span data-stu-id="9ff2b-116">The final command starts the failover job for the protected objects stored in $Protected.</span></span>

## <span data-ttu-id="9ff2b-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9ff2b-117">PARAMETERS</span></span>

### <span data-ttu-id="9ff2b-118">-Direction</span><span class="sxs-lookup"><span data-stu-id="9ff2b-118">-Direction</span></span>
<span data-ttu-id="9ff2b-119">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="9ff2b-119">Specifies the direction of the failover.</span></span>
<span data-ttu-id="9ff2b-120">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9ff2b-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9ff2b-121">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="9ff2b-121">PrimaryToRecovery</span></span>
- <span data-ttu-id="9ff2b-122">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="9ff2b-122">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="9ff2b-123">-Profile</span><span class="sxs-lookup"><span data-stu-id="9ff2b-123">-Profile</span></span>
<span data-ttu-id="9ff2b-124">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9ff2b-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9ff2b-125">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="9ff2b-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9ff2b-126">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="9ff2b-126">-ProtectionContainerId</span></span>
<span data-ttu-id="9ff2b-127">Określa identyfikator chronionego kontenera.</span><span class="sxs-lookup"><span data-stu-id="9ff2b-127">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="9ff2b-128">To polecenie cmdlet uruchamia zadanie chronionej maszyny wirtualnej należącej do kontenera, które to polecenie cmdlet określa.</span><span class="sxs-lookup"><span data-stu-id="9ff2b-128">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

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

### <span data-ttu-id="9ff2b-129">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="9ff2b-129">-ProtectionEntity</span></span>
<span data-ttu-id="9ff2b-130">Określa obiekt **ASRProtectionEntity** , dla którego ma zostać uruchomione zadanie.</span><span class="sxs-lookup"><span data-stu-id="9ff2b-130">Specifies an **ASRProtectionEntity** object for which to start the job.</span></span>
<span data-ttu-id="9ff2b-131">Aby uzyskać obiekt **ASRProtectionEntity** , użyj polecenia cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="9ff2b-131">To obtain an **ASRProtectionEntity** object, use the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>

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

### <span data-ttu-id="9ff2b-132">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="9ff2b-132">-ProtectionEntityId</span></span>
<span data-ttu-id="9ff2b-133">Określa identyfikator chronionej maszyny wirtualnej, dla której ma zostać uruchomione zadanie.</span><span class="sxs-lookup"><span data-stu-id="9ff2b-133">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

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

### <span data-ttu-id="9ff2b-134">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9ff2b-134">-RecoveryPlan</span></span>
<span data-ttu-id="9ff2b-135">Określa obiekt planu odzyskiwania, dla którego ma zostać uruchomione zadanie.</span><span class="sxs-lookup"><span data-stu-id="9ff2b-135">Specifies a recovery plan object for which to start the job.</span></span>
<span data-ttu-id="9ff2b-136">Aby uzyskać obiekt **ASRRecoveryPlan** , użyj polecenia cmdlet **Get-AzureSiteRecoveryRecoveryPlan** .</span><span class="sxs-lookup"><span data-stu-id="9ff2b-136">To obtain an **ASRRecoveryPlan** object, use the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>

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

### <span data-ttu-id="9ff2b-137">-RPId</span><span class="sxs-lookup"><span data-stu-id="9ff2b-137">-RPId</span></span>
<span data-ttu-id="9ff2b-138">Określa identyfikator planu odzyskiwania, dla którego ma zostać uruchomione zadanie.</span><span class="sxs-lookup"><span data-stu-id="9ff2b-138">Specifies the ID of a recovery plan for which to start the job.</span></span>

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

### <span data-ttu-id="9ff2b-139">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="9ff2b-139">-WaitForCompletion</span></span>
<span data-ttu-id="9ff2b-140">Wskazuje, że polecenie cmdlet oczekuje na zakończenie operacji przed zwróceniem sterowania do konsoli programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="9ff2b-140">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="9ff2b-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ff2b-141">CommonParameters</span></span>
<span data-ttu-id="9ff2b-142">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ff2b-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ff2b-143">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ff2b-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ff2b-144">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9ff2b-144">INPUTS</span></span>

## <span data-ttu-id="9ff2b-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9ff2b-145">OUTPUTS</span></span>

## <span data-ttu-id="9ff2b-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9ff2b-146">NOTES</span></span>

## <span data-ttu-id="9ff2b-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9ff2b-147">RELATED LINKS</span></span>

[<span data-ttu-id="9ff2b-148">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="9ff2b-148">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="9ff2b-149">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="9ff2b-149">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="9ff2b-150">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="9ff2b-150">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)


