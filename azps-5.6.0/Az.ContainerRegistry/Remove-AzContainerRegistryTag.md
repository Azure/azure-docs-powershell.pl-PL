---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/Remove-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
ms.openlocfilehash: 6fbc5b33bb8e9c865b5ea869deed5044ee08198f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956417"
---
# <span data-ttu-id="8a5a1-101">Remove-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="8a5a1-101">Remove-AzContainerRegistryTag</span></span>

## <span data-ttu-id="8a5a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a5a1-102">SYNOPSIS</span></span>
<span data-ttu-id="8a5a1-103">Otagowanie tagu ACR.</span><span class="sxs-lookup"><span data-stu-id="8a5a1-103">Untag ACR tag.</span></span>

## <span data-ttu-id="8a5a1-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="8a5a1-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8a5a1-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="8a5a1-105">DESCRIPTION</span></span>
<span data-ttu-id="8a5a1-106">Otagowanie tagu ACR.</span><span class="sxs-lookup"><span data-stu-id="8a5a1-106">Untag ACR tag.</span></span>
<span data-ttu-id="8a5a1-107">Aby użyć tego polecenia cmdlet, uruchom polecenie `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="8a5a1-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="8a5a1-108">.</span><span class="sxs-lookup"><span data-stu-id="8a5a1-108">first.</span></span>

## <span data-ttu-id="8a5a1-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="8a5a1-109">EXAMPLES</span></span>

### <span data-ttu-id="8a5a1-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8a5a1-110">Example 1</span></span>
```powershell
Remove-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest
True
```

<span data-ttu-id="8a5a1-111">Untag alpine:tag under registry.</span><span class="sxs-lookup"><span data-stu-id="8a5a1-111">Untag alpine:tag under registry.</span></span>

## <span data-ttu-id="8a5a1-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8a5a1-112">PARAMETERS</span></span>

### <span data-ttu-id="8a5a1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a5a1-113">-DefaultProfile</span></span>
<span data-ttu-id="8a5a1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="8a5a1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a5a1-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="8a5a1-115">-Name</span></span>
<span data-ttu-id="8a5a1-116">Tag.</span><span class="sxs-lookup"><span data-stu-id="8a5a1-116">Tag.</span></span>

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

### <span data-ttu-id="8a5a1-117">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="8a5a1-117">-RegistryName</span></span>
<span data-ttu-id="8a5a1-118">Nazwa rejestru kontenerów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="8a5a1-118">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="8a5a1-119">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="8a5a1-119">-RepositoryName</span></span>
<span data-ttu-id="8a5a1-120">Nazwa repozytorium.</span><span class="sxs-lookup"><span data-stu-id="8a5a1-120">Repository Name.</span></span>

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

### <span data-ttu-id="8a5a1-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8a5a1-121">-Confirm</span></span>
<span data-ttu-id="8a5a1-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8a5a1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8a5a1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8a5a1-123">-WhatIf</span></span>
<span data-ttu-id="8a5a1-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8a5a1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8a5a1-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="8a5a1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8a5a1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a5a1-126">CommonParameters</span></span>
<span data-ttu-id="8a5a1-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8a5a1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a5a1-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8a5a1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a5a1-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a5a1-129">INPUTS</span></span>

### <span data-ttu-id="8a5a1-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8a5a1-130">System.String</span></span>

## <span data-ttu-id="8a5a1-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8a5a1-131">OUTPUTS</span></span>

### <span data-ttu-id="8a5a1-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="8a5a1-132">System.Boolean</span></span>

## <span data-ttu-id="8a5a1-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="8a5a1-133">NOTES</span></span>

## <span data-ttu-id="8a5a1-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8a5a1-134">RELATED LINKS</span></span>
