---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADAppCredential.md
ms.openlocfilehash: 8290ad3779c91565509833bbf41d7f9b37b07635
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100186450"
---
# <span data-ttu-id="fa21a-101">New-AzADAppCredential</span><span class="sxs-lookup"><span data-stu-id="fa21a-101">New-AzADAppCredential</span></span>

## <span data-ttu-id="fa21a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fa21a-102">SYNOPSIS</span></span>
<span data-ttu-id="fa21a-103">Dodaje poświadczenia do istniejącej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fa21a-103">Adds a credential to an existing application.</span></span>

## <span data-ttu-id="fa21a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="fa21a-104">SYNTAX</span></span>

### <span data-ttu-id="fa21a-105">ApplicationObjectIdWithPasswordParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="fa21a-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa21a-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa21a-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa21a-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa21a-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa21a-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa21a-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationId <Guid> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa21a-109">DisplayNameWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa21a-109">DisplayNameWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa21a-110">DisplayNameWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa21a-110">DisplayNameWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -DisplayName <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa21a-111">ApplicationObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa21a-111">ApplicationObjectWithCertValueParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fa21a-112">ApplicationObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa21a-112">ApplicationObjectWithPasswordParameterSet</span></span>
```
New-AzADAppCredential -ApplicationObject <PSADApplication> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fa21a-113">OPIS</span><span class="sxs-lookup"><span data-stu-id="fa21a-113">DESCRIPTION</span></span>
<span data-ttu-id="fa21a-114">To New-AzADAppCredential cmdlet może służyć do dodawania nowych poświadczeń lub do rzutowania poświadczeń aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fa21a-114">The New-AzADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="fa21a-115">Aplikacja jest identyfikowana przez podanie identyfikatora obiektu aplikacji lub identyfikatora aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fa21a-115">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="fa21a-116">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="fa21a-116">EXAMPLES</span></span>

### <span data-ttu-id="fa21a-117">Przykład 1. Tworzenie nowego poświadczenia aplikacji przy użyciu hasła</span><span class="sxs-lookup"><span data-stu-id="fa21a-117">Example 1 - Create a new application credential using a password</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> New-AzADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="fa21a-118">Nowe poświadczenia hasła zostaną dodane do istniejącej aplikacji o identyfikatorze obiektu "1f89cf81-0146-4f4e-beae-2007d0668416".</span><span class="sxs-lookup"><span data-stu-id="fa21a-118">A new password credential is added to the existing application with object id '1f89cf81-0146-4f4e-beae-2007d0668416'.</span></span>

### <span data-ttu-id="fa21a-119">Przykład 2. Tworzenie nowego poświadczenia aplikacji przy użyciu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="fa21a-119">Example 2 - Create a new application credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="fa21a-120">Podany certyfikat x509 (myapp.cer) jest dodawany do istniejącej aplikacji z identyfikatorem aplikacji '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span><span class="sxs-lookup"><span data-stu-id="fa21a-120">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing application with application id '4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58'.</span></span>

### <span data-ttu-id="fa21a-121">Przykład 3. Tworzenie nowego poświadczenia aplikacji przy użyciu funkcji rurowych</span><span class="sxs-lookup"><span data-stu-id="fa21a-121">Example 3 - Create a new application credential using piping</span></span>

```
PS C:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS C:\> Get-AzADApplication -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 | New-AzADAppCredential -Password $SecureStringPassword
```

<span data-ttu-id="fa21a-122">Pobiera aplikację o identyfikatorze obiektu "1f89cf81-0146-4f4e-beae-2007d0668416" i potoki, które do systemu New-AzADAppCredential są przekierowywowane w celu utworzenia dla tej aplikacji nowego poświadczenia przy użyciu danego hasła.</span><span class="sxs-lookup"><span data-stu-id="fa21a-122">Gets the application with object id '1f89cf81-0146-4f4e-beae-2007d0668416' and pipes that to the New-AzADAppCredential to create a new application credential for that application with the given password.</span></span>

## <span data-ttu-id="fa21a-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fa21a-123">PARAMETERS</span></span>

### <span data-ttu-id="fa21a-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="fa21a-124">-ApplicationId</span></span>
<span data-ttu-id="fa21a-125">Identyfikator aplikacji, do których chcesz dodać poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="fa21a-125">The application id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="fa21a-126">-ApplicationObject</span><span class="sxs-lookup"><span data-stu-id="fa21a-126">-ApplicationObject</span></span>
<span data-ttu-id="fa21a-127">Obiekt aplikacji, do który chcesz dodać poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="fa21a-127">The application object to add the credentials to.</span></span>

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

### <span data-ttu-id="fa21a-128">-CertValue</span><span class="sxs-lookup"><span data-stu-id="fa21a-128">-CertValue</span></span>
<span data-ttu-id="fa21a-129">Wartość typu poświadczeń "asymetrycznego".</span><span class="sxs-lookup"><span data-stu-id="fa21a-129">The value of the "asymmetric" credential type.</span></span> <span data-ttu-id="fa21a-130">Reprezentuje certyfikat zakodowany na podstawie 64.</span><span class="sxs-lookup"><span data-stu-id="fa21a-130">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="fa21a-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa21a-131">-DefaultProfile</span></span>
<span data-ttu-id="fa21a-132">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="fa21a-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fa21a-133">— DisplayName</span><span class="sxs-lookup"><span data-stu-id="fa21a-133">-DisplayName</span></span>
<span data-ttu-id="fa21a-134">Nazwa wyświetlana aplikacji.</span><span class="sxs-lookup"><span data-stu-id="fa21a-134">The display name of the application.</span></span>

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

### <span data-ttu-id="fa21a-135">-EndDate</span><span class="sxs-lookup"><span data-stu-id="fa21a-135">-EndDate</span></span>
<span data-ttu-id="fa21a-136">Data zakończenia użytkowania poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="fa21a-136">The effective end date of the credential usage.</span></span> <span data-ttu-id="fa21a-137">Domyślna wartość daty końcowej wynosi jeden rok od dnia dzisiejszego.</span><span class="sxs-lookup"><span data-stu-id="fa21a-137">The default end date value is one year from today.</span></span>  <span data-ttu-id="fa21a-138">W przypadku poświadczeń typu "asymetrycznego" musi on być ustawiony na datę ważności certyfikatu X509 lub wcześniejszą.</span><span class="sxs-lookup"><span data-stu-id="fa21a-138">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="fa21a-139">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fa21a-139">-ObjectId</span></span>
<span data-ttu-id="fa21a-140">Identyfikator obiektu aplikacji, do których chcesz dodać poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="fa21a-140">The object id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="fa21a-141">— Hasło</span><span class="sxs-lookup"><span data-stu-id="fa21a-141">-Password</span></span>
<span data-ttu-id="fa21a-142">Hasło, które ma zostać skojarzone z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="fa21a-142">The password to be associated with the application.</span></span>

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

### <span data-ttu-id="fa21a-143">-StartDate</span><span class="sxs-lookup"><span data-stu-id="fa21a-143">-StartDate</span></span>
<span data-ttu-id="fa21a-144">Data rozpoczęcia użytkowania poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="fa21a-144">The effective start date of the credential usage.</span></span> <span data-ttu-id="fa21a-145">Domyślna wartość daty rozpoczęcia to dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="fa21a-145">The default start date value is today.</span></span> <span data-ttu-id="fa21a-146">W przypadku poświadczeń typu "asymetrycznego" musi on być ustawiony na datę, od kiedy certyfikat X509 jest prawidłowy, lub później.</span><span class="sxs-lookup"><span data-stu-id="fa21a-146">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="fa21a-147">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="fa21a-147">-Confirm</span></span>
<span data-ttu-id="fa21a-148">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="fa21a-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fa21a-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fa21a-149">-WhatIf</span></span>
<span data-ttu-id="fa21a-150">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="fa21a-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fa21a-151">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="fa21a-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fa21a-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa21a-152">CommonParameters</span></span>
<span data-ttu-id="fa21a-153">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa21a-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa21a-154">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fa21a-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa21a-155">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa21a-155">INPUTS</span></span>

### <span data-ttu-id="fa21a-156">System.String</span><span class="sxs-lookup"><span data-stu-id="fa21a-156">System.String</span></span>

### <span data-ttu-id="fa21a-157">System.Guid</span><span class="sxs-lookup"><span data-stu-id="fa21a-157">System.Guid</span></span>

### <span data-ttu-id="fa21a-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span><span class="sxs-lookup"><span data-stu-id="fa21a-158">Microsoft.Azure.Commands.ActiveDirectory.PSADApplication</span></span>

### <span data-ttu-id="fa21a-159">System.Security.SecureString</span><span class="sxs-lookup"><span data-stu-id="fa21a-159">System.Security.SecureString</span></span>

### <span data-ttu-id="fa21a-160">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="fa21a-160">System.DateTime</span></span>

## <span data-ttu-id="fa21a-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fa21a-161">OUTPUTS</span></span>

### <span data-ttu-id="fa21a-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="fa21a-162">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="fa21a-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="fa21a-163">NOTES</span></span>

## <span data-ttu-id="fa21a-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fa21a-164">RELATED LINKS</span></span>

[<span data-ttu-id="fa21a-165">Get-AzadAppCredential</span><span class="sxs-lookup"><span data-stu-id="fa21a-165">Get-AzADAppCredential</span></span>](./Get-AzADAppCredential.md)

[<span data-ttu-id="fa21a-166">Remove-AzadAppCredential</span><span class="sxs-lookup"><span data-stu-id="fa21a-166">Remove-AzADAppCredential</span></span>](./Remove-AzADAppCredential.md)

[<span data-ttu-id="fa21a-167">Get-AzadApplication</span><span class="sxs-lookup"><span data-stu-id="fa21a-167">Get-AzADApplication</span></span>](./Get-AzADApplication.md)

