---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: B64E9C13-97A6-4E8B-92DB-EFAF8A48C5B8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementProduct.md
ms.openlocfilehash: 9b2eb9f45f04b858e0773215ee1ed9fd98f20ff5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93704640"
---
# <span data-ttu-id="c60fe-101">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c60fe-101">Get-AzApiManagementProduct</span></span>

## <span data-ttu-id="c60fe-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c60fe-102">SYNOPSIS</span></span>
<span data-ttu-id="c60fe-103">Pobiera listę lub konkretny produkt.</span><span class="sxs-lookup"><span data-stu-id="c60fe-103">Gets a list or a particular product.</span></span>

## <span data-ttu-id="c60fe-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c60fe-104">SYNTAX</span></span>

### <span data-ttu-id="c60fe-105">GetAllProducts (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c60fe-105">GetAllProducts (Default)</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c60fe-106">GetByProductId</span><span class="sxs-lookup"><span data-stu-id="c60fe-106">GetByProductId</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c60fe-107">GetByTitle</span><span class="sxs-lookup"><span data-stu-id="c60fe-107">GetByTitle</span></span>
```
Get-AzApiManagementProduct -Context <PsApiManagementContext> [-Title <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c60fe-108">Opis</span><span class="sxs-lookup"><span data-stu-id="c60fe-108">DESCRIPTION</span></span>
<span data-ttu-id="c60fe-109">Polecenie cmdlet **Get-AzApiManagementProduct** pobiera listę lub konkretny produkt.</span><span class="sxs-lookup"><span data-stu-id="c60fe-109">The **Get-AzApiManagementProduct** cmdlet gets a list or a particular product.</span></span>

## <span data-ttu-id="c60fe-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c60fe-110">EXAMPLES</span></span>

### <span data-ttu-id="c60fe-111">Przykład 1. Pobierz wszystkie produkty</span><span class="sxs-lookup"><span data-stu-id="c60fe-111">Example 1: Get all products</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext
```

<span data-ttu-id="c60fe-112">To polecenie umożliwia uzyskiwanie wszystkich produktów zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="c60fe-112">This command get all API Management products.</span></span>

### <span data-ttu-id="c60fe-113">Przykład 2: uzyskiwanie produktu według identyfikatora</span><span class="sxs-lookup"><span data-stu-id="c60fe-113">Example 2: Get a product by ID</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementProduct -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="c60fe-114">To polecenie uzyskuje produkt administracyjny API według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="c60fe-114">This command get an API Management product by ID.</span></span>

## <span data-ttu-id="c60fe-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c60fe-115">PARAMETERS</span></span>

### <span data-ttu-id="c60fe-116">-Context</span><span class="sxs-lookup"><span data-stu-id="c60fe-116">-Context</span></span>
<span data-ttu-id="c60fe-117">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="c60fe-117">Specifies an instance of a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="c60fe-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c60fe-118">-DefaultProfile</span></span>
<span data-ttu-id="c60fe-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c60fe-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c60fe-120">-ProductId</span><span class="sxs-lookup"><span data-stu-id="c60fe-120">-ProductId</span></span>
<span data-ttu-id="c60fe-121">Określa identyfikator produktu, który ma zostać wyszukany.</span><span class="sxs-lookup"><span data-stu-id="c60fe-121">Specifies the identifier of the product to search for.</span></span>

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

### <span data-ttu-id="c60fe-122">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="c60fe-122">-Title</span></span>
<span data-ttu-id="c60fe-123">Określa tytuł produktu.</span><span class="sxs-lookup"><span data-stu-id="c60fe-123">Specifies the title of the product to look for.</span></span>
<span data-ttu-id="c60fe-124">Jeśli jest określony, polecenie cmdlet próbuje uzyskać produkt według tytułu.</span><span class="sxs-lookup"><span data-stu-id="c60fe-124">If specified, the cmdlet attempts to get the product by title.</span></span>

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

### <span data-ttu-id="c60fe-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c60fe-125">CommonParameters</span></span>
<span data-ttu-id="c60fe-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c60fe-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c60fe-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c60fe-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c60fe-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c60fe-128">INPUTS</span></span>

### <span data-ttu-id="c60fe-129">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c60fe-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c60fe-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c60fe-130">System.String</span></span>

## <span data-ttu-id="c60fe-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c60fe-131">OUTPUTS</span></span>

### <span data-ttu-id="c60fe-132">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c60fe-132">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="c60fe-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c60fe-133">NOTES</span></span>

## <span data-ttu-id="c60fe-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c60fe-134">RELATED LINKS</span></span>

[<span data-ttu-id="c60fe-135">Nowe — AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c60fe-135">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="c60fe-136">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c60fe-136">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)

[<span data-ttu-id="c60fe-137">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="c60fe-137">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


