---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
ms.openlocfilehash: d5c9061921f6ab345a027eeec69b4d6cd7230211
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717885"
---
# <span data-ttu-id="02cda-101">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="02cda-101">Add-AzureRmApiManagementApiToProduct</span></span>

## <span data-ttu-id="02cda-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02cda-102">SYNOPSIS</span></span>
<span data-ttu-id="02cda-103">Dodaje interfejs API do produktu.</span><span class="sxs-lookup"><span data-stu-id="02cda-103">Adds an API to a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02cda-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02cda-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02cda-105">Opis</span><span class="sxs-lookup"><span data-stu-id="02cda-105">DESCRIPTION</span></span>
<span data-ttu-id="02cda-106">Polecenie cmdlet **Add-AzureRmApiManagementApiToProduct** umożliwia dodanie interfejsu API zarządzania interfejsem Azure API do produktu.</span><span class="sxs-lookup"><span data-stu-id="02cda-106">The **Add-AzureRmApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="02cda-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02cda-107">EXAMPLES</span></span>

### <span data-ttu-id="02cda-108">Przykład 1: Dodawanie interfejsu API do produktu</span><span class="sxs-lookup"><span data-stu-id="02cda-108">Example 1: Add an API to a product</span></span>
```
PS C:\>Add-AzureRmApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="02cda-109">To polecenie umożliwia dodanie określonego interfejsu API do określonego produktu.</span><span class="sxs-lookup"><span data-stu-id="02cda-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="02cda-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02cda-110">PARAMETERS</span></span>

### <span data-ttu-id="02cda-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="02cda-111">-ApiId</span></span>
<span data-ttu-id="02cda-112">Określa identyfikator interfejsu API, który ma zostać dodany do produktu.</span><span class="sxs-lookup"><span data-stu-id="02cda-112">Specifies the ID of an API to add to a product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02cda-113">-Context</span><span class="sxs-lookup"><span data-stu-id="02cda-113">-Context</span></span>
<span data-ttu-id="02cda-114">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="02cda-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="02cda-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02cda-115">-PassThru</span></span>
<span data-ttu-id="02cda-116">passthru</span><span class="sxs-lookup"><span data-stu-id="02cda-116">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02cda-117">-ProductId</span><span class="sxs-lookup"><span data-stu-id="02cda-117">-ProductId</span></span>
<span data-ttu-id="02cda-118">Określa identyfikator produktu, do którego ma zostać dodany interfejs API.</span><span class="sxs-lookup"><span data-stu-id="02cda-118">Specifies the ID of the product to which to add the API.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02cda-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02cda-119">-DefaultProfile</span></span>
<span data-ttu-id="02cda-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02cda-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02cda-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02cda-121">CommonParameters</span></span>
<span data-ttu-id="02cda-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02cda-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02cda-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02cda-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02cda-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02cda-124">INPUTS</span></span>

## <span data-ttu-id="02cda-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02cda-125">OUTPUTS</span></span>

### <span data-ttu-id="02cda-126">Wartość</span><span class="sxs-lookup"><span data-stu-id="02cda-126">Boolean</span></span>

## <span data-ttu-id="02cda-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02cda-127">NOTES</span></span>

## <span data-ttu-id="02cda-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02cda-128">RELATED LINKS</span></span>

[<span data-ttu-id="02cda-129">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="02cda-129">Remove-AzureRmApiManagementApiFromProduct</span></span>](./Remove-AzureRmApiManagementApiFromProduct.md)


