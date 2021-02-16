---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/publish-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Publish-AzBlueprint.md
ms.openlocfilehash: 32b59902bca68496c3a6c9e1656ac618824b9f38
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100200906"
---
# <span data-ttu-id="c018e-101">Publish-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="c018e-101">Publish-AzBlueprint</span></span>

## <span data-ttu-id="c018e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c018e-102">SYNOPSIS</span></span>
<span data-ttu-id="c018e-103">Publikowanie nowej wersji planu.</span><span class="sxs-lookup"><span data-stu-id="c018e-103">Publish a new version of a blueprint.</span></span>

## <span data-ttu-id="c018e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="c018e-104">SYNTAX</span></span>

```
Publish-AzBlueprint -Version <String> [-ChangeNote <String>] -Blueprint <PSBlueprint>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c018e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="c018e-105">DESCRIPTION</span></span>
<span data-ttu-id="c018e-106">Publikowanie nowej wersji definicji planu.</span><span class="sxs-lookup"><span data-stu-id="c018e-106">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="c018e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="c018e-107">EXAMPLES</span></span>

### <span data-ttu-id="c018e-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="c018e-108">Example 1</span></span>
```powershell
PS C:\> Publish-AzBlueprint -Blueprint $bp -Version 1.0 

Name           : SimpleBlueprint
Id             : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/versions/1.0
SubscriptionId : 00000000-1111-0000-1111-000000000000
Version        : 1.0
Description    : My simple blueprint
TimeCreated    : 2019-05-30
TargetScope    : Subscription
Parameters     : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroups : {storageRG}
```

<span data-ttu-id="c018e-109">Publikowanie nowej wersji definicji planu.</span><span class="sxs-lookup"><span data-stu-id="c018e-109">Publish a new version of a blueprint definition.</span></span>

## <span data-ttu-id="c018e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c018e-110">PARAMETERS</span></span>

### <span data-ttu-id="c018e-111">—Plan</span><span class="sxs-lookup"><span data-stu-id="c018e-111">-Blueprint</span></span>
<span data-ttu-id="c018e-112">Obiekt Plan.</span><span class="sxs-lookup"><span data-stu-id="c018e-112">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c018e-113">-ChangeNote</span><span class="sxs-lookup"><span data-stu-id="c018e-113">-ChangeNote</span></span>
<span data-ttu-id="c018e-114">Uwagi opisujące zawartość tej wersji planu.</span><span class="sxs-lookup"><span data-stu-id="c018e-114">Notes to describe the contents of this blueprint version.</span></span>

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

### <span data-ttu-id="c018e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c018e-115">-DefaultProfile</span></span>
<span data-ttu-id="c018e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="c018e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c018e-117">— Wersja</span><span class="sxs-lookup"><span data-stu-id="c018e-117">-Version</span></span>
<span data-ttu-id="c018e-118">Wersja definicji planu.</span><span class="sxs-lookup"><span data-stu-id="c018e-118">Version for the blueprint definition.</span></span>

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

### <span data-ttu-id="c018e-119">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c018e-119">-Confirm</span></span>
<span data-ttu-id="c018e-120">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="c018e-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c018e-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c018e-121">-WhatIf</span></span>
<span data-ttu-id="c018e-122">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c018e-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c018e-123">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="c018e-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c018e-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c018e-124">CommonParameters</span></span>
<span data-ttu-id="c018e-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c018e-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c018e-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c018e-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c018e-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c018e-127">INPUTS</span></span>

### <span data-ttu-id="c018e-128">System.String</span><span class="sxs-lookup"><span data-stu-id="c018e-128">System.String</span></span>

### <span data-ttu-id="c018e-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span><span class="sxs-lookup"><span data-stu-id="c018e-129">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprint</span></span>

## <span data-ttu-id="c018e-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c018e-130">OUTPUTS</span></span>

### <span data-ttu-id="c018e-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span><span class="sxs-lookup"><span data-stu-id="c018e-131">Microsoft.Azure.Commands.Blueprint.Models.PSPublishedBlueprint</span></span>

## <span data-ttu-id="c018e-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="c018e-132">NOTES</span></span>

## <span data-ttu-id="c018e-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c018e-133">RELATED LINKS</span></span>
