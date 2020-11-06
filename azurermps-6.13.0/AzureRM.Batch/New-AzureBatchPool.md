---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: C71C486E-34EB-42B5-B38A-D85B7DAA2F74
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurebatchpool
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureBatchPool.md
ms.openlocfilehash: c401e5b4a85d8c994e96d77f39d646dabb74e02d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541935"
---
# <span data-ttu-id="7a872-101">New-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="7a872-101">New-AzureBatchPool</span></span>

## <span data-ttu-id="7a872-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a872-102">SYNOPSIS</span></span>
<span data-ttu-id="7a872-103">Tworzy pulę w usłudze przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="7a872-103">Creates a pool in the Batch service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7a872-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a872-104">SYNTAX</span></span>

### <span data-ttu-id="7a872-105">CloudServiceAndTargetDedicated (domyślny)</span><span class="sxs-lookup"><span data-stu-id="7a872-105">CloudServiceAndTargetDedicated (Default)</span></span>
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

### <span data-ttu-id="7a872-106">VirtualMachineAndTargetDedicated</span><span class="sxs-lookup"><span data-stu-id="7a872-106">VirtualMachineAndTargetDedicated</span></span>
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

### <span data-ttu-id="7a872-107">CloudServiceAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="7a872-107">CloudServiceAndAutoScale</span></span>
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

### <span data-ttu-id="7a872-108">VirtualMachineAndAutoScale</span><span class="sxs-lookup"><span data-stu-id="7a872-108">VirtualMachineAndAutoScale</span></span>
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

## <span data-ttu-id="7a872-109">Opis</span><span class="sxs-lookup"><span data-stu-id="7a872-109">DESCRIPTION</span></span>
<span data-ttu-id="7a872-110">Polecenie cmdlet **New-AzureBatchPool** tworzy pulę w usłudze Azure Batch pod kontem określonym przez parametr *BatchContext* .</span><span class="sxs-lookup"><span data-stu-id="7a872-110">The **New-AzureBatchPool** cmdlet creates a pool in the Azure Batch service under the account specified by the *BatchContext* parameter.</span></span>

## <span data-ttu-id="7a872-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a872-111">EXAMPLES</span></span>

### <span data-ttu-id="7a872-112">Przykład 1. Tworzenie nowej puli przy użyciu parametru TargetDedicated ustawionego za pomocą CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a872-112">Example 1: Create a new pool using the TargetDedicated parameter set using CloudServiceConfiguration</span></span>
```
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSCloudServiceConfiguration" -ArgumentList @(4,"*")
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -CloudServiceConfiguration $configuration  -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

### <span data-ttu-id="7a872-113">Przykład 2: Tworzenie nowej puli przy użyciu parametru TargetDedicated ustawionego za pomocą VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a872-113">Example 2: Create a new pool using the TargetDedicated parameter set using VirtualMachineConfiguration</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzureBatchPool -Id "MyPool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -BatchContext $Context
```

<span data-ttu-id="7a872-114">To polecenie tworzy nową pulę o IDENTYFIKATORze moja Pula przy użyciu zestawu parametrów TargetDedicated.</span><span class="sxs-lookup"><span data-stu-id="7a872-114">This command creates a new pool with ID MyPool using the TargetDedicated parameter set.</span></span>
<span data-ttu-id="7a872-115">Alokacja docelowa to trzy węzły obliczeniowe.</span><span class="sxs-lookup"><span data-stu-id="7a872-115">The target allocation is three compute nodes.</span></span>
<span data-ttu-id="7a872-116">Pula jest skonfigurowana w celu używania małych maszyn wirtualnych z najnowszą wersją systemu operacyjnego rodziny 4.</span><span class="sxs-lookup"><span data-stu-id="7a872-116">The pool is configured to use small virtual machines imaged with the latest operating system version of family four.</span></span>

### <span data-ttu-id="7a872-117">Przykład 3: Tworzenie nowej puli przy użyciu zestawu parametrów skalowania automatycznego</span><span class="sxs-lookup"><span data-stu-id="7a872-117">Example 3: Create a new pool using the AutoScale parameter set</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -AutoScaleFormula '$TargetDedicated=2;' -BatchContext $Context
```

<span data-ttu-id="7a872-118">To polecenie tworzy nową pulę o IDENTYFIKATORze AutoScalePool przy użyciu zestawu parametrów autoskalowania.</span><span class="sxs-lookup"><span data-stu-id="7a872-118">This command creates a new pool with ID AutoScalePool using the AutoScale parameter set.</span></span>
<span data-ttu-id="7a872-119">Pula jest skonfigurowana w celu używania małych maszyn wirtualnych z najnowszą wersją systemu operacyjnego rodziny 4, a liczba docelowa węzłów obliczeniowych jest określona przez formułę skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="7a872-119">The pool is configured to use small virtual machines imaged with the latest operating system version of family four, and the target number of compute nodes are determined by the Autoscale formula.</span></span>

### <span data-ttu-id="7a872-120">Przykład 4: Tworzenie puli z węzłami w podsieci</span><span class="sxs-lookup"><span data-stu-id="7a872-120">Example 4: Create a pool with nodes in a subnet</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$networkConfig = New-Object Microsoft.Azure.Commands.Batch.Models.PSNetworkConfiguration
PS C:\>$networkConfig.SubnetId = "/subscriptions/{subscription}/resourceGroups/{group}/providers/{provider}/virtualNetworks/{network}/subnets/{subnet}"
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -NetworkConfiguration $networkConfig -BatchContext $Context
```

### <span data-ttu-id="7a872-121">Przykład 5: Tworzenie puli z niestandardowymi kontami użytkowników</span><span class="sxs-lookup"><span data-stu-id="7a872-121">Example 5: Create a pool with custom user accounts</span></span>
```
PS C:\$imageReference = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.PSImageReference" -ArgumentList @("WindowsServer", "MicrosoftWindowsServer", "2016-Datacenter", "*")
PS C:\>$configuration = New-Object -TypeName "Microsoft.Azure.Commands.Batch.Models.VirtualMachineConfiguration" -ArgumentList @($imageReference, "batch.node.windows amd64")
PS C:\>$userAccount = New-Object Microsoft.Azure.Commands.Batch.Models.PSUserAccount -ArgumentList @("myaccount", "mypassword")
PS C:\>New-AzureBatchPool -Id "AutoScalePool" -VirtualMachineSize "Small" -VirtualMachineConfiguration $configuration -TargetDedicatedComputeNodes 3 -UserAccount $userAccount
```

## <span data-ttu-id="7a872-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a872-122">PARAMETERS</span></span>

### <span data-ttu-id="7a872-123">-ApplicationLicenses</span><span class="sxs-lookup"><span data-stu-id="7a872-123">-ApplicationLicenses</span></span>
<span data-ttu-id="7a872-124">Lista licencji na aplikacje, które usługa wsadowa będzie udostępniać w każdym węźle obliczeniowym w puli.</span><span class="sxs-lookup"><span data-stu-id="7a872-124">The list of application licenses the Batch service will make available on each compute node in the pool.</span></span>

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

### <span data-ttu-id="7a872-125">-ApplicationPackageReferences</span><span class="sxs-lookup"><span data-stu-id="7a872-125">-ApplicationPackageReferences</span></span>
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

### <span data-ttu-id="7a872-126">-AutoScaleEvaluationInterval</span><span class="sxs-lookup"><span data-stu-id="7a872-126">-AutoScaleEvaluationInterval</span></span>
<span data-ttu-id="7a872-127">Określa czas (w minutach), po upływie którego rozmiar puli będzie automatycznie dostosowywany zgodnie z formułą skalowania automatycznego.</span><span class="sxs-lookup"><span data-stu-id="7a872-127">Specifies the amount of time, in minutes, that elapses before the pool size is automatically adjusted according to the AutoScale formula.</span></span>
<span data-ttu-id="7a872-128">Wartość domyślna to 15 minut, a wartość minimalna to 5 minut.</span><span class="sxs-lookup"><span data-stu-id="7a872-128">The default value is 15 minutes, and the minimum value is 5 minutes.</span></span>

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

### <span data-ttu-id="7a872-129">-AutoScaleFormula</span><span class="sxs-lookup"><span data-stu-id="7a872-129">-AutoScaleFormula</span></span>
<span data-ttu-id="7a872-130">Określa formułę do automatycznego skalowania puli.</span><span class="sxs-lookup"><span data-stu-id="7a872-130">Specifies the formula for automatically scaling the pool.</span></span>

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

### <span data-ttu-id="7a872-131">-BatchContext</span><span class="sxs-lookup"><span data-stu-id="7a872-131">-BatchContext</span></span>
<span data-ttu-id="7a872-132">Określa wystąpienie **BatchAccountContext** , którego używa polecenie cmdlet w celu interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="7a872-132">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="7a872-133">Jeśli używasz polecenia cmdlet Get-AzureRmBatchAccount, aby uzyskać BatchAccountContext, uwierzytelnianie usługi Azure Active Directory zostanie użyte podczas interakcji z usługą przetwarzania wsadowego.</span><span class="sxs-lookup"><span data-stu-id="7a872-133">If you use the Get-AzureRmBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="7a872-134">Aby zamiast tego użyć uwierzytelniania opartego na kluczu udostępnionym, użyj polecenia cmdlet Get-AzureRmBatchAccountKeys, aby uzyskać obiekt BatchAccountContext z wypełnionymi klawiszami dostępu.</span><span class="sxs-lookup"><span data-stu-id="7a872-134">To use shared key authentication instead, use the Get-AzureRmBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="7a872-135">W przypadku korzystania z uwierzytelniania za pomocą klucza udostępnionego domyślnie jest używany podstawowy klucz dostępu.</span><span class="sxs-lookup"><span data-stu-id="7a872-135">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="7a872-136">Aby zmienić klucz, który ma być używany, ustaw właściwość BatchAccountContext. KeyInUse.</span><span class="sxs-lookup"><span data-stu-id="7a872-136">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

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

### <span data-ttu-id="7a872-137">-CertificateReferences</span><span class="sxs-lookup"><span data-stu-id="7a872-137">-CertificateReferences</span></span>
<span data-ttu-id="7a872-138">Określa Certyfikaty skojarzone z pulą.</span><span class="sxs-lookup"><span data-stu-id="7a872-138">Specifies certificates associated with the pool.</span></span>
<span data-ttu-id="7a872-139">Usługa przetwarzania wsadowego instaluje certyfikaty, których dotyczy odwołanie, w każdym węźle obliczeniowym puli.</span><span class="sxs-lookup"><span data-stu-id="7a872-139">The Batch service installs the referenced certificates on each compute node of the pool.</span></span>

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

### <span data-ttu-id="7a872-140">-CloudServiceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a872-140">-CloudServiceConfiguration</span></span>
<span data-ttu-id="7a872-141">Określa ustawienia konfiguracji puli na podstawie platformy usługi Azure Cloud.</span><span class="sxs-lookup"><span data-stu-id="7a872-141">Specifies configuration settings for a pool based on the Azure cloud service platform.</span></span>

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

### <span data-ttu-id="7a872-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a872-142">-DefaultProfile</span></span>
<span data-ttu-id="7a872-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a872-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7a872-144">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="7a872-144">-DisplayName</span></span>
<span data-ttu-id="7a872-145">Określa nazwę wyświetlaną puli.</span><span class="sxs-lookup"><span data-stu-id="7a872-145">Specifies the display name of the pool.</span></span>

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

### <span data-ttu-id="7a872-146">-ID</span><span class="sxs-lookup"><span data-stu-id="7a872-146">-Id</span></span>
<span data-ttu-id="7a872-147">Określa identyfikator puli, która ma zostać utworzona.</span><span class="sxs-lookup"><span data-stu-id="7a872-147">Specifies the ID of the pool to create.</span></span>

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

### <span data-ttu-id="7a872-148">-InterComputeNodeCommunicationEnabled</span><span class="sxs-lookup"><span data-stu-id="7a872-148">-InterComputeNodeCommunicationEnabled</span></span>
<span data-ttu-id="7a872-149">Wskazuje, że ten aplet polecenia konfiguruje pulę w celu bezpośredniej komunikacji między dedykowanymi węzłami obliczeniowymi.</span><span class="sxs-lookup"><span data-stu-id="7a872-149">Indicates that this cmdlet sets up the pool for direct communication between dedicated compute nodes.</span></span>

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

### <span data-ttu-id="7a872-150">-MaxTasksPerComputeNode</span><span class="sxs-lookup"><span data-stu-id="7a872-150">-MaxTasksPerComputeNode</span></span>
<span data-ttu-id="7a872-151">Określa maksymalną liczbę zadań, które mogą być uruchamiane w pojedynczym węźle obliczeniowym.</span><span class="sxs-lookup"><span data-stu-id="7a872-151">Specifies the maximum number of tasks that can run on a single compute node.</span></span>

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

### <span data-ttu-id="7a872-152">-Metadata</span><span class="sxs-lookup"><span data-stu-id="7a872-152">-Metadata</span></span>
<span data-ttu-id="7a872-153">Określa metadane, jako pary klucz/wartość, które mają zostać dodane do nowej puli.</span><span class="sxs-lookup"><span data-stu-id="7a872-153">Specifies the metadata, as key/value pairs, to add to the new pool.</span></span>
<span data-ttu-id="7a872-154">Klucz to nazwa metadanych.</span><span class="sxs-lookup"><span data-stu-id="7a872-154">The key is the metadata name.</span></span>
<span data-ttu-id="7a872-155">Wartość jest wartością metadanych.</span><span class="sxs-lookup"><span data-stu-id="7a872-155">The value is the metadata value.</span></span>

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

### <span data-ttu-id="7a872-156">-NetworkConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a872-156">-NetworkConfiguration</span></span>
<span data-ttu-id="7a872-157">Konfiguracja sieci dla puli.</span><span class="sxs-lookup"><span data-stu-id="7a872-157">The network configuration for the pool.</span></span>

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

### <span data-ttu-id="7a872-158">-ResizeTimeout</span><span class="sxs-lookup"><span data-stu-id="7a872-158">-ResizeTimeout</span></span>
<span data-ttu-id="7a872-159">Określa limit czasu przydzielania węzłów obliczeniowych do puli.</span><span class="sxs-lookup"><span data-stu-id="7a872-159">Specifies the time-out for allocating compute nodes to the pool.</span></span>

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

### <span data-ttu-id="7a872-160">-StartTask</span><span class="sxs-lookup"><span data-stu-id="7a872-160">-StartTask</span></span>
<span data-ttu-id="7a872-161">Określa specyfikację zadania rozpoczęcia puli.</span><span class="sxs-lookup"><span data-stu-id="7a872-161">Specifies the start task specification for the pool.</span></span>
<span data-ttu-id="7a872-162">Zadanie Rozpoczynanie jest uruchamiane, gdy węzeł obliczeniowy dołączy się do puli, lub gdy węzeł obliczeniowy zostanie ponownie uruchomiony lub ponownie wykonany.</span><span class="sxs-lookup"><span data-stu-id="7a872-162">The start task is run when a compute node joins the pool, or when the compute node is rebooted or reimaged.</span></span>

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

### <span data-ttu-id="7a872-163">-TargetDedicatedComputeNodes</span><span class="sxs-lookup"><span data-stu-id="7a872-163">-TargetDedicatedComputeNodes</span></span>
<span data-ttu-id="7a872-164">Określa liczbę docelową dedykowanych węzłów obliczeniowych do przydzielenia do puli.</span><span class="sxs-lookup"><span data-stu-id="7a872-164">Specifies the target number of dedicated compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="7a872-165">-TargetLowPriorityComputeNodes</span><span class="sxs-lookup"><span data-stu-id="7a872-165">-TargetLowPriorityComputeNodes</span></span>
<span data-ttu-id="7a872-166">Określa liczbę docelowych węzłów obliczeniowych o niskim priorytecie, które mają zostać przydzielone do puli.</span><span class="sxs-lookup"><span data-stu-id="7a872-166">Specifies the target number of low-priority compute nodes to allocate to the pool.</span></span>

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

### <span data-ttu-id="7a872-167">-TaskSchedulingPolicy</span><span class="sxs-lookup"><span data-stu-id="7a872-167">-TaskSchedulingPolicy</span></span>
<span data-ttu-id="7a872-168">Określa zasady planowania zadań, takie jak ComputeNodeFillType.</span><span class="sxs-lookup"><span data-stu-id="7a872-168">Specifies the task scheduling policy, such as the ComputeNodeFillType.</span></span>

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

### <span data-ttu-id="7a872-169">-Kontoużytkownika</span><span class="sxs-lookup"><span data-stu-id="7a872-169">-UserAccount</span></span>
<span data-ttu-id="7a872-170">Lista kont użytkowników, które mają zostać utworzone na każdym węźle w puli.</span><span class="sxs-lookup"><span data-stu-id="7a872-170">The list of user accounts to be created on each node in the pool.</span></span>

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

### <span data-ttu-id="7a872-171">-VirtualMachineConfiguration</span><span class="sxs-lookup"><span data-stu-id="7a872-171">-VirtualMachineConfiguration</span></span>
<span data-ttu-id="7a872-172">Określa ustawienia konfiguracji puli w infrastrukturze maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="7a872-172">Specifies configuration settings for a pool on the virtual machines infrastructure.</span></span>

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

### <span data-ttu-id="7a872-173">-VirtualMachineSize</span><span class="sxs-lookup"><span data-stu-id="7a872-173">-VirtualMachineSize</span></span>
<span data-ttu-id="7a872-174">Określa rozmiar maszyn wirtualnych w puli.</span><span class="sxs-lookup"><span data-stu-id="7a872-174">Specifies the size of the virtual machines in the pool.</span></span>
<span data-ttu-id="7a872-175">Aby uzyskać więcej informacji o rozmiarach maszyn wirtualnych, zobacz rozmiary dla maszyn wirtualnych https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ ( https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) w witrynie platformy Microsoft Azure).</span><span class="sxs-lookup"><span data-stu-id="7a872-175">For more information about virtual machine sizes, see Sizes for virtual machineshttps://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/ (https://azure.microsoft.com/en-us/documentation/articles/virtual-machines-size-specs/) in the Microsoft Azure site.</span></span>

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

### <span data-ttu-id="7a872-176">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a872-176">-Confirm</span></span>
<span data-ttu-id="7a872-177">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a872-177">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a872-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a872-178">-WhatIf</span></span>
<span data-ttu-id="7a872-179">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a872-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7a872-180">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7a872-180">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a872-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a872-181">CommonParameters</span></span>
<span data-ttu-id="7a872-182">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a872-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a872-183">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7a872-183">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a872-184">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a872-184">INPUTS</span></span>

### <span data-ttu-id="7a872-185">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="7a872-185">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>
<span data-ttu-id="7a872-186">Parametry: BatchContext (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7a872-186">Parameters: BatchContext (ByValue)</span></span>

## <span data-ttu-id="7a872-187">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a872-187">OUTPUTS</span></span>

### <span data-ttu-id="7a872-188">System. void</span><span class="sxs-lookup"><span data-stu-id="7a872-188">System.Void</span></span>

## <span data-ttu-id="7a872-189">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a872-189">NOTES</span></span>

## <span data-ttu-id="7a872-190">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a872-190">RELATED LINKS</span></span>

[<span data-ttu-id="7a872-191">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="7a872-191">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)

[<span data-ttu-id="7a872-192">Get-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="7a872-192">Get-AzureBatchPool</span></span>](./Get-AzureBatchPool.md)

[<span data-ttu-id="7a872-193">Remove-AzureBatchPool</span><span class="sxs-lookup"><span data-stu-id="7a872-193">Remove-AzureBatchPool</span></span>](./Remove-AzureBatchPool.md)

[<span data-ttu-id="7a872-194">Polecenia cmdlet usługi Azure Batch</span><span class="sxs-lookup"><span data-stu-id="7a872-194">Azure Batch Cmdlets</span></span>](./AzureRM.Batch.md)


