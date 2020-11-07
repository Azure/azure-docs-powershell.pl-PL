---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 219e5b18a04332d2ee840fb41b92aa9d282a1792
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93896314"
---
# <span data-ttu-id="6174c-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6174c-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="6174c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6174c-102">SYNOPSIS</span></span>
<span data-ttu-id="6174c-103">Tworzy fabrykę danych.</span><span class="sxs-lookup"><span data-stu-id="6174c-103">Creates a data factory.</span></span>

## <span data-ttu-id="6174c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6174c-104">SYNTAX</span></span>

### <span data-ttu-id="6174c-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6174c-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6174c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="6174c-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6174c-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="6174c-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6174c-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="6174c-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6174c-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="6174c-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6174c-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="6174c-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6174c-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="6174c-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6174c-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="6174c-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6174c-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="6174c-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6174c-114">Opis</span><span class="sxs-lookup"><span data-stu-id="6174c-114">DESCRIPTION</span></span>
<span data-ttu-id="6174c-115">Polecenie cmdlet **Set-AzDataFactoryV2** tworzy fabrykę danych z określoną nazwą i lokalizacją grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6174c-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="6174c-116">Wykonuj następujące operacje w następującej kolejności:--Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="6174c-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="6174c-117">--Tworzenie połączonych usług.</span><span class="sxs-lookup"><span data-stu-id="6174c-117">-- Create linked services.</span></span>
<span data-ttu-id="6174c-118">--Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="6174c-118">-- Create datasets.</span></span>
<span data-ttu-id="6174c-119">— Utwórz rurociąg.</span><span class="sxs-lookup"><span data-stu-id="6174c-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="6174c-120">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6174c-120">EXAMPLES</span></span>

### <span data-ttu-id="6174c-121">Przykład 1. Tworzenie fabryki danych</span><span class="sxs-lookup"><span data-stu-id="6174c-121">Example 1: Create a data factory</span></span>
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

### <span data-ttu-id="6174c-122">Przykład 2: Tworzenie fabryki danych przy użyciu szczegółów konfiguracji repozytorium przy użyciu istniejącego obiektu fabryki.</span><span class="sxs-lookup"><span data-stu-id="6174c-122">Example 2: Create a data factory with repo configuration details using an existing factory object.</span></span>
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

<span data-ttu-id="6174c-123">To polecenie umożliwia utworzenie fabryki danych o nazwie WikiADF w grupie zasobów o nazwie ADF w lokalizacji wschodnioazjatyckiej za pomocą konfiguracji kontroli źródła usługi Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="6174c-123">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with Azure DevOps source control configuration.</span></span>

### <span data-ttu-id="6174c-124">Przykład 3: Tworzenie fabryki danych za pomocą szczegółów konfiguracji repozytorium GitHub za pomocą nowego obiektu Factory.</span><span class="sxs-lookup"><span data-stu-id="6174c-124">Example 3: Create a data factory with GitHub repo configuration details using a new factory object.</span></span>
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

<span data-ttu-id="6174c-125">To polecenie tworzy fabrykę danych o nazwie WikiADF w grupie zasobów o nazwie ADF w lokalizacji wschodnioazjatyckiej z konfiguracją kontroli źródła GitHub.</span><span class="sxs-lookup"><span data-stu-id="6174c-125">This command creates a data factory named WikiADF in the resource group named ADF in the EastUS location with GitHub source control configuration..</span></span>

## <span data-ttu-id="6174c-126">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6174c-126">PARAMETERS</span></span>

### <span data-ttu-id="6174c-127">-AccountName</span><span class="sxs-lookup"><span data-stu-id="6174c-127">-AccountName</span></span>
<span data-ttu-id="6174c-128">Nazwa konta dla konfiguracji repozytorium.</span><span class="sxs-lookup"><span data-stu-id="6174c-128">The account name for repo configuration.</span></span>

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

### <span data-ttu-id="6174c-129">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="6174c-129">-CollaborationBranch</span></span>
<span data-ttu-id="6174c-130">Gałąź współpracy na potrzeby konfiguracji repozytorium.</span><span class="sxs-lookup"><span data-stu-id="6174c-130">The collaboration branch for repo configuration.</span></span>

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

### <span data-ttu-id="6174c-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6174c-131">-DefaultProfile</span></span>
<span data-ttu-id="6174c-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6174c-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6174c-133">-Force</span><span class="sxs-lookup"><span data-stu-id="6174c-133">-Force</span></span>
<span data-ttu-id="6174c-134">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6174c-134">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="6174c-135">-HostName</span><span class="sxs-lookup"><span data-stu-id="6174c-135">-HostName</span></span>
<span data-ttu-id="6174c-136">Nazwa hosta na potrzeby konfiguracji repozytorium GitHub.</span><span class="sxs-lookup"><span data-stu-id="6174c-136">The host name for GitHub repo configuration.</span></span>

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

### <span data-ttu-id="6174c-137">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="6174c-137">-InputObject</span></span>
<span data-ttu-id="6174c-138">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="6174c-138">The data factory object.</span></span>

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

### <span data-ttu-id="6174c-139">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="6174c-139">-LastCommitId</span></span>
<span data-ttu-id="6174c-140">Ostatni identyfikator zatwierdzenia dla konfiguracji repozytorium.</span><span class="sxs-lookup"><span data-stu-id="6174c-140">The last commit id for repo configuration.</span></span>

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

### <span data-ttu-id="6174c-141">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6174c-141">-Location</span></span>
<span data-ttu-id="6174c-142">Fabryka danych jest tworzona w tym regionie.</span><span class="sxs-lookup"><span data-stu-id="6174c-142">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="6174c-143">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6174c-143">-Name</span></span>
<span data-ttu-id="6174c-144">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="6174c-144">The data factory name.</span></span>

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

### <span data-ttu-id="6174c-145">-NazwaProjektu</span><span class="sxs-lookup"><span data-stu-id="6174c-145">-ProjectName</span></span>
<span data-ttu-id="6174c-146">Nazwa projektu dotycząca konfiguracji usługi Azure DevOps dla repozytorium.</span><span class="sxs-lookup"><span data-stu-id="6174c-146">The project name Azure DevOps for repo configuration.</span></span>

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

### <span data-ttu-id="6174c-147">-Repositoryname</span><span class="sxs-lookup"><span data-stu-id="6174c-147">-RepositoryName</span></span>
<span data-ttu-id="6174c-148">Nazwa repozytorium konfiguracji repozytorium.</span><span class="sxs-lookup"><span data-stu-id="6174c-148">The repository name for repo configuration.</span></span>

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

### <span data-ttu-id="6174c-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6174c-149">-ResourceGroupName</span></span>
<span data-ttu-id="6174c-150">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6174c-150">The resource group name.</span></span>

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

### <span data-ttu-id="6174c-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6174c-151">-ResourceId</span></span>
<span data-ttu-id="6174c-152">Identyfikator zasobu platformy Azure fabryki danych w wersji 2.</span><span class="sxs-lookup"><span data-stu-id="6174c-152">The Azure resource ID of V2 data factory.</span></span>

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

### <span data-ttu-id="6174c-153">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="6174c-153">-RootFolder</span></span>
<span data-ttu-id="6174c-154">Folder główny dla konfiguracji repozytorium.</span><span class="sxs-lookup"><span data-stu-id="6174c-154">The root folder for repo configuration.</span></span>

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

### <span data-ttu-id="6174c-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="6174c-155">-Tag</span></span>
<span data-ttu-id="6174c-156">Znaczniki fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="6174c-156">The tags of the data factory.</span></span>

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

### <span data-ttu-id="6174c-157">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="6174c-157">-TenantId</span></span>
<span data-ttu-id="6174c-158">Identyfikator dzierżawy dla konfiguracji repozytorium usługi Azure DevOps.</span><span class="sxs-lookup"><span data-stu-id="6174c-158">The tenant id for Azure DevOps repo configuration.</span></span>

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

### <span data-ttu-id="6174c-159">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6174c-159">-Confirm</span></span>
<span data-ttu-id="6174c-160">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6174c-160">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6174c-161">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6174c-161">-WhatIf</span></span>
<span data-ttu-id="6174c-162">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6174c-162">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="6174c-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6174c-163">CommonParameters</span></span>
<span data-ttu-id="6174c-164">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6174c-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6174c-165">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6174c-165">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6174c-166">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6174c-166">INPUTS</span></span>

### <span data-ttu-id="6174c-167">System. String</span><span class="sxs-lookup"><span data-stu-id="6174c-167">System.String</span></span>

### <span data-ttu-id="6174c-168">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="6174c-168">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6174c-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6174c-169">OUTPUTS</span></span>

### <span data-ttu-id="6174c-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="6174c-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="6174c-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6174c-171">NOTES</span></span>
<span data-ttu-id="6174c-172">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="6174c-172">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="6174c-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6174c-173">RELATED LINKS</span></span>

[<span data-ttu-id="6174c-174">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6174c-174">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="6174c-175">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="6174c-175">Remove-AzDataFactoryV2</span></span>]()
