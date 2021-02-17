---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 5020ddeccc755ef52bf7410d61eb57b637d261bf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194826"
---
# <span data-ttu-id="2593c-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2593c-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="2593c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2593c-102">SYNOPSIS</span></span>
<span data-ttu-id="2593c-103">Tworzy fabryczne dane.</span><span class="sxs-lookup"><span data-stu-id="2593c-103">Creates a data factory.</span></span>

## <span data-ttu-id="2593c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2593c-104">SYNTAX</span></span>

### <span data-ttu-id="2593c-105">ByFactoryName (Default)</span><span class="sxs-lookup"><span data-stu-id="2593c-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2593c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2593c-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2593c-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="2593c-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2593c-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="2593c-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2593c-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="2593c-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2593c-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="2593c-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2593c-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2593c-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2593c-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="2593c-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2593c-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="2593c-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-GlobalParameterDefinition <System.Collections.Generic.IDictionary`2[System.String,Microsoft.Azure.Management.DataFactory.Models.GlobalParameterSpecification]>]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2593c-114">OPIS</span><span class="sxs-lookup"><span data-stu-id="2593c-114">DESCRIPTION</span></span>
<span data-ttu-id="2593c-115">Polecenie **cmdlet Set-AzDataFactoryV2** tworzy grupę danych z określoną nazwą i lokalizacją grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2593c-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="2593c-116">Wykonaj następujące operacje w następującej kolejności: — Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="2593c-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="2593c-117">— Tworzenie usług połączonych.</span><span class="sxs-lookup"><span data-stu-id="2593c-117">-- Create linked services.</span></span>
<span data-ttu-id="2593c-118">— Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="2593c-118">-- Create datasets.</span></span>
<span data-ttu-id="2593c-119">— Tworzenie potoku.</span><span class="sxs-lookup"><span data-stu-id="2593c-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="2593c-120">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2593c-120">EXAMPLES</span></span>

### <span data-ttu-id="2593c-121">Przykład 1. Tworzenie fabryki danych</span><span class="sxs-lookup"><span data-stu-id="2593c-121">Example 1: Create a data factory</span></span>
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

### <span data-ttu-id="2593c-122">Przykład 2. Tworzenie fabryki danych ze szczegółami konfiguracji ponownego obiektu przy użyciu istniejącego obiektu fabrycznego.</span><span class="sxs-lookup"><span data-stu-id="2593c-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
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

<span data-ttu-id="2593c-123">To polecenie umożliwia utworzenie w grupie zasobów O nazwie ADF w lokalizacji WschódUS fabryki danych o nazwie WikiADF z konfiguracją kontroli źródła programu Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="2593c-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="2593c-124">Przykład 3. Tworzenie fabryki danych przy użyciu szczegółów konfiguracji ponownego obiektu GitHub przy użyciu nowego obiektu fabrycznego.</span><span class="sxs-lookup"><span data-stu-id="2593c-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
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

<span data-ttu-id="2593c-125">To polecenie umożliwia utworzenie w grupie zasobów O nazwie ADF w lokalizacji EastUS fabryki danych o nazwie WikiADF z konfiguracją kontroli źródła GitHub.</span><span class="sxs-lookup"><span data-stu-id="2593c-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="2593c-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2593c-126">PARAMETERS</span></span>

### <span data-ttu-id="2593c-127">-AccountName</span><span class="sxs-lookup"><span data-stu-id="2593c-127">-AccountName</span></span>
<span data-ttu-id="2593c-128">Nazwa konta dla konfiguracji ponownego konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="2593c-128">The account name for repo configuration.</span></span>

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

### <span data-ttu-id="2593c-129">— CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="2593c-129">-CollaborationBranch</span></span>
<span data-ttu-id="2593c-130">Gałąź współpracy dla konfiguracji ponownego konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="2593c-130">The collaboration branch for repo configuration.</span></span>

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

### <span data-ttu-id="2593c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2593c-131">-DefaultProfile</span></span>
<span data-ttu-id="2593c-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2593c-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2593c-133">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="2593c-133">-Force</span></span>
<span data-ttu-id="2593c-134">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2593c-134">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="2593c-135">-GlobalParameterDefinition</span><span class="sxs-lookup"><span data-stu-id="2593c-135">-GlobalParameterDefinition</span></span>
<span data-ttu-id="2593c-136">Słownik zawierający parametry globalne fabryczne.</span><span class="sxs-lookup"><span data-stu-id="2593c-136">The dictionary containing the global parameters of the data factory.</span></span>

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

### <span data-ttu-id="2593c-137">-HostName</span><span class="sxs-lookup"><span data-stu-id="2593c-137">-HostName</span></span>
<span data-ttu-id="2593c-138">Nazwa hosta konfiguracji ponownego repozytorium usługi GitHub.</span><span class="sxs-lookup"><span data-stu-id="2593c-138">The host name for GitHub repo configuration.</span></span>

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

### <span data-ttu-id="2593c-139">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2593c-139">-InputObject</span></span>
<span data-ttu-id="2593c-140">Obiekt data factory.</span><span class="sxs-lookup"><span data-stu-id="2593c-140">The data factory object.</span></span>

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

### <span data-ttu-id="2593c-141">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="2593c-141">-LastCommitId</span></span>
<span data-ttu-id="2593c-142">Ostatni identyfikator zatwierdzenia dla konfiguracji ponownego konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="2593c-142">The last commit id for repo configuration.</span></span>

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

### <span data-ttu-id="2593c-143">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2593c-143">-Location</span></span>
<span data-ttu-id="2593c-144">W tym regionie jest tworzona factory danych.</span><span class="sxs-lookup"><span data-stu-id="2593c-144">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="2593c-145">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2593c-145">-Name</span></span>
<span data-ttu-id="2593c-146">Nazwa fabryczna danych.</span><span class="sxs-lookup"><span data-stu-id="2593c-146">The data factory name.</span></span>

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

### <span data-ttu-id="2593c-147">— Nazwa_projektu</span><span class="sxs-lookup"><span data-stu-id="2593c-147">-ProjectName</span></span>
<span data-ttu-id="2593c-148">Nazwa projektu Azure DevOps dla konfiguracji ponownego konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="2593c-148">The project name Azure DevOps for repo configuration.</span></span>

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

### <span data-ttu-id="2593c-149">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="2593c-149">-RepositoryName</span></span>
<span data-ttu-id="2593c-150">Nazwa repozytorium dla konfiguracji ponownego repozytorium.</span><span class="sxs-lookup"><span data-stu-id="2593c-150">The repository name for repo configuration.</span></span>

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

### <span data-ttu-id="2593c-151">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2593c-151">-ResourceGroupName</span></span>
<span data-ttu-id="2593c-152">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2593c-152">The resource group name.</span></span>

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

### <span data-ttu-id="2593c-153">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2593c-153">-ResourceId</span></span>
<span data-ttu-id="2593c-154">Identyfikator usługi Azure Resource Factory w wersji 2.</span><span class="sxs-lookup"><span data-stu-id="2593c-154">The Azure resource ID of V2 data factory.</span></span>

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

### <span data-ttu-id="2593c-155">- RootFolder</span><span class="sxs-lookup"><span data-stu-id="2593c-155">-RootFolder</span></span>
<span data-ttu-id="2593c-156">Folder główny na konfigurację ponownego konfigurowania.</span><span class="sxs-lookup"><span data-stu-id="2593c-156">The root folder for repo configuration.</span></span>

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

### <span data-ttu-id="2593c-157">— Tag</span><span class="sxs-lookup"><span data-stu-id="2593c-157">-Tag</span></span>
<span data-ttu-id="2593c-158">Tagi fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="2593c-158">The tags of the data factory.</span></span>

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

### <span data-ttu-id="2593c-159">- TenantId</span><span class="sxs-lookup"><span data-stu-id="2593c-159">-TenantId</span></span>
<span data-ttu-id="2593c-160">Identyfikator dzierżawy konfiguracji ponownej usługi Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="2593c-160">The tenant id for Azure DevOps repo configuration.</span></span>

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

### <span data-ttu-id="2593c-161">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2593c-161">-Confirm</span></span>
<span data-ttu-id="2593c-162">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2593c-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2593c-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2593c-163">-WhatIf</span></span>
<span data-ttu-id="2593c-164">Pokazuje, co się stanie, jeśli polecenie cmdlet zostanie uruchomione, ale nie uruchomi polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2593c-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="2593c-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2593c-165">CommonParameters</span></span>
<span data-ttu-id="2593c-166">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2593c-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2593c-167">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2593c-167">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2593c-168">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2593c-168">INPUTS</span></span>

### <span data-ttu-id="2593c-169">System.String</span><span class="sxs-lookup"><span data-stu-id="2593c-169">System.String</span></span>

### <span data-ttu-id="2593c-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2593c-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

### <span data-ttu-id="2593c-171">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2593c-171">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2593c-172">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2593c-172">OUTPUTS</span></span>

### <span data-ttu-id="2593c-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="2593c-173">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="2593c-174">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2593c-174">NOTES</span></span>
<span data-ttu-id="2593c-175">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="2593c-175">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="2593c-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2593c-176">RELATED LINKS</span></span>

[<span data-ttu-id="2593c-177">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2593c-177">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="2593c-178">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="2593c-178">Remove-AzDataFactoryV2</span></span>]()
