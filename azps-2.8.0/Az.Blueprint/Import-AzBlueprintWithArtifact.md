---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 3853cc1785ca0e9f087b1e30870d17d304666df4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706606"
---
# <span data-ttu-id="8cde0-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="8cde0-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="8cde0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8cde0-102">SYNOPSIS</span></span>
<span data-ttu-id="8cde0-103">Zaimportuj plik programu plan w formacie JSON do obiektu typu plan i Zapisz go w obrębie określonej subskrypcji lub grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="8cde0-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="8cde0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8cde0-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8cde0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8cde0-105">DESCRIPTION</span></span>
<span data-ttu-id="8cde0-106">Importowanie definicji planów wraz z artefaktami.</span><span class="sxs-lookup"><span data-stu-id="8cde0-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="8cde0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8cde0-107">EXAMPLES</span></span>

### <span data-ttu-id="8cde0-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8cde0-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="8cde0-109">Importowanie definicji planów wraz z artefaktami i zapisywanie ich w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="8cde0-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="8cde0-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8cde0-110">PARAMETERS</span></span>

### <span data-ttu-id="8cde0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cde0-111">-DefaultProfile</span></span>
<span data-ttu-id="8cde0-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8cde0-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8cde0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="8cde0-113">-Force</span></span>
<span data-ttu-id="8cde0-114">Gdy jest ustawiona wartość PRAWDA, wykonanie nie poprosi o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="8cde0-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="8cde0-115">-InputPath</span><span class="sxs-lookup"><span data-stu-id="8cde0-115">-InputPath</span></span>
<span data-ttu-id="8cde0-116">Ścieżka do pliku JSON programu plan na dysku.</span><span class="sxs-lookup"><span data-stu-id="8cde0-116">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="8cde0-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="8cde0-117">-ManagementGroupId</span></span>
<span data-ttu-id="8cde0-118">Identyfikator grupy zarządzania, w której znajduje się definicja lub zostanie zapisana.</span><span class="sxs-lookup"><span data-stu-id="8cde0-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="8cde0-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8cde0-119">-Name</span></span>
<span data-ttu-id="8cde0-120">Nazwa definicji plany.</span><span class="sxs-lookup"><span data-stu-id="8cde0-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="8cde0-121">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="8cde0-121">-SubscriptionId</span></span>
<span data-ttu-id="8cde0-122">Identyfikator abonamentu, w którym znajduje się definicja lub zostanie zapisana.</span><span class="sxs-lookup"><span data-stu-id="8cde0-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="8cde0-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cde0-123">CommonParameters</span></span>
<span data-ttu-id="8cde0-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8cde0-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="8cde0-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cde0-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cde0-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8cde0-126">INPUTS</span></span>

### <span data-ttu-id="8cde0-127">System. String</span><span class="sxs-lookup"><span data-stu-id="8cde0-127">System.String</span></span>

## <span data-ttu-id="8cde0-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8cde0-128">OUTPUTS</span></span>

### <span data-ttu-id="8cde0-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8cde0-129">System.String</span></span>

## <span data-ttu-id="8cde0-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8cde0-130">NOTES</span></span>

## <span data-ttu-id="8cde0-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8cde0-131">RELATED LINKS</span></span>
