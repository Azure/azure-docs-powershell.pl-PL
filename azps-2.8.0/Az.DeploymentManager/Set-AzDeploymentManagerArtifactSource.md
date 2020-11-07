---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/az.deploymentmanager/set-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/Set-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 32e5293f7c5bb62711a6510c590aa1ba7f4229b7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93705605"
---
# <span data-ttu-id="7585e-101">Set-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="7585e-101">Set-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="7585e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7585e-102">SYNOPSIS</span></span>
<span data-ttu-id="7585e-103">Umożliwia zaktualizowanie źródła artefaktów.</span><span class="sxs-lookup"><span data-stu-id="7585e-103">Updates the artifacts source.</span></span>

## <span data-ttu-id="7585e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7585e-104">SYNTAX</span></span>

```
Set-AzDeploymentManagerArtifactSource [-InputObject] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7585e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7585e-105">DESCRIPTION</span></span>
<span data-ttu-id="7585e-106">Polecenie cmdlet **Set-AzDeploymentManagerArtifactSource** umożliwia zaktualizowanie źródła artefaktu przy użyciu określonego obiektu źródłowego artefaktu.</span><span class="sxs-lookup"><span data-stu-id="7585e-106">The **Set-AzDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="7585e-107">Polecenie cmdlet zwraca zaktualizowany obiekt ArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="7585e-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="7585e-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7585e-108">EXAMPLES</span></span>

### <span data-ttu-id="7585e-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7585e-109">Example 1</span></span>
```powershell
PS C:\> Get-AzDeploymentManagerArtifactSource -InputObject $artifactSourceObject
```

<span data-ttu-id="7585e-110">To polecenie powoduje zaktualizowanie źródła artefaktu, którego nazwa i przysourcename są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="7585e-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="7585e-111">Źródło artefaktów zostanie zaktualizowane do właściwości ustawionych w $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="7585e-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="7585e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7585e-112">PARAMETERS</span></span>

### <span data-ttu-id="7585e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7585e-113">-DefaultProfile</span></span>
<span data-ttu-id="7585e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7585e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7585e-115">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7585e-115">-InputObject</span></span>
<span data-ttu-id="7585e-116">Obiekt źródłowy artefaktu.</span><span class="sxs-lookup"><span data-stu-id="7585e-116">The artifact source object.</span></span>

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

### <span data-ttu-id="7585e-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7585e-117">-Confirm</span></span>
<span data-ttu-id="7585e-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7585e-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7585e-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7585e-119">-WhatIf</span></span>
<span data-ttu-id="7585e-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7585e-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7585e-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7585e-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7585e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7585e-122">CommonParameters</span></span>
<span data-ttu-id="7585e-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7585e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7585e-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7585e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7585e-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7585e-125">INPUTS</span></span>

### <span data-ttu-id="7585e-126">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="7585e-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="7585e-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7585e-127">OUTPUTS</span></span>

### <span data-ttu-id="7585e-128">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="7585e-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="7585e-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7585e-129">NOTES</span></span>

## <span data-ttu-id="7585e-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7585e-130">RELATED LINKS</span></span>
