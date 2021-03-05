---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: D6B7F253-03CD-40BE-87D6-E4AE300A29D5
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementProduct.md
ms.openlocfilehash: 9ad08f867bf78dc4a6bc2df5c4dd3086c3cea33c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979025"
---
# <span data-ttu-id="a07d6-101">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a07d6-101">Remove-AzApiManagementProduct</span></span>

## <span data-ttu-id="a07d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a07d6-102">SYNOPSIS</span></span>
<span data-ttu-id="a07d6-103">Usuwa istniejący produkt zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="a07d6-103">Removes an existing API Management product.</span></span>

## <span data-ttu-id="a07d6-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a07d6-104">SYNTAX</span></span>

```
Remove-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-DeleteSubscriptions]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a07d6-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a07d6-105">DESCRIPTION</span></span>
<span data-ttu-id="a07d6-106">Polecenie **cmdlet Remove-AzApiManagementProduct** usuwa istniejący produkt zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="a07d6-106">The **Remove-AzApiManagementProduct** cmdlet removes an existing API Management product.</span></span>

## <span data-ttu-id="a07d6-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a07d6-107">EXAMPLES</span></span>

### <span data-ttu-id="a07d6-108">Przykład 1. Usuwanie istniejącego produktu i wszystkich subskrypcji</span><span class="sxs-lookup"><span data-stu-id="a07d6-108">Example 1: Remove an existing product and all subscriptions</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -DeleteSubscriptions
```

<span data-ttu-id="a07d6-109">To polecenie usuwa istniejący produkt i wszystkie subskrypcje.</span><span class="sxs-lookup"><span data-stu-id="a07d6-109">This command removes an existing product and all subscriptions.</span></span>

## <span data-ttu-id="a07d6-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a07d6-110">PARAMETERS</span></span>

### <span data-ttu-id="a07d6-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="a07d6-111">-Context</span></span>
<span data-ttu-id="a07d6-112">Określa wystąpienie obiektu **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="a07d6-112">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="a07d6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a07d6-113">-DefaultProfile</span></span>
<span data-ttu-id="a07d6-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="a07d6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a07d6-115">- DeleteSubscriptions</span><span class="sxs-lookup"><span data-stu-id="a07d6-115">-DeleteSubscriptions</span></span>
<span data-ttu-id="a07d6-116">Wskazuje, czy usunąć subskrypcje produktu.</span><span class="sxs-lookup"><span data-stu-id="a07d6-116">Indicates whether to delete subscriptions to the product.</span></span>
<span data-ttu-id="a07d6-117">Jeśli ten parametr nie zostanie ustawiony, a subskrypcje już istnieją, występuje wyjątek.</span><span class="sxs-lookup"><span data-stu-id="a07d6-117">If you do not set this parameter and subscriptions exists, an exception is thrown.</span></span>

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

### <span data-ttu-id="a07d6-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a07d6-118">-PassThru</span></span>
<span data-ttu-id="a07d6-119">Wskazuje, że to polecenie cmdlet zwraca wartość $True, jeśli się powiedzie, lub wartość $False, jeśli się nie powiedzie.</span><span class="sxs-lookup"><span data-stu-id="a07d6-119">Indicates that this cmdlet returns a value of $True, if it succeeds, or a value of $False, if it fails.</span></span>

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

### <span data-ttu-id="a07d6-120">- ProductId</span><span class="sxs-lookup"><span data-stu-id="a07d6-120">-ProductId</span></span>
<span data-ttu-id="a07d6-121">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="a07d6-121">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="a07d6-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a07d6-122">-Confirm</span></span>
<span data-ttu-id="a07d6-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="a07d6-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07d6-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a07d6-124">-WhatIf</span></span>
<span data-ttu-id="a07d6-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a07d6-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a07d6-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="a07d6-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a07d6-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a07d6-127">CommonParameters</span></span>
<span data-ttu-id="a07d6-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a07d6-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a07d6-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a07d6-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a07d6-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a07d6-130">INPUTS</span></span>

### <span data-ttu-id="a07d6-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="a07d6-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="a07d6-132">System.String</span><span class="sxs-lookup"><span data-stu-id="a07d6-132">System.String</span></span>

### <span data-ttu-id="a07d6-133">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="a07d6-133">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a07d6-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a07d6-134">OUTPUTS</span></span>

### <span data-ttu-id="a07d6-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a07d6-135">System.Boolean</span></span>

## <span data-ttu-id="a07d6-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a07d6-136">NOTES</span></span>

## <span data-ttu-id="a07d6-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a07d6-137">RELATED LINKS</span></span>

[<span data-ttu-id="a07d6-138">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a07d6-138">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="a07d6-139">New-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a07d6-139">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="a07d6-140">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="a07d6-140">Set-AzApiManagementProduct</span></span>](./Set-AzApiManagementProduct.md)


