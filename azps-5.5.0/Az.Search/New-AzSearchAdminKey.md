---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
ms.openlocfilehash: 28eabb6ccc583a1f3f141c9f02239eca84b04e81
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192706"
---
# <span data-ttu-id="6191b-101">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="6191b-101">New-AzSearchAdminKey</span></span>

## <span data-ttu-id="6191b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6191b-102">SYNOPSIS</span></span>
<span data-ttu-id="6191b-103">Ponownie generuje klucz administratora usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="6191b-103">Regenerates an admin key of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="6191b-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6191b-104">SYNTAX</span></span>

### <span data-ttu-id="6191b-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6191b-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6191b-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6191b-106">ParentObjectParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6191b-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6191b-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6191b-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6191b-108">DESCRIPTION</span></span>
<span data-ttu-id="6191b-109">Polecenie **cmdlet New-AzSearchAdminKey** ponownie generuje klucz administratora usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="6191b-109">The **New-AzSearchAdminKey** cmdlet regenerates an admin key of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="6191b-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6191b-110">EXAMPLES</span></span>

### <span data-ttu-id="6191b-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6191b-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="6191b-112">Przykład ponownie generuje klucz podstawowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="6191b-112">The example regenerates Primary key of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="6191b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6191b-113">PARAMETERS</span></span>

### <span data-ttu-id="6191b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6191b-114">-DefaultProfile</span></span>
<span data-ttu-id="6191b-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6191b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6191b-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="6191b-116">-Force</span></span>
<span data-ttu-id="6191b-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6191b-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6191b-118">-KeyKind</span><span class="sxs-lookup"><span data-stu-id="6191b-118">-KeyKind</span></span>
<span data-ttu-id="6191b-119">Typ klucza administratora usługi Azure Cognitive Search Service (podstawowy/pomocniczy).</span><span class="sxs-lookup"><span data-stu-id="6191b-119">Azure Cognitive Search Service admin key kind (Primary/Secondary).</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKeyKind
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6191b-120">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="6191b-120">-ParentObject</span></span>
<span data-ttu-id="6191b-121">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="6191b-121">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="6191b-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6191b-122">-ParentResourceId</span></span>
<span data-ttu-id="6191b-123">Identyfikator zasobu usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="6191b-123">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="6191b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6191b-124">-ResourceGroupName</span></span>
<span data-ttu-id="6191b-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6191b-125">Resource Group name.</span></span>

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

### <span data-ttu-id="6191b-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6191b-126">-ServiceName</span></span>
<span data-ttu-id="6191b-127">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="6191b-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="6191b-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6191b-128">-Confirm</span></span>
<span data-ttu-id="6191b-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6191b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6191b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6191b-130">-WhatIf</span></span>
<span data-ttu-id="6191b-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6191b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6191b-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6191b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6191b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6191b-133">CommonParameters</span></span>
<span data-ttu-id="6191b-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6191b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6191b-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6191b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6191b-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6191b-136">INPUTS</span></span>

### <span data-ttu-id="6191b-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="6191b-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="6191b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6191b-138">System.String</span></span>

## <span data-ttu-id="6191b-139">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="6191b-139">OUTPUTS</span></span>

### <span data-ttu-id="6191b-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="6191b-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="6191b-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6191b-141">NOTES</span></span>

## <span data-ttu-id="6191b-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6191b-142">RELATED LINKS</span></span>

[<span data-ttu-id="6191b-143">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="6191b-143">Get-AzSearchAdminKeyPair</span></span>](./Get-AzSearchAdminKeyPair.md)
