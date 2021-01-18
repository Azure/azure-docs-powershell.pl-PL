---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: a0dddf6e7cc5080ca4028b1348381c1b5fb72df6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98498438"
---
# <span data-ttu-id="ed2b7-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="ed2b7-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="ed2b7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ed2b7-102">SYNOPSIS</span></span>
<span data-ttu-id="ed2b7-103">Pobiera klucze zapytania usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="ed2b7-103">Gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="ed2b7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ed2b7-104">SYNTAX</span></span>

### <span data-ttu-id="ed2b7-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ed2b7-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="ed2b7-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed2b7-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="ed2b7-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ed2b7-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ed2b7-108">Opis</span><span class="sxs-lookup"><span data-stu-id="ed2b7-108">DESCRIPTION</span></span>
<span data-ttu-id="ed2b7-109">Polecenie cmdlet **Get-AzSearchQueryKey** pobiera klucze zapytań usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="ed2b7-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Search service.</span></span>

## <span data-ttu-id="ed2b7-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ed2b7-110">EXAMPLES</span></span>

### <span data-ttu-id="ed2b7-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="ed2b7-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="ed2b7-112">W przykładzie są pobierane wszystkie klucze zapytań usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="ed2b7-112">The example gets all query key(s) of the Azure Search Service.</span></span>

## <span data-ttu-id="ed2b7-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ed2b7-113">PARAMETERS</span></span>

### <span data-ttu-id="ed2b7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed2b7-114">-DefaultProfile</span></span>
<span data-ttu-id="ed2b7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ed2b7-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ed2b7-116">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="ed2b7-116">-ParentObject</span></span>
<span data-ttu-id="ed2b7-117">Obiekt wejściowy usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="ed2b7-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="ed2b7-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="ed2b7-118">-ParentResourceId</span></span>
<span data-ttu-id="ed2b7-119">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="ed2b7-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="ed2b7-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed2b7-120">-ResourceGroupName</span></span>
<span data-ttu-id="ed2b7-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ed2b7-121">Resource Group name.</span></span>

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

### <span data-ttu-id="ed2b7-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="ed2b7-122">-ServiceName</span></span>
<span data-ttu-id="ed2b7-123">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="ed2b7-123">Search Service name.</span></span>

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

### <span data-ttu-id="ed2b7-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed2b7-124">CommonParameters</span></span>
<span data-ttu-id="ed2b7-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ed2b7-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed2b7-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed2b7-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed2b7-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ed2b7-127">INPUTS</span></span>

### <span data-ttu-id="ed2b7-128">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="ed2b7-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="ed2b7-129">System. String</span><span class="sxs-lookup"><span data-stu-id="ed2b7-129">System.String</span></span>

## <span data-ttu-id="ed2b7-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ed2b7-130">OUTPUTS</span></span>

### <span data-ttu-id="ed2b7-131">Microsoft. Azure. Commands. Management. Search. Search. PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="ed2b7-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="ed2b7-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ed2b7-132">NOTES</span></span>

## <span data-ttu-id="ed2b7-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ed2b7-133">RELATED LINKS</span></span>

[<span data-ttu-id="ed2b7-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="ed2b7-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="ed2b7-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="ed2b7-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)