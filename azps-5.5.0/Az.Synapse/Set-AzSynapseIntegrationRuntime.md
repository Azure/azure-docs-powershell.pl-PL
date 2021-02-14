---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 715b6a52bc2f2a19dbfec3641d54752fe4321011
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188795"
---
# <span data-ttu-id="dd7c2-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="dd7c2-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="dd7c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd7c2-102">SYNOPSIS</span></span>
<span data-ttu-id="dd7c2-103">Aktualizuje środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="dd7c2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dd7c2-104">SYNTAX</span></span>

### <span data-ttu-id="dd7c2-105">SetByIntegrationRuntimeName (Domyślna)</span><span class="sxs-lookup"><span data-stu-id="dd7c2-105">SetByIntegrationRuntimeName (Default)</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd7c2-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="dd7c2-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd7c2-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="dd7c2-107">SetByParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIP <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd7c2-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="dd7c2-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd7c2-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="dd7c2-109">SetByResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd7c2-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="dd7c2-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd7c2-111">SetByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="dd7c2-111">SetByIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIP <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd7c2-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="dd7c2-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd7c2-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="dd7c2-113">DESCRIPTION</span></span>
<span data-ttu-id="dd7c2-114">Polecenie **cmdlet Set-AzSynapseIntegrationRuntime** aktualizuje środowisko uruchomieniowe integracji o określone parametry.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="dd7c2-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dd7c2-115">EXAMPLES</span></span>

### <span data-ttu-id="dd7c2-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dd7c2-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="dd7c2-117">Polecenie cmdlet aktualizuje opis środowiska uruchomieniowego integracji o nazwie "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="dd7c2-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="dd7c2-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="dd7c2-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="dd7c2-119">Polecenie cmdlet dodaje obszar roboczy, aby korzystać z udostępnionego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="dd7c2-120">Podczas `-SharedIntegrationRuntimeResourceId` używania parametru `-Type` musi być również uwzględniony.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="dd7c2-121">Zwróć uwagę, że obszar roboczy musi mieć przyznane uprawnienie do używania środowiska uruchomieniowego integracji przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="dd7c2-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd7c2-122">PARAMETERS</span></span>

### <span data-ttu-id="dd7c2-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="dd7c2-123">-AuthKey</span></span>
<span data-ttu-id="dd7c2-124">Klucz uwierzytelniania środowiska integracji z własnym hostem.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="dd7c2-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="dd7c2-126">Poświadczenia administratora bazy danych wykazu środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="dd7c2-127">-CatalogPricingTier</span></span>
<span data-ttu-id="dd7c2-128">Warstwa cenowa bazy danych wykazu w środowisku uruchomieniowym integracji.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd7c2-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="dd7c2-130">Punkt końcowy serwera bazy danych wykazu w środowisku uruchomieniowym integracji.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="dd7c2-131">-DataFlowComputeType</span></span>
<span data-ttu-id="dd7c2-132">Typ obliczenia klastra przepływu danych, który będzie wykonywać zadanie przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="dd7c2-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="dd7c2-134">Podstawowa liczba klastrów przepływów danych, które będą wykonywać zadanie przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-134">Core count of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="dd7c2-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="dd7c2-136">Ustawienie czasu do życia (w minutach) klastra przepływu danych, które będzie wykonywać zadanie przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-137">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="dd7c2-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="dd7c2-138">Nazwa Self-Hosted Integration Runtime, która jest używana jako serwer proxy.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="dd7c2-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="dd7c2-140">Nazwa usługi połączonej magazynu obiektów blob platformy Azure, która odwołuje się do magazynu danych tymczasowego, który ma być używany podczas przenoszenia danych między środowiskiem Self-Hosted i środowiskiem Azure-SSIS Integration Runtime.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="dd7c2-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="dd7c2-142">Ścieżka tymczasowego magazynu danych, która ma być używana podczas przenoszenia danych między środowiskami Self-Hosted i Azure-SSIS Integration Runtimes, w przypadku nieokreślonego kontenera domyślnego będzie używany kontener domyślny.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd7c2-143">-DefaultProfile</span></span>
<span data-ttu-id="dd7c2-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd7c2-145">— Opis</span><span class="sxs-lookup"><span data-stu-id="dd7c2-145">-Description</span></span>
<span data-ttu-id="dd7c2-146">Opis środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="dd7c2-147">— wersja</span><span class="sxs-lookup"><span data-stu-id="dd7c2-147">-Edition</span></span>
<span data-ttu-id="dd7c2-148">Wersja środowiska integracji SSIS, która może mieć domyślną wartość Standard (Standard), jeśli nie jest określona.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="dd7c2-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="dd7c2-150">Ekspresowa konfiguracja niestandardowa środowiska uruchomieniowego integracji SSIS, która może być używana do konfigurowania konfiguracji i składników innych firm bez skryptu konfiguracji niestandardowej.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

```yaml
Type: System.Collections.ArrayList
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-151">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="dd7c2-151">-Force</span></span>
<span data-ttu-id="dd7c2-152">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="dd7c2-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dd7c2-153">-InputObject</span></span>
<span data-ttu-id="dd7c2-154">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-154">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime
Parameter Sets: SetByIntegrationRuntimeObject, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="dd7c2-155">-LicenseType</span></span>
<span data-ttu-id="dd7c2-156">Typ licencji, który chcesz wybrać dla SSIS IR.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="dd7c2-157">Istnieją dwa typy: LicenseIncluded lub BasePrice.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="dd7c2-158">Jeśli masz odpowiednie kwalifikacje do skorzystania z cennika korzyści z używania hybrydowego platformy Azure (AHUB), wybierz pozycję CenaKońcowa.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="dd7c2-159">Jeśli nie, wybierz pozycję LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-159">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-160">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dd7c2-160">-Location</span></span>
<span data-ttu-id="dd7c2-161">Opis środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-161">The integration runtime description.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="dd7c2-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="dd7c2-163">Maksymalna liczba wykonywania równoległego na węzeł dla zarządzanego dedykowanego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-164">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dd7c2-164">-Name</span></span>
<span data-ttu-id="dd7c2-165">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-165">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName, SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases: IntegrationRuntimeName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="dd7c2-166">-NodeCount</span></span>
<span data-ttu-id="dd7c2-167">Liczba węzłów docelowych środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-167">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="dd7c2-168">-NodeSize</span></span>
<span data-ttu-id="dd7c2-169">Rozmiar węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-169">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-170">— PublicIP</span><span class="sxs-lookup"><span data-stu-id="dd7c2-170">-PublicIP</span></span>
<span data-ttu-id="dd7c2-171">Statyczne publiczne adresy IP, których będzie używać środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-171">The static public IP addresses which the integration runtime will use.</span></span>

```yaml
Type: System.String[]
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: PublicIPs

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd7c2-172">-ResourceGroupName</span></span>
<span data-ttu-id="dd7c2-173">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-173">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd7c2-174">-ResourceId</span></span>
<span data-ttu-id="dd7c2-175">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-175">Resource identifier of Synapse integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId, SetByLinkedIntegrationRuntimeResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="dd7c2-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="dd7c2-177">URI SAS kontenera obiektów blob platformy Azure zawierającego niestandardowy skrypt konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="dd7c2-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="dd7c2-179">Identyfikator zasobu środowiska integracji współużytkowanej we własnym środowisku uruchomieniowym.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-179">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByLinkedIntegrationRuntimeName, SetByLinkedIntegrationRuntimeParentObject, SetByLinkedIntegrationRuntimeResourceId, SetByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-180">-Subnet</span><span class="sxs-lookup"><span data-stu-id="dd7c2-180">-Subnet</span></span>
<span data-ttu-id="dd7c2-181">Nazwa podsieci w net.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-181">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-182">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="dd7c2-182">-Type</span></span>
<span data-ttu-id="dd7c2-183">Typ środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-183">The integration runtime type.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-184">- VNetId</span><span class="sxs-lookup"><span data-stu-id="dd7c2-184">-VNetId</span></span>
<span data-ttu-id="dd7c2-185">Identyfikator sieci VNet, do której dołączy środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-185">The ID of the VNet which the integration runtime will join.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByParentObject, SetByResourceId, SetByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-186">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="dd7c2-186">-WorkspaceName</span></span>
<span data-ttu-id="dd7c2-187">Nazwa obszaru roboczego aplikacji Synapse.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-187">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByIntegrationRuntimeName, SetByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-188">- WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="dd7c2-188">-WorkspaceObject</span></span>
<span data-ttu-id="dd7c2-189">obiekt wejściowy obszaru roboczego, który zwykle przechodzi przez potok.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-189">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: SetByParentObject, SetByLinkedIntegrationRuntimeParentObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dd7c2-190">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd7c2-190">-Confirm</span></span>
<span data-ttu-id="dd7c2-191">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd7c2-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd7c2-192">-WhatIf</span></span>
<span data-ttu-id="dd7c2-193">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd7c2-194">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd7c2-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd7c2-195">CommonParameters</span></span>
<span data-ttu-id="dd7c2-196">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd7c2-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd7c2-197">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd7c2-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd7c2-198">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd7c2-198">INPUTS</span></span>

### <span data-ttu-id="dd7c2-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="dd7c2-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="dd7c2-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="dd7c2-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="dd7c2-201">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="dd7c2-201">OUTPUTS</span></span>

### <span data-ttu-id="dd7c2-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="dd7c2-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="dd7c2-203">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dd7c2-203">NOTES</span></span>

## <span data-ttu-id="dd7c2-204">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd7c2-204">RELATED LINKS</span></span>
