---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 7C86B385-D784-45FD-9B57-31C895115A2C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementapitoproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementApiToProduct.md
ms.openlocfilehash: 01767d80f0925647b2161dd26f504465d7f1d8e1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239914"
---
# <span data-ttu-id="d8b2e-101">Add-AzApiManagementApiToProduct</span><span class="sxs-lookup"><span data-stu-id="d8b2e-101">Add-AzApiManagementApiToProduct</span></span>

## <span data-ttu-id="d8b2e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8b2e-102">SYNOPSIS</span></span>
<span data-ttu-id="d8b2e-103">Dodaje interfejs API do produktu.</span><span class="sxs-lookup"><span data-stu-id="d8b2e-103">Adds an API to a product.</span></span>

## <span data-ttu-id="d8b2e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d8b2e-104">SYNTAX</span></span>

```
Add-AzApiManagementApiToProduct -Context <PsApiManagementContext> -ProductId <String> -ApiId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8b2e-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d8b2e-105">DESCRIPTION</span></span>
<span data-ttu-id="d8b2e-106">Polecenie **cmdlet Add-AzApiManagementApiToProduct** dodaje interfejs API zarządzania interfejsem Azure API do produktu.</span><span class="sxs-lookup"><span data-stu-id="d8b2e-106">The **Add-AzApiManagementApiToProduct** cmdlet adds an Azure API Management API to a product.</span></span>

## <span data-ttu-id="d8b2e-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d8b2e-107">EXAMPLES</span></span>

### <span data-ttu-id="d8b2e-108">Przykład 1. Dodawanie interfejsu API do produktu</span><span class="sxs-lookup"><span data-stu-id="d8b2e-108">Example 1: Add an API to a product</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementApiToProduct -Context $ApiMgmtContext -ProductId "0123456789" -ApiId "0001"
```

<span data-ttu-id="d8b2e-109">To polecenie dodaje określony interfejs API do określonego produktu.</span><span class="sxs-lookup"><span data-stu-id="d8b2e-109">This command adds the specified API to the specified product.</span></span>

## <span data-ttu-id="d8b2e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d8b2e-110">PARAMETERS</span></span>

### <span data-ttu-id="d8b2e-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="d8b2e-111">-ApiId</span></span>
<span data-ttu-id="d8b2e-112">Określa identyfikator interfejsu API do dodania do produktu.</span><span class="sxs-lookup"><span data-stu-id="d8b2e-112">Specifies the ID of an API to add to a product.</span></span>

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

### <span data-ttu-id="d8b2e-113">— kontekst</span><span class="sxs-lookup"><span data-stu-id="d8b2e-113">-Context</span></span>
<span data-ttu-id="d8b2e-114">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="d8b2e-114">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="d8b2e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8b2e-115">-DefaultProfile</span></span>
<span data-ttu-id="d8b2e-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d8b2e-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d8b2e-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d8b2e-117">-PassThru</span></span>
<span data-ttu-id="d8b2e-118">passthru</span><span class="sxs-lookup"><span data-stu-id="d8b2e-118">passthru</span></span>

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

### <span data-ttu-id="d8b2e-119">- ProductId</span><span class="sxs-lookup"><span data-stu-id="d8b2e-119">-ProductId</span></span>
<span data-ttu-id="d8b2e-120">Określa identyfikator produktu, do którego ma być dodać interfejs API.</span><span class="sxs-lookup"><span data-stu-id="d8b2e-120">Specifies the ID of the product to which to add the API.</span></span>

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

### <span data-ttu-id="d8b2e-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8b2e-121">CommonParameters</span></span>
<span data-ttu-id="d8b2e-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d8b2e-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8b2e-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d8b2e-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8b2e-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8b2e-124">INPUTS</span></span>

### <span data-ttu-id="d8b2e-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="d8b2e-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="d8b2e-126">System.String</span><span class="sxs-lookup"><span data-stu-id="d8b2e-126">System.String</span></span>

### <span data-ttu-id="d8b2e-127">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="d8b2e-127">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="d8b2e-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d8b2e-128">OUTPUTS</span></span>

### <span data-ttu-id="d8b2e-129">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="d8b2e-129">System.Boolean</span></span>

## <span data-ttu-id="d8b2e-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d8b2e-130">NOTES</span></span>

## <span data-ttu-id="d8b2e-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d8b2e-131">RELATED LINKS</span></span>

[<span data-ttu-id="d8b2e-132">Remove-AzApiManagementApiFromProduct</span><span class="sxs-lookup"><span data-stu-id="d8b2e-132">Remove-AzApiManagementApiFromProduct</span></span>](./Remove-AzApiManagementApiFromProduct.md)


