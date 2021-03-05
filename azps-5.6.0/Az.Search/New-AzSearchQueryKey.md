---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: 3c6335264c0d658b0c068efba30c39b4caca407b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101971754"
---
# <span data-ttu-id="9dcc7-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="9dcc7-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="9dcc7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dcc7-102">SYNOPSIS</span></span>
<span data-ttu-id="9dcc7-103">Utwórz nowy klucz zapytania dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-103">Create a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="9dcc7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9dcc7-104">SYNTAX</span></span>

### <span data-ttu-id="9dcc7-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="9dcc7-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dcc7-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dcc7-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9dcc7-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9dcc7-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9dcc7-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="9dcc7-108">DESCRIPTION</span></span>
<span data-ttu-id="9dcc7-109">Polecenie **cmdlet New-AzSearchQueryKey** tworzy nowy klucz zapytania dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="9dcc7-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9dcc7-110">EXAMPLES</span></span>

### <span data-ttu-id="9dcc7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="9dcc7-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="9dcc7-112">W tym przykładzie jest tworzyny nowy klucz zapytania dla usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-112">The example creates a new query key for the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="9dcc7-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9dcc7-113">PARAMETERS</span></span>

### <span data-ttu-id="9dcc7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dcc7-114">-DefaultProfile</span></span>
<span data-ttu-id="9dcc7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9dcc7-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="9dcc7-116">-Name</span></span>
<span data-ttu-id="9dcc7-117">Nazwa klucza zapytania usługi Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-117">Azure Cognitive Search Service query key name.</span></span>

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

### <span data-ttu-id="9dcc7-118">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="9dcc7-118">-ParentObject</span></span>
<span data-ttu-id="9dcc7-119">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-119">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="9dcc7-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9dcc7-120">-ParentResourceId</span></span>
<span data-ttu-id="9dcc7-121">Identyfikator zasobu usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-121">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="9dcc7-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9dcc7-122">-ResourceGroupName</span></span>
<span data-ttu-id="9dcc7-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-123">Resource Group name.</span></span>

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

### <span data-ttu-id="9dcc7-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9dcc7-124">-ServiceName</span></span>
<span data-ttu-id="9dcc7-125">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-125">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="9dcc7-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9dcc7-126">-Confirm</span></span>
<span data-ttu-id="9dcc7-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9dcc7-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9dcc7-128">-WhatIf</span></span>
<span data-ttu-id="9dcc7-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9dcc7-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9dcc7-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dcc7-131">CommonParameters</span></span>
<span data-ttu-id="9dcc7-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dcc7-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dcc7-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9dcc7-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dcc7-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9dcc7-134">INPUTS</span></span>

### <span data-ttu-id="9dcc7-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="9dcc7-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="9dcc7-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9dcc7-136">System.String</span></span>

## <span data-ttu-id="9dcc7-137">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9dcc7-137">OUTPUTS</span></span>

### <span data-ttu-id="9dcc7-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="9dcc7-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="9dcc7-139">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9dcc7-139">NOTES</span></span>

## <span data-ttu-id="9dcc7-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9dcc7-140">RELATED LINKS</span></span>

[<span data-ttu-id="9dcc7-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="9dcc7-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="9dcc7-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="9dcc7-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
