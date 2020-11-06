---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementProduct.md
ms.openlocfilehash: ab0aeb77bd5f28520e39548f539d07516cd17ac8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547252"
---
# <span data-ttu-id="7d58c-101">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7d58c-101">Get-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="7d58c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d58c-102">SYNOPSIS</span></span>
<span data-ttu-id="7d58c-103">Pobiera listę lub konkretny produkt.</span><span class="sxs-lookup"><span data-stu-id="7d58c-103">Gets a list or a particular product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d58c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d58c-104">SYNTAX</span></span>

### <span data-ttu-id="7d58c-105">Pobierz wszystkie producst (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="7d58c-105">Get all producst (Default)</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7d58c-106">Pobierz według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="7d58c-106">Get by Id</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7d58c-107">Przechodzenie według tytułu</span><span class="sxs-lookup"><span data-stu-id="7d58c-107">Get by Title</span></span>
```
Get-AzureRmApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d58c-108">Opis</span><span class="sxs-lookup"><span data-stu-id="7d58c-108">DESCRIPTION</span></span>
<span data-ttu-id="7d58c-109">Polecenie cmdlet **Get-AzureRmApiManagementProduct** pobiera listę lub konkretny produkt.</span><span class="sxs-lookup"><span data-stu-id="7d58c-109">The **Get-AzureRmApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="7d58c-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d58c-110">EXAMPLES</span></span>

### <span data-ttu-id="7d58c-111">Przykład 1. Pobierz wszystkie produkty</span><span class="sxs-lookup"><span data-stu-id="7d58c-111">Example 1: Get all products</span></span>
```
PS C:\>Get-AzureRmApiManagementProduct -Context $APImContext
```

<span data-ttu-id="7d58c-112">To polecenie umożliwia uzyskiwanie wszystkich produktów zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="7d58c-112">This command get all API Management products.</span></span>

### <span data-ttu-id="7d58c-113">Przykład 2: uzyskiwanie produktu według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="7d58c-113">Example 2: Get a product by ID</span></span>
```
PS C:\>Get-AzureRmApiManagementProduct -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="7d58c-114">To polecenie uzyskuje produkt administracyjny API według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="7d58c-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="7d58c-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d58c-115">PARAMETERS</span></span>

### <span data-ttu-id="7d58c-116">-Context</span><span class="sxs-lookup"><span data-stu-id="7d58c-116">-Context</span></span>
<span data-ttu-id="7d58c-117">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="7d58c-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="7d58c-118">-ProductId</span><span class="sxs-lookup"><span data-stu-id="7d58c-118">-ProductId</span></span>
<span data-ttu-id="7d58c-119">Określa identyfikator produktu, który ma zostać wyszukany.</span><span class="sxs-lookup"><span data-stu-id="7d58c-119">Specifies the identifier of the product to search for.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by Id
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d58c-120">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="7d58c-120">-Title</span></span>
<span data-ttu-id="7d58c-121">Określa tytuł produktu.</span><span class="sxs-lookup"><span data-stu-id="7d58c-121">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="7d58c-122">Jeśli jest określony, polecenie cmdlet próbuje uzyskać produkt według tytułu.</span><span class="sxs-lookup"><span data-stu-id="7d58c-122">If specified, the cmdlet attempts to get the product by title.</span></span>

```yaml
Type: System.String
Parameter Sets: Get by Title
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d58c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d58c-123">-DefaultProfile</span></span>
<span data-ttu-id="7d58c-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7d58c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7d58c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d58c-125">CommonParameters</span></span>
<span data-ttu-id="7d58c-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d58c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d58c-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d58c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d58c-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d58c-128">INPUTS</span></span>

## <span data-ttu-id="7d58c-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d58c-129">OUTPUTS</span></span>

### <span data-ttu-id="7d58c-130">IList<Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementProduct></span><span class="sxs-lookup"><span data-stu-id="7d58c-130">IList<Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct></span></span>

## <span data-ttu-id="7d58c-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d58c-131">NOTES</span></span>

## <span data-ttu-id="7d58c-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d58c-132">RELATED LINKS</span></span>

[<span data-ttu-id="7d58c-133">Nowe — AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7d58c-133">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="7d58c-134">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7d58c-134">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)

[<span data-ttu-id="7d58c-135">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="7d58c-135">Set-AzureRmApiManagementProduct</span></span>](./Set-AzureRmApiManagementProduct.md)


