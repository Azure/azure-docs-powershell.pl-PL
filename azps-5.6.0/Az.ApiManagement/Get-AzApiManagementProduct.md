---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 589338afde60e069646cb677205da11e322ba7da
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012865"
---
# <span data-ttu-id="49151-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="49151-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="49151-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49151-102">SYNOPSIS</span></span>
<span data-ttu-id="49151-103">Pobiera listę lub określony produkt.</span><span class="sxs-lookup"><span data-stu-id="49151-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="49151-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="49151-104">SYNTAX</span></span>

### <span data-ttu-id="49151-105">PobierzWszystkieProdukty (domyślne)</span><span class="sxs-lookup"><span data-stu-id="49151-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="49151-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="49151-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49151-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="49151-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="49151-108">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="49151-108">GetByApiId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="49151-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="49151-109">DESCRIPTION</span></span>
<span data-ttu-id="49151-110">Polecenie **cmdlet Get-AzApiManagementProduct** pobiera listę lub określony produkt.</span><span class="sxs-lookup"><span data-stu-id="49151-110">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="49151-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="49151-111">EXAMPLES</span></span>

### <span data-ttu-id="49151-112">Przykład 1. Pobierz wszystkie produkty</span><span class="sxs-lookup"><span data-stu-id="49151-112">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="49151-113">To polecenie pobierze wszystkie produkty do zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="49151-113">This command get all API Management products.</span></span>

### <span data-ttu-id="49151-114">Przykład 2. Uzyskiwanie produktu według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="49151-114">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="49151-115">To polecenie umożliwia uzyskiwanie produktu zarządzania interfejsem API według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="49151-115">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="49151-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49151-116">PARAMETERS</span></span>

### <span data-ttu-id="49151-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="49151-117">-ApiId</span></span>
<span data-ttu-id="49151-118">ApiId interfejsu Api, aby znaleźć skorelowane produkty.</span><span class="sxs-lookup"><span data-stu-id="49151-118">ApiId of the Api to find the correlated products.</span></span> <span data-ttu-id="49151-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="49151-119">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByApiId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49151-120">— kontekst</span><span class="sxs-lookup"><span data-stu-id="49151-120">-Context</span></span>
<span data-ttu-id="49151-121">Określa wystąpienie obiektu **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="49151-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="49151-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49151-122">-DefaultProfile</span></span>
<span data-ttu-id="49151-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="49151-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49151-124">- ProductId</span><span class="sxs-lookup"><span data-stu-id="49151-124">-ProductId</span></span>
<span data-ttu-id="49151-125">Określa identyfikator produktu, który ma być wyszukiwany.</span><span class="sxs-lookup"><span data-stu-id="49151-125">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByProductId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49151-126">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="49151-126">-Title</span></span>
<span data-ttu-id="49151-127">Określa tytuł produktu, który ma być szukać.</span><span class="sxs-lookup"><span data-stu-id="49151-127">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="49151-128">Jeśli jest to określone, polecenie cmdlet próbuje uzyskać produkt według tytułu.</span><span class="sxs-lookup"><span data-stu-id="49151-128">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByTitle
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="49151-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49151-129">CommonParameters</span></span>
<span data-ttu-id="49151-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="49151-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49151-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="49151-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49151-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49151-132">INPUTS</span></span>

### <span data-ttu-id="49151-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="49151-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="49151-134">System.String</span><span class="sxs-lookup"><span data-stu-id="49151-134">System.String</span></span>

## <span data-ttu-id="49151-135">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="49151-135">OUTPUTS</span></span>

### <span data-ttu-id="49151-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="49151-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="49151-137">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="49151-137">NOTES</span></span>

## <span data-ttu-id="49151-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="49151-138">RELATED LINKS</span></span>

[<span data-ttu-id="49151-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="49151-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="49151-140">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="49151-140">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="49151-141">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="49151-141">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


