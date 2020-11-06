---
external help file: Microsoft.Azure.Commands.Management.Search.dll-Help.xml
Module Name: AzureRM.Search
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.search/get-azurermsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Search/Commands.Management.Search/help/Get-AzureRmSearchQueryKey.md
ms.openlocfilehash: 3535e9d7723c87e0f528192e47c921d3835ff9e3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541452"
---
# <span data-ttu-id="6fd64-101">Get-AzureRmSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="6fd64-101">Get-AzureRmSearchQueryKey</span></span>

## <span data-ttu-id="6fd64-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6fd64-102">SYNOPSIS</span></span>
<span data-ttu-id="6fd64-103">Pobiera klucze zapytania usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="6fd64-103">Gets query key(s) of the Azure Search service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fd64-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6fd64-104">SYNTAX</span></span>

### <span data-ttu-id="6fd64-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="6fd64-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzureRmSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6fd64-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fd64-106">ParentObjectParameterSet</span></span>
```
Get-AzureRmSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6fd64-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6fd64-107">ParentResourceIdParameterSet</span></span>
```
Get-AzureRmSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6fd64-108">Opis</span><span class="sxs-lookup"><span data-stu-id="6fd64-108">DESCRIPTION</span></span>
<span data-ttu-id="6fd64-109">Polecenie cmdlet **Get-AzureRmSearchQueryKey** pobiera klucze zapytań usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="6fd64-109">The **Get-AzureRmSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="6fd64-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6fd64-110">EXAMPLES</span></span>

### <span data-ttu-id="6fd64-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6fd64-111">Example 1</span></span>
```powershell
PS C:\> Get-AzureRmSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="6fd64-112">W przykładzie są pobierane wszystkie klucze zapytań usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="6fd64-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="6fd64-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6fd64-113">PARAMETERS</span></span>

### <span data-ttu-id="6fd64-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fd64-114">-DefaultProfile</span></span>
<span data-ttu-id="6fd64-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6fd64-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6fd64-116">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="6fd64-116">-ParentObject</span></span>
<span data-ttu-id="6fd64-117">Obiekt wejściowy usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="6fd64-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="6fd64-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="6fd64-118">-ParentResourceId</span></span>
<span data-ttu-id="6fd64-119">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="6fd64-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="6fd64-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fd64-120">-ResourceGroupName</span></span>
<span data-ttu-id="6fd64-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6fd64-121">Resource Group name.</span></span>

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

### <span data-ttu-id="6fd64-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="6fd64-122">-ServiceName</span></span>
<span data-ttu-id="6fd64-123">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="6fd64-123">Search Service name.</span></span>

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

### <span data-ttu-id="6fd64-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fd64-124">CommonParameters</span></span>
<span data-ttu-id="6fd64-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fd64-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fd64-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fd64-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fd64-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6fd64-127">INPUTS</span></span>

### <span data-ttu-id="6fd64-128">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="6fd64-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>
<span data-ttu-id="6fd64-129">Parametry: ParentObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6fd64-129">Parameters: ParentObject (ByValue)</span></span>

### <span data-ttu-id="6fd64-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6fd64-130">System.String</span></span>

## <span data-ttu-id="6fd64-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6fd64-131">OUTPUTS</span></span>

### <span data-ttu-id="6fd64-132">Microsoft. Azure. Commands. Management. Search. Search. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="6fd64-132">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="6fd64-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6fd64-133">NOTES</span></span>

## <span data-ttu-id="6fd64-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6fd64-134">RELATED LINKS</span></span>

[<span data-ttu-id="6fd64-135">New-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="6fd64-135">New-AzureRmSearchQueryKey.md</span></span>](./New-AzureRmSearchQueryKey.md)

[<span data-ttu-id="6fd64-136">Remove-AzureRmSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="6fd64-136">Remove-AzureRmSearchQueryKey.md</span></span>](./Remove-AzureRmSearchQueryKey.md)
