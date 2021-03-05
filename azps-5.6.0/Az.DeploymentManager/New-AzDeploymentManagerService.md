---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerService.md
ms.openlocfilehash: b9922d84edfbf90e16db1f050ae7abaeef7442a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980721"
---
# <span data-ttu-id="6bc69-101">New-AzDeploymentManagerService</span><span class="sxs-lookup"><span data-stu-id="6bc69-101">New-AzDeploymentManagerService</span></span>

## <span data-ttu-id="6bc69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bc69-102">SYNOPSIS</span></span>
<span data-ttu-id="6bc69-103">Tworzy usługę w topologii określonej usługi.</span><span class="sxs-lookup"><span data-stu-id="6bc69-103">Creates a service under the specified service topology.</span></span>

## <span data-ttu-id="6bc69-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6bc69-104">SYNTAX</span></span>

### <span data-ttu-id="6bc69-105">Interakcyjna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="6bc69-105">Interactive (Default)</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> [-ServiceTopologyName] <String> -Name <String>
 -Location <String> -TargetLocation <String> -TargetSubscriptionId <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bc69-106">ByServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="6bc69-106">ByServiceTopologyObject</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyObject] <PSServiceTopologyResource>
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bc69-107">ByServiceTopologyResourceId</span><span class="sxs-lookup"><span data-stu-id="6bc69-107">ByServiceTopologyResourceId</span></span>
```
New-AzDeploymentManagerService [-ResourceGroupName] <String> -Name <String> -Location <String>
 -TargetLocation <String> -TargetSubscriptionId <String> [-ServiceTopologyId] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bc69-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6bc69-108">DESCRIPTION</span></span>
<span data-ttu-id="6bc69-109">Polecenie **cmdlet New-AzDeploymentManagerService** tworzy usługę w topologii usługi i zwraca obiekt reprezentujący usługę.</span><span class="sxs-lookup"><span data-stu-id="6bc69-109">The **New-AzDeploymentManagerService** cmdlet creates a service under a service topology, and returns an object that represents that service.</span></span>
<span data-ttu-id="6bc69-110">Określ usługę według jej nazwy, topologii usługi oraz nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6bc69-110">Specify the service by its name, service topology it is in and the resource group name.</span></span> 

<span data-ttu-id="6bc69-111">Polecenie cmdlet zwraca obiekt Service.</span><span class="sxs-lookup"><span data-stu-id="6bc69-111">The cmdlet returns a Service object.</span></span> <span data-ttu-id="6bc69-112">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany do usługi za pomocą Set-AzDeploymentManagerService cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bc69-112">You can modify this object locally, and then apply changes to the service by using the Set-AzDeploymentManagerService cmdlet.</span></span>

## <span data-ttu-id="6bc69-113">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6bc69-113">EXAMPLES</span></span>

### <span data-ttu-id="6bc69-114">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6bc69-114">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerService -ResourceGroupName ContosoResourceGroup -ServiceTopologyName ContosoServiceTopology -Name ContosoService1 -Location "Central US" -TargetLocation "East US" -TargetSubscriptionId XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX
```

<span data-ttu-id="6bc69-115">Tworzy nową usługę o nazwie ContosoService1 w topologii usługi ContosoServiceTopology w grupie zasobów ContosoResourceGroup w lokalizacji (Centralna usługa STANÓW Zjednoczonych).</span><span class="sxs-lookup"><span data-stu-id="6bc69-115">Creates a new service with name ContosoService1 under service topology ContosoServiceTopology in Resource Group ContosoResourceGroup, in the location Central US.</span></span> <span data-ttu-id="6bc69-116">Właściwość TargetLocation wskazuje, że usługa ContosoService1 powinna zostać wdrożona w regionie Wschodnioazjatyckim w określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="6bc69-116">The TargetLocation property indicates that the service ContosoService1 should be deployed to the East US region in the subscription specified.</span></span>

## <span data-ttu-id="6bc69-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6bc69-117">PARAMETERS</span></span>

### <span data-ttu-id="6bc69-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bc69-118">-DefaultProfile</span></span>
<span data-ttu-id="6bc69-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6bc69-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6bc69-120">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6bc69-120">-Location</span></span>
<span data-ttu-id="6bc69-121">Lokalizacja zasobu usługi.</span><span class="sxs-lookup"><span data-stu-id="6bc69-121">The location of the service resource.</span></span>

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

### <span data-ttu-id="6bc69-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6bc69-122">-Name</span></span>
<span data-ttu-id="6bc69-123">Nazwa usługi.</span><span class="sxs-lookup"><span data-stu-id="6bc69-123">The name of the service.</span></span>

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

### <span data-ttu-id="6bc69-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6bc69-124">-ResourceGroupName</span></span>
<span data-ttu-id="6bc69-125">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="6bc69-125">The resource group.</span></span>

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

### <span data-ttu-id="6bc69-126">-ServiceTopologyId</span><span class="sxs-lookup"><span data-stu-id="6bc69-126">-ServiceTopologyId</span></span>
<span data-ttu-id="6bc69-127">Identyfikator zasobu topologii usługi, w którym powinna zostać utworzona usługa.</span><span class="sxs-lookup"><span data-stu-id="6bc69-127">The service topology resource identifier in which the service should be created.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServiceTopologyResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bc69-128">-ServiceTopologyName</span><span class="sxs-lookup"><span data-stu-id="6bc69-128">-ServiceTopologyName</span></span>
<span data-ttu-id="6bc69-129">Nazwa topologii usługi, do której należy ta usługa.</span><span class="sxs-lookup"><span data-stu-id="6bc69-129">The name of the service topology this service belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bc69-130">-ServiceTopologyObject</span><span class="sxs-lookup"><span data-stu-id="6bc69-130">-ServiceTopologyObject</span></span>
<span data-ttu-id="6bc69-131">Obiekt topologii usługi, w którym powinna zostać utworzona usługa.</span><span class="sxs-lookup"><span data-stu-id="6bc69-131">The service topology object in which the service should be created.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource
Parameter Sets: ByServiceTopologyObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bc69-132">— Tag</span><span class="sxs-lookup"><span data-stu-id="6bc69-132">-Tag</span></span>
<span data-ttu-id="6bc69-133">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="6bc69-133">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6bc69-134">-TargetLocation</span><span class="sxs-lookup"><span data-stu-id="6bc69-134">-TargetLocation</span></span>
<span data-ttu-id="6bc69-135">Określa lokalizację, w której zostaną wdrożone zasoby w ramach usługi.</span><span class="sxs-lookup"><span data-stu-id="6bc69-135">Determines the location where resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="6bc69-136">-TargetSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6bc69-136">-TargetSubscriptionId</span></span>
<span data-ttu-id="6bc69-137">Określa subskrypcję, w której zostaną wdrożone zasoby w ramach usługi.</span><span class="sxs-lookup"><span data-stu-id="6bc69-137">Determines the subscription to which resources under the service would be deployed to.</span></span>

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

### <span data-ttu-id="6bc69-138">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6bc69-138">-Confirm</span></span>
<span data-ttu-id="6bc69-139">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6bc69-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bc69-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bc69-140">-WhatIf</span></span>
<span data-ttu-id="6bc69-141">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6bc69-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6bc69-142">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6bc69-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6bc69-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bc69-143">CommonParameters</span></span>
<span data-ttu-id="6bc69-144">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6bc69-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bc69-145">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6bc69-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bc69-146">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6bc69-146">INPUTS</span></span>

### <span data-ttu-id="6bc69-147">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6bc69-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="6bc69-148">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6bc69-148">OUTPUTS</span></span>

### <span data-ttu-id="6bc69-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span><span class="sxs-lookup"><span data-stu-id="6bc69-149">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceResource</span></span>

## <span data-ttu-id="6bc69-150">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6bc69-150">NOTES</span></span>

## <span data-ttu-id="6bc69-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6bc69-151">RELATED LINKS</span></span>
