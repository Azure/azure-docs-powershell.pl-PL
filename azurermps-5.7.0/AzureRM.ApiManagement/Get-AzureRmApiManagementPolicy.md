---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: 31b38d07aea51ad1e6bd097cc0c9f7f342e1bfb2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544608"
---
# <span data-ttu-id="a1752-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a1752-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="a1752-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a1752-102">SYNOPSIS</span></span>
<span data-ttu-id="a1752-103">Pobiera określone zasady dotyczące zakresu.</span><span class="sxs-lookup"><span data-stu-id="a1752-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1752-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a1752-104">SYNTAX</span></span>

### <span data-ttu-id="a1752-105">GetTenantLevel (domyślny)</span><span class="sxs-lookup"><span data-stu-id="a1752-105">GetTenantLevel (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1752-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="a1752-106">GetProductLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a1752-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="a1752-107">GetApiLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a1752-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="a1752-108">GetOperationLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> -OperationId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1752-109">Opis</span><span class="sxs-lookup"><span data-stu-id="a1752-109">DESCRIPTION</span></span>
<span data-ttu-id="a1752-110">Polecenie cmdlet **Get-AzureRmApiManagementPolicy** pobiera określone zasady dotyczące zakresu.</span><span class="sxs-lookup"><span data-stu-id="a1752-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="a1752-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a1752-111">EXAMPLES</span></span>

### <span data-ttu-id="a1752-112">Przykład 1: uzyskiwanie zasad na poziomie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="a1752-112">Example 1: Get the tenant level policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="a1752-113">To polecenie pobiera zasady na poziomie dzierżawy i zapisuje je w pliku o nazwie tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="a1752-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="a1752-114">Przykład 2: uzyskiwanie zasad dotyczących zakresu produktów</span><span class="sxs-lookup"><span data-stu-id="a1752-114">Example 2: Get the product-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="a1752-115">To polecenie uzyskuje zasady dotyczące zakresu produktów</span><span class="sxs-lookup"><span data-stu-id="a1752-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="a1752-116">Przykład 3: uzyskiwanie zasad dotyczących zakresu interfejsów API</span><span class="sxs-lookup"><span data-stu-id="a1752-116">Example 3: Get the API-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="a1752-117">To polecenie pobiera zasady dotyczące zakresu interfejsów API.</span><span class="sxs-lookup"><span data-stu-id="a1752-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="a1752-118">Przykład 4: uzyskiwanie zasad dotyczących zakresu operacji</span><span class="sxs-lookup"><span data-stu-id="a1752-118">Example 4: Get the operation-scope policy</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="a1752-119">To polecenie uzyskuje zasady dotyczące zakresu operacji.</span><span class="sxs-lookup"><span data-stu-id="a1752-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="a1752-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a1752-120">PARAMETERS</span></span>

### <span data-ttu-id="a1752-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="a1752-121">-ApiId</span></span>
<span data-ttu-id="a1752-122">Określa identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a1752-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="a1752-123">W przypadku określenia tego parametru polecenie cmdlet zwraca zasadę zakresu API.</span><span class="sxs-lookup"><span data-stu-id="a1752-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1752-124">-Context</span><span class="sxs-lookup"><span data-stu-id="a1752-124">-Context</span></span>
<span data-ttu-id="a1752-125">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="a1752-125">Specifies an instance of **PsApiManagementContext**.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1752-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1752-126">-DefaultProfile</span></span>
<span data-ttu-id="a1752-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a1752-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1752-128">-Force</span><span class="sxs-lookup"><span data-stu-id="a1752-128">-Force</span></span>
<span data-ttu-id="a1752-129">ps_force</span><span class="sxs-lookup"><span data-stu-id="a1752-129">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1752-130">-Format</span><span class="sxs-lookup"><span data-stu-id="a1752-130">-Format</span></span>
<span data-ttu-id="a1752-131">Określa format zasad zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="a1752-131">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="a1752-132">Domyślną wartością tego parametru jest "application/vnd. MS-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="a1752-132">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1752-133">-OperationId</span><span class="sxs-lookup"><span data-stu-id="a1752-133">-OperationId</span></span>
<span data-ttu-id="a1752-134">Określa identyfikator istniejącej operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="a1752-134">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="a1752-135">Jeśli określisz ten parametr za pomocą funkcji *ApiId* , polecenie cmdlet zwraca zasady zakresu operacja.</span><span class="sxs-lookup"><span data-stu-id="a1752-135">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetOperationLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1752-136">-ProductId</span><span class="sxs-lookup"><span data-stu-id="a1752-136">-ProductId</span></span>
<span data-ttu-id="a1752-137">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="a1752-137">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="a1752-138">W przypadku określenia tego parametru polecenie cmdlet zwraca zasadę zakresu produktu.</span><span class="sxs-lookup"><span data-stu-id="a1752-138">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: String
Parameter Sets: GetProductLevel
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1752-139">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="a1752-139">-SaveAs</span></span>
<span data-ttu-id="a1752-140">Określa ścieżkę pliku, do którego ma zostać zapisany wynik.</span><span class="sxs-lookup"><span data-stu-id="a1752-140">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="a1752-141">Jeśli nie określisz tego parametru, wynik jest przestawny jako Sting.</span><span class="sxs-lookup"><span data-stu-id="a1752-141">If you do not specify this parameter the result is pipelined as a sting.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a1752-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a1752-142">-Confirm</span></span>
<span data-ttu-id="a1752-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1752-143">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1752-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1752-144">-WhatIf</span></span>
<span data-ttu-id="a1752-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a1752-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a1752-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a1752-146">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1752-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1752-147">CommonParameters</span></span>
<span data-ttu-id="a1752-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a1752-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1752-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1752-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1752-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a1752-150">INPUTS</span></span>

### <span data-ttu-id="a1752-151">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="a1752-151">None</span></span>
<span data-ttu-id="a1752-152">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="a1752-152">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a1752-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a1752-153">OUTPUTS</span></span>

### <span data-ttu-id="a1752-154">Ciąg</span><span class="sxs-lookup"><span data-stu-id="a1752-154">String</span></span>

## <span data-ttu-id="a1752-155">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a1752-155">NOTES</span></span>

## <span data-ttu-id="a1752-156">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a1752-156">RELATED LINKS</span></span>

[<span data-ttu-id="a1752-157">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a1752-157">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="a1752-158">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="a1752-158">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


