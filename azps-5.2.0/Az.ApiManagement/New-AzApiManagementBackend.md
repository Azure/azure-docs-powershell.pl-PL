---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: 4ed63d0e3b801572698b123038a2022e89672a88
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98358402"
---
# <span data-ttu-id="6a5ec-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6a5ec-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="6a5ec-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="6a5ec-102">SYNOPSIS</span></span>
<span data-ttu-id="6a5ec-103">Tworzy nową jednostkę zaplecza.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="6a5ec-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="6a5ec-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6a5ec-105">Opis</span><span class="sxs-lookup"><span data-stu-id="6a5ec-105">DESCRIPTION</span></span>
<span data-ttu-id="6a5ec-106">Tworzy nową jednostkę zaplecza w zarządzaniu interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="6a5ec-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="6a5ec-107">EXAMPLES</span></span>

### <span data-ttu-id="6a5ec-108">Przykład 1: Tworzenie bazy danych 123 przy użyciu podstawowego schematu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="6a5ec-108">Example 1: Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="6a5ec-109">Tworzy nowy zaplecze</span><span class="sxs-lookup"><span data-stu-id="6a5ec-109">Creates a new Backend</span></span>

## <span data-ttu-id="6a5ec-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="6a5ec-110">PARAMETERS</span></span>

### <span data-ttu-id="6a5ec-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="6a5ec-111">-BackendId</span></span>
<span data-ttu-id="6a5ec-112">Identyfikator nowej wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-112">Identifier of new backend.</span></span>
<span data-ttu-id="6a5ec-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-113">This parameter is optional.</span></span>
<span data-ttu-id="6a5ec-114">Jeśli nie określono, zostanie wygenerowana.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="6a5ec-115">-Context</span><span class="sxs-lookup"><span data-stu-id="6a5ec-115">-Context</span></span>
<span data-ttu-id="6a5ec-116">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="6a5ec-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-117">This parameter is required.</span></span>

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

### <span data-ttu-id="6a5ec-118">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="6a5ec-118">-Credential</span></span>
<span data-ttu-id="6a5ec-119">Szczegóły poświadczeń, które powinny być używane podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="6a5ec-120">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="6a5ec-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a5ec-121">-DefaultProfile</span></span>
<span data-ttu-id="6a5ec-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6a5ec-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="6a5ec-123">-Description</span></span>
<span data-ttu-id="6a5ec-124">Opis zaplecza.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-124">Backend Description.</span></span>
<span data-ttu-id="6a5ec-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="6a5ec-126">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="6a5ec-126">-Protocol</span></span>
<span data-ttu-id="6a5ec-127">Protokół komunikacyjny zaplecza.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-127">Backend Communication protocol.</span></span>
<span data-ttu-id="6a5ec-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-128">This parameter is required.</span></span>
<span data-ttu-id="6a5ec-129">Prawidłowe wartości to "http" i "SOAP".</span><span class="sxs-lookup"><span data-stu-id="6a5ec-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="6a5ec-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="6a5ec-130">-Proxy</span></span>
<span data-ttu-id="6a5ec-131">Szczegóły serwera proxy do użycia podczas wysyłania żądania do wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="6a5ec-132">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="6a5ec-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6a5ec-133">-ResourceId</span></span>
<span data-ttu-id="6a5ec-134">Identyfikator URI zarządzania zasobu w systemie zewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="6a5ec-135">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-135">This parameter is optional.</span></span>
<span data-ttu-id="6a5ec-136">Ten adres URL może być identyfikatorem zasobu ARM aplikacji logicznych, aplikacjami funkcji lub aplikacjami interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="6a5ec-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="6a5ec-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="6a5ec-138">Dane zaplecza klastra usługi Fabric.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="6a5ec-139">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="6a5ec-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="6a5ec-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="6a5ec-141">Określa, czy pominąć sprawdzanie poprawności łańcucha certyfikatu podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="6a5ec-142">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="6a5ec-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="6a5ec-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="6a5ec-144">Określa, czy należy pominąć weryfikację nazwy certyfikatu podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="6a5ec-145">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="6a5ec-146">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="6a5ec-146">-Title</span></span>
<span data-ttu-id="6a5ec-147">Tytuł wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-147">Backend Title.</span></span>
<span data-ttu-id="6a5ec-148">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="6a5ec-149">-URL</span><span class="sxs-lookup"><span data-stu-id="6a5ec-149">-Url</span></span>
<span data-ttu-id="6a5ec-150">Adres URL czasu wykonywania dla wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="6a5ec-151">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-151">This parameter is required.</span></span>

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

### <span data-ttu-id="6a5ec-152">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6a5ec-152">-Confirm</span></span>
<span data-ttu-id="6a5ec-153">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6a5ec-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6a5ec-154">-WhatIf</span></span>
<span data-ttu-id="6a5ec-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6a5ec-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6a5ec-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a5ec-157">CommonParameters</span></span>
<span data-ttu-id="6a5ec-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6a5ec-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6a5ec-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="6a5ec-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a5ec-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6a5ec-160">INPUTS</span></span>

### <span data-ttu-id="6a5ec-161">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="6a5ec-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="6a5ec-162">System. String</span><span class="sxs-lookup"><span data-stu-id="6a5ec-162">System.String</span></span>

### <span data-ttu-id="6a5ec-163">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6a5ec-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6a5ec-164">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="6a5ec-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="6a5ec-165">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="6a5ec-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="6a5ec-166">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="6a5ec-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="6a5ec-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="6a5ec-167">OUTPUTS</span></span>

### <span data-ttu-id="6a5ec-168">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6a5ec-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="6a5ec-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="6a5ec-169">NOTES</span></span>

## <span data-ttu-id="6a5ec-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6a5ec-170">RELATED LINKS</span></span>

[<span data-ttu-id="6a5ec-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6a5ec-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="6a5ec-172">Nowe — AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="6a5ec-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="6a5ec-173">Nowe — AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="6a5ec-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="6a5ec-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6a5ec-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="6a5ec-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="6a5ec-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

