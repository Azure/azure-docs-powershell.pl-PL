---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 2FD2C5C0-5A5A-4CF0-9260-21B9E3DE52B9
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementproductfromgroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProductFromGroup.md
ms.openlocfilehash: 05f3ac10171c9135b59b9fb6894f5b5fbf670de0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960897"
---
# <span data-ttu-id="f0973-101">Remove-AzApiManagementProductFromGroup</span><span class="sxs-lookup"><span data-stu-id="f0973-101">Remove-AzApiManagementProductFromGroup</span></span>

## <span data-ttu-id="f0973-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0973-102">SYNOPSIS</span></span>
<span data-ttu-id="f0973-103">Usuwa produkt z grupy.</span><span class="sxs-lookup"><span data-stu-id="f0973-103">Removes a product from a group.</span></span>

## <span data-ttu-id="f0973-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f0973-104">SYNTAX</span></span>

```
Remove-AzApiManagementProductFromGroup -Context <PsApiManagementContext> -GroupId <String> -ProductId <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f0973-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="f0973-105">DESCRIPTION</span></span>
<span data-ttu-id="f0973-106">Polecenie **cmdlet Remove-AzApiManagementProductFromGroup** usuwa produkt z istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="f0973-106">The **Remove-AzApiManagementProductFromGroup** cmdlet removes a product from an existing group.</span></span>
<span data-ttu-id="f0973-107">Innymi słowy to polecenie cmdlet usuwa przypisanie grupy z produktu.</span><span class="sxs-lookup"><span data-stu-id="f0973-107">In other words, this cmdlet removes the group assignment from a product.</span></span>

## <span data-ttu-id="f0973-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f0973-108">EXAMPLES</span></span>

### <span data-ttu-id="f0973-109">Przykład 1. Usuwanie produktu z grupy</span><span class="sxs-lookup"><span data-stu-id="f0973-109">Example 1: Remove a product from a group</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProductFromGroup -Context $apimContext -GroupId "0001" -ProductId "0123456789"
```

<span data-ttu-id="f0973-110">To polecenie usuwa produkt z istniejącej grupy.</span><span class="sxs-lookup"><span data-stu-id="f0973-110">This command removes a product from an existing group.</span></span>

## <span data-ttu-id="f0973-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f0973-111">PARAMETERS</span></span>

### <span data-ttu-id="f0973-112">— kontekst</span><span class="sxs-lookup"><span data-stu-id="f0973-112">-Context</span></span>
<span data-ttu-id="f0973-113">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="f0973-113">Specifies a **PsApiManagementContext** object.</span></span>
<span data-ttu-id="f0973-114">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f0973-114">This parameter is required.</span></span>

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

### <span data-ttu-id="f0973-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0973-115">-DefaultProfile</span></span>
<span data-ttu-id="f0973-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f0973-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f0973-117">- GroupId</span><span class="sxs-lookup"><span data-stu-id="f0973-117">-GroupId</span></span>
<span data-ttu-id="f0973-118">Określa identyfikator grupy.</span><span class="sxs-lookup"><span data-stu-id="f0973-118">Specifies the group ID.</span></span>
<span data-ttu-id="f0973-119">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f0973-119">This parameter is required.</span></span>

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

### <span data-ttu-id="f0973-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f0973-120">-PassThru</span></span>
<span data-ttu-id="f0973-121">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiedzie, lub $False w przeciwnym razie.</span><span class="sxs-lookup"><span data-stu-id="f0973-121">Indicates that this cmdlet returns a value of $True, if it succeeds, or $False, otherwise.</span></span>

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

### <span data-ttu-id="f0973-122">- ProductId</span><span class="sxs-lookup"><span data-stu-id="f0973-122">-ProductId</span></span>
<span data-ttu-id="f0973-123">Określa identyfikator produktu.</span><span class="sxs-lookup"><span data-stu-id="f0973-123">Specifies the product ID.</span></span>
<span data-ttu-id="f0973-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f0973-124">This parameter is required.</span></span>

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

### <span data-ttu-id="f0973-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0973-125">CommonParameters</span></span>
<span data-ttu-id="f0973-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f0973-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f0973-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f0973-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0973-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0973-128">INPUTS</span></span>

### <span data-ttu-id="f0973-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f0973-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f0973-130">System.String</span><span class="sxs-lookup"><span data-stu-id="f0973-130">System.String</span></span>

### <span data-ttu-id="f0973-131">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="f0973-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f0973-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f0973-132">OUTPUTS</span></span>

### <span data-ttu-id="f0973-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f0973-133">System.Boolean</span></span>

## <span data-ttu-id="f0973-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f0973-134">NOTES</span></span>

## <span data-ttu-id="f0973-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f0973-135">RELATED LINKS</span></span>

[<span data-ttu-id="f0973-136">Add-AzApiManagementProductToGroup</span><span class="sxs-lookup"><span data-stu-id="f0973-136">Add-AzApiManagementProductToGroup</span></span>](./Add-AzApiManagementProductToGroup.md)


