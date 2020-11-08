---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 9AE41884-C39F-4AEB-8030-96167F98C8DD
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6b46cc27b2e5380f3cb533a4355a94170e941cd8
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054994"
---
# <span data-ttu-id="018c1-101">Start-AzureSiteRecoveryTestFailoverJob</span><span class="sxs-lookup"><span data-stu-id="018c1-101">Start-AzureSiteRecoveryTestFailoverJob</span></span>

## <span data-ttu-id="018c1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="018c1-102">SYNOPSIS</span></span>
<span data-ttu-id="018c1-103">Rozpoczyna test pracy awaryjnej jednostki ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="018c1-103">Starts a test failover for a Site Recovery protection entity.</span></span>

## <span data-ttu-id="018c1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="018c1-104">SYNTAX</span></span>

### <span data-ttu-id="018c1-105">ByPEId (domyślny)</span><span class="sxs-lookup"><span data-stu-id="018c1-105">ByPEId (Default)</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="018c1-106">ByRPId</span><span class="sxs-lookup"><span data-stu-id="018c1-106">ByRPId</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="018c1-107">ByRPIdWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="018c1-107">ByRPIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="018c1-108">ByRPIdWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="018c1-108">ByRPIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> [-Network <ASRNetwork>] [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="018c1-109">ByRPIdWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="018c1-109">ByRPIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -RpId <String> -Network <ASRNetwork> [-NetworkType <String>]
 -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="018c1-110">ByPEObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="018c1-110">ByPEObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="018c1-111">ByRPObjectWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="018c1-111">ByRPObjectWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="018c1-112">ByPEIdWithVMNetwork</span><span class="sxs-lookup"><span data-stu-id="018c1-112">ByPEIdWithVMNetwork</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob -Network <ASRNetwork> [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="018c1-113">ByRPObject</span><span class="sxs-lookup"><span data-stu-id="018c1-113">ByRPObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

### <span data-ttu-id="018c1-114">ByRPObjectWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="018c1-114">ByRPObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="018c1-115">ByRPObjectWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="018c1-115">ByRPObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>]
 -RecoveryPlan <ASRRecoveryPlan> -Direction <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="018c1-116">ByPEIdWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="018c1-116">ByPEIdWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="018c1-117">ByPEIdWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="018c1-117">ByPEIdWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntityId <String> -ProtectionContainerId <String> [-WaitForCompletion] -VmNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="018c1-118">ByPEObject</span><span class="sxs-lookup"><span data-stu-id="018c1-118">ByPEObject</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="018c1-119">ByPEObjectWithLogicalNetworkID</span><span class="sxs-lookup"><span data-stu-id="018c1-119">ByPEObjectWithLogicalNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -LogicalNetworkId <String>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="018c1-120">ByPEObjectWithVMNetworkID</span><span class="sxs-lookup"><span data-stu-id="018c1-120">ByPEObjectWithVMNetworkID</span></span>
```
Start-AzureSiteRecoveryTestFailoverJob [-Network <ASRNetwork>] [-NetworkType <String>] -Direction <String>
 -ProtectionEntity <ASRProtectionEntity> [-WaitForCompletion] -VmNetworkId <String> [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="018c1-121">Opis</span><span class="sxs-lookup"><span data-stu-id="018c1-121">DESCRIPTION</span></span>
<span data-ttu-id="018c1-122">Polecenie cmdlet **Start-AzureSiteRecoveryTestFailoverJob** rozpoczyna test pracy awaryjnej jednostki ochrony usługi Azure Site Recovery lub planu odzyskiwania.</span><span class="sxs-lookup"><span data-stu-id="018c1-122">The **Start-AzureSiteRecoveryTestFailoverJob** cmdlet starts test failover of an Azure Site Recovery protection entity or recovery plan.</span></span>
<span data-ttu-id="018c1-123">Możesz sprawdzić, czy zadanie powiodło się przy użyciu polecenia cmdlet **Get-AzureRMSiteRecoveryJob** .</span><span class="sxs-lookup"><span data-stu-id="018c1-123">You can check whether the job succeeded by using the **Get-AzureRMSiteRecoveryJob** cmdlet.</span></span>

## <span data-ttu-id="018c1-124">Przykłady</span><span class="sxs-lookup"><span data-stu-id="018c1-124">EXAMPLES</span></span>

### <span data-ttu-id="018c1-125">Przykład 1. Uruchamianie testowej pracy w trybie failover</span><span class="sxs-lookup"><span data-stu-id="018c1-125">Example 1: Start a test failover</span></span>
```
PS C:\> $ProtectionContainer = Get-AzureSiteRecoveryProtectionContainer
PS C:\> $ProtectionEntity = Get-AzureSiteRecoveryProtectionEntity -ProtectionContainer $ProtectionContainer
PS C:\> Start-AzureSiteRecoveryTestFailoverJob -ProtectionEntity $ProtectionEntity -Direction "PrimaryToRecovery"
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

<span data-ttu-id="018c1-126">W pierwszym poleceniu jest używane polecenie cmdlet **Get-AzureSiteRecoveryProtectionContainer** w celu uzyskania chronionego kontenera, a następnie zapisanie go w zmiennej $ProtectionContainer.</span><span class="sxs-lookup"><span data-stu-id="018c1-126">The first command uses the **Get-AzureSiteRecoveryProtectionContainer** cmdlet to get a protected container, and then stores it in the $ProtectionContainer variable.</span></span>

<span data-ttu-id="018c1-127">Drugie polecenie pobiera chronione jednostki należące do kontenera chronionego przechowywanego w $ProtectionContainer przy użyciu polecenia cmdlet **Get-AzureSiteRecoveryProtectionEntity** .</span><span class="sxs-lookup"><span data-stu-id="018c1-127">The second command gets the protected entities that belong to the protected container stored in $ProtectionContainer by using the **Get-AzureSiteRecoveryProtectionEntity** cmdlet.</span></span>
<span data-ttu-id="018c1-128">Polecenie zapisuje wyniki w zmiennej $ProtectionEntity.</span><span class="sxs-lookup"><span data-stu-id="018c1-128">The command stores the results in the $ProtectionEntity variable.</span></span>

<span data-ttu-id="018c1-129">Ostatnie polecenie uruchamia operację testowej pracy w trybie failover dla chronionych encji przechowywanych w $ProtectionEntity i określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="018c1-129">The final command starts the test failover operation for the protected entities stored in $ProtectionEntity and specifies the direction of the failover.</span></span>

### <span data-ttu-id="018c1-130">Przykład 2: Rozpoczynanie testowej pracy w trybie failover przy użyciu planu odzyskiwania</span><span class="sxs-lookup"><span data-stu-id="018c1-130">Example 2: Start a test failover using a recovery plan</span></span>
```
PS C:\> $RecoveryPlan = Get-AzureSiteRecoveryRecoveryPlan -Name "RecoveryPlan01"
Start-AzureSiteRecoveryTestFailoverJob -Direction PrimaryToRecovery -RecoveryPlan $RecoveryPlan
```

<span data-ttu-id="018c1-131">To polecenie pobiera plan odzyskiwania o nazwie RecoveryPlan01 dla bieżącego magazynu usługi Azure Site Recovery za pomocą polecenia cmdlet **Get-AzureSiteRecoveryRecoveryPlan** .</span><span class="sxs-lookup"><span data-stu-id="018c1-131">This command gets the recovery plan named RecoveryPlan01 for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryRecoveryPlan** cmdlet.</span></span>
<span data-ttu-id="018c1-132">Polecenie zapisuje plan w zmiennej $RecoveryPlan.</span><span class="sxs-lookup"><span data-stu-id="018c1-132">The command stores the plan in the $RecoveryPlan variable.</span></span>

<span data-ttu-id="018c1-133">Drugie polecenie uruchamia operację testowej pracy w trybie failover dla planu odzyskiwania przechowywanego w $RecoveryPlan i określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="018c1-133">The second command starts the test failover operation for the recovery plan stored in $RecoveryPlan and specifies the direction of the failover.</span></span>

## <span data-ttu-id="018c1-134">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="018c1-134">PARAMETERS</span></span>

### <span data-ttu-id="018c1-135">-Direction</span><span class="sxs-lookup"><span data-stu-id="018c1-135">-Direction</span></span>
<span data-ttu-id="018c1-136">Określa kierunek pracy awaryjnej.</span><span class="sxs-lookup"><span data-stu-id="018c1-136">Specifies the failover direction.</span></span>
<span data-ttu-id="018c1-137">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="018c1-137">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="018c1-138">PrimaryToRecovery</span><span class="sxs-lookup"><span data-stu-id="018c1-138">PrimaryToRecovery</span></span>
- <span data-ttu-id="018c1-139">RecoveryToPrimary</span><span class="sxs-lookup"><span data-stu-id="018c1-139">RecoveryToPrimary</span></span>

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

### <span data-ttu-id="018c1-140">-LogicalNetworkId</span><span class="sxs-lookup"><span data-stu-id="018c1-140">-LogicalNetworkId</span></span>
<span data-ttu-id="018c1-141">Określa identyfikator sieci logicznej.</span><span class="sxs-lookup"><span data-stu-id="018c1-141">Specifies the ID of the logical network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithLogicalNetworkID, ByRPObjectWithLogicalNetworkID, ByPEIdWithLogicalNetworkID, ByPEObjectWithLogicalNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="018c1-142">-Network</span><span class="sxs-lookup"><span data-stu-id="018c1-142">-Network</span></span>
<span data-ttu-id="018c1-143">Określa obiekt sieciowy, którego należy użyć w celu przetestowania trybu failover.</span><span class="sxs-lookup"><span data-stu-id="018c1-143">Specifies the network object to use for test failover.</span></span>
<span data-ttu-id="018c1-144">Aby uzyskać sieć, użyj polecenia cmdlet **Get-AzureSiteRecoveryNetwork** .</span><span class="sxs-lookup"><span data-stu-id="018c1-144">To obtain a network, use the **Get-AzureSiteRecoveryNetwork** cmdlet.</span></span>

```yaml
Type: ASRNetwork
Parameter Sets: ByPEId, ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPObject, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID, ByPEObject, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRNetwork
Parameter Sets: ByRPIdWithVMNetwork, ByPEObjectWithVMNetwork, ByRPObjectWithVMNetwork, ByPEIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="018c1-145">-Workname</span><span class="sxs-lookup"><span data-stu-id="018c1-145">-NetworkType</span></span>
<span data-ttu-id="018c1-146">Określa typ sieci, który ma być używany do testowania pracy w trybie failover.</span><span class="sxs-lookup"><span data-stu-id="018c1-146">Specifies the network type to use for test failover.</span></span>
<span data-ttu-id="018c1-147">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="018c1-147">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="018c1-148">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="018c1-148">None</span></span>
- <span data-ttu-id="018c1-149">Nowy</span><span class="sxs-lookup"><span data-stu-id="018c1-149">New</span></span>
- <span data-ttu-id="018c1-150">Istniejące</span><span class="sxs-lookup"><span data-stu-id="018c1-150">Existing</span></span>

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

### <span data-ttu-id="018c1-151">-Profile</span><span class="sxs-lookup"><span data-stu-id="018c1-151">-Profile</span></span>
<span data-ttu-id="018c1-152">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="018c1-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="018c1-153">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="018c1-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="018c1-154">-ProtectionContainerId</span><span class="sxs-lookup"><span data-stu-id="018c1-154">-ProtectionContainerId</span></span>
<span data-ttu-id="018c1-155">Określa identyfikator chronionego kontenera.</span><span class="sxs-lookup"><span data-stu-id="018c1-155">Specifies the ID of a protected container.</span></span>
<span data-ttu-id="018c1-156">To polecenie cmdlet uruchamia zadanie chronionej maszyny wirtualnej należącej do kontenera, które to polecenie cmdlet określa.</span><span class="sxs-lookup"><span data-stu-id="018c1-156">This cmdlet starts the job for a protected virtual machine that belongs to the container that this cmdlet specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="018c1-157">-ProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="018c1-157">-ProtectionEntity</span></span>
<span data-ttu-id="018c1-158">Określa obiekt jednostki ochrony przed odzyskiwaniem witryny.</span><span class="sxs-lookup"><span data-stu-id="018c1-158">Specifies the Site Recovery protection entity object.</span></span>

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObjectWithVMNetwork, ByPEObjectWithLogicalNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRProtectionEntity
Parameter Sets: ByPEObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="018c1-159">-ProtectionEntityId</span><span class="sxs-lookup"><span data-stu-id="018c1-159">-ProtectionEntityId</span></span>
<span data-ttu-id="018c1-160">Określa identyfikator chronionej maszyny wirtualnej, dla której ma zostać uruchomione zadanie.</span><span class="sxs-lookup"><span data-stu-id="018c1-160">Specifies the ID of a protected virtual machine for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByPEId, ByPEIdWithVMNetwork, ByPEIdWithLogicalNetworkID, ByPEIdWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="018c1-161">-RecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="018c1-161">-RecoveryPlan</span></span>
<span data-ttu-id="018c1-162">Określa plan odzyskiwania, dla którego ma zostać uruchomione zadanie.</span><span class="sxs-lookup"><span data-stu-id="018c1-162">Specifies a recovery plan for which to start the job.</span></span>

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObjectWithVMNetwork, ByRPObjectWithLogicalNetworkID, ByRPObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: ASRRecoveryPlan
Parameter Sets: ByRPObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="018c1-163">-RpId</span><span class="sxs-lookup"><span data-stu-id="018c1-163">-RpId</span></span>
<span data-ttu-id="018c1-164">Określa identyfikator planu odzyskiwania, dla którego ma zostać uruchomione zadanie.</span><span class="sxs-lookup"><span data-stu-id="018c1-164">Specifies the ID of a recovery plan for which to start the job.</span></span>

```yaml
Type: String
Parameter Sets: ByRPId, ByRPIdWithLogicalNetworkID, ByRPIdWithVMNetworkID, ByRPIdWithVMNetwork
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="018c1-165">-VmNetworkId</span><span class="sxs-lookup"><span data-stu-id="018c1-165">-VmNetworkId</span></span>
<span data-ttu-id="018c1-166">Określa identyfikator sieci maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="018c1-166">Specifies the ID of the virtual machine network.</span></span>

```yaml
Type: String
Parameter Sets: ByRPIdWithVMNetworkID, ByRPObjectWithVMNetworkID, ByPEIdWithVMNetworkID, ByPEObjectWithVMNetworkID
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="018c1-167">-WaitForCompletion</span><span class="sxs-lookup"><span data-stu-id="018c1-167">-WaitForCompletion</span></span>
<span data-ttu-id="018c1-168">Wskazuje, że polecenie cmdlet oczekuje na zakończenie operacji przed zwróceniem sterowania do konsoli programu Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="018c1-168">Indicates that the cmdlet waits for the operation to complete before it returns control to the Windows PowerShell console.</span></span>

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

### <span data-ttu-id="018c1-169">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="018c1-169">CommonParameters</span></span>
<span data-ttu-id="018c1-170">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="018c1-170">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="018c1-171">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="018c1-171">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="018c1-172">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="018c1-172">INPUTS</span></span>

## <span data-ttu-id="018c1-173">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="018c1-173">OUTPUTS</span></span>

## <span data-ttu-id="018c1-174">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="018c1-174">NOTES</span></span>

## <span data-ttu-id="018c1-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="018c1-175">RELATED LINKS</span></span>

[<span data-ttu-id="018c1-176">Get-AzureSiteRecoveryProtectionContainer</span><span class="sxs-lookup"><span data-stu-id="018c1-176">Get-AzureSiteRecoveryProtectionContainer</span></span>](./Get-AzureSiteRecoveryProtectionContainer.md)

[<span data-ttu-id="018c1-177">Get-AzureSiteRecoveryNetwork</span><span class="sxs-lookup"><span data-stu-id="018c1-177">Get-AzureSiteRecoveryNetwork</span></span>](./Get-AzureSiteRecoveryNetwork.md)

[<span data-ttu-id="018c1-178">Get-AzureSiteRecoveryProtectionEntity</span><span class="sxs-lookup"><span data-stu-id="018c1-178">Get-AzureSiteRecoveryProtectionEntity</span></span>](./Get-AzureSiteRecoveryProtectionEntity.md)

[<span data-ttu-id="018c1-179">Get-AzureSiteRecoveryRecoveryPlan</span><span class="sxs-lookup"><span data-stu-id="018c1-179">Get-AzureSiteRecoveryRecoveryPlan</span></span>](./Get-AzureSiteRecoveryRecoveryPlan.md)

[<span data-ttu-id="018c1-180">Start — AzureSiteRecoveryUnplannedFailoverJob</span><span class="sxs-lookup"><span data-stu-id="018c1-180">Start-AzureSiteRecoveryUnplannedFailoverJob</span></span>](./Start-AzureSiteRecoveryUnplannedFailoverJob.md)


