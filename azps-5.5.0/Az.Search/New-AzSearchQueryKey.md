---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: 7edca2e338c4972550d44cc6409187dbc53ab40b
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192699"
---
# <span data-ttu-id="1aab3-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="1aab3-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="1aab3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1aab3-102">SYNOPSIS</span></span>
<span data-ttu-id="1aab3-103">Utwórz nowy klucz zapytania dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="1aab3-103">Create a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="1aab3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="1aab3-104">SYNTAX</span></span>

### <span data-ttu-id="1aab3-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="1aab3-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aab3-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1aab3-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1aab3-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1aab3-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1aab3-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="1aab3-108">DESCRIPTION</span></span>
<span data-ttu-id="1aab3-109">Polecenie **cmdlet New-AzSearchQueryKey** tworzy nowy klucz zapytania dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="1aab3-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="1aab3-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="1aab3-110">EXAMPLES</span></span>

### <span data-ttu-id="1aab3-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="1aab3-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="1aab3-112">W tym przykładzie jest tworzyny nowy klucz zapytania dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="1aab3-112">The example creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="1aab3-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1aab3-113">PARAMETERS</span></span>

### <span data-ttu-id="1aab3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1aab3-114">-DefaultProfile</span></span>
<span data-ttu-id="1aab3-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="1aab3-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1aab3-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="1aab3-116">-Name</span></span>
<span data-ttu-id="1aab3-117">Nazwa klucza zapytania usługi Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="1aab3-117">Azure Cognitive Search Service query key name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aab3-118">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="1aab3-118">-ParentObject</span></span>
<span data-ttu-id="1aab3-119">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="1aab3-119">Azure Cognitive Search Service Input Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchService
Parameter Sets: ParentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1aab3-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="1aab3-120">-ParentResourceId</span></span>
<span data-ttu-id="1aab3-121">Identyfikator zasobu usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="1aab3-121">Azure Cognitive Search Service Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1aab3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1aab3-122">-ResourceGroupName</span></span>
<span data-ttu-id="1aab3-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="1aab3-123">Resource Group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aab3-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="1aab3-124">-ServiceName</span></span>
<span data-ttu-id="1aab3-125">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="1aab3-125">Azure Cognitive Search Service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1aab3-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1aab3-126">-Confirm</span></span>
<span data-ttu-id="1aab3-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1aab3-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1aab3-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1aab3-128">-WhatIf</span></span>
<span data-ttu-id="1aab3-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1aab3-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1aab3-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="1aab3-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1aab3-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1aab3-131">CommonParameters</span></span>
<span data-ttu-id="1aab3-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1aab3-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1aab3-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="1aab3-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1aab3-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1aab3-134">INPUTS</span></span>

### <span data-ttu-id="1aab3-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="1aab3-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="1aab3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="1aab3-136">System.String</span></span>

## <span data-ttu-id="1aab3-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1aab3-137">OUTPUTS</span></span>

### <span data-ttu-id="1aab3-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="1aab3-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="1aab3-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="1aab3-139">NOTES</span></span>

## <span data-ttu-id="1aab3-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1aab3-140">RELATED LINKS</span></span>

[<span data-ttu-id="1aab3-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="1aab3-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="1aab3-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="1aab3-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
