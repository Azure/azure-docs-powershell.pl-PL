---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 10759ac90bf1d92243a8d706be3bbb345af4669c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998516"
---
# <span data-ttu-id="00fca-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="00fca-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="00fca-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00fca-102">SYNOPSIS</span></span>
<span data-ttu-id="00fca-103">Tworzy fabryczne dane.</span><span class="sxs-lookup"><span data-stu-id="00fca-103">Creates a data factory.</span></span>

## <span data-ttu-id="00fca-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="00fca-104">SYNTAX</span></span>

### <span data-ttu-id="00fca-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="00fca-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00fca-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="00fca-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00fca-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="00fca-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00fca-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="00fca-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00fca-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="00fca-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="00fca-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="00fca-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00fca-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="00fca-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00fca-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="00fca-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00fca-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="00fca-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="00fca-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="00fca-114">DESCRIPTION</span></span>
<span data-ttu-id="00fca-115">Polecenie **cmdlet Set-AzDataFactoryV2** tworzy grupę danych z określoną nazwą i lokalizacją grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="00fca-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="00fca-116">Wykonaj następujące operacje w następującej kolejności: — Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="00fca-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="00fca-117">— Tworzenie usług połączonych.</span><span class="sxs-lookup"><span data-stu-id="00fca-117">-- Create linked services.</span></span>
<span data-ttu-id="00fca-118">— Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="00fca-118">-- Create datasets.</span></span>
<span data-ttu-id="00fca-119">— Tworzenie potoku.</span><span class="sxs-lookup"><span data-stu-id="00fca-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="00fca-120">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="00fca-120">EXAMPLES</span></span>

### <span data-ttu-id="00fca-121">Przykład 1. Tworzenie fabryki danych</span><span class="sxs-lookup"><span data-stu-id="00fca-121">Example 1: Create a data factory</span></span>
```
PS C:\> Set-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location "WestUS"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration :
```

### <span data-ttu-id="00fca-122">Przykład 2. Tworzenie fabryki danych ze szczegółami konfiguracji ponownego obiektu przy użyciu istniejącego obiektu fabrycznego.</span><span class="sxs-lookup"><span data-stu-id="00fca-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
```
PS C:\> Get-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" | Set-AzDataFactoryV2 -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder / -ProjectName "Azure Data Factory"

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryVSTSConfiguration
```

<span data-ttu-id="00fca-123">To polecenie umożliwia utworzenie w grupie zasobów O nazwie ADF w lokalizacji EastUS fabryki danych o nazwie WikiADF z konfiguracją kontroli źródła programu Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="00fca-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="00fca-124">Przykład 3. Tworzenie fabryki danych przy użyciu szczegółów konfiguracji ponownego obiektu GitHub przy użyciu nowego obiektu fabrycznego.</span><span class="sxs-lookup"><span data-stu-id="00fca-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
```
PS C:\> New-AzDataFactoryV2 -ResourceGroupName "ADF" -Name "WikiADF" -Location 'EastUS' -HostName 'https://github.com' -AccountName msdata -RepositoryName ADFRepo -CollaborationBranch master -RootFolder /

    DataFactoryName   : WikiADF
    DataFactoryId     : /subscriptions/3e8e61b5-9a7d-4952-bfae-545ab997b9ea/resourceGroups/adf/providers/Microsoft.DataFactory/factories/wikiadf
    ResourceGroupName : ADF
    Location          : EastUS
    Tags              : {}
    Identity          : Microsoft.Azure.Management.DataFactory.Models.FactoryIdentity
    ProvisioningState : Succeeded
    RepoConfiguration : Microsoft.Azure.Management.DataFactory.Models.FactoryGitHubConfiguration
```

<span data-ttu-id="00fca-125">To polecenie umożliwia utworzenie w grupie zasobów O nazwie ADF w lokalizacji EastUS fabryki danych o nazwie WikiADF z konfiguracją kontroli źródła GitHub.</span><span class="sxs-lookup"><span data-stu-id="00fca-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="00fca-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00fca-126">PARAMETERS</span></span>

### <span data-ttu-id="00fca-127">-AccountName</span><span class="sxs-lookup"><span data-stu-id="00fca-127">-AccountName</span></span>
<span data-ttu-id="00fca-128">Nazwa konta dla konfiguracji ponownego konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="00fca-128">The account name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fca-129">— CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="00fca-129">-CollaborationBranch</span></span>
<span data-ttu-id="00fca-130">Gałąź współpracy dla konfiguracji ponownego konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="00fca-130">The collaboration branch for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fca-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00fca-131">-DefaultProfile</span></span>
<span data-ttu-id="00fca-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="00fca-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="00fca-133">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="00fca-133">-Force</span></span>
<span data-ttu-id="00fca-134">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="00fca-134">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="00fca-135">-GlobalParameterDefinition</span><span class="sxs-lookup"><span data-stu-id="00fca-135">-GlobalParameterDefinition</span></span>
<span data-ttu-id="00fca-136">Słownik zawierający parametry globalne fabryczne.</span><span class="sxs-lookup"><span data-stu-id="00fca-136">The dictionary containing the global parameters of the data factory.</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fca-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="00fca-137">-HostName</span></span>
<span data-ttu-id="00fca-138">Nazwa hosta konfiguracji ponownego repozytorium usługi GitHub.</span><span class="sxs-lookup"><span data-stu-id="00fca-138">The host name for GitHub repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fca-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="00fca-139">-InputObject</span></span>
<span data-ttu-id="00fca-140">Obiekt data factory.</span><span class="sxs-lookup"><span data-stu-id="00fca-140">The data factory object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="00fca-141">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="00fca-141">-LastCommitId</span></span>
<span data-ttu-id="00fca-142">Ostatni identyfikator zatwierdzenia dla konfiguracji ponownego konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="00fca-142">The last commit id for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fca-143">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="00fca-143">-Location</span></span>
<span data-ttu-id="00fca-144">W tym regionie zostanie utworzona fabryczna data.</span><span class="sxs-lookup"><span data-stu-id="00fca-144">The data factory is created in this region.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00fca-145">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="00fca-145">-Name</span></span>
<span data-ttu-id="00fca-146">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="00fca-146">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases: DataFactoryName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00fca-147">— Nazwa_projektu</span><span class="sxs-lookup"><span data-stu-id="00fca-147">-ProjectName</span></span>
<span data-ttu-id="00fca-148">Nazwa projektu Azure DevOps dla konfiguracji ponownego konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="00fca-148">The project name Azure DevOps for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fca-149">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="00fca-149">-RepositoryName</span></span>
<span data-ttu-id="00fca-150">Nazwa repozytorium dla konfiguracji ponownego repozytorium.</span><span class="sxs-lookup"><span data-stu-id="00fca-150">The repository name for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fca-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00fca-151">-ResourceGroupName</span></span>
<span data-ttu-id="00fca-152">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="00fca-152">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByFactoryName, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00fca-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="00fca-153">-ResourceId</span></span>
<span data-ttu-id="00fca-154">Identyfikator usługi Azure Resource Factory w wersji 2.</span><span class="sxs-lookup"><span data-stu-id="00fca-154">The Azure resource ID of V2 data factory.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig
Aliases: Id, DataFactoryId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00fca-155">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="00fca-155">-RootFolder</span></span>
<span data-ttu-id="00fca-156">Folder główny na konfigurację ponownego konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="00fca-156">The root folder for repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fca-157">— Tag</span><span class="sxs-lookup"><span data-stu-id="00fca-157">-Tag</span></span>
<span data-ttu-id="00fca-158">Tagi fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="00fca-158">The tags of the data factory.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFactoryName, ByResourceId, ByResourceIdFactoryRepoVstsConfig, ByResourceIdFactoryRepoGitConfig, ByFactoryNameFactoryRepoGitConfig, ByFactoryNameFactoryRepoVstsConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByInputObject, ByInputObjectFactoryRepoVstsConfig, ByInputObjectFactoryRepoGitConfig
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00fca-159">- TenantId</span><span class="sxs-lookup"><span data-stu-id="00fca-159">-TenantId</span></span>
<span data-ttu-id="00fca-160">Identyfikator dzierżawy konfiguracji ponownej usługi Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="00fca-160">The tenant id for Azure DevOps repo configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceIdFactoryRepoVstsConfig, ByFactoryNameFactoryRepoVstsConfig, ByInputObjectFactoryRepoVstsConfig
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="00fca-161">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="00fca-161">-Confirm</span></span>
<span data-ttu-id="00fca-162">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="00fca-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00fca-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00fca-163">-WhatIf</span></span>
<span data-ttu-id="00fca-164">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie uruchomione, ale nie uruchomi polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00fca-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="00fca-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00fca-165">CommonParameters</span></span>
<span data-ttu-id="00fca-166">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00fca-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00fca-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00fca-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00fca-168">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00fca-168">INPUTS</span></span>

### <span data-ttu-id="00fca-169">System.String</span><span class="sxs-lookup"><span data-stu-id="00fca-169">System.String</span></span>

### <span data-ttu-id="00fca-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="00fca-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="00fca-171">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="00fca-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="00fca-172">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00fca-172">OUTPUTS</span></span>

### <span data-ttu-id="00fca-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="00fca-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="00fca-174">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="00fca-174">NOTES</span></span>
<span data-ttu-id="00fca-175">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="00fca-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="00fca-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00fca-176">RELATED LINKS</span></span>

[<span data-ttu-id="00fca-177">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="00fca-177">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="00fca-178">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="00fca-178">Remove-AzDataFactoryV2</span></span>]()
