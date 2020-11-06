---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 67EE6EFB-3297-4D21-A6EC-B03F5FE82F84
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementoperation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementOperation.md
ms.openlocfilehash: 4800d7d56d03071b57d25cdacfcf271defa9276f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545835"
---
# <span data-ttu-id="76d0b-101">Set-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="76d0b-101">Set-AzureRmApiManagementOperation</span></span>

## <span data-ttu-id="76d0b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="76d0b-102">SYNOPSIS</span></span>
<span data-ttu-id="76d0b-103">Ustawia szczegóły operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="76d0b-103">Sets API operation details.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="76d0b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="76d0b-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementOperation -Context <PsApiManagementContext> -ApiId <String> -OperationId <String>
 -Name <String> -Method <String> -UrlTemplate <String> [-Description <String>]
 [-TemplateParameters <PsApiManagementParameter[]>] [-Request <PsApiManagementRequest>]
 [-Responses <PsApiManagementResponse[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="76d0b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="76d0b-105">DESCRIPTION</span></span>
<span data-ttu-id="76d0b-106">Polecenie cmdlet **Set-AzureRmApiManagementOperation** ustawia szczegóły operacji interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="76d0b-106">The **Set-AzureRmApiManagementOperation** cmdlet sets API operation details.</span></span>

## <span data-ttu-id="76d0b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="76d0b-107">EXAMPLES</span></span>

### <span data-ttu-id="76d0b-108">Przykład 1. Ustawianie szczegółów operacji</span><span class="sxs-lookup"><span data-stu-id="76d0b-108">Example 1: Set the operation details</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzureRmApiManagementOperation -Context $apimContext -ApiId $APIID -OperationId $OperationId -Name "Get Resource" -Method GET -UrlTemplate "/newresource" -Description "Use this operation to get newresource"
```

<span data-ttu-id="76d0b-109">To polecenie ustawia szczegóły operacji zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="76d0b-109">This command sets the operation details for API management.</span></span>

## <span data-ttu-id="76d0b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="76d0b-110">PARAMETERS</span></span>

### <span data-ttu-id="76d0b-111">-ApiId</span><span class="sxs-lookup"><span data-stu-id="76d0b-111">-ApiId</span></span>
<span data-ttu-id="76d0b-112">Określa identyfikator interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="76d0b-112">Specifies the identifier of the API.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76d0b-113">-Context</span><span class="sxs-lookup"><span data-stu-id="76d0b-113">-Context</span></span>
<span data-ttu-id="76d0b-114">Określa wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="76d0b-114">Specifies an instance of **PsApiManagementContext**.</span></span>

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

### <span data-ttu-id="76d0b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76d0b-115">-DefaultProfile</span></span>
<span data-ttu-id="76d0b-116">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="76d0b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="76d0b-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="76d0b-117">-Description</span></span>
<span data-ttu-id="76d0b-118">Określa opis nowej operacji.</span><span class="sxs-lookup"><span data-stu-id="76d0b-118">Specifies the description of the new operation.</span></span>

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

### <span data-ttu-id="76d0b-119">-Method</span><span class="sxs-lookup"><span data-stu-id="76d0b-119">-Method</span></span>
<span data-ttu-id="76d0b-120">Określa metodę HTTP nowej operacji.</span><span class="sxs-lookup"><span data-stu-id="76d0b-120">Specifies the HTTP method of the new operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76d0b-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="76d0b-121">-Name</span></span>
<span data-ttu-id="76d0b-122">Określa nazwę wyświetlaną nowej operacji.</span><span class="sxs-lookup"><span data-stu-id="76d0b-122">Specifies the display name of the new operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76d0b-123">-OperationId</span><span class="sxs-lookup"><span data-stu-id="76d0b-123">-OperationId</span></span>
<span data-ttu-id="76d0b-124">Określa identyfikator istniejącej operacji.</span><span class="sxs-lookup"><span data-stu-id="76d0b-124">Specifies the identifier of the existing operation.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76d0b-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76d0b-125">-PassThru</span></span>
<span data-ttu-id="76d0b-126">passthru</span><span class="sxs-lookup"><span data-stu-id="76d0b-126">passthru</span></span>

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

### <span data-ttu-id="76d0b-127">-Request</span><span class="sxs-lookup"><span data-stu-id="76d0b-127">-Request</span></span>
<span data-ttu-id="76d0b-128">Określa szczegóły żądania operacji.</span><span class="sxs-lookup"><span data-stu-id="76d0b-128">Specifies the operation request details.</span></span>

```yaml
Type: PsApiManagementRequest
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76d0b-129">-Odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="76d0b-129">-Responses</span></span>
<span data-ttu-id="76d0b-130">Określa tablicę możliwych odpowiedzi na operacje.</span><span class="sxs-lookup"><span data-stu-id="76d0b-130">Specifies an array of possible operation responses.</span></span>

```yaml
Type: PsApiManagementResponse[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76d0b-131">-TemplateParameters</span><span class="sxs-lookup"><span data-stu-id="76d0b-131">-TemplateParameters</span></span>
<span data-ttu-id="76d0b-132">Określa tablicę lub parametry zdefiniowane w parametrach *UrlTemplate*.</span><span class="sxs-lookup"><span data-stu-id="76d0b-132">Specifies an array or parameters defined in parameter *UrlTemplate*.</span></span>
<span data-ttu-id="76d0b-133">Jeśli wartość nie zostanie określona, zostanie wygenerowana wartość domyślna na podstawie UrlTemplate.</span><span class="sxs-lookup"><span data-stu-id="76d0b-133">If you do not specify a value, a default value will be generated based on the UrlTemplate.</span></span>
<span data-ttu-id="76d0b-134">Za pomocą tego parametru można uzyskać więcej informacji na temat parametrów, takich jak opis, typ i inne możliwe wartości.</span><span class="sxs-lookup"><span data-stu-id="76d0b-134">Use the parameter to give more details on parameters such as description, type, and other possible values.</span></span>

```yaml
Type: PsApiManagementParameter[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76d0b-135">-UrlTemplate</span><span class="sxs-lookup"><span data-stu-id="76d0b-135">-UrlTemplate</span></span>
<span data-ttu-id="76d0b-136">Określa szablon adresu URL.</span><span class="sxs-lookup"><span data-stu-id="76d0b-136">Specifies the URL template.</span></span>
<span data-ttu-id="76d0b-137">Na przykład: Customers/{CID}/Orders/{OID}/? Date = {Date}.</span><span class="sxs-lookup"><span data-stu-id="76d0b-137">For instance: customers/{cid}/orders/{oid}/?date={date}.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76d0b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76d0b-138">CommonParameters</span></span>
<span data-ttu-id="76d0b-139">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="76d0b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76d0b-140">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="76d0b-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76d0b-141">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="76d0b-141">INPUTS</span></span>

### <span data-ttu-id="76d0b-142">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="76d0b-142">None</span></span>
<span data-ttu-id="76d0b-143">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="76d0b-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="76d0b-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="76d0b-144">OUTPUTS</span></span>

### <span data-ttu-id="76d0b-145">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="76d0b-145">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementOperation</span></span>

## <span data-ttu-id="76d0b-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="76d0b-146">NOTES</span></span>

## <span data-ttu-id="76d0b-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="76d0b-147">RELATED LINKS</span></span>

[<span data-ttu-id="76d0b-148">Get-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="76d0b-148">Get-AzureRmApiManagementOperation</span></span>](./Get-AzureRmApiManagementOperation.md)

[<span data-ttu-id="76d0b-149">Nowe — AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="76d0b-149">New-AzureRmApiManagementOperation</span></span>](./New-AzureRmApiManagementOperation.md)

[<span data-ttu-id="76d0b-150">Remove-AzureRmApiManagementOperation</span><span class="sxs-lookup"><span data-stu-id="76d0b-150">Remove-AzureRmApiManagementOperation</span></span>](./Remove-AzureRmApiManagementOperation.md)


