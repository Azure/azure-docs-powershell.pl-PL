---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/Remove-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Remove-AzContainerRegistryTag.md
ms.openlocfilehash: 7e6528630c731b15f906d79de45bc50f94b2a715
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199098"
---
# <span data-ttu-id="b50e4-101">Remove-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="b50e4-101">Remove-AzContainerRegistryTag</span></span>

## <span data-ttu-id="b50e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b50e4-102">SYNOPSIS</span></span>
<span data-ttu-id="b50e4-103">Otagowanie tagu ACR.</span><span class="sxs-lookup"><span data-stu-id="b50e4-103">Untag ACR tag.</span></span>

## <span data-ttu-id="b50e4-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b50e4-104">SYNTAX</span></span>

```
Remove-AzContainerRegistryTag -RepositoryName <String> -Name <String> -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b50e4-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b50e4-105">DESCRIPTION</span></span>
<span data-ttu-id="b50e4-106">Otagowanie tagu ACR.</span><span class="sxs-lookup"><span data-stu-id="b50e4-106">Untag ACR tag.</span></span>
<span data-ttu-id="b50e4-107">Aby użyć tego polecenia cmdlet, uruchom polecenie `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="b50e4-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -DeleteEnable $true`</span></span>
<span data-ttu-id="b50e4-108">.</span><span class="sxs-lookup"><span data-stu-id="b50e4-108">first.</span></span>

## <span data-ttu-id="b50e4-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b50e4-109">EXAMPLES</span></span>

### <span data-ttu-id="b50e4-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b50e4-110">Example 1</span></span>
```powershell
Remove-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest
True
```

<span data-ttu-id="b50e4-111">Untag alpine:tag under registry.</span><span class="sxs-lookup"><span data-stu-id="b50e4-111">Untag alpine:tag under registry.</span></span>

## <span data-ttu-id="b50e4-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b50e4-112">PARAMETERS</span></span>

### <span data-ttu-id="b50e4-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b50e4-113">-DefaultProfile</span></span>
<span data-ttu-id="b50e4-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b50e4-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b50e4-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b50e4-115">-Name</span></span>
<span data-ttu-id="b50e4-116">Tag.</span><span class="sxs-lookup"><span data-stu-id="b50e4-116">Tag.</span></span>

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

### <span data-ttu-id="b50e4-117">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="b50e4-117">-RegistryName</span></span>
<span data-ttu-id="b50e4-118">Nazwa rejestru kontenerów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="b50e4-118">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="b50e4-119">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="b50e4-119">-RepositoryName</span></span>
<span data-ttu-id="b50e4-120">Nazwa repozytorium.</span><span class="sxs-lookup"><span data-stu-id="b50e4-120">Repository Name.</span></span>

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

### <span data-ttu-id="b50e4-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b50e4-121">-Confirm</span></span>
<span data-ttu-id="b50e4-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b50e4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b50e4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b50e4-123">-WhatIf</span></span>
<span data-ttu-id="b50e4-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b50e4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b50e4-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b50e4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b50e4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b50e4-126">CommonParameters</span></span>
<span data-ttu-id="b50e4-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b50e4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b50e4-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b50e4-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b50e4-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b50e4-129">INPUTS</span></span>

### <span data-ttu-id="b50e4-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b50e4-130">System.String</span></span>

## <span data-ttu-id="b50e4-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b50e4-131">OUTPUTS</span></span>

### <span data-ttu-id="b50e4-132">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="b50e4-132">System.Boolean</span></span>

## <span data-ttu-id="b50e4-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b50e4-133">NOTES</span></span>

## <span data-ttu-id="b50e4-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b50e4-134">RELATED LINKS</span></span>
