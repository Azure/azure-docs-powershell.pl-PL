---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: e7a74fcc6d5e1a80282cfb365070df1b339aea45
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94220364"
---
# <span data-ttu-id="a0094-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="a0094-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="a0094-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a0094-102">SYNOPSIS</span></span>
<span data-ttu-id="a0094-103">Usuń klucz zapytania z usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="a0094-103">Remove the query key from the Azure Search service.</span></span>

## <span data-ttu-id="a0094-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a0094-104">SYNTAX</span></span>

### <span data-ttu-id="a0094-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a0094-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0094-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0094-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a0094-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a0094-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a0094-108">Opis</span><span class="sxs-lookup"><span data-stu-id="a0094-108">DESCRIPTION</span></span>
<span data-ttu-id="a0094-109">Polecenie cmdlet **Remove-AzSearchQueryKey** usuwa klucz zapytania z usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="a0094-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="a0094-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a0094-110">EXAMPLES</span></span>

### <span data-ttu-id="a0094-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a0094-111">Example 1</span></span>
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

<span data-ttu-id="a0094-112">W przykładzie usunięto klucz zapytania z usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="a0094-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="a0094-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a0094-113">PARAMETERS</span></span>

### <span data-ttu-id="a0094-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0094-114">-DefaultProfile</span></span>
<span data-ttu-id="a0094-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a0094-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a0094-116">-Force</span><span class="sxs-lookup"><span data-stu-id="a0094-116">-Force</span></span>
<span data-ttu-id="a0094-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a0094-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a0094-118">-Wartość parametru</span><span class="sxs-lookup"><span data-stu-id="a0094-118">-KeyValue</span></span>
<span data-ttu-id="a0094-119">Wartość klucza zapytania usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="a0094-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="a0094-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="a0094-120">-ParentObject</span></span>
<span data-ttu-id="a0094-121">Obiekt wejściowy usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="a0094-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="a0094-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a0094-122">-ParentResourceId</span></span>
<span data-ttu-id="a0094-123">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="a0094-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="a0094-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a0094-124">-PassThru</span></span>
<span data-ttu-id="a0094-125">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="a0094-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="a0094-126">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="a0094-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a0094-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0094-127">-ResourceGroupName</span></span>
<span data-ttu-id="a0094-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a0094-128">Resource Group name.</span></span>

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

### <span data-ttu-id="a0094-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a0094-129">-ServiceName</span></span>
<span data-ttu-id="a0094-130">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="a0094-130">Search Service name.</span></span>

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

### <span data-ttu-id="a0094-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a0094-131">-Confirm</span></span>
<span data-ttu-id="a0094-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0094-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a0094-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a0094-133">-WhatIf</span></span>
<span data-ttu-id="a0094-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a0094-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a0094-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a0094-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a0094-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0094-136">CommonParameters</span></span>
<span data-ttu-id="a0094-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a0094-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0094-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0094-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0094-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a0094-139">INPUTS</span></span>

### <span data-ttu-id="a0094-140">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="a0094-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="a0094-141">System. String</span><span class="sxs-lookup"><span data-stu-id="a0094-141">System.String</span></span>

## <span data-ttu-id="a0094-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a0094-142">OUTPUTS</span></span>

### <span data-ttu-id="a0094-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a0094-143">System.Boolean</span></span>

## <span data-ttu-id="a0094-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a0094-144">NOTES</span></span>

## <span data-ttu-id="a0094-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a0094-145">RELATED LINKS</span></span>

[<span data-ttu-id="a0094-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="a0094-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="a0094-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="a0094-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
