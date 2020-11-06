---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 16eed643397245fa54b2876430042335762ea048
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547259"
---
# <span data-ttu-id="3462d-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3462d-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="3462d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3462d-102">SYNOPSIS</span></span>
<span data-ttu-id="3462d-103">Pobiera określone zasady dotyczące zakresu.</span><span class="sxs-lookup"><span data-stu-id="3462d-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3462d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3462d-104">SYNTAX</span></span>

### <span data-ttu-id="3462d-105">Poziom dzierżawy (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="3462d-105">Tenant level (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3462d-106">Poziom produktu</span><span class="sxs-lookup"><span data-stu-id="3462d-106">Product level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3462d-107">Poziom interfejsu API</span><span class="sxs-lookup"><span data-stu-id="3462d-107">API level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3462d-108">Poziom operacji</span><span class="sxs-lookup"><span data-stu-id="3462d-108">Operation level</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> -OperationId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3462d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="3462d-109">DESCRIPTION</span></span>
<span data-ttu-id="3462d-110">Polecenie cmdlet **Get-AzureRmApiManagementPolicy** pobiera określone zasady dotyczące zakresu.</span><span class="sxs-lookup"><span data-stu-id="3462d-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="3462d-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3462d-111">EXAMPLES</span></span>

### <span data-ttu-id="3462d-112">Przykład 1: uzyskiwanie zasad na poziomie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="3462d-112">Example 1: Get the tenant level policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="3462d-113">To polecenie pobiera zasady na poziomie dzierżawy i zapisuje je w pliku o nazwie tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="3462d-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="3462d-114">Przykład 2: uzyskiwanie zasad dotyczących zakresu produktów</span><span class="sxs-lookup"><span data-stu-id="3462d-114">Example 2: Get the product-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ProductId "0123456789"
```

<span data-ttu-id="3462d-115">To polecenie uzyskuje zasady dotyczące zakresu produktów</span><span class="sxs-lookup"><span data-stu-id="3462d-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="3462d-116">Przykład 3: uzyskiwanie zasad dotyczących zakresu interfejsów API</span><span class="sxs-lookup"><span data-stu-id="3462d-116">Example 3: Get the API-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210"
```

<span data-ttu-id="3462d-117">To polecenie pobiera zasady dotyczące zakresu interfejsów API.</span><span class="sxs-lookup"><span data-stu-id="3462d-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="3462d-118">Przykład 4: uzyskiwanie zasad dotyczących zakresu operacji</span><span class="sxs-lookup"><span data-stu-id="3462d-118">Example 4: Get the operation-scope policy</span></span>
```
PS C:\>Get-AzureRmApiManagementPolicy -Context $APImContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="3462d-119">To polecenie uzyskuje zasady dotyczące zakresu operacji.</span><span class="sxs-lookup"><span data-stu-id="3462d-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="3462d-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3462d-120">PARAMETERS</span></span>

### <span data-ttu-id="3462d-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="3462d-121">-ApiId</span></span>
<span data-ttu-id="3462d-122">Określa identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="3462d-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="3462d-123">W przypadku określenia tego parametru polecenie cmdlet zwraca zasadę zakresu API.</span><span class="sxs-lookup"><span data-stu-id="3462d-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: API level, Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3462d-124">-Context</span><span class="sxs-lookup"><span data-stu-id="3462d-124">-Context</span></span>
<span data-ttu-id="3462d-125">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="3462d-125">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="3462d-126">-Force</span><span class="sxs-lookup"><span data-stu-id="3462d-126">-Force</span></span>
<span data-ttu-id="3462d-127">ps_force</span><span class="sxs-lookup"><span data-stu-id="3462d-127">ps_force</span></span>

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

### <span data-ttu-id="3462d-128">-Format</span><span class="sxs-lookup"><span data-stu-id="3462d-128">-Format</span></span>
<span data-ttu-id="3462d-129">Określa format zasad zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3462d-129">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="3462d-130">Domyślną wartością tego parametru jest "application/vnd. MS-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="3462d-130">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="3462d-131">-OperationId</span><span class="sxs-lookup"><span data-stu-id="3462d-131">-OperationId</span></span>
<span data-ttu-id="3462d-132">Określa identyfikator istniejącej operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="3462d-132">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="3462d-133">Jeśli określisz ten parametr za pomocą funkcji *ApiId* , polecenie cmdlet zwraca zasady zakresu operacja.</span><span class="sxs-lookup"><span data-stu-id="3462d-133">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Operation level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3462d-134">-ProductId</span><span class="sxs-lookup"><span data-stu-id="3462d-134">-ProductId</span></span>
<span data-ttu-id="3462d-135">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="3462d-135">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="3462d-136">W przypadku określenia tego parametru polecenie cmdlet zwraca zasadę zakresu produktu.</span><span class="sxs-lookup"><span data-stu-id="3462d-136">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: Product level
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3462d-137">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="3462d-137">-SaveAs</span></span>
<span data-ttu-id="3462d-138">Określa ścieżkę pliku, do którego ma zostać zapisany wynik.</span><span class="sxs-lookup"><span data-stu-id="3462d-138">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="3462d-139">Jeśli nie określisz tego parametru, wynik jest przestawny jako Sting.</span><span class="sxs-lookup"><span data-stu-id="3462d-139">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="3462d-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3462d-140">-Confirm</span></span>
<span data-ttu-id="3462d-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3462d-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3462d-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3462d-142">-WhatIf</span></span>
<span data-ttu-id="3462d-143">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3462d-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3462d-144">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3462d-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3462d-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3462d-145">-DefaultProfile</span></span>
<span data-ttu-id="3462d-146">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3462d-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3462d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3462d-147">CommonParameters</span></span>
<span data-ttu-id="3462d-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3462d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3462d-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3462d-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3462d-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3462d-150">INPUTS</span></span>

## <span data-ttu-id="3462d-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3462d-151">OUTPUTS</span></span>

### <span data-ttu-id="3462d-152">Ciąg</span><span class="sxs-lookup"><span data-stu-id="3462d-152">String</span></span>

## <span data-ttu-id="3462d-153">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3462d-153">NOTES</span></span>

## <span data-ttu-id="3462d-154">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3462d-154">RELATED LINKS</span></span>

[<span data-ttu-id="3462d-155">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3462d-155">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="3462d-156">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="3462d-156">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


