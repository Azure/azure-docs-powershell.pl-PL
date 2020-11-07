---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 2c349d99e8a3529d4f1423a43bd31ab2500664c1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706618"
---
# <span data-ttu-id="2b91f-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="2b91f-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="2b91f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2b91f-102">SYNOPSIS</span></span>
<span data-ttu-id="2b91f-103">Eksportowanie określonej definicji listy projektów do określonej lokalizacji wyjściowej jako pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="2b91f-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="2b91f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2b91f-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2b91f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2b91f-105">DESCRIPTION</span></span>
<span data-ttu-id="2b91f-106">Eksportowanie definicji planów wraz z artefaktami i zapisywanie na dysku.</span><span class="sxs-lookup"><span data-stu-id="2b91f-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="2b91f-107">To polecenie cmdlet eksportuje najnowszą wersję (roboczą lub opublikowaną) projektu.</span><span class="sxs-lookup"><span data-stu-id="2b91f-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="2b91f-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2b91f-108">EXAMPLES</span></span>

### <span data-ttu-id="2b91f-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2b91f-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="2b91f-110">Eksportowanie definicji planów wraz z artefaktami i zapisywanie na dysku.</span><span class="sxs-lookup"><span data-stu-id="2b91f-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="2b91f-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2b91f-111">PARAMETERS</span></span>

### <span data-ttu-id="2b91f-112">-Plan</span><span class="sxs-lookup"><span data-stu-id="2b91f-112">-Blueprint</span></span>
<span data-ttu-id="2b91f-113">Obiekt definicji plany do wyeksportowania.</span><span class="sxs-lookup"><span data-stu-id="2b91f-113">The blueprint definition object to export.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2b91f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b91f-114">-DefaultProfile</span></span>
<span data-ttu-id="2b91f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2b91f-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b91f-116">-Force</span><span class="sxs-lookup"><span data-stu-id="2b91f-116">-Force</span></span>
<span data-ttu-id="2b91f-117">Gdy jest ustawiona wartość PRAWDA, wykonanie nie poprosi o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2b91f-117">When set to true, execution will not ask for a confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2b91f-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="2b91f-118">-OutputPath</span></span>
<span data-ttu-id="2b91f-119">Ścieżka do pliku na dysku, na którym ma zostać wyeksportowana definicja programu w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="2b91f-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b91f-120">-Version</span><span class="sxs-lookup"><span data-stu-id="2b91f-120">-Version</span></span>
<span data-ttu-id="2b91f-121">Opublikowana wersja definicji planów.</span><span class="sxs-lookup"><span data-stu-id="2b91f-121">Published blueprint definition version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2b91f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b91f-122">CommonParameters</span></span>
<span data-ttu-id="2b91f-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2b91f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="2b91f-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2b91f-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b91f-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2b91f-125">INPUTS</span></span>

### <span data-ttu-id="2b91f-126">Microsoft. Azure. Commands. plan. modele. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="2b91f-126">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="2b91f-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2b91f-127">System.String</span></span>

## <span data-ttu-id="2b91f-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2b91f-128">OUTPUTS</span></span>

### <span data-ttu-id="2b91f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="2b91f-129">System.String</span></span>

## <span data-ttu-id="2b91f-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2b91f-130">NOTES</span></span>

## <span data-ttu-id="2b91f-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2b91f-131">RELATED LINKS</span></span>
