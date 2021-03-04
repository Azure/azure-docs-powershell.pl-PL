---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2457C7F5-7FB9-4712-AD7C-438E88F591A8
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementapifromproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementApiFromProduct.md
ms.openlocfilehash: af83bb3d6daa11eb62de81378e4e7d3e040b2db4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959050"
---
# <span data-ttu-id="bd7b3-101">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="bd7b3-101">Remove-AzApiManagementApiFromProduct</span></span>

## <span data-ttu-id="bd7b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd7b3-102">SYNOPSIS</span></span>
<span data-ttu-id="bd7b3-103">Usuwa interfejs API z produktu.</span><span class="sxs-lookup"><span data-stu-id="bd7b3-103">Removes an API from a product.</span></span>

## <span data-ttu-id="bd7b3-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="bd7b3-104">SYNTAX</span></span>

```
Remove-AzApiManagementApiFromProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd7b3-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="bd7b3-105">DESCRIPTION</span></span>
<span data-ttu-id="bd7b3-106">Polecenie **cmdlet Remove-AzApiManagementApiFromProduct** usuwa z produktu interfejs API zarządzania interfejsem Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="bd7b3-106">The **Remove-AzApiManagementApiFromProduct** cmdlet removes an Azure API Management API from a product.</span></span>

## <span data-ttu-id="bd7b3-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="bd7b3-107">EXAMPLES</span></span>

### <span data-ttu-id="bd7b3-108">Przykład 1. Usuwanie interfejsu API z produktu</span><span class="sxs-lookup"><span data-stu-id="bd7b3-108">Example 1: Remove an API from a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementApiFromProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001" -PassThru
```

<span data-ttu-id="bd7b3-109">To polecenie usuwa określony interfejs API z produktu.</span><span class="sxs-lookup"><span data-stu-id="bd7b3-109">This command removes the specified API from a product.</span></span>

## <span data-ttu-id="bd7b3-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bd7b3-110">PARAMETERS</span></span>

### <span data-ttu-id="bd7b3-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="bd7b3-111">-ApiId</span></span>
<span data-ttu-id="bd7b3-112">Określa identyfikator interfejsu API do usunięcia z produktu.</span><span class="sxs-lookup"><span data-stu-id="bd7b3-112">Specifies the ID of the API to remove from the product.</span></span>

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

### <span data-ttu-id="bd7b3-113">— kontekst</span><span class="sxs-lookup"><span data-stu-id="bd7b3-113">-Context</span></span>
<span data-ttu-id="bd7b3-114">Określa tekst **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="bd7b3-114">Specifies a **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="bd7b3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd7b3-115">-DefaultProfile</span></span>
<span data-ttu-id="bd7b3-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd7b3-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd7b3-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="bd7b3-117">-PassThru</span></span>
<span data-ttu-id="bd7b3-118">Wskazuje, że to polecenie cmdlet zwraca wartość $True się powiedzie lub $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="bd7b3-118">Indicates that this cmdlet returns a value of $True if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="bd7b3-119">- ProductId</span><span class="sxs-lookup"><span data-stu-id="bd7b3-119">-ProductId</span></span>
<span data-ttu-id="bd7b3-120">Określa identyfikator produktu, z którego ma być usuwany interfejs API.</span><span class="sxs-lookup"><span data-stu-id="bd7b3-120">Specifies the ID of the product from which to remove the API.</span></span>

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

### <span data-ttu-id="bd7b3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd7b3-121">CommonParameters</span></span>
<span data-ttu-id="bd7b3-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd7b3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd7b3-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd7b3-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd7b3-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd7b3-124">INPUTS</span></span>

### <span data-ttu-id="bd7b3-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="bd7b3-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="bd7b3-126">System.String</span><span class="sxs-lookup"><span data-stu-id="bd7b3-126">System.String</span></span>

### <span data-ttu-id="bd7b3-127">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="bd7b3-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="bd7b3-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd7b3-128">OUTPUTS</span></span>

### <span data-ttu-id="bd7b3-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="bd7b3-129">System.Boolean</span></span>

## <span data-ttu-id="bd7b3-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="bd7b3-130">NOTES</span></span>

## <span data-ttu-id="bd7b3-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd7b3-131">RELATED LINKS</span></span>

[<span data-ttu-id="bd7b3-132">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="bd7b3-132">Add-AzApiManagementApiToProduct</span></span>](./Add-AzApiManagementApiToProduct.md)


