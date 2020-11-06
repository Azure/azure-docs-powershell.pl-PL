---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactories/Commands.DataFactoryV2/help/Set-AzureRmDataFactoryV2IntegrationRuntime.md
gitcommit: https://github.com/Azure/azure-powershell/blob/db8032a9100d47fd3aa4248c7807d8e0bb538e83
ms.openlocfilehash: f24d42f1c4648343b979586ee906913f5d6a07f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93554382"
---
# <span data-ttu-id="c6823-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c6823-101">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>

## <span data-ttu-id="c6823-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c6823-102">SYNOPSIS</span></span>
<span data-ttu-id="c6823-103">Aktualizuje środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="c6823-103">Updates an integration runtime.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c6823-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c6823-104">SYNTAX</span></span>

### <span data-ttu-id="c6823-105">ByIntegrationRuntimeName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c6823-105">ByIntegrationRuntimeName (Default)</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-Name] <String> [-ResourceGroupName] <String>
 [-DataFactoryName] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c6823-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="c6823-106">ByResourceId</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-ResourceId] <String> [-WhatIf] [-Confirm]
```

### <span data-ttu-id="c6823-107">ByIntegrationRuntimeObject</span><span class="sxs-lookup"><span data-stu-id="c6823-107">ByIntegrationRuntimeObject</span></span>
```
Set-AzureRmDataFactoryV2IntegrationRuntime [-Type <String>] [-Description <String>] [-Location <String>]
 [-NodeSize <String>] [-NodeCount <Int32>] [-CatalogServerEndpoint <String>]
 [-CatalogAdminCredential <PSCredential>] [-CatalogPricingTier <String>] [-VNetId <String>] [-Subnet <String>]
 [-MaxParallelExecutionsPerNode <Int32>] [-Force] [-InputObject] <PSIntegrationRuntime> [-WhatIf]
 [-Confirm]
```

## <span data-ttu-id="c6823-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c6823-108">DESCRIPTION</span></span>
<span data-ttu-id="c6823-109">Polecenie cmdlet Set-AzureRmDataFactoryV2IntegrationRuntime aktualizuje środowisko uruchomieniowe integracji z określonymi parametrami.</span><span class="sxs-lookup"><span data-stu-id="c6823-109">The Set-AzureRmDataFactoryV2IntegrationRuntime cmdlet updates an integration runtime with specific parameters.</span></span>

## <span data-ttu-id="c6823-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c6823-110">EXAMPLES</span></span>

### <span data-ttu-id="c6823-111">Przykład 1: Opis aktualizacji środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="c6823-111">Example 1: Update integration runtime description.</span></span>
```
PS C:\> Set-AzureRmDataFactoryV2IntegrationRuntime -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2' -Name 'test-selfhost-ir' `
                                            -Description 'New description'

    Id                : /subscriptions/b3ee3a7f-7614-4644-ad07-afa832620b4b/resourceGroups/rg-test-dfv2/providers/Microsoft.DataFactory/factories/test-df-eu2/integrationruntimes/test-selfhost-ir
    ResourceGroupName : rg-test-dfv2
    DataFactoryName   : test-df-eu2
    Name              : test-selfhost-ir
    Description       : New description

```

<span data-ttu-id="c6823-112">Polecenie cmdlet aktualizuje Opis środowiska wykonawczego integracji o nazwie test-SelfHost-IR '.</span><span class="sxs-lookup"><span data-stu-id="c6823-112">The cmdlet updates the description of integration runtime named 'test-selfhost-ir'.</span></span>

## <span data-ttu-id="c6823-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c6823-113">PARAMETERS</span></span>

### <span data-ttu-id="c6823-114">-CatalogAdminCredential</span><span class="sxs-lookup"><span data-stu-id="c6823-114">-CatalogAdminCredential</span></span>
<span data-ttu-id="c6823-115">Poświadczenia administratora bazy danych wykazu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="c6823-115">The catalog database administrator credential of the integration runtime.</span></span>

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

### <span data-ttu-id="c6823-116">-CatalogPricingTier</span><span class="sxs-lookup"><span data-stu-id="c6823-116">-CatalogPricingTier</span></span>
<span data-ttu-id="c6823-117">Warstwa cenowa bazy danych katalogu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="c6823-117">The catalog database pricing tier of the integration runtime.</span></span>

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

### <span data-ttu-id="c6823-118">-CatalogServerEndpoint</span><span class="sxs-lookup"><span data-stu-id="c6823-118">-CatalogServerEndpoint</span></span>
<span data-ttu-id="c6823-119">Punkt końcowy serwera bazy danych wykazu w środowisku wykonawczym integracji.</span><span class="sxs-lookup"><span data-stu-id="c6823-119">The catalog database server endpoint of the integration runtime.</span></span>

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

### <span data-ttu-id="c6823-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c6823-120">-Confirm</span></span>
<span data-ttu-id="c6823-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6823-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6823-122">-Datafactoryname</span><span class="sxs-lookup"><span data-stu-id="c6823-122">-DataFactoryName</span></span>
<span data-ttu-id="c6823-123">Nazwa fabryki danych.</span><span class="sxs-lookup"><span data-stu-id="c6823-123">The data factory name.</span></span>

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

### <span data-ttu-id="c6823-124">— Opis</span><span class="sxs-lookup"><span data-stu-id="c6823-124">-Description</span></span>
<span data-ttu-id="c6823-125">Opis środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="c6823-125">The integration runtime description.</span></span>

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

### <span data-ttu-id="c6823-126">-Force</span><span class="sxs-lookup"><span data-stu-id="c6823-126">-Force</span></span>
<span data-ttu-id="c6823-127">Uruchamia polecenie cmdlet bez monitowania o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c6823-127">Runs the cmdlet without prompting for confirmation.</span></span>

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

### <span data-ttu-id="c6823-128">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="c6823-128">-InputObject</span></span>
<span data-ttu-id="c6823-129">Obiekt środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="c6823-129">The integration runtime object.</span></span>

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

### <span data-ttu-id="c6823-130">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c6823-130">-Location</span></span>
<span data-ttu-id="c6823-131">Lokalizacja środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="c6823-131">The integration runtime location.</span></span>

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

### <span data-ttu-id="c6823-132">-MaxParallelExecutionsPerNode</span><span class="sxs-lookup"><span data-stu-id="c6823-132">-MaxParallelExecutionsPerNode</span></span>
<span data-ttu-id="c6823-133">Maksymalna liczba równoległych operacji na węzeł dla zarządzanego dedykowanego środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="c6823-133">Maximum parallel execution count per node for a managed dedicated integration runtime.</span></span>

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

### <span data-ttu-id="c6823-134">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c6823-134">-Name</span></span>
<span data-ttu-id="c6823-135">Nazwa środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="c6823-135">The integration runtime name.</span></span>

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

### <span data-ttu-id="c6823-136">-NodeCount</span><span class="sxs-lookup"><span data-stu-id="c6823-136">-NodeCount</span></span>
<span data-ttu-id="c6823-137">Liczba węzłów docelowych środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="c6823-137">Target nodes count of the integration runtime.</span></span>

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

### <span data-ttu-id="c6823-138">-NodeSize</span><span class="sxs-lookup"><span data-stu-id="c6823-138">-NodeSize</span></span>
<span data-ttu-id="c6823-139">Rozmiar węzła środowiska uruchomieniowego integracji.</span><span class="sxs-lookup"><span data-stu-id="c6823-139">The integration runtime node size.</span></span>

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

### <span data-ttu-id="c6823-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6823-140">-ResourceGroupName</span></span>
<span data-ttu-id="c6823-141">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="c6823-141">The resource group name.</span></span>

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

### <span data-ttu-id="c6823-142">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c6823-142">-ResourceId</span></span>
<span data-ttu-id="c6823-143">Identyfikator zasobu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c6823-143">The Azure resource ID.</span></span>

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

### <span data-ttu-id="c6823-144">-Podsieć</span><span class="sxs-lookup"><span data-stu-id="c6823-144">-Subnet</span></span>
<span data-ttu-id="c6823-145">Nazwa podsieci w sieci wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="c6823-145">The name of the subnet in the VNet.</span></span>

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

### <span data-ttu-id="c6823-146">-Type</span><span class="sxs-lookup"><span data-stu-id="c6823-146">-Type</span></span>
<span data-ttu-id="c6823-147">Typ środowiska wykonawczego integracji.</span><span class="sxs-lookup"><span data-stu-id="c6823-147">The integration runtime type.</span></span>

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

### <span data-ttu-id="c6823-148">-VNetId</span><span class="sxs-lookup"><span data-stu-id="c6823-148">-VNetId</span></span>
<span data-ttu-id="c6823-149">Identyfikator sieci wirtualnej, z którą łączy się środowisko uruchomieniowe integracji.</span><span class="sxs-lookup"><span data-stu-id="c6823-149">The ID of the VNet that the integration runtime joins.</span></span>

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

### <span data-ttu-id="c6823-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6823-150">-WhatIf</span></span>
<span data-ttu-id="c6823-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet, ale nie jest uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c6823-151">Shows what happens if the cmdlet runs, but doesn't run the cmdlet.</span></span>

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

## <span data-ttu-id="c6823-152">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c6823-152">INPUTS</span></span>

### <span data-ttu-id="c6823-153">System. String</span><span class="sxs-lookup"><span data-stu-id="c6823-153">System.String</span></span>
<span data-ttu-id="c6823-154">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c6823-154">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c6823-155">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c6823-155">OUTPUTS</span></span>

### <span data-ttu-id="c6823-156">Microsoft. Azure. Commands. DataFactoryV2. models. PSIntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c6823-156">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="c6823-157">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c6823-157">NOTES</span></span>

## <span data-ttu-id="c6823-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c6823-158">RELATED LINKS</span></span>
[<span data-ttu-id="c6823-159">Set-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="c6823-159">Set-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()
