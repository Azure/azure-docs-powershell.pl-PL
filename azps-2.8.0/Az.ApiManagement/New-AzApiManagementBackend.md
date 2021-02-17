---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: f26cb91ef820df6dfa67a0fb5664d4607df8fb21
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399468"
---
# <span data-ttu-id="2c2b9-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2c2b9-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="2c2b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c2b9-102">SYNOPSIS</span></span>
<span data-ttu-id="2c2b9-103">Tworzy nową encję zaplecza.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="2c2b9-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2c2b9-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c2b9-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2c2b9-105">DESCRIPTION</span></span>
<span data-ttu-id="2c2b9-106">Tworzy nową jednostkę zaplecza w zarządzaniu interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="2c2b9-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2c2b9-107">EXAMPLES</span></span>

### <span data-ttu-id="2c2b9-108">Tworzenie bazy danych Backend 123 przy użyciu podstawowego schematu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="2c2b9-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="2c2b9-109">Tworzy nową kopię zapasową</span><span class="sxs-lookup"><span data-stu-id="2c2b9-109">Creates a new Backend</span></span>

## <span data-ttu-id="2c2b9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c2b9-110">PARAMETERS</span></span>

### <span data-ttu-id="2c2b9-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="2c2b9-111">-BackendId</span></span>
<span data-ttu-id="2c2b9-112">Identyfikator nowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-112">Identifier of new backend.</span></span>
<span data-ttu-id="2c2b9-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-113">This parameter is optional.</span></span>
<span data-ttu-id="2c2b9-114">Jeśli nie określono, zostanie wygenerowany.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="2c2b9-115">— kontekst</span><span class="sxs-lookup"><span data-stu-id="2c2b9-115">-Context</span></span>
<span data-ttu-id="2c2b9-116">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="2c2b9-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-117">This parameter is required.</span></span>

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

### <span data-ttu-id="2c2b9-118">- Credential</span><span class="sxs-lookup"><span data-stu-id="2c2b9-118">-Credential</span></span>
<span data-ttu-id="2c2b9-119">Szczegóły poświadczeń, których należy używać podczas rozmowy z zapleczam.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="2c2b9-120">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="2c2b9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c2b9-121">-DefaultProfile</span></span>
<span data-ttu-id="2c2b9-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2c2b9-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="2c2b9-123">-Description</span></span>
<span data-ttu-id="2c2b9-124">Opis zaplecza.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-124">Backend Description.</span></span>
<span data-ttu-id="2c2b9-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="2c2b9-126">— Protokół</span><span class="sxs-lookup"><span data-stu-id="2c2b9-126">-Protocol</span></span>
<span data-ttu-id="2c2b9-127">Protokół komunikacji zaplecza.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-127">Backend Communication protocol.</span></span>
<span data-ttu-id="2c2b9-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-128">This parameter is required.</span></span>
<span data-ttu-id="2c2b9-129">Prawidłowe wartości to "http" i "soap".</span><span class="sxs-lookup"><span data-stu-id="2c2b9-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="2c2b9-130">— serwer proxy</span><span class="sxs-lookup"><span data-stu-id="2c2b9-130">-Proxy</span></span>
<span data-ttu-id="2c2b9-131">Szczegóły serwera proxy, które mają być używane podczas wysyłania żądania do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="2c2b9-132">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="2c2b9-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c2b9-133">-ResourceId</span></span>
<span data-ttu-id="2c2b9-134">Uri zarządzania zasobu w systemie zewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="2c2b9-135">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-135">This parameter is optional.</span></span>
<span data-ttu-id="2c2b9-136">Ten adres URL może być identyfikatorem zasobu arm aplikacji logicznych, aplikacji funkcyjnych lub aplikacji api.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="2c2b9-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="2c2b9-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="2c2b9-138">Szczegóły zaplecza klastrów szkieletów usług.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="2c2b9-139">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="2c2b9-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="2c2b9-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="2c2b9-141">Czy należy pominąć sprawdzanie poprawności łańcucha certyfikatów podczas rozmowy z zapleczam.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="2c2b9-142">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="2c2b9-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="2c2b9-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="2c2b9-144">Czy pominąć sprawdzanie poprawności nazwy certyfikatu podczas mówienia z zapleczam.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="2c2b9-145">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="2c2b9-146">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="2c2b9-146">-Title</span></span>
<span data-ttu-id="2c2b9-147">Tytuł zaplecza.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-147">Backend Title.</span></span>
<span data-ttu-id="2c2b9-148">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="2c2b9-149">— adres URL</span><span class="sxs-lookup"><span data-stu-id="2c2b9-149">-Url</span></span>
<span data-ttu-id="2c2b9-150">Adres URL środowiska uruchomieniowego dla zaplecza.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="2c2b9-151">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-151">This parameter is required.</span></span>

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

### <span data-ttu-id="2c2b9-152">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2c2b9-152">-Confirm</span></span>
<span data-ttu-id="2c2b9-153">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c2b9-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c2b9-154">-WhatIf</span></span>
<span data-ttu-id="2c2b9-155">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2c2b9-156">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c2b9-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c2b9-157">CommonParameters</span></span>
<span data-ttu-id="2c2b9-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2c2b9-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c2b9-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2c2b9-159">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c2b9-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c2b9-160">INPUTS</span></span>

### <span data-ttu-id="2c2b9-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2c2b9-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="2c2b9-162">System.String</span><span class="sxs-lookup"><span data-stu-id="2c2b9-162">System.String</span></span>

### <span data-ttu-id="2c2b9-163">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2c2b9-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2c2b9-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="2c2b9-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="2c2b9-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="2c2b9-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="2c2b9-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="2c2b9-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="2c2b9-167">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2c2b9-167">OUTPUTS</span></span>

### <span data-ttu-id="2c2b9-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2c2b9-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="2c2b9-169">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2c2b9-169">NOTES</span></span>

## <span data-ttu-id="2c2b9-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2c2b9-170">RELATED LINKS</span></span>

[<span data-ttu-id="2c2b9-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2c2b9-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="2c2b9-172">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="2c2b9-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="2c2b9-173">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="2c2b9-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="2c2b9-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2c2b9-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="2c2b9-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="2c2b9-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

