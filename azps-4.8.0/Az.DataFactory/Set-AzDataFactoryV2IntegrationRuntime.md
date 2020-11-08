---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 0a687c1a2c21301ca61d92d7c4701d7b59d227f3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062346"
---
# <span data-ttu-id="dd5d4-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="dd5d4-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="dd5d4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dd5d4-102">SYNOPSIS</span></span>
<span data-ttu-id="dd5d4-103">Aktualizuje środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="dd5d4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dd5d4-104">SYNTAX</span></span>

### <span data-ttu-id="dd5d4-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="dd5d4-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>]
 [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-ExpressCustomSetup <ArrayList>]
 [-DataProxyIntegrationRuntimeName <String>] [-DataProxyStagingLinkedServiceName <String>]
 [-DataProxyStagingPath <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>]
 [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dd5d4-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dd5d4-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-PublicIPs <String[]>] [-DataFlowComputeType <String>] [-DataFlowCoreCount <Int32>]
 [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd5d4-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="dd5d4-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd5d4-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="dd5d4-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd5d4-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="dd5d4-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-PublicIPs <String[]>] [-DataFlowComputeType <String>]
 [-DataFlowCoreCount <Int32>] [-DataFlowTimeToLive <Int32>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-ExpressCustomSetup <ArrayList>] [-DataProxyIntegrationRuntimeName <String>]
 [-DataProxyStagingLinkedServiceName <String>] [-DataProxyStagingPath <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd5d4-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="dd5d4-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd5d4-111">Opis</span><span class="sxs-lookup"><span data-stu-id="dd5d4-111">DESCRIPTION</span></span>
<span data-ttu-id="dd5d4-112">Polecenie cmdlet Set-AzDataFactoryV2IntegrationRuntime aktualizuje środowisko uruchomieniowe integracji z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="dd5d4-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dd5d4-113">EXAMPLES</span></span>

### <span data-ttu-id="dd5d4-114">Przykład 1: Opis aktualizacji środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="dd5d4-115">Polecenie cmdlet aktualizuje Opis środowiska wykonawczego integracji o nazwie test-SelfHost-IR '.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="dd5d4-116">Przykład 2: udostępnianie samoobsługowego środowiska integracji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="dd5d4-117">Polecenie cmdlet umożliwia dodanie podajnika APD do korzystania z środowiska współdzielonej integracji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="dd5d4-118">W przypadku używania `-SharedIntegrationRuntimeResourceId` parametru `-Type` należy również uwzględnić te parametry.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="dd5d4-119">Pamiętaj, że przed uruchomieniem polecenia cmdlet należy udzielić firmie danych uprawnień do korzystania z środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="dd5d4-120">Przykład 3: Konfigurowanie Self-Hosted podczerwieni jako serwera proxy usługi Azure-SSIS IR w podajniku APD.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
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
    PublicIPs                         : 
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

<span data-ttu-id="dd5d4-121">Polecenie cmdlet Aktualizuj środowisko uruchomieniowe integracji usługi Azure-SSIS, aby użyć samodzielnego środowiska uruchomieniowego integracji jako serwera proxy danych.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="dd5d4-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dd5d4-122">PARAMETERS</span></span>

### <span data-ttu-id="dd5d4-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="dd5d4-123">-AuthKey</span></span>
<span data-ttu-id="dd5d4-124">Klucz uwierzytelniania w środowisku wykonawczym programu integracyjnego Self-host.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="dd5d4-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="dd5d4-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="dd5d4-126">Poświadczenia administratora bazy danych wykazu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="dd5d4-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="dd5d4-127">-CatalogPricingTier</span></span>
<span data-ttu-id="dd5d4-128">Warstwa cenowa bazy danych katalogu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="dd5d4-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="dd5d4-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="dd5d4-130">Punkt końcowy serwera bazy danych wykazu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="dd5d4-131">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="dd5d4-131">-DataFactoryName</span></span>
<span data-ttu-id="dd5d4-132">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-132">The data factory name.</span></span>

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

### <span data-ttu-id="dd5d4-133">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="dd5d4-133">-DataFlowComputeType</span></span>
<span data-ttu-id="dd5d4-134">Typ obliczania klastra przepływu danych, który będzie wykonywał zadanie przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-134">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="dd5d4-135">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="dd5d4-135">-DataFlowCoreCount</span></span>
<span data-ttu-id="dd5d4-136">Podstawowa liczba klastrów przepływów danych, które będą wykonywać zadanie przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-136">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="dd5d4-137">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="dd5d4-137">-DataFlowTimeToLive</span></span>
<span data-ttu-id="dd5d4-138">Czas trwania (w minutach) ustawienia klastra przepływu danych, który będzie wykonywał zadanie przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-138">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="dd5d4-139">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="dd5d4-139">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="dd5d4-140">Nazwa środowiska uruchomieniowego integracji Self-Hosted używana jako serwer proxy</span><span class="sxs-lookup"><span data-stu-id="dd5d4-140">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

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

### <span data-ttu-id="dd5d4-141">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="dd5d4-141">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="dd5d4-142">Nazwa połączonej usługi magazynu obiektów blob platformy Azure, która odwołuje się do magazynu danych przemieszczania, która ma być używana podczas przenoszenia danych między programem obsługi integracji Self-Hosted a usługą Azure-SSIS</span><span class="sxs-lookup"><span data-stu-id="dd5d4-142">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

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

### <span data-ttu-id="dd5d4-143">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="dd5d4-143">-DataProxyStagingPath</span></span>
<span data-ttu-id="dd5d4-144">Ścieżka w magazynie danych przemieszczania, która ma być używana podczas przenoszenia danych między systemem Self-Hosted i środowiskami do obsługi integracji Azure-SSIS, jeśli nie określono kontenera domyślnego, zostanie wykorzystany kontener domyślny</span><span class="sxs-lookup"><span data-stu-id="dd5d4-144">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

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

### <span data-ttu-id="dd5d4-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd5d4-145">-DefaultProfile</span></span>
<span data-ttu-id="dd5d4-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd5d4-147">— Opis</span><span class="sxs-lookup"><span data-stu-id="dd5d4-147">-Description</span></span>
<span data-ttu-id="dd5d4-148">Opis środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-148">The integration runtime description.</span></span>

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

### <span data-ttu-id="dd5d4-149">-Edition</span><span class="sxs-lookup"><span data-stu-id="dd5d4-149">-Edition</span></span>
<span data-ttu-id="dd5d4-150">Środowisko uruchomieniowe integracji wersji SSIS, które może być standardem lub Enterprise, domyślnie jest standardowe, jeśli nie zostało określone.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-150">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="dd5d4-151">-Force</span><span class="sxs-lookup"><span data-stu-id="dd5d4-151">-Force</span></span>
<span data-ttu-id="dd5d4-152">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-152">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="dd5d4-153">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="dd5d4-153">-InputObject</span></span>
<span data-ttu-id="dd5d4-154">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="dd5d4-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="dd5d4-155">-LicenseType</span></span>
<span data-ttu-id="dd5d4-156">Typ licencji, który ma zostać wybrany dla podczerwieni SSIS.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-156">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="dd5d4-157">Istnieją dwa typy: LicenseIncluded lub BasePrice.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-157">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="dd5d4-158">W przypadku kwalifikowania się do korzystania z cen usługi Azure hybrydowego użytkowania (AHUB) wybierz pozycję BasePrice.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="dd5d4-159">Jeśli nie, wybierz LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="dd5d4-160">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="dd5d4-160">-Location</span></span>
<span data-ttu-id="dd5d4-161">Lokalizacja środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-161">The integration runtime location.</span></span>

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

### <span data-ttu-id="dd5d4-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="dd5d4-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="dd5d4-163">Maksymalna liczba równoległych operacji na węzeł dla zarządzanego dedykowanego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="dd5d4-164">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dd5d4-164">-Name</span></span>
<span data-ttu-id="dd5d4-165">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="dd5d4-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="dd5d4-166">-NodeCount</span></span>
<span data-ttu-id="dd5d4-167">Liczba węzłów docelowych środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="dd5d4-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="dd5d4-168">-NodeSize</span></span>
<span data-ttu-id="dd5d4-169">Rozmiar węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="dd5d4-170">-PublicIPs</span><span class="sxs-lookup"><span data-stu-id="dd5d4-170">-PublicIPs</span></span>
<span data-ttu-id="dd5d4-171">Statyczne publiczne adresy IP, których będzie używać środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-171">The static public IP addresses which the integration runtime will use.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByIntegrationRuntimeName, ByResourceId, ByIntegrationRuntimeObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd5d4-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dd5d4-172">-ResourceGroupName</span></span>
<span data-ttu-id="dd5d4-173">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-173">The resource group name.</span></span>

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

### <span data-ttu-id="dd5d4-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd5d4-174">-ResourceId</span></span>
<span data-ttu-id="dd5d4-175">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-175">The Azure resource ID.</span></span>

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

### <span data-ttu-id="dd5d4-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="dd5d4-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="dd5d4-177">Identyfikator URI SAS kontenera obiektów blob platformy Azure zawierającego niestandardowy skrypt instalacji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="dd5d4-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="dd5d4-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="dd5d4-179">Identyfikator zasobu współużytkowanego środowiska obsługi integracji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="dd5d4-180">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="dd5d4-180">-Subnet</span></span>
<span data-ttu-id="dd5d4-181">Nazwa podsieci w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="dd5d4-182">-Type</span><span class="sxs-lookup"><span data-stu-id="dd5d4-182">-Type</span></span>
<span data-ttu-id="dd5d4-183">Typ środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="dd5d4-184">-VNetId</span><span class="sxs-lookup"><span data-stu-id="dd5d4-184">-VNetId</span></span>
<span data-ttu-id="dd5d4-185">Identyfikator sieci wirtualnej, z którą łączy się środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-185">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="dd5d4-186">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd5d4-186">-Confirm</span></span>
<span data-ttu-id="dd5d4-187">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd5d4-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd5d4-188">-WhatIf</span></span>
<span data-ttu-id="dd5d4-189">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-189">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="dd5d4-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd5d4-190">CommonParameters</span></span>
<span data-ttu-id="dd5d4-191">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd5d4-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd5d4-192">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dd5d4-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd5d4-193">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd5d4-193">INPUTS</span></span>

### <span data-ttu-id="dd5d4-194">System. String</span><span class="sxs-lookup"><span data-stu-id="dd5d4-194">System.String</span></span>

### <span data-ttu-id="dd5d4-195">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="dd5d4-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="dd5d4-196">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dd5d4-196">OUTPUTS</span></span>

### <span data-ttu-id="dd5d4-197">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="dd5d4-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="dd5d4-198">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dd5d4-198">NOTES</span></span>

## <span data-ttu-id="dd5d4-199">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd5d4-199">RELATED LINKS</span></span>

[<span data-ttu-id="dd5d4-200">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="dd5d4-200">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
