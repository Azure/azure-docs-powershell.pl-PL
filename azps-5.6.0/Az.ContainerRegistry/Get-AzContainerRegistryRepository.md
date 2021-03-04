---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryRepository.md
ms.openlocfilehash: efcd7fb518f66c99fab8b4cd456e8f8cea424ad7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990396"
---
# <span data-ttu-id="6c390-101">Get-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="6c390-101">Get-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="6c390-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c390-102">SYNOPSIS</span></span>
<span data-ttu-id="6c390-103">Pobierz lub przygotuj listę repozytoriów ACR.</span><span class="sxs-lookup"><span data-stu-id="6c390-103">Get or list ACR repositories.</span></span>

## <span data-ttu-id="6c390-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6c390-104">SYNTAX</span></span>

### <span data-ttu-id="6c390-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="6c390-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryRepository [-First <Int32>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c390-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="6c390-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c390-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6c390-107">DESCRIPTION</span></span>
<span data-ttu-id="6c390-108">Pobierz lub przygotuj listę repozytoriów ACR.</span><span class="sxs-lookup"><span data-stu-id="6c390-108">Get or list ACR repositories.</span></span>
<span data-ttu-id="6c390-109">Lista zwraca tylko nazwy repozytoriów.</span><span class="sxs-lookup"><span data-stu-id="6c390-109">List returns repository names only.</span></span>

## <span data-ttu-id="6c390-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6c390-110">EXAMPLES</span></span>

### <span data-ttu-id="6c390-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6c390-111">Example 1</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry
alpine
test/busybox0
test/busybox1
test/busybox10
```

<span data-ttu-id="6c390-112">Lista wszystkich repozytoriów w rejestrze.</span><span class="sxs-lookup"><span data-stu-id="6c390-112">List all repositories in registry.</span></span>

### <span data-ttu-id="6c390-113">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="6c390-113">Example 2</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -First 3
alpine
test/busybox0
test/busybox1
```

<span data-ttu-id="6c390-114">Wień pierwsze 3 repozytoria w rejestrze.</span><span class="sxs-lookup"><span data-stu-id="6c390-114">List first 3 repositories in registry.</span></span>

### <span data-ttu-id="6c390-115">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="6c390-115">Example 3</span></span>
```powershell
Get-AzContainerRegistryRepository -RegistryName registry -Name alpine

Registry             : registry.azurecr.io
ImageName            : alpine
CreatedTime          : 2020-10-13T05:45:25.5896115Z
LastUpdateTime       : 2021-01-04T08:31:46.2406505Z
ManifestCount        : 7
TagCount             : 1
ChangeableAttributes : Microsoft.Azure.Commands.ContainerRegistry.Models.PSChangeableAttribute
```

<span data-ttu-id="6c390-116">Get repository alpine under registry.</span><span class="sxs-lookup"><span data-stu-id="6c390-116">Get repository alpine under registry.</span></span>

## <span data-ttu-id="6c390-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6c390-117">PARAMETERS</span></span>

### <span data-ttu-id="6c390-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c390-118">-DefaultProfile</span></span>
<span data-ttu-id="6c390-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6c390-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c390-120">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6c390-120">-Name</span></span>
<span data-ttu-id="6c390-121">Nazwa repozytorium.</span><span class="sxs-lookup"><span data-stu-id="6c390-121">Repository Name.</span></span>

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

### <span data-ttu-id="6c390-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="6c390-122">-RegistryName</span></span>
<span data-ttu-id="6c390-123">Nazwa rejestru kontenerów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="6c390-123">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="6c390-124">— najpierw</span><span class="sxs-lookup"><span data-stu-id="6c390-124">-First</span></span>
<span data-ttu-id="6c390-125">Pierwsze n wyników.</span><span class="sxs-lookup"><span data-stu-id="6c390-125">First n results.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c390-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c390-126">CommonParameters</span></span>
<span data-ttu-id="6c390-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6c390-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c390-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6c390-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c390-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c390-129">INPUTS</span></span>

### <span data-ttu-id="6c390-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6c390-130">System.String</span></span>

## <span data-ttu-id="6c390-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6c390-131">OUTPUTS</span></span>

### <span data-ttu-id="6c390-132">System.String</span><span class="sxs-lookup"><span data-stu-id="6c390-132">System.String</span></span>

### <span data-ttu-id="6c390-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="6c390-133">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="6c390-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6c390-134">NOTES</span></span>

## <span data-ttu-id="6c390-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6c390-135">RELATED LINKS</span></span>
