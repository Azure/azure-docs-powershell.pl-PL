---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/powershell/module/az.containerregistry/update-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
ms.openlocfilehash: 68d4eab2088bc1091d812399aade67659d7db31b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956273"
---
# <span data-ttu-id="d8ad9-101">Update-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="d8ad9-101">Update-AzContainerRegistryTag</span></span>

## <span data-ttu-id="d8ad9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8ad9-102">SYNOPSIS</span></span>
<span data-ttu-id="d8ad9-103">Aktualizowanie tagu ACR.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-103">Update ACR tag.</span></span>

## <span data-ttu-id="d8ad9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d8ad9-104">SYNTAX</span></span>

```
Update-AzContainerRegistryTag -RepositoryName <String> -Name <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d8ad9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d8ad9-105">DESCRIPTION</span></span>
<span data-ttu-id="d8ad9-106">Aktualizowanie tagu ACR.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-106">Update ACR tag.</span></span>
<span data-ttu-id="d8ad9-107">Aby użyć tego polecenia cmdlet, uruchom polecenie `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="d8ad9-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="d8ad9-108">.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-108">first.</span></span>

## <span data-ttu-id="d8ad9-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d8ad9-109">EXAMPLES</span></span>

### <span data-ttu-id="d8ad9-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d8ad9-110">Example 1</span></span>
```powershell
Update-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute
```

<span data-ttu-id="d8ad9-111">Zaktualizuj atrybuty tagu do najnowszej wersji w rejestrze.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-111">Update attributes for tag latest under registry.</span></span>

## <span data-ttu-id="d8ad9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8ad9-112">PARAMETERS</span></span>

### <span data-ttu-id="d8ad9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8ad9-113">-DefaultProfile</span></span>
<span data-ttu-id="d8ad9-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8ad9-115">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ad9-115">-DeleteEnabled</span></span>
<span data-ttu-id="d8ad9-116">Usuń włącz.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-116">Delete enable.</span></span>

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

### <span data-ttu-id="d8ad9-117">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ad9-117">-ListEnabled</span></span>
<span data-ttu-id="d8ad9-118">Włączanie listy.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-118">List enable.</span></span>

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

### <span data-ttu-id="d8ad9-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="d8ad9-119">-Name</span></span>
<span data-ttu-id="d8ad9-120">Tag.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-120">Tag.</span></span>

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

### <span data-ttu-id="d8ad9-121">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ad9-121">-ReadEnabled</span></span>
<span data-ttu-id="d8ad9-122">Włącz czytanie.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-122">Read enable.</span></span>

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

### <span data-ttu-id="d8ad9-123">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="d8ad9-123">-RegistryName</span></span>
<span data-ttu-id="d8ad9-124">Nazwa rejestru kontenerów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-124">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="d8ad9-125">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="d8ad9-125">-RepositoryName</span></span>
<span data-ttu-id="d8ad9-126">Nazwa repozytorium.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-126">Repository Name.</span></span>

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

### <span data-ttu-id="d8ad9-127">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="d8ad9-127">-WriteEnabled</span></span>
<span data-ttu-id="d8ad9-128">Włącz pisanie.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-128">Write enable.</span></span>

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

### <span data-ttu-id="d8ad9-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d8ad9-129">-Confirm</span></span>
<span data-ttu-id="d8ad9-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d8ad9-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8ad9-131">-WhatIf</span></span>
<span data-ttu-id="d8ad9-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8ad9-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d8ad9-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8ad9-134">CommonParameters</span></span>
<span data-ttu-id="d8ad9-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8ad9-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8ad9-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8ad9-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8ad9-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8ad9-137">INPUTS</span></span>

### <span data-ttu-id="d8ad9-138">System.String</span><span class="sxs-lookup"><span data-stu-id="d8ad9-138">System.String</span></span>

## <span data-ttu-id="d8ad9-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8ad9-139">OUTPUTS</span></span>

### <span data-ttu-id="d8ad9-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="d8ad9-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

## <span data-ttu-id="d8ad9-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d8ad9-141">NOTES</span></span>

## <span data-ttu-id="d8ad9-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8ad9-142">RELATED LINKS</span></span>
