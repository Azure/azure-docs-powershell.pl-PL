---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/get-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryTag.md
ms.openlocfilehash: 37308ab02db132e03cf4f44536bc44d0d6845a86
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990361"
---
# <span data-ttu-id="5449f-101">Get-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="5449f-101">Get-AzContainerRegistryTag</span></span>

## <span data-ttu-id="5449f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5449f-102">SYNOPSIS</span></span>
<span data-ttu-id="5449f-103">Pobierz tag ACR lub wywszukaj go na liście.</span><span class="sxs-lookup"><span data-stu-id="5449f-103">Get or list ACR tag.</span></span> 

## <span data-ttu-id="5449f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5449f-104">SYNTAX</span></span>

### <span data-ttu-id="5449f-105">ListParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="5449f-105">ListParameterSet (Default)</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5449f-106">GetParameterSet</span><span class="sxs-lookup"><span data-stu-id="5449f-106">GetParameterSet</span></span>
```
Get-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5449f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="5449f-107">DESCRIPTION</span></span>
<span data-ttu-id="5449f-108">Pobierz tag ACR lub wywszukaj go na liście.</span><span class="sxs-lookup"><span data-stu-id="5449f-108">Get or list ACR tag.</span></span>
<span data-ttu-id="5449f-109">Aby użyć tego polecenia cmdlet, uruchom polecenie `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span><span class="sxs-lookup"><span data-stu-id="5449f-109">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -ReadEnable $true -ListEnable $true`</span></span>
<span data-ttu-id="5449f-110">.</span><span class="sxs-lookup"><span data-stu-id="5449f-110">first.</span></span>

## <span data-ttu-id="5449f-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5449f-111">EXAMPLES</span></span>

### <span data-ttu-id="5449f-112">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5449f-112">Example 1</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine

Registry                    ImageName Tags
--------                    --------- ----
registry.azurecr.io alpine    {latest}
```

<span data-ttu-id="5449f-113">Tagi listy dla repozytorium w obszarze rejestru.</span><span class="sxs-lookup"><span data-stu-id="5449f-113">List tags for repository alpine under registry.</span></span>

### <span data-ttu-id="5449f-114">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="5449f-114">Example 2</span></span>
```powershell
Get-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -name latest

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttributeBase
```

<span data-ttu-id="5449f-115">Pobierz najnowszy tag dla repozytorium w obszarze rejestru.</span><span class="sxs-lookup"><span data-stu-id="5449f-115">Get tag latest for repository alpine under registry.</span></span>

## <span data-ttu-id="5449f-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5449f-116">PARAMETERS</span></span>

### <span data-ttu-id="5449f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5449f-117">-DefaultProfile</span></span>
<span data-ttu-id="5449f-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5449f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5449f-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="5449f-119">-Name</span></span>
<span data-ttu-id="5449f-120">Tag.</span><span class="sxs-lookup"><span data-stu-id="5449f-120">Tag.</span></span>

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

### <span data-ttu-id="5449f-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="5449f-121">-RegistryName</span></span>
<span data-ttu-id="5449f-122">Nazwa rejestru kontenerów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5449f-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="5449f-123">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="5449f-123">-RepositoryName</span></span>
<span data-ttu-id="5449f-124">Nazwa repozytorium.</span><span class="sxs-lookup"><span data-stu-id="5449f-124">Repository Name.</span></span>

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

### <span data-ttu-id="5449f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5449f-125">CommonParameters</span></span>
<span data-ttu-id="5449f-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5449f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5449f-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5449f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5449f-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5449f-128">INPUTS</span></span>

### <span data-ttu-id="5449f-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5449f-129">System.String</span></span>

## <span data-ttu-id="5449f-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5449f-130">OUTPUTS</span></span>

### <span data-ttu-id="5449f-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="5449f-131">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

### <span data-ttu-id="5449f-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span><span class="sxs-lookup"><span data-stu-id="5449f-132">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagList</span></span>

## <span data-ttu-id="5449f-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5449f-133">NOTES</span></span>

## <span data-ttu-id="5449f-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5449f-134">RELATED LINKS</span></span>
