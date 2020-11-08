---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/remove-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Remove-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: fa9dc4f8234e9c6e709d59f3945b05eeceef4316
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053370"
---
# <span data-ttu-id="1491f-101">Remove-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="1491f-101">Remove-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="1491f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1491f-102">SYNOPSIS</span></span>
<span data-ttu-id="1491f-103">Usuwa określone źródło artefaktu.</span><span class="sxs-lookup"><span data-stu-id="1491f-103">Deletes the specified artifact source.</span></span>

## <span data-ttu-id="1491f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1491f-104">SYNTAX</span></span>

### <span data-ttu-id="1491f-105">Interaktywny (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="1491f-105">Interactive (Default)</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1491f-106">Zasobów</span><span class="sxs-lookup"><span data-stu-id="1491f-106">ResourceId</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1491f-107">Inputobject</span><span class="sxs-lookup"><span data-stu-id="1491f-107">InputObject</span></span>
```
Remove-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1491f-108">Opis</span><span class="sxs-lookup"><span data-stu-id="1491f-108">DESCRIPTION</span></span>
<span data-ttu-id="1491f-109">Polecenie cmdlet **Remove-AzDeploymentManagerArtifactSource** usuwa Źródło artefaktów, określając źródło artefaktu przy użyciu nazwy i nazwy grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1491f-109">The **Remove-AzDeploymentManagerArtifactSource** cmdlet deletes an artifact source Specify the artifact source by its name and resource group name.</span></span> <span data-ttu-id="1491f-110">Alternatywnie możesz podać obiekt ArtifactSource lub ResourceId.</span><span class="sxs-lookup"><span data-stu-id="1491f-110">Alternately, you can provide the ArtifactSource object or the ResourceId.</span></span>

## <span data-ttu-id="1491f-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1491f-111">EXAMPLES</span></span>

### <span data-ttu-id="1491f-112">Przykład 1: Usuwanie źródła artefaktu</span><span class="sxs-lookup"><span data-stu-id="1491f-112">Example 1: Delete an artifact source</span></span>
### <span data-ttu-id="1491f-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1491f-113">Example 1</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceGroupName "ContosoResourceGroup" -Name "ContosoArtifactSource"
```

<span data-ttu-id="1491f-114">To polecenie usuwa Źródło artefaktu o nazwie ContosoArtifactSource w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1491f-114">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="1491f-115">Przykład 2: Usuwanie źródła artefaktu przy użyciu identyfikatora zasobu</span><span class="sxs-lookup"><span data-stu-id="1491f-115">Example 2: Delete an artifact source using the resource identifier</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -ResourceId "/subscriptions/subscriptionId/resourcegroups/ContosoResourceGroup/providers/Microsoft.DeploymentManager/artifactSources/ContosoArtifactSource"
```

<span data-ttu-id="1491f-116">To polecenie usuwa Źródło artefaktu o nazwie ContosoArtifactSource w ContosoResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="1491f-116">This command deletes an artifact source named ContosoArtifactSource in ContosoResourceGroup.</span></span>

### <span data-ttu-id="1491f-117">Przykład 3: Usuwanie źródła artefaktu przy użyciu obiektu</span><span class="sxs-lookup"><span data-stu-id="1491f-117">Example 3: Delete an artifact source using an object</span></span>
```powershell
PS C:\> Remove-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="1491f-118">To polecenie powoduje usunięcie źródła artefaktów, których nazwa i przysourcename są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="1491f-118">This command deletes an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>

## <span data-ttu-id="1491f-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1491f-119">PARAMETERS</span></span>

### <span data-ttu-id="1491f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1491f-120">-DefaultProfile</span></span>
<span data-ttu-id="1491f-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1491f-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1491f-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1491f-122">-InputObject</span></span>
<span data-ttu-id="1491f-123">Źródło artefaktu, które ma zostać usunięte.</span><span class="sxs-lookup"><span data-stu-id="1491f-123">The artifact source to be removed.</span></span>

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

### <span data-ttu-id="1491f-124">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1491f-124">-Name</span></span>
<span data-ttu-id="1491f-125">Nazwa źródła artefaktu.</span><span class="sxs-lookup"><span data-stu-id="1491f-125">The name of the artifact source.</span></span>

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

### <span data-ttu-id="1491f-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1491f-126">-PassThru</span></span>
<span data-ttu-id="1491f-127">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="1491f-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="1491f-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1491f-128">-ResourceGroupName</span></span>
<span data-ttu-id="1491f-129">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="1491f-129">The resource group.</span></span>

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

### <span data-ttu-id="1491f-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1491f-130">-ResourceId</span></span>
<span data-ttu-id="1491f-131">Identyfikator zasobu.</span><span class="sxs-lookup"><span data-stu-id="1491f-131">The resource identifier.</span></span>

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

### <span data-ttu-id="1491f-132">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1491f-132">-Confirm</span></span>
<span data-ttu-id="1491f-133">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1491f-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1491f-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1491f-134">-WhatIf</span></span>
<span data-ttu-id="1491f-135">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1491f-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1491f-136">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1491f-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1491f-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1491f-137">CommonParameters</span></span>
<span data-ttu-id="1491f-138">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1491f-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1491f-139">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1491f-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1491f-140">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1491f-140">INPUTS</span></span>

### <span data-ttu-id="1491f-141">System. String</span><span class="sxs-lookup"><span data-stu-id="1491f-141">System.String</span></span>

### <span data-ttu-id="1491f-142">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="1491f-142">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="1491f-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1491f-143">OUTPUTS</span></span>

### <span data-ttu-id="1491f-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1491f-144">System.Boolean</span></span>

## <span data-ttu-id="1491f-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1491f-145">NOTES</span></span>

## <span data-ttu-id="1491f-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1491f-146">RELATED LINKS</span></span>
