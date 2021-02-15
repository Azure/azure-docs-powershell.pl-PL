---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: 0ac89ed099029fbbabe90e07da7ba9c204449db9
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100400743"
---
# <span data-ttu-id="17f70-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="17f70-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="17f70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17f70-102">SYNOPSIS</span></span>
<span data-ttu-id="17f70-103">Aktualizuje zaplecza.</span><span class="sxs-lookup"><span data-stu-id="17f70-103">Updates a Backend.</span></span>

## <span data-ttu-id="17f70-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="17f70-104">SYNTAX</span></span>

```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17f70-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="17f70-105">DESCRIPTION</span></span>
<span data-ttu-id="17f70-106">Umożliwia aktualizację istniejącej bazy danych w zarządzaniu interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="17f70-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="17f70-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="17f70-107">EXAMPLES</span></span>

### <span data-ttu-id="17f70-108">Aktualizacja opisu bazy danych Backend 123</span><span class="sxs-lookup"><span data-stu-id="17f70-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="17f70-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="17f70-109">PARAMETERS</span></span>

### <span data-ttu-id="17f70-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="17f70-110">-BackendId</span></span>
<span data-ttu-id="17f70-111">Identyfikator nowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="17f70-111">Identifier of new backend.</span></span>
<span data-ttu-id="17f70-112">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="17f70-112">This parameter is required.</span></span>

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

### <span data-ttu-id="17f70-113">— kontekst</span><span class="sxs-lookup"><span data-stu-id="17f70-113">-Context</span></span>
<span data-ttu-id="17f70-114">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="17f70-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="17f70-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="17f70-115">This parameter is required.</span></span>

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

### <span data-ttu-id="17f70-116">- Credential</span><span class="sxs-lookup"><span data-stu-id="17f70-116">-Credential</span></span>
<span data-ttu-id="17f70-117">Szczegóły poświadczeń, których należy używać podczas rozmowy z zapleczam.</span><span class="sxs-lookup"><span data-stu-id="17f70-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="17f70-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="17f70-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="17f70-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17f70-119">-DefaultProfile</span></span>
<span data-ttu-id="17f70-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="17f70-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17f70-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="17f70-121">-Description</span></span>
<span data-ttu-id="17f70-122">Opis zaplecza.</span><span class="sxs-lookup"><span data-stu-id="17f70-122">Backend Description.</span></span>
<span data-ttu-id="17f70-123">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="17f70-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="17f70-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="17f70-124">-PassThru</span></span>
<span data-ttu-id="17f70-125">Wskazuje, że to polecenie cmdlet zwraca polecenie  **PsApiManagementBackend,** które to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="17f70-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="17f70-126">— Protokół</span><span class="sxs-lookup"><span data-stu-id="17f70-126">-Protocol</span></span>
<span data-ttu-id="17f70-127">Protokół komunikacji zaplecza (http lub soap).</span><span class="sxs-lookup"><span data-stu-id="17f70-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="17f70-128">Ten parametr jest opcjonalny</span><span class="sxs-lookup"><span data-stu-id="17f70-128">This parameter is optional</span></span>

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

### <span data-ttu-id="17f70-129">— serwer proxy</span><span class="sxs-lookup"><span data-stu-id="17f70-129">-Proxy</span></span>
<span data-ttu-id="17f70-130">Szczegóły serwera proxy, które mają być używane podczas wysyłania żądania do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="17f70-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="17f70-131">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="17f70-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="17f70-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="17f70-132">-ResourceId</span></span>
<span data-ttu-id="17f70-133">Uri zarządzania zasobu w systemie zewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="17f70-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="17f70-134">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="17f70-134">This parameter is optional.</span></span>
<span data-ttu-id="17f70-135">Ten adres URL może być identyfikatorem zasobu arm aplikacji logicznych, aplikacji funkcyjnych lub aplikacji api.</span><span class="sxs-lookup"><span data-stu-id="17f70-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="17f70-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="17f70-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="17f70-137">Szczegóły zaplecza klastrów szkieletowych usług.</span><span class="sxs-lookup"><span data-stu-id="17f70-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="17f70-138">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="17f70-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="17f70-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="17f70-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="17f70-140">Czy należy pominąć sprawdzanie poprawności łańcucha certyfikatów podczas rozmowy z zapleczam.</span><span class="sxs-lookup"><span data-stu-id="17f70-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="17f70-141">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="17f70-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="17f70-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="17f70-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="17f70-143">Czy pominąć sprawdzanie poprawności nazwy certyfikatu podczas mówienia z zapleczam.</span><span class="sxs-lookup"><span data-stu-id="17f70-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="17f70-144">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="17f70-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="17f70-145">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="17f70-145">-Title</span></span>
<span data-ttu-id="17f70-146">Tytuł zaplecza.</span><span class="sxs-lookup"><span data-stu-id="17f70-146">Backend Title.</span></span>
<span data-ttu-id="17f70-147">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="17f70-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="17f70-148">— adres URL</span><span class="sxs-lookup"><span data-stu-id="17f70-148">-Url</span></span>
<span data-ttu-id="17f70-149">Adres URL środowiska uruchomieniowego dla zaplecza.</span><span class="sxs-lookup"><span data-stu-id="17f70-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="17f70-150">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="17f70-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="17f70-151">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="17f70-151">-Confirm</span></span>
<span data-ttu-id="17f70-152">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="17f70-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17f70-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17f70-153">-WhatIf</span></span>
<span data-ttu-id="17f70-154">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="17f70-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="17f70-155">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="17f70-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17f70-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17f70-156">CommonParameters</span></span>
<span data-ttu-id="17f70-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17f70-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17f70-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17f70-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17f70-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17f70-159">INPUTS</span></span>

### <span data-ttu-id="17f70-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="17f70-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="17f70-161">System.String</span><span class="sxs-lookup"><span data-stu-id="17f70-161">System.String</span></span>

### <span data-ttu-id="17f70-162">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="17f70-162">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="17f70-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="17f70-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="17f70-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="17f70-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="17f70-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="17f70-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="17f70-166">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="17f70-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="17f70-167">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17f70-167">OUTPUTS</span></span>

### <span data-ttu-id="17f70-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="17f70-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="17f70-169">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="17f70-169">NOTES</span></span>

## <span data-ttu-id="17f70-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17f70-170">RELATED LINKS</span></span>

[<span data-ttu-id="17f70-171">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="17f70-171">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="17f70-172">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="17f70-172">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="17f70-173">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="17f70-173">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="17f70-174">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="17f70-174">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="17f70-175">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="17f70-175">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
