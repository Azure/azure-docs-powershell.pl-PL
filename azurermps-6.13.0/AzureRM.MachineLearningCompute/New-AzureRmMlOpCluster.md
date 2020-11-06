---
external help file: Microsoft.Azure.Commands.MachineLearningCompute.dll-Help.xml
Module Name: AzureRM.MachineLearningCompute
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.machinelearningcompute/new-azurermmlopcluster
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearningCompute/Commands.MachineLearningCompute/help/New-AzureRmMlOpCluster.md
ms.openlocfilehash: c4092d89f8b541db92737b71e534fcc1d4d917f5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545148"
---
# <span data-ttu-id="88b8f-101">New-AzureRmMlOpCluster</span><span class="sxs-lookup"><span data-stu-id="88b8f-101">New-AzureRmMlOpCluster</span></span>

## <span data-ttu-id="88b8f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="88b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="88b8f-103">Tworzy nowy klaster operationalization.</span><span class="sxs-lookup"><span data-stu-id="88b8f-103">Creates a new operationalization cluster.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88b8f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="88b8f-104">SYNTAX</span></span>

### <span data-ttu-id="88b8f-105">CreateWithInputObject</span><span class="sxs-lookup"><span data-stu-id="88b8f-105">CreateWithInputObject</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -InputObject <PSOperationalizationCluster>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88b8f-106">CreateWithParameters</span><span class="sxs-lookup"><span data-stu-id="88b8f-106">CreateWithParameters</span></span>
```
New-AzureRmMlOpCluster -ResourceGroupName <String> -Name <String> -Location <String> -ClusterType <String>
 [-OrchestratorType <String>] [-ClientId <String>] [-Secret <String>] [-Description <String>]
 [-MasterCount <Int32>] [-AgentCount <Int32>] [-AgentVmSize <String>]
 [-GlobalServiceConfigurationETag <String>] [-SslStatus <String>] [-SslCertificate <String>] [-SslKey <String>]
 [-SslCName <String>] [-StorageAccount <String>] [-AzureContainerRegistry <String>]
 [-DefaultProfile <IAzureContextContainer>] [-GlobalServiceConfigurationAdditionalProperties <Hashtable>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88b8f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="88b8f-107">DESCRIPTION</span></span>
<span data-ttu-id="88b8f-108">Tworzy nowy klaster operationalization.</span><span class="sxs-lookup"><span data-stu-id="88b8f-108">Creates a new operationalization cluster.</span></span> <span data-ttu-id="88b8f-109">Spowoduje to utworzenie obiektu klastra, usługi kontenera w razie potrzeby, informacji o usłudze Application Insights i rejestru kontenera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="88b8f-109">This will create a cluster object, a container service if needed, application insights, and an azure container registry.</span></span>

## <span data-ttu-id="88b8f-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="88b8f-110">EXAMPLES</span></span>

### <span data-ttu-id="88b8f-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="88b8f-111">Example 1</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "ACS" -OrchestratorType "Kubernetes" -ClientId "abc" -Secret "xyz"
```

<span data-ttu-id="88b8f-112">Tworzy nowy klaster operationalization z usługą kontenera platformy Azure i Kubernetes jako koordynatorem.</span><span class="sxs-lookup"><span data-stu-id="88b8f-112">Creates a new operationalization cluster with azure container service and Kubernetes as the orchestrator.</span></span>

### <span data-ttu-id="88b8f-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="88b8f-113">Example 2</span></span>
```
PS C:\> New-AzureRmMlOpCluster -ResourceGroupName my-group -Name my-cluster -Location "East US 2" -ClusterType "Local"
```

<span data-ttu-id="88b8f-114">Tworzy nowy klaster operationalization lokalnie.</span><span class="sxs-lookup"><span data-stu-id="88b8f-114">Creates a new operationalization cluster locally.</span></span> <span data-ttu-id="88b8f-115">Spowoduje to utworzenie rejestru kontenera platformy Azure, usług Application Insights i konta magazynu, ale nie powoduje utworzenia usługi kontenera.</span><span class="sxs-lookup"><span data-stu-id="88b8f-115">This creates an azure container registry, application insights, and storage account, but does not create a container service.</span></span>

## <span data-ttu-id="88b8f-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="88b8f-116">PARAMETERS</span></span>

### <span data-ttu-id="88b8f-117">-AgentCount</span><span class="sxs-lookup"><span data-stu-id="88b8f-117">-AgentCount</span></span>
<span data-ttu-id="88b8f-118">Liczba węzłów agenta w klastrze ACS.</span><span class="sxs-lookup"><span data-stu-id="88b8f-118">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-119">-AgentVmSize</span><span class="sxs-lookup"><span data-stu-id="88b8f-119">-AgentVmSize</span></span>
<span data-ttu-id="88b8f-120">Liczba węzłów agenta w klastrze ACS.</span><span class="sxs-lookup"><span data-stu-id="88b8f-120">The number of agent nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-121">-AzureContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="88b8f-121">-AzureContainerRegistry</span></span>
<span data-ttu-id="88b8f-122">Identyfikator URI z rejestru kontenera platformy Azure, który ma być używany zamiast tworzenia go.</span><span class="sxs-lookup"><span data-stu-id="88b8f-122">The URI to the azure container registry to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-123">-ClientId</span><span class="sxs-lookup"><span data-stu-id="88b8f-123">-ClientId</span></span>
<span data-ttu-id="88b8f-124">Identyfikator podmiotu zabezpieczeń usługi Orchestrator klastra ACS.</span><span class="sxs-lookup"><span data-stu-id="88b8f-124">The ACS cluster's orchestrator service principal id.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-125">-Clustertype</span><span class="sxs-lookup"><span data-stu-id="88b8f-125">-ClusterType</span></span>
<span data-ttu-id="88b8f-126">Typ klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="88b8f-126">The operationalization cluster type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88b8f-127">-DefaultProfile</span></span>
<span data-ttu-id="88b8f-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="88b8f-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88b8f-129">— Opis</span><span class="sxs-lookup"><span data-stu-id="88b8f-129">-Description</span></span>
<span data-ttu-id="88b8f-130">Liczba węzłów głównych w klastrze usług ACS.</span><span class="sxs-lookup"><span data-stu-id="88b8f-130">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-131">-GlobalServiceConfigurationAdditionalProperties</span><span class="sxs-lookup"><span data-stu-id="88b8f-131">-GlobalServiceConfigurationAdditionalProperties</span></span>
<span data-ttu-id="88b8f-132">Dodatkowe właściwości globalnej konfiguracji usługi.</span><span class="sxs-lookup"><span data-stu-id="88b8f-132">Additional properties for the global service configuration.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-133">-GlobalServiceConfigurationETag</span><span class="sxs-lookup"><span data-stu-id="88b8f-133">-GlobalServiceConfigurationETag</span></span>
<span data-ttu-id="88b8f-134">Element ETag konfiguracji dla aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="88b8f-134">The configuration ETag for updates.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="88b8f-135">-InputObject</span></span>
<span data-ttu-id="88b8f-136">Właściwości klastra operationalization.</span><span class="sxs-lookup"><span data-stu-id="88b8f-136">The operationalization cluster properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster
Parameter Sets: CreateWithInputObject
Aliases: Cluster

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-137">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="88b8f-137">-Location</span></span>
<span data-ttu-id="88b8f-138">Lokalizacja klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="88b8f-138">The operationalization cluster's location.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-139">-MasterCount</span><span class="sxs-lookup"><span data-stu-id="88b8f-139">-MasterCount</span></span>
<span data-ttu-id="88b8f-140">Liczba węzłów głównych w klastrze usług ACS.</span><span class="sxs-lookup"><span data-stu-id="88b8f-140">The number of master nodes in the ACS cluster.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="88b8f-141">-Name</span></span>
<span data-ttu-id="88b8f-142">Nazwa klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="88b8f-142">The name of the operationalization cluster.</span></span>

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

### <span data-ttu-id="88b8f-143">-Orchestratortype</span><span class="sxs-lookup"><span data-stu-id="88b8f-143">-OrchestratorType</span></span>
<span data-ttu-id="88b8f-144">Typ programu Orchestrator klastra ACS.</span><span class="sxs-lookup"><span data-stu-id="88b8f-144">The ACS cluster's orchestrator type.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-145">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88b8f-145">-ResourceGroupName</span></span>
<span data-ttu-id="88b8f-146">Nazwa grupy zasobów dla klastra usługi operationalization.</span><span class="sxs-lookup"><span data-stu-id="88b8f-146">The name of the resource group for the operationalization cluster.</span></span>

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

### <span data-ttu-id="88b8f-147">-Secret</span><span class="sxs-lookup"><span data-stu-id="88b8f-147">-Secret</span></span>
<span data-ttu-id="88b8f-148">Główny klucz tajny usługi Orchestrator klastra ACS.</span><span class="sxs-lookup"><span data-stu-id="88b8f-148">The ACS cluster's orchestrator service principal secret.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-149">-SslCertificate</span><span class="sxs-lookup"><span data-stu-id="88b8f-149">-SslCertificate</span></span>
<span data-ttu-id="88b8f-150">Dane certyfikatu SSL w formacie PEM zakodowane jako ciąg Base64.</span><span class="sxs-lookup"><span data-stu-id="88b8f-150">The SSL certificate data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-151">-SslCName</span><span class="sxs-lookup"><span data-stu-id="88b8f-151">-SslCName</span></span>
<span data-ttu-id="88b8f-152">Certyfikat CName dla certyfikatu SSL.</span><span class="sxs-lookup"><span data-stu-id="88b8f-152">The CName for the SSL certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-153">-SslKey</span><span class="sxs-lookup"><span data-stu-id="88b8f-153">-SslKey</span></span>
<span data-ttu-id="88b8f-154">Dane klucza SSL w formacie PEM zakodowane jako ciąg Base64.</span><span class="sxs-lookup"><span data-stu-id="88b8f-154">The SSL key data in PEM format encoded as base64 string.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-155">-SslStatus</span><span class="sxs-lookup"><span data-stu-id="88b8f-155">-SslStatus</span></span>
<span data-ttu-id="88b8f-156">Stan protokołu SSL.</span><span class="sxs-lookup"><span data-stu-id="88b8f-156">SSL status.</span></span>
<span data-ttu-id="88b8f-157">Możliwe wartości to "włączone" i "wyłączone".</span><span class="sxs-lookup"><span data-stu-id="88b8f-157">Possible values are 'Enabled' and 'Disabled'.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-158">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="88b8f-158">-StorageAccount</span></span>
<span data-ttu-id="88b8f-159">Identyfikator URI do konta magazynu, który ma zostać użyty zamiast tworzenia.</span><span class="sxs-lookup"><span data-stu-id="88b8f-159">The URI to the storage account to use instead of creating one.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateWithParameters
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-160">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="88b8f-160">-Confirm</span></span>
<span data-ttu-id="88b8f-161">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88b8f-161">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-162">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88b8f-162">-WhatIf</span></span>
<span data-ttu-id="88b8f-163">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="88b8f-163">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88b8f-164">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="88b8f-164">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88b8f-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88b8f-165">CommonParameters</span></span>
<span data-ttu-id="88b8f-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="88b8f-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88b8f-167">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88b8f-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88b8f-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="88b8f-168">INPUTS</span></span>

### <span data-ttu-id="88b8f-169">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="88b8f-169">None</span></span>

## <span data-ttu-id="88b8f-170">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="88b8f-170">OUTPUTS</span></span>

### <span data-ttu-id="88b8f-171">Microsoft. Azure. Commands. MachineLearningCompute. models. PSOperationalizationCluster</span><span class="sxs-lookup"><span data-stu-id="88b8f-171">Microsoft.Azure.Commands.MachineLearningCompute.Models.PSOperationalizationCluster</span></span>

## <span data-ttu-id="88b8f-172">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="88b8f-172">NOTES</span></span>

## <span data-ttu-id="88b8f-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="88b8f-173">RELATED LINKS</span></span>
