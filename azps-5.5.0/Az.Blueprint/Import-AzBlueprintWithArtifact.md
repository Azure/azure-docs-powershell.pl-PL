---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/import-azblueprintwithartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Import-AzBlueprintWithArtifact.md
ms.openlocfilehash: 43877ecb7fe7e90f0619a26a54eea534ac1390b3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181954"
---
# <span data-ttu-id="59db6-101">Import-AzBlueprintWithArtifact</span><span class="sxs-lookup"><span data-stu-id="59db6-101">Import-AzBlueprintWithArtifact</span></span>

## <span data-ttu-id="59db6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59db6-102">SYNOPSIS</span></span>
<span data-ttu-id="59db6-103">Zaimportuj plik planu w formacie JSON do obiektu planu i zapisz go w ramach określonej subskrypcji lub grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="59db6-103">Import a blueprint file in JSON format to a blueprint object and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="59db6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="59db6-104">SYNTAX</span></span>

```
Import-AzBlueprintWithArtifact -Name <String> [-SubscriptionId <String>] [-ManagementGroupId <String>]
 -InputPath <String> [-IncludeSubFolders] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59db6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="59db6-105">DESCRIPTION</span></span>
<span data-ttu-id="59db6-106">Zaimportuj definicję planu wraz z jej artefaktami.</span><span class="sxs-lookup"><span data-stu-id="59db6-106">Import a blueprint definition with its artifacts.</span></span> 

## <span data-ttu-id="59db6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="59db6-107">EXAMPLES</span></span>

### <span data-ttu-id="59db6-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="59db6-108">Example 1</span></span>
```powershell
PS C:\> Import-AzBlueprintWithArtifact -Name MySimpleBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -InputPath  C:\Blueprints\SimpleBlueprint
```

<span data-ttu-id="59db6-109">Zaimportuj definicję planu przy użyciu jej artefaktów i zapisz ją w ramach subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="59db6-109">Import a blueprint definition with its artifacts and save within a subscription.</span></span>

## <span data-ttu-id="59db6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59db6-110">PARAMETERS</span></span>

### <span data-ttu-id="59db6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59db6-111">-DefaultProfile</span></span>
<span data-ttu-id="59db6-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="59db6-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59db6-113">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="59db6-113">-Force</span></span>
<span data-ttu-id="59db6-114">Po skonfigurowaniu wartości True (Prawda) wykonanie nie będzie prosić o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="59db6-114">When set to true, execution will not ask for a confirmation.</span></span>

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

### <span data-ttu-id="59db6-115">— IncludeSubFolders</span><span class="sxs-lookup"><span data-stu-id="59db6-115">-IncludeSubFolders</span></span>
<span data-ttu-id="59db6-116">W przypadku ustawienia wartości True (Prawda) artefakt w podfolderach zostanie uwzględniony.</span><span class="sxs-lookup"><span data-stu-id="59db6-116">When set to true, artifact in the subfolders will be included.</span></span>

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

### <span data-ttu-id="59db6-117">- InputPath</span><span class="sxs-lookup"><span data-stu-id="59db6-117">-InputPath</span></span>
<span data-ttu-id="59db6-118">Ścieżka do pliku JSON Plan na dysku.</span><span class="sxs-lookup"><span data-stu-id="59db6-118">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="59db6-119">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="59db6-119">-ManagementGroupId</span></span>
<span data-ttu-id="59db6-120">Identyfikator grupy zarządzania, w którym jest lub zostanie zapisana definicja planu.</span><span class="sxs-lookup"><span data-stu-id="59db6-120">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="59db6-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="59db6-121">-Name</span></span>
<span data-ttu-id="59db6-122">Nazwa definicji planu.</span><span class="sxs-lookup"><span data-stu-id="59db6-122">Blueprint definition name.</span></span>

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

### <span data-ttu-id="59db6-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59db6-123">-PassThru</span></span>
<span data-ttu-id="59db6-124">Po jego skonfigurowaniu polecenie cmdlet zwróci obiekt reprezentujący zaimportowaną definicję planu.</span><span class="sxs-lookup"><span data-stu-id="59db6-124">When set, the cmdlet will return an object representing the imported blueprint definition.</span></span> <span data-ttu-id="59db6-125">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="59db6-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="59db6-126">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="59db6-126">-SubscriptionId</span></span>
<span data-ttu-id="59db6-127">Identyfikator subskrypcji, w którym jest lub zostanie zapisana definicja planu.</span><span class="sxs-lookup"><span data-stu-id="59db6-127">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="59db6-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="59db6-128">-Confirm</span></span>
<span data-ttu-id="59db6-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="59db6-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59db6-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59db6-130">-WhatIf</span></span>
<span data-ttu-id="59db6-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="59db6-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="59db6-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="59db6-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59db6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59db6-133">CommonParameters</span></span>
<span data-ttu-id="59db6-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="59db6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59db6-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="59db6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59db6-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59db6-136">INPUTS</span></span>

### <span data-ttu-id="59db6-137">System.String</span><span class="sxs-lookup"><span data-stu-id="59db6-137">System.String</span></span>

## <span data-ttu-id="59db6-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="59db6-138">OUTPUTS</span></span>

### <span data-ttu-id="59db6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="59db6-139">System.String</span></span>

## <span data-ttu-id="59db6-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="59db6-140">NOTES</span></span>

## <span data-ttu-id="59db6-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="59db6-141">RELATED LINKS</span></span>
