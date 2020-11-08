---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/export-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Export-AzBlueprintWithArtifact.md
ms.openlocfilehash: 2136a224a5d187951b77c6f48e0b610b48b021b4
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051344"
---
# <span data-ttu-id="ec059-101">Export-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="ec059-101">Export-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="ec059-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ec059-102">SYNOPSIS</span></span>
<span data-ttu-id="ec059-103">Eksportowanie określonej definicji listy projektów do określonej lokalizacji wyjściowej jako pliku JSON.</span><span class="sxs-lookup"><span data-stu-id="ec059-103">Export specified blueprint definition to the specified output location as a JSON file.</span></span> 

## <span data-ttu-id="ec059-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ec059-104">SYNTAX</span></span>

```
Export-AzBlueprintWithArtifact -Blueprint <PSBlueprintBase> -OutputPath <String> [-Version <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ec059-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ec059-105">DESCRIPTION</span></span>
<span data-ttu-id="ec059-106">Eksportowanie definicji planów wraz z artefaktami i zapisywanie na dysku.</span><span class="sxs-lookup"><span data-stu-id="ec059-106">Export a blueprint definition with its artifacts and save to disk.</span></span> <span data-ttu-id="ec059-107">To polecenie cmdlet eksportuje najnowszą wersję (roboczą lub opublikowaną) projektu.</span><span class="sxs-lookup"><span data-stu-id="ec059-107">This cmdlet exports the latest version(draft or published) of the blueprint.</span></span>

## <span data-ttu-id="ec059-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ec059-108">EXAMPLES</span></span>

### <span data-ttu-id="ec059-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ec059-109">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Export-AzBlueprintWithArtifact -Blueprint $bp -Version 1.0 -OutputPath C:\Blueprints
```

<span data-ttu-id="ec059-110">Eksportowanie definicji planów wraz z artefaktami i zapisywanie na dysku.</span><span class="sxs-lookup"><span data-stu-id="ec059-110">Export a blueprint definition with its artifacts and save to disk.</span></span>

## <span data-ttu-id="ec059-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ec059-111">PARAMETERS</span></span>

### <span data-ttu-id="ec059-112">-Plan</span><span class="sxs-lookup"><span data-stu-id="ec059-112">-Blueprint</span></span>
<span data-ttu-id="ec059-113">Obiekt definicji plany do wyeksportowania.</span><span class="sxs-lookup"><span data-stu-id="ec059-113">The blueprint definition object to export.</span></span>

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

### <span data-ttu-id="ec059-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec059-114">-DefaultProfile</span></span>
<span data-ttu-id="ec059-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ec059-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ec059-116">-Force</span><span class="sxs-lookup"><span data-stu-id="ec059-116">-Force</span></span>
<span data-ttu-id="ec059-117">Gdy jest ustawiona wartość PRAWDA, wykonanie nie poprosi o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="ec059-117">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="ec059-118">-OutputPath</span><span class="sxs-lookup"><span data-stu-id="ec059-118">-OutputPath</span></span>
<span data-ttu-id="ec059-119">Ścieżka do pliku na dysku, na którym ma zostać wyeksportowana definicja programu w formacie JSON.</span><span class="sxs-lookup"><span data-stu-id="ec059-119">Path to a file on disk where to export the Blueprint definition in JSON format.</span></span>

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

### <span data-ttu-id="ec059-120">-Version</span><span class="sxs-lookup"><span data-stu-id="ec059-120">-Version</span></span>
<span data-ttu-id="ec059-121">Opublikowana wersja definicji planów.</span><span class="sxs-lookup"><span data-stu-id="ec059-121">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="ec059-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec059-122">CommonParameters</span></span>
<span data-ttu-id="ec059-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ec059-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="ec059-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec059-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec059-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ec059-125">INPUTS</span></span>

### <span data-ttu-id="ec059-126">Microsoft. Azure. Commands. plan. modele. PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="ec059-126">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="ec059-127">System. String</span><span class="sxs-lookup"><span data-stu-id="ec059-127">System.String</span></span>

## <span data-ttu-id="ec059-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ec059-128">OUTPUTS</span></span>

### <span data-ttu-id="ec059-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ec059-129">System.String</span></span>

## <span data-ttu-id="ec059-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ec059-130">NOTES</span></span>

## <span data-ttu-id="ec059-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ec059-131">RELATED LINKS</span></span>
