---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/powershell/module/az.search/new-azsearchadminkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchAdminKey.md
ms.openlocfilehash: 4724b24f995b836bbd63420c852d6f0004089a51
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990760"
---
# <span data-ttu-id="5ec48-101">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="5ec48-101">New-AzSearchAdminKey</span></span>

## <span data-ttu-id="5ec48-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ec48-102">SYNOPSIS</span></span>
<span data-ttu-id="5ec48-103">Ponownie generuje klucz administratora usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="5ec48-103">Regenerates an admin key of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="5ec48-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="5ec48-104">SYNTAX</span></span>

### <span data-ttu-id="5ec48-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="5ec48-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchAdminKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyKind <PSSearchAdminKeyKind>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ec48-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ec48-106">ParentObjectParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentObject] <PSSearchService> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5ec48-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="5ec48-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchAdminKey [-ParentResourceId] <String> -KeyKind <PSSearchAdminKeyKind> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ec48-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="5ec48-108">DESCRIPTION</span></span>
<span data-ttu-id="5ec48-109">Polecenie **cmdlet New-AzSearchAdminKey** ponownie generuje klucz administratora usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="5ec48-109">The **New-AzSearchAdminKey** cmdlet regenerates an admin key of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="5ec48-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="5ec48-110">EXAMPLES</span></span>

### <span data-ttu-id="5ec48-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="5ec48-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchAdminKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyKind Primary

Confirm
Are you sure you want to regenerate 'Primary' key for Search Service 'pstestazuresearch01'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y

Primary                          Secondary
-------                          ---------
85B3813D11904B591BE8A196C2C743A1 CEF791D5BAC2E6C0B232C56702F21E87
```

<span data-ttu-id="5ec48-112">Przykład ponownie generuje klucz podstawowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="5ec48-112">The example regenerates Primary key of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="5ec48-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5ec48-113">PARAMETERS</span></span>

### <span data-ttu-id="5ec48-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ec48-114">-DefaultProfile</span></span>
<span data-ttu-id="5ec48-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="5ec48-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5ec48-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="5ec48-116">-Force</span></span>
<span data-ttu-id="5ec48-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5ec48-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5ec48-118">-KeyKind</span><span class="sxs-lookup"><span data-stu-id="5ec48-118">-KeyKind</span></span>
<span data-ttu-id="5ec48-119">Typ klucza administratora usługi Azure Cognitive Search Service (podstawowy/pomocniczy).</span><span class="sxs-lookup"><span data-stu-id="5ec48-119">Azure Cognitive Search Service admin key kind (Primary/Secondary).</span></span>

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

### <span data-ttu-id="5ec48-120">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="5ec48-120">-ParentObject</span></span>
<span data-ttu-id="5ec48-121">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="5ec48-121">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="5ec48-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="5ec48-122">-ParentResourceId</span></span>
<span data-ttu-id="5ec48-123">Identyfikator zasobu usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="5ec48-123">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="5ec48-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ec48-124">-ResourceGroupName</span></span>
<span data-ttu-id="5ec48-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="5ec48-125">Resource Group name.</span></span>

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

### <span data-ttu-id="5ec48-126">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5ec48-126">-ServiceName</span></span>
<span data-ttu-id="5ec48-127">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="5ec48-127">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="5ec48-128">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ec48-128">-Confirm</span></span>
<span data-ttu-id="5ec48-129">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="5ec48-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ec48-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ec48-130">-WhatIf</span></span>
<span data-ttu-id="5ec48-131">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ec48-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ec48-132">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="5ec48-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ec48-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ec48-133">CommonParameters</span></span>
<span data-ttu-id="5ec48-134">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ec48-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ec48-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5ec48-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ec48-136">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ec48-136">INPUTS</span></span>

### <span data-ttu-id="5ec48-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="5ec48-137">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="5ec48-138">System.String</span><span class="sxs-lookup"><span data-stu-id="5ec48-138">System.String</span></span>

## <span data-ttu-id="5ec48-139">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ec48-139">OUTPUTS</span></span>

### <span data-ttu-id="5ec48-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="5ec48-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="5ec48-141">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="5ec48-141">NOTES</span></span>

## <span data-ttu-id="5ec48-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ec48-142">RELATED LINKS</span></span>

[<span data-ttu-id="5ec48-143">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="5ec48-143">Get-AzSearchAdminKeyPair</span></span>](./Get-AzSearchAdminKeyPair.md)
