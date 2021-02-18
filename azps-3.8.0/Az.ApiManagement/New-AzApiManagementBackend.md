---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementBackend.md
ms.openlocfilehash: cd9ce1d65a2adf13f0f33620ba41b75f394011b4
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100405418"
---
# <span data-ttu-id="b8940-101">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b8940-101">New-AzApiManagementBackend</span></span>

## <span data-ttu-id="b8940-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b8940-102">SYNOPSIS</span></span>
<span data-ttu-id="b8940-103">Tworzy nową jednostkę zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b8940-103">Creates a new backend entity.</span></span>

## <span data-ttu-id="b8940-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b8940-104">SYNTAX</span></span>

```
New-AzApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b8940-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b8940-105">DESCRIPTION</span></span>
<span data-ttu-id="b8940-106">Tworzy nową jednostkę zaplecza w zarządzaniu interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="b8940-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="b8940-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b8940-107">EXAMPLES</span></span>

### <span data-ttu-id="b8940-108">Tworzenie bazy danych Backend 123 przy użyciu podstawowego schematu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="b8940-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="b8940-109">Tworzy nową kopię zapasową</span><span class="sxs-lookup"><span data-stu-id="b8940-109">Creates a new Backend</span></span>

## <span data-ttu-id="b8940-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b8940-110">PARAMETERS</span></span>

### <span data-ttu-id="b8940-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="b8940-111">-BackendId</span></span>
<span data-ttu-id="b8940-112">Identyfikator nowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="b8940-112">Identifier of new backend.</span></span>
<span data-ttu-id="b8940-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b8940-113">This parameter is optional.</span></span>
<span data-ttu-id="b8940-114">Jeśli nie określono, zostanie wygenerowany.</span><span class="sxs-lookup"><span data-stu-id="b8940-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="b8940-115">— kontekst</span><span class="sxs-lookup"><span data-stu-id="b8940-115">-Context</span></span>
<span data-ttu-id="b8940-116">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b8940-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b8940-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b8940-117">This parameter is required.</span></span>

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

### <span data-ttu-id="b8940-118">- Credential</span><span class="sxs-lookup"><span data-stu-id="b8940-118">-Credential</span></span>
<span data-ttu-id="b8940-119">Szczegóły poświadczeń, których należy używać podczas rozmowy z zapleczam.</span><span class="sxs-lookup"><span data-stu-id="b8940-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="b8940-120">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b8940-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="b8940-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b8940-121">-DefaultProfile</span></span>
<span data-ttu-id="b8940-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b8940-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b8940-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="b8940-123">-Description</span></span>
<span data-ttu-id="b8940-124">Opis zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b8940-124">Backend Description.</span></span>
<span data-ttu-id="b8940-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b8940-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="b8940-126">— Protokół</span><span class="sxs-lookup"><span data-stu-id="b8940-126">-Protocol</span></span>
<span data-ttu-id="b8940-127">Protokół komunikacji zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b8940-127">Backend Communication protocol.</span></span>
<span data-ttu-id="b8940-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b8940-128">This parameter is required.</span></span>
<span data-ttu-id="b8940-129">Prawidłowe wartości to "http" i "soap".</span><span class="sxs-lookup"><span data-stu-id="b8940-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="b8940-130">— serwer proxy</span><span class="sxs-lookup"><span data-stu-id="b8940-130">-Proxy</span></span>
<span data-ttu-id="b8940-131">Szczegóły serwera proxy, które mają być używane podczas wysyłania żądania do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b8940-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="b8940-132">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b8940-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="b8940-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b8940-133">-ResourceId</span></span>
<span data-ttu-id="b8940-134">Uri zarządzania zasobu w systemie zewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="b8940-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="b8940-135">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b8940-135">This parameter is optional.</span></span>
<span data-ttu-id="b8940-136">Ten adres URL może być identyfikatorem zasobu arm aplikacji logicznych, aplikacji funkcyjnych lub aplikacji api.</span><span class="sxs-lookup"><span data-stu-id="b8940-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="b8940-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="b8940-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="b8940-138">Szczegóły zaplecza klastrów szkieletowych usług.</span><span class="sxs-lookup"><span data-stu-id="b8940-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="b8940-139">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b8940-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="b8940-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="b8940-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="b8940-141">Czy należy pominąć sprawdzanie poprawności łańcucha certyfikatów podczas rozmowy z zapleczam.</span><span class="sxs-lookup"><span data-stu-id="b8940-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="b8940-142">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b8940-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="b8940-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="b8940-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="b8940-144">Czy pominąć sprawdzanie poprawności nazwy certyfikatu podczas mówienia z zapleczam.</span><span class="sxs-lookup"><span data-stu-id="b8940-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="b8940-145">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b8940-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="b8940-146">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="b8940-146">-Title</span></span>
<span data-ttu-id="b8940-147">Tytuł zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b8940-147">Backend Title.</span></span>
<span data-ttu-id="b8940-148">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b8940-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="b8940-149">— adres URL</span><span class="sxs-lookup"><span data-stu-id="b8940-149">-Url</span></span>
<span data-ttu-id="b8940-150">Adres URL środowiska uruchomieniowego dla zaplecza.</span><span class="sxs-lookup"><span data-stu-id="b8940-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="b8940-151">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b8940-151">This parameter is required.</span></span>

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

### <span data-ttu-id="b8940-152">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b8940-152">-Confirm</span></span>
<span data-ttu-id="b8940-153">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b8940-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b8940-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b8940-154">-WhatIf</span></span>
<span data-ttu-id="b8940-155">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b8940-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b8940-156">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b8940-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b8940-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b8940-157">CommonParameters</span></span>
<span data-ttu-id="b8940-158">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b8940-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b8940-159">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b8940-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b8940-160">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8940-160">INPUTS</span></span>

### <span data-ttu-id="b8940-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b8940-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b8940-162">System.String</span><span class="sxs-lookup"><span data-stu-id="b8940-162">System.String</span></span>

### <span data-ttu-id="b8940-163">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="b8940-163">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="b8940-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b8940-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="b8940-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b8940-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="b8940-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="b8940-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="b8940-167">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b8940-167">OUTPUTS</span></span>

### <span data-ttu-id="b8940-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b8940-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="b8940-169">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b8940-169">NOTES</span></span>

## <span data-ttu-id="b8940-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b8940-170">RELATED LINKS</span></span>

[<span data-ttu-id="b8940-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b8940-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="b8940-172">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="b8940-172">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="b8940-173">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="b8940-173">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="b8940-174">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b8940-174">Set-AzApiManagementBackend</span></span>](./Set-AzApiManagementBackend.md)

[<span data-ttu-id="b8940-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="b8940-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)

