---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
ms.openlocfilehash: ce842abf58dabb0bdd518f02e7030f3fb2feabc1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719345"
---
# <span data-ttu-id="4998c-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4998c-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="4998c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4998c-102">SYNOPSIS</span></span>
<span data-ttu-id="4998c-103">Aktualizuje środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="4998c-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4998c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4998c-104">SYNTAX</span></span>

### <span data-ttu-id="4998c-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4998c-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4998c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="4998c-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4998c-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="4998c-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4998c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4998c-108">DESCRIPTION</span></span>
<span data-ttu-id="4998c-109">Polecenie cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime aktualizuje środowisko uruchomieniowe integracji z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="4998c-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="4998c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4998c-110">EXAMPLES</span></span>

### <span data-ttu-id="4998c-111">Przykład 1: Opis aktualizacji środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="4998c-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description
```

<span data-ttu-id="4998c-112">Polecenie cmdlet aktualizuje Opis środowiska wykonawczego integracji o nazwie test-SelfHost-IR '.</span><span class="sxs-lookup"><span data-stu-id="4998c-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="4998c-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4998c-113">PARAMETERS</span></span>

### <span data-ttu-id="4998c-114">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="4998c-114">-CatalogAdminCredential</span></span>
<span data-ttu-id="4998c-115">Poświadczenia administratora bazy danych wykazu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="4998c-115">The catalog database administrator credential of the integration runtime.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4998c-116">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="4998c-116">-CatalogPricingTier</span></span>
<span data-ttu-id="4998c-117">Warstwa cenowa bazy danych katalogu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="4998c-117">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="4998c-118">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="4998c-118">-CatalogServerEndpoint</span></span>
<span data-ttu-id="4998c-119">Punkt końcowy serwera bazy danych wykazu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="4998c-119">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="4998c-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4998c-120">-Confirm</span></span>
<span data-ttu-id="4998c-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4998c-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4998c-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="4998c-122">-DataFactoryName</span></span>
<span data-ttu-id="4998c-123">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="4998c-123">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4998c-124">— Opis</span><span class="sxs-lookup"><span data-stu-id="4998c-124">-Description</span></span>
<span data-ttu-id="4998c-125">Opis środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="4998c-125">The integration runtime description.</span></span>

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

### <span data-ttu-id="4998c-126">-Force</span><span class="sxs-lookup"><span data-stu-id="4998c-126">-Force</span></span>
<span data-ttu-id="4998c-127">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4998c-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="4998c-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="4998c-128">-InputObject</span></span>
<span data-ttu-id="4998c-129">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="4998c-129">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4998c-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="4998c-130">-Location</span></span>
<span data-ttu-id="4998c-131">Lokalizacja środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="4998c-131">The integration runtime location.</span></span>

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

### <span data-ttu-id="4998c-132">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="4998c-132">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="4998c-133">Maksymalna liczba równoległych operacji na węzeł dla zarządzanego dedykowanego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="4998c-133">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4998c-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="4998c-134">-Name</span></span>
<span data-ttu-id="4998c-135">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="4998c-135">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: IntegrationRuntimeName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4998c-136">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="4998c-136">-NodeCount</span></span>
<span data-ttu-id="4998c-137">Liczba węzłów docelowych środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="4998c-137">Target nodes count of the integration runtime.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4998c-138">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="4998c-138">-NodeSize</span></span>
<span data-ttu-id="4998c-139">Rozmiar węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="4998c-139">The integration runtime node size.</span></span>

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

### <span data-ttu-id="4998c-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4998c-140">-ResourceGroupName</span></span>
<span data-ttu-id="4998c-141">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="4998c-141">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4998c-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="4998c-142">-ResourceId</span></span>
<span data-ttu-id="4998c-143">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="4998c-143">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4998c-144">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="4998c-144">-Subnet</span></span>
<span data-ttu-id="4998c-145">Nazwa podsieci w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="4998c-145">The name of the subnet in the VNet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SubnetName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4998c-146">-Type</span><span class="sxs-lookup"><span data-stu-id="4998c-146">-Type</span></span>
<span data-ttu-id="4998c-147">Typ środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="4998c-147">The integration runtime type.</span></span>

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

### <span data-ttu-id="4998c-148">-VNetId</span><span class="sxs-lookup"><span data-stu-id="4998c-148">-VNetId</span></span>
<span data-ttu-id="4998c-149">Identyfikator sieci wirtualnej, z którą łączy się środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="4998c-149">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="4998c-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4998c-150">-WhatIf</span></span>
<span data-ttu-id="4998c-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4998c-151">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

### <span data-ttu-id="4998c-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4998c-152">-DefaultProfile</span></span>
<span data-ttu-id="4998c-153">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4998c-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4998c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4998c-154">CommonParameters</span></span>
<span data-ttu-id="4998c-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4998c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4998c-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4998c-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4998c-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4998c-157">INPUTS</span></span>

### <span data-ttu-id="4998c-158">System. String</span><span class="sxs-lookup"><span data-stu-id="4998c-158">System.String</span></span>
<span data-ttu-id="4998c-159">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4998c-159">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="4998c-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4998c-160">OUTPUTS</span></span>

### <span data-ttu-id="4998c-161">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4998c-161">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="4998c-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4998c-162">NOTES</span></span>

## <span data-ttu-id="4998c-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4998c-163">RELATED LINKS</span></span>

[<span data-ttu-id="4998c-164">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4998c-164">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
