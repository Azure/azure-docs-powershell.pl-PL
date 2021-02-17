---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrytag
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryTag.md
ms.openlocfilehash: 48fb77eb9c718a09a7e13e6d6ab5af5bfc60c912
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100238570"
---
# <span data-ttu-id="44268-101">Update-AzContainerRegistryTag</span><span class="sxs-lookup"><span data-stu-id="44268-101">Update-AzContainerRegistryTag</span></span>

## <span data-ttu-id="44268-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="44268-102">SYNOPSIS</span></span>
<span data-ttu-id="44268-103">Aktualizowanie tagu ACR.</span><span class="sxs-lookup"><span data-stu-id="44268-103">Update ACR tag.</span></span>

## <span data-ttu-id="44268-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="44268-104">SYNTAX</span></span>

```
Update-AzContainerRegistryTag -RepositoryName <String> -Name <String> [-DeleteEnabled <Boolean>]
 [-WriteEnabled <Boolean>] [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="44268-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="44268-105">DESCRIPTION</span></span>
<span data-ttu-id="44268-106">Aktualizowanie tagu ACR.</span><span class="sxs-lookup"><span data-stu-id="44268-106">Update ACR tag.</span></span>
<span data-ttu-id="44268-107">Aby użyć tego polecenia cmdlet, uruchom polecenie `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span><span class="sxs-lookup"><span data-stu-id="44268-107">To use this cmdlet please run `Update-AzContainerRegistryRepository -RegistryName XXX -Repository XXX -WriteEnable $true`</span></span>
<span data-ttu-id="44268-108">.</span><span class="sxs-lookup"><span data-stu-id="44268-108">first.</span></span>

## <span data-ttu-id="44268-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="44268-109">EXAMPLES</span></span>

### <span data-ttu-id="44268-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="44268-110">Example 1</span></span>
```powershell
Update-AzContainerRegistryTag -RegistryName registry -RepositoryName alpine -Name latest -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry                    ImageName Attributes
--------                    --------- ----------
registry.azurecr.io alpine    Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute
```

<span data-ttu-id="44268-111">Zaktualizuj atrybuty tagu do najnowszej wersji w rejestrze.</span><span class="sxs-lookup"><span data-stu-id="44268-111">Update attributes for tag latest under registry.</span></span>

## <span data-ttu-id="44268-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="44268-112">PARAMETERS</span></span>

### <span data-ttu-id="44268-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="44268-113">-DefaultProfile</span></span>
<span data-ttu-id="44268-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="44268-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="44268-115">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="44268-115">-DeleteEnabled</span></span>
<span data-ttu-id="44268-116">Usuń włącz.</span><span class="sxs-lookup"><span data-stu-id="44268-116">Delete enable.</span></span>

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

### <span data-ttu-id="44268-117">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="44268-117">-ListEnabled</span></span>
<span data-ttu-id="44268-118">Włączanie listy.</span><span class="sxs-lookup"><span data-stu-id="44268-118">List enable.</span></span>

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

### <span data-ttu-id="44268-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="44268-119">-Name</span></span>
<span data-ttu-id="44268-120">Tag.</span><span class="sxs-lookup"><span data-stu-id="44268-120">Tag.</span></span>

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

### <span data-ttu-id="44268-121">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="44268-121">-ReadEnabled</span></span>
<span data-ttu-id="44268-122">Włącz czytanie.</span><span class="sxs-lookup"><span data-stu-id="44268-122">Read enable.</span></span>

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

### <span data-ttu-id="44268-123">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="44268-123">-RegistryName</span></span>
<span data-ttu-id="44268-124">Nazwa rejestru kontenerów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="44268-124">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="44268-125">-RepositoryName</span><span class="sxs-lookup"><span data-stu-id="44268-125">-RepositoryName</span></span>
<span data-ttu-id="44268-126">Nazwa repozytorium.</span><span class="sxs-lookup"><span data-stu-id="44268-126">Repository Name.</span></span>

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

### <span data-ttu-id="44268-127">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="44268-127">-WriteEnabled</span></span>
<span data-ttu-id="44268-128">Włącz pisanie.</span><span class="sxs-lookup"><span data-stu-id="44268-128">Write enable.</span></span>

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

### <span data-ttu-id="44268-129">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="44268-129">-Confirm</span></span>
<span data-ttu-id="44268-130">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="44268-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="44268-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="44268-131">-WhatIf</span></span>
<span data-ttu-id="44268-132">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="44268-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="44268-133">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="44268-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="44268-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="44268-134">CommonParameters</span></span>
<span data-ttu-id="44268-135">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="44268-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="44268-136">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="44268-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="44268-137">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="44268-137">INPUTS</span></span>

### <span data-ttu-id="44268-138">System.String</span><span class="sxs-lookup"><span data-stu-id="44268-138">System.String</span></span>

## <span data-ttu-id="44268-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="44268-139">OUTPUTS</span></span>

### <span data-ttu-id="44268-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span><span class="sxs-lookup"><span data-stu-id="44268-140">Microsoft.Azure.Commands.ContainerRegistry.Models.PSTagAttribute</span></span>

## <span data-ttu-id="44268-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="44268-141">NOTES</span></span>

## <span data-ttu-id="44268-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="44268-142">RELATED LINKS</span></span>
