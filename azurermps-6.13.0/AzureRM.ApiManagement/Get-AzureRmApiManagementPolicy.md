---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 7BCEB0EF-1A09-4CED-9F34-CE3AB03181A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementPolicy.md
ms.openlocfilehash: fcf88fcb9b54adec01b8a04b50f557b6a74e7ca8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524750"
---
# <span data-ttu-id="f79eb-101">Get-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f79eb-101">Get-AzureRmApiManagementPolicy</span></span>

## <span data-ttu-id="f79eb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f79eb-102">SYNOPSIS</span></span>
<span data-ttu-id="f79eb-103">Pobiera określone zasady dotyczące zakresu.</span><span class="sxs-lookup"><span data-stu-id="f79eb-103">Gets the specified scope policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f79eb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f79eb-104">SYNTAX</span></span>

### <span data-ttu-id="f79eb-105">GetTenantLevel (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f79eb-105">GetTenantLevel (Default)</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f79eb-106">GetProductLevel</span><span class="sxs-lookup"><span data-stu-id="f79eb-106">GetProductLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ProductId <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f79eb-107">GetApiLevel</span><span class="sxs-lookup"><span data-stu-id="f79eb-107">GetApiLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f79eb-108">GetOperationLevel</span><span class="sxs-lookup"><span data-stu-id="f79eb-108">GetOperationLevel</span></span>
```
Get-AzureRmApiManagementPolicy -Context <PsApiManagementContext> [-Format <String>] [-SaveAs <String>]
 -ApiId <String> [-ApiRevision <String>] -OperationId <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f79eb-109">Opis</span><span class="sxs-lookup"><span data-stu-id="f79eb-109">DESCRIPTION</span></span>
<span data-ttu-id="f79eb-110">Polecenie cmdlet **Get-AzureRmApiManagementPolicy** pobiera określone zasady dotyczące zakresu.</span><span class="sxs-lookup"><span data-stu-id="f79eb-110">The **Get-AzureRmApiManagementPolicy** cmdlet gets the specified scope policy.</span></span>

## <span data-ttu-id="f79eb-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f79eb-111">EXAMPLES</span></span>

### <span data-ttu-id="f79eb-112">Przykład 1: uzyskiwanie zasad na poziomie dzierżawy</span><span class="sxs-lookup"><span data-stu-id="f79eb-112">Example 1: Get the tenant level policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -SaveAs "C:\contoso\policies\tenantpolicy.xml"
```

<span data-ttu-id="f79eb-113">To polecenie pobiera zasady na poziomie dzierżawy i zapisuje je w pliku o nazwie tenantpolicy.xml.</span><span class="sxs-lookup"><span data-stu-id="f79eb-113">This command gets tenant level policy and saves it to a file named tenantpolicy.xml.</span></span>

### <span data-ttu-id="f79eb-114">Przykład 2: uzyskiwanie zasad dotyczących zakresu produktów</span><span class="sxs-lookup"><span data-stu-id="f79eb-114">Example 2: Get the product-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ProductId "0123456789"
```

<span data-ttu-id="f79eb-115">To polecenie uzyskuje zasady dotyczące zakresu produktów</span><span class="sxs-lookup"><span data-stu-id="f79eb-115">This command gets product-scope policy</span></span>

### <span data-ttu-id="f79eb-116">Przykład 3: uzyskiwanie zasad dotyczących zakresu interfejsów API</span><span class="sxs-lookup"><span data-stu-id="f79eb-116">Example 3: Get the API-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210"
```

<span data-ttu-id="f79eb-117">To polecenie pobiera zasady dotyczące zakresu interfejsów API.</span><span class="sxs-lookup"><span data-stu-id="f79eb-117">This command gets API-scope policy.</span></span>

### <span data-ttu-id="f79eb-118">Przykład 4: uzyskiwanie zasad dotyczących zakresu operacji</span><span class="sxs-lookup"><span data-stu-id="f79eb-118">Example 4: Get the operation-scope policy</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementPolicy -Context $apimContext -ApiId "9876543210" -OperationId "777"
```

<span data-ttu-id="f79eb-119">To polecenie uzyskuje zasady dotyczące zakresu operacji.</span><span class="sxs-lookup"><span data-stu-id="f79eb-119">This command gets the operation-scope policy.</span></span>

## <span data-ttu-id="f79eb-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f79eb-120">PARAMETERS</span></span>

### <span data-ttu-id="f79eb-121">-ApiId</span><span class="sxs-lookup"><span data-stu-id="f79eb-121">-ApiId</span></span>
<span data-ttu-id="f79eb-122">Określa identyfikator istniejącego interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="f79eb-122">Specifies the identifier of the existing API.</span></span>
<span data-ttu-id="f79eb-123">W przypadku określenia tego parametru polecenie cmdlet zwraca zasadę zakresu API.</span><span class="sxs-lookup"><span data-stu-id="f79eb-123">If you specify this parameter the cmdlet returns the API-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f79eb-124">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="f79eb-124">-ApiRevision</span></span>
<span data-ttu-id="f79eb-125">Identyfikator wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="f79eb-125">Identifier of API Revision.</span></span> <span data-ttu-id="f79eb-126">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f79eb-126">This parameter is optional.</span></span> <span data-ttu-id="f79eb-127">Jeśli ta pozycja nie jest określona, zasady zostaną pobrane z wersji obecnie aktywnej interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="f79eb-127">If not specified, the policy will be retrieved from the currently active api revision.</span></span>

```yaml
Type: System.String
Parameter Sets: GetApiLevel, GetOperationLevel
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f79eb-128">-Context</span><span class="sxs-lookup"><span data-stu-id="f79eb-128">-Context</span></span>
<span data-ttu-id="f79eb-129">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="f79eb-129">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="f79eb-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f79eb-130">-DefaultProfile</span></span>
<span data-ttu-id="f79eb-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f79eb-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f79eb-132">-Force</span><span class="sxs-lookup"><span data-stu-id="f79eb-132">-Force</span></span>
<span data-ttu-id="f79eb-133">ps_force</span><span class="sxs-lookup"><span data-stu-id="f79eb-133">ps_force</span></span>

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

### <span data-ttu-id="f79eb-134">-Format</span><span class="sxs-lookup"><span data-stu-id="f79eb-134">-Format</span></span>
<span data-ttu-id="f79eb-135">Określa format zasad zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f79eb-135">Specifies the format of the API management policy.</span></span>
<span data-ttu-id="f79eb-136">Domyślną wartością tego parametru jest "application/vnd. MS-Azure-APIM. Policy + XML".</span><span class="sxs-lookup"><span data-stu-id="f79eb-136">The default value for this parameter is "application/vnd.ms-azure-apim.policy+xml".</span></span>

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

### <span data-ttu-id="f79eb-137">-OperationId</span><span class="sxs-lookup"><span data-stu-id="f79eb-137">-OperationId</span></span>
<span data-ttu-id="f79eb-138">Określa identyfikator istniejącej operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="f79eb-138">Specifies the identifier of the existing API operation.</span></span>
<span data-ttu-id="f79eb-139">Jeśli określisz ten parametr za pomocą funkcji *ApiId* , polecenie cmdlet zwraca zasady zakresu operacja.</span><span class="sxs-lookup"><span data-stu-id="f79eb-139">If you specify this parameter with *ApiId* the cmdlet returns operation-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperationLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f79eb-140">-ProductId</span><span class="sxs-lookup"><span data-stu-id="f79eb-140">-ProductId</span></span>
<span data-ttu-id="f79eb-141">Określa identyfikator istniejącego produktu.</span><span class="sxs-lookup"><span data-stu-id="f79eb-141">Specifies the identifier of an existing product.</span></span>
<span data-ttu-id="f79eb-142">W przypadku określenia tego parametru polecenie cmdlet zwraca zasadę zakresu produktu.</span><span class="sxs-lookup"><span data-stu-id="f79eb-142">If you specify this parameter the cmdlet returns the product-scope policy.</span></span>

```yaml
Type: System.String
Parameter Sets: GetProductLevel
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f79eb-143">-SaveAs</span><span class="sxs-lookup"><span data-stu-id="f79eb-143">-SaveAs</span></span>
<span data-ttu-id="f79eb-144">Określa ścieżkę pliku, do którego ma zostać zapisany wynik.</span><span class="sxs-lookup"><span data-stu-id="f79eb-144">Specifies the file path to save the result to.</span></span>
<span data-ttu-id="f79eb-145">Jeśli nie określisz tego parametru, wynik jest przestawny jako Sting.</span><span class="sxs-lookup"><span data-stu-id="f79eb-145">If you do not specify this parameter the result is pipelined as a sting.</span></span>

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

### <span data-ttu-id="f79eb-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f79eb-146">-Confirm</span></span>
<span data-ttu-id="f79eb-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f79eb-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f79eb-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f79eb-148">-WhatIf</span></span>
<span data-ttu-id="f79eb-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f79eb-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f79eb-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f79eb-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f79eb-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f79eb-151">CommonParameters</span></span>
<span data-ttu-id="f79eb-152">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f79eb-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f79eb-153">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f79eb-153">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f79eb-154">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f79eb-154">INPUTS</span></span>

### <span data-ttu-id="f79eb-155">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f79eb-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f79eb-156">System. String</span><span class="sxs-lookup"><span data-stu-id="f79eb-156">System.String</span></span>

### <span data-ttu-id="f79eb-157">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="f79eb-157">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="f79eb-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f79eb-158">OUTPUTS</span></span>

### <span data-ttu-id="f79eb-159">System. String</span><span class="sxs-lookup"><span data-stu-id="f79eb-159">System.String</span></span>

## <span data-ttu-id="f79eb-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f79eb-160">NOTES</span></span>

## <span data-ttu-id="f79eb-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f79eb-161">RELATED LINKS</span></span>

[<span data-ttu-id="f79eb-162">Remove-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f79eb-162">Remove-AzureRmApiManagementPolicy</span></span>](./Remove-AzureRmApiManagementPolicy.md)

[<span data-ttu-id="f79eb-163">Set-AzureRmApiManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="f79eb-163">Set-AzureRmApiManagementPolicy</span></span>](./Set-AzureRmApiManagementPolicy.md)


