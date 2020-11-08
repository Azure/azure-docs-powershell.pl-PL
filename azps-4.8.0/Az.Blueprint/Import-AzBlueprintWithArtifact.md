---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 43877ecb7fe7e90f0619a26a54eea534ac1390b3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062942"
---
# <span data-ttu-id="7a5f1-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="7a5f1-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="7a5f1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7a5f1-102">SYNOPSIS</span></span>
<span data-ttu-id="7a5f1-103">Zaimportuj plik programu plan w formacie JSON do obiektu typu plan i Zapisz go w obrębie określonej subskrypcji lub grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="7a5f1-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="7a5f1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7a5f1-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7a5f1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7a5f1-105">DESCRIPTION</span></span>
<span data-ttu-id="7a5f1-106">Importowanie definicji planów wraz z artefaktami.</span><span class="sxs-lookup"><span data-stu-id="7a5f1-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="7a5f1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7a5f1-107">EXAMPLES</span></span>

### <span data-ttu-id="7a5f1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7a5f1-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="7a5f1-109">Importowanie definicji planów wraz z artefaktami i zapisywanie ich w ramach abonamentu.</span><span class="sxs-lookup"><span data-stu-id="7a5f1-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="7a5f1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7a5f1-110">PARAMETERS</span></span>

### <span data-ttu-id="7a5f1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a5f1-111">-DefaultProfile</span></span>
<span data-ttu-id="7a5f1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7a5f1-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7a5f1-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7a5f1-113">-Force</span></span>
<span data-ttu-id="7a5f1-114">Gdy jest ustawiona wartość PRAWDA, wykonanie nie poprosi o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="7a5f1-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="7a5f1-115">-IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="7a5f1-115">-IncludeSubFolders</span></span>
<span data-ttu-id="7a5f1-116">Po ustawieniu wartości true artefakt w podfolderach zostanie dołączony.</span><span class="sxs-lookup"><span data-stu-id="7a5f1-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="7a5f1-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="7a5f1-117">-InputPath</span></span>
<span data-ttu-id="7a5f1-118">Ścieżka do pliku JSON programu plan na dysku.</span><span class="sxs-lookup"><span data-stu-id="7a5f1-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="7a5f1-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="7a5f1-119">-ManagementGroupId</span></span>
<span data-ttu-id="7a5f1-120">Identyfikator grupy zarządzania, w której znajduje się definicja lub zostanie zapisana.</span><span class="sxs-lookup"><span data-stu-id="7a5f1-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="7a5f1-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7a5f1-121">-Name</span></span>
<span data-ttu-id="7a5f1-122">Nazwa definicji plany.</span><span class="sxs-lookup"><span data-stu-id="7a5f1-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="7a5f1-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7a5f1-123">-PassThru</span></span>
<span data-ttu-id="7a5f1-124">Po ustawieniu polecenie cmdlet zwróci obiekt reprezentujący zaimportowaną definicję.</span><span class="sxs-lookup"><span data-stu-id="7a5f1-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="7a5f1-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="7a5f1-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7a5f1-126">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="7a5f1-126">-SubscriptionId</span></span>
<span data-ttu-id="7a5f1-127">Identyfikator abonamentu, w którym znajduje się definicja lub zostanie zapisana.</span><span class="sxs-lookup"><span data-stu-id="7a5f1-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="7a5f1-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7a5f1-128">-Confirm</span></span>
<span data-ttu-id="7a5f1-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a5f1-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7a5f1-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7a5f1-130">-WhatIf</span></span>
<span data-ttu-id="7a5f1-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7a5f1-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7a5f1-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7a5f1-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7a5f1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a5f1-133">CommonParameters</span></span>
<span data-ttu-id="7a5f1-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7a5f1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a5f1-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7a5f1-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a5f1-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7a5f1-136">INPUTS</span></span>

### <span data-ttu-id="7a5f1-137">System. String</span><span class="sxs-lookup"><span data-stu-id="7a5f1-137">System.String</span></span>

## <span data-ttu-id="7a5f1-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7a5f1-138">OUTPUTS</span></span>

### <span data-ttu-id="7a5f1-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7a5f1-139">System.String</span></span>

## <span data-ttu-id="7a5f1-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7a5f1-140">NOTES</span></span>

## <span data-ttu-id="7a5f1-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7a5f1-141">RELATED LINKS</span></span>
