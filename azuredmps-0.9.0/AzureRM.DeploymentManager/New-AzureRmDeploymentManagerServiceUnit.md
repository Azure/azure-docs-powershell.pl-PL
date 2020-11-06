---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerserviceunit
schema: 2.0.0
ms.openlocfilehash: e732463984088bbcb507eb55594f7de2114d25d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523086"
---
# <span data-ttu-id="26e3e-101">New-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="26e3e-101">New-AzureRmDeploymentManagerServiceUnit</span></span>

## <span data-ttu-id="26e3e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="26e3e-102">SYNOPSIS</span></span>
<span data-ttu-id="26e3e-103">Tworzy nową jednostkę usługi w ramach usługi w topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="26e3e-103">Creates a new service unit under a service in a service topology.</span></span>

## <span data-ttu-id="26e3e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="26e3e-104">SYNTAX</span></span>

### <span data-ttu-id="26e3e-105">ByTopologyAndServiceNames (domyślny)</span><span class="sxs-lookup"><span data-stu-id="26e3e-105">ByTopologyAndServiceNames (Default)</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-ServiceName] <String> [-Name] <String> -Location <String> -TargetResourceGroup <String>
 -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="26e3e-106">ByTopologyObjectAndServiceName</span><span class="sxs-lookup"><span data-stu-id="26e3e-106">ByTopologyObjectAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>]
 [-ServiceTopology] <PSServiceTopologyResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e3e-107">ByTopologyResourceAndServiceName</span><span class="sxs-lookup"><span data-stu-id="26e3e-107">ByTopologyResourceAndServiceName</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-ServiceName] <String> [-Name] <String>
 -Location <String> -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>]
 [-TemplateUri <String>] [-TemplateArtifactSourceRelativePath <String>]
 [-ParametersArtifactSourceRelativePath <String>] [-Tag <Hashtable>] [-ServiceTopologyResourceId] <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e3e-108">ByServiceObject</span><span class="sxs-lookup"><span data-stu-id="26e3e-108">ByServiceObject</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-Service] <PSServiceResource> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="26e3e-109">ByServiceResourceId</span><span class="sxs-lookup"><span data-stu-id="26e3e-109">ByServiceResourceId</span></span>
```
New-AzureRmDeploymentManagerServiceUnit [-ResourceGroupName] <String> [-Name] <String> -Location <String>
 -TargetResourceGroup <String> -DeploymentMode <String> [-ParametersUri <String>] [-TemplateUri <String>]
 [-TemplateArtifactSourceRelativePath <String>] [-ParametersArtifactSourceRelativePath <String>]
 [-Tag <Hashtable>] [-ServiceResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26e3e-110">Opis</span><span class="sxs-lookup"><span data-stu-id="26e3e-110">DESCRIPTION</span></span>
<span data-ttu-id="26e3e-111">Polecenie cmdlet **New-AzureRmDeploymentManagerServiceUnit** tworzy usługę w ramach usługi w topologii usług i zwraca obiekt reprezentujący tę jednostkę.</span><span class="sxs-lookup"><span data-stu-id="26e3e-111">The **New-AzureRmDeploymentManagerServiceUnit** cmdlet creates a service under a service in a service topology, and returns an object that represents that service unit.</span></span>
<span data-ttu-id="26e3e-112">Określ jednostkę usługi, podając jej nazwę, nazwę usługi, topologię usługi, a następnie nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="26e3e-112">Specify the service unit by its name, service name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="26e3e-113">Polecenie cmdlet zwraca obiekt serviceunit.</span><span class="sxs-lookup"><span data-stu-id="26e3e-113">The cmdlet returns a ServiceUnit object.</span></span> <span data-ttu-id="26e3e-114">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany w usłudze za pomocą polecenia cmdlet Set-AzureRmDeploymentManagerService.</span><span class="sxs-lookup"><span data-stu-id="26e3e-114">You can modify this object locally, and then apply changes to the service by using the Set-AzureRmDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="26e3e-115">Przykłady</span><span class="sxs-lookup"><span data-stu-id="26e3e-115">EXAMPLES</span></span>

### <span data-ttu-id="26e3e-116">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="26e3e-116">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Incremental -TemplateArtifactSourceRelativePath "Templates/Service2.Storage.json" -ParametersArtifactSourceRelativePath "Parameters/Service2Storage.Parameters.json"
```

<span data-ttu-id="26e3e-117">To polecenie cmdlet tworzy nową jednostkę usługi o nazwie ContosoService2Storage w ContosoResourceGroup w obszarze ContosoService2 usługi w topologii głównej.</span><span class="sxs-lookup"><span data-stu-id="26e3e-117">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="26e3e-118">Pliki szablonów i parametrów są zdefiniowane jako ścieżki względne w lokalizacji źródłowej artefaktu, do której odwołuje się ContosoServiceTopology topologii usług.</span><span class="sxs-lookup"><span data-stu-id="26e3e-118">The Template and parameters files are defined as relative paths into the artifact source location referenced in the Service Topology ContosoServiceTopology.</span></span> <span data-ttu-id="26e3e-119">Zasoby zdefiniowane w tym szablonie należy wdrożyć w service2ResourceGroup grupy zasobów docelowych z trybem wdrażania ustawionym na wartość przyrostowa.</span><span class="sxs-lookup"><span data-stu-id="26e3e-119">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Incremental.</span></span>

### <span data-ttu-id="26e3e-120">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="26e3e-120">Example 2</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceUnit -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology1 -ServiceName ContosoService2 -Name ContosoService2Storage -Location "Central US" -TargetResourceGroup service2ResourceGroup -DeploymentMode Complete -TemplateUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Templates/Service2.Storage.json?sasParameters" -ParametersUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts/Parameters/Service2Storage.Parameters.json?sasParameters"
```

<span data-ttu-id="26e3e-121">To polecenie cmdlet tworzy nową jednostkę usługi o nazwie ContosoService2Storage w ContosoResourceGroup w obszarze ContosoService2 usługi w topologii głównej.</span><span class="sxs-lookup"><span data-stu-id="26e3e-121">This cmdlet creates a new service unit with name ContosoService2Storage in the ContosoResourceGroup under the service ContosoService2 in topology ContosoServiceTopology, in the location Central US.</span></span> <span data-ttu-id="26e3e-122">Odwołania szablonu i parametrów są podane jako identyfikator URI SAS jako identyfikator zasobu źródłowego artefaktu nie podano w ContosoServiceTopology1ie topologii usług.</span><span class="sxs-lookup"><span data-stu-id="26e3e-122">The Template and parameters references are provided as SAS Uri's as artifact source ResourceId was not provided in the Service Topology ContosoServiceTopology1.</span></span> <span data-ttu-id="26e3e-123">Zasoby zdefiniowane w tym szablonie należy wdrożyć w service2ResourceGroup grupy zasobów docelowych, korzystając z trybu wdrażania ustawionego na ukończone.</span><span class="sxs-lookup"><span data-stu-id="26e3e-123">The resources defined in this template are to be deployed into the target resource group service2ResourceGroup with the deployment mode set to Complete.</span></span>

## <span data-ttu-id="26e3e-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="26e3e-124">PARAMETERS</span></span>

### <span data-ttu-id="26e3e-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="26e3e-125">-AsJob</span></span>
<span data-ttu-id="26e3e-126">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="26e3e-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="26e3e-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26e3e-127">-DefaultProfile</span></span>
<span data-ttu-id="26e3e-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="26e3e-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="26e3e-129">-DeploymentMode</span><span class="sxs-lookup"><span data-stu-id="26e3e-129">-DeploymentMode</span></span>
<span data-ttu-id="26e3e-130">Tryb wdrażania, który ma być używany podczas wdrażania zasobów w jednostce usługi.</span><span class="sxs-lookup"><span data-stu-id="26e3e-130">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="26e3e-131">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="26e3e-131">-Location</span></span>
<span data-ttu-id="26e3e-132">Lokalizacja zasobu jednostki usług.</span><span class="sxs-lookup"><span data-stu-id="26e3e-132">The location of the service unit resource.</span></span>

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

### <span data-ttu-id="26e3e-133">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="26e3e-133">-Name</span></span>
<span data-ttu-id="26e3e-134">Nazwa jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="26e3e-134">The name of the service unit.</span></span>

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

### <span data-ttu-id="26e3e-135">-ParametersArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="26e3e-135">-ParametersArtifactSourceRelativePath</span></span>
<span data-ttu-id="26e3e-136">Tryb wdrażania, który ma być używany podczas wdrażania zasobów w jednostce usługi.</span><span class="sxs-lookup"><span data-stu-id="26e3e-136">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="26e3e-137">-ParametersUri</span><span class="sxs-lookup"><span data-stu-id="26e3e-137">-ParametersUri</span></span>
<span data-ttu-id="26e3e-138">Tryb wdrażania, który ma być używany podczas wdrażania zasobów w jednostce usługi.</span><span class="sxs-lookup"><span data-stu-id="26e3e-138">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="26e3e-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="26e3e-139">-ResourceGroupName</span></span>
<span data-ttu-id="26e3e-140">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="26e3e-140">The resource group.</span></span>

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

### <span data-ttu-id="26e3e-141">-Service</span><span class="sxs-lookup"><span data-stu-id="26e3e-141">-Service</span></span>
<span data-ttu-id="26e3e-142">Obiekt usługi, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="26e3e-142">The service object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="26e3e-143">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="26e3e-143">-ServiceName</span></span>
<span data-ttu-id="26e3e-144">Nazwa usługi, do której należy ta jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="26e3e-144">The name of the service this service unit is a part of.</span></span>

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

### <span data-ttu-id="26e3e-145">-Serviceresourceid</span><span class="sxs-lookup"><span data-stu-id="26e3e-145">-ServiceResourceId</span></span>
<span data-ttu-id="26e3e-146">Identyfikator zasobu usługi, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="26e3e-146">The service resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="26e3e-147">-Servicetopology</span><span class="sxs-lookup"><span data-stu-id="26e3e-147">-ServiceTopology</span></span>
<span data-ttu-id="26e3e-148">Obiekt z topologią usług, w którym należy utworzyć jednostkę usługi.</span><span class="sxs-lookup"><span data-stu-id="26e3e-148">The service topology object in which the service unit should be created.</span></span>

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

### <span data-ttu-id="26e3e-149">-Servicetopologyname</span><span class="sxs-lookup"><span data-stu-id="26e3e-149">-ServiceTopologyName</span></span>
<span data-ttu-id="26e3e-150">Nazwa topologii serivce, której częścią jest ta jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="26e3e-150">The name of the serivce topology this service unit is a part of.</span></span>

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

### <span data-ttu-id="26e3e-151">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="26e3e-151">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="26e3e-152">Identyfikator zasobu topologii usług, w którym ma zostać utworzona jednostka usługi.</span><span class="sxs-lookup"><span data-stu-id="26e3e-152">The service topology resource identifier in which the service unit should be created.</span></span>

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

### <span data-ttu-id="26e3e-153">-Tag</span><span class="sxs-lookup"><span data-stu-id="26e3e-153">-Tag</span></span>
<span data-ttu-id="26e3e-154">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="26e3e-154">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="26e3e-155">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="26e3e-155">-TargetResourceGroup</span></span>
<span data-ttu-id="26e3e-156">Określa lokalizację, do której będą wdrażane zasoby w ramach jednostki usługi.</span><span class="sxs-lookup"><span data-stu-id="26e3e-156">Determines the location where resources under the service unit would be deployed to.</span></span>

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

### <span data-ttu-id="26e3e-157">-TemplateArtifactSourceRelativePath</span><span class="sxs-lookup"><span data-stu-id="26e3e-157">-TemplateArtifactSourceRelativePath</span></span>
<span data-ttu-id="26e3e-158">Tryb wdrażania, który ma być używany podczas wdrażania zasobów w jednostce usługi.</span><span class="sxs-lookup"><span data-stu-id="26e3e-158">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="26e3e-159">-TemplateUri</span><span class="sxs-lookup"><span data-stu-id="26e3e-159">-TemplateUri</span></span>
<span data-ttu-id="26e3e-160">Tryb wdrażania, który ma być używany podczas wdrażania zasobów w jednostce usługi.</span><span class="sxs-lookup"><span data-stu-id="26e3e-160">The deployment mode to use when deploying the resources in the service unit.</span></span>

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

### <span data-ttu-id="26e3e-161">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="26e3e-161">-Confirm</span></span>
<span data-ttu-id="26e3e-162">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26e3e-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26e3e-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26e3e-163">-WhatIf</span></span>
<span data-ttu-id="26e3e-164">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="26e3e-164">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="26e3e-165">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="26e3e-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26e3e-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26e3e-166">CommonParameters</span></span>
<span data-ttu-id="26e3e-167">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="26e3e-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26e3e-168">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="26e3e-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26e3e-169">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="26e3e-169">INPUTS</span></span>

### <span data-ttu-id="26e3e-170">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="26e3e-170">None</span></span>

## <span data-ttu-id="26e3e-171">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="26e3e-171">OUTPUTS</span></span>

### <span data-ttu-id="26e3e-172">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceUnitResource</span><span class="sxs-lookup"><span data-stu-id="26e3e-172">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceUnitResource</span></span>

## <span data-ttu-id="26e3e-173">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="26e3e-173">NOTES</span></span>

## <span data-ttu-id="26e3e-174">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="26e3e-174">RELATED LINKS</span></span>

[<span data-ttu-id="26e3e-175">Get-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="26e3e-175">Get-AzureRmDeploymentManagerServiceUnit</span></span>](./Get-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="26e3e-176">Remove-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="26e3e-176">Remove-AzureRmDeploymentManagerServiceUnit</span></span>](./Remove-AzureRmDeploymentManagerServiceUnit.md)

[<span data-ttu-id="26e3e-177">Set-AzureRmDeploymentManagerServiceUnit</span><span class="sxs-lookup"><span data-stu-id="26e3e-177">Set-AzureRmDeploymentManagerServiceUnit</span></span>](./Set-AzureRmDeploymentManagerServiceUnit.md)