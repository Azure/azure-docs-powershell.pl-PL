---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: 10b17f60ae100004c23a16f341924de6de11b0eb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524749"
---
# <span data-ttu-id="4bb22-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4bb22-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="4bb22-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4bb22-102">SYNOPSIS</span></span>
<span data-ttu-id="4bb22-103">Pobiera listę lub konkretny produkt.</span><span class="sxs-lookup"><span data-stu-id="4bb22-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4bb22-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4bb22-104">SYNTAX</span></span>

### <span data-ttu-id="4bb22-105">GetAllProducts (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4bb22-105">GetAllProducts (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4bb22-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="4bb22-106">GetByProductId</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4bb22-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="4bb22-107">GetByTitle</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4bb22-108">Opis</span><span class="sxs-lookup"><span data-stu-id="4bb22-108">DESCRIPTION</span></span>
<span data-ttu-id="4bb22-109">Polecenie cmdlet **Get-AzureRmApiManagementProduct** pobiera listę lub konkretny produkt.</span><span class="sxs-lookup"><span data-stu-id="4bb22-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="4bb22-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4bb22-110">EXAMPLES</span></span>

### <span data-ttu-id="4bb22-111">Przykład 1. Pobierz wszystkie produkty</span><span class="sxs-lookup"><span data-stu-id="4bb22-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext
```

<span data-ttu-id="4bb22-112">To polecenie umożliwia uzyskiwanie wszystkich produktów zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="4bb22-112">This command get all API Management products.</span></span>

### <span data-ttu-id="4bb22-113">Przykład 2: uzyskiwanie produktu według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="4bb22-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="4bb22-114">To polecenie uzyskuje produkt administracyjny API według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="4bb22-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="4bb22-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4bb22-115">PARAMETERS</span></span>

### <span data-ttu-id="4bb22-116">-Context</span><span class="sxs-lookup"><span data-stu-id="4bb22-116">-Context</span></span>
<span data-ttu-id="4bb22-117">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4bb22-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4bb22-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4bb22-118">-DefaultProfile</span></span>
<span data-ttu-id="4bb22-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4bb22-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4bb22-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="4bb22-120">-ProductId</span></span>
<span data-ttu-id="4bb22-121">Określa identyfikator produktu, który ma zostać wyszukany.</span><span class="sxs-lookup"><span data-stu-id="4bb22-121">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="4bb22-122">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="4bb22-122">-Title</span></span>
<span data-ttu-id="4bb22-123">Określa tytuł produktu.</span><span class="sxs-lookup"><span data-stu-id="4bb22-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="4bb22-124">Jeśli jest określony, polecenie cmdlet próbuje uzyskać produkt według tytułu.</span><span class="sxs-lookup"><span data-stu-id="4bb22-124">If specified, the cmdlet attempts to get the product by title.</span></span>

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

### <span data-ttu-id="4bb22-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4bb22-125">CommonParameters</span></span>
<span data-ttu-id="4bb22-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4bb22-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4bb22-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4bb22-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4bb22-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4bb22-128">INPUTS</span></span>

### <span data-ttu-id="4bb22-129">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4bb22-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4bb22-130">System. String</span><span class="sxs-lookup"><span data-stu-id="4bb22-130">System.String</span></span>

## <span data-ttu-id="4bb22-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4bb22-131">OUTPUTS</span></span>

### <span data-ttu-id="4bb22-132">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4bb22-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="4bb22-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4bb22-133">NOTES</span></span>

## <span data-ttu-id="4bb22-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4bb22-134">RELATED LINKS</span></span>

[<span data-ttu-id="4bb22-135">Nowe — AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4bb22-135">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="4bb22-136">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4bb22-136">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="4bb22-137">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="4bb22-137">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


