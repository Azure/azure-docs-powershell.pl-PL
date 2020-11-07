---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/set-azdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Set-AzDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: e92d04e60132463b22741242f411f6af5d09c2b0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93868683"
---
# <span data-ttu-id="5f2a8-101">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5f2a8-101">Set-AzDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="5f2a8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5f2a8-102">SYNOPSIS</span></span>
<span data-ttu-id="5f2a8-103">Aktualizuje środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-103">Updates an integration runtime.</span></span>

## <span data-ttu-id="5f2a8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5f2a8-104">SYNTAX</span></span>

### <span data-ttu-id="5f2a8-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5f2a8-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] [-Location <String>] [-NodeSize <String>]
 [-NodeCount <Int32>] [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>]
 [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>]
 [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f2a8-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="5f2a8-106">ByResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f2a8-107">ByLinkedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="5f2a8-107">ByLinkedIntegrationRuntimeResourceId</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceId] <String> [-Type <String>] [-Description <String>]
 -SharedIntegrationRuntimeResourceId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f2a8-108">ByLinkedIntegrationRuntimeName</span><span class="sxs-lookup"><span data-stu-id="5f2a8-108">ByLinkedIntegrationRuntimeName</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-ResourceGroupName] <String> [-DataFactoryName] <String>
 [-Name] <String> [-Type <String>] [-Description <String>] -SharedIntegrationRuntimeResourceId <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f2a8-109">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="5f2a8-109">ByIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] [-Location <String>] [-NodeSize <String>] [-NodeCount <Int32>]
 [-CatalogServerEndpoint <String>] [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>]
 [-VNetId <String>] [-Subnet <String>] [-SetupScriptContainerSasUri <String>] [-Edition <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-LicenseType <String>] [-AuthKey <SecureString>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5f2a8-110">ByLinkedIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="5f2a8-110">ByLinkedIntegrationRuntimeObject</span></span>
```
Set-AzDataFactoryV2IntegrationRuntime [-InputObject] <PSIntegrationRuntime> [-Type <String>]
 [-Description <String>] -SharedIntegrationRuntimeResourceId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f2a8-111">Opis</span><span class="sxs-lookup"><span data-stu-id="5f2a8-111">DESCRIPTION</span></span>
<span data-ttu-id="5f2a8-112">Polecenie cmdlet Set-AzDataFactoryV2IntegrationRuntime aktualizuje środowisko uruchomieniowe integracji z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-112">The Set-AzDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="5f2a8-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5f2a8-113">EXAMPLES</span></span>

### <span data-ttu-id="5f2a8-114">Przykład 1: Opis aktualizacji środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-114">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="5f2a8-115">Polecenie cmdlet aktualizuje Opis środowiska wykonawczego integracji o nazwie test-SelfHost-IR '.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-115">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

### <span data-ttu-id="5f2a8-116">Przykład 2: udostępnianie samoobsługowego środowiska integracji.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-116">Example 2: Share Self-hosted integration runtime.</span></span>
```
PS C:\> Set-AzDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -SharedIntegrationRuntimeResourceId '/subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir' -Type "SelfHosted"

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="5f2a8-117">Polecenie cmdlet umożliwia dodanie podajnika APD do korzystania z środowiska współdzielonej integracji.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-117">The cmdlet adds the ADF to use the shared integration runtime.</span></span> <span data-ttu-id="5f2a8-118">W przypadku używania `-SharedIntegrationRuntimeResourceId` parametru `-Type` należy również uwzględnić te parametry.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-118">When using `-SharedIntegrationRuntimeResourceId` parameter the `-Type` must also be included.</span></span> <span data-ttu-id="5f2a8-119">Pamiętaj, że przed uruchomieniem polecenia cmdlet należy udzielić firmie danych uprawnień do korzystania z środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-119">Note that the data factory need to be granted permission to use the integration runtime before running cmdlet.</span></span>

## <span data-ttu-id="5f2a8-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5f2a8-120">PARAMETERS</span></span>

### <span data-ttu-id="5f2a8-121">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="5f2a8-121">-AuthKey</span></span>
<span data-ttu-id="5f2a8-122">Klucz uwierzytelniania w środowisku wykonawczym programu integracyjnego Self-host.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-122">The authentication key of the self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="5f2a8-123">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="5f2a8-123">-CatalogAdminCredential</span></span>
<span data-ttu-id="5f2a8-124">Poświadczenia administratora bazy danych wykazu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-124">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="5f2a8-125">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="5f2a8-125">-CatalogPricingTier</span></span>
<span data-ttu-id="5f2a8-126">Warstwa cenowa bazy danych katalogu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-126">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="5f2a8-127">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="5f2a8-127">-CatalogServerEndpoint</span></span>
<span data-ttu-id="5f2a8-128">Punkt końcowy serwera bazy danych wykazu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-128">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="5f2a8-129">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="5f2a8-129">-DataFactoryName</span></span>
<span data-ttu-id="5f2a8-130">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-130">The data factory name.</span></span>

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

### <span data-ttu-id="5f2a8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f2a8-131">-DefaultProfile</span></span>
<span data-ttu-id="5f2a8-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f2a8-133">— Opis</span><span class="sxs-lookup"><span data-stu-id="5f2a8-133">-Description</span></span>
<span data-ttu-id="5f2a8-134">Opis środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-134">The integration runtime description.</span></span>

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

### <span data-ttu-id="5f2a8-135">-Edition</span><span class="sxs-lookup"><span data-stu-id="5f2a8-135">-Edition</span></span>
<span data-ttu-id="5f2a8-136">Środowisko uruchomieniowe integracji wersji SSIS, które może być standardem lub Enterprise, domyślnie jest standardowe, jeśli nie zostało określone.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-136">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

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

### <span data-ttu-id="5f2a8-137">-Force</span><span class="sxs-lookup"><span data-stu-id="5f2a8-137">-Force</span></span>
<span data-ttu-id="5f2a8-138">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-138">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="5f2a8-139">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5f2a8-139">-InputObject</span></span>
<span data-ttu-id="5f2a8-140">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-140">The integration runtime object.</span></span>

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

### <span data-ttu-id="5f2a8-141">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="5f2a8-141">-LicenseType</span></span>
<span data-ttu-id="5f2a8-142">Typ licencji, który ma zostać wybrany dla podczerwieni SSIS.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-142">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="5f2a8-143">Istnieją dwa typy: LicenseIncluded lub BasePrice.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-143">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="5f2a8-144">W przypadku kwalifikowania się do korzystania z cen usługi Azure hybrydowego użytkowania (AHUB) wybierz pozycję BasePrice.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-144">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="5f2a8-145">Jeśli nie, wybierz LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-145">If not, please select LicenseIncluded.</span></span>

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

### <span data-ttu-id="5f2a8-146">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="5f2a8-146">-Location</span></span>
<span data-ttu-id="5f2a8-147">Lokalizacja środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-147">The integration runtime location.</span></span>

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

### <span data-ttu-id="5f2a8-148">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="5f2a8-148">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="5f2a8-149">Maksymalna liczba równoległych operacji na węzeł dla zarządzanego dedykowanego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-149">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="5f2a8-150">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5f2a8-150">-Name</span></span>
<span data-ttu-id="5f2a8-151">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-151">The integration runtime name.</span></span>

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

### <span data-ttu-id="5f2a8-152">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="5f2a8-152">-NodeCount</span></span>
<span data-ttu-id="5f2a8-153">Liczba węzłów docelowych środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-153">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="5f2a8-154">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="5f2a8-154">-NodeSize</span></span>
<span data-ttu-id="5f2a8-155">Rozmiar węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-155">The integration runtime node size.</span></span>

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

### <span data-ttu-id="5f2a8-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f2a8-156">-ResourceGroupName</span></span>
<span data-ttu-id="5f2a8-157">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-157">The resource group name.</span></span>

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

### <span data-ttu-id="5f2a8-158">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5f2a8-158">-ResourceId</span></span>
<span data-ttu-id="5f2a8-159">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-159">The Azure resource ID.</span></span>

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

### <span data-ttu-id="5f2a8-160">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="5f2a8-160">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="5f2a8-161">Identyfikator URI SAS kontenera obiektów blob platformy Azure zawierającego niestandardowy skrypt instalacji.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-161">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

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

### <span data-ttu-id="5f2a8-162">-SharedIntegrationRuntimeResourceId</span><span class="sxs-lookup"><span data-stu-id="5f2a8-162">-SharedIntegrationRuntimeResourceId</span></span>
<span data-ttu-id="5f2a8-163">Identyfikator zasobu współużytkowanego środowiska obsługi integracji.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-163">The resource id of the shared self-hosted integration runtime.</span></span>

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

### <span data-ttu-id="5f2a8-164">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="5f2a8-164">-Subnet</span></span>
<span data-ttu-id="5f2a8-165">Nazwa podsieci w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-165">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="5f2a8-166">-Type</span><span class="sxs-lookup"><span data-stu-id="5f2a8-166">-Type</span></span>
<span data-ttu-id="5f2a8-167">Typ środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-167">The integration runtime type.</span></span>

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

### <span data-ttu-id="5f2a8-168">-VNetId</span><span class="sxs-lookup"><span data-stu-id="5f2a8-168">-VNetId</span></span>
<span data-ttu-id="5f2a8-169">Identyfikator sieci wirtualnej, z którą łączy się środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-169">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="5f2a8-170">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5f2a8-170">-Confirm</span></span>
<span data-ttu-id="5f2a8-171">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-171">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f2a8-172">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f2a8-172">-WhatIf</span></span>
<span data-ttu-id="5f2a8-173">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-173">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="5f2a8-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f2a8-174">CommonParameters</span></span>
<span data-ttu-id="5f2a8-175">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f2a8-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f2a8-176">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f2a8-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f2a8-177">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5f2a8-177">INPUTS</span></span>

### <span data-ttu-id="5f2a8-178">System. String</span><span class="sxs-lookup"><span data-stu-id="5f2a8-178">System.String</span></span>

### <span data-ttu-id="5f2a8-179">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5f2a8-179">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5f2a8-180">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5f2a8-180">OUTPUTS</span></span>

### <span data-ttu-id="5f2a8-181">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5f2a8-181">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="5f2a8-182">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5f2a8-182">NOTES</span></span>

## <span data-ttu-id="5f2a8-183">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5f2a8-183">RELATED LINKS</span></span>

[<span data-ttu-id="5f2a8-184">Set-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="5f2a8-184">Set-AzDataFactoryV2IntegrationRuntime</span></span>]()
