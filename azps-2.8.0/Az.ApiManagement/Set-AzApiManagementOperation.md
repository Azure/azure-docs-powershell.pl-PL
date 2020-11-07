---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementOperation.md
ms.openlocfilehash: 0e5764ec40c05c6894715e718926714a4cbc7070
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706894"
---
# <span data-ttu-id="90f69-101">Set-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="90f69-101">Set-AzApiManagementOperation</span></span>

## <span data-ttu-id="90f69-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90f69-102">SYNOPSIS</span></span>
<span data-ttu-id="90f69-103">Ustawia szczegóły operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="90f69-103">Sets API operation details.</span></span>

## <span data-ttu-id="90f69-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90f69-104">SYNTAX</span></span>

```
Set-AzApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90f69-105">Opis</span><span class="sxs-lookup"><span data-stu-id="90f69-105">DESCRIPTION</span></span>
<span data-ttu-id="90f69-106">Polecenie cmdlet **Set-AzApiManagementOperation** ustawia szczegóły operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="90f69-106">The **Set-AzApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="90f69-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90f69-107">EXAMPLES</span></span>

### <span data-ttu-id="90f69-108">Przykład 1. Ustawianie szczegółów operacji</span><span class="sxs-lookup"><span data-stu-id="90f69-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="90f69-109">To polecenie ustawia szczegóły operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="90f69-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="90f69-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90f69-110">PARAMETERS</span></span>

### <span data-ttu-id="90f69-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="90f69-111">-ApiId</span></span>
<span data-ttu-id="90f69-112">Określa identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="90f69-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="90f69-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="90f69-113">-ApiRevision</span></span>
<span data-ttu-id="90f69-114">Identyfikator wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="90f69-114">Identifier of API Revision.</span></span> <span data-ttu-id="90f69-115">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="90f69-115">This parameter is optional.</span></span> <span data-ttu-id="90f69-116">Jeśli argument nie zostanie określony, operacja zostanie zaktualizowana w wersji obecnie aktywnej funkcji API.</span><span class="sxs-lookup"><span data-stu-id="90f69-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="90f69-117">-Context</span><span class="sxs-lookup"><span data-stu-id="90f69-117">-Context</span></span>
<span data-ttu-id="90f69-118">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="90f69-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="90f69-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90f69-119">-DefaultProfile</span></span>
<span data-ttu-id="90f69-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90f69-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90f69-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="90f69-121">-Description</span></span>
<span data-ttu-id="90f69-122">Określa opis nowej operacji.</span><span class="sxs-lookup"><span data-stu-id="90f69-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="90f69-123">-Method</span><span class="sxs-lookup"><span data-stu-id="90f69-123">-Method</span></span>
<span data-ttu-id="90f69-124">Określa metodę HTTP nowej operacji.</span><span class="sxs-lookup"><span data-stu-id="90f69-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="90f69-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="90f69-125">-Name</span></span>
<span data-ttu-id="90f69-126">Określa nazwę wyświetlaną nowej operacji.</span><span class="sxs-lookup"><span data-stu-id="90f69-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="90f69-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="90f69-127">-OperationId</span></span>
<span data-ttu-id="90f69-128">Określa identyfikator istniejącej operacji.</span><span class="sxs-lookup"><span data-stu-id="90f69-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="90f69-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90f69-129">-PassThru</span></span>
<span data-ttu-id="90f69-130">passthru</span><span class="sxs-lookup"><span data-stu-id="90f69-130">passthru</span></span>

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

### <span data-ttu-id="90f69-131">-Request</span><span class="sxs-lookup"><span data-stu-id="90f69-131">-Request</span></span>
<span data-ttu-id="90f69-132">Określa szczegóły żądania operacji.</span><span class="sxs-lookup"><span data-stu-id="90f69-132">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="90f69-133">-Odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="90f69-133">-Responses</span></span>
<span data-ttu-id="90f69-134">Określa tablicę możliwych odpowiedzi na operacje.</span><span class="sxs-lookup"><span data-stu-id="90f69-134">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="90f69-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="90f69-135">-TemplateParameters</span></span>
<span data-ttu-id="90f69-136">Określa tablicę lub parametry zdefiniowane w parametrach *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="90f69-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="90f69-137">Jeśli wartość nie zostanie określona, zostanie wygenerowana wartość domyślna na podstawie UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="90f69-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="90f69-138">Za pomocą tego parametru można uzyskać więcej informacji na temat parametrów, takich jak opis, typ i inne możliwe wartości.</span><span class="sxs-lookup"><span data-stu-id="90f69-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="90f69-139">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="90f69-139">-UrlTemplate</span></span>
<span data-ttu-id="90f69-140">Określa szablon adresu URL.</span><span class="sxs-lookup"><span data-stu-id="90f69-140">Specifies the URL template.</span></span>
<span data-ttu-id="90f69-141">Na przykład: Customers/{CID}/Orders/{OID}/? Date = {Date}.</span><span class="sxs-lookup"><span data-stu-id="90f69-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="90f69-142">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90f69-142">-Confirm</span></span>
<span data-ttu-id="90f69-143">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90f69-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90f69-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90f69-144">-WhatIf</span></span>
<span data-ttu-id="90f69-145">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90f69-145">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="90f69-146">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="90f69-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90f69-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90f69-147">CommonParameters</span></span>
<span data-ttu-id="90f69-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90f69-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90f69-149">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="90f69-149">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90f69-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90f69-150">INPUTS</span></span>

### <span data-ttu-id="90f69-151">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="90f69-151">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="90f69-152">System. String</span><span class="sxs-lookup"><span data-stu-id="90f69-152">System.String</span></span>

### <span data-ttu-id="90f69-153">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="90f69-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="90f69-154">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="90f69-154">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="90f69-155">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="90f69-155">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="90f69-156">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="90f69-156">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="90f69-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90f69-157">OUTPUTS</span></span>

### <span data-ttu-id="90f69-158">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="90f69-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="90f69-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90f69-159">NOTES</span></span>

## <span data-ttu-id="90f69-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90f69-160">RELATED LINKS</span></span>

[<span data-ttu-id="90f69-161">Get-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="90f69-161">Get-AzApiManagementOperation</span></span>](./Get-AzApiManagementOperation.md)

[<span data-ttu-id="90f69-162">Nowe — AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="90f69-162">New-AzApiManagementOperation</span></span>](./New-AzApiManagementOperation.md)

[<span data-ttu-id="90f69-163">Remove-AzApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="90f69-163">Remove-AzApiManagementOperation</span></span>](./Remove-AzApiManagementOperation.md)


