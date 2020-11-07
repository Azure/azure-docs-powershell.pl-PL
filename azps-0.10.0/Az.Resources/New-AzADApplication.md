---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADApplication.md
ms.openlocfilehash: 3850e5f142e7ec1496ace1225ab53c160794775a
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892534"
---
# <span data-ttu-id="92afb-101">New-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="92afb-101">New-AzADApplication</span></span>

## <span data-ttu-id="92afb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="92afb-102">SYNOPSIS</span></span>
<span data-ttu-id="92afb-103">Tworzy nową aplikację usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="92afb-103">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="92afb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="92afb-104">SYNTAX</span></span>

### <span data-ttu-id="92afb-105">ApplicationWithoutCredentialParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="92afb-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92afb-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="92afb-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92afb-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="92afb-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92afb-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="92afb-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92afb-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="92afb-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92afb-110">Opis</span><span class="sxs-lookup"><span data-stu-id="92afb-110">DESCRIPTION</span></span>
<span data-ttu-id="92afb-111">Tworzy nową aplikację usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="92afb-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="92afb-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="92afb-112">EXAMPLES</span></span>

### <span data-ttu-id="92afb-113">Przykład 1-Tworzenie nowej aplikacji AAD.</span><span class="sxs-lookup"><span data-stu-id="92afb-113">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="92afb-114">Tworzy nową aplikację usługi Azure Active Directory bez żadnych poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="92afb-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="92afb-115">Przykład 2 — Tworzenie nowej aplikacji AAD przy użyciu hasła.</span><span class="sxs-lookup"><span data-stu-id="92afb-115">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADApplication -DisplayName "NewApplication" -HomePage "http://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="92afb-116">Tworzy nową aplikację usługi Azure Active Directory i kojarzy z nią poświadczenia hasła.</span><span class="sxs-lookup"><span data-stu-id="92afb-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="92afb-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="92afb-117">PARAMETERS</span></span>

### <span data-ttu-id="92afb-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="92afb-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="92afb-119">Wartość określająca, czy aplikacja jest jedną dzierżawą, czy wieloma dzierżawami.</span><span class="sxs-lookup"><span data-stu-id="92afb-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="92afb-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="92afb-120">-CertValue</span></span>
<span data-ttu-id="92afb-121">Wartość "asymetrycznego" typu poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="92afb-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="92afb-122">Reprezentuje certyfikat zakodowany Base 64.</span><span class="sxs-lookup"><span data-stu-id="92afb-122">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="92afb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92afb-123">-DefaultProfile</span></span>
<span data-ttu-id="92afb-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="92afb-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="92afb-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="92afb-125">-DisplayName</span></span>
<span data-ttu-id="92afb-126">Nazwa wyświetlana nowej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="92afb-126">Display name of the new application.</span></span>

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

### <span data-ttu-id="92afb-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="92afb-127">-EndDate</span></span>
<span data-ttu-id="92afb-128">Efektywna Data zakończenia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="92afb-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="92afb-129">Domyślną wartością daty zakończenia jest rok od dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="92afb-129">The default end date value is one year from today.</span></span> <span data-ttu-id="92afb-130">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub przed datą ważności certyfikatu x509.</span><span class="sxs-lookup"><span data-stu-id="92afb-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="92afb-131">-Strona główna</span><span class="sxs-lookup"><span data-stu-id="92afb-131">-HomePage</span></span>
<span data-ttu-id="92afb-132">Adres URL strony głównej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="92afb-132">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="92afb-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="92afb-133">-IdentifierUris</span></span>
<span data-ttu-id="92afb-134">Identyfikatory URI identyfikujące aplikację.</span><span class="sxs-lookup"><span data-stu-id="92afb-134">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="92afb-135">-Poświadczenia</span><span class="sxs-lookup"><span data-stu-id="92afb-135">-KeyCredentials</span></span>
<span data-ttu-id="92afb-136">Lista poświadczeń certyfikatów skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="92afb-136">The list of certificate credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92afb-137">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="92afb-137">-Password</span></span>
<span data-ttu-id="92afb-138">Hasło, które ma zostać skojarzone z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="92afb-138">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="92afb-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="92afb-139">-PasswordCredentials</span></span>
<span data-ttu-id="92afb-140">Lista poświadczeń haseł skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="92afb-140">The list of password credentials associated with the application.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="92afb-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="92afb-141">-ReplyUrls</span></span>
<span data-ttu-id="92afb-142">Adresy URL odpowiedzi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="92afb-142">The application reply urls.</span></span>

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

### <span data-ttu-id="92afb-143">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="92afb-143">-StartDate</span></span>
<span data-ttu-id="92afb-144">Efektywna Data rozpoczęcia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="92afb-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="92afb-145">Domyślna wartość daty rozpoczęcia przypada dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="92afb-145">The default start date value is today.</span></span> <span data-ttu-id="92afb-146">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub po dniu, od którego certyfikat x509 jest ważny.</span><span class="sxs-lookup"><span data-stu-id="92afb-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="92afb-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="92afb-147">-Confirm</span></span>
<span data-ttu-id="92afb-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92afb-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92afb-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92afb-149">-WhatIf</span></span>
<span data-ttu-id="92afb-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="92afb-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92afb-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="92afb-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92afb-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92afb-152">CommonParameters</span></span>
<span data-ttu-id="92afb-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92afb-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92afb-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92afb-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92afb-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="92afb-155">INPUTS</span></span>

### <span data-ttu-id="92afb-156">System. String</span><span class="sxs-lookup"><span data-stu-id="92afb-156">System.String</span></span>

### <span data-ttu-id="92afb-157">System. String []</span><span class="sxs-lookup"><span data-stu-id="92afb-157">System.String[]</span></span>

### <span data-ttu-id="92afb-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="92afb-158">System.Boolean</span></span>

### <span data-ttu-id="92afb-159">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="92afb-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="92afb-160">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="92afb-160">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="92afb-161">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="92afb-161">System.Security.SecureString</span></span>

### <span data-ttu-id="92afb-162">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="92afb-162">System.DateTime</span></span>

## <span data-ttu-id="92afb-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="92afb-163">OUTPUTS</span></span>

### <span data-ttu-id="92afb-164">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="92afb-164">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="92afb-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="92afb-165">NOTES</span></span>
<span data-ttu-id="92afb-166">Słowa kluczowe: Azure, AZ, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="92afb-166">Keywords: azure, Az, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="92afb-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="92afb-167">RELATED LINKS</span></span>

[<span data-ttu-id="92afb-168">Remove-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="92afb-168">Remove-AzADApplication</span></span>](./Remove-AzADApplication.md)

[<span data-ttu-id="92afb-169">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="92afb-169">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

[<span data-ttu-id="92afb-170">Nowe — AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="92afb-170">New-AzADServicePrincipal</span></span>](./New-AzADServicePrincipal.md)

[<span data-ttu-id="92afb-171">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="92afb-171">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="92afb-172">Nowe — AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="92afb-172">New-AzADAppCredential</span></span>](./New-AzADAppCredential.md)

[<span data-ttu-id="92afb-173">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="92afb-173">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

