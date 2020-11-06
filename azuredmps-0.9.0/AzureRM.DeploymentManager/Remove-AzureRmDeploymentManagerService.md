---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservice
schema: 2.0.0
ms.openlocfilehash: 4b2cd4ef2dde674b10d51dc378578acbd13c4a7b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523077"
---
# <span data-ttu-id="d414a-101">Remove-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="d414a-101">Remove-AzureRmDeploymentManagerService</span></span>

## <span data-ttu-id="d414a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d414a-102">SYNOPSIS</span></span>
<span data-ttu-id="d414a-103">Usuwa usługę w topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="d414a-103">Deletes a service in a service topology.</span></span>

## <span data-ttu-id="d414a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d414a-104">SYNTAX</span></span>

### <span data-ttu-id="d414a-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="d414a-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String>
 [-Name] <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d414a-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="d414a-106">ByServiceTopologyObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d414a-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="d414a-107">ByServiceTopologyResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-Name] <String> [-ServiceTopologyResourceId] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d414a-108">Zasobów</span><span class="sxs-lookup"><span data-stu-id="d414a-108">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerService [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d414a-109">Inputobject</span><span class="sxs-lookup"><span data-stu-id="d414a-109">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerService [-Service] <PSServiceResource> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d414a-110">Opis</span><span class="sxs-lookup"><span data-stu-id="d414a-110">DESCRIPTION</span></span>
<span data-ttu-id="d414a-111">Polecenie cmdlet **Remove-AzureRmDeploymentManagerService** usuwa usługę w ramach topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="d414a-111">The **Remove-AzureRmDeploymentManagerService** cmdlet deletes a service under a service topology.</span></span>
<span data-ttu-id="d414a-112">Określ usługę za pomocą jej nazwy, topologii usługi i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="d414a-112">Specify the service by its name, service topology it is in and the resource group name.</span></span> <span data-ttu-id="d414a-113">Alternatywnie możesz podać obiekt Service lub ResourceId.</span><span class="sxs-lookup"><span data-stu-id="d414a-113">Alternately, you can provide the Service object or the ResourceId.</span></span>

## <span data-ttu-id="d414a-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d414a-114">EXAMPLES</span></span>

### <span data-ttu-id="d414a-115">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d414a-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1
```

<span data-ttu-id="d414a-116">To polecenie usuwa usługę o nazwie ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d414a-116">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="d414a-117">Przykład 2: Usunięcie usługi przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="d414a-117">Example 2: Delete a service using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology/services/ContosoService1"
```

<span data-ttu-id="d414a-118">To polecenie usuwa usługę o nazwie ContosoService1 w topologii usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="d414a-118">This command deletes a service named ContosoService1 in a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="d414a-119">Przykład 3: Usuwanie usługi za pomocą obiektu usługi.</span><span class="sxs-lookup"><span data-stu-id="d414a-119">Example 3: Delete a service using the service object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -Service $serviceObject
```

<span data-ttu-id="d414a-120">To polecenie usuwa usługę, której nazwa, nazwa topologii usługi i nazwa źródła zasobów są zgodne z właściwościami Name, servicetopologyname i ResourceGroupName w $serviceObject.</span><span class="sxs-lookup"><span data-stu-id="d414a-120">This command deletes a service whose name, service topology name and ResourceGroup match the Name, ServiceTopologyName and ResourceGroupName properties of the $serviceObject, respectively.</span></span>

## <span data-ttu-id="d414a-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d414a-121">PARAMETERS</span></span>

### <span data-ttu-id="d414a-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d414a-122">-DefaultProfile</span></span>
<span data-ttu-id="d414a-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d414a-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d414a-124">-Force</span><span class="sxs-lookup"><span data-stu-id="d414a-124">-Force</span></span>
<span data-ttu-id="d414a-125">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d414a-125">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="d414a-126">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="d414a-126">-Name</span></span>
<span data-ttu-id="d414a-127">Nazwa usługi.</span><span class="sxs-lookup"><span data-stu-id="d414a-127">The name of the service.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive, ByServiceTopologyObject, ByServiceTopologyResourceId
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d414a-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d414a-128">-PassThru</span></span>
<span data-ttu-id="d414a-129">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="d414a-129">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="d414a-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d414a-130">-ResourceGroupName</span></span>
<span data-ttu-id="d414a-131">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="d414a-131">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d414a-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d414a-132">-ResourceId</span></span>
<span data-ttu-id="d414a-133">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="d414a-133">The resource identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d414a-134">-Service</span><span class="sxs-lookup"><span data-stu-id="d414a-134">-Service</span></span>
<span data-ttu-id="d414a-135">Zasób, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="d414a-135">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d414a-136">-Servicetopology</span><span class="sxs-lookup"><span data-stu-id="d414a-136">-ServiceTopology</span></span>
<span data-ttu-id="d414a-137">Obiekt z topologią usług, w którym ma zostać utworzona usługa.</span><span class="sxs-lookup"><span data-stu-id="d414a-137">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d414a-138">-Servicetopologyname</span><span class="sxs-lookup"><span data-stu-id="d414a-138">-ServiceTopologyName</span></span>
<span data-ttu-id="d414a-139">Nazwa topologii usług, do której należy usługa.</span><span class="sxs-lookup"><span data-stu-id="d414a-139">The name of the service topology the service belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d414a-140">-ServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="d414a-140">-ServiceTopologyResourceId</span></span>
<span data-ttu-id="d414a-141">Identyfikator zasobu topologii usług, w którym ma zostać utworzona usługa.</span><span class="sxs-lookup"><span data-stu-id="d414a-141">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d414a-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d414a-142">-Confirm</span></span>
<span data-ttu-id="d414a-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d414a-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d414a-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d414a-144">-WhatIf</span></span>
<span data-ttu-id="d414a-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d414a-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d414a-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d414a-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d414a-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d414a-147">CommonParameters</span></span>
<span data-ttu-id="d414a-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d414a-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d414a-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d414a-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d414a-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d414a-150">INPUTS</span></span>

### <span data-ttu-id="d414a-151">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="d414a-151">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="d414a-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d414a-152">OUTPUTS</span></span>

### <span data-ttu-id="d414a-153">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d414a-153">System.Boolean</span></span>

## <span data-ttu-id="d414a-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d414a-154">NOTES</span></span>

## <span data-ttu-id="d414a-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d414a-155">RELATED LINKS</span></span>

[<span data-ttu-id="d414a-156">Nowe — AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="d414a-156">New-AzureRmDeploymentManagerService</span></span>](./New-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="d414a-157">Get-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="d414a-157">Get-AzureRmDeploymentManagerService</span></span>](./Get-AzureRmDeploymentManagerService.md)

[<span data-ttu-id="d414a-158">Set-AzureRmDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="d414a-158">Set-AzureRmDeploymentManagerService</span></span>](./Set-AzureRmDeploymentManagerService.md)