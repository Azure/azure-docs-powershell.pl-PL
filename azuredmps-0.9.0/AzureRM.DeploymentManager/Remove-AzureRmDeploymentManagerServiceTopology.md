---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/remove-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: be95f5fffe4483c74d8b1438819cf084eaa0693b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523161"
---
# <span data-ttu-id="9885c-101">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="9885c-101">Remove-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="9885c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9885c-102">SYNOPSIS</span></span>
<span data-ttu-id="9885c-103">Usuwa topologię usługi i wszystkie jej zasoby.</span><span class="sxs-lookup"><span data-stu-id="9885c-103">Deletes a service topology and all its resources.</span></span>

## <span data-ttu-id="9885c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9885c-104">SYNTAX</span></span>

### <span data-ttu-id="9885c-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9885c-105">Interactive (Default)</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9885c-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="9885c-106">ResourceId</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ResourceId] <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9885c-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="9885c-107">InputObject</span></span>
```
Remove-AzureRmDeploymentManagerServiceTopology [-ServiceTopology] <PSServiceTopologyResource> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9885c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="9885c-108">DESCRIPTION</span></span>
<span data-ttu-id="9885c-109">Polecenie cmdlet **Remove-AzureRmDeploymentManagerServiceTopology** usuwa topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="9885c-109">The **Remove-AzureRmDeploymentManagerServiceTopology** cmdlet deletes a service topology.</span></span>

<span data-ttu-id="9885c-110">Określ topologię usługi według jej nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9885c-110">Specify the service topology by its name and the resource group name.</span></span> <span data-ttu-id="9885c-111">Alternatywnie możesz podać obiekt servicetopology lub identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="9885c-111">Alternately, you can provide the ServiceTopology object or the ResourceId.</span></span>

## <span data-ttu-id="9885c-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9885c-112">EXAMPLES</span></span>

### <span data-ttu-id="9885c-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9885c-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology
```

<span data-ttu-id="9885c-114">To polecenie usuwa topologię usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9885c-114">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="9885c-115">Przykład 2: usunięcie topologii usługi przy użyciu identyfikatora zasobu.</span><span class="sxs-lookup"><span data-stu-id="9885c-115">Example 2: Delete a service topology using the resource identifier.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerServiceTopology -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/serviceTopologies/ContosoServiceTopology"
```

<span data-ttu-id="9885c-116">To polecenie usuwa topologię usługi o nazwie ContosoServiceTopology w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="9885c-116">This command deletes a service topology named ContosoServiceTopology in the ContosoResourceGroup.</span></span>

### <span data-ttu-id="9885c-117">Przykład 3: usuwanie topologii usług przy użyciu obiektu typu topologia usług.</span><span class="sxs-lookup"><span data-stu-id="9885c-117">Example 3: Delete a service topology using the service topology object.</span></span>
```powershell
PS C:\> Remove-AzureRmDeploymentManagerService -ServiceTopology $serviceTopologyObject
```

<span data-ttu-id="9885c-118">To polecenie usuwa topologię usługi, której nazwa i nazwa źródła danych są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $serviceTopologyObject.</span><span class="sxs-lookup"><span data-stu-id="9885c-118">This command deletes a service topology whose name and ResourceGroup match the Name and ResourceGroupName properties of the $serviceTopologyObject, respectively.</span></span>

## <span data-ttu-id="9885c-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9885c-119">PARAMETERS</span></span>

### <span data-ttu-id="9885c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9885c-120">-DefaultProfile</span></span>
<span data-ttu-id="9885c-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9885c-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9885c-122">-Force</span><span class="sxs-lookup"><span data-stu-id="9885c-122">-Force</span></span>
<span data-ttu-id="9885c-123">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9885c-123">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="9885c-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9885c-124">-Name</span></span>
<span data-ttu-id="9885c-125">Nazwa topologii usługi.</span><span class="sxs-lookup"><span data-stu-id="9885c-125">The name of the service topology.</span></span>

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

### <span data-ttu-id="9885c-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9885c-126">-PassThru</span></span>
<span data-ttu-id="9885c-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="9885c-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="9885c-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9885c-128">-ResourceGroupName</span></span>
<span data-ttu-id="9885c-129">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="9885c-129">The resource group.</span></span>

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

### <span data-ttu-id="9885c-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9885c-130">-ResourceId</span></span>
<span data-ttu-id="9885c-131">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="9885c-131">The resource identifier.</span></span>

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

### <span data-ttu-id="9885c-132">-Servicetopology</span><span class="sxs-lookup"><span data-stu-id="9885c-132">-ServiceTopology</span></span>
<span data-ttu-id="9885c-133">Zasób, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="9885c-133">The resource to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9885c-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9885c-134">-Confirm</span></span>
<span data-ttu-id="9885c-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9885c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9885c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9885c-136">-WhatIf</span></span>
<span data-ttu-id="9885c-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9885c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9885c-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9885c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9885c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9885c-139">CommonParameters</span></span>
<span data-ttu-id="9885c-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9885c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9885c-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9885c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9885c-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9885c-142">INPUTS</span></span>

### <span data-ttu-id="9885c-143">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="9885c-143">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="9885c-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9885c-144">OUTPUTS</span></span>

### <span data-ttu-id="9885c-145">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="9885c-145">System.Boolean</span></span>

## <span data-ttu-id="9885c-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9885c-146">NOTES</span></span>

## <span data-ttu-id="9885c-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9885c-147">RELATED LINKS</span></span>

[<span data-ttu-id="9885c-148">Nowe — AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="9885c-148">New-AzureRmDeploymentManagerServiceTopology</span></span>](./New-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="9885c-149">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="9885c-149">Get-AzureRmDeploymentManagerServiceTopology</span></span>](./Get-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="9885c-150">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="9885c-150">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)