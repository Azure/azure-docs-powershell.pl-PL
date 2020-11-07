---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 3ae1aeb86e96bc3f37142e03c31cebbcf102ad3c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705625"
---
# <span data-ttu-id="a8810-101">New-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="a8810-101">New-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="a8810-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a8810-102">SYNOPSIS</span></span>
<span data-ttu-id="a8810-103">Tworzy jednostkę usługi pod określoną topologią usługi i usługi.</span><span class="sxs-lookup"><span data-stu-id="a8810-103">Creates a service unit under the specified service and service topology.</span></span>

## <span data-ttu-id="a8810-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a8810-104">SYNTAX</span></span>

### <span data-ttu-id="a8810-105">ByTopologyAndServiceNames (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a8810-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a8810-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="a8810-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8810-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="a8810-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8810-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="a8810-108">ByServiceObject</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceObject] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a8810-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="a8810-109">ByServiceResourceId</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a8810-110">Opis</span><span class="sxs-lookup"><span data-stu-id="a8810-110">DESCRIPTION</span></span>
<span data-ttu-id="a8810-111">Polecenie cmdlet **New-AzDeploymentManagerServiceUnit** tworzy usługę w ramach usługi w topologii usług i zwraca obiekt reprezentujący tę jednostkę.</span><span class="sxs-lookup"><span data-stu-id="a8810-111">The **New-AzDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="a8810-112">Określ jednostkę usługi, podając jej nazwę, nazwę usługi, topologię usługi, a następnie nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a8810-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="a8810-113">Polecenie cmdlet zwraca obiekt serviceunit.</span><span class="sxs-lookup"><span data-stu-id="a8810-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="a8810-114">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany w usłudze za pomocą polecenia cmdlet Set-AzDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="a8810-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="a8810-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a8810-115">EXAMPLES</span></span>

### <span data-ttu-id="a8810-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a8810-116">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="a8810-117">To polecenie cmdlet tworzy nową jednostkę usługi o nazwie ContosoService2Storage w ContosoResourceGroup w obszarze ContosoService2 usługi w topologii głównej.</span><span class="sxs-lookup"><span data-stu-id="a8810-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="a8810-118">Pliki szablonów i parametrów są zdefiniowane jako ścieżki względne w lokalizacji źródłowej artefaktu, do której odwołuje się ContosoServiceTopology topologii usług.</span><span class="sxs-lookup"><span data-stu-id="a8810-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="a8810-119">Zasoby zdefiniowane w tym szablonie należy wdrożyć w service2ResourceGroup grupy zasobów docelowych z trybem wdrażania ustawionym na wartość przyrostowa.</span><span class="sxs-lookup"><span data-stu-id="a8810-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="a8810-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="a8810-120">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="a8810-121">To polecenie cmdlet tworzy nową jednostkę usługi o nazwie ContosoService2Storage w ContosoResourceGroup w obszarze ContosoService2 usługi w topologii głównej.</span><span class="sxs-lookup"><span data-stu-id="a8810-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="a8810-122">Odwołania szablonu i parametrów są podane jako identyfikator URI SAS jako identyfikator zasobu źródłowego artefaktu nie podano w ContosoServiceTopology1ie topologii usług.</span><span class="sxs-lookup"><span data-stu-id="a8810-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="a8810-123">Zasoby zdefiniowane w tym szablonie należy wdrożyć w service2ResourceGroup grupy zasobów docelowych, korzystając z trybu wdrażania ustawionego na ukończone.</span><span class="sxs-lookup"><span data-stu-id="a8810-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="a8810-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a8810-124">PARAMETERS</span></span>

### <span data-ttu-id="a8810-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a8810-125">-AsJob</span></span>
<span data-ttu-id="a8810-126">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="a8810-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a8810-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a8810-127">-DefaultProfile</span></span>
<span data-ttu-id="a8810-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a8810-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a8810-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="a8810-129">-DeploymentMode</span></span>
<span data-ttu-id="a8810-130">Tryb wdrażania, który ma być używany podczas wdrażania zasobów w jednostce usługi.</span><span class="sxs-lookup"><span data-stu-id="a8810-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="a8810-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="a8810-131">-Location</span></span>
<span data-ttu-id="a8810-132">Lokalizacja zasobu jednostki usług.</span><span class="sxs-lookup"><span data-stu-id="a8810-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="a8810-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a8810-133">-Name</span></span>
<span data-ttu-id="a8810-134">Nazwa jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="a8810-134">The name of the service unit.</span></span>

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

### <span data-ttu-id="a8810-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="a8810-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="a8810-136">Ścieżka do pliku parametrów względem źródła artefaktu.</span><span class="sxs-lookup"><span data-stu-id="a8810-136">The path to the parameters file relative to the artifact source.</span></span>
<span data-ttu-id="a8810-137">Wymaga odwołania do ArtifactSource w usłudze servicetopology.</span><span class="sxs-lookup"><span data-stu-id="a8810-137">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="a8810-138">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="a8810-138">-ParametersUri</span></span>
<span data-ttu-id="a8810-139">Identyfikator URI SAS do pliku parametrów.</span><span class="sxs-lookup"><span data-stu-id="a8810-139">The SAS Uri to the parameters file.</span></span>
<span data-ttu-id="a8810-140">Jeśli w usłudze servicetopology odwołuje się ArtifactSourceId, określ ścieżkę względną przy użyciu ParametersArtifactSourceRelativePath.</span><span class="sxs-lookup"><span data-stu-id="a8810-140">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using ParametersArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="a8810-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a8810-141">-ResourceGroupName</span></span>
<span data-ttu-id="a8810-142">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="a8810-142">The resource group.</span></span>

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

### <span data-ttu-id="a8810-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a8810-143">-ServiceName</span></span>
<span data-ttu-id="a8810-144">Nazwa usługi, do której należy ta jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="a8810-144">The name of the service this service unit is a part of.</span></span>

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

### <span data-ttu-id="a8810-145">-Serviceobject</span><span class="sxs-lookup"><span data-stu-id="a8810-145">-ServiceObject</span></span>
<span data-ttu-id="a8810-146">Obiekt usługi, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="a8810-146">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="a8810-147">-Serviceresourceid</span><span class="sxs-lookup"><span data-stu-id="a8810-147">-ServiceResourceId</span></span>
<span data-ttu-id="a8810-148">Identyfikator zasobu usługi, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="a8810-148">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="a8810-149">-Servicetopologyname</span><span class="sxs-lookup"><span data-stu-id="a8810-149">-ServiceTopologyName</span></span>
<span data-ttu-id="a8810-150">Nazwa topologii usługi, do której należy ta jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="a8810-150">The name of the service topology this service unit is a part of.</span></span>

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

### <span data-ttu-id="a8810-151">-Servicetopologyobject</span><span class="sxs-lookup"><span data-stu-id="a8810-151">-ServiceTopologyObject</span></span>
<span data-ttu-id="a8810-152">Obiekt z topologią usług, w którym należy utworzyć jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="a8810-152">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="a8810-153">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="a8810-153">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="a8810-154">Identyfikator zasobu topologii usług, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="a8810-154">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="a8810-155">-Tag</span><span class="sxs-lookup"><span data-stu-id="a8810-155">-Tag</span></span>
<span data-ttu-id="a8810-156">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="a8810-156">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="a8810-157">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a8810-157">-TargetResourceGroup</span></span>
<span data-ttu-id="a8810-158">Określa lokalizację, do której będą wdrażane zasoby w ramach jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="a8810-158">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="a8810-159">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="a8810-159">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="a8810-160">Ścieżka do pliku szablonu względem źródła artefaktu.</span><span class="sxs-lookup"><span data-stu-id="a8810-160">The path to the template file relative to the artifact source.</span></span>
<span data-ttu-id="a8810-161">Wymaga odwołania do ArtifactSource w usłudze servicetopology.</span><span class="sxs-lookup"><span data-stu-id="a8810-161">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="a8810-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="a8810-162">-TemplateUri</span></span>
<span data-ttu-id="a8810-163">Identyfikator URI SAS do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="a8810-163">The SAS Uri to the template file.</span></span>
<span data-ttu-id="a8810-164">Jeśli w usłudze servicetopology odwołuje się ArtifactSourceId, określ ścieżkę względną przy użyciu TemplateArtifactSourceRelativePath.</span><span class="sxs-lookup"><span data-stu-id="a8810-164">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using TemplateArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="a8810-165">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a8810-165">-Confirm</span></span>
<span data-ttu-id="a8810-166">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8810-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a8810-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a8810-167">-WhatIf</span></span>
<span data-ttu-id="a8810-168">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a8810-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a8810-169">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a8810-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a8810-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a8810-170">CommonParameters</span></span>
<span data-ttu-id="a8810-171">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a8810-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a8810-172">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a8810-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a8810-173">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a8810-173">INPUTS</span></span>

### <span data-ttu-id="a8810-174">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="a8810-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="a8810-175">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a8810-175">OUTPUTS</span></span>

### <span data-ttu-id="a8810-176">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="a8810-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="a8810-177">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a8810-177">NOTES</span></span>

## <span data-ttu-id="a8810-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a8810-178">RELATED LINKS</span></span>