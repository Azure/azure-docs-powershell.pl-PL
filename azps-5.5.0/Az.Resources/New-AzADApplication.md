---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: 7ab7c679bc623a9eaa0f99bcdba1ab8281bd7d8f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201883"
---
# <span data-ttu-id="4d8ae-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="4d8ae-101">New-AzADApplication</span></span>

## <span data-ttu-id="4d8ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d8ae-102">SYNOPSIS</span></span>
<span data-ttu-id="4d8ae-103">Tworzy nową aplikację usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="4d8ae-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4d8ae-104">SYNTAX</span></span>

### <span data-ttu-id="4d8ae-105">ApplicationWithoutCredentialParameterSet (domyślne)</span><span class="sxs-lookup"><span data-stu-id="4d8ae-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d8ae-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d8ae-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d8ae-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d8ae-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d8ae-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d8ae-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4d8ae-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="4d8ae-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4d8ae-110">OPIS</span><span class="sxs-lookup"><span data-stu-id="4d8ae-110">DESCRIPTION</span></span>
<span data-ttu-id="4d8ae-111">Tworzy nową aplikację usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-111">Creates a new azure active directory application.</span></span> <span data-ttu-id="4d8ae-112">Poniżej przedstawiono uprawnienia wymagane do utworzenia aplikacji:</span><span class="sxs-lookup"><span data-stu-id="4d8ae-112">Below are the permissions needed to create an application:</span></span>

- <span data-ttu-id="4d8ae-113">Azure Active Directory Graph</span><span class="sxs-lookup"><span data-stu-id="4d8ae-113">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="4d8ae-114">Application.ReadWrite.OwnedBy</span><span class="sxs-lookup"><span data-stu-id="4d8ae-114">Application.ReadWrite.OwnedBy</span></span>
- <span data-ttu-id="4d8ae-115">Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="4d8ae-115">Microsoft Graph</span></span>
  - <span data-ttu-id="4d8ae-116">Directory.AccessAsUser.All</span><span class="sxs-lookup"><span data-stu-id="4d8ae-116">Directory.AccessAsUser.All</span></span>
  - <span data-ttu-id="4d8ae-117">Directory.ReadWrite.All</span><span class="sxs-lookup"><span data-stu-id="4d8ae-117">Directory.ReadWrite.All</span></span>

## <span data-ttu-id="4d8ae-118">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4d8ae-118">EXAMPLES</span></span>

### <span data-ttu-id="4d8ae-119">Przykład 1. Tworzenie nowej aplikacji AAD.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-119">Example 1: Create new AAD application.</span></span>

```powershell
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="4d8ae-120">Tworzy nową aplikację usługi Azure Active Directory bez poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-120">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="4d8ae-121">Przykład 2. Tworzenie nowej aplikacji AAD za pomocą hasła.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-121">Example 2: Create new AAD application with password.</span></span>

```powershell
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="4d8ae-122">Tworzy nową aplikację usługi Azure Active Directory i skojarzy z nim poświadczenia hasła.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-122">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="4d8ae-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4d8ae-123">PARAMETERS</span></span>

### <span data-ttu-id="4d8ae-124">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="4d8ae-124">-AvailableToOtherTenants</span></span>
<span data-ttu-id="4d8ae-125">Wartość określająca, czy aplikacja jest jedną dzierżawą, czy wielodostępną.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-125">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8ae-126">-CertValue</span><span class="sxs-lookup"><span data-stu-id="4d8ae-126">-CertValue</span></span>
<span data-ttu-id="4d8ae-127">Wartość typu poświadczeń "asymetrycznego".</span><span class="sxs-lookup"><span data-stu-id="4d8ae-127">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="4d8ae-128">Reprezentuje certyfikat zakodowany na podstawie 64.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-128">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8ae-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d8ae-129">-DefaultProfile</span></span>
<span data-ttu-id="4d8ae-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="4d8ae-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4d8ae-131">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="4d8ae-131">-DisplayName</span></span>
<span data-ttu-id="4d8ae-132">Nazwa wyświetlana nowej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-132">Display name of the new application.</span></span>

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

### <span data-ttu-id="4d8ae-133">-EndDate</span><span class="sxs-lookup"><span data-stu-id="4d8ae-133">-EndDate</span></span>
<span data-ttu-id="4d8ae-134">Data zakończenia użytkowania poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-134">The effective end date of the credential usage.</span></span>
<span data-ttu-id="4d8ae-135">Domyślna wartość daty końcowej to rok od dnia dzisiejszego.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-135">The default end date value is one year from today.</span></span> <span data-ttu-id="4d8ae-136">W przypadku poświadczeń typu "asymetrycznego" musi on być ustawiony na datę ważności certyfikatu X509 lub wcześniejszą.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-136">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8ae-137">-Strona główna</span><span class="sxs-lookup"><span data-stu-id="4d8ae-137">-HomePage</span></span>
<span data-ttu-id="4d8ae-138">Adres URL strony głównej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-138">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="4d8ae-139">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="4d8ae-139">-IdentifierUris</span></span>
<span data-ttu-id="4d8ae-140">URI identyfikujące aplikację.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-140">The URIs that identify the application.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8ae-141">- KeyCredentials</span><span class="sxs-lookup"><span data-stu-id="4d8ae-141">-KeyCredentials</span></span>
<span data-ttu-id="4d8ae-142">Lista poświadczeń certyfikatu skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-142">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8ae-143">— Hasło</span><span class="sxs-lookup"><span data-stu-id="4d8ae-143">-Password</span></span>
<span data-ttu-id="4d8ae-144">Hasło, które ma zostać skojarzone z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-144">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8ae-145">- PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="4d8ae-145">-PasswordCredentials</span></span>
<span data-ttu-id="4d8ae-146">Lista poświadczeń hasła skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-146">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8ae-147">- ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="4d8ae-147">-ReplyUrls</span></span>
<span data-ttu-id="4d8ae-148">Adresy URL odpowiedzi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-148">The application reply urls.</span></span>

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

### <span data-ttu-id="4d8ae-149">-StartDate</span><span class="sxs-lookup"><span data-stu-id="4d8ae-149">-StartDate</span></span>
<span data-ttu-id="4d8ae-150">Data rozpoczęcia użytkowania poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="4d8ae-151">Domyślną wartością daty rozpoczęcia jest dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-151">The default start date value is today.</span></span> <span data-ttu-id="4d8ae-152">W przypadku poświadczeń typu "asymetrycznego" musi on być ustawiony na datę ważności certyfikatu X509 lub późniejszą.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8ae-153">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4d8ae-153">-Confirm</span></span>
<span data-ttu-id="4d8ae-154">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4d8ae-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4d8ae-155">-WhatIf</span></span>
<span data-ttu-id="4d8ae-156">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4d8ae-157">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4d8ae-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d8ae-158">CommonParameters</span></span>
<span data-ttu-id="4d8ae-159">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4d8ae-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d8ae-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4d8ae-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d8ae-161">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d8ae-161">INPUTS</span></span>

### <span data-ttu-id="4d8ae-162">System.String</span><span class="sxs-lookup"><span data-stu-id="4d8ae-162">System.String</span></span>

### <span data-ttu-id="4d8ae-163">System.String[]</span><span class="sxs-lookup"><span data-stu-id="4d8ae-163">System.String[]</span></span>

### <span data-ttu-id="4d8ae-164">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4d8ae-164">System.Boolean</span></span>

### <span data-ttu-id="4d8ae-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span><span class="sxs-lookup"><span data-stu-id="4d8ae-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="4d8ae-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span><span class="sxs-lookup"><span data-stu-id="4d8ae-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="4d8ae-167">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="4d8ae-167">System.Security.SecureString</span></span>

### <span data-ttu-id="4d8ae-168">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="4d8ae-168">System.DateTime</span></span>

## <span data-ttu-id="4d8ae-169">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4d8ae-169">OUTPUTS</span></span>

### <span data-ttu-id="4d8ae-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="4d8ae-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="4d8ae-171">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4d8ae-171">NOTES</span></span>
<span data-ttu-id="4d8ae-172">Słowa kluczowe: azure, azurerm, arm, resource, management, manager, zasób, grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="4d8ae-172">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="4d8ae-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4d8ae-173">RELATED LINKS</span></span>

[<span data-ttu-id="4d8ae-174">Remove-AzadApplication</span><span class="sxs-lookup"><span data-stu-id="4d8ae-174">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="4d8ae-175">Get-AzadApplication</span><span class="sxs-lookup"><span data-stu-id="4d8ae-175">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="4d8ae-176">New-AzadServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="4d8ae-176">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="4d8ae-177">Get-AzadAppCredential</span><span class="sxs-lookup"><span data-stu-id="4d8ae-177">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="4d8ae-178">New-AzadAppCredential</span><span class="sxs-lookup"><span data-stu-id="4d8ae-178">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="4d8ae-179">Remove-AzadAppCredential</span><span class="sxs-lookup"><span data-stu-id="4d8ae-179">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

