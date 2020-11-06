---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/set-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Set-AzureRmApiManagementBackend.md
ms.openlocfilehash: 52e159ae0f9d1b94b316394ddefe04f0bd8aa1c8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524690"
---
# <span data-ttu-id="df0a9-101">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="df0a9-101">Set-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="df0a9-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="df0a9-102">SYNOPSIS</span></span>
<span data-ttu-id="df0a9-103">Umożliwia zaktualizowanie wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="df0a9-103">Updates a Backend.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="df0a9-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="df0a9-104">SYNTAX</span></span>

```
Set-AzureRmApiManagementBackend -Context <PsApiManagementContext> -BackendId <String> [-Protocol <String>]
 [-Url <String>] [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df0a9-105">Opis</span><span class="sxs-lookup"><span data-stu-id="df0a9-105">DESCRIPTION</span></span>
<span data-ttu-id="df0a9-106">Umożliwia zaktualizowanie istniejącej wewnętrznej bazy danych w ramach zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="df0a9-106">Updates an existing backend in the Api Management.</span></span>

## <span data-ttu-id="df0a9-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="df0a9-107">EXAMPLES</span></span>

### <span data-ttu-id="df0a9-108">Aktualizuje opis wewnętrznej bazy danych 123</span><span class="sxs-lookup"><span data-stu-id="df0a9-108">Updates the Description of the Backend 123</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Set-AzureRmApiManagementBackend -Context $apimContext -BackendId 123 -Description "updated description" -PassThru
```

## <span data-ttu-id="df0a9-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="df0a9-109">PARAMETERS</span></span>

### <span data-ttu-id="df0a9-110">-BackendId</span><span class="sxs-lookup"><span data-stu-id="df0a9-110">-BackendId</span></span>
<span data-ttu-id="df0a9-111">Identyfikator nowej wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="df0a9-111">Identifier of new backend.</span></span>
<span data-ttu-id="df0a9-112">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="df0a9-112">This parameter is required.</span></span>

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

### <span data-ttu-id="df0a9-113">-Context</span><span class="sxs-lookup"><span data-stu-id="df0a9-113">-Context</span></span>
<span data-ttu-id="df0a9-114">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="df0a9-114">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="df0a9-115">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="df0a9-115">This parameter is required.</span></span>

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

### <span data-ttu-id="df0a9-116">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="df0a9-116">-Credential</span></span>
<span data-ttu-id="df0a9-117">Szczegóły poświadczeń, które powinny być używane podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="df0a9-117">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="df0a9-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="df0a9-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="df0a9-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df0a9-119">-DefaultProfile</span></span>
<span data-ttu-id="df0a9-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="df0a9-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="df0a9-121">— Opis</span><span class="sxs-lookup"><span data-stu-id="df0a9-121">-Description</span></span>
<span data-ttu-id="df0a9-122">Opis zaplecza.</span><span class="sxs-lookup"><span data-stu-id="df0a9-122">Backend Description.</span></span>
<span data-ttu-id="df0a9-123">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="df0a9-123">This parameter is optional.</span></span>

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

### <span data-ttu-id="df0a9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="df0a9-124">-PassThru</span></span>
<span data-ttu-id="df0a9-125">Wskazuje, że to polecenie cmdlet zwróci  **PsApiManagementBackend** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df0a9-125">Indicates that this cmdlet returns the  **PsApiManagementBackend** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="df0a9-126">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="df0a9-126">-Protocol</span></span>
<span data-ttu-id="df0a9-127">Protokół komunikacyjny zaplecza (http lub SOAP).</span><span class="sxs-lookup"><span data-stu-id="df0a9-127">Backend Communication protocol (http or soap).</span></span>
<span data-ttu-id="df0a9-128">Ten parametr jest opcjonalny</span><span class="sxs-lookup"><span data-stu-id="df0a9-128">This parameter is optional</span></span>

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

### <span data-ttu-id="df0a9-129">-Proxy</span><span class="sxs-lookup"><span data-stu-id="df0a9-129">-Proxy</span></span>
<span data-ttu-id="df0a9-130">Szczegóły serwera proxy do użycia podczas wysyłania żądania do wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="df0a9-130">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="df0a9-131">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="df0a9-131">This parameter is optional.</span></span>

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

### <span data-ttu-id="df0a9-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="df0a9-132">-ResourceId</span></span>
<span data-ttu-id="df0a9-133">Identyfikator URI zarządzania zasobu w systemie zewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="df0a9-133">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="df0a9-134">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="df0a9-134">This parameter is optional.</span></span>
<span data-ttu-id="df0a9-135">Ten adres URL może być identyfikatorem zasobu ARM aplikacji logicznych, aplikacjami funkcji lub aplikacjami interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="df0a9-135">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="df0a9-136">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="df0a9-136">-ServiceFabricCluster</span></span>
<span data-ttu-id="df0a9-137">Dane zaplecza klastra usługi Fabric.</span><span class="sxs-lookup"><span data-stu-id="df0a9-137">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="df0a9-138">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="df0a9-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="df0a9-139">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="df0a9-139">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="df0a9-140">Określa, czy pominąć sprawdzanie poprawności łańcucha certyfikatu podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="df0a9-140">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="df0a9-141">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="df0a9-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="df0a9-142">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="df0a9-142">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="df0a9-143">Określa, czy należy pominąć weryfikację nazwy certyfikatu podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="df0a9-143">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="df0a9-144">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="df0a9-144">This parameter is optional.</span></span>

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

### <span data-ttu-id="df0a9-145">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="df0a9-145">-Title</span></span>
<span data-ttu-id="df0a9-146">Tytuł wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="df0a9-146">Backend Title.</span></span>
<span data-ttu-id="df0a9-147">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="df0a9-147">This parameter is optional.</span></span>

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

### <span data-ttu-id="df0a9-148">-URL</span><span class="sxs-lookup"><span data-stu-id="df0a9-148">-Url</span></span>
<span data-ttu-id="df0a9-149">Adres URL czasu wykonywania dla wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="df0a9-149">Runtime Url for the Backend.</span></span>
<span data-ttu-id="df0a9-150">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="df0a9-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="df0a9-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="df0a9-151">-Confirm</span></span>
<span data-ttu-id="df0a9-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df0a9-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df0a9-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df0a9-153">-WhatIf</span></span>
<span data-ttu-id="df0a9-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="df0a9-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="df0a9-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="df0a9-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df0a9-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df0a9-156">CommonParameters</span></span>
<span data-ttu-id="df0a9-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="df0a9-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df0a9-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df0a9-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df0a9-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="df0a9-159">INPUTS</span></span>

### <span data-ttu-id="df0a9-160">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="df0a9-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="df0a9-161">System. String</span><span class="sxs-lookup"><span data-stu-id="df0a9-161">System.String</span></span>

### <span data-ttu-id="df0a9-162">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="df0a9-162">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="df0a9-163">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="df0a9-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="df0a9-164">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="df0a9-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="df0a9-165">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="df0a9-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

### <span data-ttu-id="df0a9-166">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="df0a9-166">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="df0a9-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="df0a9-167">OUTPUTS</span></span>

### <span data-ttu-id="df0a9-168">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="df0a9-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="df0a9-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="df0a9-169">NOTES</span></span>

## <span data-ttu-id="df0a9-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="df0a9-170">RELATED LINKS</span></span>

[<span data-ttu-id="df0a9-171">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="df0a9-171">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="df0a9-172">Nowe — AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="df0a9-172">New-AzureRmApiManagementBackend</span></span>](./New-AzureRmApiManagementBackend.md)

[<span data-ttu-id="df0a9-173">Nowe — AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="df0a9-173">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="df0a9-174">Nowe — AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="df0a9-174">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="df0a9-175">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="df0a9-175">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)
