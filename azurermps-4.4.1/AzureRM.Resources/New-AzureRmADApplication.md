---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: F58FD77E-2946-44B1-B410-6E983FC20E21
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADApplication.md
ms.openlocfilehash: c43bba247268d7ffcdbc2c33d7198415738c5694
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553775"
---
# <span data-ttu-id="16d4c-101">New-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="16d4c-101">New-AzureRmADApplication</span></span>

## <span data-ttu-id="16d4c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="16d4c-102">SYNOPSIS</span></span>
<span data-ttu-id="16d4c-103">Tworzy nową aplikację usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="16d4c-103">Creates a new azure active directory application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16d4c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="16d4c-104">SYNTAX</span></span>

### <span data-ttu-id="16d4c-105">ApplicationWithoutCredentialParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="16d4c-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16d4c-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="16d4c-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16d4c-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="16d4c-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16d4c-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="16d4c-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16d4c-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="16d4c-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADApplication -DisplayName <String> -IdentifierUris <String[]> [-HomePage <String>]
 [-ReplyUrls <String[]>] [-AvailableToOtherTenants <Boolean>] -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16d4c-110">Opis</span><span class="sxs-lookup"><span data-stu-id="16d4c-110">DESCRIPTION</span></span>
<span data-ttu-id="16d4c-111">Tworzy nową aplikację usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="16d4c-111">Creates a new azure active directory application.</span></span>

## <span data-ttu-id="16d4c-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="16d4c-112">EXAMPLES</span></span>

### <span data-ttu-id="16d4c-113">--------------------------Utworzyć nową aplikację AAD.</span><span class="sxs-lookup"><span data-stu-id="16d4c-113">--------------------------  Create new AAD application.</span></span>  --------------------------
```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http://NewApplication"
```

<span data-ttu-id="16d4c-114">Tworzy nową aplikację usługi Azure Active Directory bez żadnych poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="16d4c-114">Creates a new azure active directory application without any credentials.</span></span>

### <span data-ttu-id="16d4c-115">--------------------------Utworzyć nową aplikację AAD przy użyciu hasła.</span><span class="sxs-lookup"><span data-stu-id="16d4c-115">--------------------------  Create new AAD application with password.</span></span>  --------------------------
```
PS C:\> New-AzureRmADApplication -DisplayName "NewApplication" -HomePage "https://www.microsoft.com" -IdentifierUris "http:
//NewApplication" -Password "password"
```

<span data-ttu-id="16d4c-116">Tworzy nową aplikację usługi Azure Active Directory i kojarzy z nią poświadczenia hasła.</span><span class="sxs-lookup"><span data-stu-id="16d4c-116">Creates a new azure active directory application and associates password credentials with it.</span></span>

## <span data-ttu-id="16d4c-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="16d4c-117">PARAMETERS</span></span>

### <span data-ttu-id="16d4c-118">-AvailableToOtherTenants</span><span class="sxs-lookup"><span data-stu-id="16d4c-118">-AvailableToOtherTenants</span></span>
<span data-ttu-id="16d4c-119">Wartość określająca, czy aplikacja jest jedną dzierżawą, czy wieloma dzierżawami.</span><span class="sxs-lookup"><span data-stu-id="16d4c-119">The value specifying whether the application is a single tenant or a multi-tenant.</span></span>

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

### <span data-ttu-id="16d4c-120">-CertValue</span><span class="sxs-lookup"><span data-stu-id="16d4c-120">-CertValue</span></span>
<span data-ttu-id="16d4c-121">Wartość "asymetrycznego" typu poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="16d4c-121">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="16d4c-122">Reprezentuje certyfikat zakodowany Base 64.</span><span class="sxs-lookup"><span data-stu-id="16d4c-122">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="16d4c-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="16d4c-123">-DisplayName</span></span>
<span data-ttu-id="16d4c-124">Nazwa wyświetlana nowej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="16d4c-124">Display name of the new application.</span></span>

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

### <span data-ttu-id="16d4c-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="16d4c-125">-EndDate</span></span>
<span data-ttu-id="16d4c-126">Efektywna Data zakończenia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="16d4c-126">The effective end date of the credential usage.</span></span>
<span data-ttu-id="16d4c-127">Domyślną wartością daty zakończenia jest rok od dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="16d4c-127">The default end date value is one year from today.</span></span> <span data-ttu-id="16d4c-128">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub przed datą ważności certyfikatu x509.</span><span class="sxs-lookup"><span data-stu-id="16d4c-128">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="16d4c-129">-Strona główna</span><span class="sxs-lookup"><span data-stu-id="16d4c-129">-HomePage</span></span>
<span data-ttu-id="16d4c-130">Adres URL strony głównej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="16d4c-130">The URL to the application homepage.</span></span>

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

### <span data-ttu-id="16d4c-131">-IdentifierUris</span><span class="sxs-lookup"><span data-stu-id="16d4c-131">-IdentifierUris</span></span>
<span data-ttu-id="16d4c-132">Identyfikatory URI identyfikujące aplikację.</span><span class="sxs-lookup"><span data-stu-id="16d4c-132">The URIs that identify the application.</span></span>

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

### <span data-ttu-id="16d4c-133">-Poświadczenia</span><span class="sxs-lookup"><span data-stu-id="16d4c-133">-KeyCredentials</span></span>
<span data-ttu-id="16d4c-134">Lista poświadczeń certyfikatów skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="16d4c-134">The list of certificate credentials associated with the application.</span></span>

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

### <span data-ttu-id="16d4c-135">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="16d4c-135">-Password</span></span>
<span data-ttu-id="16d4c-136">Hasło, które ma zostać skojarzone z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="16d4c-136">The password to be associated with the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithPasswordPlainParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16d4c-137">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="16d4c-137">-PasswordCredentials</span></span>
<span data-ttu-id="16d4c-138">Lista poświadczeń haseł skojarzonych z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="16d4c-138">The list of password credentials associated with the application.</span></span>

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

### <span data-ttu-id="16d4c-139">-ReplyUrls</span><span class="sxs-lookup"><span data-stu-id="16d4c-139">-ReplyUrls</span></span>
<span data-ttu-id="16d4c-140">Adresy URL odpowiedzi aplikacji.</span><span class="sxs-lookup"><span data-stu-id="16d4c-140">The application reply urls.</span></span>

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

### <span data-ttu-id="16d4c-141">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="16d4c-141">-StartDate</span></span>
<span data-ttu-id="16d4c-142">Efektywna Data rozpoczęcia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="16d4c-142">The effective start date of the credential usage.</span></span>
<span data-ttu-id="16d4c-143">Domyślna wartość daty rozpoczęcia przypada dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="16d4c-143">The default start date value is today.</span></span> <span data-ttu-id="16d4c-144">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub po dniu, od którego certyfikat x509 jest ważny.</span><span class="sxs-lookup"><span data-stu-id="16d4c-144">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="16d4c-145">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="16d4c-145">-Confirm</span></span>
<span data-ttu-id="16d4c-146">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="16d4c-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16d4c-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16d4c-147">-WhatIf</span></span>
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

### <span data-ttu-id="16d4c-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d4c-148">-DefaultProfile</span></span>
<span data-ttu-id="16d4c-149">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="16d4c-149">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="16d4c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d4c-150">CommonParameters</span></span>
<span data-ttu-id="16d4c-151">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="16d4c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d4c-152">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16d4c-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d4c-153">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="16d4c-153">INPUTS</span></span>

## <span data-ttu-id="16d4c-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="16d4c-154">OUTPUTS</span></span>

### <span data-ttu-id="16d4c-155">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="16d4c-155">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>

## <span data-ttu-id="16d4c-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="16d4c-156">NOTES</span></span>
<span data-ttu-id="16d4c-157">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="16d4c-157">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="16d4c-158">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="16d4c-158">RELATED LINKS</span></span>

[<span data-ttu-id="16d4c-159">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="16d4c-159">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="16d4c-160">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="16d4c-160">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

[<span data-ttu-id="16d4c-161">Nowe — AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="16d4c-161">New-AzureRmADServicePrincipal</span></span>](./New-AzureRmADServicePrincipal.md)

[<span data-ttu-id="16d4c-162">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="16d4c-162">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="16d4c-163">Nowe — AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="16d4c-163">New-AzureRmADAppCredential</span></span>](./New-AzureRmADAppCredential.md)

[<span data-ttu-id="16d4c-164">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="16d4c-164">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

