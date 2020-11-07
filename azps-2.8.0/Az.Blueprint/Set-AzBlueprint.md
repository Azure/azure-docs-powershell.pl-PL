---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprint.md
ms.openlocfilehash: 7366e263f6106d2d332daab95f029d07c824aa90
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706598"
---
# <span data-ttu-id="b6a1f-101">Set-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="b6a1f-101">Set-AzBlueprint</span></span>

## <span data-ttu-id="b6a1f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b6a1f-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a1f-103">Aktualizowanie definicji planów.</span><span class="sxs-lookup"><span data-stu-id="b6a1f-103">Update a blueprint definition.</span></span>

## <span data-ttu-id="b6a1f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b6a1f-104">SYNTAX</span></span>

### <span data-ttu-id="b6a1f-105">UpdateBlueprintBySubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="b6a1f-105">UpdateBlueprintBySubscription (Default)</span></span>
```
Set-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b6a1f-106">UpdateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="b6a1f-106">UpdateBlueprintByManagementGroup</span></span>
```
Set-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b6a1f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="b6a1f-107">DESCRIPTION</span></span>
<span data-ttu-id="b6a1f-108">Zaktualizuj definicję i Zapisz ją w określonej subskrypcji lub grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="b6a1f-108">Update a blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="b6a1f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b6a1f-109">EXAMPLES</span></span>

### <span data-ttu-id="b6a1f-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b6a1f-110">Example 1</span></span>
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

<span data-ttu-id="b6a1f-111">Aktualizowanie definicji planów przy użyciu nowych parametrów.</span><span class="sxs-lookup"><span data-stu-id="b6a1f-111">Update a blueprint definition with new parameters.</span></span>

## <span data-ttu-id="b6a1f-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b6a1f-112">PARAMETERS</span></span>

### <span data-ttu-id="b6a1f-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="b6a1f-113">-BlueprintFile</span></span>
<span data-ttu-id="b6a1f-114">Ścieżka do pliku JSON programu plan na dysku.</span><span class="sxs-lookup"><span data-stu-id="b6a1f-114">Path to a Blueprint JSON file on disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a1f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a1f-115">-DefaultProfile</span></span>
<span data-ttu-id="b6a1f-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b6a1f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6a1f-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="b6a1f-117">-ManagementGroupId</span></span>
<span data-ttu-id="b6a1f-118">Identyfikator grupy zarządzania, w której znajduje się definicja lub zostanie zapisana.</span><span class="sxs-lookup"><span data-stu-id="b6a1f-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintByManagementGroup, ManagementGroupScope, ByManagementGroupAndName, ByManagementGroupNameAndVersion, ByManagementGroupNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ImportBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a1f-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b6a1f-119">-Name</span></span>
<span data-ttu-id="b6a1f-120">Nazwa definicji plany.</span><span class="sxs-lookup"><span data-stu-id="b6a1f-120">Blueprint definition name.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, CreateBlueprintByManagementGroup, ImportBlueprint
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a1f-121">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="b6a1f-121">-SubscriptionId</span></span>
<span data-ttu-id="b6a1f-122">Identyfikator abonamentu, w którym znajduje się definicja lub zostanie zapisana.</span><span class="sxs-lookup"><span data-stu-id="b6a1f-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription, ImportBlueprint, SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndVersion, BySubscriptionNameAndLatestPublished
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6a1f-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b6a1f-123">-Confirm</span></span>
<span data-ttu-id="b6a1f-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6a1f-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a1f-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b6a1f-125">-WhatIf</span></span>
<span data-ttu-id="b6a1f-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b6a1f-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b6a1f-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b6a1f-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6a1f-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a1f-128">CommonParameters</span></span>
<span data-ttu-id="b6a1f-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b6a1f-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="b6a1f-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6a1f-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a1f-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b6a1f-131">INPUTS</span></span>

### <span data-ttu-id="b6a1f-132">System. String</span><span class="sxs-lookup"><span data-stu-id="b6a1f-132">System.String</span></span>

## <span data-ttu-id="b6a1f-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b6a1f-133">OUTPUTS</span></span>

### <span data-ttu-id="b6a1f-134">Microsoft. Azure. Commands. plan. modele. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="b6a1f-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="b6a1f-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b6a1f-135">NOTES</span></span>

## <span data-ttu-id="b6a1f-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b6a1f-136">RELATED LINKS</span></span>
