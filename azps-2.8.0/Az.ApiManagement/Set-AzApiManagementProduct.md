---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementProduct.md
ms.openlocfilehash: a4c25514f955b4ea380458cdb1ef845d7b54eb28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706891"
---
# <span data-ttu-id="47da7-101">Set-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="47da7-101">Set-AzApiManagementProduct</span></span>

## <span data-ttu-id="47da7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="47da7-102">SYNOPSIS</span></span>
<span data-ttu-id="47da7-103">Ustawia szczegóły produktu do zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="47da7-103">Sets the API Management product details.</span></span>

## <span data-ttu-id="47da7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="47da7-104">SYNTAX</span></span>

```
Set-AzApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47da7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="47da7-105">DESCRIPTION</span></span>
<span data-ttu-id="47da7-106">Polecenie cmdlet **Set-AzApiManagementProduct** ustawia szczegóły produktu zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="47da7-106">The **Set-AzApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="47da7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="47da7-107">EXAMPLES</span></span>

### <span data-ttu-id="47da7-108">Przykład 1: aktualizowanie szczegółów produktu</span><span class="sxs-lookup"><span data-stu-id="47da7-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="47da7-109">To polecenie aktualizuje szczegóły dotyczące produktu zarządzania interfejsem API, wymaga subskrypcji, a następnie cofa publikowanie.</span><span class="sxs-lookup"><span data-stu-id="47da7-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="47da7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="47da7-110">PARAMETERS</span></span>

### <span data-ttu-id="47da7-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="47da7-111">-ApprovalRequired</span></span>
<span data-ttu-id="47da7-112">Wskazuje, czy subskrypcja produktu wymaga zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="47da7-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="47da7-113">Wartość domyślna to **$false**.</span><span class="sxs-lookup"><span data-stu-id="47da7-113">The default value is **$False**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47da7-114">-Context</span><span class="sxs-lookup"><span data-stu-id="47da7-114">-Context</span></span>
<span data-ttu-id="47da7-115">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="47da7-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="47da7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47da7-116">-DefaultProfile</span></span>
<span data-ttu-id="47da7-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="47da7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47da7-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="47da7-118">-Description</span></span>
<span data-ttu-id="47da7-119">Określa opis produktu.</span><span class="sxs-lookup"><span data-stu-id="47da7-119">Specifies the product description.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47da7-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="47da7-120">-LegalTerms</span></span>
<span data-ttu-id="47da7-121">Określa warunki prawne użytkowania produktu.</span><span class="sxs-lookup"><span data-stu-id="47da7-121">Specifies the legal terms of use of the product.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47da7-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="47da7-122">-PassThru</span></span>
<span data-ttu-id="47da7-123">passthru</span><span class="sxs-lookup"><span data-stu-id="47da7-123">passthru</span></span>

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

### <span data-ttu-id="47da7-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="47da7-124">-ProductId</span></span>
<span data-ttu-id="47da7-125">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="47da7-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="47da7-126">-State</span><span class="sxs-lookup"><span data-stu-id="47da7-126">-State</span></span>
<span data-ttu-id="47da7-127">Określa stan produktu.</span><span class="sxs-lookup"><span data-stu-id="47da7-127">Specifies the product state.</span></span>
<span data-ttu-id="47da7-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="47da7-128">psdx_paramvalues</span></span>
- <span data-ttu-id="47da7-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="47da7-129">NotPublished</span></span>
- <span data-ttu-id="47da7-130">Podawane</span><span class="sxs-lookup"><span data-stu-id="47da7-130">Published</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState]
Parameter Sets: (All)
Aliases:
Accepted values: NotPublished, Published

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47da7-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="47da7-131">-SubscriptionRequired</span></span>
<span data-ttu-id="47da7-132">Wskazuje, czy produkt wymaga subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="47da7-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="47da7-133">Domyślną wartością tego parametru jest **$true**.</span><span class="sxs-lookup"><span data-stu-id="47da7-133">The default value for this parameter is **$True**.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47da7-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="47da7-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="47da7-135">Określa maksymalną liczbę jednoczesnych subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="47da7-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="47da7-136">Wartość domyślna tego parametru to 1.</span><span class="sxs-lookup"><span data-stu-id="47da7-136">The default value for this parameter is 1.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47da7-137">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="47da7-137">-Title</span></span>
<span data-ttu-id="47da7-138">Określa tytuł produktu ustawiony przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47da7-138">Specifies the product title this cmdlet sets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="47da7-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="47da7-139">-Confirm</span></span>
<span data-ttu-id="47da7-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47da7-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47da7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47da7-141">-WhatIf</span></span>
<span data-ttu-id="47da7-142">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="47da7-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47da7-143">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="47da7-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="47da7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47da7-144">CommonParameters</span></span>
<span data-ttu-id="47da7-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="47da7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47da7-146">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="47da7-146">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47da7-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="47da7-147">INPUTS</span></span>

### <span data-ttu-id="47da7-148">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="47da7-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="47da7-149">System. String</span><span class="sxs-lookup"><span data-stu-id="47da7-149">System.String</span></span>

### <span data-ttu-id="47da7-150">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="47da7-150">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="47da7-151">System. Nullable ' 1 [[System. Int32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="47da7-151">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="47da7-152">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementProductState, Microsoft. Azure. PowerShell. cmdlet. ApiManagement. servicemanagement, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="47da7-152">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="47da7-153">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="47da7-153">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="47da7-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="47da7-154">OUTPUTS</span></span>

### <span data-ttu-id="47da7-155">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="47da7-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="47da7-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="47da7-156">NOTES</span></span>

## <span data-ttu-id="47da7-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="47da7-157">RELATED LINKS</span></span>

[<span data-ttu-id="47da7-158">Get-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="47da7-158">Get-AzApiManagementProduct</span></span>](./Get-AzApiManagementProduct.md)

[<span data-ttu-id="47da7-159">Nowe — AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="47da7-159">New-AzApiManagementProduct</span></span>](./New-AzApiManagementProduct.md)

[<span data-ttu-id="47da7-160">Remove-AzApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="47da7-160">Remove-AzApiManagementProduct</span></span>](./Remove-AzApiManagementProduct.md)


