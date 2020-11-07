---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2.md
ms.openlocfilehash: 374263c26a3572e8d85e18d1795c27a761866a4a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705938"
---
# <span data-ttu-id="12489-101">Set-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="12489-101">Set-AzDataFactoryV2</span></span>

## <span data-ttu-id="12489-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="12489-102">SYNOPSIS</span></span>
<span data-ttu-id="12489-103">Tworzy fabrykę danych.</span><span class="sxs-lookup"><span data-stu-id="12489-103">Creates a data factory.</span></span>

## <span data-ttu-id="12489-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="12489-104">SYNTAX</span></span>

### <span data-ttu-id="12489-105">ByFactoryName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="12489-105">ByFactoryName (Default)</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12489-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="12489-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12489-107">ByResourceIdFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="12489-107">ByResourceIdFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12489-108">ByResourceIdFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="12489-108">ByResourceIdFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceId] <String> [-Location] <String> [[-Tag] <Hashtable>] [-Force]
 -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12489-109">ByFactoryNameFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="12489-109">ByFactoryNameFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="12489-110">ByFactoryNameFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="12489-110">ByFactoryNameFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [[-Tag] <Hashtable>]
 [-Force] -AccountName <String> -RepositoryName <String> -CollaborationBranch <String> -RootFolder <String>
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12489-111">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="12489-111">ByInputObject</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12489-112">ByInputObjectFactoryRepoVstsConfig</span><span class="sxs-lookup"><span data-stu-id="12489-112">ByInputObjectFactoryRepoVstsConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -ProjectName <String> [-TenantId <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12489-113">ByInputObjectFactoryRepoGitConfig</span><span class="sxs-lookup"><span data-stu-id="12489-113">ByInputObjectFactoryRepoGitConfig</span></span>
```
Set-AzDataFactoryV2 -InputObject <PSDataFactory> [[-Location] <String>] [[-Tag] <Hashtable>] [-Force]
 [-AccountName <String>] [-RepositoryName <String>] [-CollaborationBranch <String>] [-RootFolder <String>]
 [-LastCommitId <String>] -HostName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12489-114">Opis</span><span class="sxs-lookup"><span data-stu-id="12489-114">DESCRIPTION</span></span>
<span data-ttu-id="12489-115">Polecenie cmdlet **Set-AzDataFactoryV2** tworzy fabrykę danych z określoną nazwą i lokalizacją grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="12489-115">The **Set-AzDataFactoryV2** cmdlet creates a data factory with the specified resource group name and location.</span></span>
<span data-ttu-id="12489-116">Wykonuj następujące operacje w następującej kolejności:--Tworzenie fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="12489-116">Perform these operations in the following order: -- Create a data factory.</span></span>
<span data-ttu-id="12489-117">--Tworzenie połączonych usług.</span><span class="sxs-lookup"><span data-stu-id="12489-117">-- Create linked services.</span></span>
<span data-ttu-id="12489-118">--Tworzenie zestawów danych.</span><span class="sxs-lookup"><span data-stu-id="12489-118">-- Create datasets.</span></span>
<span data-ttu-id="12489-119">— Utwórz rurociąg.</span><span class="sxs-lookup"><span data-stu-id="12489-119">-- Create a pipeline.</span></span>

## <span data-ttu-id="12489-120">Przykłady</span><span class="sxs-lookup"><span data-stu-id="12489-120">EXAMPLES</span></span>

### <span data-ttu-id="12489-121">Przykład 1. Tworzenie fabryki danych</span><span class="sxs-lookup"><span data-stu-id="12489-121">Example 1: Create a data factory</span></span>
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

### <span data-ttu-id="12489-122">Przykład 2: Tworzenie fabryki danych ze szczegółami repoconfiguration przy użyciu istniejącego obiektu fabryki.</span><span class="sxs-lookup"><span data-stu-id="12489-122">Example 2: Create a data factory with repoconfiguration details using an existing factory object.</span></span>
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

<span data-ttu-id="12489-123">To polecenie tworzy fabrykę danych o nazwie WikiADF w grupie zasobów o nazwie ADF w lokalizacji na zachód.</span><span class="sxs-lookup"><span data-stu-id="12489-123">This command creates a data factory named WikiADF in the resource group named ADF in the WestUS location.</span></span>

## <span data-ttu-id="12489-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="12489-124">PARAMETERS</span></span>

### <span data-ttu-id="12489-125">-AccountName</span><span class="sxs-lookup"><span data-stu-id="12489-125">-AccountName</span></span>
<span data-ttu-id="12489-126">Nazwa konta dla konfiguracji repozytorium.</span><span class="sxs-lookup"><span data-stu-id="12489-126">The account name for repo configuration.</span></span>

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

### <span data-ttu-id="12489-127">-CollaborationBranch</span><span class="sxs-lookup"><span data-stu-id="12489-127">-CollaborationBranch</span></span>
<span data-ttu-id="12489-128">Gałąź współpracy na potrzeby konfiguracji repozytorium.</span><span class="sxs-lookup"><span data-stu-id="12489-128">The collaboration branch for repo configuration.</span></span>

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

### <span data-ttu-id="12489-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12489-129">-DefaultProfile</span></span>
<span data-ttu-id="12489-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="12489-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="12489-131">-Force</span><span class="sxs-lookup"><span data-stu-id="12489-131">-Force</span></span>
<span data-ttu-id="12489-132">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="12489-132">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="12489-133">-HostName</span><span class="sxs-lookup"><span data-stu-id="12489-133">-HostName</span></span>
<span data-ttu-id="12489-134">Nazwa hosta dla konfiguracji repozytorium.</span><span class="sxs-lookup"><span data-stu-id="12489-134">The host name for repo configuration.</span></span>

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

### <span data-ttu-id="12489-135">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="12489-135">-InputObject</span></span>
<span data-ttu-id="12489-136">Obiekt fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="12489-136">The data factory object.</span></span>

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

### <span data-ttu-id="12489-137">-LastCommitId</span><span class="sxs-lookup"><span data-stu-id="12489-137">-LastCommitId</span></span>
<span data-ttu-id="12489-138">Ostatni identyfikator zatwierdzenia dla konfiguracji repozytorium.</span><span class="sxs-lookup"><span data-stu-id="12489-138">The last commit id for repo configuration.</span></span>

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

### <span data-ttu-id="12489-139">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="12489-139">-Location</span></span>
<span data-ttu-id="12489-140">Fabryka danych jest tworzona w tym regionie.</span><span class="sxs-lookup"><span data-stu-id="12489-140">The data factory is created in this region.</span></span>

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

### <span data-ttu-id="12489-141">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="12489-141">-Name</span></span>
<span data-ttu-id="12489-142">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="12489-142">The data factory name.</span></span>

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

### <span data-ttu-id="12489-143">-NazwaProjektu</span><span class="sxs-lookup"><span data-stu-id="12489-143">-ProjectName</span></span>
<span data-ttu-id="12489-144">Nazwa projektu dla konfiguracji repozytorium.</span><span class="sxs-lookup"><span data-stu-id="12489-144">The project name for repo configuration.</span></span>

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

### <span data-ttu-id="12489-145">-Repositoryname</span><span class="sxs-lookup"><span data-stu-id="12489-145">-RepositoryName</span></span>
<span data-ttu-id="12489-146">Nazwa repozytorium konfiguracji repozytorium.</span><span class="sxs-lookup"><span data-stu-id="12489-146">The repository name for repo configuration.</span></span>

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

### <span data-ttu-id="12489-147">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12489-147">-ResourceGroupName</span></span>
<span data-ttu-id="12489-148">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="12489-148">The resource group name.</span></span>

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

### <span data-ttu-id="12489-149">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12489-149">-ResourceId</span></span>
<span data-ttu-id="12489-150">Identyfikator zasobu platformy Azure fabryki danych w wersji 2.</span><span class="sxs-lookup"><span data-stu-id="12489-150">The Azure resource ID of V2 data factory.</span></span>

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

### <span data-ttu-id="12489-151">-RootFolder</span><span class="sxs-lookup"><span data-stu-id="12489-151">-RootFolder</span></span>
<span data-ttu-id="12489-152">Folder główny dla konfiguracji repozytorium.</span><span class="sxs-lookup"><span data-stu-id="12489-152">The root folder for repo configuration.</span></span>

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

### <span data-ttu-id="12489-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="12489-153">-Tag</span></span>
<span data-ttu-id="12489-154">Znaczniki fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="12489-154">The tags of the data factory.</span></span>

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

### <span data-ttu-id="12489-155">-Dzierżawy</span><span class="sxs-lookup"><span data-stu-id="12489-155">-TenantId</span></span>
<span data-ttu-id="12489-156">Identyfikator dzierżawy dla konfiguracji repozytorium.</span><span class="sxs-lookup"><span data-stu-id="12489-156">The tenant id for repo configuration.</span></span>

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

### <span data-ttu-id="12489-157">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="12489-157">-Confirm</span></span>
<span data-ttu-id="12489-158">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12489-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12489-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12489-159">-WhatIf</span></span>
<span data-ttu-id="12489-160">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="12489-160">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="12489-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12489-161">CommonParameters</span></span>
<span data-ttu-id="12489-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="12489-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12489-163">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="12489-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12489-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="12489-164">INPUTS</span></span>

### <span data-ttu-id="12489-165">System. String</span><span class="sxs-lookup"><span data-stu-id="12489-165">System.String</span></span>

### <span data-ttu-id="12489-166">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="12489-166">System.Collections.Hashtable</span></span>

## <span data-ttu-id="12489-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="12489-167">OUTPUTS</span></span>

### <span data-ttu-id="12489-168">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span><span class="sxs-lookup"><span data-stu-id="12489-168">Microsoft.Azure.Commands.DataFactoryV2.Models.PSDataFactory</span></span>

## <span data-ttu-id="12489-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="12489-169">NOTES</span></span>
<span data-ttu-id="12489-170">Słowa kluczowe: Azure, azurerm, ARM, Resource, Management, Manager, dane, fabryki</span><span class="sxs-lookup"><span data-stu-id="12489-170">Keywords: azure, azurerm, arm, resource, management, manager, data, factories</span></span>

## <span data-ttu-id="12489-171">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="12489-171">RELATED LINKS</span></span>

[<span data-ttu-id="12489-172">Get-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="12489-172">Get-AzDataFactoryV2</span></span>]()

[<span data-ttu-id="12489-173">Remove-AzDataFactoryV2</span><span class="sxs-lookup"><span data-stu-id="12489-173">Remove-AzDataFactoryV2</span></span>]()
