---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/remove-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Remove-AzureRmSearchQueryKey.md
ms.openlocfilehash: 1dbdf342335ca204287ccfd2efea737f2eb747fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549279"
---
# <span data-ttu-id="eb7d5-101">Remove-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="eb7d5-101">Remove-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="eb7d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="eb7d5-102">SYNOPSIS</span></span>
<span data-ttu-id="eb7d5-103">Usuń klucz zapytania z usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="eb7d5-103">Remove the query key from the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="eb7d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="eb7d5-104">SYNTAX</span></span>

### <span data-ttu-id="eb7d5-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="eb7d5-105">ResourceNameParameterSet (Default)</span></span>
```
Remove-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -KeyValue <String> [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb7d5-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb7d5-106">ParentObjectParameterSet</span></span>
```
Remove-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="eb7d5-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="eb7d5-107">ParentResourceIdParameterSet</span></span>
```
Remove-AzureRmSearchQueryKey [-ParentResourceId] <String> -KeyValue <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="eb7d5-108">Opis</span><span class="sxs-lookup"><span data-stu-id="eb7d5-108">DESCRIPTION</span></span>
<span data-ttu-id="eb7d5-109">Polecenie cmdlet **Remove-AzureRmSearchQueryKey** usuwa klucz zapytania z usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="eb7d5-109">The **Remove-AzureRmSearchQueryKey** cmdlet removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="eb7d5-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="eb7d5-110">EXAMPLES</span></span>

### <span data-ttu-id="eb7d5-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="eb7d5-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name         Key                             
----         ---                             
             D260F448EA192EBC19D59F7E5670E8BB
NewQueryKey1 B4C13E3F6FA76100D3488673CFDCD438

PS C:\> Remove-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -KeyValue B4C13E3F6FA76100D3488673CFDCD438

Confirm
Are you sure you want to remove query key 'B4C13E3F6FA76100D3488673CFDCD438'?
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y
PS C:\>
```

<span data-ttu-id="eb7d5-112">W przykładzie usunięto klucz zapytania z usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="eb7d5-112">The example removes the query key from the Azure Search service.</span></span>

## <span data-ttu-id="eb7d5-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="eb7d5-113">PARAMETERS</span></span>

### <span data-ttu-id="eb7d5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="eb7d5-114">-DefaultProfile</span></span>
<span data-ttu-id="eb7d5-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="eb7d5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="eb7d5-116">-Force</span><span class="sxs-lookup"><span data-stu-id="eb7d5-116">-Force</span></span>
<span data-ttu-id="eb7d5-117">Nie pytaj o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="eb7d5-117">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="eb7d5-118">-Wartość parametru</span><span class="sxs-lookup"><span data-stu-id="eb7d5-118">-KeyValue</span></span>
<span data-ttu-id="eb7d5-119">Wartość klucza zapytania usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="eb7d5-119">Search Service query key value.</span></span>

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

### <span data-ttu-id="eb7d5-120">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="eb7d5-120">-ParentObject</span></span>
<span data-ttu-id="eb7d5-121">Obiekt wejściowy usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="eb7d5-121">Search Service Input Object.</span></span>

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

### <span data-ttu-id="eb7d5-122">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="eb7d5-122">-ParentResourceId</span></span>
<span data-ttu-id="eb7d5-123">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="eb7d5-123">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="eb7d5-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="eb7d5-124">-PassThru</span></span>
<span data-ttu-id="eb7d5-125">To polecenie cmdlet domyślnie nie zwraca obiektu.</span><span class="sxs-lookup"><span data-stu-id="eb7d5-125">This Cmdlet does not return an object by default.</span></span> <span data-ttu-id="eb7d5-126">Jeśli ten przełącznik jest określony, zwraca wartość PRAWDA, jeśli powiodło się.</span><span class="sxs-lookup"><span data-stu-id="eb7d5-126">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="eb7d5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="eb7d5-127">-ResourceGroupName</span></span>
<span data-ttu-id="eb7d5-128">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="eb7d5-128">Resource Group name.</span></span>

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

### <span data-ttu-id="eb7d5-129">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="eb7d5-129">-ServiceName</span></span>
<span data-ttu-id="eb7d5-130">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="eb7d5-130">Search Service name.</span></span>

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

### <span data-ttu-id="eb7d5-131">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="eb7d5-131">-Confirm</span></span>
<span data-ttu-id="eb7d5-132">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb7d5-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="eb7d5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="eb7d5-133">-WhatIf</span></span>
<span data-ttu-id="eb7d5-134">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="eb7d5-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="eb7d5-135">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="eb7d5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="eb7d5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="eb7d5-136">CommonParameters</span></span>
<span data-ttu-id="eb7d5-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="eb7d5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="eb7d5-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="eb7d5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="eb7d5-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="eb7d5-139">INPUTS</span></span>

### <span data-ttu-id="eb7d5-140">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="eb7d5-140">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="eb7d5-141">Parametry: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="eb7d5-141">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="eb7d5-142">System. String</span><span class="sxs-lookup"><span data-stu-id="eb7d5-142">System.String</span></span>

## <span data-ttu-id="eb7d5-143">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="eb7d5-143">OUTPUTS</span></span>

### <span data-ttu-id="eb7d5-144">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="eb7d5-144">System.Boolean</span></span>

## <span data-ttu-id="eb7d5-145">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="eb7d5-145">NOTES</span></span>

## <span data-ttu-id="eb7d5-146">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="eb7d5-146">RELATED LINKS</span></span>

[<span data-ttu-id="eb7d5-147">New-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="eb7d5-147">New-AzureRmSearchQueryKey.md</span></span>](./New-AzureRmSearchQueryKey.md)

[<span data-ttu-id="eb7d5-148">Get-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="eb7d5-148">Get-AzureRmSearchQueryKey.md</span></span>](./Get-AzureRmSearchQueryKey.md)
