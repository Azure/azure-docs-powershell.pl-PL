---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 223FBBA6-4405-4B7A-BA63-5F2434A2A50D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementproduct
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementProduct.md
ms.openlocfilehash: f28bfc223ed187724aa8702c378bfce5d88755fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716596"
---
# <span data-ttu-id="9062e-101">Set-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9062e-101">Set-AzureRmApiManagementProduct</span></span>

## <span data-ttu-id="9062e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9062e-102">SYNOPSIS</span></span>
<span data-ttu-id="9062e-103">Ustawia szczegóły produktu do zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="9062e-103">Sets the API Management product details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9062e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9062e-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementProduct -Context <PsApiManagementContext> -ProductId <String> [-Title <String>]
 [-Description <String>] [-LegalTerms <String>] [-SubscriptionRequired <Boolean>] [-ApprovalRequired <Boolean>]
 [-SubscriptionsLimit <Int32>] [-State <PsApiManagementProductState>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9062e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9062e-105">DESCRIPTION</span></span>
<span data-ttu-id="9062e-106">Polecenie cmdlet **Set-AzureRmApiManagementProduct** ustawia szczegóły produktu zarządzania API.</span><span class="sxs-lookup"><span data-stu-id="9062e-106">The **Set-AzureRmApiManagementProduct** cmdlet sets the API Management product details.</span></span>

## <span data-ttu-id="9062e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9062e-107">EXAMPLES</span></span>

### <span data-ttu-id="9062e-108">Przykład 1: aktualizowanie szczegółów produktu</span><span class="sxs-lookup"><span data-stu-id="9062e-108">Example 1: Update the product details</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementProduct -Context $apimContext -ProductId "0123456789" -Title "Starter" -Description "Starter Product" -LegalTerms "Free for all" -SubscriptionRequired $True -State "NotPublished"
```

<span data-ttu-id="9062e-109">To polecenie aktualizuje szczegóły dotyczące produktu zarządzania interfejsem API, wymaga subskrypcji, a następnie cofa publikowanie.</span><span class="sxs-lookup"><span data-stu-id="9062e-109">This command updates the API Management product details, requires a subscription, and then unpublishes.</span></span>

## <span data-ttu-id="9062e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9062e-110">PARAMETERS</span></span>

### <span data-ttu-id="9062e-111">-ApprovalRequired</span><span class="sxs-lookup"><span data-stu-id="9062e-111">-ApprovalRequired</span></span>
<span data-ttu-id="9062e-112">Wskazuje, czy subskrypcja produktu wymaga zatwierdzenia.</span><span class="sxs-lookup"><span data-stu-id="9062e-112">Indicates whether the subscription to the product requires approval.</span></span>
<span data-ttu-id="9062e-113">Wartość domyślna to **$false**.</span><span class="sxs-lookup"><span data-stu-id="9062e-113">The default value is **$False**.</span></span>

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

### <span data-ttu-id="9062e-114">-Context</span><span class="sxs-lookup"><span data-stu-id="9062e-114">-Context</span></span>
<span data-ttu-id="9062e-115">Określa wystąpienie obiektu **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="9062e-115">Specifies an instance of the **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="9062e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9062e-116">-DefaultProfile</span></span>
<span data-ttu-id="9062e-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="9062e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9062e-118">— Opis</span><span class="sxs-lookup"><span data-stu-id="9062e-118">-Description</span></span>
<span data-ttu-id="9062e-119">Określa opis produktu.</span><span class="sxs-lookup"><span data-stu-id="9062e-119">Specifies the product description.</span></span>

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

### <span data-ttu-id="9062e-120">-LegalTerms</span><span class="sxs-lookup"><span data-stu-id="9062e-120">-LegalTerms</span></span>
<span data-ttu-id="9062e-121">Określa warunki prawne użytkowania produktu.</span><span class="sxs-lookup"><span data-stu-id="9062e-121">Specifies the legal terms of use of the product.</span></span>

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

### <span data-ttu-id="9062e-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9062e-122">-PassThru</span></span>
<span data-ttu-id="9062e-123">passthru</span><span class="sxs-lookup"><span data-stu-id="9062e-123">passthru</span></span>

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

### <span data-ttu-id="9062e-124">-ProductId</span><span class="sxs-lookup"><span data-stu-id="9062e-124">-ProductId</span></span>
<span data-ttu-id="9062e-125">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="9062e-125">Specifies the identifier of the existing product.</span></span>

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

### <span data-ttu-id="9062e-126">-State</span><span class="sxs-lookup"><span data-stu-id="9062e-126">-State</span></span>
<span data-ttu-id="9062e-127">Określa stan produktu.</span><span class="sxs-lookup"><span data-stu-id="9062e-127">Specifies the product state.</span></span>
<span data-ttu-id="9062e-128">psdx_paramvalues</span><span class="sxs-lookup"><span data-stu-id="9062e-128">psdx_paramvalues</span></span>
- <span data-ttu-id="9062e-129">NotPublished</span><span class="sxs-lookup"><span data-stu-id="9062e-129">NotPublished</span></span>
- <span data-ttu-id="9062e-130">Podawane</span><span class="sxs-lookup"><span data-stu-id="9062e-130">Published</span></span>

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

### <span data-ttu-id="9062e-131">-SubscriptionRequired</span><span class="sxs-lookup"><span data-stu-id="9062e-131">-SubscriptionRequired</span></span>
<span data-ttu-id="9062e-132">Wskazuje, czy produkt wymaga subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9062e-132">Indicates whether the product requires a subscription.</span></span>
<span data-ttu-id="9062e-133">Domyślną wartością tego parametru jest **$true**.</span><span class="sxs-lookup"><span data-stu-id="9062e-133">The default value for this parameter is **$True**.</span></span>

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

### <span data-ttu-id="9062e-134">-SubscriptionsLimit</span><span class="sxs-lookup"><span data-stu-id="9062e-134">-SubscriptionsLimit</span></span>
<span data-ttu-id="9062e-135">Określa maksymalną liczbę jednoczesnych subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="9062e-135">Specifies the maximum number of simultaneous subscriptions.</span></span>
<span data-ttu-id="9062e-136">Wartość domyślna tego parametru to 1.</span><span class="sxs-lookup"><span data-stu-id="9062e-136">The default value for this parameter is 1.</span></span>

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

### <span data-ttu-id="9062e-137">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="9062e-137">-Title</span></span>
<span data-ttu-id="9062e-138">Określa tytuł produktu ustawiony przez polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9062e-138">Specifies the product title this cmdlet sets.</span></span>

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

### <span data-ttu-id="9062e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9062e-139">CommonParameters</span></span>
<span data-ttu-id="9062e-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9062e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9062e-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9062e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9062e-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9062e-142">INPUTS</span></span>

### <span data-ttu-id="9062e-143">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="9062e-143">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="9062e-144">System. String</span><span class="sxs-lookup"><span data-stu-id="9062e-144">System.String</span></span>

### <span data-ttu-id="9062e-145">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9062e-145">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="9062e-146">System. Nullable "1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="9062e-146">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="9062e-147">System. Nullable "1 [[Microsoft. Azure. Commands. ApiManagement. servicemanagement. modele. PsApiManagementProductState, Microsoft. Azure. Commands. ApiManagement. servicemanagement, Version = 6.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="9062e-147">System.Nullable\`1[[Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProductState, Microsoft.Azure.Commands.ApiManagement.ServiceManagement, Version=6.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9062e-148">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9062e-148">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="9062e-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9062e-149">OUTPUTS</span></span>

### <span data-ttu-id="9062e-150">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9062e-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementProduct</span></span>

## <span data-ttu-id="9062e-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9062e-151">NOTES</span></span>

## <span data-ttu-id="9062e-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9062e-152">RELATED LINKS</span></span>

[<span data-ttu-id="9062e-153">Get-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9062e-153">Get-AzureRmApiManagementProduct</span></span>](./Get-AzureRmApiManagementProduct.md)

[<span data-ttu-id="9062e-154">Nowe — AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9062e-154">New-AzureRmApiManagementProduct</span></span>](./New-AzureRmApiManagementProduct.md)

[<span data-ttu-id="9062e-155">Remove-AzureRmApiManagementProduct</span><span class="sxs-lookup"><span data-stu-id="9062e-155">Remove-AzureRmApiManagementProduct</span></span>](./Remove-AzureRmApiManagementProduct.md)


