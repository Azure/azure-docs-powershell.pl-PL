---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: ce27a151ebb6d778ed647fb81909c44c11edbf8e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869355"
---
# <span data-ttu-id="db0d7-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="db0d7-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="db0d7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="db0d7-102">SYNOPSIS</span></span>
<span data-ttu-id="db0d7-103">Umożliwia zaktualizowanie wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="db0d7-103">Updates a Backend.</span></span>

## <span data-ttu-id="db0d7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="db0d7-104">SYNTAX</span></span>

```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db0d7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="db0d7-105">DESCRIPTION</span></span>
<span data-ttu-id="db0d7-106">Umożliwia zaktualizowanie istniejącej wewnętrznej bazy danych w ramach zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="db0d7-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="db0d7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="db0d7-107">EXAMPLES</span></span>

### <span data-ttu-id="db0d7-108">Aktualizuje opis wewnętrznej bazy danych 123</span><span class="sxs-lookup"><span data-stu-id="db0d7-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="db0d7-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="db0d7-109">PARAMETERS</span></span>

### <span data-ttu-id="db0d7-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="db0d7-110">-BackendId</span></span>
<span data-ttu-id="db0d7-111">Identyfikator nowej wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="db0d7-111">Identifier of new backend.</span></span>
<span data-ttu-id="db0d7-112">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="db0d7-112">This parameter is required.</span></span>

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

### <span data-ttu-id="db0d7-113">-Context</span><span class="sxs-lookup"><span data-stu-id="db0d7-113">-Context</span></span>
<span data-ttu-id="db0d7-114">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="db0d7-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="db0d7-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="db0d7-115">This parameter is required.</span></span>

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

### <span data-ttu-id="db0d7-116">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="db0d7-116">-Credential</span></span>
<span data-ttu-id="db0d7-117">Szczegóły poświadczeń, które powinny być używane podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="db0d7-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="db0d7-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="db0d7-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="db0d7-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db0d7-119">-DefaultProfile</span></span>
<span data-ttu-id="db0d7-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="db0d7-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db0d7-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="db0d7-121">-Description</span></span>
<span data-ttu-id="db0d7-122">Opis zaplecza.</span><span class="sxs-lookup"><span data-stu-id="db0d7-122">Backend Description.</span></span>
<span data-ttu-id="db0d7-123">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="db0d7-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="db0d7-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="db0d7-124">-PassThru</span></span>
<span data-ttu-id="db0d7-125">Wskazuje, że to polecenie cmdlet zwróci  **PsApiManagementBackend** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db0d7-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="db0d7-126">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="db0d7-126">-Protocol</span></span>
<span data-ttu-id="db0d7-127">Protokół komunikacyjny zaplecza (http lub SOAP).</span><span class="sxs-lookup"><span data-stu-id="db0d7-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="db0d7-128">Ten parametr jest opcjonalny</span><span class="sxs-lookup"><span data-stu-id="db0d7-128">This parameter is optional</span></span>

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

### <span data-ttu-id="db0d7-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="db0d7-129">-Proxy</span></span>
<span data-ttu-id="db0d7-130">Szczegóły serwera proxy do użycia podczas wysyłania żądania do wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="db0d7-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="db0d7-131">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="db0d7-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="db0d7-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="db0d7-132">-ResourceId</span></span>
<span data-ttu-id="db0d7-133">Identyfikator URI zarządzania zasobu w systemie zewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="db0d7-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="db0d7-134">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="db0d7-134">This parameter is optional.</span></span>
<span data-ttu-id="db0d7-135">Ten adres URL może być identyfikatorem zasobu ARM aplikacji logicznych, aplikacjami funkcji lub aplikacjami interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="db0d7-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="db0d7-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="db0d7-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="db0d7-137">Dane zaplecza klastra usługi Fabric.</span><span class="sxs-lookup"><span data-stu-id="db0d7-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="db0d7-138">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="db0d7-138">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db0d7-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="db0d7-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="db0d7-140">Określa, czy pominąć sprawdzanie poprawności łańcucha certyfikatu podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="db0d7-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="db0d7-141">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="db0d7-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="db0d7-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="db0d7-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="db0d7-143">Określa, czy należy pominąć weryfikację nazwy certyfikatu podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="db0d7-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="db0d7-144">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="db0d7-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="db0d7-145">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="db0d7-145">-Title</span></span>
<span data-ttu-id="db0d7-146">Tytuł wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="db0d7-146">Backend Title.</span></span>
<span data-ttu-id="db0d7-147">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="db0d7-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="db0d7-148">-URL</span><span class="sxs-lookup"><span data-stu-id="db0d7-148">-Url</span></span>
<span data-ttu-id="db0d7-149">Adres URL czasu wykonywania dla wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="db0d7-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="db0d7-150">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="db0d7-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="db0d7-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="db0d7-151">-Confirm</span></span>
<span data-ttu-id="db0d7-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db0d7-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db0d7-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db0d7-153">-WhatIf</span></span>
<span data-ttu-id="db0d7-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="db0d7-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="db0d7-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="db0d7-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db0d7-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db0d7-156">CommonParameters</span></span>
<span data-ttu-id="db0d7-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="db0d7-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db0d7-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db0d7-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db0d7-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="db0d7-159">INPUTS</span></span>

### <span data-ttu-id="db0d7-160">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="db0d7-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="db0d7-161">System. String</span><span class="sxs-lookup"><span data-stu-id="db0d7-161">System.String</span></span>

### <span data-ttu-id="db0d7-162">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="db0d7-162">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="db0d7-163">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="db0d7-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="db0d7-164">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="db0d7-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="db0d7-165">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="db0d7-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="db0d7-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="db0d7-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="db0d7-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="db0d7-167">OUTPUTS</span></span>

### <span data-ttu-id="db0d7-168">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="db0d7-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="db0d7-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="db0d7-169">NOTES</span></span>

## <span data-ttu-id="db0d7-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="db0d7-170">RELATED LINKS</span></span>

[<span data-ttu-id="db0d7-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="db0d7-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="db0d7-172">Nowe — AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="db0d7-172">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="db0d7-173">Nowe — AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="db0d7-173">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="db0d7-174">Nowe — AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="db0d7-174">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="db0d7-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="db0d7-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
