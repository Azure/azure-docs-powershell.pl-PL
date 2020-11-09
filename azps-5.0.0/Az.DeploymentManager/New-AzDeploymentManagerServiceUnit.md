---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 9a03dd861ee380b0ab01348e01091844240bfc04
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304951"
---
# <span data-ttu-id="52098-101">New-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="52098-101">New-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="52098-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="52098-102">SYNOPSIS</span></span>
<span data-ttu-id="52098-103">Tworzy jednostkę usługi pod określoną topologią usługi i usługi.</span><span class="sxs-lookup"><span data-stu-id="52098-103">Creates a service unit under the specified service and service topology.</span></span>

## <span data-ttu-id="52098-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="52098-104">SYNTAX</span></span>

### <span data-ttu-id="52098-105">ByTopologyAndServiceNames (domyślny)</span><span class="sxs-lookup"><span data-stu-id="52098-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="52098-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="52098-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52098-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="52098-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52098-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="52098-108">ByServiceObject</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceObject] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="52098-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="52098-109">ByServiceResourceId</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52098-110">Opis</span><span class="sxs-lookup"><span data-stu-id="52098-110">DESCRIPTION</span></span>
<span data-ttu-id="52098-111">Polecenie cmdlet **New-AzDeploymentManagerServiceUnit** tworzy usługę w ramach usługi w topologii usług i zwraca obiekt reprezentujący tę jednostkę.</span><span class="sxs-lookup"><span data-stu-id="52098-111">The **New-AzDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="52098-112">Określ jednostkę usługi, podając jej nazwę, nazwę usługi, topologię usługi, a następnie nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="52098-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="52098-113">Polecenie cmdlet zwraca obiekt serviceunit.</span><span class="sxs-lookup"><span data-stu-id="52098-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="52098-114">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany w usłudze za pomocą polecenia cmdlet Set-AzDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="52098-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="52098-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="52098-115">EXAMPLES</span></span>

### <span data-ttu-id="52098-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="52098-116">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="52098-117">To polecenie cmdlet tworzy nową jednostkę usługi o nazwie ContosoService2Storage w ContosoResourceGroup w obszarze ContosoService2 usługi w topologii głównej.</span><span class="sxs-lookup"><span data-stu-id="52098-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="52098-118">Pliki szablonów i parametrów są zdefiniowane jako ścieżki względne w lokalizacji źródłowej artefaktu, do której odwołuje się ContosoServiceTopology topologii usług.</span><span class="sxs-lookup"><span data-stu-id="52098-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="52098-119">Zasoby zdefiniowane w tym szablonie należy wdrożyć w service2ResourceGroup grupy zasobów docelowych z trybem wdrażania ustawionym na wartość przyrostowa.</span><span class="sxs-lookup"><span data-stu-id="52098-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="52098-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="52098-120">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="52098-121">To polecenie cmdlet tworzy nową jednostkę usługi o nazwie ContosoService2Storage w ContosoResourceGroup w obszarze ContosoService2 usługi w topologii głównej.</span><span class="sxs-lookup"><span data-stu-id="52098-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="52098-122">Odwołania szablonu i parametrów są podane jako identyfikator URI SAS jako identyfikator zasobu źródłowego artefaktu nie podano w ContosoServiceTopology1ie topologii usług.</span><span class="sxs-lookup"><span data-stu-id="52098-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="52098-123">Zasoby zdefiniowane w tym szablonie należy wdrożyć w service2ResourceGroup grupy zasobów docelowych, korzystając z trybu wdrażania ustawionego na ukończone.</span><span class="sxs-lookup"><span data-stu-id="52098-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="52098-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="52098-124">PARAMETERS</span></span>

### <span data-ttu-id="52098-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="52098-125">-AsJob</span></span>
<span data-ttu-id="52098-126">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="52098-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="52098-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52098-127">-DefaultProfile</span></span>
<span data-ttu-id="52098-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="52098-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52098-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="52098-129">-DeploymentMode</span></span>
<span data-ttu-id="52098-130">Tryb wdrażania, który ma być używany podczas wdrażania zasobów w jednostce usługi.</span><span class="sxs-lookup"><span data-stu-id="52098-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Incremental, Complete

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52098-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="52098-131">-Location</span></span>
<span data-ttu-id="52098-132">Lokalizacja zasobu jednostki usług.</span><span class="sxs-lookup"><span data-stu-id="52098-132">The location of the service unit resource.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52098-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="52098-133">-Name</span></span>
<span data-ttu-id="52098-134">Nazwa jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="52098-134">The name of the service unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52098-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="52098-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="52098-136">Ścieżka do pliku parametrów względem źródła artefaktu.</span><span class="sxs-lookup"><span data-stu-id="52098-136">The path to the parameters file relative to the artifact source.</span></span>
<span data-ttu-id="52098-137">Wymaga odwołania do ArtifactSource w usłudze servicetopology.</span><span class="sxs-lookup"><span data-stu-id="52098-137">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="52098-138">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="52098-138">-ParametersUri</span></span>
<span data-ttu-id="52098-139">Identyfikator URI SAS do pliku parametrów.</span><span class="sxs-lookup"><span data-stu-id="52098-139">The SAS Uri to the parameters file.</span></span>
<span data-ttu-id="52098-140">Jeśli w usłudze servicetopology odwołuje się ArtifactSourceId, określ ścieżkę względną przy użyciu ParametersArtifactSourceRelativePath.</span><span class="sxs-lookup"><span data-stu-id="52098-140">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using ParametersArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="52098-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="52098-141">-ResourceGroupName</span></span>
<span data-ttu-id="52098-142">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="52098-142">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52098-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="52098-143">-ServiceName</span></span>
<span data-ttu-id="52098-144">Nazwa usługi, do której należy ta jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="52098-144">The name of the service this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames, ByTopologyObjectAndServiceName, ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52098-145">-Serviceobject</span><span class="sxs-lookup"><span data-stu-id="52098-145">-ServiceObject</span></span>
<span data-ttu-id="52098-146">Obiekt usługi, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="52098-146">The service object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: ByServiceObject
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52098-147">-Serviceresourceid</span><span class="sxs-lookup"><span data-stu-id="52098-147">-ServiceResourceId</span></span>
<span data-ttu-id="52098-148">Identyfikator zasobu usługi, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="52098-148">The service resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52098-149">-Servicetopologyname</span><span class="sxs-lookup"><span data-stu-id="52098-149">-ServiceTopologyName</span></span>
<span data-ttu-id="52098-150">Nazwa topologii usługi, do której należy ta jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="52098-150">The name of the service topology this service unit is a part of.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyAndServiceNames
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52098-151">-Servicetopologyobject</span><span class="sxs-lookup"><span data-stu-id="52098-151">-ServiceTopologyObject</span></span>
<span data-ttu-id="52098-152">Obiekt z topologią usług, w którym należy utworzyć jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="52098-152">The service topology object in which the service unit should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByTopologyObjectAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52098-153">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="52098-153">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="52098-154">Identyfikator zasobu topologii usług, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="52098-154">The service topology resource identifier in which the service unit should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTopologyResourceAndServiceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52098-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="52098-155">-Tag</span></span>
<span data-ttu-id="52098-156">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="52098-156">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52098-157">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="52098-157">-TargetResourceGroup</span></span>
<span data-ttu-id="52098-158">Określa lokalizację, do której będą wdrażane zasoby w ramach jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="52098-158">Determines the location where resources under the service unit would be deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52098-159">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="52098-159">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="52098-160">Ścieżka do pliku szablonu względem źródła artefaktu.</span><span class="sxs-lookup"><span data-stu-id="52098-160">The path to the template file relative to the artifact source.</span></span>
<span data-ttu-id="52098-161">Wymaga odwołania do ArtifactSource w usłudze servicetopology.</span><span class="sxs-lookup"><span data-stu-id="52098-161">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="52098-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="52098-162">-TemplateUri</span></span>
<span data-ttu-id="52098-163">Identyfikator URI SAS do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="52098-163">The SAS Uri to the template file.</span></span>
<span data-ttu-id="52098-164">Jeśli w usłudze servicetopology odwołuje się ArtifactSourceId, określ ścieżkę względną przy użyciu TemplateArtifactSourceRelativePath.</span><span class="sxs-lookup"><span data-stu-id="52098-164">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using TemplateArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="52098-165">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="52098-165">-Confirm</span></span>
<span data-ttu-id="52098-166">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52098-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52098-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52098-167">-WhatIf</span></span>
<span data-ttu-id="52098-168">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52098-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52098-169">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="52098-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52098-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52098-170">CommonParameters</span></span>
<span data-ttu-id="52098-171">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52098-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52098-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="52098-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52098-173">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52098-173">INPUTS</span></span>

### <span data-ttu-id="52098-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="52098-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="52098-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="52098-175">OUTPUTS</span></span>

### <span data-ttu-id="52098-176">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="52098-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="52098-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="52098-177">NOTES</span></span>

## <span data-ttu-id="52098-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52098-178">RELATED LINKS</span></span>
