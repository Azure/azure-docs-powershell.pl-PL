---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/get-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Get-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 54cccbedc45977505b10526d4806b64c8118380e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705640"
---
# <span data-ttu-id="59bc3-101">Get-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="59bc3-101">Get-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="59bc3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="59bc3-102">SYNOPSIS</span></span>

<span data-ttu-id="59bc3-103">Pobiera źródło artefaktu.</span><span class="sxs-lookup"><span data-stu-id="59bc3-103">Gets the Artifact source.</span></span>

## <span data-ttu-id="59bc3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="59bc3-104">SYNTAX</span></span>

### <span data-ttu-id="59bc3-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="59bc3-105">Interactive (Default)</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="59bc3-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="59bc3-106">ResourceId</span></span>
```
Get-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="59bc3-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="59bc3-107">InputObject</span></span>
```
Get-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59bc3-108">Opis</span><span class="sxs-lookup"><span data-stu-id="59bc3-108">DESCRIPTION</span></span>
<span data-ttu-id="59bc3-109">Polecenie cmdlet **Get-AzDeploymentManagerArtifactSource** Pobiera źródło artefaktów i zwraca obiekt reprezentujący to źródło artefaktu.</span><span class="sxs-lookup"><span data-stu-id="59bc3-109">The **Get-AzDeploymentManagerArtifactSource** cmdlet gets an artifact source, and returns an object that represents that artifact source.</span></span>
<span data-ttu-id="59bc3-110">Określ źródło artefaktu, podając jego nazwę i nazwę grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="59bc3-110">Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="59bc3-111">Alternatywnie możesz podać obiekt ArtifactSource lub ResourceId.</span><span class="sxs-lookup"><span data-stu-id="59bc3-111">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="59bc3-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="59bc3-112">EXAMPLES</span></span>

### <span data-ttu-id="59bc3-113">Przykład 1: uzyskiwanie źródła artefaktu</span><span class="sxs-lookup"><span data-stu-id="59bc3-113">Example 1: Get an artifact source</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="59bc3-114">To polecenie pobiera Źródło artefaktów o nazwie ContosoArtifactSource w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="59bc3-114">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="59bc3-115">Przykład 2: uzyskiwanie źródła artefaktu przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="59bc3-115">Example 2: Get an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="59bc3-116">To polecenie pobiera Źródło artefaktów o nazwie ContosoArtifactSource w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="59bc3-116">This command gets an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="59bc3-117">Przykład 3: uzyskiwanie źródła artefaktu przy użyciu obiektu zwróconego przez New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="59bc3-117">Example 3: Get an artifact source using an object returned by New-AzDeploymentManagerArtifactSource</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="59bc3-118">To polecenie uzyskuje Źródło artefaktów, których nazwa i przysourcename są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="59bc3-118">This command gets an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="59bc3-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="59bc3-119">PARAMETERS</span></span>

### <span data-ttu-id="59bc3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59bc3-120">-DefaultProfile</span></span>
<span data-ttu-id="59bc3-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="59bc3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59bc3-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="59bc3-122">-InputObject</span></span>
<span data-ttu-id="59bc3-123">Obiekt źródłowy artefaktu.</span><span class="sxs-lookup"><span data-stu-id="59bc3-123">Artifact Source object.</span></span>

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

### <span data-ttu-id="59bc3-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="59bc3-124">-Name</span></span>
<span data-ttu-id="59bc3-125">Nazwa źródła artefaktu.</span><span class="sxs-lookup"><span data-stu-id="59bc3-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="59bc3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59bc3-126">-ResourceGroupName</span></span>
<span data-ttu-id="59bc3-127">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="59bc3-127">The resource group.</span></span>

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

### <span data-ttu-id="59bc3-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="59bc3-128">-ResourceId</span></span>
<span data-ttu-id="59bc3-129">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="59bc3-129">The resource identifier.</span></span>

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

### <span data-ttu-id="59bc3-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59bc3-130">CommonParameters</span></span>
<span data-ttu-id="59bc3-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59bc3-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59bc3-132">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59bc3-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59bc3-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59bc3-133">INPUTS</span></span>

### <span data-ttu-id="59bc3-134">System. String</span><span class="sxs-lookup"><span data-stu-id="59bc3-134">System.String</span></span>

### <span data-ttu-id="59bc3-135">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="59bc3-135">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="59bc3-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="59bc3-136">OUTPUTS</span></span>

### <span data-ttu-id="59bc3-137">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="59bc3-137">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="59bc3-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="59bc3-138">NOTES</span></span>

## <span data-ttu-id="59bc3-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59bc3-139">RELATED LINKS</span></span>
