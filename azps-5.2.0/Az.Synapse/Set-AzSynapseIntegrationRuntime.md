---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/set-azsynapseintegrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Set-AzSynapseIntegrationRuntime.md
ms.openlocfilehash: 715b6a52bc2f2a19dbfec3641d54752fe4321011
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333397"
---
# <span data-ttu-id="219ea-101">Set-AzSynapseIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="219ea-101">Set-AzSynapseIntegrationRuntime</span></span>

## <span data-ttu-id="219ea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="219ea-102">SYNOPSIS</span></span>
<span data-ttu-id="219ea-103">Aktualizuje środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="219ea-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="219ea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="219ea-104">SYNTAX</span></span>

### <span data-ttu-id="219ea-105">SetByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="219ea-105">SetByIntegrationRuntimeName (Default)</span></span>
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

### <span data-ttu-id="219ea-106">SetByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="219ea-106">SetByLinkedIntegrationRuntimeName</span></span>
```
Set-AzSynapseIntegrationRuntime [-ResourceGroupName <String>] -WorkspaceName <String> -Name <String>
 [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="219ea-107">SetByParentObject</span><span class="sxs-lookup"><span data-stu-id="219ea-107">SetByParentObject</span></span>
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

### <span data-ttu-id="219ea-108">SetByLinkedIntegrationRuntimeParentObject</span><span class="sxs-lookup"><span data-stu-id="219ea-108">SetByLinkedIntegrationRuntimeParentObject</span></span>
```
Set-AzSynapseIntegrationRuntime -Name <String> -WorkspaceObject <PSSynapseWorkspace> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="219ea-109">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="219ea-109">SetByResourceId</span></span>
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

### <span data-ttu-id="219ea-110">SetByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="219ea-110">SetByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzSynapseIntegrationRuntime -ResourceId <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="219ea-111">SetByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="219ea-111">SetByIntegrationRuntimeObject</span></span>
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

### <span data-ttu-id="219ea-112">SetByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="219ea-112">SetByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzSynapseIntegrationRuntime -InputObject <PSIntegrationRuntime> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="219ea-113">Opis</span><span class="sxs-lookup"><span data-stu-id="219ea-113">DESCRIPTION</span></span>
<span data-ttu-id="219ea-114">Polecenie cmdlet **Set-AzSynapseIntegrationRuntime** aktualizuje środowisko uruchomieniowe integracji z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="219ea-114">The **Set-AzSynapseIntegrationRuntime** cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="219ea-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="219ea-115">EXAMPLES</span></span>

### <span data-ttu-id="219ea-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="219ea-116">Example 1</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' -Description 'New description'
```

<span data-ttu-id="219ea-117">Polecenie cmdlet aktualizuje Opis środowiska wykonawczego integracji o nazwie test-SelfHost-IR '.</span><span class="sxs-lookup"><span data-stu-id="219ea-117">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="219ea-118">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="219ea-118">Example 2</span></span>
```powershell
PS C:\> Set-AzSynapseIntegrationRuntime -WorkspaceName ContosoWorkspace -Name 'test-selfhost-ir' `
                                        -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"
```

<span data-ttu-id="219ea-119">Polecenie cmdlet umożliwia dodanie obszaru roboczego do użycia współużytkowanego środowiska integracji.</span><span class="sxs-lookup"><span data-stu-id="219ea-119">The cmdlet adds the workspace to use the shared integration runtime.</span></span> <span data-ttu-id="219ea-120">W przypadku używania `-SharedIntegrationRuntimeResourceId` parametru `-Type` należy również uwzględnić te parametry.</span><span class="sxs-lookup"><span data-stu-id="219ea-120">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="219ea-121">Należy pamiętać, że przed uruchomieniem polecenia cmdlet należy udzielić temu obszarowi uprawnień do korzystania z środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="219ea-121">Note that the workspace need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="219ea-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="219ea-122">PARAMETERS</span></span>

### <span data-ttu-id="219ea-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="219ea-123">-AuthKey</span></span>
<span data-ttu-id="219ea-124">Klucz uwierzytelniania w środowisku wykonawczym programu integracyjnego Self-host.</span><span class="sxs-lookup"><span data-stu-id="219ea-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="219ea-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="219ea-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="219ea-126">Poświadczenia administratora bazy danych wykazu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="219ea-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="219ea-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="219ea-127">-CatalogPricingTier</span></span>
<span data-ttu-id="219ea-128">Warstwa cenowa bazy danych katalogu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="219ea-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="219ea-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="219ea-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="219ea-130">Punkt końcowy serwera bazy danych wykazu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="219ea-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="219ea-131">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="219ea-131">-DataFlowComputeType</span></span>
<span data-ttu-id="219ea-132">Typ obliczania klastra przepływu danych, który będzie wykonywał zadanie przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="219ea-132">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="219ea-133">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="219ea-133">-DataFlowCoreCount</span></span>
<span data-ttu-id="219ea-134">Podstawowa liczba klastrów przepływów danych, które będą wykonywać zadanie przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="219ea-134">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="219ea-135">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="219ea-135">-DataFlowTimeToLive</span></span>
<span data-ttu-id="219ea-136">Czas trwania (w minutach) ustawienia klastra przepływu danych, który będzie wykonywał zadanie przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="219ea-136">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="219ea-137">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="219ea-137">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="219ea-138">Nazwa środowiska uruchomieniowego integracji Self-Hosted używana jako serwer proxy.</span><span class="sxs-lookup"><span data-stu-id="219ea-138">The Self-Hosted Integration Runtime name which is used as a proxy.</span></span>

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

### <span data-ttu-id="219ea-139">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="219ea-139">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="219ea-140">Nazwa połączonej usługi magazynu obiektów blob platformy Azure odwołująca się do magazynu danych przemieszczania, która ma być używana podczas przenoszenia danych między programem integracyjnym usługi Self-Hosted i Azure-SSIS.</span><span class="sxs-lookup"><span data-stu-id="219ea-140">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime.</span></span>

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

### <span data-ttu-id="219ea-141">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="219ea-141">-DataProxyStagingPath</span></span>
<span data-ttu-id="219ea-142">Ścieżka w magazynie danych przemieszczania, która ma być używana podczas przenoszenia danych między programem do obsługi integracji usługi Self-Hosted i usługą Azure-SSIS, zostanie użyte domyślne kontener, jeśli nie określono tego elementu.</span><span class="sxs-lookup"><span data-stu-id="219ea-142">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified.</span></span>

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

### <span data-ttu-id="219ea-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="219ea-143">-DefaultProfile</span></span>
<span data-ttu-id="219ea-144">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="219ea-144">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="219ea-145">— Opis</span><span class="sxs-lookup"><span data-stu-id="219ea-145">-Description</span></span>
<span data-ttu-id="219ea-146">Opis środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="219ea-146">The integration runtime description.</span></span>

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

### <span data-ttu-id="219ea-147">-Edition</span><span class="sxs-lookup"><span data-stu-id="219ea-147">-Edition</span></span>
<span data-ttu-id="219ea-148">Środowisko uruchomieniowe integracji wersji SSIS, które może być standardem lub Enterprise, domyślnie jest standardowe, jeśli nie zostało określone.</span><span class="sxs-lookup"><span data-stu-id="219ea-148">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="219ea-149">-ExpressCustomSetup</span><span class="sxs-lookup"><span data-stu-id="219ea-149">-ExpressCustomSetup</span></span>
<span data-ttu-id="219ea-150">Niestandardowa Konfiguracja niestandardowa programu SSIS Integration Runtime, która może być używana do konfiguracji konfiguracji i składników innych firm bez niestandardowego skryptu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="219ea-150">The express custom setup for SSIS integration runtime which could be used to setup configurations and 3rd party components without custom setup script.</span></span>

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

### <span data-ttu-id="219ea-151">-Force</span><span class="sxs-lookup"><span data-stu-id="219ea-151">-Force</span></span>
<span data-ttu-id="219ea-152">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="219ea-152">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="219ea-153">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="219ea-153">-InputObject</span></span>
<span data-ttu-id="219ea-154">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="219ea-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="219ea-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="219ea-155">-LicenseType</span></span>
<span data-ttu-id="219ea-156">Typ licencji, który ma zostać wybrany dla podczerwieni SSIS.</span><span class="sxs-lookup"><span data-stu-id="219ea-156">The license type that you want to select for the SSIS IR.</span></span>
<span data-ttu-id="219ea-157">Istnieją dwa typy: LicenseIncluded lub BasePrice.</span><span class="sxs-lookup"><span data-stu-id="219ea-157">There are two types: LicenseIncluded or BasePrice.</span></span>
<span data-ttu-id="219ea-158">W przypadku kwalifikowania się do korzystania z cen usługi Azure hybrydowego użytkowania (AHUB) wybierz pozycję BasePrice.</span><span class="sxs-lookup"><span data-stu-id="219ea-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span>
<span data-ttu-id="219ea-159">Jeśli nie, wybierz LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="219ea-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="219ea-160">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="219ea-160">-Location</span></span>
<span data-ttu-id="219ea-161">Opis środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="219ea-161">The integration runtime description.</span></span>

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

### <span data-ttu-id="219ea-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="219ea-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="219ea-163">Maksymalna liczba równoległych operacji na węzeł dla zarządzanego dedykowanego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="219ea-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="219ea-164">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="219ea-164">-Name</span></span>
<span data-ttu-id="219ea-165">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="219ea-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="219ea-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="219ea-166">-NodeCount</span></span>
<span data-ttu-id="219ea-167">Liczba węzłów docelowych środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="219ea-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="219ea-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="219ea-168">-NodeSize</span></span>
<span data-ttu-id="219ea-169">Rozmiar węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="219ea-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="219ea-170">-PublicIP</span><span class="sxs-lookup"><span data-stu-id="219ea-170">-PublicIP</span></span>
<span data-ttu-id="219ea-171">Statyczne publiczne adresy IP, których będzie używać środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="219ea-171">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="219ea-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="219ea-172">-ResourceGroupName</span></span>
<span data-ttu-id="219ea-173">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="219ea-173">Resource group name.</span></span>

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

### <span data-ttu-id="219ea-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="219ea-174">-ResourceId</span></span>
<span data-ttu-id="219ea-175">Identyfikator zasobu środowiska uruchomieniowego integracji Synapse.</span><span class="sxs-lookup"><span data-stu-id="219ea-175">Resource identifier of Synapse integration runtime.</span></span>

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

### <span data-ttu-id="219ea-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="219ea-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="219ea-177">Identyfikator URI SAS kontenera obiektów blob platformy Azure zawierającego niestandardowy skrypt instalacji.</span><span class="sxs-lookup"><span data-stu-id="219ea-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="219ea-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="219ea-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="219ea-179">Identyfikator zasobu współużytkowanego środowiska obsługi integracji.</span><span class="sxs-lookup"><span data-stu-id="219ea-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="219ea-180">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="219ea-180">-Subnet</span></span>
<span data-ttu-id="219ea-181">Nazwa podsieci w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="219ea-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="219ea-182">-Type</span><span class="sxs-lookup"><span data-stu-id="219ea-182">-Type</span></span>
<span data-ttu-id="219ea-183">Typ środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="219ea-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="219ea-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="219ea-184">-VNetId</span></span>
<span data-ttu-id="219ea-185">Identyfikator sieci wirtualnej, do której zostanie dołączona środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="219ea-185">The ID of the VNet which the integration runtime will join.</span></span>

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

### <span data-ttu-id="219ea-186">-Nazwa_obszaru_roboczego</span><span class="sxs-lookup"><span data-stu-id="219ea-186">-WorkspaceName</span></span>
<span data-ttu-id="219ea-187">Nazwa obszaru roboczego Synapse.</span><span class="sxs-lookup"><span data-stu-id="219ea-187">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="219ea-188">-Workspaceobject</span><span class="sxs-lookup"><span data-stu-id="219ea-188">-WorkspaceObject</span></span>
<span data-ttu-id="219ea-189">obiekt wejściowy obszaru roboczego, zwykle przepuszczany przez rurociąg.</span><span class="sxs-lookup"><span data-stu-id="219ea-189">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="219ea-190">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="219ea-190">-Confirm</span></span>
<span data-ttu-id="219ea-191">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="219ea-191">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="219ea-192">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="219ea-192">-WhatIf</span></span>
<span data-ttu-id="219ea-193">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="219ea-193">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="219ea-194">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="219ea-194">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="219ea-195">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="219ea-195">CommonParameters</span></span>
<span data-ttu-id="219ea-196">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="219ea-196">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="219ea-197">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="219ea-197">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="219ea-198">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="219ea-198">INPUTS</span></span>

### <span data-ttu-id="219ea-199">Microsoft. Azure. Commands. Synapse. models. PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="219ea-199">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

### <span data-ttu-id="219ea-200">Microsoft. Azure. Commands. Synapse. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="219ea-200">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="219ea-201">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="219ea-201">OUTPUTS</span></span>

### <span data-ttu-id="219ea-202">Microsoft. Azure. Commands. Synapse. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="219ea-202">Microsoft.Azure.Commands.Synapse.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="219ea-203">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="219ea-203">NOTES</span></span>

## <span data-ttu-id="219ea-204">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="219ea-204">RELATED LINKS</span></span>
