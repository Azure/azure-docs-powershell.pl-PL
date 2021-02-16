---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177890"
---
# <span data-ttu-id="1e772-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="1e772-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="1e772-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e772-102">SYNOPSIS</span></span>
<span data-ttu-id="1e772-103">Wyeksportuj określoną definicję planu do określonej lokalizacji wyjściowej jako plik JSON.</span><span class="sxs-lookup"><span data-stu-id="1e772-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="1e772-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1e772-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e772-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="1e772-105">DESCRIPTION</span></span>
<span data-ttu-id="1e772-106">Wyeksportuj definicję planu z jej artefaktami i zapisz ją na dysku.</span><span class="sxs-lookup"><span data-stu-id="1e772-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="1e772-107">To polecenie cmdlet eksportuje najnowszą wersję (wersję roboczą lub opublikowaną) planu.</span><span class="sxs-lookup"><span data-stu-id="1e772-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="1e772-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1e772-108">EXAMPLES</span></span>

### <span data-ttu-id="1e772-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1e772-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="1e772-110">Wyeksportuj definicję planu z jej artefaktami i zapisz ją na dysku.</span><span class="sxs-lookup"><span data-stu-id="1e772-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="1e772-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1e772-111">PARAMETERS</span></span>

### <span data-ttu-id="1e772-112">—Plan</span><span class="sxs-lookup"><span data-stu-id="1e772-112">-Blueprint</span></span>
<span data-ttu-id="1e772-113">Obiekt definicji planu do wyeksportowania.</span><span class="sxs-lookup"><span data-stu-id="1e772-113">The blueprint definition object to export.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1e772-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e772-114">-DefaultProfile</span></span>
<span data-ttu-id="1e772-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1e772-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e772-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="1e772-116">-Force</span></span>
<span data-ttu-id="1e772-117">Po skonfigurowaniu wartości True (Prawda) wykonanie nie będzie prosić o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1e772-117">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e772-118">- OutputPath</span><span class="sxs-lookup"><span data-stu-id="1e772-118">-OutputPath</span></span>
<span data-ttu-id="1e772-119">Ścieżka do pliku na dysku, na którym można wyeksportować definicję Plan w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="1e772-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="1e772-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1e772-120">-PassThru</span></span>
<span data-ttu-id="1e772-121">Po jego skonfigurowaniu polecenie cmdlet zwróci obiekt reprezentujący eksportowaną definicję planu.</span><span class="sxs-lookup"><span data-stu-id="1e772-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="1e772-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="1e772-122">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1e772-123">— Wersja</span><span class="sxs-lookup"><span data-stu-id="1e772-123">-Version</span></span>
<span data-ttu-id="1e772-124">Opublikowano wersję definicji planu.</span><span class="sxs-lookup"><span data-stu-id="1e772-124">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1e772-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1e772-125">-Confirm</span></span>
<span data-ttu-id="1e772-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1e772-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e772-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e772-127">-WhatIf</span></span>
<span data-ttu-id="1e772-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1e772-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e772-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1e772-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e772-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e772-130">CommonParameters</span></span>
<span data-ttu-id="1e772-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1e772-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e772-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1e772-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e772-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1e772-133">INPUTS</span></span>

### <span data-ttu-id="1e772-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="1e772-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="1e772-135">System.String</span><span class="sxs-lookup"><span data-stu-id="1e772-135">System.String</span></span>

## <span data-ttu-id="1e772-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="1e772-136">OUTPUTS</span></span>

### <span data-ttu-id="1e772-137">System.String</span><span class="sxs-lookup"><span data-stu-id="1e772-137">System.String</span></span>

## <span data-ttu-id="1e772-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1e772-138">NOTES</span></span>

## <span data-ttu-id="1e772-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1e772-139">RELATED LINKS</span></span>
