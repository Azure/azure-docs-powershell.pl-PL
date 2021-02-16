---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/remove-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryRepository.md
ms.openlocfilehash: a99d020bbdef81868fb0e4338c7bc6c722723254
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199107"
---
# <span data-ttu-id="aa147-101">Remove-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="aa147-101">Remove-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="aa147-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa147-102">SYNOPSIS</span></span>
<span data-ttu-id="aa147-103">Usuwanie repozytorium z acr.</span><span class="sxs-lookup"><span data-stu-id="aa147-103">Delete repository from ACR.</span></span>

## <span data-ttu-id="aa147-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="aa147-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryRepository -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa147-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="aa147-105">DESCRIPTION</span></span>
<span data-ttu-id="aa147-106">Usuwanie repozytorium z acr.</span><span class="sxs-lookup"><span data-stu-id="aa147-106">Delete repository from ACR.</span></span>

## <span data-ttu-id="aa147-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="aa147-107">EXAMPLES</span></span>

### <span data-ttu-id="aa147-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aa147-108">Example 1</span></span>
```powershell
Remove-AzContainerRegistryRepository -RegistryName registry -Name test/busybox15

ManifestsDeleted                                                          TagsDeleted
----------------                                                          -----------
{sha256:31a54a0cf86d7354788a8265f60ae6acb4b348a67efbcf7c1007dd3cf7af05ab} {latest}
```

<span data-ttu-id="aa147-109">Usuń test repozytorium/skrzynkę zajęty15 w rejestrze.</span><span class="sxs-lookup"><span data-stu-id="aa147-109">Delete repository test/busybox15 under registry.</span></span>

## <span data-ttu-id="aa147-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa147-110">PARAMETERS</span></span>

### <span data-ttu-id="aa147-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa147-111">-DefaultProfile</span></span>
<span data-ttu-id="aa147-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa147-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa147-113">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="aa147-113">-Name</span></span>
<span data-ttu-id="aa147-114">Nazwa repozytorium.</span><span class="sxs-lookup"><span data-stu-id="aa147-114">Repository Name.</span></span>

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

### <span data-ttu-id="aa147-115">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="aa147-115">-RegistryName</span></span>
<span data-ttu-id="aa147-116">Nazwa rejestru kontenerów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="aa147-116">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="aa147-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa147-117">-Confirm</span></span>
<span data-ttu-id="aa147-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="aa147-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa147-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa147-119">-WhatIf</span></span>
<span data-ttu-id="aa147-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa147-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa147-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="aa147-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa147-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa147-122">CommonParameters</span></span>
<span data-ttu-id="aa147-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa147-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa147-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa147-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa147-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa147-125">INPUTS</span></span>

### <span data-ttu-id="aa147-126">System.String</span><span class="sxs-lookup"><span data-stu-id="aa147-126">System.String</span></span>

## <span data-ttu-id="aa147-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="aa147-127">OUTPUTS</span></span>

### <span data-ttu-id="aa147-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span><span class="sxs-lookup"><span data-stu-id="aa147-128">Microsoft.Azure.Commands.ContainerRegistry.Models.PSDeletedRepository</span></span>

## <span data-ttu-id="aa147-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="aa147-129">NOTES</span></span>

## <span data-ttu-id="aa147-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa147-130">RELATED LINKS</span></span>
