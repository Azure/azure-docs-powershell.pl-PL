---
external help file: Microsoft.Azure.Commands.DeploymentManager.dll-Help.xml
Module Name: AzureRM.DeploymentManager
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.deploymentmanager/set-azurermdeploymentmanagerartifactsource
schema: 2.0.0
ms.openlocfilehash: 230e443fad4740b6bf9896164f02ae9b382e3ed2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93523337"
---
# <span data-ttu-id="2681f-101">Set-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="2681f-101">Set-AzureRmDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="2681f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2681f-102">SYNOPSIS</span></span>
<span data-ttu-id="2681f-103">Umożliwia zaktualizowanie źródła artefaktu.</span><span class="sxs-lookup"><span data-stu-id="2681f-103">Updates an artifact source.</span></span>

## <span data-ttu-id="2681f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2681f-104">SYNTAX</span></span>

```
Set-AzureRmDeploymentManagerArtifactSource [-ArtifactSource] <PSArtifactSource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2681f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2681f-105">DESCRIPTION</span></span>
<span data-ttu-id="2681f-106">Polecenie cmdlet **Set-AzureRmDeploymentManagerArtifactSource** umożliwia zaktualizowanie źródła artefaktu przy użyciu określonego obiektu źródłowego artefaktu.</span><span class="sxs-lookup"><span data-stu-id="2681f-106">The **Set-AzureRmDeploymentManagerArtifactSource** cmdlet updates an artifact source with the specified artifact source object.</span></span>
<span data-ttu-id="2681f-107">Polecenie cmdlet zwraca zaktualizowany obiekt ArtifactSource.</span><span class="sxs-lookup"><span data-stu-id="2681f-107">The cmdlet returns the updated ArtifactSource object.</span></span>

## <span data-ttu-id="2681f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2681f-108">EXAMPLES</span></span>

### <span data-ttu-id="2681f-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2681f-109">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmDeploymentManagerArtifactSource -ArtifactSource $artifactSourceObject
```

<span data-ttu-id="2681f-110">To polecenie powoduje zaktualizowanie źródła artefaktu, którego nazwa i przysourcename są zgodne z właściwościami Name i ResourceGroupName odpowiednio w $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="2681f-110">This command updates an artifact source whose name and ResourceGroup match the Name and ResourceGroupName properties of the $artifactSourceObject, respectively.</span></span>
<span data-ttu-id="2681f-111">Źródło artefaktów zostanie zaktualizowane do właściwości ustawionych w $artifactSourceObject.</span><span class="sxs-lookup"><span data-stu-id="2681f-111">The artifact source would be updated to the properties set in the $artifactSourceObject.</span></span>

## <span data-ttu-id="2681f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2681f-112">PARAMETERS</span></span>

### <span data-ttu-id="2681f-113">-ArtifactSource</span><span class="sxs-lookup"><span data-stu-id="2681f-113">-ArtifactSource</span></span>
<span data-ttu-id="2681f-114">Obiekt źródłowy artefaktu.</span><span class="sxs-lookup"><span data-stu-id="2681f-114">The artifact source object.</span></span>

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

### <span data-ttu-id="2681f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2681f-115">-DefaultProfile</span></span>
<span data-ttu-id="2681f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2681f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2681f-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2681f-117">-Confirm</span></span>
<span data-ttu-id="2681f-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2681f-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2681f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2681f-119">-WhatIf</span></span>
<span data-ttu-id="2681f-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2681f-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2681f-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2681f-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2681f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2681f-122">CommonParameters</span></span>
<span data-ttu-id="2681f-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2681f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2681f-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2681f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2681f-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2681f-125">INPUTS</span></span>

### <span data-ttu-id="2681f-126">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="2681f-126">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="2681f-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2681f-127">OUTPUTS</span></span>

### <span data-ttu-id="2681f-128">Microsoft. Azure. Commands. Deploymentmanager. MODELES. PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="2681f-128">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="2681f-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2681f-129">NOTES</span></span>

## <span data-ttu-id="2681f-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2681f-130">RELATED LINKS</span></span>

[<span data-ttu-id="2681f-131">Nowe — AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="2681f-131">New-AzureRmDeploymentManagerArtifactSource</span></span>](./New-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="2681f-132">Get-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="2681f-132">Get-AzureRmDeploymentManagerArtifactSource</span></span>](./Get-AzureRmDeploymentManagerArtifactSource.md)

[<span data-ttu-id="2681f-133">Remove-AzureRmDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="2681f-133">Remove-AzureRmDeploymentManagerArtifactSource</span></span>](./Remove-AzureRmDeploymentManagerArtifactSource.md)