---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 9ad3c6b149e58bcd81ec8ce9c15ddc27fff85878
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707065"
---
# <span data-ttu-id="72433-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="72433-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="72433-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72433-102">SYNOPSIS</span></span>
<span data-ttu-id="72433-103">Pobiera listę lub konkretny produkt.</span><span class="sxs-lookup"><span data-stu-id="72433-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="72433-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72433-104">SYNTAX</span></span>

### <span data-ttu-id="72433-105">GetAllProducts (domyślny)</span><span class="sxs-lookup"><span data-stu-id="72433-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="72433-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="72433-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72433-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="72433-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="72433-108">GetByApiId</span><span class="sxs-lookup"><span data-stu-id="72433-108">GetByApiId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ApiId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="72433-109">Opis</span><span class="sxs-lookup"><span data-stu-id="72433-109">DESCRIPTION</span></span>
<span data-ttu-id="72433-110">Polecenie cmdlet **Get-AzApiManagementProduct** pobiera listę lub konkretny produkt.</span><span class="sxs-lookup"><span data-stu-id="72433-110">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="72433-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72433-111">EXAMPLES</span></span>

### <span data-ttu-id="72433-112">Przykład 1. Pobierz wszystkie produkty</span><span class="sxs-lookup"><span data-stu-id="72433-112">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="72433-113">To polecenie umożliwia uzyskiwanie wszystkich produktów zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="72433-113">This command get all API Management products.</span></span>

### <span data-ttu-id="72433-114">Przykład 2: uzyskiwanie produktu według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="72433-114">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="72433-115">To polecenie uzyskuje produkt administracyjny API według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="72433-115">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="72433-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72433-116">PARAMETERS</span></span>

### <span data-ttu-id="72433-117">-ApiId</span><span class="sxs-lookup"><span data-stu-id="72433-117">-ApiId</span></span>
<span data-ttu-id="72433-118">ApiId interfejs API, aby znaleźć produkty skorelowane.</span><span class="sxs-lookup"><span data-stu-id="72433-118">ApiId of the Api to find the correlated products.</span></span> <span data-ttu-id="72433-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="72433-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="72433-120">-Context</span><span class="sxs-lookup"><span data-stu-id="72433-120">-Context</span></span>
<span data-ttu-id="72433-121">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="72433-121">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="72433-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72433-122">-DefaultProfile</span></span>
<span data-ttu-id="72433-123">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="72433-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="72433-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="72433-124">-ProductId</span></span>
<span data-ttu-id="72433-125">Określa identyfikator produktu, który ma zostać wyszukany.</span><span class="sxs-lookup"><span data-stu-id="72433-125">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="72433-126">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="72433-126">-Title</span></span>
<span data-ttu-id="72433-127">Określa tytuł produktu.</span><span class="sxs-lookup"><span data-stu-id="72433-127">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="72433-128">Jeśli jest określony, polecenie cmdlet próbuje uzyskać produkt według tytułu.</span><span class="sxs-lookup"><span data-stu-id="72433-128">If specified, the cmdlet attempts to get the product by title.</span></span>

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

### <span data-ttu-id="72433-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72433-129">CommonParameters</span></span>
<span data-ttu-id="72433-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72433-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72433-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72433-131">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72433-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72433-132">INPUTS</span></span>

### <span data-ttu-id="72433-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="72433-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="72433-134">System. String</span><span class="sxs-lookup"><span data-stu-id="72433-134">System.String</span></span>

## <span data-ttu-id="72433-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72433-135">OUTPUTS</span></span>

### <span data-ttu-id="72433-136">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="72433-136">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="72433-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72433-137">NOTES</span></span>

## <span data-ttu-id="72433-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72433-138">RELATED LINKS</span></span>

[<span data-ttu-id="72433-139">Nowe — AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="72433-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="72433-140">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="72433-140">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="72433-141">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="72433-141">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)

