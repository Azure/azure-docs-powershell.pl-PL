---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/powershell/module/az.batch/new-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
ms.openlocfilehash: 7fef035eda89d68d757658a512ca00369b69694a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992965"
---
# <span data-ttu-id="5e70c-101">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="5e70c-101">New-AzBatchPool</span></span>

## <span data-ttu-id="5e70c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e70c-102">SYNOPSIS</span></span>
<span data-ttu-id="5e70c-103">Tworzy pulę w usłudze wsadowej.</span><span class="sxs-lookup"><span data-stu-id="5e70c-103">Creates a pool in the Batch service.</span></span>

## <span data-ttu-id="5e70c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5e70c-104">SYNTAX</span></span>

### <span data-ttu-id="5e70c-105">CloudServiceAndTargetDedicated (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5e70c-105">CloudServiceAndTargetDedicated (Default)</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-MountConfiguration <PSMountConfiguration[]>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e70c-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="5e70c-106">VirtualMachineAndTargetDedicated</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>] [-ResizeTimeout <TimeSpan>]
 [-TargetDedicatedComputeNodes <Int32>] [-TargetLowPriorityComputeNodes <Int32>]
 [-MaxTasksPerComputeNode <Int32>] [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-MountConfiguration <PSMountConfiguration[]>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e70c-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="5e70c-107">CloudServiceAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-CloudServiceConfiguration <PSCloudServiceConfiguration>] [-NetworkConfiguration <PSNetworkConfiguration>]
 [-MountConfiguration <PSMountConfiguration[]>] [-UserAccount <PSUserAccount[]>]
 -BatchContext <BatchAccountContext> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5e70c-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="5e70c-108">VirtualMachineAndAutoScale</span></span>
```
New-AzBatchPool [-Id] <String> -VirtualMachineSize <String> [-DisplayName <String>]
 [-AutoScaleEvaluationInterval <TimeSpan>] [-AutoScaleFormula <String>] [-MaxTasksPerComputeNode <Int32>]
 [-TaskSchedulingPolicy <PSTaskSchedulingPolicy>] [-Metadata <IDictionary>]
 [-InterComputeNodeCommunicationEnabled] [-StartTask <PSStartTask>]
 [-CertificateReferences <PSCertificateReference[]>]
 [-ApplicationPackageReferences <PSApplicationPackageReference[]>]
 [-ApplicationLicenses <System.Collections.Generic.List`1[System.String]>]
 [-VirtualMachineConfiguration <PSVirtualMachineConfiguration>]
 [-NetworkConfiguration <PSNetworkConfiguration>] [-MountConfiguration <PSMountConfiguration[]>]
 [-UserAccount <PSUserAccount[]>] -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e70c-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="5e70c-109">DESCRIPTION</span></span>
<span data-ttu-id="5e70c-110">Polecenie **cmdlet New-AzBatchPool** tworzy pulę w usłudze Azure Batch w ramach konta określonego przez *parametr BatchContext.*</span><span class="sxs-lookup"><span data-stu-id="5e70c-110">The **New-AzBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="5e70c-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5e70c-111">EXAMPLES</span></span>

### <span data-ttu-id="5e70c-112">Przykład 1. Tworzenie nowej puli przy użyciu zestawu parametrów TargetDedicated przy użyciu parametru CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e70c-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="5e70c-113">Pula jest skonfigurowana do korzystania z STANDARD_D1_V2 maszyn wirtualnych w wersji systemu operacyjnego dla czteroszpowiątowej rodziny.</span><span class="sxs-lookup"><span data-stu-id="5e70c-113">The pool is configured to use STANDARD_D1_V2 virtual machines with operating system version of family four.</span></span>

### <span data-ttu-id="5e70c-114">Przykład 2. Tworzenie nowej puli przy użyciu zestawu parametrów TargetDedicated przy użyciu parametru VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e70c-114">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="5e70c-115">To polecenie tworzy nową pulę o identyfikatorze MyPool przy użyciu zestawu parametrów TargetDedicated.</span><span class="sxs-lookup"><span data-stu-id="5e70c-115">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="5e70c-116">Alokacja docelowa to trzy węzły obliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="5e70c-116">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="5e70c-117">Pula jest skonfigurowana do używania STANDARD_D1_V2 maszyn wirtualnych z obrazem systemu operacyjnego Centrum danych w systemie operacyjnym Windows-2016.</span><span class="sxs-lookup"><span data-stu-id="5e70c-117">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image.</span></span>

### <span data-ttu-id="5e70c-118">Przykład 3. Tworzenie nowej puli przy użyciu zestawu parametrów Autoscale</span><span class="sxs-lookup"><span data-stu-id="5e70c-118">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="5e70c-119">To polecenie tworzy nową pulę z identyfikatorem AutoScalePool przy użyciu zestawu parametrów Autoscale.</span><span class="sxs-lookup"><span data-stu-id="5e70c-119">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="5e70c-120">Pula jest skonfigurowana do używania STANDARD_D1_V2 maszyn wirtualnych z obrazem systemu operacyjnego centrum danych w systemie Windows-2016, a docelowa liczba węzłów obliczeniowych jest ustalana na podstawie formuły Skala automatyczna.</span><span class="sxs-lookup"><span data-stu-id="5e70c-120">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="5e70c-121">Przykład 4. Tworzenie puli z węzłami w podsieci</span><span class="sxs-lookup"><span data-stu-id="5e70c-121">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="5e70c-122">Przykład 5. Tworzenie puli z niestandardowymi kontami użytkowników</span><span class="sxs-lookup"><span data-stu-id="5e70c-122">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="5e70c-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5e70c-123">PARAMETERS</span></span>

### <span data-ttu-id="5e70c-124">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="5e70c-124">-ApplicationLicenses</span></span>
<span data-ttu-id="5e70c-125">Lista licencji aplikacji, które usługa Batch udostępni w każdym węźle obliczeniowym w puli.</span><span class="sxs-lookup"><span data-stu-id="5e70c-125">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

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

### <span data-ttu-id="5e70c-126">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="5e70c-126">-ApplicationPackageReferences</span></span>
```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSApplicationPackageReference[]
Parameter Sets: (All)
Aliases: ApplicationPackageReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e70c-127">-AutoScaleEvaluationIntervalation</span><span class="sxs-lookup"><span data-stu-id="5e70c-127">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="5e70c-128">Określa czas (w minutach), który upływa, zanim rozmiar puli zostanie automatycznie dostosowany zgodnie z formułą Autoskalowanie.</span><span class="sxs-lookup"><span data-stu-id="5e70c-128">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="5e70c-129">Wartość domyślna to 15 minut, a wartość minimalna to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="5e70c-129">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="5e70c-130">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="5e70c-130">-AutoScaleFormula</span></span>
<span data-ttu-id="5e70c-131">Określa formułę automatycznego skalowania puli.</span><span class="sxs-lookup"><span data-stu-id="5e70c-131">Specifies the formula for automatically scaling the pool.</span></span>

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

### <span data-ttu-id="5e70c-132">- BatchContext</span><span class="sxs-lookup"><span data-stu-id="5e70c-132">-BatchContext</span></span>
<span data-ttu-id="5e70c-133">Określa wystąpienie **BatchAccountContext** używane przez to polecenie cmdlet do interakcji z usługą Batch.</span><span class="sxs-lookup"><span data-stu-id="5e70c-133">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="5e70c-134">Jeśli użyjesz Get-AzBatchAccount cmdlet w celu uzyskania batchAccountContext, podczas interakcji z usługą Batch będzie używane uwierzytelnianie usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="5e70c-134">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="5e70c-135">Aby zamiast tego użyć uwierzytelniania przy użyciu klucza udostępnionego, Get-AzBatchAccountKey cmdlet w celu uzyskania obiektu BatchAccountContext z wypełnionymi kluczami dostępu.</span><span class="sxs-lookup"><span data-stu-id="5e70c-135">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="5e70c-136">Podczas korzystania z uwierzytelniania za pomocą klucza udostępnionego klucz dostępu jest domyślnie używany.</span><span class="sxs-lookup"><span data-stu-id="5e70c-136">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="5e70c-137">Aby zmienić klucz do użycia, ustaw właściwość BatchAccountContext.KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="5e70c-137">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="5e70c-138">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="5e70c-138">-CertificateReferences</span></span>
<span data-ttu-id="5e70c-139">Określa certyfikaty skojarzone z pulą.</span><span class="sxs-lookup"><span data-stu-id="5e70c-139">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="5e70c-140">Usługa wsadowa instaluje certyfikaty, do których się odwołujesz, na każdym węźle obliczeniowym puli.</span><span class="sxs-lookup"><span data-stu-id="5e70c-140">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSCertificateReference[]
Parameter Sets: (All)
Aliases: CertificateReference

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e70c-141">— CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e70c-141">-CloudServiceConfiguration</span></span>
<span data-ttu-id="5e70c-142">Określa ustawienia konfiguracji puli na podstawie platformy usług Azure w chmurze.</span><span class="sxs-lookup"><span data-stu-id="5e70c-142">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

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

### <span data-ttu-id="5e70c-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e70c-143">-DefaultProfile</span></span>
<span data-ttu-id="5e70c-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e70c-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5e70c-145">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="5e70c-145">-DisplayName</span></span>
<span data-ttu-id="5e70c-146">Określa nazwę wyświetlaną puli.</span><span class="sxs-lookup"><span data-stu-id="5e70c-146">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="5e70c-147">— Identyfikator</span><span class="sxs-lookup"><span data-stu-id="5e70c-147">-Id</span></span>
<span data-ttu-id="5e70c-148">Określa identyfikator puli, która ma być tworzyć.</span><span class="sxs-lookup"><span data-stu-id="5e70c-148">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="5e70c-149">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="5e70c-149">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="5e70c-150">Wskazuje, że to polecenie cmdlet konfiguruje pulę na komunikacji bezpośredniej między dedykowanymi węzłami obliczeniowymi.</span><span class="sxs-lookup"><span data-stu-id="5e70c-150">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="5e70c-151">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="5e70c-151">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="5e70c-152">Określa maksymalną liczbę zadań, które można uruchomić w pojedynczym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="5e70c-152">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="5e70c-153">— Metadane</span><span class="sxs-lookup"><span data-stu-id="5e70c-153">-Metadata</span></span>
<span data-ttu-id="5e70c-154">Określa metadane (jako pary klucz/wartość), które mają być dodane do nowej puli.</span><span class="sxs-lookup"><span data-stu-id="5e70c-154">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="5e70c-155">Kluczem jest nazwa metadanych.</span><span class="sxs-lookup"><span data-stu-id="5e70c-155">The key is the metadata name.</span></span>
<span data-ttu-id="5e70c-156">Wartość jest wartością metadanych.</span><span class="sxs-lookup"><span data-stu-id="5e70c-156">The value is the metadata value.</span></span>

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

### <span data-ttu-id="5e70c-157">- MountConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e70c-157">-MountConfiguration</span></span>
<span data-ttu-id="5e70c-158">Lista systemów plików do instalacji na każdym węźle w puli.</span><span class="sxs-lookup"><span data-stu-id="5e70c-158">A list of file systems to mount on each node in the pool.</span></span> <span data-ttu-id="5e70c-159">Obsługuje to pliki Azure, NFS, CIFS/SMB i blobfuse.</span><span class="sxs-lookup"><span data-stu-id="5e70c-159">This supports Azure Files, NFS, CIFS/SMB, and Blobfuse.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSMountConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e70c-160">— NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e70c-160">-NetworkConfiguration</span></span>
<span data-ttu-id="5e70c-161">Konfiguracja sieci puli.</span><span class="sxs-lookup"><span data-stu-id="5e70c-161">The network configuration for the pool.</span></span>

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

### <span data-ttu-id="5e70c-162">- ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="5e70c-162">-ResizeTimeout</span></span>
<span data-ttu-id="5e70c-163">Określa przechył czasu na przydzielanie węzłów obliczeniowych do puli.</span><span class="sxs-lookup"><span data-stu-id="5e70c-163">Specifies the time-out for allocating compute nodes to the pool.</span></span>

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

### <span data-ttu-id="5e70c-164">- StartTask</span><span class="sxs-lookup"><span data-stu-id="5e70c-164">-StartTask</span></span>
<span data-ttu-id="5e70c-165">Określa specyfikację zadania rozpoczęcia dla puli.</span><span class="sxs-lookup"><span data-stu-id="5e70c-165">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="5e70c-166">Zadanie startowe jest uruchamiane, gdy węzeł obliczeniowy łączy się z pulą lub gdy węzeł obliczeniowy jest ponownie uruchamiany lub ponownie uruchamiany.</span><span class="sxs-lookup"><span data-stu-id="5e70c-166">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

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

### <span data-ttu-id="5e70c-167">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="5e70c-167">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="5e70c-168">Określa docelową liczbę dedykowanych węzłów obliczeniowych do przydzielenia puli.</span><span class="sxs-lookup"><span data-stu-id="5e70c-168">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CloudServiceAndTargetDedicated, VirtualMachineAndTargetDedicated
Aliases: TargetDedicated

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e70c-169">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="5e70c-169">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="5e70c-170">Określa docelową liczbę węzłów obliczeniowych o niskim priorytecie, które należy przydzielić do puli.</span><span class="sxs-lookup"><span data-stu-id="5e70c-170">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="5e70c-171">- TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="5e70c-171">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="5e70c-172">Określa zasady planowania zadań, na przykład typ ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="5e70c-172">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

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

### <span data-ttu-id="5e70c-173">-UserAccount</span><span class="sxs-lookup"><span data-stu-id="5e70c-173">-UserAccount</span></span>
<span data-ttu-id="5e70c-174">Lista kont użytkowników, które mają zostać utworzone w każdym węźle w puli.</span><span class="sxs-lookup"><span data-stu-id="5e70c-174">The list of user accounts to be created on each node in the pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.Models.PSUserAccount[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e70c-175">- VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="5e70c-175">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="5e70c-176">Określa ustawienia konfiguracji puli w infrastrukturze maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="5e70c-176">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

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

### <span data-ttu-id="5e70c-177">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="5e70c-177">-VirtualMachineSize</span></span>
<span data-ttu-id="5e70c-178">Określa rozmiar maszyn wirtualnych w puli.</span><span class="sxs-lookup"><span data-stu-id="5e70c-178">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="5e70c-179">Aby uzyskać więcej informacji na temat rozmiarów maszyn wirtualnych, zobacz "Rozmiary maszyn https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ wirtualnych" https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) (w witrynie platformy Microsoft Azure).</span><span class="sxs-lookup"><span data-stu-id="5e70c-179">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="5e70c-180">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e70c-180">-Confirm</span></span>
<span data-ttu-id="5e70c-181">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5e70c-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e70c-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e70c-182">-WhatIf</span></span>
<span data-ttu-id="5e70c-183">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e70c-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e70c-184">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5e70c-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e70c-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e70c-185">CommonParameters</span></span>
<span data-ttu-id="5e70c-186">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e70c-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e70c-187">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5e70c-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e70c-188">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e70c-188">INPUTS</span></span>

### <span data-ttu-id="5e70c-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="5e70c-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="5e70c-190">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e70c-190">OUTPUTS</span></span>

### <span data-ttu-id="5e70c-191">System.Void</span><span class="sxs-lookup"><span data-stu-id="5e70c-191">System.Void</span></span>

## <span data-ttu-id="5e70c-192">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5e70c-192">NOTES</span></span>

## <span data-ttu-id="5e70c-193">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e70c-193">RELATED LINKS</span></span>

[<span data-ttu-id="5e70c-194">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="5e70c-194">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="5e70c-195">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="5e70c-195">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="5e70c-196">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="5e70c-196">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="5e70c-197">Polecenia cmdlet partii platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5e70c-197">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
