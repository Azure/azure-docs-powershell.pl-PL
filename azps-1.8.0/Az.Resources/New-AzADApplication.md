---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: fa861a7be0716ec1da1f2f2a100e7dbbdc97af51
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93708373"
---
# <span data-ttu-id="f79b0-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="f79b0-101">New-AzADApplication</span></span>

## <span data-ttu-id="f79b0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f79b0-102">SYNOPSIS</span></span>
<span data-ttu-id="f79b0-103">Tworzy nową aplikację usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f79b0-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="f79b0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f79b0-104">SYNTAX</span></span>

### <span data-ttu-id="f79b0-105">ApplicationWithoutCredentialParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f79b0-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f79b0-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="f79b0-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f79b0-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="f79b0-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f79b0-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="f79b0-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f79b0-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="f79b0-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f79b0-110">Opis</span><span class="sxs-lookup"><span data-stu-id="f79b0-110">DESCRIPTION</span></span>
<span data-ttu-id="f79b0-111">Tworzy nową aplikację usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f79b0-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="f79b0-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f79b0-112">EXAMPLES</span></span>

### <span data-ttu-id="f79b0-113">Przykład 1-Tworzenie nowej aplikacji AAD.</span><span class="sxs-lookup"><span data-stu-id="f79b0-113">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="f79b0-114">Tworzy nową aplikację usługi Azure Active Directory bez żadnych poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="f79b0-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="f79b0-115">Przykład 2 — Tworzenie nowej aplikacji AAD przy użyciu hasła.</span><span class="sxs-lookup"><span data-stu-id="f79b0-115">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="f79b0-116">Tworzy nową aplikację usługi Azure Active Directory i kojarzy z nią poświadczenia hasła.</span><span class="sxs-lookup"><span data-stu-id="f79b0-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="f79b0-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f79b0-117">PARAMETERS</span></span>

### <span data-ttu-id="f79b0-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="f79b0-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="f79b0-119">Wartość określająca, czy aplikacja jest jedną dzierżawą, czy wieloma dzierżawami.</span><span class="sxs-lookup"><span data-stu-id="f79b0-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="f79b0-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="f79b0-120">-CertValue</span></span>
<span data-ttu-id="f79b0-121">Wartość "asymetrycznego" typu poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="f79b0-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="f79b0-122">Reprezentuje certyfikat zakodowany Base 64.</span><span class="sxs-lookup"><span data-stu-id="f79b0-122">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="f79b0-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f79b0-123">-DefaultProfile</span></span>
<span data-ttu-id="f79b0-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f79b0-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f79b0-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f79b0-125">-DisplayName</span></span>
<span data-ttu-id="f79b0-126">Nazwa wyświetlana nowej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f79b0-126">Display name of the new application.</span></span>

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

### <span data-ttu-id="f79b0-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="f79b0-127">-EndDate</span></span>
<span data-ttu-id="f79b0-128">Efektywna Data zakończenia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="f79b0-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="f79b0-129">Domyślną wartością daty zakończenia jest rok od dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="f79b0-129">The default end date value is one year from today.</span></span> <span data-ttu-id="f79b0-130">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub przed datą ważności certyfikatu x509.</span><span class="sxs-lookup"><span data-stu-id="f79b0-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="f79b0-131">-Strona główna</span><span class="sxs-lookup"><span data-stu-id="f79b0-131">-HomePage</span></span>
<span data-ttu-id="f79b0-132">Adres URL strony głównej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f79b0-132">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="f79b0-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="f79b0-133">-IdentifierUris</span></span>
<span data-ttu-id="f79b0-134">Identyfikatory URI identyfikujące aplikację.</span><span class="sxs-lookup"><span data-stu-id="f79b0-134">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="f79b0-135">-Poświadczenia</span><span class="sxs-lookup"><span data-stu-id="f79b0-135">-KeyCredentials</span></span>
<span data-ttu-id="f79b0-136">Lista poświadczeń certyfikatów skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="f79b0-136">The list of certificate credentials associated with the application.</span></span>

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

### <span data-ttu-id="f79b0-137">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="f79b0-137">-Password</span></span>
<span data-ttu-id="f79b0-138">Hasło, które ma zostać skojarzone z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="f79b0-138">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="f79b0-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="f79b0-139">-PasswordCredentials</span></span>
<span data-ttu-id="f79b0-140">Lista poświadczeń haseł skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="f79b0-140">The list of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="f79b0-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="f79b0-141">-ReplyUrls</span></span>
<span data-ttu-id="f79b0-142">Adresy URL odpowiedzi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="f79b0-142">The application reply urls.</span></span>

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

### <span data-ttu-id="f79b0-143">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="f79b0-143">-StartDate</span></span>
<span data-ttu-id="f79b0-144">Efektywna Data rozpoczęcia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="f79b0-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="f79b0-145">Domyślna wartość daty rozpoczęcia przypada dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="f79b0-145">The default start date value is today.</span></span> <span data-ttu-id="f79b0-146">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub po dniu, od którego certyfikat x509 jest ważny.</span><span class="sxs-lookup"><span data-stu-id="f79b0-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="f79b0-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f79b0-147">-Confirm</span></span>
<span data-ttu-id="f79b0-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f79b0-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f79b0-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f79b0-149">-WhatIf</span></span>
<span data-ttu-id="f79b0-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f79b0-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f79b0-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f79b0-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f79b0-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f79b0-152">CommonParameters</span></span>
<span data-ttu-id="f79b0-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f79b0-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f79b0-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f79b0-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f79b0-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f79b0-155">INPUTS</span></span>

### <span data-ttu-id="f79b0-156">System. String</span><span class="sxs-lookup"><span data-stu-id="f79b0-156">System.String</span></span>

### <span data-ttu-id="f79b0-157">System. String []</span><span class="sxs-lookup"><span data-stu-id="f79b0-157">System.String[]</span></span>

### <span data-ttu-id="f79b0-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="f79b0-158">System.Boolean</span></span>

### <span data-ttu-id="f79b0-159">Microsoft. Azure. Commands. pozycji. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="f79b0-159">Microsoft.Azure.Commands.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="f79b0-160">Microsoft. Azure. Commands. pozycji. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="f79b0-160">Microsoft.Azure.Commands.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="f79b0-161">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="f79b0-161">System.Security.SecureString</span></span>

### <span data-ttu-id="f79b0-162">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="f79b0-162">System.DateTime</span></span>

## <span data-ttu-id="f79b0-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f79b0-163">OUTPUTS</span></span>

### <span data-ttu-id="f79b0-164">Microsoft. Azure. Commands. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="f79b0-164">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="f79b0-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f79b0-165">NOTES</span></span>
<span data-ttu-id="f79b0-166">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="f79b0-166">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="f79b0-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f79b0-167">RELATED LINKS</span></span>

[<span data-ttu-id="f79b0-168">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="f79b0-168">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="f79b0-169">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="f79b0-169">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="f79b0-170">Nowe — AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f79b0-170">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="f79b0-171">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f79b0-171">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="f79b0-172">Nowe — AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f79b0-172">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="f79b0-173">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="f79b0-173">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

