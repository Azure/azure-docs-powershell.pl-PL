---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
ms.openlocfilehash: 92848cb2daa0976d8206549fc16d1a6f039199a6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94053144"
---
# <span data-ttu-id="93030-101">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="93030-101">Set-AzApiManagementOperation</span></span>

## <span data-ttu-id="93030-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="93030-102">SYNOPSIS</span></span>
<span data-ttu-id="93030-103">Ustawia szczegóły operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="93030-103">Sets API operation details.</span></span>

## <span data-ttu-id="93030-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="93030-104">SYNTAX</span></span>

```
Set-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="93030-105">Opis</span><span class="sxs-lookup"><span data-stu-id="93030-105">DESCRIPTION</span></span>
<span data-ttu-id="93030-106">Polecenie cmdlet **Set-AzApiManagementOperation** ustawia szczegóły operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="93030-106">The **Set-AzApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="93030-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="93030-107">EXAMPLES</span></span>

### <span data-ttu-id="93030-108">Przykład 1. Ustawianie szczegółów operacji</span><span class="sxs-lookup"><span data-stu-id="93030-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="93030-109">To polecenie ustawia szczegóły operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="93030-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="93030-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="93030-110">PARAMETERS</span></span>

### <span data-ttu-id="93030-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="93030-111">-ApiId</span></span>
<span data-ttu-id="93030-112">Określa identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="93030-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="93030-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="93030-113">-ApiRevision</span></span>
<span data-ttu-id="93030-114">Identyfikator wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="93030-114">Identifier of API Revision.</span></span> <span data-ttu-id="93030-115">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="93030-115">This parameter is optional.</span></span> <span data-ttu-id="93030-116">Jeśli argument nie zostanie określony, operacja zostanie zaktualizowana w wersji obecnie aktywnej funkcji API.</span><span class="sxs-lookup"><span data-stu-id="93030-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="93030-117">-Context</span><span class="sxs-lookup"><span data-stu-id="93030-117">-Context</span></span>
<span data-ttu-id="93030-118">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="93030-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="93030-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93030-119">-DefaultProfile</span></span>
<span data-ttu-id="93030-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="93030-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93030-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="93030-121">-Description</span></span>
<span data-ttu-id="93030-122">Określa opis nowej operacji.</span><span class="sxs-lookup"><span data-stu-id="93030-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="93030-123">-Method</span><span class="sxs-lookup"><span data-stu-id="93030-123">-Method</span></span>
<span data-ttu-id="93030-124">Określa metodę HTTP nowej operacji.</span><span class="sxs-lookup"><span data-stu-id="93030-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="93030-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="93030-125">-Name</span></span>
<span data-ttu-id="93030-126">Określa nazwę wyświetlaną nowej operacji.</span><span class="sxs-lookup"><span data-stu-id="93030-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="93030-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="93030-127">-OperationId</span></span>
<span data-ttu-id="93030-128">Określa identyfikator istniejącej operacji.</span><span class="sxs-lookup"><span data-stu-id="93030-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="93030-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="93030-129">-PassThru</span></span>
<span data-ttu-id="93030-130">passthru</span><span class="sxs-lookup"><span data-stu-id="93030-130">passthru</span></span>

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

### <span data-ttu-id="93030-131">-Request</span><span class="sxs-lookup"><span data-stu-id="93030-131">-Request</span></span>
<span data-ttu-id="93030-132">Określa szczegóły żądania operacji.</span><span class="sxs-lookup"><span data-stu-id="93030-132">Specifies the operation request details.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93030-133">-Odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="93030-133">-Responses</span></span>
<span data-ttu-id="93030-134">Określa tablicę możliwych odpowiedzi na operacje.</span><span class="sxs-lookup"><span data-stu-id="93030-134">Specifies an array of possible operation responses.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93030-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="93030-135">-TemplateParameters</span></span>
<span data-ttu-id="93030-136">Określa tablicę lub parametry zdefiniowane w parametrach *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="93030-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="93030-137">Jeśli wartość nie zostanie określona, zostanie wygenerowana wartość domyślna na podstawie UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="93030-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="93030-138">Za pomocą tego parametru można uzyskać więcej informacji na temat parametrów, takich jak opis, typ i inne możliwe wartości.</span><span class="sxs-lookup"><span data-stu-id="93030-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="93030-139">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="93030-139">-UrlTemplate</span></span>
<span data-ttu-id="93030-140">Określa szablon adresu URL.</span><span class="sxs-lookup"><span data-stu-id="93030-140">Specifies the URL template.</span></span>
<span data-ttu-id="93030-141">Na przykład: Customers/{CID}/Orders/{OID}/? Date = {Date}.</span><span class="sxs-lookup"><span data-stu-id="93030-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="93030-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="93030-142">-Confirm</span></span>
<span data-ttu-id="93030-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93030-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93030-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93030-144">-WhatIf</span></span>
<span data-ttu-id="93030-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="93030-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="93030-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="93030-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93030-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93030-147">CommonParameters</span></span>
<span data-ttu-id="93030-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93030-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93030-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="93030-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93030-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93030-150">INPUTS</span></span>

### <span data-ttu-id="93030-151">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="93030-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="93030-152">System. String</span><span class="sxs-lookup"><span data-stu-id="93030-152">System.String</span></span>

### <span data-ttu-id="93030-153">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="93030-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="93030-154">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="93030-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="93030-155">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="93030-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="93030-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="93030-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="93030-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="93030-157">OUTPUTS</span></span>

### <span data-ttu-id="93030-158">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="93030-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="93030-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="93030-159">NOTES</span></span>

## <span data-ttu-id="93030-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93030-160">RELATED LINKS</span></span>

[<span data-ttu-id="93030-161">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="93030-161">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="93030-162">Nowe — AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="93030-162">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="93030-163">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="93030-163">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)


