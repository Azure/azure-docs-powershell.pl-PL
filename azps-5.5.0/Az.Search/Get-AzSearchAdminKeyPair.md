---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchadminkeypair
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchAdminKeyPair.md
ms.openlocfilehash: e6f2495392eed73e5576d8502f86a08e325337f2
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183611"
---
# <span data-ttu-id="a69de-101">Get-AzSearchAdminKeyPair</span><span class="sxs-lookup"><span data-stu-id="a69de-101">Get-AzSearchAdminKeyPair</span></span>

## <span data-ttu-id="a69de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a69de-102">SYNOPSIS</span></span>
<span data-ttu-id="a69de-103">Pobiera parę klucza administratora usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="a69de-103">Gets admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="a69de-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a69de-104">SYNTAX</span></span>

### <span data-ttu-id="a69de-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="a69de-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchAdminKeyPair [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a69de-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="a69de-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a69de-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a69de-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchAdminKeyPair [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a69de-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="a69de-108">DESCRIPTION</span></span>
<span data-ttu-id="a69de-109">Polecenie **cmdlet Get-AzSearchAdminKeyPair** pobiera parę klucza administratora usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="a69de-109">The **Get-AzSearchAdminKeyPair** cmdlet gets the admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="a69de-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a69de-110">EXAMPLES</span></span>

### <span data-ttu-id="a69de-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="a69de-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchAdminKeyPair -ResourceGroupName felixwa-01 -ServiceName felixwa-basic-search

Primary                          Secondary                       
-------                          ---------                       
3B06A25BDADFF72EC132736BAA2547A1 E643B75A52E04DF13EB690807C451C55
```

<span data-ttu-id="a69de-112">Przykład pobiera parę klucza administratora usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="a69de-112">The example gets admin key pair of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="a69de-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a69de-113">PARAMETERS</span></span>

### <span data-ttu-id="a69de-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a69de-114">-DefaultProfile</span></span>
<span data-ttu-id="a69de-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a69de-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a69de-116">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="a69de-116">-ParentObject</span></span>
<span data-ttu-id="a69de-117">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="a69de-117">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="a69de-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="a69de-118">-ParentResourceId</span></span>
<span data-ttu-id="a69de-119">Identyfikator zasobu usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="a69de-119">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="a69de-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a69de-120">-ResourceGroupName</span></span>
<span data-ttu-id="a69de-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a69de-121">Resource Group name.</span></span>

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

### <span data-ttu-id="a69de-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="a69de-122">-ServiceName</span></span>
<span data-ttu-id="a69de-123">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="a69de-123">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="a69de-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a69de-124">CommonParameters</span></span>
<span data-ttu-id="a69de-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a69de-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a69de-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a69de-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a69de-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a69de-127">INPUTS</span></span>

### <span data-ttu-id="a69de-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="a69de-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="a69de-129">System.String</span><span class="sxs-lookup"><span data-stu-id="a69de-129">System.String</span></span>

## <span data-ttu-id="a69de-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a69de-130">OUTPUTS</span></span>

### <span data-ttu-id="a69de-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="a69de-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchAdminKey</span></span>

## <span data-ttu-id="a69de-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a69de-132">NOTES</span></span>

## <span data-ttu-id="a69de-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a69de-133">RELATED LINKS</span></span>

[<span data-ttu-id="a69de-134">New-AzSearchAdminKey</span><span class="sxs-lookup"><span data-stu-id="a69de-134">New-AzSearchAdminKey</span></span>](./New-AzSearchAdminKey.md)
