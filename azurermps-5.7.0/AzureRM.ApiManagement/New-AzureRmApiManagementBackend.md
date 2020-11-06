---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: c337e82c88c7fdbbc1f8a3663249126c9d92b19f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553713"
---
# <span data-ttu-id="d784c-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d784c-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="d784c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d784c-102">SYNOPSIS</span></span>
<span data-ttu-id="d784c-103">Tworzy nową jednostkę zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d784c-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d784c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d784c-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d784c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d784c-105">DESCRIPTION</span></span>
<span data-ttu-id="d784c-106">Tworzy nową jednostkę zaplecza w zarządzaniu interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="d784c-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="d784c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d784c-107">EXAMPLES</span></span>

### <span data-ttu-id="d784c-108">Tworzenie bazy danych 123 przy użyciu podstawowego schematu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="d784c-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="d784c-109">Tworzy nowy zaplecze</span><span class="sxs-lookup"><span data-stu-id="d784c-109">Creates a new Backend</span></span>

## <span data-ttu-id="d784c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d784c-110">PARAMETERS</span></span>

### <span data-ttu-id="d784c-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="d784c-111">-BackendId</span></span>
<span data-ttu-id="d784c-112">Identyfikator nowej wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d784c-112">Identifier of new backend.</span></span>
<span data-ttu-id="d784c-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d784c-113">This parameter is optional.</span></span>
<span data-ttu-id="d784c-114">Jeśli nie określono, zostanie wygenerowana.</span><span class="sxs-lookup"><span data-stu-id="d784c-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="d784c-115">-Context</span><span class="sxs-lookup"><span data-stu-id="d784c-115">-Context</span></span>
<span data-ttu-id="d784c-116">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="d784c-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="d784c-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d784c-117">This parameter is required.</span></span>

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

### <span data-ttu-id="d784c-118">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="d784c-118">-Credential</span></span>
<span data-ttu-id="d784c-119">Szczegóły poświadczeń, które powinny być używane podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="d784c-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="d784c-120">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d784c-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="d784c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d784c-121">-DefaultProfile</span></span>
<span data-ttu-id="d784c-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d784c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
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

### <span data-ttu-id="d784c-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="d784c-123">-Description</span></span>
<span data-ttu-id="d784c-124">Opis zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d784c-124">Backend Description.</span></span>
<span data-ttu-id="d784c-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d784c-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="d784c-126">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="d784c-126">-Protocol</span></span>
<span data-ttu-id="d784c-127">Protokół komunikacyjny zaplecza.</span><span class="sxs-lookup"><span data-stu-id="d784c-127">Backend Communication protocol.</span></span>
<span data-ttu-id="d784c-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d784c-128">This parameter is required.</span></span>
<span data-ttu-id="d784c-129">Prawidłowe wartości to "http" i "SOAP".</span><span class="sxs-lookup"><span data-stu-id="d784c-129">Valid values are 'http' and 'soap'.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d784c-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="d784c-130">-Proxy</span></span>
<span data-ttu-id="d784c-131">Szczegóły serwera proxy do użycia podczas wysyłania żądania do wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d784c-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="d784c-132">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d784c-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="d784c-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d784c-133">-ResourceId</span></span>
<span data-ttu-id="d784c-134">Identyfikator URI zarządzania zasobu w systemie zewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="d784c-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="d784c-135">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d784c-135">This parameter is optional.</span></span>
<span data-ttu-id="d784c-136">Ten adres URL może być identyfikatorem zasobu ARM aplikacji logicznych, aplikacjami funkcji lub aplikacjami interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="d784c-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="d784c-137">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="d784c-137">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="d784c-138">Określa, czy pominąć sprawdzanie poprawności łańcucha certyfikatu podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="d784c-138">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="d784c-139">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d784c-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="d784c-140">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="d784c-140">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="d784c-141">Określa, czy należy pominąć weryfikację nazwy certyfikatu podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="d784c-141">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="d784c-142">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d784c-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="d784c-143">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="d784c-143">-Title</span></span>
<span data-ttu-id="d784c-144">Tytuł wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d784c-144">Backend Title.</span></span>
<span data-ttu-id="d784c-145">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d784c-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="d784c-146">-URL</span><span class="sxs-lookup"><span data-stu-id="d784c-146">-Url</span></span>
<span data-ttu-id="d784c-147">Adres URL czasu wykonywania dla wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="d784c-147">Runtime Url for the Backend.</span></span>
<span data-ttu-id="d784c-148">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="d784c-148">This parameter is required.</span></span>

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

### <span data-ttu-id="d784c-149">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="d784c-149">-Confirm</span></span>
<span data-ttu-id="d784c-150">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d784c-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d784c-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d784c-151">-WhatIf</span></span>
<span data-ttu-id="d784c-152">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="d784c-152">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d784c-153">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="d784c-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d784c-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d784c-154">CommonParameters</span></span>
<span data-ttu-id="d784c-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d784c-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d784c-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d784c-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d784c-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d784c-157">INPUTS</span></span>

### <span data-ttu-id="d784c-158">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d784c-158">None</span></span>
<span data-ttu-id="d784c-159">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="d784c-159">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d784c-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d784c-160">OUTPUTS</span></span>

### <span data-ttu-id="d784c-161">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d784c-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="d784c-162">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d784c-162">NOTES</span></span>

## <span data-ttu-id="d784c-163">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d784c-163">RELATED LINKS</span></span>

[<span data-ttu-id="d784c-164">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d784c-164">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="d784c-165">Nowe — AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="d784c-165">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="d784c-166">Nowe — AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="d784c-166">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="d784c-167">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d784c-167">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="d784c-168">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="d784c-168">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

