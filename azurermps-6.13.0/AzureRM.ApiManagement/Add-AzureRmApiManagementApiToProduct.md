---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/add-azurermapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Add-AzureRmApiManagementApiToProduct.md
ms.openlocfilehash: 16bb651efd13d42b25509834637faea866678459
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718395"
---
# <span data-ttu-id="77d66-101">Add-AzureRmApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="77d66-101">Add-AzureRmApiManagementApiToProduct</span></span>

## <span data-ttu-id="77d66-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77d66-102">SYNOPSIS</span></span>
<span data-ttu-id="77d66-103">Dodaje interfejs API do produktu.</span><span class="sxs-lookup"><span data-stu-id="77d66-103">Adds an API to a product.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77d66-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77d66-104">SYNTAX</span></span>

```
Add-AzureRmApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77d66-105">Opis</span><span class="sxs-lookup"><span data-stu-id="77d66-105">DESCRIPTION</span></span>
<span data-ttu-id="77d66-106">Polecenie cmdlet **Add-AzureRmApiManagementApiToProduct** umożliwia dodanie interfejsu API zarządzania interfejsem Azure API do produktu.</span><span class="sxs-lookup"><span data-stu-id="77d66-106">The **Add-AzureRmApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="77d66-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77d66-107">EXAMPLES</span></span>

### <span data-ttu-id="77d66-108">Przykład 1: Dodawanie interfejsu API do produktu</span><span class="sxs-lookup"><span data-stu-id="77d66-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzureRmApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="77d66-109">To polecenie umożliwia dodanie określonego interfejsu API do określonego produktu.</span><span class="sxs-lookup"><span data-stu-id="77d66-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="77d66-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77d66-110">PARAMETERS</span></span>

### <span data-ttu-id="77d66-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="77d66-111">-ApiId</span></span>
<span data-ttu-id="77d66-112">Określa identyfikator interfejsu API, który ma zostać dodany do produktu.</span><span class="sxs-lookup"><span data-stu-id="77d66-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="77d66-113">-Context</span><span class="sxs-lookup"><span data-stu-id="77d66-113">-Context</span></span>
<span data-ttu-id="77d66-114">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="77d66-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="77d66-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77d66-115">-DefaultProfile</span></span>
<span data-ttu-id="77d66-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77d66-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77d66-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77d66-117">-PassThru</span></span>
<span data-ttu-id="77d66-118">passthru</span><span class="sxs-lookup"><span data-stu-id="77d66-118">passthru</span></span>

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

### <span data-ttu-id="77d66-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="77d66-119">-ProductId</span></span>
<span data-ttu-id="77d66-120">Określa identyfikator produktu, do którego ma zostać dodany interfejs API.</span><span class="sxs-lookup"><span data-stu-id="77d66-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="77d66-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77d66-121">CommonParameters</span></span>
<span data-ttu-id="77d66-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77d66-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77d66-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77d66-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77d66-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77d66-124">INPUTS</span></span>

### <span data-ttu-id="77d66-125">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="77d66-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="77d66-126">System. String</span><span class="sxs-lookup"><span data-stu-id="77d66-126">System.String</span></span>

### <span data-ttu-id="77d66-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="77d66-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="77d66-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77d66-128">OUTPUTS</span></span>

### <span data-ttu-id="77d66-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="77d66-129">System.Boolean</span></span>

## <span data-ttu-id="77d66-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77d66-130">NOTES</span></span>

## <span data-ttu-id="77d66-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77d66-131">RELATED LINKS</span></span>

[<span data-ttu-id="77d66-132">Remove-AzureRmApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="77d66-132">Remove-AzureRmApiManagementApiFromProduct</span></span>](./Remove-AzureRmApiManagementApiFromProduct.md)


