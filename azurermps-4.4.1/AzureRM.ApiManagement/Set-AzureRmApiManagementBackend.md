---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: 85545777f5a76f3f75e81648a009ffcdcad8ab30
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718749"
---
# <span data-ttu-id="0c094-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0c094-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="0c094-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0c094-102">SYNOPSIS</span></span>
<span data-ttu-id="0c094-103">Umożliwia zaktualizowanie wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0c094-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0c094-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0c094-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c094-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0c094-105">DESCRIPTION</span></span>
<span data-ttu-id="0c094-106">Umożliwia zaktualizowanie istniejącej wewnętrznej bazy danych w ramach zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="0c094-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="0c094-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0c094-107">EXAMPLES</span></span>

### <span data-ttu-id="0c094-108">Aktualizuje opis wewnętrznej bazy danych 123</span><span class="sxs-lookup"><span data-stu-id="0c094-108">Updates the Description of the Backend 123</span></span>
```
Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="0c094-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0c094-109">PARAMETERS</span></span>

### <span data-ttu-id="0c094-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="0c094-110">-BackendId</span></span>
<span data-ttu-id="0c094-111">Identyfikator nowej wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0c094-111">Identifier of new backend.</span></span>
<span data-ttu-id="0c094-112">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="0c094-112">This parameter is required.</span></span>

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

### <span data-ttu-id="0c094-113">-Context</span><span class="sxs-lookup"><span data-stu-id="0c094-113">-Context</span></span>
<span data-ttu-id="0c094-114">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="0c094-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="0c094-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="0c094-115">This parameter is required.</span></span>

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

### <span data-ttu-id="0c094-116">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="0c094-116">-Credential</span></span>
<span data-ttu-id="0c094-117">Szczegóły poświadczeń, które powinny być używane podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="0c094-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="0c094-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="0c094-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="0c094-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="0c094-119">-Description</span></span>
<span data-ttu-id="0c094-120">Opis zaplecza.</span><span class="sxs-lookup"><span data-stu-id="0c094-120">Backend Description.</span></span>
<span data-ttu-id="0c094-121">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="0c094-121">This parameter is optional.</span></span>

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

### <span data-ttu-id="0c094-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0c094-122">-PassThru</span></span>
<span data-ttu-id="0c094-123">Wskazuje, że to polecenie cmdlet zwróci  **PsApiManagementBackend** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c094-123">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0c094-124">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="0c094-124">-Protocol</span></span>
<span data-ttu-id="0c094-125">Protokół komunikacyjny zaplecza (http lub SOAP).</span><span class="sxs-lookup"><span data-stu-id="0c094-125">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="0c094-126">Ten parametr jest opcjonalny</span><span class="sxs-lookup"><span data-stu-id="0c094-126">This parameter is optional</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 
Accepted values: http, soap

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c094-127">-Proxy</span><span class="sxs-lookup"><span data-stu-id="0c094-127">-Proxy</span></span>
<span data-ttu-id="0c094-128">Szczegóły serwera proxy do użycia podczas wysyłania żądania do wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0c094-128">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="0c094-129">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="0c094-129">This parameter is optional.</span></span>

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

### <span data-ttu-id="0c094-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0c094-130">-ResourceId</span></span>
<span data-ttu-id="0c094-131">Identyfikator URI zarządzania zasobu w systemie zewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="0c094-131">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="0c094-132">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="0c094-132">This parameter is optional.</span></span>
<span data-ttu-id="0c094-133">Ten adres URL może być identyfikatorem zasobu ARM aplikacji logicznych, aplikacjami funkcji lub aplikacjami interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="0c094-133">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="0c094-134">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="0c094-134">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="0c094-135">Określa, czy pominąć sprawdzanie poprawności łańcucha certyfikatu podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="0c094-135">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="0c094-136">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="0c094-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="0c094-137">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="0c094-137">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="0c094-138">Określa, czy należy pominąć weryfikację nazwy certyfikatu podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="0c094-138">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="0c094-139">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="0c094-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="0c094-140">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="0c094-140">-Title</span></span>
<span data-ttu-id="0c094-141">Tytuł wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0c094-141">Backend Title.</span></span>
<span data-ttu-id="0c094-142">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="0c094-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="0c094-143">-URL</span><span class="sxs-lookup"><span data-stu-id="0c094-143">-Url</span></span>
<span data-ttu-id="0c094-144">Adres URL czasu wykonywania dla wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="0c094-144">Runtime Url for the Backend.</span></span>
<span data-ttu-id="0c094-145">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="0c094-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="0c094-146">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0c094-146">-Confirm</span></span>
<span data-ttu-id="0c094-147">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c094-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c094-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c094-148">-WhatIf</span></span>
<span data-ttu-id="0c094-149">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0c094-149">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0c094-150">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0c094-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c094-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c094-151">-DefaultProfile</span></span>
<span data-ttu-id="0c094-152">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="0c094-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0c094-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c094-153">CommonParameters</span></span>
<span data-ttu-id="0c094-154">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c094-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c094-155">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c094-155">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c094-156">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0c094-156">INPUTS</span></span>

## <span data-ttu-id="0c094-157">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0c094-157">OUTPUTS</span></span>

### <span data-ttu-id="0c094-158">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0c094-158">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="0c094-159">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0c094-159">NOTES</span></span>

## <span data-ttu-id="0c094-160">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0c094-160">RELATED LINKS</span></span>

[<span data-ttu-id="0c094-161">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0c094-161">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="0c094-162">Nowe — AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0c094-162">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="0c094-163">Nowe — AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="0c094-163">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="0c094-164">Nowe — AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="0c094-164">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="0c094-165">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="0c094-165">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
