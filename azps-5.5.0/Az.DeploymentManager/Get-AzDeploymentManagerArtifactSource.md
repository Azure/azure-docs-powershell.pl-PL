---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 5b330b2f20fb0611d4bfdea37756b4d62e3bbd69
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196522"
---
# <span data-ttu-id="b7ed6-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b7ed6-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="b7ed6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7ed6-102">SYNOPSIS</span></span>

<span data-ttu-id="b7ed6-103">Pobiera źródło Artefakt.</span><span class="sxs-lookup"><span data-stu-id="b7ed6-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="b7ed6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b7ed6-104">SYNTAX</span></span>

### <span data-ttu-id="b7ed6-105">Interakcyjna (domyślna)</span><span class="sxs-lookup"><span data-stu-id="b7ed6-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7ed6-106">ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7ed6-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="b7ed6-107">InputObject</span><span class="sxs-lookup"><span data-stu-id="b7ed6-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7ed6-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="b7ed6-108">DESCRIPTION</span></span>
<span data-ttu-id="b7ed6-109">Polecenie **cmdlet Get-AzDeploymentManagerArtifactSource** pobiera źródło artefaktu i zwraca obiekt reprezentujący to źródło artefaktu.</span><span class="sxs-lookup"><span data-stu-id="b7ed6-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="b7ed6-110">Określ źródło artefaktu według jego nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7ed6-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="b7ed6-111">Ewentualnie możesz podać obiekt ArtifactSource lub ResourceId.</span><span class="sxs-lookup"><span data-stu-id="b7ed6-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="b7ed6-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b7ed6-112">EXAMPLES</span></span>

### <span data-ttu-id="b7ed6-113">Przykład 1. Uzyskiwanie źródła artefaktu</span><span class="sxs-lookup"><span data-stu-id="b7ed6-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="b7ed6-114">To polecenie pobiera źródło artefaktów o nazwie ContosoArtifactSource w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b7ed6-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b7ed6-115">Przykład 2. Uzyskiwanie źródła artefaktu przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="b7ed6-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="b7ed6-116">To polecenie pobiera źródło artefaktów o nazwie ContosoArtifactSource w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b7ed6-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="b7ed6-117">Przykład 3. Uzyskiwanie źródła artefaktu przy użyciu obiektu zwróconego przez New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b7ed6-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="b7ed6-118">To polecenie pobiera źródło artefaktu, którego nazwa i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa) $artifactSourceObject ResourceGroupName (Nazwa grupy zasobów).</span><span class="sxs-lookup"><span data-stu-id="b7ed6-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="b7ed6-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7ed6-119">PARAMETERS</span></span>

### <span data-ttu-id="b7ed6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7ed6-120">-DefaultProfile</span></span>
<span data-ttu-id="b7ed6-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b7ed6-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7ed6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7ed6-122">-InputObject</span></span>
<span data-ttu-id="b7ed6-123">Obiekt Źródło artefaktu.</span><span class="sxs-lookup"><span data-stu-id="b7ed6-123">Artifact Source object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: InputObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b7ed6-124">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b7ed6-124">-Name</span></span>
<span data-ttu-id="b7ed6-125">Nazwa źródła artefaktu.</span><span class="sxs-lookup"><span data-stu-id="b7ed6-125">The name of the artifact source.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ed6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7ed6-126">-ResourceGroupName</span></span>
<span data-ttu-id="b7ed6-127">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="b7ed6-127">The resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Interactive
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7ed6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b7ed6-128">-ResourceId</span></span>
<span data-ttu-id="b7ed6-129">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="b7ed6-129">The resource identifier.</span></span>

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

### <span data-ttu-id="b7ed6-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7ed6-130">CommonParameters</span></span>
<span data-ttu-id="b7ed6-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b7ed6-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7ed6-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b7ed6-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7ed6-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7ed6-133">INPUTS</span></span>

### <span data-ttu-id="b7ed6-134">System.String</span><span class="sxs-lookup"><span data-stu-id="b7ed6-134">System.String</span></span>

### <span data-ttu-id="b7ed6-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b7ed6-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="b7ed6-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b7ed6-136">OUTPUTS</span></span>

### <span data-ttu-id="b7ed6-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="b7ed6-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="b7ed6-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b7ed6-138">NOTES</span></span>

## <span data-ttu-id="b7ed6-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b7ed6-139">RELATED LINKS</span></span>
