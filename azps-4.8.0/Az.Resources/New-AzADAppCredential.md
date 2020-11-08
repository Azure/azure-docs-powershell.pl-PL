---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
ms.openlocfilehash: 8290ad3779c91565509833bbf41d7f9b37b07635
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94062136"
---
# <span data-ttu-id="fc4a5-101">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="fc4a5-101">New-AzADAppCredential</span></span>

## <span data-ttu-id="fc4a5-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fc4a5-102">SYNOPSIS</span></span>
<span data-ttu-id="fc4a5-103">Umożliwia dodanie poświadczenia do istniejącej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-103">Adds a credential to an existing application.</span></span>

## <span data-ttu-id="fc4a5-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fc4a5-104">SYNTAX</span></span>

### <span data-ttu-id="fc4a5-105">ApplicationObjectIdWithPasswordParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="fc4a5-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4a5-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4a5-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4a5-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4a5-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4a5-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4a5-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4a5-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4a5-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4a5-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4a5-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4a5-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4a5-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fc4a5-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="fc4a5-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc4a5-113">Opis</span><span class="sxs-lookup"><span data-stu-id="fc4a5-113">DESCRIPTION</span></span>
<span data-ttu-id="fc4a5-114">Za pomocą polecenia cmdlet New-AzADAppCredential można dodać nowe poświadczenia lub wycofać poświadczenia dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-114">The New-AzADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="fc4a5-115">Aplikacja jest identyfikowana przez podanie identyfikatora obiektu aplikacji lub identyfikatora aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="fc4a5-116">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fc4a5-116">EXAMPLES</span></span>

### <span data-ttu-id="fc4a5-117">Przykład 1-Tworzenie nowego poświadczenia aplikacji przy użyciu hasła</span><span class="sxs-lookup"><span data-stu-id="fc4a5-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="fc4a5-118">Do istniejącej aplikacji zostanie dodane nowe poświadczenie hasła z obiektem o identyfikatorze "1f89cf81-0146-4f4e-beae-2007d0668416".</span><span class="sxs-lookup"><span data-stu-id="fc4a5-118">A new password credential is added to the existing application with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="fc4a5-119">Przykład 2 — Tworzenie nowego poświadczenia aplikacji przy użyciu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="fc4a5-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="fc4a5-120">Publiczny certyfikat x509 zakodowany w formacie base64 ("MojaApl. cer") zostanie dodany do istniejącej aplikacji z identyfikatorem aplikacji "4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58".</span><span class="sxs-lookup"><span data-stu-id="fc4a5-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="fc4a5-121">Przykład 3 — Tworzenie nowego poświadczenia aplikacji przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="fc4a5-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="fc4a5-122">Pobiera aplikację o identyfikatorze obiektu "1f89cf81-0146-4f4e-beae-2007d0668416" i potokach, które mają New-AzADAppCredential, aby utworzyć nowe poświadczenie aplikacji dla tej aplikacji z danym hasłem.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="fc4a5-123">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fc4a5-123">PARAMETERS</span></span>

### <span data-ttu-id="fc4a5-124">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="fc4a5-124">-ApplicationId</span></span>
<span data-ttu-id="fc4a5-125">Identyfikator aplikacji, do której ma zostać dodane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-125">The application id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="fc4a5-126">-Applicationobject</span><span class="sxs-lookup"><span data-stu-id="fc4a5-126">-ApplicationObject</span></span>
<span data-ttu-id="fc4a5-127">Obiekt aplikacji, do którego mają zostać dodane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-127">The application object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADApplication
Parameter Sets: ApplicationObjectWithCertValueParameterSet, ApplicationObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4a5-128">-CertValue</span><span class="sxs-lookup"><span data-stu-id="fc4a5-128">-CertValue</span></span>
<span data-ttu-id="fc4a5-129">Wartość "asymetrycznego" typu poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="fc4a5-130">Reprezentuje certyfikat zakodowany Base 64.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-130">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="fc4a5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc4a5-131">-DefaultProfile</span></span>
<span data-ttu-id="fc4a5-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fc4a5-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc4a5-133">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="fc4a5-133">-DisplayName</span></span>
<span data-ttu-id="fc4a5-134">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-134">The display name of the application.</span></span>

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

### <span data-ttu-id="fc4a5-135">-EndDate</span><span class="sxs-lookup"><span data-stu-id="fc4a5-135">-EndDate</span></span>
<span data-ttu-id="fc4a5-136">Efektywna Data zakończenia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="fc4a5-137">Domyślną wartością daty zakończenia jest rok od dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="fc4a5-138">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub przed datą ważności certyfikatu x509.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="fc4a5-139">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fc4a5-139">-ObjectId</span></span>
<span data-ttu-id="fc4a5-140">Identyfikator obiektu aplikacji, do którego mają zostać dodane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-140">The object id of the application to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fc4a5-141">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="fc4a5-141">-Password</span></span>
<span data-ttu-id="fc4a5-142">Hasło, które ma zostać skojarzone z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-142">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="fc4a5-143">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="fc4a5-143">-StartDate</span></span>
<span data-ttu-id="fc4a5-144">Efektywna Data rozpoczęcia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="fc4a5-145">Domyślna wartość daty rozpoczęcia przypada dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-145">The default start date value is today.</span></span> <span data-ttu-id="fc4a5-146">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub po dniu, od którego certyfikat x509 jest ważny.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="fc4a5-147">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fc4a5-147">-Confirm</span></span>
<span data-ttu-id="fc4a5-148">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc4a5-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc4a5-149">-WhatIf</span></span>
<span data-ttu-id="fc4a5-150">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc4a5-151">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc4a5-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc4a5-152">CommonParameters</span></span>
<span data-ttu-id="fc4a5-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fc4a5-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc4a5-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fc4a5-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc4a5-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fc4a5-155">INPUTS</span></span>

### <span data-ttu-id="fc4a5-156">System. String</span><span class="sxs-lookup"><span data-stu-id="fc4a5-156">System.String</span></span>

### <span data-ttu-id="fc4a5-157">System. GUID</span><span class="sxs-lookup"><span data-stu-id="fc4a5-157">System.Guid</span></span>

### <span data-ttu-id="fc4a5-158">Microsoft. Azure. Commands. pozycji. PSADApplication</span><span class="sxs-lookup"><span data-stu-id="fc4a5-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="fc4a5-159">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="fc4a5-159">System.Security.SecureString</span></span>

### <span data-ttu-id="fc4a5-160">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="fc4a5-160">System.DateTime</span></span>

## <span data-ttu-id="fc4a5-161">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fc4a5-161">OUTPUTS</span></span>

### <span data-ttu-id="fc4a5-162">Microsoft. Azure. Commands. pozycji. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="fc4a5-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="fc4a5-163">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fc4a5-163">NOTES</span></span>

## <span data-ttu-id="fc4a5-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fc4a5-164">RELATED LINKS</span></span>

[<span data-ttu-id="fc4a5-165">Get-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="fc4a5-165">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="fc4a5-166">Remove-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="fc4a5-166">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="fc4a5-167">Get-AzADApplication</span><span class="sxs-lookup"><span data-stu-id="fc4a5-167">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

