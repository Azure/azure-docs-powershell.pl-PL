---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprint.md
ms.openlocfilehash: 3213d5dbb981d9cc7d7871ce97f9fd78f375a59a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706601"
---
# <span data-ttu-id="bdef2-101">New-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="bdef2-101">New-AzBlueprint</span></span>

## <span data-ttu-id="bdef2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bdef2-102">SYNOPSIS</span></span>
<span data-ttu-id="bdef2-103">Utwórz nową definicję i Zapisz ją w określonej subskrypcji lub grupie zarządzania.</span><span class="sxs-lookup"><span data-stu-id="bdef2-103">Create a new blueprint definition and save it within the specified subscription or management group.</span></span>

## <span data-ttu-id="bdef2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bdef2-104">SYNTAX</span></span>

### <span data-ttu-id="bdef2-105">CreateBlueprintBySubscription (domyślny)</span><span class="sxs-lookup"><span data-stu-id="bdef2-105">CreateBlueprintBySubscription (Default)</span></span>
```
New-AzBlueprint -Name <String> [-SubscriptionId <String>] -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdef2-106">CreateBlueprintByManagementGroup</span><span class="sxs-lookup"><span data-stu-id="bdef2-106">CreateBlueprintByManagementGroup</span></span>
```
New-AzBlueprint -Name <String> -ManagementGroupId <String> -BlueprintFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdef2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="bdef2-107">DESCRIPTION</span></span>
<span data-ttu-id="bdef2-108">Tworzenie nowej definicji planów.</span><span class="sxs-lookup"><span data-stu-id="bdef2-108">Create a new blueprint definition.</span></span> 

## <span data-ttu-id="bdef2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bdef2-109">EXAMPLES</span></span>

### <span data-ttu-id="bdef2-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="bdef2-110">Example 1</span></span>
```powershell
PS C:\> New-AzBlueprint -Name MyNewBlueprint -SubscriptionId 00000000-1111-0000-1111-000000000000 -BlueprintFile C:\Blueprint.json

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

<span data-ttu-id="bdef2-111">Tworzenie nowej definicji planów w ramach określonego abonamentu.</span><span class="sxs-lookup"><span data-stu-id="bdef2-111">Create a new blueprint definition within the specified subscription.</span></span>

## <span data-ttu-id="bdef2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bdef2-112">PARAMETERS</span></span>

### <span data-ttu-id="bdef2-113">-BlueprintFile</span><span class="sxs-lookup"><span data-stu-id="bdef2-113">-BlueprintFile</span></span>
<span data-ttu-id="bdef2-114">Ścieżka do pliku JSON programu plan na dysku.</span><span class="sxs-lookup"><span data-stu-id="bdef2-114">Path to a Blueprint JSON file on disk.</span></span>

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

### <span data-ttu-id="bdef2-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdef2-115">-DefaultProfile</span></span>
<span data-ttu-id="bdef2-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bdef2-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bdef2-117">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="bdef2-117">-ManagementGroupId</span></span>
<span data-ttu-id="bdef2-118">Identyfikator grupy zarządzania, w której znajduje się definicja lub zostanie zapisana.</span><span class="sxs-lookup"><span data-stu-id="bdef2-118">Management Group Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintByManagementGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdef2-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bdef2-119">-Name</span></span>
<span data-ttu-id="bdef2-120">Nazwa definicji plany.</span><span class="sxs-lookup"><span data-stu-id="bdef2-120">Blueprint definition name.</span></span>

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

### <span data-ttu-id="bdef2-121">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="bdef2-121">-SubscriptionId</span></span>
<span data-ttu-id="bdef2-122">Identyfikator abonamentu, w którym znajduje się definicja lub zostanie zapisana.</span><span class="sxs-lookup"><span data-stu-id="bdef2-122">Subscription Id where the blueprint definition is or will be saved.</span></span>

```yaml
Type: String
Parameter Sets: CreateBlueprintBySubscription
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdef2-123">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bdef2-123">-Confirm</span></span>
<span data-ttu-id="bdef2-124">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdef2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdef2-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdef2-125">-WhatIf</span></span>
<span data-ttu-id="bdef2-126">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bdef2-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdef2-127">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bdef2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdef2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdef2-128">CommonParameters</span></span>
<span data-ttu-id="bdef2-129">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdef2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="bdef2-130">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdef2-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdef2-131">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdef2-131">INPUTS</span></span>

### <span data-ttu-id="bdef2-132">System. String</span><span class="sxs-lookup"><span data-stu-id="bdef2-132">System.String</span></span>

## <span data-ttu-id="bdef2-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bdef2-133">OUTPUTS</span></span>

### <span data-ttu-id="bdef2-134">Microsoft. Azure. Commands. plan. modele. PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="bdef2-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="bdef2-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bdef2-135">NOTES</span></span>

## <span data-ttu-id="bdef2-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdef2-136">RELATED LINKS</span></span>