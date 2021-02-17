---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: c104f074b972e42aaa21ce4e85c6076294ec5aa2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196514"
---
# <span data-ttu-id="ad318-101">New-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="ad318-101">New-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="ad318-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ad318-102">SYNOPSIS</span></span>
<span data-ttu-id="ad318-103">Tworzy topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="ad318-103">Creates a service topology.</span></span>

## <span data-ttu-id="ad318-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ad318-104">SYNTAX</span></span>

```
New-AzDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ad318-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ad318-105">DESCRIPTION</span></span>
<span data-ttu-id="ad318-106">Polecenie **cmdlet New-AzDeploymentManagerServiceTopology** tworzy topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="ad318-106">The **New-AzDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="ad318-107">Zwrócony obiekt ServiceTopology można zmodyfikować lokalnie, a następnie zastosować zmiany do topologii za pomocą Set-AzDeploymentManagerServiceTopology cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad318-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="ad318-108">Zwrócony obiekt</span><span class="sxs-lookup"><span data-stu-id="ad318-108">The returned object</span></span> 

<span data-ttu-id="ad318-109">Zwrócony obiekt zawiera pole ResourceId, do którego można się odwołać w zasobie wdrażania, aby wskazać, że usługi deklarowane w tej topologii usługi zostaną wdrożone podczas wdrażania.</span><span class="sxs-lookup"><span data-stu-id="ad318-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="ad318-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ad318-110">EXAMPLES</span></span>

### <span data-ttu-id="ad318-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ad318-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="ad318-112">To polecenie cmdlet tworzy nową topologię usługi w grupie zasobów ContosoResourceGroup o nazwie ContosoServiceTopology i w lokalizacji — Centrum us.</span><span class="sxs-lookup"><span data-stu-id="ad318-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="ad318-113">Wartość ResourceId źródła artefaktu wskazuje, że artefakty wymagane dla definicji jednostek usługi w tej topologii muszą zostać odczytane z określonego źródła artefaktu.</span><span class="sxs-lookup"><span data-stu-id="ad318-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="ad318-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ad318-114">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="ad318-115">To polecenie cmdlet tworzy nową topologię usługi w grupie zasobów ContosoResourceGroup o nazwie ContosoServiceTopology i w lokalizacji — Centrum us.</span><span class="sxs-lookup"><span data-stu-id="ad318-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="ad318-116">Brak odwołania do źródła artefaktu oznacza, że artefakty wymagane dla definicji jednostek usługi w tej topologii zostaną podane jako bezwzględne URI SAS w jednostce usługi.</span><span class="sxs-lookup"><span data-stu-id="ad318-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="ad318-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ad318-117">PARAMETERS</span></span>

### <span data-ttu-id="ad318-118">-ArtifactSourceId</span><span class="sxs-lookup"><span data-stu-id="ad318-118">-ArtifactSourceId</span></span>
<span data-ttu-id="ad318-119">Identyfikator źródła artefaktu, w którym są przechowywane artefakty, które są przechowywane w topologii.</span><span class="sxs-lookup"><span data-stu-id="ad318-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

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

### <span data-ttu-id="ad318-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad318-120">-DefaultProfile</span></span>
<span data-ttu-id="ad318-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ad318-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ad318-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ad318-122">-Location</span></span>
<span data-ttu-id="ad318-123">Lokalizacja topologii.</span><span class="sxs-lookup"><span data-stu-id="ad318-123">The location of the topology.</span></span>

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

### <span data-ttu-id="ad318-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="ad318-124">-Name</span></span>
<span data-ttu-id="ad318-125">Nazwa topologii.</span><span class="sxs-lookup"><span data-stu-id="ad318-125">The name of the topology.</span></span>

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

### <span data-ttu-id="ad318-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad318-126">-ResourceGroupName</span></span>
<span data-ttu-id="ad318-127">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad318-127">The resource group.</span></span>

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

### <span data-ttu-id="ad318-128">— Tag</span><span class="sxs-lookup"><span data-stu-id="ad318-128">-Tag</span></span>
<span data-ttu-id="ad318-129">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="ad318-129">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="ad318-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ad318-130">-Confirm</span></span>
<span data-ttu-id="ad318-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ad318-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ad318-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ad318-132">-WhatIf</span></span>
<span data-ttu-id="ad318-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ad318-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ad318-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ad318-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ad318-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad318-135">CommonParameters</span></span>
<span data-ttu-id="ad318-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad318-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad318-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ad318-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad318-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ad318-138">INPUTS</span></span>

### <span data-ttu-id="ad318-139">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ad318-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ad318-140">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ad318-140">OUTPUTS</span></span>

### <span data-ttu-id="ad318-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="ad318-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="ad318-142">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ad318-142">NOTES</span></span>

## <span data-ttu-id="ad318-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ad318-143">RELATED LINKS</span></span>
