---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 647d626a0b4d59f219020d66c3c1ec8a5218355b
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363862"
---
# <span data-ttu-id="5e859-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="5e859-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="5e859-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5e859-102">SYNOPSIS</span></span>
<span data-ttu-id="5e859-103">Eksportowanie określonej definicji listy projektów do określonej lokalizacji wyjściowej jako pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="5e859-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="5e859-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5e859-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e859-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5e859-105">DESCRIPTION</span></span>
<span data-ttu-id="5e859-106">Eksportowanie definicji planów wraz z artefaktami i zapisywanie na dysku.</span><span class="sxs-lookup"><span data-stu-id="5e859-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="5e859-107">To polecenie cmdlet eksportuje najnowszą wersję (roboczą lub opublikowaną) projektu.</span><span class="sxs-lookup"><span data-stu-id="5e859-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="5e859-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5e859-108">EXAMPLES</span></span>

### <span data-ttu-id="5e859-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5e859-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="5e859-110">Eksportowanie definicji planów wraz z artefaktami i zapisywanie na dysku.</span><span class="sxs-lookup"><span data-stu-id="5e859-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="5e859-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5e859-111">PARAMETERS</span></span>

### <span data-ttu-id="5e859-112">-Plan</span><span class="sxs-lookup"><span data-stu-id="5e859-112">-Blueprint</span></span>
<span data-ttu-id="5e859-113">Obiekt definicji plany do wyeksportowania.</span><span class="sxs-lookup"><span data-stu-id="5e859-113">The blueprint definition object to export.</span></span>

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

### <span data-ttu-id="5e859-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e859-114">-DefaultProfile</span></span>
<span data-ttu-id="5e859-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5e859-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e859-116">-Force</span><span class="sxs-lookup"><span data-stu-id="5e859-116">-Force</span></span>
<span data-ttu-id="5e859-117">Gdy jest ustawiona wartość PRAWDA, wykonanie nie poprosi o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5e859-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="5e859-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="5e859-118">-OutputPath</span></span>
<span data-ttu-id="5e859-119">Ścieżka do pliku na dysku, na którym ma zostać wyeksportowana definicja programu w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="5e859-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="5e859-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e859-120">-PassThru</span></span>
<span data-ttu-id="5e859-121">Po ustawieniu polecenie cmdlet zwróci obiekt reprezentujący definicję eksportowanego elementu.</span><span class="sxs-lookup"><span data-stu-id="5e859-121">When set, the cmdlet will return an object representing the exported blueprint definition.</span></span> <span data-ttu-id="5e859-122">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="5e859-122">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="5e859-123">-Version</span><span class="sxs-lookup"><span data-stu-id="5e859-123">-Version</span></span>
<span data-ttu-id="5e859-124">Opublikowana wersja definicji planów.</span><span class="sxs-lookup"><span data-stu-id="5e859-124">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="5e859-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5e859-125">-Confirm</span></span>
<span data-ttu-id="5e859-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e859-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e859-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e859-127">-WhatIf</span></span>
<span data-ttu-id="5e859-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5e859-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5e859-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5e859-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e859-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e859-130">CommonParameters</span></span>
<span data-ttu-id="5e859-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e859-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e859-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5e859-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e859-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5e859-133">INPUTS</span></span>

### <span data-ttu-id="5e859-134">Microsoft. Azure. Commands. plan. modele. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="5e859-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="5e859-135">System. String</span><span class="sxs-lookup"><span data-stu-id="5e859-135">System.String</span></span>

## <span data-ttu-id="5e859-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5e859-136">OUTPUTS</span></span>

### <span data-ttu-id="5e859-137">System. String</span><span class="sxs-lookup"><span data-stu-id="5e859-137">System.String</span></span>

## <span data-ttu-id="5e859-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5e859-138">NOTES</span></span>

## <span data-ttu-id="5e859-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5e859-139">RELATED LINKS</span></span>
