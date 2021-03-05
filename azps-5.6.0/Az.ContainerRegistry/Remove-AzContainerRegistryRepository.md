---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/remove-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
ms.openlocfilehash: 1c0ad2ae46987a526be4e8fda110dada914bd27e
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101975450"
---
# <span data-ttu-id="8c189-101">Remove-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="8c189-101">Remove-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="8c189-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8c189-102">SYNOPSIS</span></span>
<span data-ttu-id="8c189-103">Usuwanie repozytorium z acr.</span><span class="sxs-lookup"><span data-stu-id="8c189-103">Delete repository from ACR.</span></span>

## <span data-ttu-id="8c189-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8c189-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8c189-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8c189-105">DESCRIPTION</span></span>
<span data-ttu-id="8c189-106">Usuwanie repozytorium z acr.</span><span class="sxs-lookup"><span data-stu-id="8c189-106">Delete repository from ACR.</span></span>

## <span data-ttu-id="8c189-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8c189-107">EXAMPLES</span></span>

### <span data-ttu-id="8c189-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8c189-108">Example 1</span></span>
```powershell
Remove-AzContainerRegistryRepository -RegistryName registry -Name test/busybox15

ManifestsDeleted                                                          TagsDeleted
----------------                                                          -----------
{sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab} {latest}
```

<span data-ttu-id="8c189-109">Usuń test repozytorium/skrzynkę zajęty15 w rejestrze.</span><span class="sxs-lookup"><span data-stu-id="8c189-109">Delete repository test/busybox15 under registry.</span></span>

## <span data-ttu-id="8c189-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8c189-110">PARAMETERS</span></span>

### <span data-ttu-id="8c189-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8c189-111">-DefaultProfile</span></span>
<span data-ttu-id="8c189-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8c189-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8c189-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8c189-113">-Name</span></span>
<span data-ttu-id="8c189-114">Nazwa repozytorium.</span><span class="sxs-lookup"><span data-stu-id="8c189-114">Repository Name.</span></span>

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

### <span data-ttu-id="8c189-115">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="8c189-115">-RegistryName</span></span>
<span data-ttu-id="8c189-116">Nazwa rejestru kontenerów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8c189-116">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="8c189-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8c189-117">-Confirm</span></span>
<span data-ttu-id="8c189-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8c189-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8c189-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8c189-119">-WhatIf</span></span>
<span data-ttu-id="8c189-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8c189-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8c189-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8c189-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8c189-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8c189-122">CommonParameters</span></span>
<span data-ttu-id="8c189-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8c189-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8c189-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8c189-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8c189-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c189-125">INPUTS</span></span>

### <span data-ttu-id="8c189-126">System.String</span><span class="sxs-lookup"><span data-stu-id="8c189-126">System.String</span></span>

## <span data-ttu-id="8c189-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8c189-127">OUTPUTS</span></span>

### <span data-ttu-id="8c189-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span><span class="sxs-lookup"><span data-stu-id="8c189-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span></span>

## <span data-ttu-id="8c189-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8c189-129">NOTES</span></span>

## <span data-ttu-id="8c189-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8c189-130">RELATED LINKS</span></span>
