---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: 3d4610f83b348864fc57cf6894db1ab7455a8485
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100240010"
---
# <span data-ttu-id="00f8a-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="00f8a-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="00f8a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00f8a-102">SYNOPSIS</span></span>
<span data-ttu-id="00f8a-103">Usuń klucz zapytania z usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="00f8a-103">Remove the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="00f8a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="00f8a-104">SYNTAX</span></span>

### <span data-ttu-id="00f8a-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="00f8a-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00f8a-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="00f8a-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="00f8a-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="00f8a-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="00f8a-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="00f8a-108">DESCRIPTION</span></span>
<span data-ttu-id="00f8a-109">Polecenie **cmdlet Remove-AzSearchQueryKey** usuwa klucz zapytania z usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="00f8a-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="00f8a-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="00f8a-110">EXAMPLES</span></span>

### <span data-ttu-id="00f8a-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="00f8a-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name         Key                             
----         ---                             
             D260F448EA192EBC19D59F7E5670E8BB
NewQueryKey1 B4C13E3F6FA76100D3488673CFDCD438

PS C:\> Remove-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyValue B4C13E3F6FA76100D3488673CFDCD438

Confirm
Are you sure you want to remove query key 'B4C13E3F6FA76100D3488673CFDCD438'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="00f8a-112">W tym przykładzie klucz zapytania jest usuwany z usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="00f8a-112">The example removes the query key from the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="00f8a-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="00f8a-113">PARAMETERS</span></span>

### <span data-ttu-id="00f8a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00f8a-114">-DefaultProfile</span></span>
<span data-ttu-id="00f8a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="00f8a-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00f8a-116">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="00f8a-116">-Force</span></span>
<span data-ttu-id="00f8a-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="00f8a-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="00f8a-118">-KeyValue</span><span class="sxs-lookup"><span data-stu-id="00f8a-118">-KeyValue</span></span>
<span data-ttu-id="00f8a-119">Wartość klucza zapytania usługi Azure Cognitive Search Service.</span><span class="sxs-lookup"><span data-stu-id="00f8a-119">Azure Cognitive Search Service query key value.</span></span>

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

### <span data-ttu-id="00f8a-120">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="00f8a-120">-ParentObject</span></span>
<span data-ttu-id="00f8a-121">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="00f8a-121">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="00f8a-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="00f8a-122">-ParentResourceId</span></span>
<span data-ttu-id="00f8a-123">Identyfikator zasobu usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="00f8a-123">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="00f8a-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="00f8a-124">-PassThru</span></span>
<span data-ttu-id="00f8a-125">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="00f8a-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="00f8a-126">Jeśli ten przełącznik zostanie określony, zostanie on podany jako prawda, jeśli zostanie pomyślnie określony.</span><span class="sxs-lookup"><span data-stu-id="00f8a-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="00f8a-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00f8a-127">-ResourceGroupName</span></span>
<span data-ttu-id="00f8a-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="00f8a-128">Resource Group name.</span></span>

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

### <span data-ttu-id="00f8a-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="00f8a-129">-ServiceName</span></span>
<span data-ttu-id="00f8a-130">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="00f8a-130">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="00f8a-131">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="00f8a-131">-Confirm</span></span>
<span data-ttu-id="00f8a-132">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="00f8a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="00f8a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="00f8a-133">-WhatIf</span></span>
<span data-ttu-id="00f8a-134">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="00f8a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="00f8a-135">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="00f8a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="00f8a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00f8a-136">CommonParameters</span></span>
<span data-ttu-id="00f8a-137">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="00f8a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00f8a-138">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="00f8a-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00f8a-139">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00f8a-139">INPUTS</span></span>

### <span data-ttu-id="00f8a-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="00f8a-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="00f8a-141">System.String</span><span class="sxs-lookup"><span data-stu-id="00f8a-141">System.String</span></span>

## <span data-ttu-id="00f8a-142">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="00f8a-142">OUTPUTS</span></span>

### <span data-ttu-id="00f8a-143">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="00f8a-143">System.Boolean</span></span>

## <span data-ttu-id="00f8a-144">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="00f8a-144">NOTES</span></span>

## <span data-ttu-id="00f8a-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="00f8a-145">RELATED LINKS</span></span>

[<span data-ttu-id="00f8a-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="00f8a-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="00f8a-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="00f8a-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
