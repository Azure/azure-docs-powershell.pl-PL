---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: 46977fe6b2e6cf3c3811c7d9bbd49262b06cec54
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242547"
---
# <span data-ttu-id="b20ac-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b20ac-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="b20ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b20ac-102">SYNOPSIS</span></span>
<span data-ttu-id="b20ac-103">Dodaje poświadczenia do istniejącego podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="b20ac-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="b20ac-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b20ac-104">SYNTAX</span></span>

### <span data-ttu-id="b20ac-105">SpObjectIdWithPasswordParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b20ac-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b20ac-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="b20ac-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b20ac-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="b20ac-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b20ac-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="b20ac-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b20ac-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="b20ac-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b20ac-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="b20ac-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b20ac-111">OPIS</span><span class="sxs-lookup"><span data-stu-id="b20ac-111">DESCRIPTION</span></span>
<span data-ttu-id="b20ac-112">To New-AzADSpCredential cmdlet może służyć do dodawania nowych poświadczeń lub do rollowania poświadczeń podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="b20ac-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="b20ac-113">Podmiot zabezpieczeń usługi jest identyfikowany przez dostarczenie identyfikatora obiektu lub nazwy podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="b20ac-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="b20ac-114">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b20ac-114">EXAMPLES</span></span>

### <span data-ttu-id="b20ac-115">Przykład 1. Tworzenie nowego poświadczenia podmiotu zabezpieczeń usługi przy użyciu wygenerowanego hasła</span><span class="sxs-lookup"><span data-stu-id="b20ac-115">Example 1: Create a new service principal credential using a generated password</span></span>

```powershell
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="b20ac-116">Nowe poświadczenia hasła są dodawane do istniejącego podmiotu zabezpieczeń usługi o identyfikatorze obiektu "1f99cf81-0146-4f4e-beae-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="b20ac-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="b20ac-117">Przykład 2. Tworzenie nowego poświadczenia podmiotu zabezpieczeń usługi przy użyciu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="b20ac-117">Example 2: Create a new service principal credential using a certificate</span></span>

```powershell
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="b20ac-118">Podany certyfikat X509 z kodem base64 jest dodawany do istniejącego podmiotu zabezpieczeń usługi przy użyciu jego publicznej sieci (SPN).</span><span class="sxs-lookup"><span data-stu-id="b20ac-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="b20ac-119">Przykład 3. Tworzenie nowego poświadczenia podmiotu zabezpieczeń usługi przy użyciu funkcji pipingu</span><span class="sxs-lookup"><span data-stu-id="b20ac-119">Example 3: Create a new service principal credential using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="b20ac-120">Pobiera podmiot zabezpieczeń usługi z identyfikatorem obiektu "1f99cf81-0146-4f4e-beae-2007d0668476" i potokami, które do New-AzADSpCredential, tworzą nowe poświadczenia podmiotu zabezpieczeń usługi dla tego podmiotu zabezpieczeń usługi z wygenerowanym hasłem.</span><span class="sxs-lookup"><span data-stu-id="b20ac-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="b20ac-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b20ac-121">PARAMETERS</span></span>

### <span data-ttu-id="b20ac-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="b20ac-122">-CertValue</span></span>
<span data-ttu-id="b20ac-123">Wartość typu poświadczeń "asymetrycznego".</span><span class="sxs-lookup"><span data-stu-id="b20ac-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="b20ac-124">Reprezentuje certyfikat zakodowany na podstawie 64.</span><span class="sxs-lookup"><span data-stu-id="b20ac-124">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithCertValueParameterSet, SPNWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b20ac-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b20ac-125">-DefaultProfile</span></span>
<span data-ttu-id="b20ac-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b20ac-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b20ac-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="b20ac-127">-EndDate</span></span>
<span data-ttu-id="b20ac-128">Data zakończenia użytkowania poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="b20ac-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="b20ac-129">Domyślna wartość daty końcowej wynosi jeden rok od dnia dzisiejszego.</span><span class="sxs-lookup"><span data-stu-id="b20ac-129">The default end date value is one year from today.</span></span>
<span data-ttu-id="b20ac-130">W przypadku poświadczeń typu "asymetrycznego" musi on być ustawiony na datę ważności certyfikatu X509 lub wcześniejszą.</span><span class="sxs-lookup"><span data-stu-id="b20ac-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="b20ac-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b20ac-131">-ObjectId</span></span>
<span data-ttu-id="b20ac-132">Identyfikator obiektu podmiotu zabezpieczeń usługi, do których chcesz dodać poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="b20ac-132">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b20ac-133">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="b20ac-133">-ServicePrincipalName</span></span>
<span data-ttu-id="b20ac-134">Nazwa (SPN) podmiotu zabezpieczeń usługi, do których chcesz dodać poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="b20ac-134">The name (SPN) of the service principal to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithCertValueParameterSet, SPNWithPasswordParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b20ac-135">-ServicePrincipalObject</span><span class="sxs-lookup"><span data-stu-id="b20ac-135">-ServicePrincipalObject</span></span>
<span data-ttu-id="b20ac-136">Obiekt podmiotu zabezpieczeń usługi, do który chcesz dodać poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="b20ac-136">The service principal object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b20ac-137">-StartDate</span><span class="sxs-lookup"><span data-stu-id="b20ac-137">-StartDate</span></span>
<span data-ttu-id="b20ac-138">Data rozpoczęcia użytkowania poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="b20ac-138">The effective start date of the credential usage.</span></span>
<span data-ttu-id="b20ac-139">Domyślna wartość daty rozpoczęcia to dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="b20ac-139">The default start date value is today.</span></span>
<span data-ttu-id="b20ac-140">W przypadku poświadczeń typu "asymetrycznego" musi on być ustawiony na datę, od kiedy certyfikat X509 jest prawidłowy, lub później.</span><span class="sxs-lookup"><span data-stu-id="b20ac-140">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="b20ac-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b20ac-141">-Confirm</span></span>
<span data-ttu-id="b20ac-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b20ac-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b20ac-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b20ac-143">-WhatIf</span></span>
<span data-ttu-id="b20ac-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b20ac-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b20ac-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b20ac-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b20ac-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b20ac-146">CommonParameters</span></span>
<span data-ttu-id="b20ac-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b20ac-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b20ac-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b20ac-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b20ac-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b20ac-149">INPUTS</span></span>

### <span data-ttu-id="b20ac-150">System.String</span><span class="sxs-lookup"><span data-stu-id="b20ac-150">System.String</span></span>

### <span data-ttu-id="b20ac-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b20ac-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="b20ac-152">System.DateTime</span><span class="sxs-lookup"><span data-stu-id="b20ac-152">System.DateTime</span></span>

## <span data-ttu-id="b20ac-153">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b20ac-153">OUTPUTS</span></span>

### <span data-ttu-id="b20ac-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span><span class="sxs-lookup"><span data-stu-id="b20ac-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="b20ac-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="b20ac-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="b20ac-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b20ac-156">NOTES</span></span>

## <span data-ttu-id="b20ac-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b20ac-157">RELATED LINKS</span></span>

[<span data-ttu-id="b20ac-158">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b20ac-158">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="b20ac-159">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="b20ac-159">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="b20ac-160">Get-AzadServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="b20ac-160">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



