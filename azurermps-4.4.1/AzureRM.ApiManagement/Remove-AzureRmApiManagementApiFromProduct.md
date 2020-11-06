---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
ms.openlocfilehash: 957a2fbecc588f9b04400571e587c6ba56e16df5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525786"
---
# <span data-ttu-id="fa832-101">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="fa832-101">Remove-AzureRmApiManagementApiFromProduct</span></span>

## <span data-ttu-id="fa832-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fa832-102">SYNOPSIS</span></span>
<span data-ttu-id="fa832-103">Usuwa interfejs API z produktu.</span><span class="sxs-lookup"><span data-stu-id="fa832-103">Removes an API from a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa832-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fa832-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa832-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fa832-105">DESCRIPTION</span></span>
<span data-ttu-id="fa832-106">Polecenie cmdlet **Remove-AzureRmApiManagementApiFromProduct** Usuwa interfejs API zarządzania interfejsem Azure API z produktu.</span><span class="sxs-lookup"><span data-stu-id="fa832-106">The **Remove-AzureRmApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="fa832-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fa832-107">EXAMPLES</span></span>

### <span data-ttu-id="fa832-108">Przykład 1: Usuwanie interfejsu API z produktu</span><span class="sxs-lookup"><span data-stu-id="fa832-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>Remove-AzureRmApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="fa832-109">Ten commnd usuwa określony interfejs API z produktu.</span><span class="sxs-lookup"><span data-stu-id="fa832-109">This commnd removes the specified API from a product.</span></span>

## <span data-ttu-id="fa832-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fa832-110">PARAMETERS</span></span>

### <span data-ttu-id="fa832-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="fa832-111">-ApiId</span></span>
<span data-ttu-id="fa832-112">Określa identyfikator interfejsu API, który ma zostać usunięty z produktu.</span><span class="sxs-lookup"><span data-stu-id="fa832-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="fa832-113">-Context</span><span class="sxs-lookup"><span data-stu-id="fa832-113">-Context</span></span>
<span data-ttu-id="fa832-114">Określa **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="fa832-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="fa832-115">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fa832-115">-PassThru</span></span>
<span data-ttu-id="fa832-116">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiedzie lub $False, w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="fa832-116">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="fa832-117">-ProductId</span><span class="sxs-lookup"><span data-stu-id="fa832-117">-ProductId</span></span>
<span data-ttu-id="fa832-118">Określa identyfikator produktu, z którego ma zostać usunięty interfejs API.</span><span class="sxs-lookup"><span data-stu-id="fa832-118">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="fa832-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa832-119">-DefaultProfile</span></span>
<span data-ttu-id="fa832-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fa832-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa832-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa832-121">CommonParameters</span></span>
<span data-ttu-id="fa832-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa832-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa832-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa832-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa832-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa832-124">INPUTS</span></span>

## <span data-ttu-id="fa832-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fa832-125">OUTPUTS</span></span>

### <span data-ttu-id="fa832-126">logiczną</span><span class="sxs-lookup"><span data-stu-id="fa832-126">bool</span></span>

## <span data-ttu-id="fa832-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fa832-127">NOTES</span></span>

## <span data-ttu-id="fa832-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa832-128">RELATED LINKS</span></span>

[<span data-ttu-id="fa832-129">Dodaj-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="fa832-129">Add-AzureRmApiManagementApiToProduct</span></span>](./Add-AzureRmApiManagementApiToProduct.md)


