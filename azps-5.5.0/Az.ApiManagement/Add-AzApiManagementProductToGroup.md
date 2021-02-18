---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 1058BA4E-CD79-429D-BB05-422AE39230C4
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/add-azapimanagementproducttogroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Add-AzApiManagementProductToGroup.md
ms.openlocfilehash: a92387392c540c75cfa96ecaf4c4acf026ade9f5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239907"
---
# <span data-ttu-id="f00db-101">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="f00db-101">Add-AzApiManagementProductToGroup</span></span>

## <span data-ttu-id="f00db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f00db-102">SYNOPSIS</span></span>
<span data-ttu-id="f00db-103">Dodaje produkt do grupy.</span><span class="sxs-lookup"><span data-stu-id="f00db-103">Adds a product to a group.</span></span>

## <span data-ttu-id="f00db-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f00db-104">SYNTAX</span></span>

```
Add-AzApiManagementProductToGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f00db-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f00db-105">DESCRIPTION</span></span>
<span data-ttu-id="f00db-106">Polecenie **cmdlet Add-AzApiManagementProductToGroup** dodaje produkt do istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="f00db-106">The **Add-AzApiManagementProductToGroup** cmdlet adds a product to an existing group.</span></span>
<span data-ttu-id="f00db-107">Innymi słowy to polecenie cmdlet przypisuje grupę do produktu.</span><span class="sxs-lookup"><span data-stu-id="f00db-107">In other words, this cmdlet assigns a group to a product.</span></span>

## <span data-ttu-id="f00db-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f00db-108">EXAMPLES</span></span>

### <span data-ttu-id="f00db-109">Przykład 1. Dodawanie produktu do grupy</span><span class="sxs-lookup"><span data-stu-id="f00db-109">Example 1: Add a product to a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Add-AzApiManagementProductToGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="f00db-110">To polecenie powoduje dodanie produktu do istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="f00db-110">This command adds a product to an existing group.</span></span>

## <span data-ttu-id="f00db-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f00db-111">PARAMETERS</span></span>

### <span data-ttu-id="f00db-112">— kontekst</span><span class="sxs-lookup"><span data-stu-id="f00db-112">-Context</span></span>
<span data-ttu-id="f00db-113">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="f00db-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f00db-114">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f00db-114">This parameter is required.</span></span>

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

### <span data-ttu-id="f00db-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f00db-115">-DefaultProfile</span></span>
<span data-ttu-id="f00db-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f00db-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f00db-117">- GroupId</span><span class="sxs-lookup"><span data-stu-id="f00db-117">-GroupId</span></span>
<span data-ttu-id="f00db-118">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="f00db-118">Specifies the group ID.</span></span>
<span data-ttu-id="f00db-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f00db-119">This parameter is required.</span></span>

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

### <span data-ttu-id="f00db-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f00db-120">-PassThru</span></span>
<span data-ttu-id="f00db-121">passthru</span><span class="sxs-lookup"><span data-stu-id="f00db-121">passthru</span></span>

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

### <span data-ttu-id="f00db-122">- ProductId</span><span class="sxs-lookup"><span data-stu-id="f00db-122">-ProductId</span></span>
<span data-ttu-id="f00db-123">Określa identyfikator produktu.</span><span class="sxs-lookup"><span data-stu-id="f00db-123">Specifies the product ID.</span></span>
<span data-ttu-id="f00db-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f00db-124">This parameter is required.</span></span>

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

### <span data-ttu-id="f00db-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f00db-125">CommonParameters</span></span>
<span data-ttu-id="f00db-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f00db-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f00db-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f00db-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f00db-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f00db-128">INPUTS</span></span>

### <span data-ttu-id="f00db-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f00db-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f00db-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f00db-130">System.String</span></span>

### <span data-ttu-id="f00db-131">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="f00db-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f00db-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f00db-132">OUTPUTS</span></span>

### <span data-ttu-id="f00db-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f00db-133">System.Boolean</span></span>

## <span data-ttu-id="f00db-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f00db-134">NOTES</span></span>

## <span data-ttu-id="f00db-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f00db-135">RELATED LINKS</span></span>

[<span data-ttu-id="f00db-136">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="f00db-136">Remove-AzApiManagementProductFromGroup</span></span>](./Remove-AzApiManagementProductFromGroup.md)


