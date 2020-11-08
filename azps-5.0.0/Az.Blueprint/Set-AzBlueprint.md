---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: cbfd316b459c9cd2e1fc60e4416e50c426a3dc19
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225062"
---
# <span data-ttu-id="79270-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="79270-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="79270-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79270-102">SYNOPSIS</span></span>
<span data-ttu-id="79270-103">Aktualizowanie definicji planów.</span><span class="sxs-lookup"><span data-stu-id="79270-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="79270-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79270-104">SYNTAX</span></span>

### <span data-ttu-id="79270-105">UpdateBlueprintBySubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="79270-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79270-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="79270-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79270-107">Opis</span><span class="sxs-lookup"><span data-stu-id="79270-107">DESCRIPTION</span></span>
<span data-ttu-id="79270-108">Zaktualizuj definicję i Zapisz ją w określonej subskrypcji lub grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="79270-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="79270-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79270-109">EXAMPLES</span></span>

### <span data-ttu-id="79270-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="79270-110">Example 1</span></span>
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

<span data-ttu-id="79270-111">Aktualizowanie definicji planów przy użyciu nowych parametrów.</span><span class="sxs-lookup"><span data-stu-id="79270-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="79270-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79270-112">PARAMETERS</span></span>

### <span data-ttu-id="79270-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="79270-113">-BlueprintFile</span></span>
<span data-ttu-id="79270-114">Ścieżka do pliku JSON programu plan na dysku.</span><span class="sxs-lookup"><span data-stu-id="79270-114">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="79270-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79270-115">-DefaultProfile</span></span>
<span data-ttu-id="79270-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="79270-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79270-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="79270-117">-ManagementGroupId</span></span>
<span data-ttu-id="79270-118">Identyfikator grupy zarządzania, w której znajduje się definicja lub zostanie zapisana.</span><span class="sxs-lookup"><span data-stu-id="79270-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="79270-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="79270-119">-Name</span></span>
<span data-ttu-id="79270-120">Nazwa definicji plany.</span><span class="sxs-lookup"><span data-stu-id="79270-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="79270-121">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="79270-121">-SubscriptionId</span></span>
<span data-ttu-id="79270-122">Identyfikator abonamentu, w którym znajduje się definicja lub zostanie zapisana.</span><span class="sxs-lookup"><span data-stu-id="79270-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

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

### <span data-ttu-id="79270-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79270-123">-Confirm</span></span>
<span data-ttu-id="79270-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79270-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79270-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79270-125">-WhatIf</span></span>
<span data-ttu-id="79270-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79270-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79270-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79270-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79270-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79270-128">CommonParameters</span></span>
<span data-ttu-id="79270-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79270-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79270-130">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="79270-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79270-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79270-131">INPUTS</span></span>

### <span data-ttu-id="79270-132">System. String</span><span class="sxs-lookup"><span data-stu-id="79270-132">System.String</span></span>

## <span data-ttu-id="79270-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79270-133">OUTPUTS</span></span>

### <span data-ttu-id="79270-134">Microsoft. Azure. Commands. plan. modele. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="79270-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="79270-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79270-135">NOTES</span></span>

## <span data-ttu-id="79270-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79270-136">RELATED LINKS</span></span>
