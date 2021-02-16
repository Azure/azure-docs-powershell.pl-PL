---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Search.dll-Help.xml
Module Name: Az.Search
online version: https://docs.microsoft.com/en-us/powershell/module/az.search/get-azsearchquerykey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Search/Search/help/Get-AzSearchQueryKey.md
ms.openlocfilehash: 1c5845b0273d47f1aa1a18782a9243bc5ee5ca9f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242427"
---
# <span data-ttu-id="955ba-101">Get-AzSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="955ba-101">Get-AzSearchQueryKey</span></span>

## <span data-ttu-id="955ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="955ba-102">SYNOPSIS</span></span>
<span data-ttu-id="955ba-103">Pobiera klucz(-y) zapytania usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="955ba-103">Gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="955ba-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="955ba-104">SYNTAX</span></span>

### <span data-ttu-id="955ba-105">ResourceNameParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="955ba-105">ResourceNameParameterSet (Default)</span></span>
```
Get-AzSearchQueryKey [-ResourceGroupName] <String> [-ServiceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="955ba-106">ParentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="955ba-106">ParentObjectParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentObject] <PSSearchService> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="955ba-107">ParentResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="955ba-107">ParentResourceIdParameterSet</span></span>
```
Get-AzSearchQueryKey [-ParentResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="955ba-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="955ba-108">DESCRIPTION</span></span>
<span data-ttu-id="955ba-109">Polecenie **cmdlet Get-AzSearchQueryKey** pobiera klucze zapytań usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="955ba-109">The **Get-AzSearchQueryKey** cmdlet gets query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="955ba-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="955ba-110">EXAMPLES</span></span>

### <span data-ttu-id="955ba-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="955ba-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSearchQueryKey -ResourceGroupName "TestAzureSearchPsGroup" -ServiceName "pstestazuresearch01"

Name Key                             
---- ---                             
     896AA09C167541072D404E1BE0442CE9
```

<span data-ttu-id="955ba-112">W tym przykładzie są zwracane wszystkie klucz(-y) zapytania usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="955ba-112">The example gets all query key(s) of the Azure Cognitive Search service.</span></span>

## <span data-ttu-id="955ba-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="955ba-113">PARAMETERS</span></span>

### <span data-ttu-id="955ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="955ba-114">-DefaultProfile</span></span>
<span data-ttu-id="955ba-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="955ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="955ba-116">- ParentObject</span><span class="sxs-lookup"><span data-stu-id="955ba-116">-ParentObject</span></span>
<span data-ttu-id="955ba-117">Obiekt wejściowy usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="955ba-117">Azure Cognitive Search Service Input Object.</span></span>

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

### <span data-ttu-id="955ba-118">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="955ba-118">-ParentResourceId</span></span>
<span data-ttu-id="955ba-119">Identyfikator zasobu usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="955ba-119">Azure Cognitive Search Service Resource Id.</span></span>

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

### <span data-ttu-id="955ba-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="955ba-120">-ResourceGroupName</span></span>
<span data-ttu-id="955ba-121">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="955ba-121">Resource Group name.</span></span>

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

### <span data-ttu-id="955ba-122">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="955ba-122">-ServiceName</span></span>
<span data-ttu-id="955ba-123">Nazwa usługi Azure Cognitive Search.</span><span class="sxs-lookup"><span data-stu-id="955ba-123">Azure Cognitive Search Service name.</span></span>

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

### <span data-ttu-id="955ba-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="955ba-124">CommonParameters</span></span>
<span data-ttu-id="955ba-125">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="955ba-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="955ba-126">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="955ba-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="955ba-127">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="955ba-127">INPUTS</span></span>

### <span data-ttu-id="955ba-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span><span class="sxs-lookup"><span data-stu-id="955ba-128">Microsoft.Azure.Commands.Management.Search.Models.PSSearchService</span></span>

### <span data-ttu-id="955ba-129">System.String</span><span class="sxs-lookup"><span data-stu-id="955ba-129">System.String</span></span>

## <span data-ttu-id="955ba-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="955ba-130">OUTPUTS</span></span>

### <span data-ttu-id="955ba-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span><span class="sxs-lookup"><span data-stu-id="955ba-131">Microsoft.Azure.Commands.Management.Search.Models.PSSearchQueryKey</span></span>

## <span data-ttu-id="955ba-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="955ba-132">NOTES</span></span>

## <span data-ttu-id="955ba-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="955ba-133">RELATED LINKS</span></span>

[<span data-ttu-id="955ba-134">New-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="955ba-134">New-AzSearchQueryKey.md</span></span>](./New-AzSearchQueryKey.md)

[<span data-ttu-id="955ba-135">Remove-AzSearchQueryKey.md</span><span class="sxs-lookup"><span data-stu-id="955ba-135">Remove-AzSearchQueryKey.md</span></span>](./Remove-AzSearchQueryKey.md)