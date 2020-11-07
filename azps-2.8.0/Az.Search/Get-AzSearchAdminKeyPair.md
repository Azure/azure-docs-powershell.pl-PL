---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: cd944184f4691b3f88934afc3a7bd9132eb23fda
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871724"
---
# <span data-ttu-id="8633d-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="8633d-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="8633d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8633d-102">SYNOPSIS</span></span>
<span data-ttu-id="8633d-103">Pobiera parę kluczy administratora usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="8633d-103">Gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="8633d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8633d-104">SYNTAX</span></span>

### <span data-ttu-id="8633d-105">ResourceNameParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8633d-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8633d-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8633d-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8633d-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8633d-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8633d-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8633d-108">DESCRIPTION</span></span>
<span data-ttu-id="8633d-109">Polecenie cmdlet **Get-AzSearchAdminKeyPair** pobiera parę kluczy administrator usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="8633d-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="8633d-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8633d-110">EXAMPLES</span></span>

### <span data-ttu-id="8633d-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="8633d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="8633d-112">W przykładzie otrzymano parę kluczy administrator usługi Azure Search.</span><span class="sxs-lookup"><span data-stu-id="8633d-112">The example gets admin key pair of the Azure Search service.</span></span>

## <span data-ttu-id="8633d-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8633d-113">PARAMETERS</span></span>

### <span data-ttu-id="8633d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8633d-114">-DefaultProfile</span></span>
<span data-ttu-id="8633d-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8633d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8633d-116">-Obiekt nadrzędnyobject</span><span class="sxs-lookup"><span data-stu-id="8633d-116">-ParentObject</span></span>
<span data-ttu-id="8633d-117">Obiekt wejściowy usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="8633d-117">Search Service Input Object.</span></span>

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

### <span data-ttu-id="8633d-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8633d-118">-ParentResourceId</span></span>
<span data-ttu-id="8633d-119">Identyfikator zasobu usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="8633d-119">Search Service Resource Id.</span></span>

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

### <span data-ttu-id="8633d-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8633d-120">-ResourceGroupName</span></span>
<span data-ttu-id="8633d-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="8633d-121">Resource Group name.</span></span>

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

### <span data-ttu-id="8633d-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="8633d-122">-ServiceName</span></span>
<span data-ttu-id="8633d-123">Nazwa usługi wyszukiwania.</span><span class="sxs-lookup"><span data-stu-id="8633d-123">Search Service name.</span></span>

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

### <span data-ttu-id="8633d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8633d-124">CommonParameters</span></span>
<span data-ttu-id="8633d-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8633d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8633d-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8633d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8633d-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8633d-127">INPUTS</span></span>

### <span data-ttu-id="8633d-128">Microsoft. Azure. Commands. Management. Search. Search. PSSearchService</span><span class="sxs-lookup"><span data-stu-id="8633d-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="8633d-129">System. String</span><span class="sxs-lookup"><span data-stu-id="8633d-129">System.String</span></span>

## <span data-ttu-id="8633d-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8633d-130">OUTPUTS</span></span>

### <span data-ttu-id="8633d-131">Microsoft. Azure. Commands. Management. Search. Search. PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="8633d-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="8633d-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8633d-132">NOTES</span></span>

## <span data-ttu-id="8633d-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8633d-133">RELATED LINKS</span></span>

[<span data-ttu-id="8633d-134">Nowe — AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="8633d-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
