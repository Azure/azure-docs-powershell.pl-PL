---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: fd9e4cec821b08c9ac2bbd5cd2ac43e5e5b114ba
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051870"
---
# <span data-ttu-id="5b45b-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="5b45b-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="5b45b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5b45b-102">SYNOPSIS</span></span>
<span data-ttu-id="5b45b-103">Usuwa interfejs API z produktu.</span><span class="sxs-lookup"><span data-stu-id="5b45b-103">Removes an API from a product.</span></span>

## <span data-ttu-id="5b45b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5b45b-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5b45b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5b45b-105">DESCRIPTION</span></span>
<span data-ttu-id="5b45b-106">Polecenie cmdlet **Remove-AzApiManagementApiFromProduct** Usuwa interfejs API zarządzania interfejsem Azure API z produktu.</span><span class="sxs-lookup"><span data-stu-id="5b45b-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="5b45b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5b45b-107">EXAMPLES</span></span>

### <span data-ttu-id="5b45b-108">Przykład 1: Usuwanie interfejsu API z produktu</span><span class="sxs-lookup"><span data-stu-id="5b45b-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="5b45b-109">To polecenie usuwa określony interfejs API z produktu.</span><span class="sxs-lookup"><span data-stu-id="5b45b-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="5b45b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5b45b-110">PARAMETERS</span></span>

### <span data-ttu-id="5b45b-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="5b45b-111">-ApiId</span></span>
<span data-ttu-id="5b45b-112">Określa identyfikator interfejsu API, który ma zostać usunięty z produktu.</span><span class="sxs-lookup"><span data-stu-id="5b45b-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="5b45b-113">-Context</span><span class="sxs-lookup"><span data-stu-id="5b45b-113">-Context</span></span>
<span data-ttu-id="5b45b-114">Określa **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="5b45b-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="5b45b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b45b-115">-DefaultProfile</span></span>
<span data-ttu-id="5b45b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5b45b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5b45b-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5b45b-117">-PassThru</span></span>
<span data-ttu-id="5b45b-118">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiedzie lub $False, w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="5b45b-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="5b45b-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="5b45b-119">-ProductId</span></span>
<span data-ttu-id="5b45b-120">Określa identyfikator produktu, z którego ma zostać usunięty interfejs API.</span><span class="sxs-lookup"><span data-stu-id="5b45b-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="5b45b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b45b-121">CommonParameters</span></span>
<span data-ttu-id="5b45b-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5b45b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b45b-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="5b45b-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b45b-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5b45b-124">INPUTS</span></span>

### <span data-ttu-id="5b45b-125">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="5b45b-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="5b45b-126">System. String</span><span class="sxs-lookup"><span data-stu-id="5b45b-126">System.String</span></span>

### <span data-ttu-id="5b45b-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="5b45b-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="5b45b-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5b45b-128">OUTPUTS</span></span>

### <span data-ttu-id="5b45b-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5b45b-129">System.Boolean</span></span>

## <span data-ttu-id="5b45b-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5b45b-130">NOTES</span></span>

## <span data-ttu-id="5b45b-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5b45b-131">RELATED LINKS</span></span>

[<span data-ttu-id="5b45b-132">Dodaj-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="5b45b-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


