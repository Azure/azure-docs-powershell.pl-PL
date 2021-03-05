---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 9d5d79f65adbcab7ce61ad125e78189d0f84f9a7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980593"
---
# <span data-ttu-id="42edb-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="42edb-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="42edb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42edb-102">SYNOPSIS</span></span>
<span data-ttu-id="42edb-103">Aktualizuje źródło artefaktów.</span><span class="sxs-lookup"><span data-stu-id="42edb-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="42edb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="42edb-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42edb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="42edb-105">DESCRIPTION</span></span>
<span data-ttu-id="42edb-106">Polecenie **cmdlet Set-AzDeploymentManagerArtifactSource** aktualizuje źródło artefaktu za pomocą określonego obiektu źródłowego artefaktu.</span><span class="sxs-lookup"><span data-stu-id="42edb-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="42edb-107">Polecenie cmdlet zwraca zaktualizowany obiekt ArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="42edb-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="42edb-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="42edb-108">EXAMPLES</span></span>

### <span data-ttu-id="42edb-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="42edb-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="42edb-110">To polecenie aktualizuje źródło artefaktu, którego nazwa i grupa zasobów są zgodne odpowiednio z właściwościami Name (Nazwa) $artifactSourceObject ResourceGroupName (Nazwa grupy zasobów).</span><span class="sxs-lookup"><span data-stu-id="42edb-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="42edb-111">Źródło artefaktu zostanie zaktualizowane do właściwości określonych w $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="42edb-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="42edb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="42edb-112">PARAMETERS</span></span>

### <span data-ttu-id="42edb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42edb-113">-DefaultProfile</span></span>
<span data-ttu-id="42edb-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="42edb-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42edb-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="42edb-115">-InputObject</span></span>
<span data-ttu-id="42edb-116">Obiekt źródłowy artefaktu.</span><span class="sxs-lookup"><span data-stu-id="42edb-116">The artifact source object.</span></span>

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

### <span data-ttu-id="42edb-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="42edb-117">-Confirm</span></span>
<span data-ttu-id="42edb-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="42edb-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42edb-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42edb-119">-WhatIf</span></span>
<span data-ttu-id="42edb-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="42edb-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42edb-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="42edb-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42edb-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42edb-122">CommonParameters</span></span>
<span data-ttu-id="42edb-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="42edb-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42edb-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="42edb-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="42edb-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42edb-125">INPUTS</span></span>

### <span data-ttu-id="42edb-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="42edb-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="42edb-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="42edb-127">OUTPUTS</span></span>

### <span data-ttu-id="42edb-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="42edb-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="42edb-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="42edb-129">NOTES</span></span>

## <span data-ttu-id="42edb-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="42edb-130">RELATED LINKS</span></span>
