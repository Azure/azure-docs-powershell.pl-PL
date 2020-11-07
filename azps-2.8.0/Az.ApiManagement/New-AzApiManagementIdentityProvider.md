---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementIdentityProvider.md
ms.openlocfilehash: fc033eb1989838d8ed8e20d568f92ef20f8275e8
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707007"
---
# <span data-ttu-id="c436a-101">New-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c436a-101">New-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="c436a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c436a-102">SYNOPSIS</span></span>
<span data-ttu-id="c436a-103">Tworzy nową konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="c436a-103">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="c436a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c436a-104">SYNTAX</span></span>

```
New-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> -ClientId <String> -ClientSecret <String>
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c436a-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c436a-105">DESCRIPTION</span></span>
<span data-ttu-id="c436a-106">Tworzy nową konfigurację dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="c436a-106">Creates a new Identity Provider configuration.</span></span>

## <span data-ttu-id="c436a-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c436a-107">EXAMPLES</span></span>

### <span data-ttu-id="c436a-108">Przykład 1: Konfigurowanie serwisu Facebook jako dostawcy tożsamości na potrzeby logowania w portalu dewelopera</span><span class="sxs-lookup"><span data-stu-id="c436a-108">Example 1: Configures Facebook as an identity Provider for Developer Portal Logins</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>New-AzApiManagementIdentityProvider -Context $apimContext -Type 'Facebook' -ClientId 'sdfsfwerwerw' -ClientSecret 'sdgsdfgfst43tewfewrf'
```

<span data-ttu-id="c436a-109">To polecenie konfiguruje tożsamość w serwisie Facebook jako zaakceptowanego dostawcy tożsamości w portalu dewelopera usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="c436a-109">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="c436a-110">Zajmie to ClientId i ClientSecret aplikacji Facebook.</span><span class="sxs-lookup"><span data-stu-id="c436a-110">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

### <span data-ttu-id="c436a-111">Przykład 2: konfiguruje adB2C jako dostawcę tożsamości dla logowania w portalu dewelopera</span><span class="sxs-lookup"><span data-stu-id="c436a-111">Example 2: Configures adB2C as an identity Provider for Developer Portal Logins</span></span>
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

<span data-ttu-id="c436a-112">To polecenie konfiguruje tożsamość w serwisie Facebook jako zaakceptowanego dostawcy tożsamości w portalu dewelopera usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="c436a-112">This command configures Facebook Identity as a accepted Identity Provider on the Developer Portal of the ApiManagement service.</span></span>
<span data-ttu-id="c436a-113">Zajmie to ClientId i ClientSecret aplikacji Facebook.</span><span class="sxs-lookup"><span data-stu-id="c436a-113">This takes as input the ClientId and ClientSecret of the Facebook app.</span></span>

## <span data-ttu-id="c436a-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c436a-114">PARAMETERS</span></span>

### <span data-ttu-id="c436a-115">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="c436a-115">-AllowedTenants</span></span>
<span data-ttu-id="c436a-116">Lista dozwolonych dzierżaw usługi Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="c436a-116">List of allowed Azure Active Directory Tenants</span></span>

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

### <span data-ttu-id="c436a-117">-Authority</span><span class="sxs-lookup"><span data-stu-id="c436a-117">-Authority</span></span>
<span data-ttu-id="c436a-118">OpenID Połącz hosta punktu końcowego odnajdowania w usłudze AAD lub AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="c436a-118">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="c436a-119">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c436a-119">This parameter is optional.</span></span>

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

### <span data-ttu-id="c436a-120">-ClientId</span><span class="sxs-lookup"><span data-stu-id="c436a-120">-ClientId</span></span>
<span data-ttu-id="c436a-121">Identyfikator klienta aplikacji w zewnętrznym dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="c436a-121">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="c436a-122">Jest to identyfikator aplikacji dla logowania do serwisu Facebook, identyfikator klienta Google login, identyfikator aplikacji dla firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c436a-122">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="c436a-123">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="c436a-123">-ClientSecret</span></span>
<span data-ttu-id="c436a-124">Klucz tajny klienta aplikacji w zewnętrznym dostawcy tożsamości, służący do uwierzytelniania żądania logowania.</span><span class="sxs-lookup"><span data-stu-id="c436a-124">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="c436a-125">Na przykład jest to klucz tajny aplikacji dla logowania do serwisu Facebook, klucz interfejsu API logowania Google, klucz publiczny dla firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c436a-125">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="c436a-126">-Context</span><span class="sxs-lookup"><span data-stu-id="c436a-126">-Context</span></span>
<span data-ttu-id="c436a-127">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="c436a-127">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="c436a-128">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="c436a-128">This parameter is required.</span></span>

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

### <span data-ttu-id="c436a-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c436a-129">-DefaultProfile</span></span>
<span data-ttu-id="c436a-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c436a-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c436a-131">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="c436a-131">-PasswordResetPolicyName</span></span>
<span data-ttu-id="c436a-132">Nazwa zasady resetowania hasła.</span><span class="sxs-lookup"><span data-stu-id="c436a-132">Password Reset Policy Name.</span></span> <span data-ttu-id="c436a-133">Dotyczy tylko dostawcy tożsamości usługi AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="c436a-133">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="c436a-134">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c436a-134">This parameter is optional.</span></span>

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

### <span data-ttu-id="c436a-135">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="c436a-135">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="c436a-136">Nazwa zasad edytowania profilu.</span><span class="sxs-lookup"><span data-stu-id="c436a-136">Profile Editing Policy Name.</span></span> <span data-ttu-id="c436a-137">Dotyczy tylko dostawcy tożsamości usługi AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="c436a-137">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="c436a-138">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c436a-138">This parameter is optional.</span></span>

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

### <span data-ttu-id="c436a-139">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="c436a-139">-SigninPolicyName</span></span>
<span data-ttu-id="c436a-140">Nazwa zasady logowanie się.</span><span class="sxs-lookup"><span data-stu-id="c436a-140">Signin Policy Name.</span></span> <span data-ttu-id="c436a-141">Dotyczy tylko dostawcy tożsamości usługi AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="c436a-141">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="c436a-142">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c436a-142">This parameter is optional.</span></span>

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

### <span data-ttu-id="c436a-143">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="c436a-143">-SignupPolicyName</span></span>
<span data-ttu-id="c436a-144">Nazwa zasad zapisywania się.</span><span class="sxs-lookup"><span data-stu-id="c436a-144">Signup Policy Name.</span></span> <span data-ttu-id="c436a-145">Dotyczy tylko dostawcy tożsamości usługi AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="c436a-145">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="c436a-146">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c436a-146">This parameter is optional.</span></span>

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

### <span data-ttu-id="c436a-147">-Type</span><span class="sxs-lookup"><span data-stu-id="c436a-147">-Type</span></span>
<span data-ttu-id="c436a-148">Identyfikator dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="c436a-148">Identifier of a Identity Provider.</span></span>
<span data-ttu-id="c436a-149">Jeśli zostanie określona, spróbuje znaleźć konfigurację dostawcy tożsamości przez identyfikator.</span><span class="sxs-lookup"><span data-stu-id="c436a-149">If specified will try to find identity provider configuration by the identifier.</span></span>
<span data-ttu-id="c436a-150">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="c436a-150">This parameter is optional.</span></span>

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

### <span data-ttu-id="c436a-151">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c436a-151">-Confirm</span></span>
<span data-ttu-id="c436a-152">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c436a-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c436a-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c436a-153">-WhatIf</span></span>
<span data-ttu-id="c436a-154">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c436a-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c436a-155">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c436a-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c436a-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c436a-156">CommonParameters</span></span>
<span data-ttu-id="c436a-157">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c436a-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c436a-158">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="c436a-158">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c436a-159">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c436a-159">INPUTS</span></span>

### <span data-ttu-id="c436a-160">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="c436a-160">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="c436a-161">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="c436a-161">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="c436a-162">System. String</span><span class="sxs-lookup"><span data-stu-id="c436a-162">System.String</span></span>

### <span data-ttu-id="c436a-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="c436a-163">System.String[]</span></span>

## <span data-ttu-id="c436a-164">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c436a-164">OUTPUTS</span></span>

### <span data-ttu-id="c436a-165">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c436a-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="c436a-166">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c436a-166">NOTES</span></span>

## <span data-ttu-id="c436a-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c436a-167">RELATED LINKS</span></span>

[<span data-ttu-id="c436a-168">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c436a-168">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="c436a-169">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c436a-169">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="c436a-170">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="c436a-170">Set-AzApiManagementIdentityProvider</span></span>](./Set-AzApiManagementIdentityProvider.md)
