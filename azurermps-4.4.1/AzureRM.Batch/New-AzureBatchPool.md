---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: 3a9534ea2fd0f1bcfc17f9eb5df63b25f7760f2f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547051"
---
# <span data-ttu-id="8da82-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="8da82-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="8da82-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8da82-102">SYNOPSIS</span></span>
<span data-ttu-id="8da82-103">Tworzy pulę w usłudze przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="8da82-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8da82-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8da82-104">SYNTAX</span></span>

### <span data-ttu-id="8da82-105">CloudServiceAndTargetDedicated (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8da82-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8da82-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="8da82-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-ResizeTimeout <TimeSpan>] [-TargetDedicated <Int32>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8da82-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="8da82-107">CloudServiceAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8da82-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="8da82-108">VirtualMachineAndAutoScale</span></span>
```
New-AzureBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8da82-109">Opis</span><span class="sxs-lookup"><span data-stu-id="8da82-109">DESCRIPTION</span></span>
<span data-ttu-id="8da82-110">Polecenie cmdlet **New-AzureBatchPool** tworzy pulę w usłudze Azure Batch pod kontem określonym przez parametr *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="8da82-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="8da82-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8da82-111">EXAMPLES</span></span>

### <span data-ttu-id="8da82-112">Przykład 1. Tworzenie nowej puli przy użyciu zestawu parametrów TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="8da82-112">Example 1: Create a new pool using the TargetDedicated parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -TargetDedicated 3 -BatchContext $Context
```

<span data-ttu-id="8da82-113">To polecenie tworzy nową pulę o IDENTYFIKATORze moja Pula przy użyciu zestawu parametrów TargetDedicated.</span><span class="sxs-lookup"><span data-stu-id="8da82-113">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="8da82-114">Alokacja docelowa to trzy węzły obliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="8da82-114">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="8da82-115">Pula jest skonfigurowana w celu używania małych maszyn wirtualnych z najnowszą wersją systemu operacyjnego rodziny 4.</span><span class="sxs-lookup"><span data-stu-id="8da82-115">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="8da82-116">Przykład 2: Tworzenie nowej puli przy użyciu zestawu parametrów skalowania automatycznego</span><span class="sxs-lookup"><span data-stu-id="8da82-116">Example 2: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -OSFamily "4" -TargetOSVersion "*" -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="8da82-117">To polecenie tworzy nową pulę o IDENTYFIKATORze AutoScalePool przy użyciu zestawu parametrów autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="8da82-117">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="8da82-118">Pula jest skonfigurowana w celu używania małych maszyn wirtualnych z najnowszą wersją systemu operacyjnego rodziny 4, a liczba docelowa węzłów obliczeniowych jest określona przez formułę skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="8da82-118">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

## <span data-ttu-id="8da82-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8da82-119">PARAMETERS</span></span>

### <span data-ttu-id="8da82-120">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="8da82-120">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-121">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="8da82-121">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="8da82-122">Określa czas (w minutach), po upływie którego rozmiar puli będzie automatycznie dostosowywany zgodnie z formułą skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="8da82-122">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="8da82-123">Wartość domyślna to 15 minut, a wartość minimalna to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="8da82-123">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-124">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="8da82-124">-AutoScaleFormula</span></span>
<span data-ttu-id="8da82-125">Określa formułę do automatycznego skalowania puli.</span><span class="sxs-lookup"><span data-stu-id="8da82-125">Specifies the formula for automatically scaling the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: CloudServiceAndAutoScale, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-126">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="8da82-126">-BatchContext</span></span>
<span data-ttu-id="8da82-127">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="8da82-127">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="8da82-128">Aby uzyskać obiekt **BatchAccountContext** , który zawiera klucze dostępu dla subskrypcji, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys.</span><span class="sxs-lookup"><span data-stu-id="8da82-128">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-129">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="8da82-129">-CertificateReferences</span></span>
<span data-ttu-id="8da82-130">Określa Certyfikaty skojarzone z pulą.</span><span class="sxs-lookup"><span data-stu-id="8da82-130">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="8da82-131">Usługa przetwarzania wsadowego instaluje certyfikaty, których dotyczy odwołanie, w każdym węźle obliczeniowym puli.</span><span class="sxs-lookup"><span data-stu-id="8da82-131">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-132">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="8da82-132">-CloudServiceConfiguration</span></span>
<span data-ttu-id="8da82-133">Określa ustawienia konfiguracji puli na podstawie platformy usługi Azure Cloud.</span><span class="sxs-lookup"><span data-stu-id="8da82-133">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration
Parameter Sets: CloudServiceAndTargetDedicated, CloudServiceAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-134">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8da82-134">-DisplayName</span></span>
<span data-ttu-id="8da82-135">Określa nazwę wyświetlaną puli.</span><span class="sxs-lookup"><span data-stu-id="8da82-135">Specifies the display name of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-136">-ID</span><span class="sxs-lookup"><span data-stu-id="8da82-136">-Id</span></span>
<span data-ttu-id="8da82-137">Określa identyfikator puli, która ma zostać utworzona.</span><span class="sxs-lookup"><span data-stu-id="8da82-137">Specifies the ID of the pool to create.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-138">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="8da82-138">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="8da82-139">Wskazuje, że ten aplet polecenia konfiguruje pulę w celu bezpośredniej komunikacji między dedykowanymi węzłami obliczeniowymi.</span><span class="sxs-lookup"><span data-stu-id="8da82-139">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-140">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="8da82-140">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="8da82-141">Określa maksymalną liczbę zadań, które mogą być uruchamiane w pojedynczym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="8da82-141">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-142">-Metadata</span><span class="sxs-lookup"><span data-stu-id="8da82-142">-Metadata</span></span>
<span data-ttu-id="8da82-143">Określa metadane, jako pary klucz/wartość, które mają zostać dodane do nowej puli.</span><span class="sxs-lookup"><span data-stu-id="8da82-143">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="8da82-144">Klucz to nazwa metadanych.</span><span class="sxs-lookup"><span data-stu-id="8da82-144">The key is the metadata name.</span></span>
<span data-ttu-id="8da82-145">Wartość jest wartością metadanych.</span><span class="sxs-lookup"><span data-stu-id="8da82-145">The value is the metadata value.</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-146">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="8da82-146">-NetworkConfiguration</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-147">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="8da82-147">-ResizeTimeout</span></span>
<span data-ttu-id="8da82-148">Określa limit czasu przydzielania węzłów obliczeniowych do puli.</span><span class="sxs-lookup"><span data-stu-id="8da82-148">Specifies the time-out for allocating compute nodes to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.TimeSpan]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-149">-StartTask</span><span class="sxs-lookup"><span data-stu-id="8da82-149">-StartTask</span></span>
<span data-ttu-id="8da82-150">Określa specyfikację zadania rozpoczęcia puli.</span><span class="sxs-lookup"><span data-stu-id="8da82-150">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="8da82-151">Zadanie Rozpoczynanie jest uruchamiane, gdy węzeł obliczeniowy dołączy się do puli, lub gdy węzeł obliczeniowy zostanie ponownie uruchomiony lub ponownie wykonany.</span><span class="sxs-lookup"><span data-stu-id="8da82-151">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSStartTask
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-152">-TargetDedicated</span><span class="sxs-lookup"><span data-stu-id="8da82-152">-TargetDedicated</span></span>
<span data-ttu-id="8da82-153">Określa liczbę docelową węzłów obliczeniowych, które mają zostać przydzielone do puli.</span><span class="sxs-lookup"><span data-stu-id="8da82-153">Specifies the target number of compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-154">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="8da82-154">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="8da82-155">Określa zasady planowania zadań, takie jak ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="8da82-155">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSTaskSchedulingPolicy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-156">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="8da82-156">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="8da82-157">Określa ustawienia konfiguracji puli w infrastrukturze maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="8da82-157">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration
Parameter Sets: VirtualMachineAndTargetDedicated, VirtualMachineAndAutoScale
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-158">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="8da82-158">-VirtualMachineSize</span></span>
<span data-ttu-id="8da82-159">Określa rozmiar maszyn wirtualnych w puli.</span><span class="sxs-lookup"><span data-stu-id="8da82-159">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="8da82-160">Aby uzyskać więcej informacji o rozmiarach maszyn wirtualnych, zobacz rozmiary dla maszyn wirtualnych https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) w witrynie platformy Microsoft Azure).</span><span class="sxs-lookup"><span data-stu-id="8da82-160">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-161">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8da82-161">-Confirm</span></span>
<span data-ttu-id="8da82-162">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8da82-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8da82-163">-WhatIf</span></span>
<span data-ttu-id="8da82-164">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8da82-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8da82-165">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8da82-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-166">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da82-166">-DefaultProfile</span></span>
<span data-ttu-id="8da82-167">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8da82-167">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8da82-168">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da82-168">CommonParameters</span></span>
<span data-ttu-id="8da82-169">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8da82-169">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da82-170">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8da82-170">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da82-171">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8da82-171">INPUTS</span></span>

### <span data-ttu-id="8da82-172">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="8da82-172">BatchAccountContext</span></span>
<span data-ttu-id="8da82-173">Parametr "BatchContext" akceptuje wartość typu "BatchAccountContext" z rurociągu</span><span class="sxs-lookup"><span data-stu-id="8da82-173">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

## <span data-ttu-id="8da82-174">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8da82-174">OUTPUTS</span></span>

## <span data-ttu-id="8da82-175">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8da82-175">NOTES</span></span>

## <span data-ttu-id="8da82-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8da82-176">RELATED LINKS</span></span>

[<span data-ttu-id="8da82-177">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="8da82-177">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="8da82-178">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="8da82-178">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="8da82-179">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="8da82-179">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="8da82-180">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="8da82-180">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


