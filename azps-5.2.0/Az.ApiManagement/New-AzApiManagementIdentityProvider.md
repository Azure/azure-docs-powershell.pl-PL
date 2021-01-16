---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: 75f6b7cee1517a3f9ae363a7e28df420e18d37ab
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344422"
---
# <span data-ttu-id="686fb-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="686fb-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="686fb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="686fb-102">SYNOPSIS</span></span>
<span data-ttu-id="686fb-103">Tworzy nową konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="686fb-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="686fb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="686fb-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SigninTenant <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="686fb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="686fb-105">DESCRIPTION</span></span>
<span data-ttu-id="686fb-106">Tworzy nową konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="686fb-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="686fb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="686fb-107">EXAMPLES</span></span>

### <span data-ttu-id="686fb-108">Przykład 1: Konfigurowanie serwisu Facebook jako dostawcy tożsamości na potrzeby logowania w portalu dewelopera</span><span class="sxs-lookup"><span data-stu-id="686fb-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="686fb-109">To polecenie konfiguruje tożsamość w serwisie Facebook jako zaakceptowanego dostawcy tożsamości w portalu dewelopera usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="686fb-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="686fb-110">Zajmie to ClientId i ClientSecret aplikacji Facebook.</span><span class="sxs-lookup"><span data-stu-id="686fb-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="686fb-111">Przykład 2: konfiguruje adB2C jako dostawcę tożsamości dla logowania w portalu dewelopera</span><span class="sxs-lookup"><span data-stu-id="686fb-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
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

<span data-ttu-id="686fb-112">To polecenie konfiguruje tożsamość w serwisie Facebook jako zaakceptowanego dostawcy tożsamości w portalu dewelopera usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="686fb-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="686fb-113">Zajmie to ClientId i ClientSecret aplikacji Facebook.</span><span class="sxs-lookup"><span data-stu-id="686fb-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="686fb-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="686fb-114">PARAMETERS</span></span>

### <span data-ttu-id="686fb-115">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="686fb-115">-AllowedTenants</span></span>
<span data-ttu-id="686fb-116">Lista dozwolonych dzierżaw usługi Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="686fb-116">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="686fb-117">-Authority</span><span class="sxs-lookup"><span data-stu-id="686fb-117">-Authority</span></span>
<span data-ttu-id="686fb-118">OpenID Połącz hosta punktu końcowego odnajdowania w usłudze AAD lub AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="686fb-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="686fb-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="686fb-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="686fb-120">-ClientId</span><span class="sxs-lookup"><span data-stu-id="686fb-120">-ClientId</span></span>
<span data-ttu-id="686fb-121">Identyfikator klienta aplikacji w zewnętrznym dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="686fb-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="686fb-122">Jest to identyfikator aplikacji dla logowania do serwisu Facebook, identyfikator klienta Google login, identyfikator aplikacji dla firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="686fb-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="686fb-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="686fb-123">-ClientSecret</span></span>
<span data-ttu-id="686fb-124">Klucz tajny klienta aplikacji w zewnętrznym dostawcy tożsamości, służący do uwierzytelniania żądania logowania.</span><span class="sxs-lookup"><span data-stu-id="686fb-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="686fb-125">Na przykład jest to klucz tajny aplikacji dla logowania do serwisu Facebook, klucz interfejsu API logowania Google, klucz publiczny dla firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="686fb-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="686fb-126">-Context</span><span class="sxs-lookup"><span data-stu-id="686fb-126">-Context</span></span>
<span data-ttu-id="686fb-127">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="686fb-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="686fb-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="686fb-128">This parameter is required.</span></span>

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

### <span data-ttu-id="686fb-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="686fb-129">-DefaultProfile</span></span>
<span data-ttu-id="686fb-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="686fb-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="686fb-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="686fb-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="686fb-132">Nazwa zasady resetowania hasła.</span><span class="sxs-lookup"><span data-stu-id="686fb-132">Password Reset Policy Name.</span></span> <span data-ttu-id="686fb-133">Dotyczy tylko dostawcy tożsamości usługi AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="686fb-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="686fb-134">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="686fb-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="686fb-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="686fb-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="686fb-136">Nazwa zasad edytowania profilu.</span><span class="sxs-lookup"><span data-stu-id="686fb-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="686fb-137">Dotyczy tylko dostawcy tożsamości usługi AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="686fb-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="686fb-138">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="686fb-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="686fb-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="686fb-139">-SigninPolicyName</span></span>
<span data-ttu-id="686fb-140">Nazwa zasady logowanie się.</span><span class="sxs-lookup"><span data-stu-id="686fb-140">Signin Policy Name.</span></span> <span data-ttu-id="686fb-141">Dotyczy tylko dostawcy tożsamości usługi AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="686fb-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="686fb-142">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="686fb-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="686fb-143">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="686fb-143">-SigninTenant</span></span>
<span data-ttu-id="686fb-144">Zaloguj się, aby zastąpić w usłudze AAD B2C zamiast `common` dzierżawy</span><span class="sxs-lookup"><span data-stu-id="686fb-144">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

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

### <span data-ttu-id="686fb-145">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="686fb-145">-SignupPolicyName</span></span>
<span data-ttu-id="686fb-146">Nazwa zasad zapisywania się.</span><span class="sxs-lookup"><span data-stu-id="686fb-146">Signup Policy Name.</span></span> <span data-ttu-id="686fb-147">Dotyczy tylko dostawcy tożsamości usługi AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="686fb-147">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="686fb-148">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="686fb-148">This parameter is optional.</span></span>

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

### <span data-ttu-id="686fb-149">-Type</span><span class="sxs-lookup"><span data-stu-id="686fb-149">-Type</span></span>
<span data-ttu-id="686fb-150">Identyfikator dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="686fb-150">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="686fb-151">Jeśli zostanie określona, spróbuje znaleźć konfigurację dostawcy tożsamości przez identyfikator.</span><span class="sxs-lookup"><span data-stu-id="686fb-151">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="686fb-152">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="686fb-152">This parameter is optional.</span></span>

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

### <span data-ttu-id="686fb-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="686fb-153">-Confirm</span></span>
<span data-ttu-id="686fb-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="686fb-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="686fb-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="686fb-155">-WhatIf</span></span>
<span data-ttu-id="686fb-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="686fb-156">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="686fb-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="686fb-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="686fb-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="686fb-158">CommonParameters</span></span>
<span data-ttu-id="686fb-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="686fb-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="686fb-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="686fb-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="686fb-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="686fb-161">INPUTS</span></span>

### <span data-ttu-id="686fb-162">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="686fb-162">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="686fb-163">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="686fb-163">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="686fb-164">System. String</span><span class="sxs-lookup"><span data-stu-id="686fb-164">System.String</span></span>

### <span data-ttu-id="686fb-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="686fb-165">System.String[]</span></span>

## <span data-ttu-id="686fb-166">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="686fb-166">OUTPUTS</span></span>

### <span data-ttu-id="686fb-167">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="686fb-167">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="686fb-168">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="686fb-168">NOTES</span></span>

## <span data-ttu-id="686fb-169">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="686fb-169">RELATED LINKS</span></span>

[<span data-ttu-id="686fb-170">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="686fb-170">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="686fb-171">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="686fb-171">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="686fb-172">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="686fb-172">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
