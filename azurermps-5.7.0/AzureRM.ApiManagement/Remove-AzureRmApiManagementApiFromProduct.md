---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementApiFromProduct.md
ms.openlocfilehash: 413d03723ee2acdc162c1f1f5501d90156e16069
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553710"
---
# <span data-ttu-id="02f81-101">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="02f81-101">Remove-AzureRmApiManagementApiFromProduct</span></span>

## <span data-ttu-id="02f81-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="02f81-102">SYNOPSIS</span></span>
<span data-ttu-id="02f81-103">Usuwa interfejs API z produktu.</span><span class="sxs-lookup"><span data-stu-id="02f81-103">Removes an API from a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02f81-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="02f81-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="02f81-105">Opis</span><span class="sxs-lookup"><span data-stu-id="02f81-105">DESCRIPTION</span></span>
<span data-ttu-id="02f81-106">Polecenie cmdlet **Remove-AzureRmApiManagementApiFromProduct** Usuwa interfejs API zarządzania interfejsem Azure API z produktu.</span><span class="sxs-lookup"><span data-stu-id="02f81-106">The **Remove-AzureRmApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="02f81-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="02f81-107">EXAMPLES</span></span>

### <span data-ttu-id="02f81-108">Przykład 1: Usuwanie interfejsu API z produktu</span><span class="sxs-lookup"><span data-stu-id="02f81-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="02f81-109">Ten commnd usuwa określony interfejs API z produktu.</span><span class="sxs-lookup"><span data-stu-id="02f81-109">This commnd removes the specified API from a product.</span></span>

## <span data-ttu-id="02f81-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="02f81-110">PARAMETERS</span></span>

### <span data-ttu-id="02f81-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="02f81-111">-ApiId</span></span>
<span data-ttu-id="02f81-112">Określa identyfikator interfejsu API, który ma zostać usunięty z produktu.</span><span class="sxs-lookup"><span data-stu-id="02f81-112">Specifies the ID of the API to remove from the product.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02f81-113">-Context</span><span class="sxs-lookup"><span data-stu-id="02f81-113">-Context</span></span>
<span data-ttu-id="02f81-114">Określa **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="02f81-114">Specifies a **PsApiManagementContext**.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02f81-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02f81-115">-DefaultProfile</span></span>
<span data-ttu-id="02f81-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="02f81-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02f81-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02f81-117">-PassThru</span></span>
<span data-ttu-id="02f81-118">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiedzie lub $False, w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="02f81-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02f81-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="02f81-119">-ProductId</span></span>
<span data-ttu-id="02f81-120">Określa identyfikator produktu, z którego ma zostać usunięty interfejs API.</span><span class="sxs-lookup"><span data-stu-id="02f81-120">Specifies the ID of the product from which to remove the API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02f81-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02f81-121">CommonParameters</span></span>
<span data-ttu-id="02f81-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02f81-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02f81-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02f81-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02f81-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="02f81-124">INPUTS</span></span>

### <span data-ttu-id="02f81-125">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="02f81-125">None</span></span>
<span data-ttu-id="02f81-126">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="02f81-126">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="02f81-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="02f81-127">OUTPUTS</span></span>

### <span data-ttu-id="02f81-128">logiczną</span><span class="sxs-lookup"><span data-stu-id="02f81-128">bool</span></span>

## <span data-ttu-id="02f81-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="02f81-129">NOTES</span></span>

## <span data-ttu-id="02f81-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="02f81-130">RELATED LINKS</span></span>

[<span data-ttu-id="02f81-131">Dodaj-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="02f81-131">Add-AzureRmApiManagementApiToProduct</span></span>](./Add-AzureRmApiManagementApiToProduct.md)


