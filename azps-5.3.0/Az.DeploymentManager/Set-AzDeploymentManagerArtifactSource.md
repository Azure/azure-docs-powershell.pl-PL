---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: ee69c178d48775a870b229e652a1584c413bd7ca
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98499293"
---
# <span data-ttu-id="111c3-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="111c3-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="111c3-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="111c3-102">SYNOPSIS</span></span>
<span data-ttu-id="111c3-103">Umożliwia zaktualizowanie źródła artefaktów.</span><span class="sxs-lookup"><span data-stu-id="111c3-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="111c3-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="111c3-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="111c3-105">Opis</span><span class="sxs-lookup"><span data-stu-id="111c3-105">DESCRIPTION</span></span>
<span data-ttu-id="111c3-106">Polecenie cmdlet **Set-AzDeploymentManagerArtifactSource** umożliwia zaktualizowanie źródła artefaktu przy użyciu określonego obiektu źródłowego artefaktu.</span><span class="sxs-lookup"><span data-stu-id="111c3-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="111c3-107">Polecenie cmdlet zwraca zaktualizowany obiekt ArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="111c3-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="111c3-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="111c3-108">EXAMPLES</span></span>

### <span data-ttu-id="111c3-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="111c3-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="111c3-110">To polecenie powoduje zaktualizowanie źródła artefaktu, którego nazwa i przysourcename są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="111c3-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="111c3-111">Źródło artefaktów zostanie zaktualizowane do właściwości ustawionych w $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="111c3-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="111c3-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="111c3-112">PARAMETERS</span></span>

### <span data-ttu-id="111c3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="111c3-113">-DefaultProfile</span></span>
<span data-ttu-id="111c3-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="111c3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="111c3-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="111c3-115">-InputObject</span></span>
<span data-ttu-id="111c3-116">Obiekt źródłowy artefaktu.</span><span class="sxs-lookup"><span data-stu-id="111c3-116">The artifact source object.</span></span>

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

### <span data-ttu-id="111c3-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="111c3-117">-Confirm</span></span>
<span data-ttu-id="111c3-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="111c3-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="111c3-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="111c3-119">-WhatIf</span></span>
<span data-ttu-id="111c3-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="111c3-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="111c3-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="111c3-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="111c3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="111c3-122">CommonParameters</span></span>
<span data-ttu-id="111c3-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="111c3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="111c3-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="111c3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="111c3-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="111c3-125">INPUTS</span></span>

### <span data-ttu-id="111c3-126">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="111c3-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="111c3-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="111c3-127">OUTPUTS</span></span>

### <span data-ttu-id="111c3-128">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="111c3-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="111c3-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="111c3-129">NOTES</span></span>

## <span data-ttu-id="111c3-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="111c3-130">RELATED LINKS</span></span>
