---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/new-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/New-AzSearchQueryKey.md
ms.openlocfilehash: e01e5e244bd34e3e18aa287e0f2f5709c5e208ec
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498429"
---
# <span data-ttu-id="3a579-101">New-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="3a579-101">New-AzSearchQueryKey</span></span>

## <span data-ttu-id="3a579-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3a579-102">SYNOPSIS</span></span>
<span data-ttu-id="3a579-103">Utwórz nowy klucz kwerendy dla usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="3a579-103">Create a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="3a579-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3a579-104">SYNTAX</span></span>

### <span data-ttu-id="3a579-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3a579-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a579-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a579-106">ParentObjectParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentObject] <PSSearchService> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a579-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a579-107">ParentResourceIdParameterSet</span></span>
```
New-AzSearchQueryKey [-ParentResourceId] <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a579-108">Opis</span><span class="sxs-lookup"><span data-stu-id="3a579-108">DESCRIPTION</span></span>
<span data-ttu-id="3a579-109">Polecenie cmdlet **New-AzSearchQueryKey** tworzy nowy klucz kwerendy dla usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="3a579-109">The **New-AzSearchQueryKey** cmdlet creates a new query key for the Azure Search Service.</span></span>

## <span data-ttu-id="3a579-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3a579-110">EXAMPLES</span></span>

### <span data-ttu-id="3a579-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="3a579-111">Example 1</span></span>
```powershell
PS C:\> New-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01" -Name "NewQueryKey1" -Force

Name         Key                             
----         ---                             
NewQueryKey1 65FBCF561228C5F0E01F8F2114C80459
```

<span data-ttu-id="3a579-112">W przykładzie tworzony jest nowy klucz kwerendy dla usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="3a579-112">The example creates a new query key for the Azure Search service.</span></span>

## <span data-ttu-id="3a579-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3a579-113">PARAMETERS</span></span>

### <span data-ttu-id="3a579-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a579-114">-DefaultProfile</span></span>
<span data-ttu-id="3a579-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3a579-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a579-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="3a579-116">-Name</span></span>
<span data-ttu-id="3a579-117">Nazwa klucza zapytania usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="3a579-117">Search Service query key name.</span></span>

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

### <span data-ttu-id="3a579-118">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="3a579-118">-ParentObject</span></span>
<span data-ttu-id="3a579-119">Obiekt wejściowy usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="3a579-119">Search Service Input Object.</span></span>

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

### <span data-ttu-id="3a579-120">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="3a579-120">-ParentResourceId</span></span>
<span data-ttu-id="3a579-121">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="3a579-121">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="3a579-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a579-122">-ResourceGroupName</span></span>
<span data-ttu-id="3a579-123">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="3a579-123">Resource Group name.</span></span>

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

### <span data-ttu-id="3a579-124">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3a579-124">-ServiceName</span></span>
<span data-ttu-id="3a579-125">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="3a579-125">Search Service name.</span></span>

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

### <span data-ttu-id="3a579-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3a579-126">-Confirm</span></span>
<span data-ttu-id="3a579-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a579-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a579-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a579-128">-WhatIf</span></span>
<span data-ttu-id="3a579-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3a579-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3a579-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3a579-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a579-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a579-131">CommonParameters</span></span>
<span data-ttu-id="3a579-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3a579-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a579-133">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a579-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a579-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3a579-134">INPUTS</span></span>

### <span data-ttu-id="3a579-135">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="3a579-135">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="3a579-136">System. String</span><span class="sxs-lookup"><span data-stu-id="3a579-136">System.String</span></span>

## <span data-ttu-id="3a579-137">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3a579-137">OUTPUTS</span></span>

### <span data-ttu-id="3a579-138">Microsoft. Azure. Commands. Management. Search. Search. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="3a579-138">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="3a579-139">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3a579-139">NOTES</span></span>

## <span data-ttu-id="3a579-140">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3a579-140">RELATED LINKS</span></span>

[<span data-ttu-id="3a579-141">Get-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="3a579-141">Get-AzSearchQueryKey.md</span></span>](./Get-AzSearchQueryKey.md)

[<span data-ttu-id="3a579-142">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="3a579-142">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)
