---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: 144830c2155379683c8568eda6e0d1bc021b38fb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547232"
---
# <span data-ttu-id="bea3d-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="bea3d-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="bea3d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bea3d-102">SYNOPSIS</span></span>
<span data-ttu-id="bea3d-103">Tworzy nową jednostkę zaplecza.</span><span class="sxs-lookup"><span data-stu-id="bea3d-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bea3d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bea3d-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bea3d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="bea3d-105">DESCRIPTION</span></span>
<span data-ttu-id="bea3d-106">Tworzy nową jednostkę zaplecza w zarządzaniu interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="bea3d-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="bea3d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bea3d-107">EXAMPLES</span></span>

### <span data-ttu-id="bea3d-108">Tworzenie bazy danych 123 przy użyciu podstawowego schematu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="bea3d-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```
$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="bea3d-109">Tworzy nowy zaplecze</span><span class="sxs-lookup"><span data-stu-id="bea3d-109">Creates a new Backend</span></span>

## <span data-ttu-id="bea3d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bea3d-110">PARAMETERS</span></span>

### <span data-ttu-id="bea3d-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="bea3d-111">-BackendId</span></span>
<span data-ttu-id="bea3d-112">Identyfikator nowej wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="bea3d-112">Identifier of new backend.</span></span>
<span data-ttu-id="bea3d-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="bea3d-113">This parameter is optional.</span></span>
<span data-ttu-id="bea3d-114">Jeśli nie określono, zostanie wygenerowana.</span><span class="sxs-lookup"><span data-stu-id="bea3d-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="bea3d-115">-Context</span><span class="sxs-lookup"><span data-stu-id="bea3d-115">-Context</span></span>
<span data-ttu-id="bea3d-116">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="bea3d-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="bea3d-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="bea3d-117">This parameter is required.</span></span>

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

### <span data-ttu-id="bea3d-118">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="bea3d-118">-Credential</span></span>
<span data-ttu-id="bea3d-119">Szczegóły poświadczeń, które powinny być używane podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="bea3d-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="bea3d-120">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="bea3d-120">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea3d-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="bea3d-121">-Description</span></span>
<span data-ttu-id="bea3d-122">Opis zaplecza.</span><span class="sxs-lookup"><span data-stu-id="bea3d-122">Backend Description.</span></span>
<span data-ttu-id="bea3d-123">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="bea3d-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="bea3d-124">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="bea3d-124">-Protocol</span></span>
<span data-ttu-id="bea3d-125">Protokół komunikacyjny zaplecza.</span><span class="sxs-lookup"><span data-stu-id="bea3d-125">Backend Communication protocol.</span></span>
<span data-ttu-id="bea3d-126">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="bea3d-126">This parameter is required.</span></span>
<span data-ttu-id="bea3d-127">Prawidłowe wartości to "http" i "SOAP".</span><span class="sxs-lookup"><span data-stu-id="bea3d-127">Valid values are 'http' and 'soap'.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea3d-128">-Proxy</span><span class="sxs-lookup"><span data-stu-id="bea3d-128">-Proxy</span></span>
<span data-ttu-id="bea3d-129">Szczegóły serwera proxy do użycia podczas wysyłania żądania do wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="bea3d-129">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="bea3d-130">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="bea3d-130">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea3d-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="bea3d-131">-ResourceId</span></span>
<span data-ttu-id="bea3d-132">Identyfikator URI zarządzania zasobu w systemie zewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="bea3d-132">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="bea3d-133">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="bea3d-133">This parameter is optional.</span></span>
<span data-ttu-id="bea3d-134">Ten adres URL może być identyfikatorem zasobu ARM aplikacji logicznych, aplikacjami funkcji lub aplikacjami interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="bea3d-134">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="bea3d-135">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="bea3d-135">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="bea3d-136">Określa, czy pominąć sprawdzanie poprawności łańcucha certyfikatu podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="bea3d-136">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="bea3d-137">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="bea3d-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="bea3d-138">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="bea3d-138">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="bea3d-139">Określa, czy należy pominąć weryfikację nazwy certyfikatu podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="bea3d-139">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="bea3d-140">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="bea3d-140">This parameter is optional.</span></span>

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

### <span data-ttu-id="bea3d-141">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="bea3d-141">-Title</span></span>
<span data-ttu-id="bea3d-142">Tytuł wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="bea3d-142">Backend Title.</span></span>
<span data-ttu-id="bea3d-143">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="bea3d-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="bea3d-144">-URL</span><span class="sxs-lookup"><span data-stu-id="bea3d-144">-Url</span></span>
<span data-ttu-id="bea3d-145">Adres URL czasu wykonywania dla wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="bea3d-145">Runtime Url for the Backend.</span></span>
<span data-ttu-id="bea3d-146">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="bea3d-146">This parameter is required.</span></span>

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

### <span data-ttu-id="bea3d-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="bea3d-147">-Confirm</span></span>
<span data-ttu-id="bea3d-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bea3d-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bea3d-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bea3d-149">-WhatIf</span></span>
<span data-ttu-id="bea3d-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bea3d-150">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bea3d-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="bea3d-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bea3d-152">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea3d-152">-DefaultProfile</span></span>
<span data-ttu-id="bea3d-153">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bea3d-153">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bea3d-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea3d-154">CommonParameters</span></span>
<span data-ttu-id="bea3d-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bea3d-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea3d-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bea3d-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea3d-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bea3d-157">INPUTS</span></span>

## <span data-ttu-id="bea3d-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bea3d-158">OUTPUTS</span></span>

### <span data-ttu-id="bea3d-159">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="bea3d-159">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="bea3d-160">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bea3d-160">NOTES</span></span>

## <span data-ttu-id="bea3d-161">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bea3d-161">RELATED LINKS</span></span>

[<span data-ttu-id="bea3d-162">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="bea3d-162">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="bea3d-163">Nowe — AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="bea3d-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="bea3d-164">Nowe — AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="bea3d-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="bea3d-165">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="bea3d-165">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="bea3d-166">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="bea3d-166">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

