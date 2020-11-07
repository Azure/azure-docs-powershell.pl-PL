---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 274c6cda9154348bfeffe600fd19512d1a85502d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705932"
---
# <span data-ttu-id="86ad8-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="86ad8-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="86ad8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="86ad8-102">SYNOPSIS</span></span>
<span data-ttu-id="86ad8-103">Aktualizuje środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="86ad8-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="86ad8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="86ad8-104">SYNTAX</span></span>

### <span data-ttu-id="86ad8-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="86ad8-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ad8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="86ad8-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ad8-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="86ad8-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ad8-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="86ad8-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ad8-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="86ad8-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>]  [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ad8-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="86ad8-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="86ad8-111">Opis</span><span class="sxs-lookup"><span data-stu-id="86ad8-111">DESCRIPTION</span></span>
<span data-ttu-id="86ad8-112">Polecenie cmdlet Set-AzDataFactoryV2IntegrationRuntime aktualizuje środowisko uruchomieniowe integracji z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="86ad8-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="86ad8-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="86ad8-113">EXAMPLES</span></span>

### <span data-ttu-id="86ad8-114">Przykład 1: Opis aktualizacji środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="86ad8-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="86ad8-115">Polecenie cmdlet aktualizuje Opis środowiska wykonawczego integracji o nazwie test-SelfHost-IR '.</span><span class="sxs-lookup"><span data-stu-id="86ad8-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="86ad8-116">Przykład 2: udostępnianie samoobsługowego środowiska integracji.</span><span class="sxs-lookup"><span data-stu-id="86ad8-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="86ad8-117">Polecenie cmdlet umożliwia dodanie podajnika APD do korzystania z środowiska współdzielonej integracji.</span><span class="sxs-lookup"><span data-stu-id="86ad8-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="86ad8-118">W przypadku używania `-SharedIntegrationRuntimeResourceId` parametru `-Type` należy również uwzględnić te parametry.</span><span class="sxs-lookup"><span data-stu-id="86ad8-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="86ad8-119">Pamiętaj, że przed uruchomieniem polecenia cmdlet należy udzielić firmie danych uprawnień do korzystania z środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="86ad8-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="86ad8-120">Przykład 3: Konfigurowanie Self-Hosted podczerwieni jako serwera proxy usługi Azure-SSIS IR w podajniku APD.</span><span class="sxs-lookup"><span data-stu-id="86ad8-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName testgroup `
                                           -DataFactoryName testdf `
                                           -Name SSISIRWithDataProxy `
                                           -DataProxyIntegrationRuntimeName proxySelfhostedIR `
                                           -DataProxyStagingLinkedServiceName AzureBlobStorage `
                                           -DataProxyStagingPath teststaging

    Location                          : EastUS
    NodeSize                          : Standard_D8_v3
    NodeCount                         : 1
    MaxParallelExecutionsPerNode      : 8
    CatalogServerEndpoint             : 
    CatalogAdminUserName              : 
    CatalogAdminPassword              : 
    CatalogPricingTier                : 
    VNetId                            : 
    Subnet                            : 
    State                             : Initial
    LicenseType                       : LicenseIncluded
    SetupScriptContainerSasUri        : 
    DataProxyIntegrationRuntimeName   : proxySelfhostedIR
    DataProxyStagingLinkedServiceName : AzureBlobStorage
    DataProxyStagingPath              : 
    Edition                           : Standard
    Name                              : SSISIRWithDataProxy
    Type                              : Managed
    ResourceGroupName                 : testgroup
    DataFactoryName                   : testdf
    Description                       : 
    Id                                : /subscriptions/cb715d05-3337-4640-8c43-4f943c50d06e/resourceGroups/testgroup/providers/Microsoft.DataFactory/factories/testdf/integrationruntimes/SSISIRWithDataProxy
```

<span data-ttu-id="86ad8-121">Polecenie cmdlet Aktualizuj środowisko uruchomieniowe integracji usługi Azure-SSIS, aby użyć samodzielnego środowiska uruchomieniowego integracji jako serwera proxy danych.</span><span class="sxs-lookup"><span data-stu-id="86ad8-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="86ad8-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="86ad8-122">PARAMETERS</span></span>

### <span data-ttu-id="86ad8-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="86ad8-123">-AuthKey</span></span>
<span data-ttu-id="86ad8-124">Klucz uwierzytelniania w środowisku wykonawczym programu integracyjnego Self-host.</span><span class="sxs-lookup"><span data-stu-id="86ad8-124">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="86ad8-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="86ad8-126">Poświadczenia administratora bazy danych wykazu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="86ad8-126">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="86ad8-127">-CatalogPricingTier</span></span>
<span data-ttu-id="86ad8-128">Warstwa cenowa bazy danych katalogu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="86ad8-128">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="86ad8-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="86ad8-130">Punkt końcowy serwera bazy danych wykazu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="86ad8-130">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-131">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="86ad8-131">-DataFactoryName</span></span>
<span data-ttu-id="86ad8-132">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="86ad8-132">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-133">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="86ad8-133">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="86ad8-134">Nazwa środowiska uruchomieniowego integracji Self-Hosted używana jako serwer proxy</span><span class="sxs-lookup"><span data-stu-id="86ad8-134">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-135">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="86ad8-135">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="86ad8-136">Nazwa połączonej usługi magazynu obiektów blob platformy Azure, która odwołuje się do magazynu danych przemieszczania, która ma być używana podczas przenoszenia danych między programem obsługi integracji Self-Hosted a usługą Azure-SSIS</span><span class="sxs-lookup"><span data-stu-id="86ad8-136">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-137">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="86ad8-137">-DataProxyStagingPath</span></span>
<span data-ttu-id="86ad8-138">Ścieżka w magazynie danych przemieszczania, która ma być używana podczas przenoszenia danych między systemem Self-Hosted i środowiskami do obsługi integracji Azure-SSIS, jeśli nie określono kontenera domyślnego, zostanie wykorzystany kontener domyślny</span><span class="sxs-lookup"><span data-stu-id="86ad8-138">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86ad8-139">-DefaultProfile</span></span>
<span data-ttu-id="86ad8-140">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="86ad8-140">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="86ad8-141">— Opis</span><span class="sxs-lookup"><span data-stu-id="86ad8-141">-Description</span></span>
<span data-ttu-id="86ad8-142">Opis środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="86ad8-142">The integration runtime description.</span></span>

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

### <span data-ttu-id="86ad8-143">-Edition</span><span class="sxs-lookup"><span data-stu-id="86ad8-143">-Edition</span></span>
<span data-ttu-id="86ad8-144">Środowisko uruchomieniowe integracji wersji SSIS, które może być standardem lub Enterprise, domyślnie jest standardowe, jeśli nie zostało określone.</span><span class="sxs-lookup"><span data-stu-id="86ad8-144">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-145">-Force</span><span class="sxs-lookup"><span data-stu-id="86ad8-145">-Force</span></span>
<span data-ttu-id="86ad8-146">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="86ad8-146">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="86ad8-147">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="86ad8-147">-InputObject</span></span>
<span data-ttu-id="86ad8-148">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="86ad8-148">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-149">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="86ad8-149">-LicenseType</span></span>
<span data-ttu-id="86ad8-150">Typ licencji, który ma zostać wybrany dla podczerwieni SSIS.</span><span class="sxs-lookup"><span data-stu-id="86ad8-150">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="86ad8-151">Istnieją dwa typy: LicenseIncluded lub BasePrice.</span><span class="sxs-lookup"><span data-stu-id="86ad8-151">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="86ad8-152">W przypadku kwalifikowania się do korzystania z cen usługi Azure hybrydowego użytkowania (AHUB) wybierz pozycję BasePrice.</span><span class="sxs-lookup"><span data-stu-id="86ad8-152">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="86ad8-153">Jeśli nie, wybierz LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="86ad8-153">If not, please select LicenseIncluded.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-154">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="86ad8-154">-Location</span></span>
<span data-ttu-id="86ad8-155">Lokalizacja środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="86ad8-155">The integration runtime location.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-156">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="86ad8-156">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="86ad8-157">Maksymalna liczba równoległych operacji na węzeł dla zarządzanego dedykowanego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="86ad8-157">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-158">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="86ad8-158">-Name</span></span>
<span data-ttu-id="86ad8-159">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="86ad8-159">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-160">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="86ad8-160">-NodeCount</span></span>
<span data-ttu-id="86ad8-161">Liczba węzłów docelowych środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="86ad8-161">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-162">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="86ad8-162">-NodeSize</span></span>
<span data-ttu-id="86ad8-163">Rozmiar węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="86ad8-163">The integration runtime node size.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-164">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86ad8-164">-ResourceGroupName</span></span>
<span data-ttu-id="86ad8-165">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="86ad8-165">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByLinkedIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-166">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86ad8-166">-ResourceId</span></span>
<span data-ttu-id="86ad8-167">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="86ad8-167">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByLinkedIntegrationRuntimeResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-168">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="86ad8-168">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="86ad8-169">Identyfikator URI SAS kontenera obiektów blob platformy Azure zawierającego niestandardowy skrypt instalacji.</span><span class="sxs-lookup"><span data-stu-id="86ad8-169">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-170">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="86ad8-170">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="86ad8-171">Identyfikator zasobu współużytkowanego środowiska obsługi integracji.</span><span class="sxs-lookup"><span data-stu-id="86ad8-171">The resource id of the shared self-hosted integration runtime.</span></span>

```yaml
Type: System.String
Parameter Sets: ByLinkedIntegrationRuntimeResourceId, ByLinkedIntegrationRuntimeName, ByLinkedIntegrationRuntimeObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-172">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="86ad8-172">-Subnet</span></span>
<span data-ttu-id="86ad8-173">Nazwa podsieci w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="86ad8-173">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-174">-Type</span><span class="sxs-lookup"><span data-stu-id="86ad8-174">-Type</span></span>
<span data-ttu-id="86ad8-175">Typ środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="86ad8-175">The integration runtime type.</span></span>

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

### <span data-ttu-id="86ad8-176">-VNetId</span><span class="sxs-lookup"><span data-stu-id="86ad8-176">-VNetId</span></span>
<span data-ttu-id="86ad8-177">Identyfikator sieci wirtualnej, z którą łączy się środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="86ad8-177">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ad8-178">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="86ad8-178">-Confirm</span></span>
<span data-ttu-id="86ad8-179">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86ad8-179">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86ad8-180">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86ad8-180">-WhatIf</span></span>
<span data-ttu-id="86ad8-181">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="86ad8-181">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="86ad8-182">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ad8-182">CommonParameters</span></span>
<span data-ttu-id="86ad8-183">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="86ad8-183">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ad8-184">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="86ad8-184">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ad8-185">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="86ad8-185">INPUTS</span></span>

### <span data-ttu-id="86ad8-186">System. String</span><span class="sxs-lookup"><span data-stu-id="86ad8-186">System.String</span></span>

### <span data-ttu-id="86ad8-187">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="86ad8-187">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="86ad8-188">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="86ad8-188">OUTPUTS</span></span>

### <span data-ttu-id="86ad8-189">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="86ad8-189">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="86ad8-190">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="86ad8-190">NOTES</span></span>

## <span data-ttu-id="86ad8-191">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="86ad8-191">RELATED LINKS</span></span>

[<span data-ttu-id="86ad8-192">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="86ad8-192">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
