---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadapplication
schema: 2.0.0
ms.openlocfilehash: 71e5e6c3cc80235b68df5c90e95a96e760abf80b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898865"
---
# <span data-ttu-id="376d5-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="376d5-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="376d5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="376d5-102">SYNOPSIS</span></span>
<span data-ttu-id="376d5-103">Tworzy nową aplikację usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="376d5-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="376d5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="376d5-104">SYNTAX</span></span>

### <span data-ttu-id="376d5-105">ApplicationWithoutCredentialParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="376d5-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="376d5-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="376d5-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="376d5-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="376d5-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="376d5-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="376d5-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="376d5-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="376d5-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="376d5-110">Opis</span><span class="sxs-lookup"><span data-stu-id="376d5-110">DESCRIPTION</span></span>
<span data-ttu-id="376d5-111">Tworzy nową aplikację usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="376d5-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="376d5-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="376d5-112">EXAMPLES</span></span>

### <span data-ttu-id="376d5-113">Przykład 1-Tworzenie nowej aplikacji AAD.</span><span class="sxs-lookup"><span data-stu-id="376d5-113">Example 1 - Create new AAD application.</span></span>

```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="376d5-114">Tworzy nową aplikację usługi Azure Active Directory bez żadnych poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="376d5-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="376d5-115">Przykład 2 — Tworzenie nowej aplikacji AAD przy użyciu hasła.</span><span class="sxs-lookup"><span data-stu-id="376d5-115">Example 2 - Create new AAD application with password.</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password $SecureStringPassword
```

<span data-ttu-id="376d5-116">Tworzy nową aplikację usługi Azure Active Directory i kojarzy z nią poświadczenia hasła.</span><span class="sxs-lookup"><span data-stu-id="376d5-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="376d5-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="376d5-117">PARAMETERS</span></span>

### <span data-ttu-id="376d5-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="376d5-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="376d5-119">Wartość określająca, czy aplikacja jest jedną dzierżawą, czy wieloma dzierżawami.</span><span class="sxs-lookup"><span data-stu-id="376d5-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="376d5-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="376d5-120">-CertValue</span></span>
<span data-ttu-id="376d5-121">Wartość "asymetrycznego" typu poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="376d5-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="376d5-122">Reprezentuje certyfikat zakodowany Base 64.</span><span class="sxs-lookup"><span data-stu-id="376d5-122">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="376d5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="376d5-123">-DefaultProfile</span></span>
<span data-ttu-id="376d5-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="376d5-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="376d5-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="376d5-125">-DisplayName</span></span>
<span data-ttu-id="376d5-126">Nazwa wyświetlana nowej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="376d5-126">Display name of the new application.</span></span>

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

### <span data-ttu-id="376d5-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="376d5-127">-EndDate</span></span>
<span data-ttu-id="376d5-128">Efektywna Data zakończenia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="376d5-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="376d5-129">Domyślną wartością daty zakończenia jest rok od dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="376d5-129">The default end date value is one year from today.</span></span> <span data-ttu-id="376d5-130">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub przed datą ważności certyfikatu x509.</span><span class="sxs-lookup"><span data-stu-id="376d5-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="376d5-131">-Strona główna</span><span class="sxs-lookup"><span data-stu-id="376d5-131">-HomePage</span></span>
<span data-ttu-id="376d5-132">Adres URL strony głównej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="376d5-132">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="376d5-133">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="376d5-133">-IdentifierUris</span></span>
<span data-ttu-id="376d5-134">Identyfikatory URI identyfikujące aplikację.</span><span class="sxs-lookup"><span data-stu-id="376d5-134">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="376d5-135">-Poświadczenia</span><span class="sxs-lookup"><span data-stu-id="376d5-135">-KeyCredentials</span></span>
<span data-ttu-id="376d5-136">Lista poświadczeń certyfikatów skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="376d5-136">The list of certificate credentials associated with the application.</span></span>

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

### <span data-ttu-id="376d5-137">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="376d5-137">-Password</span></span>
<span data-ttu-id="376d5-138">Hasło, które ma zostać skojarzone z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="376d5-138">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="376d5-139">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="376d5-139">-PasswordCredentials</span></span>
<span data-ttu-id="376d5-140">Lista poświadczeń haseł skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="376d5-140">The list of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="376d5-141">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="376d5-141">-ReplyUrls</span></span>
<span data-ttu-id="376d5-142">Adresy URL odpowiedzi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="376d5-142">The application reply urls.</span></span>

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

### <span data-ttu-id="376d5-143">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="376d5-143">-StartDate</span></span>
<span data-ttu-id="376d5-144">Efektywna Data rozpoczęcia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="376d5-144">The effective start date of the credential usage.</span></span>
<span data-ttu-id="376d5-145">Domyślna wartość daty rozpoczęcia przypada dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="376d5-145">The default start date value is today.</span></span> <span data-ttu-id="376d5-146">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub po dniu, od którego certyfikat x509 jest ważny.</span><span class="sxs-lookup"><span data-stu-id="376d5-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="376d5-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="376d5-147">-Confirm</span></span>
<span data-ttu-id="376d5-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="376d5-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="376d5-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="376d5-149">-WhatIf</span></span>
<span data-ttu-id="376d5-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="376d5-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="376d5-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="376d5-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="376d5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="376d5-152">CommonParameters</span></span>
<span data-ttu-id="376d5-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="376d5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="376d5-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="376d5-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="376d5-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="376d5-155">INPUTS</span></span>

### <span data-ttu-id="376d5-156">System. String</span><span class="sxs-lookup"><span data-stu-id="376d5-156">System.String</span></span>

### <span data-ttu-id="376d5-157">System. String []</span><span class="sxs-lookup"><span data-stu-id="376d5-157">System.String[]</span></span>

### <span data-ttu-id="376d5-158">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="376d5-158">System.Boolean</span></span>

### <span data-ttu-id="376d5-159">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADPasswordCredential []</span><span class="sxs-lookup"><span data-stu-id="376d5-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]</span></span>

### <span data-ttu-id="376d5-160">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADKeyCredential []</span><span class="sxs-lookup"><span data-stu-id="376d5-160">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]</span></span>

### <span data-ttu-id="376d5-161">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="376d5-161">System.Security.SecureString</span></span>

### <span data-ttu-id="376d5-162">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="376d5-162">System.DateTime</span></span>

## <span data-ttu-id="376d5-163">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="376d5-163">OUTPUTS</span></span>

### <span data-ttu-id="376d5-164">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="376d5-164">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="376d5-165">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="376d5-165">NOTES</span></span>
<span data-ttu-id="376d5-166">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="376d5-166">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="376d5-167">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="376d5-167">RELATED LINKS</span></span>

[<span data-ttu-id="376d5-168">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="376d5-168">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="376d5-169">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="376d5-169">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="376d5-170">Nowe — AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="376d5-170">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="376d5-171">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="376d5-171">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="376d5-172">Nowe — AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="376d5-172">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="376d5-173">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="376d5-173">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

