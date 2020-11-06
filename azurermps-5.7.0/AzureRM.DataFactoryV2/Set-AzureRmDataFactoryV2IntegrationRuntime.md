---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/set-azurermdatafactoryv2integrationruntime
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: 8b91e1a68fc731476240021889cc80c9c4848357
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544440"
---
# <span data-ttu-id="429ab-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="429ab-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="429ab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="429ab-102">SYNOPSIS</span></span>
<span data-ttu-id="429ab-103">Aktualizuje środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="429ab-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="429ab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="429ab-104">SYNTAX</span></span>

### <span data-ttu-id="429ab-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="429ab-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="429ab-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="429ab-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="429ab-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="429ab-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-SetupScriptContainerSasUri <String>] [-Edition <String>] [-MaxParallelExecutionsPerNode <Int32>]
 [-LicenseType <String>] [-AuthKey <SecureString>] [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="429ab-108">Opis</span><span class="sxs-lookup"><span data-stu-id="429ab-108">DESCRIPTION</span></span>
<span data-ttu-id="429ab-109">Polecenie cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime aktualizuje środowisko uruchomieniowe integracji z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="429ab-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="429ab-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="429ab-110">EXAMPLES</span></span>

### <span data-ttu-id="429ab-111">Przykład 1: Opis aktualizacji środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="429ab-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="429ab-112">Polecenie cmdlet aktualizuje Opis środowiska wykonawczego integracji o nazwie test-SelfHost-IR '.</span><span class="sxs-lookup"><span data-stu-id="429ab-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="429ab-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="429ab-113">PARAMETERS</span></span>

### <span data-ttu-id="429ab-114">-AuthKey</span><span class="sxs-lookup"><span data-stu-id="429ab-114">-AuthKey</span></span>
<span data-ttu-id="429ab-115">Klucz uwierzytelniania w środowisku wykonawczym programu integracyjnego Self-host.</span><span class="sxs-lookup"><span data-stu-id="429ab-115">The authentication key of the self-hosted integration runtime.</span></span>

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-116">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="429ab-116">-CatalogAdminCredential</span></span>
<span data-ttu-id="429ab-117">Poświadczenia administratora bazy danych wykazu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="429ab-117">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-118">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="429ab-118">-CatalogPricingTier</span></span>
<span data-ttu-id="429ab-119">Warstwa cenowa bazy danych katalogu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="429ab-119">The catalog database pricing tier of the integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-120">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="429ab-120">-CatalogServerEndpoint</span></span>
<span data-ttu-id="429ab-121">Punkt końcowy serwera bazy danych wykazu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="429ab-121">The catalog database server endpoint of the integration runtime.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="429ab-122">-DataFactoryName</span></span>
<span data-ttu-id="429ab-123">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="429ab-123">The data factory name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="429ab-124">-DefaultProfile</span></span>
<span data-ttu-id="429ab-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="429ab-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-126">— Opis</span><span class="sxs-lookup"><span data-stu-id="429ab-126">-Description</span></span>
<span data-ttu-id="429ab-127">Opis środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="429ab-127">The integration runtime description.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-128">-Edition</span><span class="sxs-lookup"><span data-stu-id="429ab-128">-Edition</span></span>
<span data-ttu-id="429ab-129">Środowisko uruchomieniowe integracji wersji SSIS, które może być standardem lub Enterprise, domyślnie jest standardowe, jeśli nie zostało określone.</span><span class="sxs-lookup"><span data-stu-id="429ab-129">The edition for SSIS integration runtime which could be Standard or Enterprise, default is Standard if it is not specified.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Enterprise

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-130">-Force</span><span class="sxs-lookup"><span data-stu-id="429ab-130">-Force</span></span>
<span data-ttu-id="429ab-131">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="429ab-131">Runs the cmdlet without prompting for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-132">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="429ab-132">-InputObject</span></span>
<span data-ttu-id="429ab-133">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="429ab-133">The integration runtime object.</span></span>

```yaml
Type: PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-134">-LicenseType</span><span class="sxs-lookup"><span data-stu-id="429ab-134">-LicenseType</span></span>
<span data-ttu-id="429ab-135">Typ licencji, który ma zostać wybrany dla podczerwieni SSIS.</span><span class="sxs-lookup"><span data-stu-id="429ab-135">The license type that you want to select for the SSIS IR.</span></span> <span data-ttu-id="429ab-136">Istnieją dwa typy: LicenseIncluded lub BasePrice.</span><span class="sxs-lookup"><span data-stu-id="429ab-136">There are two types: LicenseIncluded or BasePrice.</span></span> <span data-ttu-id="429ab-137">W przypadku kwalifikowania się do korzystania z cen usługi Azure hybrydowego użytkowania (AHUB) wybierz pozycję BasePrice.</span><span class="sxs-lookup"><span data-stu-id="429ab-137">If you are qualified for the Azure Hybrid Use Benefit (AHUB) pricing, please select BasePrice.</span></span> <span data-ttu-id="429ab-138">Jeśli nie, wybierz LicenseIncluded.</span><span class="sxs-lookup"><span data-stu-id="429ab-138">If not, please select LicenseIncluded.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: LicenseIncluded, BasePrice

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-139">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="429ab-139">-Location</span></span>
<span data-ttu-id="429ab-140">Lokalizacja środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="429ab-140">The integration runtime location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-141">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="429ab-141">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="429ab-142">Maksymalna liczba równoległych operacji na węzeł dla zarządzanego dedykowanego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="429ab-142">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-143">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="429ab-143">-Name</span></span>
<span data-ttu-id="429ab-144">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="429ab-144">The integration runtime name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-145">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="429ab-145">-NodeCount</span></span>
<span data-ttu-id="429ab-146">Liczba węzłów docelowych środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="429ab-146">Target nodes count of the integration runtime.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-147">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="429ab-147">-NodeSize</span></span>
<span data-ttu-id="429ab-148">Rozmiar węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="429ab-148">The integration runtime node size.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-149">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="429ab-149">-ResourceGroupName</span></span>
<span data-ttu-id="429ab-150">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="429ab-150">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-151">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="429ab-151">-ResourceId</span></span>
<span data-ttu-id="429ab-152">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="429ab-152">The Azure resource ID.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-153">-SetupScriptContainerSasUri</span><span class="sxs-lookup"><span data-stu-id="429ab-153">-SetupScriptContainerSasUri</span></span>
<span data-ttu-id="429ab-154">Identyfikator URI SAS kontenera obiektów blob platformy Azure zawierającego niestandardowy skrypt instalacji.</span><span class="sxs-lookup"><span data-stu-id="429ab-154">The SAS URI of the Azure blob container that contains the custom setup script.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-155">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="429ab-155">-Subnet</span></span>
<span data-ttu-id="429ab-156">Nazwa podsieci w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="429ab-156">The name of the subnet in the VNet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-157">-Type</span><span class="sxs-lookup"><span data-stu-id="429ab-157">-Type</span></span>
<span data-ttu-id="429ab-158">Typ środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="429ab-158">The integration runtime type.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Managed, SelfHosted

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-159">-VNetId</span><span class="sxs-lookup"><span data-stu-id="429ab-159">-VNetId</span></span>
<span data-ttu-id="429ab-160">Identyfikator sieci wirtualnej, z którą łączy się środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="429ab-160">The ID of the VNet that the integration runtime joins.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-161">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="429ab-161">-Confirm</span></span>
<span data-ttu-id="429ab-162">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="429ab-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="429ab-163">-WhatIf</span></span>
<span data-ttu-id="429ab-164">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="429ab-164">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="429ab-165">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="429ab-165">CommonParameters</span></span>
<span data-ttu-id="429ab-166">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="429ab-166">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="429ab-167">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="429ab-167">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="429ab-168">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="429ab-168">INPUTS</span></span>

### <span data-ttu-id="429ab-169">System. String</span><span class="sxs-lookup"><span data-stu-id="429ab-169">System.String</span></span>
<span data-ttu-id="429ab-170">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="429ab-170">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="429ab-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="429ab-171">OUTPUTS</span></span>

### <span data-ttu-id="429ab-172">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="429ab-172">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="429ab-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="429ab-173">NOTES</span></span>

## <span data-ttu-id="429ab-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="429ab-174">RELATED LINKS</span></span>

[<span data-ttu-id="429ab-175">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="429ab-175">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
