---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchPool.md
ms.openlocfilehash: 3c66893875dedd5e7298b9c6239c3da7ee86212e
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98502143"
---
# <span data-ttu-id="f1443-101">New-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="f1443-101">New-AzBatchPool</span></span>

## <span data-ttu-id="f1443-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f1443-102">SYNOPSIS</span></span>
<span data-ttu-id="f1443-103">Tworzy pulę w usłudze przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="f1443-103">Creates a pool in the Batch service.</span></span>

## <span data-ttu-id="f1443-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f1443-104">SYNTAX</span></span>

### <span data-ttu-id="f1443-105">CloudServiceAndTargetDedicated (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f1443-105">CloudServiceAndTargetDedicated (Default)</span></span>
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

### <span data-ttu-id="f1443-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="f1443-106">VirtualMachineAndTargetDedicated</span></span>
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

### <span data-ttu-id="f1443-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="f1443-107">CloudServiceAndAutoScale</span></span>
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

### <span data-ttu-id="f1443-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="f1443-108">VirtualMachineAndAutoScale</span></span>
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

## <span data-ttu-id="f1443-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f1443-109">DESCRIPTION</span></span>
<span data-ttu-id="f1443-110">Polecenie cmdlet **New-AzBatchPool** tworzy pulę w usłudze Azure Batch pod kontem określonym przez parametr *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="f1443-110">The **New-AzBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="f1443-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f1443-111">EXAMPLES</span></span>

### <span data-ttu-id="f1443-112">Przykład 1. Tworzenie nowej puli przy użyciu parametru TargetDedicated ustawionego za pomocą CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1443-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="f1443-113">Pula jest skonfigurowana do używania STANDARD_D1_V2 maszyn wirtualnych z wersją z rodziny 4 w systemie operacyjnym.</span><span class="sxs-lookup"><span data-stu-id="f1443-113">The pool is configured to use STANDARD_D1_V2 virtual machines with operating system version of family four.</span></span>

### <span data-ttu-id="f1443-114">Przykład 2: Tworzenie nowej puli przy użyciu parametru TargetDedicated ustawionego za pomocą VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1443-114">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "MyPool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="f1443-115">To polecenie tworzy nową pulę o IDENTYFIKATORze moja Pula przy użyciu zestawu parametrów TargetDedicated.</span><span class="sxs-lookup"><span data-stu-id="f1443-115">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="f1443-116">Alokacja docelowa to trzy węzły obliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="f1443-116">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="f1443-117">Pula jest skonfigurowana do używania STANDARD_D1_V2 maszyn wirtualnych z obrazem systemu operacyjnego Windows-2016-Datacenter.</span><span class="sxs-lookup"><span data-stu-id="f1443-117">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image.</span></span>

### <span data-ttu-id="f1443-118">Przykład 3: Tworzenie nowej puli przy użyciu zestawu parametrów skalowania automatycznego</span><span class="sxs-lookup"><span data-stu-id="f1443-118">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="f1443-119">To polecenie tworzy nową pulę o IDENTYFIKATORze AutoScalePool przy użyciu zestawu parametrów autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="f1443-119">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="f1443-120">Pula jest skonfigurowana do korzystania z STANDARD_D1_V2 maszyn wirtualnych z obrazem systemu operacyjnego Windows-2016-Datacenter, a liczba docelowa węzłów obliczeniowych jest określana przez formułę skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="f1443-120">The pool is configured to use STANDARD_D1_V2 virtual machines with the Windows-2016-Datacenter operating system image, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="f1443-121">Przykład 4: Tworzenie puli z węzłami w podsieci</span><span class="sxs-lookup"><span data-stu-id="f1443-121">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="f1443-122">Przykład 5: Tworzenie puli z niestandardowymi kontami użytkowników</span><span class="sxs-lookup"><span data-stu-id="f1443-122">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\>$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSVirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzBatchPool -Id "AutoScalePool" -VirtualMachineSize "STANDARD_D1_V2" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="f1443-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f1443-123">PARAMETERS</span></span>

### <span data-ttu-id="f1443-124">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="f1443-124">-ApplicationLicenses</span></span>
<span data-ttu-id="f1443-125">Lista licencji na aplikacje, które usługa wsadowa będzie udostępniać w każdym węźle obliczeniowym w puli.</span><span class="sxs-lookup"><span data-stu-id="f1443-125">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

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

### <span data-ttu-id="f1443-126">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="f1443-126">-ApplicationPackageReferences</span></span>
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

### <span data-ttu-id="f1443-127">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="f1443-127">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="f1443-128">Określa czas (w minutach), po upływie którego rozmiar puli będzie automatycznie dostosowywany zgodnie z formułą skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="f1443-128">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="f1443-129">Wartość domyślna to 15 minut, a wartość minimalna to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="f1443-129">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="f1443-130">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="f1443-130">-AutoScaleFormula</span></span>
<span data-ttu-id="f1443-131">Określa formułę do automatycznego skalowania puli.</span><span class="sxs-lookup"><span data-stu-id="f1443-131">Specifies the formula for automatically scaling the pool.</span></span>

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

### <span data-ttu-id="f1443-132">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="f1443-132">-BatchContext</span></span>
<span data-ttu-id="f1443-133">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="f1443-133">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="f1443-134">Jeśli używasz polecenia cmdlet Get-AzBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="f1443-134">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="f1443-135">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzBatchAccountKey, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="f1443-135">To use shared key authentication instead, use the Get-AzBatchAccountKey cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="f1443-136">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="f1443-136">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="f1443-137">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="f1443-137">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="f1443-138">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="f1443-138">-CertificateReferences</span></span>
<span data-ttu-id="f1443-139">Określa Certyfikaty skojarzone z pulą.</span><span class="sxs-lookup"><span data-stu-id="f1443-139">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="f1443-140">Usługa przetwarzania wsadowego instaluje certyfikaty, których dotyczy odwołanie, w każdym węźle obliczeniowym puli.</span><span class="sxs-lookup"><span data-stu-id="f1443-140">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

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

### <span data-ttu-id="f1443-141">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1443-141">-CloudServiceConfiguration</span></span>
<span data-ttu-id="f1443-142">Określa ustawienia konfiguracji puli na podstawie platformy usługi Azure Cloud.</span><span class="sxs-lookup"><span data-stu-id="f1443-142">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

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

### <span data-ttu-id="f1443-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1443-143">-DefaultProfile</span></span>
<span data-ttu-id="f1443-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f1443-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1443-145">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f1443-145">-DisplayName</span></span>
<span data-ttu-id="f1443-146">Określa nazwę wyświetlaną puli.</span><span class="sxs-lookup"><span data-stu-id="f1443-146">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="f1443-147">-ID</span><span class="sxs-lookup"><span data-stu-id="f1443-147">-Id</span></span>
<span data-ttu-id="f1443-148">Określa identyfikator puli, która ma zostać utworzona.</span><span class="sxs-lookup"><span data-stu-id="f1443-148">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="f1443-149">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="f1443-149">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="f1443-150">Wskazuje, że ten aplet polecenia konfiguruje pulę w celu bezpośredniej komunikacji między dedykowanymi węzłami obliczeniowymi.</span><span class="sxs-lookup"><span data-stu-id="f1443-150">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="f1443-151">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="f1443-151">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="f1443-152">Określa maksymalną liczbę zadań, które mogą być uruchamiane w pojedynczym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="f1443-152">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="f1443-153">-Metadata</span><span class="sxs-lookup"><span data-stu-id="f1443-153">-Metadata</span></span>
<span data-ttu-id="f1443-154">Określa metadane, jako pary klucz/wartość, które mają zostać dodane do nowej puli.</span><span class="sxs-lookup"><span data-stu-id="f1443-154">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="f1443-155">Klucz to nazwa metadanych.</span><span class="sxs-lookup"><span data-stu-id="f1443-155">The key is the metadata name.</span></span>
<span data-ttu-id="f1443-156">Wartość jest wartością metadanych.</span><span class="sxs-lookup"><span data-stu-id="f1443-156">The value is the metadata value.</span></span>

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

### <span data-ttu-id="f1443-157">-MountConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1443-157">-MountConfiguration</span></span>
<span data-ttu-id="f1443-158">Lista systemów plików do zainstalowania na każdym węźle w puli.</span><span class="sxs-lookup"><span data-stu-id="f1443-158">A list of file systems to mount on each node in the pool.</span></span> <span data-ttu-id="f1443-159">Obsługuje to pliki na platformie Azure, NFS, CIFS/SMB oraz Blobfuse.</span><span class="sxs-lookup"><span data-stu-id="f1443-159">This supports Azure Files, NFS, CIFS/SMB, and Blobfuse.</span></span>

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

### <span data-ttu-id="f1443-160">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1443-160">-NetworkConfiguration</span></span>
<span data-ttu-id="f1443-161">Konfiguracja sieci dla puli.</span><span class="sxs-lookup"><span data-stu-id="f1443-161">The network configuration for the pool.</span></span>

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

### <span data-ttu-id="f1443-162">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="f1443-162">-ResizeTimeout</span></span>
<span data-ttu-id="f1443-163">Określa limit czasu przydzielania węzłów obliczeniowych do puli.</span><span class="sxs-lookup"><span data-stu-id="f1443-163">Specifies the time-out for allocating compute nodes to the pool.</span></span>

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

### <span data-ttu-id="f1443-164">-StartTask</span><span class="sxs-lookup"><span data-stu-id="f1443-164">-StartTask</span></span>
<span data-ttu-id="f1443-165">Określa specyfikację zadania rozpoczęcia puli.</span><span class="sxs-lookup"><span data-stu-id="f1443-165">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="f1443-166">Zadanie Rozpoczynanie jest uruchamiane, gdy węzeł obliczeniowy dołączy się do puli, lub gdy węzeł obliczeniowy zostanie ponownie uruchomiony lub ponownie wykonany.</span><span class="sxs-lookup"><span data-stu-id="f1443-166">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

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

### <span data-ttu-id="f1443-167">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="f1443-167">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="f1443-168">Określa liczbę docelową dedykowanych węzłów obliczeniowych do przydzielenia do puli.</span><span class="sxs-lookup"><span data-stu-id="f1443-168">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="f1443-169">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="f1443-169">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="f1443-170">Określa liczbę docelowych węzłów obliczeniowych o niskim priorytecie, które mają zostać przydzielone do puli.</span><span class="sxs-lookup"><span data-stu-id="f1443-170">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="f1443-171">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="f1443-171">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="f1443-172">Określa zasady planowania zadań, takie jak ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="f1443-172">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

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

### <span data-ttu-id="f1443-173">-Kontoużytkownika</span><span class="sxs-lookup"><span data-stu-id="f1443-173">-UserAccount</span></span>
<span data-ttu-id="f1443-174">Lista kont użytkowników, które mają zostać utworzone na każdym węźle w puli.</span><span class="sxs-lookup"><span data-stu-id="f1443-174">The list of user accounts to be created on each node in the pool.</span></span>

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

### <span data-ttu-id="f1443-175">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="f1443-175">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="f1443-176">Określa ustawienia konfiguracji puli w infrastrukturze maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="f1443-176">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

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

### <span data-ttu-id="f1443-177">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="f1443-177">-VirtualMachineSize</span></span>
<span data-ttu-id="f1443-178">Określa rozmiar maszyn wirtualnych w puli.</span><span class="sxs-lookup"><span data-stu-id="f1443-178">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="f1443-179">Aby uzyskać więcej informacji o rozmiarach maszyn wirtualnych, zobacz rozmiary dla maszyn wirtualnych https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) w witrynie platformy Microsoft Azure).</span><span class="sxs-lookup"><span data-stu-id="f1443-179">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="f1443-180">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f1443-180">-Confirm</span></span>
<span data-ttu-id="f1443-181">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1443-181">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1443-182">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1443-182">-WhatIf</span></span>
<span data-ttu-id="f1443-183">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f1443-183">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1443-184">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f1443-184">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1443-185">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1443-185">CommonParameters</span></span>
<span data-ttu-id="f1443-186">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1443-186">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1443-187">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f1443-187">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1443-188">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f1443-188">INPUTS</span></span>

### <span data-ttu-id="f1443-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="f1443-189">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="f1443-190">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f1443-190">OUTPUTS</span></span>

### <span data-ttu-id="f1443-191">System. void</span><span class="sxs-lookup"><span data-stu-id="f1443-191">System.Void</span></span>

## <span data-ttu-id="f1443-192">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f1443-192">NOTES</span></span>

## <span data-ttu-id="f1443-193">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f1443-193">RELATED LINKS</span></span>

[<span data-ttu-id="f1443-194">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="f1443-194">Get-AzBatchAccountKey</span></span>](./Get-AzBatchAccountKey.md)

[<span data-ttu-id="f1443-195">Get-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="f1443-195">Get-AzBatchPool</span></span>](./Get-AzBatchPool.md)

[<span data-ttu-id="f1443-196">Remove-AzBatchPool</span><span class="sxs-lookup"><span data-stu-id="f1443-196">Remove-AzBatchPool</span></span>](./Remove-AzBatchPool.md)

[<span data-ttu-id="f1443-197">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="f1443-197">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
