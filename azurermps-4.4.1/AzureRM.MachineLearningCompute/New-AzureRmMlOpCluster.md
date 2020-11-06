---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
ms.openlocfilehash: 222813dc78b4dd7c0118b8146a75ca4d225ce83c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549983"
---
# <span data-ttu-id="5bb36-101">New-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="5bb36-101">New-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="5bb36-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5bb36-102">SYNOPSIS</span></span>
<span data-ttu-id="5bb36-103">Tworzy nowy klaster operationalization.</span><span class="sxs-lookup"><span data-stu-id="5bb36-103">Creates a new operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5bb36-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5bb36-104">SYNTAX</span></span>

### <span data-ttu-id="5bb36-105">Utwórz nowy klaster operationalization z poziomu OperationalizationCluster definicji wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="5bb36-105">Create a new operationalization cluster from an OperationalizationCluster instance definition.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-WhatIf] [-Confirm]
```

### <span data-ttu-id="5bb36-106">Utwórz nowy klaster operationalization z parametrów wejściowych polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bb36-106">Create a new operationalization cluster from cmdlet input parameters.</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ServicePrincipalName <String>] [-ServicePrincipalSecret <String>]
 [-Description <String>] [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-GlobalServiceConfigurationAdditionalProperties <Hashtable>] [-WhatIf] [-Confirm]
```

## <span data-ttu-id="5bb36-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5bb36-107">DESCRIPTION</span></span>
<span data-ttu-id="5bb36-108">Tworzy nowy klaster operationalization.</span><span class="sxs-lookup"><span data-stu-id="5bb36-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="5bb36-109">Spowoduje to utworzenie obiektu klastra, usługi kontenera w razie potrzeby, informacji o usłudze Application Insights i rejestru kontenera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5bb36-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="5bb36-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5bb36-110">EXAMPLES</span></span>

### <span data-ttu-id="5bb36-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5bb36-111">Example 1</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="5bb36-112">Tworzy nowy klaster operationalization z usługą kontenera platformy Azure i Kubernetes jako koordynatorem.</span><span class="sxs-lookup"><span data-stu-id="5bb36-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="5bb36-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5bb36-113">Example 2</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="5bb36-114">Tworzy nowy klaster operationalization lokalnie.</span><span class="sxs-lookup"><span data-stu-id="5bb36-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="5bb36-115">Spowoduje to utworzenie rejestru kontenera platformy Azure, usług Application Insights i konta magazynu, ale nie powoduje utworzenia usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="5bb36-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="5bb36-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5bb36-116">PARAMETERS</span></span>

### <span data-ttu-id="5bb36-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="5bb36-117">-AgentCount</span></span>
<span data-ttu-id="5bb36-118">Liczba węzłów agenta w klastrze ACS.</span><span class="sxs-lookup"><span data-stu-id="5bb36-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb36-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="5bb36-119">-AgentVmSize</span></span>
<span data-ttu-id="5bb36-120">Liczba węzłów agenta w klastrze ACS.</span><span class="sxs-lookup"><span data-stu-id="5bb36-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb36-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5bb36-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="5bb36-122">Identyfikator URI z rejestru kontenera platformy Azure, który ma być używany zamiast tworzenia go.</span><span class="sxs-lookup"><span data-stu-id="5bb36-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb36-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5bb36-123">-InputObject</span></span>
<span data-ttu-id="5bb36-124">Właściwości klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="5bb36-124">The operationalization cluster properties.</span></span>

```yaml
Type: PSOperationalizationCluster
Parameter Sets: Create a new operationalization cluster from an OperationalizationCluster instance definition.
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb36-125">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="5bb36-125">-ClusterType</span></span>
<span data-ttu-id="5bb36-126">Typ klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="5bb36-126">The operationalization cluster type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb36-127">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5bb36-127">-Confirm</span></span>
<span data-ttu-id="5bb36-128">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bb36-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb36-129">— Opis</span><span class="sxs-lookup"><span data-stu-id="5bb36-129">-Description</span></span>
<span data-ttu-id="5bb36-130">Liczba węzłów głównych w klastrze usług ACS.</span><span class="sxs-lookup"><span data-stu-id="5bb36-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb36-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="5bb36-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="5bb36-132">Dodatkowe właściwości globalnej konfiguracji usługi.</span><span class="sxs-lookup"><span data-stu-id="5bb36-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: Hashtable
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb36-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="5bb36-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="5bb36-134">Element ETag konfiguracji dla aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="5bb36-134">The configuration ETag for updates.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb36-135">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5bb36-135">-Location</span></span>
<span data-ttu-id="5bb36-136">Lokalizacja klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="5bb36-136">The operationalization cluster's location.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb36-137">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="5bb36-137">-MasterCount</span></span>
<span data-ttu-id="5bb36-138">Liczba węzłów głównych w klastrze usług ACS.</span><span class="sxs-lookup"><span data-stu-id="5bb36-138">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: Int32
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb36-139">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5bb36-139">-Name</span></span>
<span data-ttu-id="5bb36-140">Nazwa klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="5bb36-140">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="5bb36-141">-Orchestratortype</span><span class="sxs-lookup"><span data-stu-id="5bb36-141">-OrchestratorType</span></span>
<span data-ttu-id="5bb36-142">Typ programu Orchestrator klastra ACS.</span><span class="sxs-lookup"><span data-stu-id="5bb36-142">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb36-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5bb36-143">-ResourceGroupName</span></span>
<span data-ttu-id="5bb36-144">Nazwa grupy zasobów dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="5bb36-144">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="5bb36-145">-ClientId</span><span class="sxs-lookup"><span data-stu-id="5bb36-145">-ClientId</span></span>
<span data-ttu-id="5bb36-146">Identyfikator podmiotu zabezpieczeń usługi Orchestrator klastra ACS.</span><span class="sxs-lookup"><span data-stu-id="5bb36-146">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb36-147">-Secret</span><span class="sxs-lookup"><span data-stu-id="5bb36-147">-Secret</span></span>
<span data-ttu-id="5bb36-148">Główny klucz tajny usługi Orchestrator klastra ACS.</span><span class="sxs-lookup"><span data-stu-id="5bb36-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb36-149">-SslCName</span><span class="sxs-lookup"><span data-stu-id="5bb36-149">-SslCName</span></span>
<span data-ttu-id="5bb36-150">Certyfikat CName dla certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="5bb36-150">The CName for the SSL certificate.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb36-151">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="5bb36-151">-SslCertificate</span></span>
<span data-ttu-id="5bb36-152">Dane certyfikatu SSL w formacie PEM zakodowane jako ciąg Base64.</span><span class="sxs-lookup"><span data-stu-id="5bb36-152">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb36-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="5bb36-153">-SslKey</span></span>
<span data-ttu-id="5bb36-154">Dane klucza SSL w formacie PEM zakodowane jako ciąg Base64.</span><span class="sxs-lookup"><span data-stu-id="5bb36-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb36-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="5bb36-155">-SslStatus</span></span>
<span data-ttu-id="5bb36-156">Stan protokołu SSL.</span><span class="sxs-lookup"><span data-stu-id="5bb36-156">SSL status.</span></span>
<span data-ttu-id="5bb36-157">Możliwe wartości to "włączone" i "wyłączone".</span><span class="sxs-lookup"><span data-stu-id="5bb36-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb36-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="5bb36-158">-StorageAccount</span></span>
<span data-ttu-id="5bb36-159">Identyfikator URI do konta magazynu, który ma zostać użyty zamiast tworzenia.</span><span class="sxs-lookup"><span data-stu-id="5bb36-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: String
Parameter Sets: Create a new operationalization cluster from cmdlet input parameters.
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bb36-160">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5bb36-160">-WhatIf</span></span>
<span data-ttu-id="5bb36-161">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5bb36-161">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5bb36-162">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5bb36-162">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="5bb36-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5bb36-163">INPUTS</span></span>

### <span data-ttu-id="5bb36-164">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5bb36-164">None</span></span>


## <span data-ttu-id="5bb36-165">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5bb36-165">OUTPUTS</span></span>

### <span data-ttu-id="5bb36-166">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="5bb36-166">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>


## <span data-ttu-id="5bb36-167">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5bb36-167">NOTES</span></span>

## <span data-ttu-id="5bb36-168">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5bb36-168">RELATED LINKS</span></span>

