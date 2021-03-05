---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DeploymentManager.dll-Help.xml
Module Name: Az.DeploymentManager
online version: https://docs.microsoft.com/powershell/module/az.deploymentmanager/new-azdeploymentmanagerartifactsource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DeploymentManager/DeploymentManager/help/New-AzDeploymentManagerArtifactSource.md
ms.openlocfilehash: 8aab061d7f61605273bd7147dc5a85ca45bf8ad0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966321"
---
# <span data-ttu-id="2d7c3-101">New-AzDeploymentManagerArtifactSource</span><span class="sxs-lookup"><span data-stu-id="2d7c3-101">New-AzDeploymentManagerArtifactSource</span></span>

## <span data-ttu-id="2d7c3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d7c3-102">SYNOPSIS</span></span>
<span data-ttu-id="2d7c3-103">Tworzy źródło artefaktu.</span><span class="sxs-lookup"><span data-stu-id="2d7c3-103">Creates an artifact source.</span></span>

## <span data-ttu-id="2d7c3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2d7c3-104">SYNTAX</span></span>

```
New-AzDeploymentManagerArtifactSource -ResourceGroupName <String> -Name <String> -Location <String>
 -SasUri <String> [-Tag <Hashtable>] [-ArtifactRoot <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d7c3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2d7c3-105">DESCRIPTION</span></span>
<span data-ttu-id="2d7c3-106">Polecenie **cmdlet New-AzDeploymentManagerArtifactSource** tworzy źródło artefaktu.</span><span class="sxs-lookup"><span data-stu-id="2d7c3-106">The **New-AzDeploymentManagerArtifactSource** cmdlet creates an artifact source.</span></span>
<span data-ttu-id="2d7c3-107">Określ właściwości *Name (Nazwa* *Grupy Zasobów)* i Required (Nazwa Grupy Zasobów).</span><span class="sxs-lookup"><span data-stu-id="2d7c3-107">Specify the *Name*, *ResourceGroupName* and required properties.</span></span>

<span data-ttu-id="2d7c3-108">Zwrócony obiekt można zmodyfikować lokalnie, a następnie zastosować zmiany do źródła artefaktu za pomocą Set-AzDeploymentManagerArtifactSource cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d7c3-108">You can modify the returned object locally and then apply the changes to the artifact source by using the Set-AzDeploymentManagerArtifactSource cmdlet.</span></span>

<span data-ttu-id="2d7c3-109">Polecenie cmdlet zwraca obiekt ArtifactSource o identyfikatorze Zasobu, do którego można się odwołać w tym poleceniem cmdlet programu New-AzDeploymentManagerServiceTopology, dzięki czemu do artefaktów wymaganych dla zasobu ServiceUnit, plików Template i Parameters można odwoływać się z tej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="2d7c3-109">The cmdlet returns an ArtifactSource object that has a ResourceId which can be referenced in the New-AzDeploymentManagerServiceTopology cmdlet so that artifacts required for a ServiceUnit resource, the Template and Parameters files, can be referenced from this location.</span></span>

## <span data-ttu-id="2d7c3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2d7c3-110">EXAMPLES</span></span>

### <span data-ttu-id="2d7c3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2d7c3-111">Example 1</span></span>
```powershell
PS C:\> New-AzDeploymentManagerArtifactSource -ResourceGroupName ContosoResourceGroup -Name ContosoArtifactSource -Location "Central US" -SasUri "https://ContosoStorage.blob.core.windows.net/ContosoArtifacts?sasParameters"
```

<span data-ttu-id="2d7c3-112">Tworzy źródło artefaktu w grupie ContosoResourceGroup o nazwie ContosoArtifactSource (Źródło ContosoArtifactSource) z lokalizacją zasobu w Środkowych Stanów Zjednoczonych.</span><span class="sxs-lookup"><span data-stu-id="2d7c3-112">Creates an artifact source in the ContosoResourceGroup with the name ContosoArtifactSource with Central US as the location of the resource.</span></span> <span data-ttu-id="2d7c3-113">Właściwość SasUri dostarcza do kontenera magazynu, w którym są przechowywane artefakty, wartość SAS Uri magazynu platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2d7c3-113">The SasUri property provides an Azure Storage SAS Uri to the storage container where the artifacts are stored.</span></span>

## <span data-ttu-id="2d7c3-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d7c3-114">PARAMETERS</span></span>

### <span data-ttu-id="2d7c3-115">-ArtifactRoot</span><span class="sxs-lookup"><span data-stu-id="2d7c3-115">-ArtifactRoot</span></span>
<span data-ttu-id="2d7c3-116">Opcjonalne przesunięcie katalogu pod kontenerem magazynu dla artefaktów.</span><span class="sxs-lookup"><span data-stu-id="2d7c3-116">The optional directory offset under the storage container for the artifacts.</span></span>

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

### <span data-ttu-id="2d7c3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d7c3-117">-DefaultProfile</span></span>
<span data-ttu-id="2d7c3-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d7c3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2d7c3-119">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="2d7c3-119">-Location</span></span>
<span data-ttu-id="2d7c3-120">Lokalizacja zasobu.</span><span class="sxs-lookup"><span data-stu-id="2d7c3-120">The location of the resource.</span></span>

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

### <span data-ttu-id="2d7c3-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="2d7c3-121">-Name</span></span>
<span data-ttu-id="2d7c3-122">Nazwa źródła artefaktu.</span><span class="sxs-lookup"><span data-stu-id="2d7c3-122">The name of the artifact source.</span></span>

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

### <span data-ttu-id="2d7c3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d7c3-123">-ResourceGroupName</span></span>
<span data-ttu-id="2d7c3-124">Grupa zasobów.</span><span class="sxs-lookup"><span data-stu-id="2d7c3-124">The resource group.</span></span>

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

### <span data-ttu-id="2d7c3-125">- SasUri</span><span class="sxs-lookup"><span data-stu-id="2d7c3-125">-SasUri</span></span>
<span data-ttu-id="2d7c3-126">Uri SAS do kontenera magazynu platformy Azure, w którym są przechowywane artefakty.</span><span class="sxs-lookup"><span data-stu-id="2d7c3-126">The SAS Uri to the Azure storage container where the artifacts are stored.</span></span>

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

### <span data-ttu-id="2d7c3-127">— Tag</span><span class="sxs-lookup"><span data-stu-id="2d7c3-127">-Tag</span></span>
<span data-ttu-id="2d7c3-128">Tabela skrótów reprezentująca tagi zasobów.</span><span class="sxs-lookup"><span data-stu-id="2d7c3-128">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="2d7c3-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2d7c3-129">-Confirm</span></span>
<span data-ttu-id="2d7c3-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2d7c3-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d7c3-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d7c3-131">-WhatIf</span></span>
<span data-ttu-id="2d7c3-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d7c3-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d7c3-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2d7c3-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d7c3-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d7c3-134">CommonParameters</span></span>
<span data-ttu-id="2d7c3-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d7c3-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d7c3-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2d7c3-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d7c3-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d7c3-137">INPUTS</span></span>

### <span data-ttu-id="2d7c3-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2d7c3-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2d7c3-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d7c3-139">OUTPUTS</span></span>

### <span data-ttu-id="2d7c3-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span><span class="sxs-lookup"><span data-stu-id="2d7c3-140">Microsoft.Azure.Commands.DeploymentManager.Models.PSArtifactSource</span></span>

## <span data-ttu-id="2d7c3-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2d7c3-141">NOTES</span></span>

## <span data-ttu-id="2d7c3-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d7c3-142">RELATED LINKS</span></span>
