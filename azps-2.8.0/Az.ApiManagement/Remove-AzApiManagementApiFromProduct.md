---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: 497e830ff5ee51a9b18480a4d3f31f7c51949723
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706971"
---
# <span data-ttu-id="a4115-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="a4115-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="a4115-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a4115-102">SYNOPSIS</span></span>
<span data-ttu-id="a4115-103">Usuwa interfejs API z produktu.</span><span class="sxs-lookup"><span data-stu-id="a4115-103">Removes an API from a product.</span></span>

## <span data-ttu-id="a4115-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a4115-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4115-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a4115-105">DESCRIPTION</span></span>
<span data-ttu-id="a4115-106">Polecenie cmdlet **Remove-AzApiManagementApiFromProduct** Usuwa interfejs API zarządzania interfejsem Azure API z produktu.</span><span class="sxs-lookup"><span data-stu-id="a4115-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="a4115-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a4115-107">EXAMPLES</span></span>

### <span data-ttu-id="a4115-108">Przykład 1: Usuwanie interfejsu API z produktu</span><span class="sxs-lookup"><span data-stu-id="a4115-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="a4115-109">To polecenie usuwa określony interfejs API z produktu.</span><span class="sxs-lookup"><span data-stu-id="a4115-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="a4115-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a4115-110">PARAMETERS</span></span>

### <span data-ttu-id="a4115-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a4115-111">-ApiId</span></span>
<span data-ttu-id="a4115-112">Określa identyfikator interfejsu API, który ma zostać usunięty z produktu.</span><span class="sxs-lookup"><span data-stu-id="a4115-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="a4115-113">-Context</span><span class="sxs-lookup"><span data-stu-id="a4115-113">-Context</span></span>
<span data-ttu-id="a4115-114">Określa **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="a4115-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="a4115-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4115-115">-DefaultProfile</span></span>
<span data-ttu-id="a4115-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a4115-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4115-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a4115-117">-PassThru</span></span>
<span data-ttu-id="a4115-118">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiedzie lub $False, w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="a4115-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="a4115-119">-ProductId</span><span class="sxs-lookup"><span data-stu-id="a4115-119">-ProductId</span></span>
<span data-ttu-id="a4115-120">Określa identyfikator produktu, z którego ma zostać usunięty interfejs API.</span><span class="sxs-lookup"><span data-stu-id="a4115-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="a4115-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4115-121">CommonParameters</span></span>
<span data-ttu-id="a4115-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a4115-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4115-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a4115-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4115-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a4115-124">INPUTS</span></span>

### <span data-ttu-id="a4115-125">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a4115-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a4115-126">System. String</span><span class="sxs-lookup"><span data-stu-id="a4115-126">System.String</span></span>

### <span data-ttu-id="a4115-127">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a4115-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a4115-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a4115-128">OUTPUTS</span></span>

### <span data-ttu-id="a4115-129">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="a4115-129">System.Boolean</span></span>

## <span data-ttu-id="a4115-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a4115-130">NOTES</span></span>

## <span data-ttu-id="a4115-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a4115-131">RELATED LINKS</span></span>

[<span data-ttu-id="a4115-132">Dodaj-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="a4115-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


