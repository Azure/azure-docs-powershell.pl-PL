---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrymanifest
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryManifest.md
ms.openlocfilehash: 5477dc0402d79228a9283f9c9e88b0fd34e425ba
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004417"
---
# <span data-ttu-id="94d21-101">Get-AzContainerRegistryManifest</span><span class="sxs-lookup"><span data-stu-id="94d21-101">Get-AzContainerRegistryManifest</span></span>

## <span data-ttu-id="94d21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94d21-102">SYNOPSIS</span></span>
<span data-ttu-id="94d21-103">Pobierz manifest ACR lub przygotuj go na liście.</span><span class="sxs-lookup"><span data-stu-id="94d21-103">Get or list ACR manifest.</span></span> 

## <span data-ttu-id="94d21-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="94d21-104">SYNTAX</span></span>

### <span data-ttu-id="94d21-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="94d21-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="94d21-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="94d21-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryManifest -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="94d21-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="94d21-107">DESCRIPTION</span></span>
<span data-ttu-id="94d21-108">Pobierz manifest ACR lub przygotuj go na liście.</span><span class="sxs-lookup"><span data-stu-id="94d21-108">Get or list ACR manifest.</span></span>
<span data-ttu-id="94d21-109">Aby użyć tego polecenia cmdlet, uruchom polecenie `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="94d21-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="94d21-110">.</span><span class="sxs-lookup"><span data-stu-id="94d21-110">first.</span></span>

## <span data-ttu-id="94d21-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="94d21-111">EXAMPLES</span></span>

### <span data-ttu-id="94d21-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="94d21-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine

Registry                    ImageName                   ManifestsAttributes
--------                    ---------                   -------------------
registry.azurecr.io         registry.azurecr.io         {Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase, Microsoft.Azure.Comm…}
```

<span data-ttu-id="94d21-113">Manifesty listy dla repozytorium w obszarze rejestru.</span><span class="sxs-lookup"><span data-stu-id="94d21-113">List manifests for repository alpine under registry.</span></span>

### <span data-ttu-id="94d21-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="94d21-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryManifest -RegistryName registry -RepositoryName alpine -Name sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttributeBase
```

<span data-ttu-id="94d21-115">Pobierz manifesty: sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0 dla repozytorium alpine w rejestrze.</span><span class="sxs-lookup"><span data-stu-id="94d21-115">Get manifests sha256:a5426f084c755f4d6c1d1562a2d456aa574a24a61706f6806415627360c06ac0 for repository alpine under registry.</span></span>

## <span data-ttu-id="94d21-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="94d21-116">PARAMETERS</span></span>

### <span data-ttu-id="94d21-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94d21-117">-DefaultProfile</span></span>
<span data-ttu-id="94d21-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="94d21-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="94d21-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="94d21-119">-Name</span></span>
<span data-ttu-id="94d21-120">Odwołanie manifestu.</span><span class="sxs-lookup"><span data-stu-id="94d21-120">Manifest reference.</span></span>

```yaml
Type: System.String
Parameter Sets: GetParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="94d21-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="94d21-121">-RegistryName</span></span>
<span data-ttu-id="94d21-122">Nazwa rejestru kontenerów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="94d21-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="94d21-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="94d21-123">-RepositoryName</span></span>
<span data-ttu-id="94d21-124">Nazwa repozytorium.</span><span class="sxs-lookup"><span data-stu-id="94d21-124">Repository Name.</span></span>

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

### <span data-ttu-id="94d21-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94d21-125">CommonParameters</span></span>
<span data-ttu-id="94d21-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94d21-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94d21-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="94d21-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94d21-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94d21-128">INPUTS</span></span>

### <span data-ttu-id="94d21-129">System.String</span><span class="sxs-lookup"><span data-stu-id="94d21-129">System.String</span></span>

## <span data-ttu-id="94d21-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="94d21-130">OUTPUTS</span></span>

### <span data-ttu-id="94d21-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span><span class="sxs-lookup"><span data-stu-id="94d21-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSManifestAttribute</span></span>

### <span data-ttu-id="94d21-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSAcrManifest</span><span class="sxs-lookup"><span data-stu-id="94d21-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSAcrManifest</span></span>

## <span data-ttu-id="94d21-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="94d21-133">NOTES</span></span>

## <span data-ttu-id="94d21-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="94d21-134">RELATED LINKS</span></span>
