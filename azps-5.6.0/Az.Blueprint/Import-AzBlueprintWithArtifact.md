---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: eb0fddc34a83d5a23aeb990c920f36d7a3e03ff2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978874"
---
# <span data-ttu-id="aa009-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="aa009-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="aa009-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa009-102">SYNOPSIS</span></span>
<span data-ttu-id="aa009-103">Zaimportuj plik planu w formacie JSON do obiektu planu i zapisz go w ramach określonej subskrypcji lub grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="aa009-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="aa009-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="aa009-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa009-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="aa009-105">DESCRIPTION</span></span>
<span data-ttu-id="aa009-106">Importowanie definicji planu z jej artefaktami.</span><span class="sxs-lookup"><span data-stu-id="aa009-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="aa009-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="aa009-107">EXAMPLES</span></span>

### <span data-ttu-id="aa009-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="aa009-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="aa009-109">Zaimportuj definicję planu przy użyciu jej artefaktów i zapisz ją w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="aa009-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="aa009-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="aa009-110">PARAMETERS</span></span>

### <span data-ttu-id="aa009-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa009-111">-DefaultProfile</span></span>
<span data-ttu-id="aa009-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="aa009-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa009-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="aa009-113">-Force</span></span>
<span data-ttu-id="aa009-114">Po skonfigurowaniu wartości True (Prawda) wykonanie nie będzie prosić o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="aa009-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="aa009-115">— IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="aa009-115">-IncludeSubFolders</span></span>
<span data-ttu-id="aa009-116">W przypadku ustawienia wartości True (Prawda) artefakt w podfolderach zostanie uwzględniony.</span><span class="sxs-lookup"><span data-stu-id="aa009-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="aa009-117">-InputPath</span><span class="sxs-lookup"><span data-stu-id="aa009-117">-InputPath</span></span>
<span data-ttu-id="aa009-118">Ścieżka do pliku JSON Plan na dysku.</span><span class="sxs-lookup"><span data-stu-id="aa009-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="aa009-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="aa009-119">-ManagementGroupId</span></span>
<span data-ttu-id="aa009-120">Identyfikator grupy zarządzania, w którym jest lub zostanie zapisana definicja planu.</span><span class="sxs-lookup"><span data-stu-id="aa009-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="aa009-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="aa009-121">-Name</span></span>
<span data-ttu-id="aa009-122">Nazwa definicji planu.</span><span class="sxs-lookup"><span data-stu-id="aa009-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="aa009-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aa009-123">-PassThru</span></span>
<span data-ttu-id="aa009-124">Po jego skonfigurowaniu polecenie cmdlet zwróci obiekt reprezentujący zaimportowaną definicję planu.</span><span class="sxs-lookup"><span data-stu-id="aa009-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="aa009-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="aa009-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="aa009-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aa009-126">-SubscriptionId</span></span>
<span data-ttu-id="aa009-127">Identyfikator subskrypcji, w którym jest lub zostanie zapisana definicja planu.</span><span class="sxs-lookup"><span data-stu-id="aa009-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="aa009-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="aa009-128">-Confirm</span></span>
<span data-ttu-id="aa009-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="aa009-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa009-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa009-130">-WhatIf</span></span>
<span data-ttu-id="aa009-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="aa009-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="aa009-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="aa009-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa009-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa009-133">CommonParameters</span></span>
<span data-ttu-id="aa009-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="aa009-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa009-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="aa009-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa009-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa009-136">INPUTS</span></span>

### <span data-ttu-id="aa009-137">System.String</span><span class="sxs-lookup"><span data-stu-id="aa009-137">System.String</span></span>

## <span data-ttu-id="aa009-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="aa009-138">OUTPUTS</span></span>

### <span data-ttu-id="aa009-139">System.String</span><span class="sxs-lookup"><span data-stu-id="aa009-139">System.String</span></span>

## <span data-ttu-id="aa009-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="aa009-140">NOTES</span></span>

## <span data-ttu-id="aa009-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="aa009-141">RELATED LINKS</span></span>
