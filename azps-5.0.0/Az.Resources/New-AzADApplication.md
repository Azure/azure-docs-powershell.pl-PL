---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: 7ab7c679bc623a9eaa0f99bcdba1ab8281bd7d8f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308785"
---
# <span data-ttu-id="8e312-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8e312-101">New-AzADApplication</span></span>

## <span data-ttu-id="8e312-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8e312-102">SYNOPSIS</span></span>
<span data-ttu-id="8e312-103">Tworzy nową aplikację usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8e312-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="8e312-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8e312-104">SYNTAX</span></span>

### <span data-ttu-id="8e312-105">ApplicationWithoutCredentialParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8e312-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e312-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e312-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e312-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e312-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e312-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e312-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8e312-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="8e312-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8e312-110">Opis</span><span class="sxs-lookup"><span data-stu-id="8e312-110">DESCRIPTION</span></span>
<span data-ttu-id="8e312-111">Tworzy nową aplikację usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="8e312-111">Creates a new azure active directory application.</span></span> <span data-ttu-id="8e312-112">Poniżej znajdują się uprawnienia potrzebne do utworzenia aplikacji:</span><span class="sxs-lookup"><span data-stu-id="8e312-112">Below are the permissions needed to create an application:</span></span>

- <span data-ttu-id="8e312-113">Wykres usługi Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="8e312-113">Azure Active Directory Graph</span></span>
  - <span data-ttu-id="8e312-114">Application. ReadWrite. OwnedBy</span><span class="sxs-lookup"><span data-stu-id="8e312-114">Application.ReadWrite.OwnedBy</span></span>
- <span data-ttu-id="8e312-115">Program Microsoft Graph</span><span class="sxs-lookup"><span data-stu-id="8e312-115">Microsoft Graph</span></span>
  - <span data-ttu-id="8e312-116">Directory. AccessAsUser. All</span><span class="sxs-lookup"><span data-stu-id="8e312-116">Directory.AccessAsUser.All</span></span>
  - <span data-ttu-id="8e312-117">Directory. ReadWrite. All</span><span class="sxs-lookup"><span data-stu-id="8e312-117">Directory.ReadWrite.All</span></span>

## <span data-ttu-id="8e312-118">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8e312-118">EXAMPLES</span></span>

### <span data-ttu-id="8e312-119">Przykład 1: Tworzenie nowej aplikacji AAD.</span><span class="sxs-lookup"><span data-stu-id="8e312-119">Example 1: Create new AAD application.</span></span>

```powershell
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="8e312-120">Tworzy nową aplikację usługi Azure Active Directory bez żadnych poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="8e312-120">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="8e312-121">Przykład 2: Tworzenie nowej aplikacji AAD przy użyciu hasła.</span><span class="sxs-lookup"><span data-stu-id="8e312-121">Example 2: Create new AAD application with password.</span></span>

```powershell
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="8e312-122">Tworzy nową aplikację usługi Azure Active Directory i kojarzy z nią poświadczenia hasła.</span><span class="sxs-lookup"><span data-stu-id="8e312-122">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="8e312-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8e312-123">PARAMETERS</span></span>

### <span data-ttu-id="8e312-124">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="8e312-124">-AvailableToOtherTenants</span></span>
<span data-ttu-id="8e312-125">Wartość określająca, czy aplikacja jest jedną dzierżawą, czy wieloma dzierżawami.</span><span class="sxs-lookup"><span data-stu-id="8e312-125">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="8e312-126">-CertValue</span><span class="sxs-lookup"><span data-stu-id="8e312-126">-CertValue</span></span>
<span data-ttu-id="8e312-127">Wartość "asymetrycznego" typu poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="8e312-127">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="8e312-128">Reprezentuje certyfikat zakodowany Base 64.</span><span class="sxs-lookup"><span data-stu-id="8e312-128">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="8e312-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8e312-129">-DefaultProfile</span></span>
<span data-ttu-id="8e312-130">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="8e312-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8e312-131">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="8e312-131">-DisplayName</span></span>
<span data-ttu-id="8e312-132">Nazwa wyświetlana nowej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8e312-132">Display name of the new application.</span></span>

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

### <span data-ttu-id="8e312-133">-EndDate</span><span class="sxs-lookup"><span data-stu-id="8e312-133">-EndDate</span></span>
<span data-ttu-id="8e312-134">Efektywna Data zakończenia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="8e312-134">The effective end date of the credential usage.</span></span>
<span data-ttu-id="8e312-135">Domyślną wartością daty zakończenia jest rok od dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="8e312-135">The default end date value is one year from today.</span></span> <span data-ttu-id="8e312-136">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub przed datą ważności certyfikatu x509.</span><span class="sxs-lookup"><span data-stu-id="8e312-136">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="8e312-137">-Strona główna</span><span class="sxs-lookup"><span data-stu-id="8e312-137">-HomePage</span></span>
<span data-ttu-id="8e312-138">Adres URL strony głównej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8e312-138">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="8e312-139">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="8e312-139">-IdentifierUris</span></span>
<span data-ttu-id="8e312-140">Identyfikatory URI identyfikujące aplikację.</span><span class="sxs-lookup"><span data-stu-id="8e312-140">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="8e312-141">-Poświadczenia</span><span class="sxs-lookup"><span data-stu-id="8e312-141">-KeyCredentials</span></span>
<span data-ttu-id="8e312-142">Lista poświadczeń certyfikatów skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="8e312-142">The list of certificate credentials associated with the application.</span></span>

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

### <span data-ttu-id="8e312-143">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="8e312-143">-Password</span></span>
<span data-ttu-id="8e312-144">Hasło, które ma zostać skojarzone z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="8e312-144">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="8e312-145">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="8e312-145">-PasswordCredentials</span></span>
<span data-ttu-id="8e312-146">Lista poświadczeń haseł skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="8e312-146">The list of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="8e312-147">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="8e312-147">-ReplyUrls</span></span>
<span data-ttu-id="8e312-148">Adresy URL odpowiedzi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="8e312-148">The application reply urls.</span></span>

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

### <span data-ttu-id="8e312-149">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="8e312-149">-StartDate</span></span>
<span data-ttu-id="8e312-150">Efektywna Data rozpoczęcia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="8e312-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="8e312-151">Domyślna wartość daty rozpoczęcia przypada dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="8e312-151">The default start date value is today.</span></span> <span data-ttu-id="8e312-152">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub po dniu, od którego certyfikat x509 jest ważny.</span><span class="sxs-lookup"><span data-stu-id="8e312-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="8e312-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8e312-153">-Confirm</span></span>
<span data-ttu-id="8e312-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e312-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8e312-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8e312-155">-WhatIf</span></span>
<span data-ttu-id="8e312-156">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8e312-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8e312-157">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8e312-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8e312-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8e312-158">CommonParameters</span></span>
<span data-ttu-id="8e312-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8e312-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8e312-160">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8e312-160">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8e312-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8e312-161">INPUTS</span></span>

### <span data-ttu-id="8e312-162">System. String</span><span class="sxs-lookup"><span data-stu-id="8e312-162">System.String</span></span>

### <span data-ttu-id="8e312-163">System. String []</span><span class="sxs-lookup"><span data-stu-id="8e312-163">System.String[]</span></span>

### <span data-ttu-id="8e312-164">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="8e312-164">System.Boolean</span></span>

### <span data-ttu-id="8e312-165">Microsoft. Azure. Commands. pozycji. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="8e312-165">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="8e312-166">Microsoft. Azure. Commands. pozycji. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="8e312-166">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="8e312-167">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="8e312-167">System.Security.SecureString</span></span>

### <span data-ttu-id="8e312-168">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="8e312-168">System.DateTime</span></span>

## <span data-ttu-id="8e312-169">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8e312-169">OUTPUTS</span></span>

### <span data-ttu-id="8e312-170">Microsoft. Azure. Commands. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="8e312-170">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="8e312-171">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8e312-171">NOTES</span></span>
<span data-ttu-id="8e312-172">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="8e312-172">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="8e312-173">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8e312-173">RELATED LINKS</span></span>

[<span data-ttu-id="8e312-174">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8e312-174">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="8e312-175">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="8e312-175">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="8e312-176">Nowe — AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="8e312-176">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="8e312-177">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8e312-177">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="8e312-178">Nowe — AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8e312-178">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="8e312-179">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="8e312-179">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

