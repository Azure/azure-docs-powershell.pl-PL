---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/new-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/New-AzureRmSearchQueryKey.md
ms.openlocfilehash: 417e1a546777824df86b72f3740079ac91835192
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549283"
---
# <span data-ttu-id="3cc27-101">New-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="3cc27-101">New-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="3cc27-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3cc27-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc27-103">Utwórz nowy klucz kwerendy dla usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="3cc27-103">Create a new query key for the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3cc27-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3cc27-104">SYNTAX</span></span>

### <span data-ttu-id="3cc27-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3cc27-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cc27-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cc27-106">ParentObjectParameterSet</span></span>
```
New-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3cc27-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3cc27-107">ParentResourceIdParameterSet</span></span>
```
New-AzureRmSearchQueryKey [-ParentResourceId] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3cc27-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3cc27-108">DESCRIPTION</span></span>
<span data-ttu-id="3cc27-109">Polecenie cmdlet **New-AzureRmSearchQueryKey** tworzy nowy klucz kwerendy dla usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="3cc27-109">The **New-AzureRmSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="3cc27-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3cc27-110">EXAMPLES</span></span>

### <span data-ttu-id="3cc27-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3cc27-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="3cc27-112">W przykładzie tworzony jest nowy klucz kwerendy dla usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="3cc27-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="3cc27-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3cc27-113">PARAMETERS</span></span>

### <span data-ttu-id="3cc27-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc27-114">-DefaultProfile</span></span>
<span data-ttu-id="3cc27-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3cc27-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cc27-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3cc27-116">-Name</span></span>
<span data-ttu-id="3cc27-117">Nazwa klucza zapytania usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="3cc27-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="3cc27-118">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="3cc27-118">-ParentObject</span></span>
<span data-ttu-id="3cc27-119">Obiekt wejściowy usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="3cc27-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="3cc27-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3cc27-120">-ParentResourceId</span></span>
<span data-ttu-id="3cc27-121">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="3cc27-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="3cc27-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cc27-122">-ResourceGroupName</span></span>
<span data-ttu-id="3cc27-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3cc27-123">Resource Group name.</span></span>

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

### <span data-ttu-id="3cc27-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3cc27-124">-ServiceName</span></span>
<span data-ttu-id="3cc27-125">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="3cc27-125">Search Service name.</span></span>

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

### <span data-ttu-id="3cc27-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3cc27-126">-Confirm</span></span>
<span data-ttu-id="3cc27-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cc27-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3cc27-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cc27-128">-WhatIf</span></span>
<span data-ttu-id="3cc27-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3cc27-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3cc27-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3cc27-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3cc27-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc27-131">CommonParameters</span></span>
<span data-ttu-id="3cc27-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3cc27-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc27-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3cc27-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc27-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3cc27-134">INPUTS</span></span>

### <span data-ttu-id="3cc27-135">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="3cc27-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="3cc27-136">Parametry: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="3cc27-136">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="3cc27-137">System. String</span><span class="sxs-lookup"><span data-stu-id="3cc27-137">System.String</span></span>

## <span data-ttu-id="3cc27-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3cc27-138">OUTPUTS</span></span>

### <span data-ttu-id="3cc27-139">Microsoft. Azure. Commands. Management. Search. Search. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="3cc27-139">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="3cc27-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3cc27-140">NOTES</span></span>

## <span data-ttu-id="3cc27-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3cc27-141">RELATED LINKS</span></span>

[<span data-ttu-id="3cc27-142">Get-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="3cc27-142">Get-AzureRmSearchQueryKey.md</span></span>](./Get-AzureRmSearchQueryKey.md)

[<span data-ttu-id="3cc27-143">Remove-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="3cc27-143">Remove-AzureRmSearchQueryKey.md</span></span>](./Remove-AzureRmSearchQueryKey.md)
