---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: 748dc399c68a299ef0d567fbd65ec7154061869c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954906"
---
# <span data-ttu-id="9deaf-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="9deaf-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="9deaf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9deaf-102">SYNOPSIS</span></span>
<span data-ttu-id="9deaf-103">Dodaje produkt do grupy.</span><span class="sxs-lookup"><span data-stu-id="9deaf-103">Adds a product to a group.</span></span>

## <span data-ttu-id="9deaf-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="9deaf-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9deaf-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="9deaf-105">DESCRIPTION</span></span>
<span data-ttu-id="9deaf-106">Polecenie **cmdlet Add-AzApiManagementProductToGroup** dodaje produkt do istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="9deaf-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="9deaf-107">Innymi słowy to polecenie cmdlet przypisuje grupę do produktu.</span><span class="sxs-lookup"><span data-stu-id="9deaf-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="9deaf-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="9deaf-108">EXAMPLES</span></span>

### <span data-ttu-id="9deaf-109">Przykład 1. Dodawanie produktu do grupy</span><span class="sxs-lookup"><span data-stu-id="9deaf-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="9deaf-110">To polecenie powoduje dodanie produktu do istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="9deaf-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="9deaf-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9deaf-111">PARAMETERS</span></span>

### <span data-ttu-id="9deaf-112">— kontekst</span><span class="sxs-lookup"><span data-stu-id="9deaf-112">-Context</span></span>
<span data-ttu-id="9deaf-113">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="9deaf-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="9deaf-114">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9deaf-114">This parameter is required.</span></span>

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

### <span data-ttu-id="9deaf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9deaf-115">-DefaultProfile</span></span>
<span data-ttu-id="9deaf-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="9deaf-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9deaf-117">- GroupId</span><span class="sxs-lookup"><span data-stu-id="9deaf-117">-GroupId</span></span>
<span data-ttu-id="9deaf-118">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="9deaf-118">Specifies the group ID.</span></span>
<span data-ttu-id="9deaf-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9deaf-119">This parameter is required.</span></span>

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

### <span data-ttu-id="9deaf-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9deaf-120">-PassThru</span></span>
<span data-ttu-id="9deaf-121">passthru</span><span class="sxs-lookup"><span data-stu-id="9deaf-121">passthru</span></span>

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

### <span data-ttu-id="9deaf-122">- ProductId</span><span class="sxs-lookup"><span data-stu-id="9deaf-122">-ProductId</span></span>
<span data-ttu-id="9deaf-123">Określa identyfikator produktu.</span><span class="sxs-lookup"><span data-stu-id="9deaf-123">Specifies the product ID.</span></span>
<span data-ttu-id="9deaf-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="9deaf-124">This parameter is required.</span></span>

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

### <span data-ttu-id="9deaf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9deaf-125">CommonParameters</span></span>
<span data-ttu-id="9deaf-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9deaf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9deaf-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9deaf-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9deaf-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9deaf-128">INPUTS</span></span>

### <span data-ttu-id="9deaf-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9deaf-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9deaf-130">System.String</span><span class="sxs-lookup"><span data-stu-id="9deaf-130">System.String</span></span>

### <span data-ttu-id="9deaf-131">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="9deaf-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9deaf-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9deaf-132">OUTPUTS</span></span>

### <span data-ttu-id="9deaf-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9deaf-133">System.Boolean</span></span>

## <span data-ttu-id="9deaf-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="9deaf-134">NOTES</span></span>

## <span data-ttu-id="9deaf-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9deaf-135">RELATED LINKS</span></span>

[<span data-ttu-id="9deaf-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="9deaf-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


