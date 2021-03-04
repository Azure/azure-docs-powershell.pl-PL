---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryManifest.md
ms.openlocfilehash: 030f0b00ba77bc967a53ce43c4f08d66c214f67e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956289"
---
# <span data-ttu-id="e743c-101">Update-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="e743c-101">Update-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="e743c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e743c-102">SYNOPSIS</span></span>
<span data-ttu-id="e743c-103">Aktualizowanie manifestu usługi ACR.</span><span class="sxs-lookup"><span data-stu-id="e743c-103">Update ACR manifest.</span></span> 

## <span data-ttu-id="e743c-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e743c-104">SYNTAX</span></span>

### <span data-ttu-id="e743c-105">ByManifestParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="e743c-105">ByManifestParameterSet (Default)</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e743c-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="e743c-106">ByTagParameterSet</span></span>
```
Update-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e743c-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e743c-107">DESCRIPTION</span></span>
<span data-ttu-id="e743c-108">Aktualizowanie manifestu usługi ACR.</span><span class="sxs-lookup"><span data-stu-id="e743c-108">Update ACR manifest.</span></span>
<span data-ttu-id="e743c-109">Aby użyć tego polecenia cmdlet, uruchom polecenie `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="e743c-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="e743c-110">.</span><span class="sxs-lookup"><span data-stu-id="e743c-110">first.</span></span>

## <span data-ttu-id="e743c-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e743c-111">EXAMPLES</span></span>

### <span data-ttu-id="e743c-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="e743c-112">Example 1</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="e743c-113">Update attributes for manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 under registry.</span><span class="sxs-lookup"><span data-stu-id="e743c-113">Update attributes for manifest sha256:185518070891758909c9f839cf4ca393ee977ac378609f700f60a771a2dfe321 under registry.</span></span>

### <span data-ttu-id="e743c-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="e743c-114">Example 2</span></span>
```powershell
Update-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Tag latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="e743c-115">Aktualizowanie atrybutów manifestu przy użyciu tagu najnowsze w rejestrze.</span><span class="sxs-lookup"><span data-stu-id="e743c-115">Update attributes for manifest with tag latest under registry.</span></span>

## <span data-ttu-id="e743c-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e743c-116">PARAMETERS</span></span>

### <span data-ttu-id="e743c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e743c-117">-DefaultProfile</span></span>
<span data-ttu-id="e743c-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e743c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e743c-119">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="e743c-119">-DeleteEnabled</span></span>
<span data-ttu-id="e743c-120">Usuń włącz.</span><span class="sxs-lookup"><span data-stu-id="e743c-120">Delete enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e743c-121">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="e743c-121">-ListEnabled</span></span>
<span data-ttu-id="e743c-122">Włączanie listy.</span><span class="sxs-lookup"><span data-stu-id="e743c-122">List enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e743c-123">-Manifest</span><span class="sxs-lookup"><span data-stu-id="e743c-123">-Manifest</span></span>
<span data-ttu-id="e743c-124">Odwołanie manifestu.</span><span class="sxs-lookup"><span data-stu-id="e743c-124">Manifest reference.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManifestParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e743c-125">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="e743c-125">-ReadEnabled</span></span>
<span data-ttu-id="e743c-126">Włącz czytanie.</span><span class="sxs-lookup"><span data-stu-id="e743c-126">Read enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e743c-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="e743c-127">-RegistryName</span></span>
<span data-ttu-id="e743c-128">Nazwa rejestru kontenerów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e743c-128">Azure Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e743c-129">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="e743c-129">-RepositoryName</span></span>
<span data-ttu-id="e743c-130">Nazwa repozytorium.</span><span class="sxs-lookup"><span data-stu-id="e743c-130">Repository Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e743c-131">— Tag</span><span class="sxs-lookup"><span data-stu-id="e743c-131">-Tag</span></span>
<span data-ttu-id="e743c-132">Tag.</span><span class="sxs-lookup"><span data-stu-id="e743c-132">Tag.</span></span>

```yaml
Type: System.String
Parameter Sets: ByTagParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e743c-133">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="e743c-133">-WriteEnabled</span></span>
<span data-ttu-id="e743c-134">Włącz pisanie.</span><span class="sxs-lookup"><span data-stu-id="e743c-134">Write enable.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e743c-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e743c-135">-Confirm</span></span>
<span data-ttu-id="e743c-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e743c-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e743c-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e743c-137">-WhatIf</span></span>
<span data-ttu-id="e743c-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e743c-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e743c-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e743c-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e743c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e743c-140">CommonParameters</span></span>
<span data-ttu-id="e743c-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e743c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e743c-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e743c-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e743c-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e743c-143">INPUTS</span></span>

### <span data-ttu-id="e743c-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e743c-144">System.String</span></span>

## <span data-ttu-id="e743c-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e743c-145">OUTPUTS</span></span>

### <span data-ttu-id="e743c-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span><span class="sxs-lookup"><span data-stu-id="e743c-146">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

## <span data-ttu-id="e743c-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e743c-147">NOTES</span></span>

## <span data-ttu-id="e743c-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e743c-148">RELATED LINKS</span></span>
