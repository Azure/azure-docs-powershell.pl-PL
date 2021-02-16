---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryManifest.md
ms.openlocfilehash: a37073de6a7960ae1ab90746372179db8e9d9386
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199115"
---
# <span data-ttu-id="d0f38-101">Remove-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="d0f38-101">Remove-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="d0f38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d0f38-102">SYNOPSIS</span></span>
<span data-ttu-id="d0f38-103">Usuwanie manifestu ACR.</span><span class="sxs-lookup"><span data-stu-id="d0f38-103">Delete ACR manifest.</span></span> 

## <span data-ttu-id="d0f38-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d0f38-104">SYNTAX</span></span>

### <span data-ttu-id="d0f38-105">ByManifestParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="d0f38-105">ByManifestParameterSet (Default)</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Manifest <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d0f38-106">ByTagParameterSet</span><span class="sxs-lookup"><span data-stu-id="d0f38-106">ByTagParameterSet</span></span>
```
Remove-AzContainerRegistryManifest -RepositoryName <String> -Tag <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d0f38-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="d0f38-107">DESCRIPTION</span></span>
<span data-ttu-id="d0f38-108">Usuwanie manifestu ACR.</span><span class="sxs-lookup"><span data-stu-id="d0f38-108">Delete ACR manifest.</span></span>
<span data-ttu-id="d0f38-109">Aby użyć tego polecenia cmdlet, uruchom polecenie `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="d0f38-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="d0f38-110">.</span><span class="sxs-lookup"><span data-stu-id="d0f38-110">first.</span></span>

## <span data-ttu-id="d0f38-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d0f38-111">EXAMPLES</span></span>

### <span data-ttu-id="d0f38-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d0f38-112">Example 1</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab
True
```

<span data-ttu-id="d0f38-113">Usuń manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under registry</span><span class="sxs-lookup"><span data-stu-id="d0f38-113">Delete manifest sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab for repository test/busybox27 under registry</span></span>

### <span data-ttu-id="d0f38-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="d0f38-114">Example 2</span></span>
```powershell
Remove-AzContainerRegistryManifest -RegistryName registry -RepositoryName test/busybox27 -Tag latest
True
```

<span data-ttu-id="d0f38-115">Usuwanie manifestu z najnowszym tagiem dla testu repozytorium/skrzynką busybox27 w rejestrze</span><span class="sxs-lookup"><span data-stu-id="d0f38-115">Delete manifest with tag latest for repository test/busybox27 under registry</span></span>

## <span data-ttu-id="d0f38-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d0f38-116">PARAMETERS</span></span>

### <span data-ttu-id="d0f38-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0f38-117">-DefaultProfile</span></span>
<span data-ttu-id="d0f38-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f38-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d0f38-119">- Manifest</span><span class="sxs-lookup"><span data-stu-id="d0f38-119">-Manifest</span></span>
<span data-ttu-id="d0f38-120">Odwołanie manifestu.</span><span class="sxs-lookup"><span data-stu-id="d0f38-120">Manifest reference.</span></span>

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

### <span data-ttu-id="d0f38-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="d0f38-121">-RegistryName</span></span>
<span data-ttu-id="d0f38-122">Nazwa rejestru kontenera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d0f38-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="d0f38-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="d0f38-123">-RepositoryName</span></span>
<span data-ttu-id="d0f38-124">Nazwa repozytorium.</span><span class="sxs-lookup"><span data-stu-id="d0f38-124">Repository Name.</span></span>

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

### <span data-ttu-id="d0f38-125">— Tag</span><span class="sxs-lookup"><span data-stu-id="d0f38-125">-Tag</span></span>
<span data-ttu-id="d0f38-126">Tag.</span><span class="sxs-lookup"><span data-stu-id="d0f38-126">Tag.</span></span>

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

### <span data-ttu-id="d0f38-127">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d0f38-127">-Confirm</span></span>
<span data-ttu-id="d0f38-128">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d0f38-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d0f38-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d0f38-129">-WhatIf</span></span>
<span data-ttu-id="d0f38-130">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d0f38-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d0f38-131">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d0f38-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d0f38-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0f38-132">CommonParameters</span></span>
<span data-ttu-id="d0f38-133">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0f38-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0f38-134">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d0f38-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0f38-135">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0f38-135">INPUTS</span></span>

### <span data-ttu-id="d0f38-136">System.String</span><span class="sxs-lookup"><span data-stu-id="d0f38-136">System.String</span></span>

## <span data-ttu-id="d0f38-137">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d0f38-137">OUTPUTS</span></span>

### <span data-ttu-id="d0f38-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d0f38-138">System.Boolean</span></span>

## <span data-ttu-id="d0f38-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d0f38-139">NOTES</span></span>

## <span data-ttu-id="d0f38-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0f38-140">RELATED LINKS</span></span>
