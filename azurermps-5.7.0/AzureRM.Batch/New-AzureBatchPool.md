---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 54a5d6dc737bc0bd6a7f1d236ce855b2a08dca6a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554158"
---
# <span data-ttu-id="5320a-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="5320a-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="5320a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5320a-102">SYNOPSIS</span></span>
<span data-ttu-id="5320a-103">Tworzy pulę w usłudze przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="5320a-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5320a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5320a-104">SYNTAX</span></span>

### <span data-ttu-id="5320a-105">CloudServiceAndTargetDedicated (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5320a-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5320a-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="5320a-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5320a-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="5320a-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5320a-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="5320a-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5320a-109">Opis</span><span class="sxs-lookup"><span data-stu-id="5320a-109">DESCRIPTION</span></span>
<span data-ttu-id="5320a-110">Polecenie cmdlet **New-AzureBatchPool** tworzy pulę w usłudze Azure Batch pod kontem określonym przez parametr *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="5320a-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="5320a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5320a-111">EXAMPLES</span></span>

### <span data-ttu-id="5320a-112">Przykład 1. Tworzenie nowej puli przy użyciu zestawu parametrów TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="5320a-112">Example 1: Create a new pool using the TargetDedicated parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="5320a-113">To polecenie tworzy nową pulę o IDENTYFIKATORze moja Pula przy użyciu zestawu parametrów TargetDedicated.</span><span class="sxs-lookup"><span data-stu-id="5320a-113">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="5320a-114">Alokacja docelowa to trzy węzły obliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="5320a-114">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="5320a-115">Pula jest skonfigurowana w celu używania małych maszyn wirtualnych z najnowszą wersją systemu operacyjnego rodziny 4.</span><span class="sxs-lookup"><span data-stu-id="5320a-115">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="5320a-116">Przykład 2: Tworzenie nowej puli przy użyciu zestawu parametrów skalowania automatycznego</span><span class="sxs-lookup"><span data-stu-id="5320a-116">Example 2: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="5320a-117">To polecenie tworzy nową pulę o IDENTYFIKATORze AutoScalePool przy użyciu zestawu parametrów autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="5320a-117">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="5320a-118">Pula jest skonfigurowana w celu używania małych maszyn wirtualnych z najnowszą wersją systemu operacyjnego rodziny 4, a liczba docelowa węzłów obliczeniowych jest określona przez formułę skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="5320a-118">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="5320a-119">Przykład 3: Tworzenie puli z węzłami w podsieci</span><span class="sxs-lookup"><span data-stu-id="5320a-119">Example 3: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="5320a-120">Przykład 4: Tworzenie puli z niestandardowymi kontami użytkowników</span><span class="sxs-lookup"><span data-stu-id="5320a-120">Example 4: Create a pool with custom user accounts</span></span>
```
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="5320a-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5320a-121">PARAMETERS</span></span>

### <span data-ttu-id="5320a-122">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="5320a-122">-ApplicationLicenses</span></span>
<span data-ttu-id="5320a-123">Lista licencji na aplikacje, które usługa wsadowa będzie udostępniać w każdym węźle obliczeniowym w puli.</span><span class="sxs-lookup"><span data-stu-id="5320a-123">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases: ApplicationLicense

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-124">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="5320a-124">-ApplicationPackageReferences</span></span>
```yaml
Type: PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-125">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="5320a-125">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="5320a-126">Określa czas (w minutach), po upływie którego rozmiar puli będzie automatycznie dostosowywany zgodnie z formułą skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="5320a-126">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="5320a-127">Wartość domyślna to 15 minut, a wartość minimalna to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="5320a-127">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-128">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="5320a-128">-AutoScaleFormula</span></span>
<span data-ttu-id="5320a-129">Określa formułę do automatycznego skalowania puli.</span><span class="sxs-lookup"><span data-stu-id="5320a-129">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-130">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="5320a-130">-BatchContext</span></span>
<span data-ttu-id="5320a-131">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="5320a-131">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5320a-132">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="5320a-132">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5320a-133">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="5320a-133">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5320a-134">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="5320a-134">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5320a-135">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="5320a-135">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-136">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="5320a-136">-CertificateReferences</span></span>
<span data-ttu-id="5320a-137">Określa Certyfikaty skojarzone z pulą.</span><span class="sxs-lookup"><span data-stu-id="5320a-137">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="5320a-138">Usługa przetwarzania wsadowego instaluje certyfikaty, których dotyczy odwołanie, w każdym węźle obliczeniowym puli.</span><span class="sxs-lookup"><span data-stu-id="5320a-138">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-139">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5320a-139">-CloudServiceConfiguration</span></span>
<span data-ttu-id="5320a-140">Określa ustawienia konfiguracji puli na podstawie platformy usługi Azure Cloud.</span><span class="sxs-lookup"><span data-stu-id="5320a-140">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5320a-141">-DefaultProfile</span></span>
<span data-ttu-id="5320a-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5320a-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5320a-143">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="5320a-143">-DisplayName</span></span>
<span data-ttu-id="5320a-144">Określa nazwę wyświetlaną puli.</span><span class="sxs-lookup"><span data-stu-id="5320a-144">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="5320a-145">-ID</span><span class="sxs-lookup"><span data-stu-id="5320a-145">-Id</span></span>
<span data-ttu-id="5320a-146">Określa identyfikator puli, która ma zostać utworzona.</span><span class="sxs-lookup"><span data-stu-id="5320a-146">Specifies the ID of the pool to create.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-147">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="5320a-147">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="5320a-148">Wskazuje, że ten aplet polecenia konfiguruje pulę w celu bezpośredniej komunikacji między dedykowanymi węzłami obliczeniowymi.</span><span class="sxs-lookup"><span data-stu-id="5320a-148">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="5320a-149">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="5320a-149">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="5320a-150">Określa maksymalną liczbę zadań, które mogą być uruchamiane w pojedynczym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="5320a-150">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-151">-Metadata</span><span class="sxs-lookup"><span data-stu-id="5320a-151">-Metadata</span></span>
<span data-ttu-id="5320a-152">Określa metadane, jako pary klucz/wartość, które mają zostać dodane do nowej puli.</span><span class="sxs-lookup"><span data-stu-id="5320a-152">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="5320a-153">Klucz to nazwa metadanych.</span><span class="sxs-lookup"><span data-stu-id="5320a-153">The key is the metadata name.</span></span>
<span data-ttu-id="5320a-154">Wartość jest wartością metadanych.</span><span class="sxs-lookup"><span data-stu-id="5320a-154">The value is the metadata value.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-155">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5320a-155">-NetworkConfiguration</span></span>
<span data-ttu-id="5320a-156">Konfiguracja sieci dla puli.</span><span class="sxs-lookup"><span data-stu-id="5320a-156">The network configuration for the pool.</span></span>

```yaml
Type: PSNetworkConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-157">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="5320a-157">-ResizeTimeout</span></span>
<span data-ttu-id="5320a-158">Określa limit czasu przydzielania węzłów obliczeniowych do puli.</span><span class="sxs-lookup"><span data-stu-id="5320a-158">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-159">-StartTask</span><span class="sxs-lookup"><span data-stu-id="5320a-159">-StartTask</span></span>
<span data-ttu-id="5320a-160">Określa specyfikację zadania rozpoczęcia puli.</span><span class="sxs-lookup"><span data-stu-id="5320a-160">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="5320a-161">Zadanie Rozpoczynanie jest uruchamiane, gdy węzeł obliczeniowy dołączy się do puli, lub gdy węzeł obliczeniowy zostanie ponownie uruchomiony lub ponownie wykonany.</span><span class="sxs-lookup"><span data-stu-id="5320a-161">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: PSStartTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-162">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="5320a-162">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="5320a-163">Określa liczbę docelową dedykowanych węzłów obliczeniowych do przydzielenia do puli.</span><span class="sxs-lookup"><span data-stu-id="5320a-163">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-164">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="5320a-164">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="5320a-165">Określa liczbę docelowych węzłów obliczeniowych o niskim priorytecie, które mają zostać przydzielone do puli.</span><span class="sxs-lookup"><span data-stu-id="5320a-165">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

```yaml
Type: Int32
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-166">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="5320a-166">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="5320a-167">Określa zasady planowania zadań, takie jak ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="5320a-167">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-168">-Kontoużytkownika</span><span class="sxs-lookup"><span data-stu-id="5320a-168">-UserAccount</span></span>
<span data-ttu-id="5320a-169">Lista kont użytkowników, które mają zostać utworzone na każdym węźle w puli.</span><span class="sxs-lookup"><span data-stu-id="5320a-169">The list of user accounts to be created on each node in the pool.</span></span>

```yaml
Type: PSUserAccount[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-170">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="5320a-170">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="5320a-171">Określa ustawienia konfiguracji puli w infrastrukturze maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="5320a-171">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-172">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="5320a-172">-VirtualMachineSize</span></span>
<span data-ttu-id="5320a-173">Określa rozmiar maszyn wirtualnych w puli.</span><span class="sxs-lookup"><span data-stu-id="5320a-173">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="5320a-174">Aby uzyskać więcej informacji o rozmiarach maszyn wirtualnych, zobacz rozmiary dla maszyn wirtualnych https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) w witrynie platformy Microsoft Azure).</span><span class="sxs-lookup"><span data-stu-id="5320a-174">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="5320a-175">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5320a-175">-Confirm</span></span>
<span data-ttu-id="5320a-176">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5320a-176">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-177">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5320a-177">-WhatIf</span></span>
<span data-ttu-id="5320a-178">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5320a-178">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5320a-179">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5320a-179">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5320a-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5320a-180">CommonParameters</span></span>
<span data-ttu-id="5320a-181">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5320a-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5320a-182">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5320a-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5320a-183">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5320a-183">INPUTS</span></span>

### <span data-ttu-id="5320a-184">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5320a-184">BatchAccountContext</span></span>
<span data-ttu-id="5320a-185">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="5320a-185">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="5320a-186">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5320a-186">OUTPUTS</span></span>

## <span data-ttu-id="5320a-187">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5320a-187">NOTES</span></span>

## <span data-ttu-id="5320a-188">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5320a-188">RELATED LINKS</span></span>

[<span data-ttu-id="5320a-189">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="5320a-189">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="5320a-190">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="5320a-190">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="5320a-191">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="5320a-191">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="5320a-192">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="5320a-192">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


