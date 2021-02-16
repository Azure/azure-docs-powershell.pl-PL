---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementBackend.md
ms.openlocfilehash: cb7348e31ca80834836b27c97aa7f68e4207ed24
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100404330"
---
# <span data-ttu-id="e8549-101">Set-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e8549-101">Set-AzApiManagementBackend</span></span>

## <span data-ttu-id="e8549-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8549-102">SYNOPSIS</span></span>
<span data-ttu-id="e8549-103">Aktualizuje zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e8549-103">Updates a Backend.</span></span>

## <span data-ttu-id="e8549-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e8549-104">SYNTAX</span></span>

### <span data-ttu-id="e8549-105">ContextParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e8549-105">ContextParameterSet (Default)</span></span>
```
Set-AzApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8549-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="e8549-106">ByInputObject</span></span>
```
Set-AzApiManagementBackend -InputObject <PsApiManagementBackend> [-Protocol <String>] [-Url <String>]
 [-ResourceId <String>] [-Title <String>] [-Description <String>] [-SkipCertificateChainValidation <Boolean>]
 [-SkipCertificateNameValidation <Boolean>] [-Credential <PsApiManagementBackendCredential>]
 [-Proxy <PsApiManagementBackendProxy>] [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8549-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e8549-107">DESCRIPTION</span></span>
<span data-ttu-id="e8549-108">Umożliwia aktualizację istniejącej bazy danych w zarządzaniu interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="e8549-108">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="e8549-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e8549-109">EXAMPLES</span></span>

### <span data-ttu-id="e8549-110">Aktualizacja opisu bazy danych Backend 123</span><span class="sxs-lookup"><span data-stu-id="e8549-110">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="e8549-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8549-111">PARAMETERS</span></span>

### <span data-ttu-id="e8549-112">-BackendId</span><span class="sxs-lookup"><span data-stu-id="e8549-112">-BackendId</span></span>
<span data-ttu-id="e8549-113">Identyfikator nowej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="e8549-113">Identifier of new backend.</span></span>
<span data-ttu-id="e8549-114">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e8549-114">This parameter is required.</span></span>

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

### <span data-ttu-id="e8549-115">— kontekst</span><span class="sxs-lookup"><span data-stu-id="e8549-115">-Context</span></span>
<span data-ttu-id="e8549-116">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="e8549-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="e8549-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e8549-117">This parameter is required.</span></span>

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

### <span data-ttu-id="e8549-118">- Credential</span><span class="sxs-lookup"><span data-stu-id="e8549-118">-Credential</span></span>
<span data-ttu-id="e8549-119">Szczegóły poświadczeń, których należy używać podczas rozmowy z zapleczam.</span><span class="sxs-lookup"><span data-stu-id="e8549-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="e8549-120">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e8549-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8549-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8549-121">-DefaultProfile</span></span>
<span data-ttu-id="e8549-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8549-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8549-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="e8549-123">-Description</span></span>
<span data-ttu-id="e8549-124">Opis zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e8549-124">Backend Description.</span></span>
<span data-ttu-id="e8549-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e8549-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8549-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e8549-126">-InputObject</span></span>
<span data-ttu-id="e8549-127">Wystąpienie programu PsApiManagementBackend.</span><span class="sxs-lookup"><span data-stu-id="e8549-127">Instance of PsApiManagementBackend.</span></span> <span data-ttu-id="e8549-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e8549-128">This parameter is required.</span></span>

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

### <span data-ttu-id="e8549-129">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8549-129">-PassThru</span></span>
<span data-ttu-id="e8549-130">Wskazuje, że to polecenie cmdlet zwraca polecenie  **PsApiManagementBackend,** które to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="e8549-130">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e8549-131">— Protokół</span><span class="sxs-lookup"><span data-stu-id="e8549-131">-Protocol</span></span>
<span data-ttu-id="e8549-132">Protokół komunikacji zaplecza (http lub soap).</span><span class="sxs-lookup"><span data-stu-id="e8549-132">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="e8549-133">Ten parametr jest opcjonalny</span><span class="sxs-lookup"><span data-stu-id="e8549-133">This parameter is optional</span></span>

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

### <span data-ttu-id="e8549-134">— serwer proxy</span><span class="sxs-lookup"><span data-stu-id="e8549-134">-Proxy</span></span>
<span data-ttu-id="e8549-135">Szczegóły serwera proxy, które mają być używane podczas wysyłania żądania do zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e8549-135">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="e8549-136">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e8549-136">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8549-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e8549-137">-ResourceId</span></span>
<span data-ttu-id="e8549-138">Uri zarządzania zasobu w systemie zewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="e8549-138">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="e8549-139">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e8549-139">This parameter is optional.</span></span>
<span data-ttu-id="e8549-140">Ten adres URL może być identyfikatorem zasobu arm aplikacji logicznych, aplikacji funkcyjnych lub aplikacji api.</span><span class="sxs-lookup"><span data-stu-id="e8549-140">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="e8549-141">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="e8549-141">-ServiceFabricCluster</span></span>
<span data-ttu-id="e8549-142">Szczegóły zaplecza klastrów szkieletów usług.</span><span class="sxs-lookup"><span data-stu-id="e8549-142">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="e8549-143">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e8549-143">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8549-144">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="e8549-144">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="e8549-145">Czy należy pominąć sprawdzanie poprawności łańcucha certyfikatów podczas rozmowy z zapleczam.</span><span class="sxs-lookup"><span data-stu-id="e8549-145">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="e8549-146">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e8549-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8549-147">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="e8549-147">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="e8549-148">Czy pominąć sprawdzanie poprawności nazwy certyfikatu podczas mówienia z zapleczam.</span><span class="sxs-lookup"><span data-stu-id="e8549-148">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="e8549-149">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e8549-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8549-150">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="e8549-150">-Title</span></span>
<span data-ttu-id="e8549-151">Tytuł zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e8549-151">Backend Title.</span></span>
<span data-ttu-id="e8549-152">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e8549-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8549-153">— adres URL</span><span class="sxs-lookup"><span data-stu-id="e8549-153">-Url</span></span>
<span data-ttu-id="e8549-154">Adres URL środowiska uruchomieniowego dla zaplecza.</span><span class="sxs-lookup"><span data-stu-id="e8549-154">Runtime Url for the Backend.</span></span>
<span data-ttu-id="e8549-155">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="e8549-155">This parameter is optional.</span></span>

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

### <span data-ttu-id="e8549-156">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8549-156">-Confirm</span></span>
<span data-ttu-id="e8549-157">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e8549-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8549-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8549-158">-WhatIf</span></span>
<span data-ttu-id="e8549-159">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8549-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e8549-160">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e8549-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8549-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8549-161">CommonParameters</span></span>
<span data-ttu-id="e8549-162">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8549-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8549-163">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e8549-163">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8549-164">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8549-164">INPUTS</span></span>

### <span data-ttu-id="e8549-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e8549-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e8549-166">System.String</span><span class="sxs-lookup"><span data-stu-id="e8549-166">System.String</span></span>

### <span data-ttu-id="e8549-167">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="e8549-167">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="e8549-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e8549-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="e8549-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e8549-169">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="e8549-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="e8549-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="e8549-171">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="e8549-171">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="e8549-172">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8549-172">OUTPUTS</span></span>

### <span data-ttu-id="e8549-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e8549-173">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="e8549-174">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e8549-174">NOTES</span></span>

## <span data-ttu-id="e8549-175">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8549-175">RELATED LINKS</span></span>

[<span data-ttu-id="e8549-176">Get-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e8549-176">Get-AzApiManagementBackend</span></span>](./Get-AzApiManagementBackend.md)

[<span data-ttu-id="e8549-177">New-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e8549-177">New-AzApiManagementBackend</span></span>](./New-AzApiManagementBackend.md)

[<span data-ttu-id="e8549-178">New-AzApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="e8549-178">New-AzApiManagementBackendCredential</span></span>](./New-AzApiManagementBackendCredential.md)

[<span data-ttu-id="e8549-179">New-AzApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="e8549-179">New-AzApiManagementBackendProxy</span></span>](./New-AzApiManagementBackendProxy.md)

[<span data-ttu-id="e8549-180">Remove-AzApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="e8549-180">Remove-AzApiManagementBackend</span></span>](./Remove-AzApiManagementBackend.md)
