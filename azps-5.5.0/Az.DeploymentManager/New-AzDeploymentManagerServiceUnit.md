---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerserviceunit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceUnit.md
ms.openlocfilehash: 9a03dd861ee380b0ab01348e01091844240bfc04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242698"
---
# <span data-ttu-id="cdb35-101">New-AzDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="cdb35-101">New-AzDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="cdb35-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cdb35-102">SYNOPSIS</span></span>
<span data-ttu-id="cdb35-103">Tworzy jednostkę usługi w ramach określonej topologii usług i usług.</span><span class="sxs-lookup"><span data-stu-id="cdb35-103">Creates a service unit under the specified service and service topology.</span></span>

## <span data-ttu-id="cdb35-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="cdb35-104">SYNTAX</span></span>

### <span data-ttu-id="cdb35-105">ByTopologyAndServiceNames (domyślne)</span><span class="sxs-lookup"><span data-stu-id="cdb35-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="cdb35-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="cdb35-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopologyObject] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdb35-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="cdb35-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdb35-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="cdb35-108">ByServiceObject</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceObject] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cdb35-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="cdb35-109">ByServiceResourceId</span></span>
```
New-AzDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cdb35-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="cdb35-110">DESCRIPTION</span></span>
<span data-ttu-id="cdb35-111">Polecenie **cmdlet New-AzDeploymentManagerServiceUnit** tworzy usługę w topologii usługi i zwraca obiekt reprezentujący jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="cdb35-111">The **New-AzDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="cdb35-112">Określ jednostkę usługi według jej nazwy, nazwy usługi, topologii usługi, w których się znajduje, oraz nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cdb35-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="cdb35-113">Polecenie cmdlet zwraca obiekt ServiceUnit.</span><span class="sxs-lookup"><span data-stu-id="cdb35-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="cdb35-114">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany do usługi za pomocą Set-AzDeploymentManagerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdb35-114">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="cdb35-115">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="cdb35-115">EXAMPLES</span></span>

### <span data-ttu-id="cdb35-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cdb35-116">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="cdb35-117">To polecenie cmdlet tworzy nową jednostkę usługi o nazwie ContosoService2Storage w grupie ContosoResourceGroup w obszarze usługi ContosoService2 w topologii ContosoServiceTopology w lokalizacji Centralnej Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="cdb35-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="cdb35-118">Pliki szablonu i parametrów są zdefiniowane jako ścieżki względne do lokalizacji źródła artefaktu, do których odwołuje się topologia usługi ContosoServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="cdb35-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="cdb35-119">Zasoby zdefiniowane w tym szablonie należy wdrożyć w grupie docelowej service2ResourceGroup z trybem wdrażania ustawionym na wartość Przyrostowe.</span><span class="sxs-lookup"><span data-stu-id="cdb35-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="cdb35-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="cdb35-120">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="cdb35-121">To polecenie cmdlet tworzy nową jednostkę usługi o nazwie ContosoService2Storage w grupie ContosoResourceGroup w obszarze usługi ContosoService2 w topologii ContosoServiceTopology w lokalizacji Centralnej Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="cdb35-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="cdb35-122">Odwołania do szablonu i parametrów są udostępniane jako wartości Uri SAS, ponieważ w topologii usługi ContosoServiceTopology1 nie podano wartości ResourceId źródła artefaktu.</span><span class="sxs-lookup"><span data-stu-id="cdb35-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="cdb35-123">Zasoby zdefiniowane w tym szablonie należy wdrożyć w grupie docelowej service2ResourceGroup z trybem wdrażania ustawionym na wartość Ukończono.</span><span class="sxs-lookup"><span data-stu-id="cdb35-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="cdb35-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="cdb35-124">PARAMETERS</span></span>

### <span data-ttu-id="cdb35-125">— AsJob</span><span class="sxs-lookup"><span data-stu-id="cdb35-125">-AsJob</span></span>
<span data-ttu-id="cdb35-126">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cdb35-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cdb35-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cdb35-127">-DefaultProfile</span></span>
<span data-ttu-id="cdb35-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="cdb35-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cdb35-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="cdb35-129">-DeploymentMode</span></span>
<span data-ttu-id="cdb35-130">Tryb wdrażania do użycia podczas wdrażania zasobów w jednostce usługi.</span><span class="sxs-lookup"><span data-stu-id="cdb35-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="cdb35-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="cdb35-131">-Location</span></span>
<span data-ttu-id="cdb35-132">Lokalizacja zasobu jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="cdb35-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="cdb35-133">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="cdb35-133">-Name</span></span>
<span data-ttu-id="cdb35-134">Nazwa jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="cdb35-134">The name of the service unit.</span></span>

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

### <span data-ttu-id="cdb35-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="cdb35-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="cdb35-136">Ścieżka do pliku parametrów względem źródła artefaktu.</span><span class="sxs-lookup"><span data-stu-id="cdb35-136">The path to the parameters file relative to the artifact source.</span></span>
<span data-ttu-id="cdb35-137">Wymaga odwoływać się do źródła ArtifactSource w ologii ServiceTopologii.</span><span class="sxs-lookup"><span data-stu-id="cdb35-137">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="cdb35-138">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="cdb35-138">-ParametersUri</span></span>
<span data-ttu-id="cdb35-139">Uri SAS do pliku parametrów.</span><span class="sxs-lookup"><span data-stu-id="cdb35-139">The SAS Uri to the parameters file.</span></span>
<span data-ttu-id="cdb35-140">Jeśli w ologii ServiceTopologii dowoływano się do wartości ArtifactSourceId, określ ścieżkę względną przy użyciu parametru ParametersArtifactSourceRelativePath.</span><span class="sxs-lookup"><span data-stu-id="cdb35-140">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using ParametersArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="cdb35-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cdb35-141">-ResourceGroupName</span></span>
<span data-ttu-id="cdb35-142">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="cdb35-142">The resource group.</span></span>

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

### <span data-ttu-id="cdb35-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="cdb35-143">-ServiceName</span></span>
<span data-ttu-id="cdb35-144">Nazwa usługi, do których należy ta jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="cdb35-144">The name of the service this service unit is a part of.</span></span>

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

### <span data-ttu-id="cdb35-145">-ServiceObject</span><span class="sxs-lookup"><span data-stu-id="cdb35-145">-ServiceObject</span></span>
<span data-ttu-id="cdb35-146">Obiekt usługi, w którym powinna zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="cdb35-146">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="cdb35-147">-ServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="cdb35-147">-ServiceResourceId</span></span>
<span data-ttu-id="cdb35-148">Identyfikator zasobu usługi, w którym powinna zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="cdb35-148">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="cdb35-149">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="cdb35-149">-ServiceTopologyName</span></span>
<span data-ttu-id="cdb35-150">Nazwa topologii usługi, do których należy ta jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="cdb35-150">The name of the service topology this service unit is a part of.</span></span>

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

### <span data-ttu-id="cdb35-151">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="cdb35-151">-ServiceTopologyObject</span></span>
<span data-ttu-id="cdb35-152">Obiekt topologii usługi, w którym powinna zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="cdb35-152">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="cdb35-153">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="cdb35-153">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="cdb35-154">Identyfikator zasobu topologii usługi, w którym powinna zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="cdb35-154">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="cdb35-155">— Tag</span><span class="sxs-lookup"><span data-stu-id="cdb35-155">-Tag</span></span>
<span data-ttu-id="cdb35-156">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="cdb35-156">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="cdb35-157">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="cdb35-157">-TargetResourceGroup</span></span>
<span data-ttu-id="cdb35-158">Określa lokalizację, w której zostaną wdrożone zasoby w ramach jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="cdb35-158">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="cdb35-159">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="cdb35-159">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="cdb35-160">Ścieżka do pliku szablonu względem źródła artefaktu.</span><span class="sxs-lookup"><span data-stu-id="cdb35-160">The path to the template file relative to the artifact source.</span></span>
<span data-ttu-id="cdb35-161">Wymaga odwoływać się do źródła ArtifactSource w ologii ServiceTopologii.</span><span class="sxs-lookup"><span data-stu-id="cdb35-161">Requires ArtifactSource to be referenced in ServiceTopology.</span></span>

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

### <span data-ttu-id="cdb35-162">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="cdb35-162">-TemplateUri</span></span>
<span data-ttu-id="cdb35-163">Uri SAS do pliku szablonu.</span><span class="sxs-lookup"><span data-stu-id="cdb35-163">The SAS Uri to the template file.</span></span>
<span data-ttu-id="cdb35-164">Jeśli w ologii ServiceTopologii dowoływano się do wartości ArtifactSourceId, określ ścieżkę względną przy użyciu szablonu TemplateArtifactSourceRelativePath.</span><span class="sxs-lookup"><span data-stu-id="cdb35-164">If ArtifactSourceId was referenced in the ServiceTopology, specify relative path using TemplateArtifactSourceRelativePath.</span></span>

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

### <span data-ttu-id="cdb35-165">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cdb35-165">-Confirm</span></span>
<span data-ttu-id="cdb35-166">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="cdb35-166">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cdb35-167">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cdb35-167">-WhatIf</span></span>
<span data-ttu-id="cdb35-168">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cdb35-168">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cdb35-169">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="cdb35-169">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cdb35-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cdb35-170">CommonParameters</span></span>
<span data-ttu-id="cdb35-171">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cdb35-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cdb35-172">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="cdb35-172">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cdb35-173">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cdb35-173">INPUTS</span></span>

### <span data-ttu-id="cdb35-174">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="cdb35-174">System.Collections.Hashtable</span></span>

## <span data-ttu-id="cdb35-175">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="cdb35-175">OUTPUTS</span></span>

### <span data-ttu-id="cdb35-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="cdb35-176">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="cdb35-177">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="cdb35-177">NOTES</span></span>

## <span data-ttu-id="cdb35-178">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cdb35-178">RELATED LINKS</span></span>
