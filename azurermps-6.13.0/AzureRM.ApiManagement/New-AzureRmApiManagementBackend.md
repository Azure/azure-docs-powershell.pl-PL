---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/new-azurermapimanagementbackend
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementBackend.md
ms.openlocfilehash: 46e0a864bcedd8ac0c23761545f5480eaa4a093a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542044"
---
# <span data-ttu-id="f2485-101">New-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f2485-101">New-AzureRmApiManagementBackend</span></span>

## <span data-ttu-id="f2485-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f2485-102">SYNOPSIS</span></span>
<span data-ttu-id="f2485-103">Tworzy nową jednostkę zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f2485-103">Creates a new backend entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f2485-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f2485-104">SYNTAX</span></span>

```
New-AzureRmApiManagementBackend -Context <PsApiManagementContext> [-BackendId <String>] -Protocol <String>
 -Url <String> [-ResourceId <String>] [-Title <String>] [-Description <String>]
 [-SkipCertificateChainValidation <Boolean>] [-SkipCertificateNameValidation <Boolean>]
 [-Credential <PsApiManagementBackendCredential>] [-Proxy <PsApiManagementBackendProxy>]
 [-ServiceFabricCluster <PsApiManagementServiceFabric>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2485-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f2485-105">DESCRIPTION</span></span>
<span data-ttu-id="f2485-106">Tworzy nową jednostkę zaplecza w zarządzaniu interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="f2485-106">Creates a new backend entity in Api Management.</span></span>

## <span data-ttu-id="f2485-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f2485-107">EXAMPLES</span></span>

### <span data-ttu-id="f2485-108">Tworzenie bazy danych 123 przy użyciu podstawowego schematu autoryzacji</span><span class="sxs-lookup"><span data-stu-id="f2485-108">Create Backend 123 with a Basic Authorization Scheme</span></span>
```powershell
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$credential = New-AzureRmApiManagementBackendCredential -AuthorizationHeaderScheme basic -AuthorizationHeaderParameter opensesame -Query @{"sv" = @('xx', 'bb'); "sr" = @('cc')} -Header @{"x-my-1" = @('val1', 'val2')}

PS C:\>$backend = New-AzureRmApiManagementBackend -Context  $apimContext -BackendId 123 -Url 'https://contoso.com/awesomeapi' -Protocol http -Title "first backend" -SkipCertificateChainValidation $true -Credential $credential -Description "my backend"
```

<span data-ttu-id="f2485-109">Tworzy nowy zaplecze</span><span class="sxs-lookup"><span data-stu-id="f2485-109">Creates a new Backend</span></span>

## <span data-ttu-id="f2485-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f2485-110">PARAMETERS</span></span>

### <span data-ttu-id="f2485-111">-BackendId</span><span class="sxs-lookup"><span data-stu-id="f2485-111">-BackendId</span></span>
<span data-ttu-id="f2485-112">Identyfikator nowej wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f2485-112">Identifier of new backend.</span></span>
<span data-ttu-id="f2485-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f2485-113">This parameter is optional.</span></span>
<span data-ttu-id="f2485-114">Jeśli nie określono, zostanie wygenerowana.</span><span class="sxs-lookup"><span data-stu-id="f2485-114">If not specified will be generated.</span></span>

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

### <span data-ttu-id="f2485-115">-Context</span><span class="sxs-lookup"><span data-stu-id="f2485-115">-Context</span></span>
<span data-ttu-id="f2485-116">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="f2485-116">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="f2485-117">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f2485-117">This parameter is required.</span></span>

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

### <span data-ttu-id="f2485-118">— Poświadczenie</span><span class="sxs-lookup"><span data-stu-id="f2485-118">-Credential</span></span>
<span data-ttu-id="f2485-119">Szczegóły poświadczeń, które powinny być używane podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="f2485-119">Credential details which should be used when talking to the Backend.</span></span>
<span data-ttu-id="f2485-120">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f2485-120">This parameter is optional.</span></span>

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

### <span data-ttu-id="f2485-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2485-121">-DefaultProfile</span></span>
<span data-ttu-id="f2485-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f2485-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f2485-123">— Opis</span><span class="sxs-lookup"><span data-stu-id="f2485-123">-Description</span></span>
<span data-ttu-id="f2485-124">Opis zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f2485-124">Backend Description.</span></span>
<span data-ttu-id="f2485-125">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f2485-125">This parameter is optional.</span></span>

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

### <span data-ttu-id="f2485-126">-Protocol (protokół)</span><span class="sxs-lookup"><span data-stu-id="f2485-126">-Protocol</span></span>
<span data-ttu-id="f2485-127">Protokół komunikacyjny zaplecza.</span><span class="sxs-lookup"><span data-stu-id="f2485-127">Backend Communication protocol.</span></span>
<span data-ttu-id="f2485-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f2485-128">This parameter is required.</span></span>
<span data-ttu-id="f2485-129">Prawidłowe wartości to "http" i "SOAP".</span><span class="sxs-lookup"><span data-stu-id="f2485-129">Valid values are 'http' and 'soap'.</span></span>

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

### <span data-ttu-id="f2485-130">-Proxy</span><span class="sxs-lookup"><span data-stu-id="f2485-130">-Proxy</span></span>
<span data-ttu-id="f2485-131">Szczegóły serwera proxy do użycia podczas wysyłania żądania do wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f2485-131">Proxy Server details to be used while sending request to the Backend.</span></span>
<span data-ttu-id="f2485-132">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f2485-132">This parameter is optional.</span></span>

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

### <span data-ttu-id="f2485-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2485-133">-ResourceId</span></span>
<span data-ttu-id="f2485-134">Identyfikator URI zarządzania zasobu w systemie zewnętrznym.</span><span class="sxs-lookup"><span data-stu-id="f2485-134">Management Uri of the Resource in External System.</span></span>
<span data-ttu-id="f2485-135">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f2485-135">This parameter is optional.</span></span>
<span data-ttu-id="f2485-136">Ten adres URL może być identyfikatorem zasobu ARM aplikacji logicznych, aplikacjami funkcji lub aplikacjami interfejsu API.</span><span class="sxs-lookup"><span data-stu-id="f2485-136">This url can be the Arm Resource Id of Logic Apps, Function Apps or Api Apps.</span></span>

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

### <span data-ttu-id="f2485-137">-ServiceFabricCluster</span><span class="sxs-lookup"><span data-stu-id="f2485-137">-ServiceFabricCluster</span></span>
<span data-ttu-id="f2485-138">Dane zaplecza klastra usługi Fabric.</span><span class="sxs-lookup"><span data-stu-id="f2485-138">Service Fabric Cluster Backend details.</span></span> <span data-ttu-id="f2485-139">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f2485-139">This parameter is optional.</span></span>

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

### <span data-ttu-id="f2485-140">-SkipCertificateChainValidation</span><span class="sxs-lookup"><span data-stu-id="f2485-140">-SkipCertificateChainValidation</span></span>
<span data-ttu-id="f2485-141">Określa, czy pominąć sprawdzanie poprawności łańcucha certyfikatu podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="f2485-141">Whether to Skip Certificate Chain Validation when talking to the Backend.</span></span>
<span data-ttu-id="f2485-142">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f2485-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="f2485-143">-SkipCertificateNameValidation</span><span class="sxs-lookup"><span data-stu-id="f2485-143">-SkipCertificateNameValidation</span></span>
<span data-ttu-id="f2485-144">Określa, czy należy pominąć weryfikację nazwy certyfikatu podczas rozmowy z wewnętrzną zapleczem.</span><span class="sxs-lookup"><span data-stu-id="f2485-144">Whether to skip Certificate Name Validation when talking to the Backend.</span></span>
<span data-ttu-id="f2485-145">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f2485-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="f2485-146">— Tytuł</span><span class="sxs-lookup"><span data-stu-id="f2485-146">-Title</span></span>
<span data-ttu-id="f2485-147">Tytuł wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f2485-147">Backend Title.</span></span>
<span data-ttu-id="f2485-148">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="f2485-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="f2485-149">-URL</span><span class="sxs-lookup"><span data-stu-id="f2485-149">-Url</span></span>
<span data-ttu-id="f2485-150">Adres URL czasu wykonywania dla wewnętrznej bazy danych.</span><span class="sxs-lookup"><span data-stu-id="f2485-150">Runtime Url for the Backend.</span></span>
<span data-ttu-id="f2485-151">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="f2485-151">This parameter is required.</span></span>

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

### <span data-ttu-id="f2485-152">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f2485-152">-Confirm</span></span>
<span data-ttu-id="f2485-153">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2485-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2485-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2485-154">-WhatIf</span></span>
<span data-ttu-id="f2485-155">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f2485-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f2485-156">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f2485-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2485-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2485-157">CommonParameters</span></span>
<span data-ttu-id="f2485-158">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f2485-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2485-159">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f2485-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2485-160">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f2485-160">INPUTS</span></span>

### <span data-ttu-id="f2485-161">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="f2485-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="f2485-162">System. String</span><span class="sxs-lookup"><span data-stu-id="f2485-162">System.String</span></span>

### <span data-ttu-id="f2485-163">System. Nullable "1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f2485-163">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f2485-164">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="f2485-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendCredential</span></span>

### <span data-ttu-id="f2485-165">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="f2485-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackendProxy</span></span>

### <span data-ttu-id="f2485-166">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementServiceFabric</span><span class="sxs-lookup"><span data-stu-id="f2485-166">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementServiceFabric</span></span>

## <span data-ttu-id="f2485-167">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f2485-167">OUTPUTS</span></span>

### <span data-ttu-id="f2485-168">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f2485-168">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementBackend</span></span>

## <span data-ttu-id="f2485-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f2485-169">NOTES</span></span>

## <span data-ttu-id="f2485-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f2485-170">RELATED LINKS</span></span>

[<span data-ttu-id="f2485-171">Get-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f2485-171">Get-AzureRmApiManagementBackend</span></span>](./Get-AzureRmApiManagementBackend)

[<span data-ttu-id="f2485-172">Nowe — AzureRmApiManagementBackendCredential</span><span class="sxs-lookup"><span data-stu-id="f2485-172">New-AzureRmApiManagementBackendCredential</span></span>](./New-AzureRmApiManagementBackendCredential.md)

[<span data-ttu-id="f2485-173">Nowe — AzureRmApiManagementBackendProxy</span><span class="sxs-lookup"><span data-stu-id="f2485-173">New-AzureRmApiManagementBackendProxy</span></span>](./New-AzureRmApiManagementBackendProxy.md)

[<span data-ttu-id="f2485-174">Set-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f2485-174">Set-AzureRmApiManagementBackend</span></span>](./Set-AzureRmApiManagementBackend.md)

[<span data-ttu-id="f2485-175">Remove-AzureRmApiManagementBackend</span><span class="sxs-lookup"><span data-stu-id="f2485-175">Remove-AzureRmApiManagementBackend</span></span>](./Remove-AzureRmApiManagementBackend.md)

