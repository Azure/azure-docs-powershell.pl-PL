---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: b5e51891f82b2a12f42fac3a1535f974912ca1dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93545840"
---
# <span data-ttu-id="b5190-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b5190-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="b5190-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b5190-102">SYNOPSIS</span></span>
<span data-ttu-id="b5190-103">Umożliwia zaktualizowanie wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b5190-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5190-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b5190-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b5190-105">Opis</span><span class="sxs-lookup"><span data-stu-id="b5190-105">DESCRIPTION</span></span>
<span data-ttu-id="b5190-106">Umożliwia zaktualizowanie istniejącej wewnętrznej bazy danych w ramach zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="b5190-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="b5190-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b5190-107">EXAMPLES</span></span>

### <span data-ttu-id="b5190-108">Aktualizuje opis wewnętrznej bazy danych 123</span><span class="sxs-lookup"><span data-stu-id="b5190-108">Updates the Description of the Backend 123</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="b5190-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b5190-109">PARAMETERS</span></span>

### <span data-ttu-id="b5190-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="b5190-110">-BackendId</span></span>
<span data-ttu-id="b5190-111">Identyfikator nowej wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b5190-111">Identifier of new backend.</span></span>
<span data-ttu-id="b5190-112">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b5190-112">This parameter is required.</span></span>

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

### <span data-ttu-id="b5190-113">-Context</span><span class="sxs-lookup"><span data-stu-id="b5190-113">-Context</span></span>
<span data-ttu-id="b5190-114">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b5190-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b5190-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b5190-115">This parameter is required.</span></span>

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

### <span data-ttu-id="b5190-116">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="b5190-116">-Credential</span></span>
<span data-ttu-id="b5190-117">Szczegóły poświadczeń, które powinny być używane podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="b5190-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="b5190-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b5190-118">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5190-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5190-119">-DefaultProfile</span></span>
<span data-ttu-id="b5190-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b5190-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="b5190-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="b5190-121">-Description</span></span>
<span data-ttu-id="b5190-122">Opis zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b5190-122">Backend Description.</span></span>
<span data-ttu-id="b5190-123">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b5190-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="b5190-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b5190-124">-PassThru</span></span>
<span data-ttu-id="b5190-125">Wskazuje, że to polecenie cmdlet zwróci  **PsApiManagementBackend** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5190-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5190-126">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="b5190-126">-Protocol</span></span>
<span data-ttu-id="b5190-127">Protokół komunikacyjny zaplecza (http lub SOAP).</span><span class="sxs-lookup"><span data-stu-id="b5190-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="b5190-128">Ten parametr jest opcjonalny</span><span class="sxs-lookup"><span data-stu-id="b5190-128">This parameter is optional</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5190-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="b5190-129">-Proxy</span></span>
<span data-ttu-id="b5190-130">Szczegóły serwera proxy do użycia podczas wysyłania żądania do wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b5190-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="b5190-131">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b5190-131">This parameter is optional.</span></span>

```yaml
Type: PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5190-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b5190-132">-ResourceId</span></span>
<span data-ttu-id="b5190-133">Identyfikator URI zarządzania zasobu w systemie zewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="b5190-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="b5190-134">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b5190-134">This parameter is optional.</span></span>
<span data-ttu-id="b5190-135">Ten adres URL może być identyfikatorem zasobu ARM aplikacji logicznych, aplikacjami funkcji lub aplikacjami interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="b5190-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="b5190-136">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="b5190-136">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="b5190-137">Określa, czy pominąć sprawdzanie poprawności łańcucha certyfikatu podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="b5190-137">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="b5190-138">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b5190-138">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5190-139">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="b5190-139">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="b5190-140">Określa, czy należy pominąć weryfikację nazwy certyfikatu podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="b5190-140">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="b5190-141">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b5190-141">This parameter is optional.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b5190-142">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="b5190-142">-Title</span></span>
<span data-ttu-id="b5190-143">Tytuł wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b5190-143">Backend Title.</span></span>
<span data-ttu-id="b5190-144">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b5190-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="b5190-145">-URL</span><span class="sxs-lookup"><span data-stu-id="b5190-145">-Url</span></span>
<span data-ttu-id="b5190-146">Adres URL czasu wykonywania dla wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b5190-146">Runtime Url for the Backend.</span></span>
<span data-ttu-id="b5190-147">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b5190-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="b5190-148">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b5190-148">-Confirm</span></span>
<span data-ttu-id="b5190-149">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5190-149">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5190-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b5190-150">-WhatIf</span></span>
<span data-ttu-id="b5190-151">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b5190-151">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b5190-152">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="b5190-152">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5190-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5190-153">CommonParameters</span></span>
<span data-ttu-id="b5190-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b5190-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5190-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5190-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5190-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b5190-156">INPUTS</span></span>

### <span data-ttu-id="b5190-157">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b5190-157">None</span></span>
<span data-ttu-id="b5190-158">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b5190-158">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b5190-159">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b5190-159">OUTPUTS</span></span>

### <span data-ttu-id="b5190-160">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b5190-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="b5190-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b5190-161">NOTES</span></span>

## <span data-ttu-id="b5190-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b5190-162">RELATED LINKS</span></span>

[<span data-ttu-id="b5190-163">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b5190-163">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="b5190-164">Nowe — AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b5190-164">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="b5190-165">Nowe — AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b5190-165">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="b5190-166">Nowe — AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b5190-166">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="b5190-167">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b5190-167">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
