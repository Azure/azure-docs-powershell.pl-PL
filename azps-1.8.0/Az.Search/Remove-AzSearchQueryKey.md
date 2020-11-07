---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/remove-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Remove-AzSearchQueryKey.md
ms.openlocfilehash: ae781b4c53e373cdbd8338f4db75d6913c863bfd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708241"
---
# <span data-ttu-id="6ff17-101">Remove-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="6ff17-101">Remove-AzSearchQueryKey</span></span>

## <span data-ttu-id="6ff17-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6ff17-102">SYNOPSIS</span></span>
<span data-ttu-id="6ff17-103">Usuń klucz zapytania z usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="6ff17-103">Remove the query key from the Azure Search service.</span></span>

## <span data-ttu-id="6ff17-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6ff17-104">SYNTAX</span></span>

### <span data-ttu-id="6ff17-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6ff17-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ff17-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ff17-106">ParentObjectParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ff17-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ff17-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ff17-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6ff17-108">DESCRIPTION</span></span>
<span data-ttu-id="6ff17-109">Polecenie cmdlet **Remove-AzSearchQueryKey** usuwa klucz zapytania z usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="6ff17-109">The **Remove-AzSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="6ff17-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6ff17-110">EXAMPLES</span></span>

### <span data-ttu-id="6ff17-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6ff17-111">Example 1</span></span>
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

<span data-ttu-id="6ff17-112">W przykładzie usunięto klucz zapytania z usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="6ff17-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="6ff17-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6ff17-113">PARAMETERS</span></span>

### <span data-ttu-id="6ff17-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ff17-114">-DefaultProfile</span></span>
<span data-ttu-id="6ff17-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ff17-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ff17-116">-Force</span><span class="sxs-lookup"><span data-stu-id="6ff17-116">-Force</span></span>
<span data-ttu-id="6ff17-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6ff17-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="6ff17-118">-Wartość parametru</span><span class="sxs-lookup"><span data-stu-id="6ff17-118">-KeyValue</span></span>
<span data-ttu-id="6ff17-119">Wartość klucza zapytania usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="6ff17-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="6ff17-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="6ff17-120">-ParentObject</span></span>
<span data-ttu-id="6ff17-121">Obiekt wejściowy usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="6ff17-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="6ff17-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6ff17-122">-ParentResourceId</span></span>
<span data-ttu-id="6ff17-123">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="6ff17-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="6ff17-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6ff17-124">-PassThru</span></span>
<span data-ttu-id="6ff17-125">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="6ff17-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="6ff17-126">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="6ff17-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="6ff17-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ff17-127">-ResourceGroupName</span></span>
<span data-ttu-id="6ff17-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6ff17-128">Resource Group name.</span></span>

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

### <span data-ttu-id="6ff17-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6ff17-129">-ServiceName</span></span>
<span data-ttu-id="6ff17-130">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="6ff17-130">Search Service name.</span></span>

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

### <span data-ttu-id="6ff17-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ff17-131">-Confirm</span></span>
<span data-ttu-id="6ff17-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ff17-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ff17-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ff17-133">-WhatIf</span></span>
<span data-ttu-id="6ff17-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ff17-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ff17-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6ff17-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ff17-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ff17-136">CommonParameters</span></span>
<span data-ttu-id="6ff17-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ff17-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ff17-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6ff17-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ff17-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ff17-139">INPUTS</span></span>

### <span data-ttu-id="6ff17-140">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="6ff17-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="6ff17-141">System. String</span><span class="sxs-lookup"><span data-stu-id="6ff17-141">System.String</span></span>

## <span data-ttu-id="6ff17-142">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6ff17-142">OUTPUTS</span></span>

### <span data-ttu-id="6ff17-143">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="6ff17-143">System.Boolean</span></span>

## <span data-ttu-id="6ff17-144">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6ff17-144">NOTES</span></span>

## <span data-ttu-id="6ff17-145">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ff17-145">RELATED LINKS</span></span>

[<span data-ttu-id="6ff17-146">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="6ff17-146">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="6ff17-147">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="6ff17-147">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)
