---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
ms.openlocfilehash: 37354a29a0ec6b8994ef05d7bf8859be249e6e88
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544843"
---
# <span data-ttu-id="cb166-101">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="cb166-101">New-AzureRmADAppCredential</span></span>

## <span data-ttu-id="cb166-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cb166-102">SYNOPSIS</span></span>
<span data-ttu-id="cb166-103">Umożliwia dodanie poświadczenia do istniejącej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cb166-103">Adds a credential to an existing application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb166-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cb166-104">SYNTAX</span></span>

### <span data-ttu-id="cb166-105">ApplicationObjectIdWithPasswordParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cb166-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADAppCredential -ObjectId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb166-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb166-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ObjectId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb166-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb166-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb166-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb166-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb166-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb166-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb166-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb166-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb166-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb166-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb166-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb166-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="cb166-113">Opis</span><span class="sxs-lookup"><span data-stu-id="cb166-113">DESCRIPTION</span></span>
<span data-ttu-id="cb166-114">Za pomocą polecenia cmdlet New-AzureRmADAppCredential można dodać nowe poświadczenia lub wycofać poświadczenia dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cb166-114">The New-AzureRmADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="cb166-115">Aplikacja jest identyfikowana przez podanie identyfikatora obiektu aplikacji lub identyfikatora aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cb166-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="cb166-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cb166-116">EXAMPLES</span></span>

### <span data-ttu-id="cb166-117">Przykład 1-Tworzenie nowego poświadczenia aplikacji przy użyciu hasła</span><span class="sxs-lookup"><span data-stu-id="cb166-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzureRmADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="cb166-118">Nowe poświadczenie hasła zostanie dodane do istniejącego Appplication o identyfikatorze obiektu "1f89cf81-0146-4f4e-beae-2007d0668416".</span><span class="sxs-lookup"><span data-stu-id="cb166-118">A new password credential is added to the existing appplication with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="cb166-119">Przykład 2 — Tworzenie nowego poświadczenia aplikacji przy użyciu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="cb166-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 
PS C:\> $cer.Import("C:\myapp.cer") 
PS C:\> $binCert = $cer.GetRawCertData() 
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="cb166-120">Publiczny certyfikat x509 zakodowany w formacie base64 ("MojaApl. cer") zostanie dodany do istniejącej aplikacji z identyfikatorem aplikacji "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span><span class="sxs-lookup"><span data-stu-id="cb166-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="cb166-121">Przykład 3 — Tworzenie nowego poświadczenia aplikacji przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="cb166-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzureRmADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzureRmADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="cb166-122">Pobiera aplikację o identyfikatorze obiektu "1f89cf81-0146-4f4e-beae-2007d0668416" i potokach, które mają New-AzureRmADAppCredential, aby utworzyć nowe poświadczenie aplikacji dla tej aplikacji z danym hasłem.</span><span class="sxs-lookup"><span data-stu-id="cb166-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzureRmADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="cb166-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cb166-123">PARAMETERS</span></span>

### <span data-ttu-id="cb166-124">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="cb166-124">-ApplicationId</span></span>
<span data-ttu-id="cb166-125">Identyfikator aplikacji, do której ma zostać dodane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="cb166-125">The application id of the application to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb166-126">-Applicationobject</span><span class="sxs-lookup"><span data-stu-id="cb166-126">-ApplicationObject</span></span>
<span data-ttu-id="cb166-127">Obiekt aplikacji, do którego mają zostać dodane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="cb166-127">The application object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithCertValueParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cb166-128">-CertValue</span><span class="sxs-lookup"><span data-stu-id="cb166-128">-CertValue</span></span>
<span data-ttu-id="cb166-129">Wartość "asymetrycznego" typu poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="cb166-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="cb166-130">Reprezentuje certyfikat zakodowany Base 64.</span><span class="sxs-lookup"><span data-stu-id="cb166-130">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DisplayNameWithCertValueParameterSet, ApplicationObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb166-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb166-131">-DefaultProfile</span></span>
<span data-ttu-id="cb166-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="cb166-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cb166-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="cb166-133">-DisplayName</span></span>
<span data-ttu-id="cb166-134">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cb166-134">The display name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithPasswordParameterSet, DisplayNameWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb166-135">-EndDate</span><span class="sxs-lookup"><span data-stu-id="cb166-135">-EndDate</span></span>
<span data-ttu-id="cb166-136">Efektywna Data zakończenia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="cb166-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="cb166-137">Domyślną wartością daty zakończenia jest rok od dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="cb166-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="cb166-138">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub przed datą ważności certyfikatu x509.</span><span class="sxs-lookup"><span data-stu-id="cb166-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb166-139">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cb166-139">-ObjectId</span></span>
<span data-ttu-id="cb166-140">Identyfikator obiektu aplikacji, do którego mają zostać dodane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="cb166-140">The object id of the application to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb166-141">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="cb166-141">-Password</span></span>
<span data-ttu-id="cb166-142">Hasło, które ma zostać skojarzone z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="cb166-142">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: DisplayNameWithPasswordParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb166-143">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="cb166-143">-StartDate</span></span>
<span data-ttu-id="cb166-144">Efektywna Data rozpoczęcia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="cb166-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="cb166-145">Domyślna wartość daty rozpoczęcia przypada dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="cb166-145">The default start date value is today.</span></span> <span data-ttu-id="cb166-146">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub po dniu, od którego certyfikat x509 jest ważny.</span><span class="sxs-lookup"><span data-stu-id="cb166-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb166-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cb166-147">-Confirm</span></span>
<span data-ttu-id="cb166-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb166-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb166-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb166-149">-WhatIf</span></span>
<span data-ttu-id="cb166-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb166-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cb166-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cb166-151">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cb166-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb166-152">CommonParameters</span></span>
<span data-ttu-id="cb166-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb166-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb166-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb166-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb166-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb166-155">INPUTS</span></span>

### <span data-ttu-id="cb166-156">System. GUID</span><span class="sxs-lookup"><span data-stu-id="cb166-156">System.Guid</span></span>

### <span data-ttu-id="cb166-157">System. String</span><span class="sxs-lookup"><span data-stu-id="cb166-157">System.String</span></span>

### <span data-ttu-id="cb166-158">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="cb166-158">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADApplication</span></span>
<span data-ttu-id="cb166-159">Parametry: Applicationobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="cb166-159">Parameters: ApplicationObject (ByValue)</span></span>

### <span data-ttu-id="cb166-160">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="cb166-160">System.Security.SecureString</span></span>

### <span data-ttu-id="cb166-161">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="cb166-161">System.DateTime</span></span>

## <span data-ttu-id="cb166-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cb166-162">OUTPUTS</span></span>

### <span data-ttu-id="cb166-163">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="cb166-163">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="cb166-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cb166-164">NOTES</span></span>

## <span data-ttu-id="cb166-165">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb166-165">RELATED LINKS</span></span>

[<span data-ttu-id="cb166-166">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="cb166-166">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="cb166-167">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="cb166-167">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="cb166-168">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="cb166-168">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)
