---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: e50e912c55a09ef5d036bee668bc45f58fc42c19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526394"
---
# <span data-ttu-id="82f9d-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="82f9d-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="82f9d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="82f9d-102">SYNOPSIS</span></span>
<span data-ttu-id="82f9d-103">Ustawia szczegóły operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="82f9d-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82f9d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="82f9d-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> [-ApiRevision <String>]
 -OperationId <String> -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82f9d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="82f9d-105">DESCRIPTION</span></span>
<span data-ttu-id="82f9d-106">Polecenie cmdlet **Set-AzureRmApiManagementOperation** ustawia szczegóły operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="82f9d-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="82f9d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="82f9d-107">EXAMPLES</span></span>

### <span data-ttu-id="82f9d-108">Przykład 1. Ustawianie szczegółów operacji</span><span class="sxs-lookup"><span data-stu-id="82f9d-108">Example 1: Set the operation details</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="82f9d-109">To polecenie ustawia szczegóły operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="82f9d-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="82f9d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="82f9d-110">PARAMETERS</span></span>

### <span data-ttu-id="82f9d-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="82f9d-111">-ApiId</span></span>
<span data-ttu-id="82f9d-112">Określa identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="82f9d-112">Specifies the identifier of the API.</span></span>

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

### <span data-ttu-id="82f9d-113">-ApiRevision</span><span class="sxs-lookup"><span data-stu-id="82f9d-113">-ApiRevision</span></span>
<span data-ttu-id="82f9d-114">Identyfikator wersji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="82f9d-114">Identifier of API Revision.</span></span> <span data-ttu-id="82f9d-115">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="82f9d-115">This parameter is optional.</span></span> <span data-ttu-id="82f9d-116">Jeśli argument nie zostanie określony, operacja zostanie zaktualizowana w wersji obecnie aktywnej funkcji API.</span><span class="sxs-lookup"><span data-stu-id="82f9d-116">If not specified, the operation will be updated in the currently active api revision.</span></span>

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

### <span data-ttu-id="82f9d-117">-Context</span><span class="sxs-lookup"><span data-stu-id="82f9d-117">-Context</span></span>
<span data-ttu-id="82f9d-118">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="82f9d-118">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="82f9d-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82f9d-119">-DefaultProfile</span></span>
<span data-ttu-id="82f9d-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="82f9d-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="82f9d-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="82f9d-121">-Description</span></span>
<span data-ttu-id="82f9d-122">Określa opis nowej operacji.</span><span class="sxs-lookup"><span data-stu-id="82f9d-122">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="82f9d-123">-Method</span><span class="sxs-lookup"><span data-stu-id="82f9d-123">-Method</span></span>
<span data-ttu-id="82f9d-124">Określa metodę HTTP nowej operacji.</span><span class="sxs-lookup"><span data-stu-id="82f9d-124">Specifies the HTTP method of the new operation.</span></span>

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

### <span data-ttu-id="82f9d-125">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="82f9d-125">-Name</span></span>
<span data-ttu-id="82f9d-126">Określa nazwę wyświetlaną nowej operacji.</span><span class="sxs-lookup"><span data-stu-id="82f9d-126">Specifies the display name of the new operation.</span></span>

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

### <span data-ttu-id="82f9d-127">-OperationId</span><span class="sxs-lookup"><span data-stu-id="82f9d-127">-OperationId</span></span>
<span data-ttu-id="82f9d-128">Określa identyfikator istniejącej operacji.</span><span class="sxs-lookup"><span data-stu-id="82f9d-128">Specifies the identifier of the existing operation.</span></span>

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

### <span data-ttu-id="82f9d-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="82f9d-129">-PassThru</span></span>
<span data-ttu-id="82f9d-130">passthru</span><span class="sxs-lookup"><span data-stu-id="82f9d-130">passthru</span></span>

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

### <span data-ttu-id="82f9d-131">-Request</span><span class="sxs-lookup"><span data-stu-id="82f9d-131">-Request</span></span>
<span data-ttu-id="82f9d-132">Określa szczegóły żądania operacji.</span><span class="sxs-lookup"><span data-stu-id="82f9d-132">Specifies the operation request details.</span></span>

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

### <span data-ttu-id="82f9d-133">-Odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="82f9d-133">-Responses</span></span>
<span data-ttu-id="82f9d-134">Określa tablicę możliwych odpowiedzi na operacje.</span><span class="sxs-lookup"><span data-stu-id="82f9d-134">Specifies an array of possible operation responses.</span></span>

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

### <span data-ttu-id="82f9d-135">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="82f9d-135">-TemplateParameters</span></span>
<span data-ttu-id="82f9d-136">Określa tablicę lub parametry zdefiniowane w parametrach *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="82f9d-136">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="82f9d-137">Jeśli wartość nie zostanie określona, zostanie wygenerowana wartość domyślna na podstawie UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="82f9d-137">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="82f9d-138">Za pomocą tego parametru można uzyskać więcej informacji na temat parametrów, takich jak opis, typ i inne możliwe wartości.</span><span class="sxs-lookup"><span data-stu-id="82f9d-138">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

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

### <span data-ttu-id="82f9d-139">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="82f9d-139">-UrlTemplate</span></span>
<span data-ttu-id="82f9d-140">Określa szablon adresu URL.</span><span class="sxs-lookup"><span data-stu-id="82f9d-140">Specifies the URL template.</span></span>
<span data-ttu-id="82f9d-141">Na przykład: Customers/{CID}/Orders/{OID}/? Date = {Date}.</span><span class="sxs-lookup"><span data-stu-id="82f9d-141">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

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

### <span data-ttu-id="82f9d-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82f9d-142">CommonParameters</span></span>
<span data-ttu-id="82f9d-143">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="82f9d-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82f9d-144">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82f9d-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82f9d-145">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="82f9d-145">INPUTS</span></span>

### <span data-ttu-id="82f9d-146">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="82f9d-146">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="82f9d-147">System. String</span><span class="sxs-lookup"><span data-stu-id="82f9d-147">System.String</span></span>

### <span data-ttu-id="82f9d-148">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementParameter []</span><span class="sxs-lookup"><span data-stu-id="82f9d-148">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementParameter[]</span></span>

### <span data-ttu-id="82f9d-149">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementRequest</span><span class="sxs-lookup"><span data-stu-id="82f9d-149">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementRequest</span></span>

### <span data-ttu-id="82f9d-150">Microsoft. Azure. Commands. ApiManagement. servicemanagement. models. PsApiManagementResponse []</span><span class="sxs-lookup"><span data-stu-id="82f9d-150">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResponse[]</span></span>

### <span data-ttu-id="82f9d-151">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="82f9d-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="82f9d-152">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="82f9d-152">OUTPUTS</span></span>

### <span data-ttu-id="82f9d-153">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="82f9d-153">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="82f9d-154">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="82f9d-154">NOTES</span></span>

## <span data-ttu-id="82f9d-155">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="82f9d-155">RELATED LINKS</span></span>

[<span data-ttu-id="82f9d-156">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="82f9d-156">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="82f9d-157">Nowe — AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="82f9d-157">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="82f9d-158">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="82f9d-158">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


