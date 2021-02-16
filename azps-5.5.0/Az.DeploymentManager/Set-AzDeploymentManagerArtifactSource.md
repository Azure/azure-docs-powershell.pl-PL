---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: ee69c178d48775a870b229e652a1584c413bd7ca
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242674"
---
# <span data-ttu-id="ba73b-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="ba73b-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="ba73b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba73b-102">SYNOPSIS</span></span>
<span data-ttu-id="ba73b-103">Aktualizuje źródło artefaktów.</span><span class="sxs-lookup"><span data-stu-id="ba73b-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="ba73b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="ba73b-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba73b-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="ba73b-105">DESCRIPTION</span></span>
<span data-ttu-id="ba73b-106">Polecenie **cmdlet Set-AzDeploymentManagerArtifactSource** aktualizuje źródło artefaktu za pomocą określonego obiektu źródłowego artefaktu.</span><span class="sxs-lookup"><span data-stu-id="ba73b-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="ba73b-107">Polecenie cmdlet zwraca zaktualizowany obiekt ArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="ba73b-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="ba73b-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="ba73b-108">EXAMPLES</span></span>

### <span data-ttu-id="ba73b-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ba73b-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="ba73b-110">To polecenie aktualizuje źródło artefaktu, którego nazwa i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa) $artifactSourceObject ResourceGroupName (Nazwa grupy zasobów).</span><span class="sxs-lookup"><span data-stu-id="ba73b-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="ba73b-111">Źródło artefaktu zostanie zaktualizowane do właściwości określonych w $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="ba73b-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="ba73b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ba73b-112">PARAMETERS</span></span>

### <span data-ttu-id="ba73b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba73b-113">-DefaultProfile</span></span>
<span data-ttu-id="ba73b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="ba73b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ba73b-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ba73b-115">-InputObject</span></span>
<span data-ttu-id="ba73b-116">Obiekt źródłowy artefaktu.</span><span class="sxs-lookup"><span data-stu-id="ba73b-116">The artifact source object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba73b-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ba73b-117">-Confirm</span></span>
<span data-ttu-id="ba73b-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ba73b-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ba73b-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba73b-119">-WhatIf</span></span>
<span data-ttu-id="ba73b-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ba73b-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ba73b-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="ba73b-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ba73b-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba73b-122">CommonParameters</span></span>
<span data-ttu-id="ba73b-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ba73b-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba73b-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ba73b-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba73b-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ba73b-125">INPUTS</span></span>

### <span data-ttu-id="ba73b-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="ba73b-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="ba73b-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="ba73b-127">OUTPUTS</span></span>

### <span data-ttu-id="ba73b-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="ba73b-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="ba73b-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="ba73b-129">NOTES</span></span>

## <span data-ttu-id="ba73b-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ba73b-130">RELATED LINKS</span></span>
