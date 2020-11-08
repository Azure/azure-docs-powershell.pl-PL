---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/set-azapimanagementidentityprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Set-AzApiManagementIdentityProvider.md
ms.openlocfilehash: a110e950bff46bba7d3c7b5033c01b95ac2397f1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94052821"
---
# <span data-ttu-id="98c65-101">Set-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="98c65-101">Set-AzApiManagementIdentityProvider</span></span>

## <span data-ttu-id="98c65-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="98c65-102">SYNOPSIS</span></span>
<span data-ttu-id="98c65-103">Umożliwia zaktualizowanie konfiguracji istniejącego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="98c65-103">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="98c65-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="98c65-104">SYNTAX</span></span>

### <span data-ttu-id="98c65-105">ExpandedParameter (domyślny)</span><span class="sxs-lookup"><span data-stu-id="98c65-105">ExpandedParameter (Default)</span></span>
```
Set-AzApiManagementIdentityProvider -Context <PsApiManagementContext>
 -Type <PsApiManagementIdentityProviderType> [-ClientId <String>] [-ClientSecret <String>]
 [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>] [-SigninPolicyName <String>]
 [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>] [-SignInTenant <String>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="98c65-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="98c65-106">ByInputObject</span></span>
```
Set-AzApiManagementIdentityProvider -InputObject <PsApiManagementIdentityProvider> [-ClientId <String>]
 [-ClientSecret <String>] [-AllowedTenants <String[]>] [-Authority <String>] [-SignupPolicyName <String>]
 [-SigninPolicyName <String>] [-ProfileEditingPolicyName <String>] [-PasswordResetPolicyName <String>]
 [-SignInTenant <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98c65-107">Opis</span><span class="sxs-lookup"><span data-stu-id="98c65-107">DESCRIPTION</span></span>
<span data-ttu-id="98c65-108">Umożliwia zaktualizowanie konfiguracji istniejącego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="98c65-108">Updates the Configuration of an existing Identity Provider.</span></span>

## <span data-ttu-id="98c65-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="98c65-109">EXAMPLES</span></span>

### <span data-ttu-id="98c65-110">Przykład 1: aktualizowanie dostawcy tożsamości w serwisie Facebook</span><span class="sxs-lookup"><span data-stu-id="98c65-110">Example 1 : Update the facebook Identity Provider</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\> Set-AzApiManagementIdentityProvider -Context $apimContext -Type Facebook -ClientSecret "updatedSecret" -PassThru
```

<span data-ttu-id="98c65-111">Polecenie cmdlet aktualizuje klucz tajny klienta usługi Facebook Identity Provider.</span><span class="sxs-lookup"><span data-stu-id="98c65-111">The cmdlet updates the Client Secret of the Facebook Identity Provider;</span></span>

## <span data-ttu-id="98c65-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="98c65-112">PARAMETERS</span></span>

### <span data-ttu-id="98c65-113">-AllowedTenants</span><span class="sxs-lookup"><span data-stu-id="98c65-113">-AllowedTenants</span></span>
<span data-ttu-id="98c65-114">Lista dozwolonych dzierżaw usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="98c65-114">List of allowed Azure Active Directory Tenants.</span></span>

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

### <span data-ttu-id="98c65-115">-Authority</span><span class="sxs-lookup"><span data-stu-id="98c65-115">-Authority</span></span>
<span data-ttu-id="98c65-116">OpenID Połącz hosta punktu końcowego odnajdowania w usłudze AAD lub AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="98c65-116">OpenID Connect discovery endpoint hostname for AAD or AAD B2C.</span></span> <span data-ttu-id="98c65-117">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="98c65-117">This parameter is optional.</span></span>

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

### <span data-ttu-id="98c65-118">-ClientId</span><span class="sxs-lookup"><span data-stu-id="98c65-118">-ClientId</span></span>
<span data-ttu-id="98c65-119">Identyfikator klienta aplikacji w zewnętrznym dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="98c65-119">Client Id of the Application in the external Identity Provider.</span></span>
<span data-ttu-id="98c65-120">Jest to identyfikator aplikacji dla logowania do serwisu Facebook, identyfikator klienta Google login, identyfikator aplikacji dla firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="98c65-120">It is App ID for Facebook login, Client ID for Google login, App ID for Microsoft.</span></span>

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

### <span data-ttu-id="98c65-121">-ClientSecret</span><span class="sxs-lookup"><span data-stu-id="98c65-121">-ClientSecret</span></span>
<span data-ttu-id="98c65-122">Klucz tajny klienta aplikacji w zewnętrznym dostawcy tożsamości, służący do uwierzytelniania żądania logowania.</span><span class="sxs-lookup"><span data-stu-id="98c65-122">Client secret of the Application in external Identity Provider, used to authenticate login request.</span></span>
<span data-ttu-id="98c65-123">Na przykład jest to klucz tajny aplikacji dla logowania do serwisu Facebook, klucz interfejsu API logowania Google, klucz publiczny dla firmy Microsoft.</span><span class="sxs-lookup"><span data-stu-id="98c65-123">For example, it is App Secret for Facebook login, API Key for Google login, Public Key for Microsoft.</span></span>

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

### <span data-ttu-id="98c65-124">-Context</span><span class="sxs-lookup"><span data-stu-id="98c65-124">-Context</span></span>
<span data-ttu-id="98c65-125">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="98c65-125">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="98c65-126">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="98c65-126">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ExpandedParameter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98c65-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c65-127">-DefaultProfile</span></span>
<span data-ttu-id="98c65-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="98c65-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98c65-129">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="98c65-129">-InputObject</span></span>
<span data-ttu-id="98c65-130">Wystąpienie PsApiManagementIdentityProvider.</span><span class="sxs-lookup"><span data-stu-id="98c65-130">Instance of PsApiManagementIdentityProvider.</span></span> <span data-ttu-id="98c65-131">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="98c65-131">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="98c65-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="98c65-132">-PassThru</span></span>
<span data-ttu-id="98c65-133">Wskazuje, że to polecenie cmdlet zwróci  **PsApiManagementIdentityProvider** , które modyfikuje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98c65-133">Indicates that this cmdlet returns the  **PsApiManagementIdentityProvider** that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="98c65-134">-PasswordResetPolicyName</span><span class="sxs-lookup"><span data-stu-id="98c65-134">-PasswordResetPolicyName</span></span>
<span data-ttu-id="98c65-135">Nazwa zasady resetowania hasła.</span><span class="sxs-lookup"><span data-stu-id="98c65-135">Password Reset Policy Name.</span></span> <span data-ttu-id="98c65-136">Dotyczy tylko dostawcy tożsamości usługi AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="98c65-136">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="98c65-137">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="98c65-137">This parameter is optional.</span></span>

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

### <span data-ttu-id="98c65-138">-ProfileEditingPolicyName</span><span class="sxs-lookup"><span data-stu-id="98c65-138">-ProfileEditingPolicyName</span></span>
<span data-ttu-id="98c65-139">Nazwa zasad edytowania profilu.</span><span class="sxs-lookup"><span data-stu-id="98c65-139">Profile Editing Policy Name.</span></span> <span data-ttu-id="98c65-140">Dotyczy tylko dostawcy tożsamości usługi AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="98c65-140">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="98c65-141">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="98c65-141">This parameter is optional.</span></span>

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

### <span data-ttu-id="98c65-142">-SigninPolicyName</span><span class="sxs-lookup"><span data-stu-id="98c65-142">-SigninPolicyName</span></span>
<span data-ttu-id="98c65-143">Nazwa zasady logowanie się.</span><span class="sxs-lookup"><span data-stu-id="98c65-143">Signin Policy Name.</span></span> <span data-ttu-id="98c65-144">Dotyczy tylko dostawcy tożsamości usługi AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="98c65-144">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="98c65-145">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="98c65-145">This parameter is optional.</span></span>

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

### <span data-ttu-id="98c65-146">-SignupPolicyName</span><span class="sxs-lookup"><span data-stu-id="98c65-146">-SignupPolicyName</span></span>
<span data-ttu-id="98c65-147">Nazwa zasad zapisywania się.</span><span class="sxs-lookup"><span data-stu-id="98c65-147">Signup Policy Name.</span></span> <span data-ttu-id="98c65-148">Dotyczy tylko dostawcy tożsamości usługi AAD B2C.</span><span class="sxs-lookup"><span data-stu-id="98c65-148">Only applies to AAD B2C Identity Provider.</span></span> <span data-ttu-id="98c65-149">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="98c65-149">This parameter is optional.</span></span>

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

### <span data-ttu-id="98c65-150">-Type</span><span class="sxs-lookup"><span data-stu-id="98c65-150">-Type</span></span>
<span data-ttu-id="98c65-151">Identyfikator istniejącego dostawcy tożsamości.</span><span class="sxs-lookup"><span data-stu-id="98c65-151">Identifier of an existing Identity Provider.</span></span>
<span data-ttu-id="98c65-152">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="98c65-152">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType
Parameter Sets: ExpandedParameter
Aliases:
Accepted values: Facebook, Google, Microsoft, Twitter, Aad, AadB2C

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98c65-153">-SigninTenant</span><span class="sxs-lookup"><span data-stu-id="98c65-153">-SigninTenant</span></span>
<span data-ttu-id="98c65-154">Zaloguj się, aby zastąpić w usłudze AAD B2C zamiast `common` dzierżawy</span><span class="sxs-lookup"><span data-stu-id="98c65-154">Signin Tenant to override in AAD B2C instead of the `common` Tenant</span></span>

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

### <span data-ttu-id="98c65-155">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="98c65-155">-Confirm</span></span>
<span data-ttu-id="98c65-156">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98c65-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98c65-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98c65-157">-WhatIf</span></span>
<span data-ttu-id="98c65-158">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="98c65-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98c65-159">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="98c65-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98c65-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c65-160">CommonParameters</span></span>
<span data-ttu-id="98c65-161">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="98c65-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c65-162">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="98c65-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c65-163">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="98c65-163">INPUTS</span></span>

### <span data-ttu-id="98c65-164">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="98c65-164">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="98c65-165">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProviderType</span><span class="sxs-lookup"><span data-stu-id="98c65-165">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProviderType</span></span>

### <span data-ttu-id="98c65-166">System. String</span><span class="sxs-lookup"><span data-stu-id="98c65-166">System.String</span></span>

### <span data-ttu-id="98c65-167">System. String []</span><span class="sxs-lookup"><span data-stu-id="98c65-167">System.String[]</span></span>

### <span data-ttu-id="98c65-168">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="98c65-168">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="98c65-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="98c65-169">OUTPUTS</span></span>

### <span data-ttu-id="98c65-170">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="98c65-170">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementIdentityProvider</span></span>

## <span data-ttu-id="98c65-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="98c65-171">NOTES</span></span>

## <span data-ttu-id="98c65-172">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="98c65-172">RELATED LINKS</span></span>

[<span data-ttu-id="98c65-173">Nowe — AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="98c65-173">New-AzApiManagementIdentityProvider</span></span>](./New-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="98c65-174">Get-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="98c65-174">Get-AzApiManagementIdentityProvider</span></span>](./Get-AzApiManagementIdentityProvider.md)

[<span data-ttu-id="98c65-175">Remove-AzApiManagementIdentityProvider</span><span class="sxs-lookup"><span data-stu-id="98c65-175">Remove-AzApiManagementIdentityProvider</span></span>](./Remove-AzApiManagementIdentityProvider.md)
