---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 30947e52e5a7afaa8bf2890b95f48f6bb6f36bce
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052825"
---
# <span data-ttu-id="ab69c-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ab69c-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="ab69c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ab69c-102">SYNOPSIS</span></span>
<span data-ttu-id="ab69c-103">Umożliwia zaktualizowanie wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ab69c-103">Updates a Backend.</span></span>

## <span data-ttu-id="ab69c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ab69c-104">SYNTAX</span></span>

### <span data-ttu-id="ab69c-105">ContextParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="ab69c-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ab69c-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="ab69c-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ab69c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="ab69c-107">DESCRIPTION</span></span>
<span data-ttu-id="ab69c-108">Umożliwia zaktualizowanie istniejącej wewnętrznej bazy danych w ramach zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="ab69c-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="ab69c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ab69c-109">EXAMPLES</span></span>

### <span data-ttu-id="ab69c-110">Aktualizuje opis wewnętrznej bazy danych 123</span><span class="sxs-lookup"><span data-stu-id="ab69c-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="ab69c-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ab69c-111">PARAMETERS</span></span>

### <span data-ttu-id="ab69c-112">-BackendId</span><span class="sxs-lookup"><span data-stu-id="ab69c-112">-BackendId</span></span>
<span data-ttu-id="ab69c-113">Identyfikator nowej wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ab69c-113">Identifier of new backend.</span></span>
<span data-ttu-id="ab69c-114">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="ab69c-114">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ab69c-115">-Context</span><span class="sxs-lookup"><span data-stu-id="ab69c-115">-Context</span></span>
<span data-ttu-id="ab69c-116">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="ab69c-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="ab69c-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="ab69c-117">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab69c-118">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="ab69c-118">-Credential</span></span>
<span data-ttu-id="ab69c-119">Szczegóły poświadczeń, które powinny być używane podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="ab69c-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="ab69c-120">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ab69c-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="ab69c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ab69c-121">-DefaultProfile</span></span>
<span data-ttu-id="ab69c-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="ab69c-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ab69c-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="ab69c-123">-Description</span></span>
<span data-ttu-id="ab69c-124">Opis zaplecza.</span><span class="sxs-lookup"><span data-stu-id="ab69c-124">Backend Description.</span></span>
<span data-ttu-id="ab69c-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ab69c-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="ab69c-126">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="ab69c-126">-InputObject</span></span>
<span data-ttu-id="ab69c-127">Wystąpienie PsApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="ab69c-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="ab69c-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="ab69c-128">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ab69c-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ab69c-129">-PassThru</span></span>
<span data-ttu-id="ab69c-130">Wskazuje, że to polecenie cmdlet zwróci  **PsApiManagementBackend** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab69c-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="ab69c-131">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="ab69c-131">-Protocol</span></span>
<span data-ttu-id="ab69c-132">Protokół komunikacyjny zaplecza (http lub SOAP).</span><span class="sxs-lookup"><span data-stu-id="ab69c-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="ab69c-133">Ten parametr jest opcjonalny</span><span class="sxs-lookup"><span data-stu-id="ab69c-133">This parameter is optional</span></span>

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

### <span data-ttu-id="ab69c-134">-Proxy</span><span class="sxs-lookup"><span data-stu-id="ab69c-134">-Proxy</span></span>
<span data-ttu-id="ab69c-135">Szczegóły serwera proxy do użycia podczas wysyłania żądania do wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ab69c-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="ab69c-136">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ab69c-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="ab69c-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ab69c-137">-ResourceId</span></span>
<span data-ttu-id="ab69c-138">Identyfikator URI zarządzania zasobu w systemie zewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="ab69c-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="ab69c-139">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ab69c-139">This parameter is optional.</span></span>
<span data-ttu-id="ab69c-140">Ten adres URL może być identyfikatorem zasobu ARM aplikacji logicznych, aplikacjami funkcji lub aplikacjami interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="ab69c-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="ab69c-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="ab69c-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="ab69c-142">Dane zaplecza klastra usługi Fabric.</span><span class="sxs-lookup"><span data-stu-id="ab69c-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="ab69c-143">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ab69c-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="ab69c-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="ab69c-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="ab69c-145">Określa, czy pominąć sprawdzanie poprawności łańcucha certyfikatu podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="ab69c-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="ab69c-146">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ab69c-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="ab69c-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="ab69c-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="ab69c-148">Określa, czy należy pominąć weryfikację nazwy certyfikatu podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="ab69c-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="ab69c-149">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ab69c-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="ab69c-150">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="ab69c-150">-Title</span></span>
<span data-ttu-id="ab69c-151">Tytuł wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ab69c-151">Backend Title.</span></span>
<span data-ttu-id="ab69c-152">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ab69c-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="ab69c-153">-URL</span><span class="sxs-lookup"><span data-stu-id="ab69c-153">-Url</span></span>
<span data-ttu-id="ab69c-154">Adres URL czasu wykonywania dla wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="ab69c-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="ab69c-155">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="ab69c-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="ab69c-156">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ab69c-156">-Confirm</span></span>
<span data-ttu-id="ab69c-157">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab69c-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ab69c-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ab69c-158">-WhatIf</span></span>
<span data-ttu-id="ab69c-159">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ab69c-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ab69c-160">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ab69c-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ab69c-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ab69c-161">CommonParameters</span></span>
<span data-ttu-id="ab69c-162">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ab69c-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ab69c-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ab69c-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ab69c-164">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ab69c-164">INPUTS</span></span>

### <span data-ttu-id="ab69c-165">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="ab69c-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="ab69c-166">System. String</span><span class="sxs-lookup"><span data-stu-id="ab69c-166">System.String</span></span>

### <span data-ttu-id="ab69c-167">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ab69c-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="ab69c-168">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="ab69c-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="ab69c-169">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ab69c-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="ab69c-170">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="ab69c-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="ab69c-171">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="ab69c-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="ab69c-172">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ab69c-172">OUTPUTS</span></span>

### <span data-ttu-id="ab69c-173">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ab69c-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="ab69c-174">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ab69c-174">NOTES</span></span>

## <span data-ttu-id="ab69c-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ab69c-175">RELATED LINKS</span></span>

[<span data-ttu-id="ab69c-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ab69c-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend)

[<span data-ttu-id="ab69c-177">Nowe — AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ab69c-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="ab69c-178">Nowe — AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="ab69c-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="ab69c-179">Nowe — AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="ab69c-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="ab69c-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="ab69c-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
