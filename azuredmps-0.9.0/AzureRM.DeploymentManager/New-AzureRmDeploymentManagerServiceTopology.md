---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/new-azurermdeploymentmanagerservicetopology
schema: 2.0.0
ms.openlocfilehash: d7e3055c6443faa2c85d63e6cfdb611cb7d2eb41
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523813"
---
# <span data-ttu-id="6aeee-101">New-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="6aeee-101">New-AzureRmDeploymentManagerServiceTopology</span></span>

## <span data-ttu-id="6aeee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6aeee-102">SYNOPSIS</span></span>
<span data-ttu-id="6aeee-103">Tworzy nową topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="6aeee-103">Creates a new service topology.</span></span>

## <span data-ttu-id="6aeee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6aeee-104">SYNTAX</span></span>

```
New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName <String> -Name <String> -Location <String>
 [-ArtifactSourceId <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6aeee-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6aeee-105">DESCRIPTION</span></span>
<span data-ttu-id="6aeee-106">Polecenie cmdlet **New-AzureRmDeploymentManagerServiceTopology** tworzy topologię usługi.</span><span class="sxs-lookup"><span data-stu-id="6aeee-106">The **New-AzureRmDeploymentManagerServiceTopology** cmdlet creates a service topology.</span></span>

<span data-ttu-id="6aeee-107">Zwrócony obiekt servicetopology można zmodyfikować lokalnie, a następnie zastosować zmiany w topologii przy użyciu polecenia cmdlet Set-AzureRmDeploymentManagerServiceTopology.</span><span class="sxs-lookup"><span data-stu-id="6aeee-107">You can modify the returned ServiceTopology object locally, and then apply changes to the topology by using the Set-AzureRmDeploymentManagerServiceTopology cmdlet.</span></span>
<span data-ttu-id="6aeee-108">Zwrócony obiekt</span><span class="sxs-lookup"><span data-stu-id="6aeee-108">The returned object</span></span> 

<span data-ttu-id="6aeee-109">Zwrócony obiekt zawiera pole ResourceId, do którego można odwołać się w zasobie wdrożeniowym, aby wskazać, że usługi zadeklarowane w tej topologii usługi zostaną wdrożone w trakcie wdrażania.</span><span class="sxs-lookup"><span data-stu-id="6aeee-109">The returned object has a ResourceId field which can be referenced in a rollout resource to indicate that the services declared in this service topology would be deployed in the rollout.</span></span>

## <span data-ttu-id="6aeee-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6aeee-110">EXAMPLES</span></span>

### <span data-ttu-id="6aeee-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6aeee-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US" -ArtifactSourceId "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="6aeee-112">To polecenie cmdlet powoduje utworzenie nowej topologii usługi w grupie zasobów ContosoResourceGroup z nazwą ContosoServiceTopology i w polu Lokalizacja Centralna US.</span><span class="sxs-lookup"><span data-stu-id="6aeee-112">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="6aeee-113">Identyfikator zasobu źródłowego artefaktu wskazuje, że artefakty wymagane do definicji jednostek usług w tej topologii muszą być odczytywane z określonego źródła artefaktu.</span><span class="sxs-lookup"><span data-stu-id="6aeee-113">The artifact source ResourceId indicates that the artifacts required for the service unit definitions in this topology need to be read from the specified artifact source.</span></span>

### <span data-ttu-id="6aeee-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6aeee-114">Example 2</span></span>
```powershell
PS C:\> New-AzureRmDeploymentManagerServiceTopology -ResourceGroupName ContosoResourceGroup -Name ContosoServiceTopology -Location "Central US"
```

<span data-ttu-id="6aeee-115">To polecenie cmdlet powoduje utworzenie nowej topologii usługi w grupie zasobów ContosoResourceGroup z nazwą ContosoServiceTopology i w polu Lokalizacja Centralna US.</span><span class="sxs-lookup"><span data-stu-id="6aeee-115">This cmdlet creates a new service topology in the resource group ContosoResourceGroup with the name ContosoServiceTopology and in location Central US.</span></span> <span data-ttu-id="6aeee-116">Brak odwołania do źródła artefaktów wskazuje, że artefakty wymagane dla definicji jednostek usług w tej topologii będą podane jako bezwzględne identyfikatory URI w jednostce usługi.</span><span class="sxs-lookup"><span data-stu-id="6aeee-116">The absence of an artifact source reference indicates that the artifacts required for the service unit definitions in this topology would be provided as absolute SAS URIs in the service unit.</span></span>

## <span data-ttu-id="6aeee-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6aeee-117">PARAMETERS</span></span>

### <span data-ttu-id="6aeee-118">-ArtifactSourceId</span><span class="sxs-lookup"><span data-stu-id="6aeee-118">-ArtifactSourceId</span></span>
<span data-ttu-id="6aeee-119">Identyfikator źródła artefaktu, w którym są przechowywane artefakty składające się na topologię.</span><span class="sxs-lookup"><span data-stu-id="6aeee-119">The identifier of the artifact source, where the artifacts that make up the topology are stored.</span></span>

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

### <span data-ttu-id="6aeee-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aeee-120">-DefaultProfile</span></span>
<span data-ttu-id="6aeee-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6aeee-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6aeee-122">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="6aeee-122">-Location</span></span>
<span data-ttu-id="6aeee-123">Lokalizacja topologii.</span><span class="sxs-lookup"><span data-stu-id="6aeee-123">The location of the topology.</span></span>

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

### <span data-ttu-id="6aeee-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="6aeee-124">-Name</span></span>
<span data-ttu-id="6aeee-125">Nazwa topologii.</span><span class="sxs-lookup"><span data-stu-id="6aeee-125">The name of the topology.</span></span>

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

### <span data-ttu-id="6aeee-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6aeee-126">-ResourceGroupName</span></span>
<span data-ttu-id="6aeee-127">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="6aeee-127">The resource group.</span></span>

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

### <span data-ttu-id="6aeee-128">-Tag</span><span class="sxs-lookup"><span data-stu-id="6aeee-128">-Tag</span></span>
<span data-ttu-id="6aeee-129">Tabela skrótów reprezentująca znaczniki zasobów.</span><span class="sxs-lookup"><span data-stu-id="6aeee-129">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="6aeee-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6aeee-130">-Confirm</span></span>
<span data-ttu-id="6aeee-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aeee-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6aeee-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6aeee-132">-WhatIf</span></span>
<span data-ttu-id="6aeee-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6aeee-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6aeee-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6aeee-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6aeee-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aeee-135">CommonParameters</span></span>
<span data-ttu-id="6aeee-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6aeee-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aeee-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aeee-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aeee-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6aeee-138">INPUTS</span></span>

### <span data-ttu-id="6aeee-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="6aeee-139">None</span></span>

## <span data-ttu-id="6aeee-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6aeee-140">OUTPUTS</span></span>

### <span data-ttu-id="6aeee-141">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSServiceTopologyResource</span><span class="sxs-lookup"><span data-stu-id="6aeee-141">Microsoft.Azure.Commands.DeploymentManager.Models.PSServiceTopologyResource</span></span>

## <span data-ttu-id="6aeee-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6aeee-142">NOTES</span></span>

## <span data-ttu-id="6aeee-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6aeee-143">RELATED LINKS</span></span>

[<span data-ttu-id="6aeee-144">Get-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="6aeee-144">Get-AzureRmDeploymentManagerServiceTopology</span></span>](./Get-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="6aeee-145">Remove-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="6aeee-145">Remove-AzureRmDeploymentManagerServiceTopology</span></span>](./Remove-AzureRmDeploymentManagerServiceTopology.md)

[<span data-ttu-id="6aeee-146">Set-AzureRmDeploymentManagerServiceTopology</span><span class="sxs-lookup"><span data-stu-id="6aeee-146">Set-AzureRmDeploymentManagerServiceTopology</span></span>](./Set-AzureRmDeploymentManagerServiceTopology.md)