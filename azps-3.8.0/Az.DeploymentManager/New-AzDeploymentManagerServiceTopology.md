---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/new-azdeploymentmanagerservicetopology
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerServiceTopology.md
ms.openlocfilehash: c104f074b972e42aaa21ce4e85c6076294ec5aa2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053349"
---
# <span data-ttu-id="ec5f7-101">New-AzDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="ec5f7-101">New-AzDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="ec5f7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec5f7-102">SYNOPSIS</span></span>
<span data-ttu-id="ec5f7-103">Tworzy topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="ec5f7-103">Creates a service topology.</span></span>

## <span data-ttu-id="ec5f7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec5f7-104">SYNTAX</span></span>

```
New-AzDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec5f7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ec5f7-105">DESCRIPTION</span></span>
<span data-ttu-id="ec5f7-106">Polecenie cmdlet **New-AzDeploymentManagerServiceTopology** tworzy topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="ec5f7-106">The **New-AzDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="ec5f7-107">Zwrócony obiekt servicetopology można zmodyfikować lokalnie, a następnie zastosować zmiany w topologii przy użyciu polecenia cmdlet Set-AzDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="ec5f7-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="ec5f7-108">Zwrócony obiekt</span><span class="sxs-lookup"><span data-stu-id="ec5f7-108">The returned object</span></span> 

<span data-ttu-id="ec5f7-109">Zwrócony obiekt zawiera pole ResourceId, do którego można odwołać się w zasobie wdrożeniowym, aby wskazać, że usługi zadeklarowane w tej topologii usługi zostaną wdrożone w trakcie wdrażania.</span><span class="sxs-lookup"><span data-stu-id="ec5f7-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="ec5f7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec5f7-110">EXAMPLES</span></span>

### <span data-ttu-id="ec5f7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ec5f7-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="ec5f7-112">To polecenie cmdlet powoduje utworzenie nowej topologii usługi w grupie zasobów ContosoResourceGroup z nazwą ContosoServiceTopology i w polu Lokalizacja Centralna US.</span><span class="sxs-lookup"><span data-stu-id="ec5f7-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="ec5f7-113">Identyfikator zasobu źródłowego artefaktu wskazuje, że artefakty wymagane do definicji jednostek usług w tej topologii muszą być odczytywane z określonego źródła artefaktu.</span><span class="sxs-lookup"><span data-stu-id="ec5f7-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="ec5f7-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="ec5f7-114">Example 2</span></span>
```powershell
PS C:\> New-AzDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="ec5f7-115">To polecenie cmdlet powoduje utworzenie nowej topologii usługi w grupie zasobów ContosoResourceGroup z nazwą ContosoServiceTopology i w polu Lokalizacja Centralna US.</span><span class="sxs-lookup"><span data-stu-id="ec5f7-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="ec5f7-116">Brak odwołania do źródła artefaktów wskazuje, że artefakty wymagane dla definicji jednostek usług w tej topologii będą podane jako bezwzględne identyfikatory URI w jednostce usługi.</span><span class="sxs-lookup"><span data-stu-id="ec5f7-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="ec5f7-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec5f7-117">PARAMETERS</span></span>

### <span data-ttu-id="ec5f7-118">-ArtifactSourceId</span><span class="sxs-lookup"><span data-stu-id="ec5f7-118">-ArtifactSourceId</span></span>
<span data-ttu-id="ec5f7-119">Identyfikator źródła artefaktu, w którym są przechowywane artefakty składające się na topologię.</span><span class="sxs-lookup"><span data-stu-id="ec5f7-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

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

### <span data-ttu-id="ec5f7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec5f7-120">-DefaultProfile</span></span>
<span data-ttu-id="ec5f7-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec5f7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec5f7-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="ec5f7-122">-Location</span></span>
<span data-ttu-id="ec5f7-123">Lokalizacja topologii.</span><span class="sxs-lookup"><span data-stu-id="ec5f7-123">The location of the topology.</span></span>

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

### <span data-ttu-id="ec5f7-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="ec5f7-124">-Name</span></span>
<span data-ttu-id="ec5f7-125">Nazwa topologii.</span><span class="sxs-lookup"><span data-stu-id="ec5f7-125">The name of the topology.</span></span>

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

### <span data-ttu-id="ec5f7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec5f7-126">-ResourceGroupName</span></span>
<span data-ttu-id="ec5f7-127">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="ec5f7-127">The resource group.</span></span>

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

### <span data-ttu-id="ec5f7-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="ec5f7-128">-Tag</span></span>
<span data-ttu-id="ec5f7-129">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="ec5f7-129">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="ec5f7-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ec5f7-130">-Confirm</span></span>
<span data-ttu-id="ec5f7-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec5f7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec5f7-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec5f7-132">-WhatIf</span></span>
<span data-ttu-id="ec5f7-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ec5f7-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec5f7-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ec5f7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec5f7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec5f7-135">CommonParameters</span></span>
<span data-ttu-id="ec5f7-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec5f7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec5f7-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ec5f7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec5f7-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec5f7-138">INPUTS</span></span>

### <span data-ttu-id="ec5f7-139">System. Collections. Hashtable</span><span class="sxs-lookup"><span data-stu-id="ec5f7-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="ec5f7-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec5f7-140">OUTPUTS</span></span>

### <span data-ttu-id="ec5f7-141">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="ec5f7-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="ec5f7-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec5f7-142">NOTES</span></span>

## <span data-ttu-id="ec5f7-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec5f7-143">RELATED LINKS</span></span>
