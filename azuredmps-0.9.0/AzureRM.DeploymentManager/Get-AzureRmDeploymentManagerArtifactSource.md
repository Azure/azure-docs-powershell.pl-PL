---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/get-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: baf5059d3a952e90422f3e16d83634291aa87614
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710748"
---
# <span data-ttu-id="5ccdc-101">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="5ccdc-101">Get-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="5ccdc-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ccdc-102">SYNOPSIS</span></span>
<span data-ttu-id="5ccdc-103">Pobiera źródło artefaktu.</span><span class="sxs-lookup"><span data-stu-id="5ccdc-103">Gets an artifact source.</span></span>

## <span data-ttu-id="5ccdc-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ccdc-104">SYNTAX</span></span>

### <span data-ttu-id="5ccdc-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="5ccdc-105">Interactive (Default)</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5ccdc-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="5ccdc-106">ResourceId</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="5ccdc-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="5ccdc-107">InputObject</span></span>
```
Get-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5ccdc-108">Opis</span><span class="sxs-lookup"><span data-stu-id="5ccdc-108">DESCRIPTION</span></span>
<span data-ttu-id="5ccdc-109">Polecenie cmdlet **Get-AzureRmDeploymentManagerArtifactSource** Pobiera źródło artefaktów i zwraca obiekt reprezentujący to źródło artefaktu.</span><span class="sxs-lookup"><span data-stu-id="5ccdc-109">The **Get-AzureRmDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="5ccdc-110">Określ źródło artefaktu, podając jego nazwę i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ccdc-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="5ccdc-111">Alternatywnie możesz podać obiekt ArtifactSource lub ResourceId.</span><span class="sxs-lookup"><span data-stu-id="5ccdc-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

<span data-ttu-id="5ccdc-112">Możesz zmodyfikować ten obiekt lokalnie, a następnie zastosować zmiany w źródle artefaktów, korzystając z polecenia cmdlet Set-AzureRmDeploymentManagerArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="5ccdc-112">You can modify this object locally, and then apply changes to the artifact source by using the Set-AzureRmDeploymentManagerArtifactSource cmdlet.</span></span>

## <span data-ttu-id="5ccdc-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ccdc-113">EXAMPLES</span></span>

### <span data-ttu-id="5ccdc-114">Przykład 1: uzyskiwanie źródła artefaktu</span><span class="sxs-lookup"><span data-stu-id="5ccdc-114">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="5ccdc-115">To polecenie pobiera Źródło artefaktów o nazwie ContosoArtifactSource w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5ccdc-115">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="5ccdc-116">Przykład 2: uzyskiwanie źródła artefaktu przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="5ccdc-116">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="5ccdc-117">To polecenie pobiera Źródło artefaktów o nazwie ContosoArtifactSource w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="5ccdc-117">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="5ccdc-118">Przykład 3: uzyskiwanie źródła artefaktu przy użyciu obiektu zwróconego przez New-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="5ccdc-118">Example 3: Get an artifact source using an object returned by New-AzureRmDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="5ccdc-119">To polecenie uzyskuje Źródło artefaktów, których nazwa i przysourcename są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="5ccdc-119">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="5ccdc-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ccdc-120">PARAMETERS</span></span>

### <span data-ttu-id="5ccdc-121">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="5ccdc-121">-ArtifactSource</span></span>
<span data-ttu-id="5ccdc-122">Obiekt źródłowy artefaktu.</span><span class="sxs-lookup"><span data-stu-id="5ccdc-122">Artifact Source object.</span></span>

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

### <span data-ttu-id="5ccdc-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ccdc-123">-DefaultProfile</span></span>
<span data-ttu-id="5ccdc-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ccdc-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ccdc-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="5ccdc-125">-Name</span></span>
<span data-ttu-id="5ccdc-126">Nazwa źródła artefaktu.</span><span class="sxs-lookup"><span data-stu-id="5ccdc-126">The name of the artifact source.</span></span>

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

### <span data-ttu-id="5ccdc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ccdc-127">-ResourceGroupName</span></span>
<span data-ttu-id="5ccdc-128">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ccdc-128">The resource group.</span></span>

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

### <span data-ttu-id="5ccdc-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5ccdc-129">-ResourceId</span></span>
<span data-ttu-id="5ccdc-130">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="5ccdc-130">The resource identifier.</span></span>

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

### <span data-ttu-id="5ccdc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ccdc-131">CommonParameters</span></span>
<span data-ttu-id="5ccdc-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ccdc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ccdc-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ccdc-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ccdc-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ccdc-134">INPUTS</span></span>

### <span data-ttu-id="5ccdc-135">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5ccdc-135">None</span></span>

## <span data-ttu-id="5ccdc-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ccdc-136">OUTPUTS</span></span>

### <span data-ttu-id="5ccdc-137">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="5ccdc-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="5ccdc-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ccdc-138">NOTES</span></span>

## <span data-ttu-id="5ccdc-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ccdc-139">RELATED LINKS</span></span>

[<span data-ttu-id="5ccdc-140">Nowe — AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="5ccdc-140">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="5ccdc-141">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="5ccdc-141">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="5ccdc-142">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="5ccdc-142">Set-AzureRmDeploymentManagerArtifactSource</span></span>](./Set-AzureRmDeploymentManagerArtifactSource.md)