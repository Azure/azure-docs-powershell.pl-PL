---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistryrepository
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryRepository.md
ms.openlocfilehash: ce6f235669ebe4a32958229422f4612f3b8cb340
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196883"
---
# <span data-ttu-id="52306-101">Update-AzContainerRegistryRepository</span><span class="sxs-lookup"><span data-stu-id="52306-101">Update-AzContainerRegistryRepository</span></span>

## <span data-ttu-id="52306-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52306-102">SYNOPSIS</span></span>
<span data-ttu-id="52306-103">Aktualizowanie repozytorium ACR.</span><span class="sxs-lookup"><span data-stu-id="52306-103">Update ACR repository.</span></span>

## <span data-ttu-id="52306-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="52306-104">SYNTAX</span></span>

```
Update-AzContainerRegistryRepository -Name <String> [-DeleteEnabled <Boolean>] [-WriteEnabled <Boolean>]
 [-ListEnabled <Boolean>] [-ReadEnabled <Boolean>] -RegistryName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52306-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="52306-105">DESCRIPTION</span></span>
<span data-ttu-id="52306-106">Aktualizowanie repozytorium ACR.</span><span class="sxs-lookup"><span data-stu-id="52306-106">Update ACR repository.</span></span>

## <span data-ttu-id="52306-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="52306-107">EXAMPLES</span></span>

### <span data-ttu-id="52306-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="52306-108">Example 1</span></span>
```powershell
Update-AzContainerRegistryRepository -RegistryName registry -Name test/busybox8 -DeleteEnabled $false -WriteEnabled $true -ListEnabled $true -ReadEnabled $true

Registry             : registry.azurecr.io
ImageName            : test/busybox8
CreatedTime          : 2020-12-11T08:57:56.2070002Z
LastUpdateTime       : 2020-12-11T08:57:56.5188237Z
ManifestCount        : 1
TagCount             : 1
ChangeableAttributes : Microsoft.Azure.Commands.ContainerRegistry.Models.PSChangeableAttribute
```

<span data-ttu-id="52306-109">Aktualizowanie atrybutów repozytorium w obszarze rejestru.</span><span class="sxs-lookup"><span data-stu-id="52306-109">Update attributes for repository alpine under registry.</span></span>

## <span data-ttu-id="52306-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52306-110">PARAMETERS</span></span>

### <span data-ttu-id="52306-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52306-111">-DefaultProfile</span></span>
<span data-ttu-id="52306-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="52306-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="52306-113">-DeleteEnabled</span><span class="sxs-lookup"><span data-stu-id="52306-113">-DeleteEnabled</span></span>
<span data-ttu-id="52306-114">Usuń włącz.</span><span class="sxs-lookup"><span data-stu-id="52306-114">Delete enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52306-115">-ListEnabled</span><span class="sxs-lookup"><span data-stu-id="52306-115">-ListEnabled</span></span>
<span data-ttu-id="52306-116">Włączanie listy.</span><span class="sxs-lookup"><span data-stu-id="52306-116">List enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52306-117">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="52306-117">-Name</span></span>
<span data-ttu-id="52306-118">Nazwa repozytorium.</span><span class="sxs-lookup"><span data-stu-id="52306-118">Repository Name.</span></span>

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

### <span data-ttu-id="52306-119">-ReadEnabled</span><span class="sxs-lookup"><span data-stu-id="52306-119">-ReadEnabled</span></span>
<span data-ttu-id="52306-120">Włącz czytanie.</span><span class="sxs-lookup"><span data-stu-id="52306-120">Read enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52306-121">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="52306-121">-RegistryName</span></span>
<span data-ttu-id="52306-122">Nazwa rejestru kontenera platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="52306-122">Azure Container Registry Name.</span></span>

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

### <span data-ttu-id="52306-123">-WriteEnabled</span><span class="sxs-lookup"><span data-stu-id="52306-123">-WriteEnabled</span></span>
<span data-ttu-id="52306-124">Włącz pisanie.</span><span class="sxs-lookup"><span data-stu-id="52306-124">Write enable.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="52306-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="52306-125">-Confirm</span></span>
<span data-ttu-id="52306-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="52306-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52306-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52306-127">-WhatIf</span></span>
<span data-ttu-id="52306-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52306-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="52306-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="52306-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52306-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52306-130">CommonParameters</span></span>
<span data-ttu-id="52306-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52306-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52306-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52306-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52306-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52306-133">INPUTS</span></span>

### <span data-ttu-id="52306-134">System.String</span><span class="sxs-lookup"><span data-stu-id="52306-134">System.String</span></span>

## <span data-ttu-id="52306-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52306-135">OUTPUTS</span></span>

### <span data-ttu-id="52306-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span><span class="sxs-lookup"><span data-stu-id="52306-136">Microsoft.Azure.Commands.ContainerRegistry.Models.PSRepositoryAttribute</span></span>

## <span data-ttu-id="52306-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="52306-137">NOTES</span></span>

## <span data-ttu-id="52306-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52306-138">RELATED LINKS</span></span>
