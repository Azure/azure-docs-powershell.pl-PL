---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: cbfd316b459c9cd2e1fc60e4416e50c426a3dc19
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200899"
---
# <span data-ttu-id="176de-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="176de-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="176de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="176de-102">SYNOPSIS</span></span>
<span data-ttu-id="176de-103">Zaktualizuj definicję planu.</span><span class="sxs-lookup"><span data-stu-id="176de-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="176de-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="176de-104">SYNTAX</span></span>

### <span data-ttu-id="176de-105">UpdateBlueprintBySubscription (domyślne)</span><span class="sxs-lookup"><span data-stu-id="176de-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="176de-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="176de-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="176de-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="176de-107">DESCRIPTION</span></span>
<span data-ttu-id="176de-108">Zaktualizuj definicję planu i zapisz ją w ramach określonej subskrypcji lub grupy zarządzania.</span><span class="sxs-lookup"><span data-stu-id="176de-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="176de-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="176de-109">EXAMPLES</span></span>

### <span data-ttu-id="176de-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="176de-110">Example 1</span></span>
```powershell
PS C:\> Set-AzBlueprint -Name MyBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

Name              : SimpleBlueprint
Id                : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint
ManagementGroupId : myManagementGroupId
Versions          : 
Description       : test
TimeCreated       : 2019-05-12
TargetScope       : Subscription
Parameters        : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue}
ResourceGroups    : {AppNetworkRG}
```

<span data-ttu-id="176de-111">Zaktualizuj definicję planu przy użyciu nowych parametrów.</span><span class="sxs-lookup"><span data-stu-id="176de-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="176de-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="176de-112">PARAMETERS</span></span>

### <span data-ttu-id="176de-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="176de-113">-BlueprintFile</span></span>
<span data-ttu-id="176de-114">Ścieżka do pliku JSON Plan na dysku.</span><span class="sxs-lookup"><span data-stu-id="176de-114">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="176de-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="176de-115">-DefaultProfile</span></span>
<span data-ttu-id="176de-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="176de-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="176de-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="176de-117">-ManagementGroupId</span></span>
<span data-ttu-id="176de-118">Identyfikator grupy zarządzania, w którym jest lub zostanie zapisana definicja planu.</span><span class="sxs-lookup"><span data-stu-id="176de-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="176de-119">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="176de-119">-Name</span></span>
<span data-ttu-id="176de-120">Nazwa definicji planu.</span><span class="sxs-lookup"><span data-stu-id="176de-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="176de-121">- SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="176de-121">-SubscriptionId</span></span>
<span data-ttu-id="176de-122">Identyfikator subskrypcji, w którym jest lub zostanie zapisana definicja planu.</span><span class="sxs-lookup"><span data-stu-id="176de-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="176de-123">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="176de-123">-Confirm</span></span>
<span data-ttu-id="176de-124">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="176de-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="176de-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="176de-125">-WhatIf</span></span>
<span data-ttu-id="176de-126">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="176de-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="176de-127">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="176de-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="176de-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="176de-128">CommonParameters</span></span>
<span data-ttu-id="176de-129">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="176de-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="176de-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="176de-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="176de-131">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="176de-131">INPUTS</span></span>

### <span data-ttu-id="176de-132">System.String</span><span class="sxs-lookup"><span data-stu-id="176de-132">System.String</span></span>

## <span data-ttu-id="176de-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="176de-133">OUTPUTS</span></span>

### <span data-ttu-id="176de-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="176de-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="176de-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="176de-135">NOTES</span></span>

## <span data-ttu-id="176de-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="176de-136">RELATED LINKS</span></span>
