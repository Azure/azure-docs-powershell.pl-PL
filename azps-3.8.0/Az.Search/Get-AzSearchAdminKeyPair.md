---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: dafc9da9669a7c07f982e4fee87a37e1581af40a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93894974"
---
# <span data-ttu-id="10d60-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="10d60-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="10d60-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="10d60-102">SYNOPSIS</span></span>
<span data-ttu-id="10d60-103">Pobiera parę kluczy administratora usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="10d60-103">Gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="10d60-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="10d60-104">SYNTAX</span></span>

### <span data-ttu-id="10d60-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="10d60-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="10d60-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="10d60-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="10d60-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="10d60-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="10d60-108">Opis</span><span class="sxs-lookup"><span data-stu-id="10d60-108">DESCRIPTION</span></span>
<span data-ttu-id="10d60-109">Polecenie cmdlet **Get-AzSearchAdminKeyPair** pobiera parę kluczy administrator usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="10d60-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="10d60-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="10d60-110">EXAMPLES</span></span>

### <span data-ttu-id="10d60-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="10d60-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="10d60-112">W przykładzie otrzymano parę kluczy administrator usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="10d60-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="10d60-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="10d60-113">PARAMETERS</span></span>

### <span data-ttu-id="10d60-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="10d60-114">-DefaultProfile</span></span>
<span data-ttu-id="10d60-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="10d60-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="10d60-116">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="10d60-116">-ParentObject</span></span>
<span data-ttu-id="10d60-117">Obiekt wejściowy usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="10d60-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="10d60-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="10d60-118">-ParentResourceId</span></span>
<span data-ttu-id="10d60-119">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="10d60-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="10d60-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="10d60-120">-ResourceGroupName</span></span>
<span data-ttu-id="10d60-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="10d60-121">Resource Group name.</span></span>

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

### <span data-ttu-id="10d60-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="10d60-122">-ServiceName</span></span>
<span data-ttu-id="10d60-123">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="10d60-123">Search Service name.</span></span>

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

### <span data-ttu-id="10d60-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="10d60-124">CommonParameters</span></span>
<span data-ttu-id="10d60-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="10d60-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="10d60-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="10d60-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="10d60-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="10d60-127">INPUTS</span></span>

### <span data-ttu-id="10d60-128">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="10d60-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="10d60-129">System. String</span><span class="sxs-lookup"><span data-stu-id="10d60-129">System.String</span></span>

## <span data-ttu-id="10d60-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="10d60-130">OUTPUTS</span></span>

### <span data-ttu-id="10d60-131">Microsoft. Azure. Commands. Management. Search. Search. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="10d60-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="10d60-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="10d60-132">NOTES</span></span>

## <span data-ttu-id="10d60-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="10d60-133">RELATED LINKS</span></span>

[<span data-ttu-id="10d60-134">Nowe — AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="10d60-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
