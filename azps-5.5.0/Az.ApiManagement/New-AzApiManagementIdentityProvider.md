---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 75f6b7cee1517a3f9ae363a7e28df420e18d37ab
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190378"
---
# <span data-ttu-id="52fa2-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="52fa2-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="52fa2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52fa2-102">SYNOPSIS</span></span>
<span data-ttu-id="52fa2-103">Tworzy nową konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="52fa2-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="52fa2-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="52fa2-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SigninTenant <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="52fa2-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="52fa2-105">DESCRIPTION</span></span>
<span data-ttu-id="52fa2-106">Tworzy nową konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="52fa2-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="52fa2-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="52fa2-107">EXAMPLES</span></span>

### <span data-ttu-id="52fa2-108">Przykład 1. Konfigurowanie serwisu Facebook jako dostawcy tożsamości dla logowania w portalu dewelopera</span><span class="sxs-lookup"><span data-stu-id="52fa2-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="52fa2-109">To polecenie konfiguruje tożsamość serwisu Facebook jako zaakceptowanego dostawcę tożsamości w portalu dewelopera usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="52fa2-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="52fa2-110">Przyjmuje to jako dane wejściowe ClientId i ClientSecret aplikacji facebook.</span><span class="sxs-lookup"><span data-stu-id="52fa2-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="52fa2-111">Przykład 2. Konfigurowanie usługi adB2C jako dostawcy tożsamości dla logowania w portalu dewelopera</span><span class="sxs-lookup"><span data-stu-id="52fa2-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $context -Type AadB2C -ClientId 6b1fc750-9e68-450c-97d2-ba6acd0fbc20 -ClientSecret "foobar" -AllowedTenants 'samirtestbc.onmicrosoft.com' -SignupPolicyName B2C_1_signup-policy

Type                     : AadB2C
ClientId                 : 6b1fc750-9e68-450c-97d2-ba6acd0fbc20
ClientSecret             : foobar
AllowedTenants           : {samirtestbc.onmicrosoft.com}
Authority                : login.microsoftonline.com
SignupPolicyName         : B2C_1_signup-policy
SigninPolicyName         :
ProfileEditingPolicyName :
PasswordResetPolicyName  :
Id                       : /subscriptions/subid/resourceGroups/Api-Default-WestUS/providers/Microsoft.ApiManagement/service/contoso/identityProviders/AadB2C
ResourceGroupName        : Api-Default-WestUS
ServiceName              : contoso
```

<span data-ttu-id="52fa2-112">To polecenie konfiguruje tożsamość serwisu Facebook jako zaakceptowanego dostawcę tożsamości w portalu dewelopera usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="52fa2-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="52fa2-113">Przyjmuje to jako dane wejściowe ClientId i ClientSecret aplikacji facebook.</span><span class="sxs-lookup"><span data-stu-id="52fa2-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="52fa2-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="52fa2-114">PARAMETERS</span></span>

### <span data-ttu-id="52fa2-115">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="52fa2-115">-AllowedTenants</span></span>
<span data-ttu-id="52fa2-116">Lista dozwolonych dzierżaw usługi Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="52fa2-116">List of allowed Azure Active Directory Tenants</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52fa2-117">— Urząd</span><span class="sxs-lookup"><span data-stu-id="52fa2-117">-Authority</span></span>
<span data-ttu-id="52fa2-118">Nazwa hosta punktu końcowego odnajdowania OpenID Connect dla AAD lub AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="52fa2-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="52fa2-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="52fa2-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="52fa2-120">-ClientId</span><span class="sxs-lookup"><span data-stu-id="52fa2-120">-ClientId</span></span>
<span data-ttu-id="52fa2-121">Identyfikator klienta aplikacji u zewnętrznego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="52fa2-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="52fa2-122">Jest to identyfikator aplikacji do logowania do serwisu Facebook, identyfikator klienta logowania Google, identyfikator aplikacji firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="52fa2-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="52fa2-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="52fa2-123">-ClientSecret</span></span>
<span data-ttu-id="52fa2-124">Klucz tajny klienta aplikacji w zewnętrznym dostawcy tożsamości używany do uwierzytelniania żądania logowania.</span><span class="sxs-lookup"><span data-stu-id="52fa2-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="52fa2-125">Na przykład nazwa ta jest kluczem tajnym aplikacji do logowania do serwisu Facebook, kluczem API logowania firmy Google, kluczem publicznym firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="52fa2-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="52fa2-126">— kontekst</span><span class="sxs-lookup"><span data-stu-id="52fa2-126">-Context</span></span>
<span data-ttu-id="52fa2-127">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="52fa2-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="52fa2-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="52fa2-128">This parameter is required.</span></span>

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

### <span data-ttu-id="52fa2-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52fa2-129">-DefaultProfile</span></span>
<span data-ttu-id="52fa2-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="52fa2-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52fa2-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="52fa2-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="52fa2-132">Nazwa zasad resetowania hasła.</span><span class="sxs-lookup"><span data-stu-id="52fa2-132">Password Reset Policy Name.</span></span> <span data-ttu-id="52fa2-133">Dotyczy tylko dostawcy tożsamości B2C AAD.</span><span class="sxs-lookup"><span data-stu-id="52fa2-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="52fa2-134">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="52fa2-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="52fa2-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="52fa2-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="52fa2-136">Nazwa zasad edytowania profilu.</span><span class="sxs-lookup"><span data-stu-id="52fa2-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="52fa2-137">Dotyczy tylko dostawcy tożsamości B2C AAD.</span><span class="sxs-lookup"><span data-stu-id="52fa2-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="52fa2-138">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="52fa2-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="52fa2-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="52fa2-139">-SigninPolicyName</span></span>
<span data-ttu-id="52fa2-140">Nazwa zasad logowania.</span><span class="sxs-lookup"><span data-stu-id="52fa2-140">Signin Policy Name.</span></span> <span data-ttu-id="52fa2-141">Dotyczy tylko dostawcy tożsamości B2C AAD.</span><span class="sxs-lookup"><span data-stu-id="52fa2-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="52fa2-142">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="52fa2-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="52fa2-143">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="52fa2-143">-SigninTenant</span></span>
<span data-ttu-id="52fa2-144">Dzierżawa logowania do zastępowania w AAD B2C zamiast w `common` dzierżawie</span><span class="sxs-lookup"><span data-stu-id="52fa2-144">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

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

### <span data-ttu-id="52fa2-145">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="52fa2-145">-SignupPolicyName</span></span>
<span data-ttu-id="52fa2-146">Nazwa zasad rejestracji.</span><span class="sxs-lookup"><span data-stu-id="52fa2-146">Signup Policy Name.</span></span> <span data-ttu-id="52fa2-147">Dotyczy tylko dostawcy tożsamości B2C AAD.</span><span class="sxs-lookup"><span data-stu-id="52fa2-147">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="52fa2-148">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="52fa2-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="52fa2-149">— Wpisz</span><span class="sxs-lookup"><span data-stu-id="52fa2-149">-Type</span></span>
<span data-ttu-id="52fa2-150">Identyfikator dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="52fa2-150">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="52fa2-151">Jeśli zostanie określona, spróbuje znaleźć konfigurację dostawcy tożsamości za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="52fa2-151">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="52fa2-152">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="52fa2-152">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: (All)
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="52fa2-153">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="52fa2-153">-Confirm</span></span>
<span data-ttu-id="52fa2-154">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="52fa2-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="52fa2-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="52fa2-155">-WhatIf</span></span>
<span data-ttu-id="52fa2-156">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="52fa2-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="52fa2-157">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="52fa2-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="52fa2-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52fa2-158">CommonParameters</span></span>
<span data-ttu-id="52fa2-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="52fa2-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52fa2-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="52fa2-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52fa2-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52fa2-161">INPUTS</span></span>

### <span data-ttu-id="52fa2-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="52fa2-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="52fa2-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="52fa2-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="52fa2-164">System.String</span><span class="sxs-lookup"><span data-stu-id="52fa2-164">System.String</span></span>

### <span data-ttu-id="52fa2-165">System.String[]</span><span class="sxs-lookup"><span data-stu-id="52fa2-165">System.String[]</span></span>

## <span data-ttu-id="52fa2-166">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="52fa2-166">OUTPUTS</span></span>

### <span data-ttu-id="52fa2-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="52fa2-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="52fa2-168">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="52fa2-168">NOTES</span></span>

## <span data-ttu-id="52fa2-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="52fa2-169">RELATED LINKS</span></span>

[<span data-ttu-id="52fa2-170">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="52fa2-170">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="52fa2-171">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="52fa2-171">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="52fa2-172">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="52fa2-172">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
