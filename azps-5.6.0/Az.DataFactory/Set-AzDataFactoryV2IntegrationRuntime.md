---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 09b0ac3083a0440b6c229da6f45bf6412817b7ea
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964938"
---
# <span data-ttu-id="a6480-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a6480-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="a6480-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6480-102">SYNOPSIS</span></span>
<span data-ttu-id="a6480-103">Aktualizuje środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="a6480-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="a6480-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a6480-104">SYNTAX</span></span>

### <span data-ttu-id="a6480-105">ByIntegrationRuntimeName (domyślna)</span><span class="sxs-lookup"><span data-stu-id="a6480-105">ByIntegrationRuntimeName (Default)</span></span>
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

### <span data-ttu-id="a6480-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="a6480-106">ByResourceId</span></span>
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

### <span data-ttu-id="a6480-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="a6480-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6480-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="a6480-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6480-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="a6480-109">ByIntegrationRuntimeObject</span></span>
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

### <span data-ttu-id="a6480-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="a6480-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6480-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="a6480-111">DESCRIPTION</span></span>
<span data-ttu-id="a6480-112">Polecenie Set-AzDataFactoryV2IntegrationRuntime cmdlet aktualizuje środowisko uruchomieniowe integracji o określone parametry.</span><span class="sxs-lookup"><span data-stu-id="a6480-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="a6480-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a6480-113">EXAMPLES</span></span>

### <span data-ttu-id="a6480-114">Przykład 1. Opis środowiska uruchomieniowego integracji aktualizacji.</span><span class="sxs-lookup"><span data-stu-id="a6480-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="a6480-115">Polecenie cmdlet aktualizuje opis środowiska uruchomieniowego integracji o nazwie "test-selfhost-ir".</span><span class="sxs-lookup"><span data-stu-id="a6480-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="a6480-116">Przykład 2. Udostępnianie środowiska integracji samoobsługowej.</span><span class="sxs-lookup"><span data-stu-id="a6480-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="a6480-117">Polecenie cmdlet dodaje ADF, aby użyć udostępnionego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="a6480-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="a6480-118">Podczas `-SharedIntegrationRuntimeResourceId` używania parametru `-Type` musi być również uwzględniony.</span><span class="sxs-lookup"><span data-stu-id="a6480-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="a6480-119">Pamiętaj, że aby można było uruchamiać polecenie cmdlet, należy przyznać aplikacji data factory uprawnienia do używania środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="a6480-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

### <span data-ttu-id="a6480-120">Przykład 3. Konfigurowanie Self-Hosted IR jako serwera proxy dla usługi Azure-SSIS IR w forsłudze ADF.</span><span class="sxs-lookup"><span data-stu-id="a6480-120">Example 3: Configure Self-Hosted IR as a proxy for Azure-SSIS IR in ADF.</span></span>
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

<span data-ttu-id="a6480-121">Aktualizacja polecenia cmdlet środowiska uruchomieniowego integracji azure-SSIS w celu używania środowiska integracji samoobsługowej jako serwera proxy danych.</span><span class="sxs-lookup"><span data-stu-id="a6480-121">The cmdlet update Azure-SSIS integration runtime to use Self-hosted integration runtime as a data proxy.</span></span>

## <span data-ttu-id="a6480-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6480-122">PARAMETERS</span></span>

### <span data-ttu-id="a6480-123">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="a6480-123">-AuthKey</span></span>
<span data-ttu-id="a6480-124">Klucz uwierzytelniania środowiska integracji samoobsługowej.</span><span class="sxs-lookup"><span data-stu-id="a6480-124">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="a6480-125">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="a6480-125">-CatalogAdminCredential</span></span>
<span data-ttu-id="a6480-126">Poświadczenia administratora bazy danych wykazu środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="a6480-126">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="a6480-127">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="a6480-127">-CatalogPricingTier</span></span>
<span data-ttu-id="a6480-128">Warstwa cenowa bazy danych wykazu w środowisku uruchomieniowym integracji.</span><span class="sxs-lookup"><span data-stu-id="a6480-128">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="a6480-129">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="a6480-129">-CatalogServerEndpoint</span></span>
<span data-ttu-id="a6480-130">Punkt końcowy serwera bazy danych wykazu w środowisku uruchomieniowym integracji.</span><span class="sxs-lookup"><span data-stu-id="a6480-130">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="a6480-131">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="a6480-131">-DataFactoryName</span></span>
<span data-ttu-id="a6480-132">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="a6480-132">The data factory name.</span></span>

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

### <span data-ttu-id="a6480-133">-DataFlowComputeType</span><span class="sxs-lookup"><span data-stu-id="a6480-133">-DataFlowComputeType</span></span>
<span data-ttu-id="a6480-134">Typ obliczenia klastra przepływu danych, który będzie wykonywać zadanie przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="a6480-134">Compute type of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="a6480-135">-DataFlowCoreCount</span><span class="sxs-lookup"><span data-stu-id="a6480-135">-DataFlowCoreCount</span></span>
<span data-ttu-id="a6480-136">Podstawowa liczba klastrów przepływów danych, które będą wykonywać zadanie przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="a6480-136">Core count of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="a6480-137">-DataFlowTimeToLive</span><span class="sxs-lookup"><span data-stu-id="a6480-137">-DataFlowTimeToLive</span></span>
<span data-ttu-id="a6480-138">Ustawienie czasu do życia (w minutach) klastra przepływu danych, które będzie wykonywać zadanie przepływu danych.</span><span class="sxs-lookup"><span data-stu-id="a6480-138">Time to live (in minutes) setting of the data flow cluster which will execute data flow job.</span></span>

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

### <span data-ttu-id="a6480-139">-DataProxyIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="a6480-139">-DataProxyIntegrationRuntimeName</span></span>
<span data-ttu-id="a6480-140">Nazwa środowiska Self-Hosted Integration Runtime, która jest używana jako serwer proxy</span><span class="sxs-lookup"><span data-stu-id="a6480-140">The Self-Hosted Integration Runtime name which is used as a proxy</span></span>

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

### <span data-ttu-id="a6480-141">-DataProxyStagingLinkedServiceName</span><span class="sxs-lookup"><span data-stu-id="a6480-141">-DataProxyStagingLinkedServiceName</span></span>
<span data-ttu-id="a6480-142">Nazwa usługi połączonej magazynu obiektów blob platformy Azure, która odwołuje się do magazynu danych tymczasowego, który ma być używany podczas przenoszenia danych między środowiskiem Self-Hosted i środowiskiem Azure-SSIS Integration Runtime</span><span class="sxs-lookup"><span data-stu-id="a6480-142">The Azure Blob Storage Linked Service name that references the staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtime</span></span>

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

### <span data-ttu-id="a6480-143">-DataProxyStagingPath</span><span class="sxs-lookup"><span data-stu-id="a6480-143">-DataProxyStagingPath</span></span>
<span data-ttu-id="a6480-144">Ścieżka w magazynie danych tymczasowego, która ma być używana podczas przenoszenia danych między środowiskami Self-Hosted i Azure-SSIS Integration Runtimes, w przypadku nieokreślonego kontenera domyślnego będzie używany kontener domyślny</span><span class="sxs-lookup"><span data-stu-id="a6480-144">The path in staging data store to be used when moving data between Self-Hosted and Azure-SSIS Integration Runtimes, a default container will be used if unspecified</span></span>

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

### <span data-ttu-id="a6480-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6480-145">-DefaultProfile</span></span>
<span data-ttu-id="a6480-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a6480-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a6480-147">— Opis</span><span class="sxs-lookup"><span data-stu-id="a6480-147">-Description</span></span>
<span data-ttu-id="a6480-148">Opis środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="a6480-148">The integration runtime description.</span></span>

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

### <span data-ttu-id="a6480-149">— wersja</span><span class="sxs-lookup"><span data-stu-id="a6480-149">-Edition</span></span>
<span data-ttu-id="a6480-150">Wersja środowiska integracji SSIS, która może mieć domyślną wersję Standard lub Enterprise (Standard), jeśli nie jest określona.</span><span class="sxs-lookup"><span data-stu-id="a6480-150">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="a6480-151">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="a6480-151">-Force</span></span>
<span data-ttu-id="a6480-152">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a6480-152">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="a6480-153">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6480-153">-InputObject</span></span>
<span data-ttu-id="a6480-154">Obiekt środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="a6480-154">The integration runtime object.</span></span>

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

### <span data-ttu-id="a6480-155">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="a6480-155">-LicenseType</span></span>
<span data-ttu-id="a6480-156">Typ licencji, który chcesz wybrać dla licencji SSIS IR.</span><span class="sxs-lookup"><span data-stu-id="a6480-156">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="a6480-157">Istnieją dwa typy: LicenseIncluded lub BasePrice.</span><span class="sxs-lookup"><span data-stu-id="a6480-157">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="a6480-158">Jeśli masz odpowiednie kwalifikacje do skorzystania z cennika korzyści z używania hybrydowego platformy Azure (AHUB), wybierz pozycję CenaKońcowa.</span><span class="sxs-lookup"><span data-stu-id="a6480-158">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="a6480-159">Jeśli nie, wybierz pozycję LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="a6480-159">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="a6480-160">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a6480-160">-Location</span></span>
<span data-ttu-id="a6480-161">Lokalizacja środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="a6480-161">The integration runtime location.</span></span>

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

### <span data-ttu-id="a6480-162">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="a6480-162">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="a6480-163">Maksymalna liczba wykonywania równoległego na węzeł dla zarządzanego dedykowanego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="a6480-163">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="a6480-164">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a6480-164">-Name</span></span>
<span data-ttu-id="a6480-165">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="a6480-165">The integration runtime name.</span></span>

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

### <span data-ttu-id="a6480-166">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="a6480-166">-NodeCount</span></span>
<span data-ttu-id="a6480-167">Liczba węzłów docelowych środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="a6480-167">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="a6480-168">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="a6480-168">-NodeSize</span></span>
<span data-ttu-id="a6480-169">Rozmiar węzła integracji środowiska uruchomieniowego.</span><span class="sxs-lookup"><span data-stu-id="a6480-169">The integration runtime node size.</span></span>

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

### <span data-ttu-id="a6480-170">— PublicIPs</span><span class="sxs-lookup"><span data-stu-id="a6480-170">-PublicIPs</span></span>
<span data-ttu-id="a6480-171">Statyczne publiczne adresy IP, których będzie używać środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="a6480-171">The static public IP addresses which the integration runtime will use.</span></span>

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

### <span data-ttu-id="a6480-172">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6480-172">-ResourceGroupName</span></span>
<span data-ttu-id="a6480-173">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a6480-173">The resource group name.</span></span>

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

### <span data-ttu-id="a6480-174">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6480-174">-ResourceId</span></span>
<span data-ttu-id="a6480-175">Identyfikator zasobu Azure.</span><span class="sxs-lookup"><span data-stu-id="a6480-175">The Azure resource ID.</span></span>

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

### <span data-ttu-id="a6480-176">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="a6480-176">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="a6480-177">URI SAS kontenera obiektów blob platformy Azure zawierającego niestandardowy skrypt konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="a6480-177">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="a6480-178">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="a6480-178">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="a6480-179">Identyfikator zasobu środowiska integracji współużytkowanej we własnym środowisku uruchomieniowym.</span><span class="sxs-lookup"><span data-stu-id="a6480-179">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="a6480-180">-Subnet</span><span class="sxs-lookup"><span data-stu-id="a6480-180">-Subnet</span></span>
<span data-ttu-id="a6480-181">Nazwa podsieci w net.</span><span class="sxs-lookup"><span data-stu-id="a6480-181">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="a6480-182">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="a6480-182">-Type</span></span>
<span data-ttu-id="a6480-183">Typ środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="a6480-183">The integration runtime type.</span></span>

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

### <span data-ttu-id="a6480-184">- VNetId</span><span class="sxs-lookup"><span data-stu-id="a6480-184">-VNetId</span></span>
<span data-ttu-id="a6480-185">Identyfikator sieci VNet, do których dołącza środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="a6480-185">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="a6480-186">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a6480-186">-Confirm</span></span>
<span data-ttu-id="a6480-187">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a6480-187">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6480-188">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6480-188">-WhatIf</span></span>
<span data-ttu-id="a6480-189">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie uruchomione, ale nie uruchomi polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6480-189">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="a6480-190">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6480-190">CommonParameters</span></span>
<span data-ttu-id="a6480-191">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6480-191">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6480-192">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6480-192">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6480-193">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6480-193">INPUTS</span></span>

### <span data-ttu-id="a6480-194">System.String</span><span class="sxs-lookup"><span data-stu-id="a6480-194">System.String</span></span>

### <span data-ttu-id="a6480-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a6480-195">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a6480-196">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6480-196">OUTPUTS</span></span>

### <span data-ttu-id="a6480-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a6480-197">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="a6480-198">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a6480-198">NOTES</span></span>

## <span data-ttu-id="a6480-199">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6480-199">RELATED LINKS</span></span>

[<span data-ttu-id="a6480-200">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="a6480-200">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
