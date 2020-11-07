---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: 4c68470b97134019b0abf7724012f3a6fab4627f
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93892537"
---
# <span data-ttu-id="79896-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="79896-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="79896-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="79896-102">SYNOPSIS</span></span>
<span data-ttu-id="79896-103">Umożliwia dodanie poświadczenia do istniejącego podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="79896-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="79896-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="79896-104">SYNTAX</span></span>

### <span data-ttu-id="79896-105">SpObjectIdWithPasswordParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="79896-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <Guid> [-Password <SecureString>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79896-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="79896-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <Guid> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79896-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="79896-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79896-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="79896-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-Password <SecureString>] [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79896-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="79896-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String>
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="79896-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="79896-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-Password <SecureString>]
 [-StartDate <DateTime>] [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="79896-111">Opis</span><span class="sxs-lookup"><span data-stu-id="79896-111">DESCRIPTION</span></span>
<span data-ttu-id="79896-112">Za pomocą polecenia cmdlet New-AzADSpCredential można dodać nowe poświadczenia lub wycofać poświadczenia dla podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="79896-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="79896-113">Wartość główna usługi jest identyfikowana przez podanie identyfikatora obiektu lub nazwy głównej usługi.</span><span class="sxs-lookup"><span data-stu-id="79896-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="79896-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="79896-114">EXAMPLES</span></span>

### <span data-ttu-id="79896-115">Przykład 1-Tworzenie nowego poświadczenia podmiotu zabezpieczeń usługi przy użyciu wygenerowanego hasła</span><span class="sxs-lookup"><span data-stu-id="79896-115">Example 1 - Create a new service principal credential using a generated password</span></span>

```
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="79896-116">Nowe poświadczenie hasła zostanie dodane do istniejącego podmiotu usługi z identyfikatorem obiektu "1f99cf81-0146-4f4e-beae-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="79896-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="79896-117">Przykład 2 — Tworzenie nowego poświadczenia podmiotu zabezpieczeń usługi przy użyciu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="79896-117">Example 2 - Create a new service principal credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 
PS C:\> $cer.Import("C:\myapp.cer") 
PS C:\> $binCert = $cer.GetRawCertData() 
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="79896-118">Publiczny certyfikat x509 zakodowany w formacie base64 ("MojaApl. cer") jest dodawany do istniejącego podmiotu usługi przy użyciu jego nazwy SPN.</span><span class="sxs-lookup"><span data-stu-id="79896-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="79896-119">Przykład 3 — Tworzenie nowego poświadczenia podmiotu zabezpieczeń usługi przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="79896-119">Example 3 - Create a new service principal credential using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="79896-120">Pobiera podmiot zabezpieczeń usługi o identyfikatorze obiektu "1f99cf81-0146-4f4e-beae-2007d0668476" i potoki, które mają New-AzADSpCredential, aby utworzyć nową główną nazwę poświadczenia usługi dla tego podmiotu usługi z wygenerowanym hasłem.</span><span class="sxs-lookup"><span data-stu-id="79896-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="79896-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="79896-121">PARAMETERS</span></span>

### <span data-ttu-id="79896-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="79896-122">-CertValue</span></span>
<span data-ttu-id="79896-123">Wartość "asymetrycznego" typu poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="79896-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="79896-124">Reprezentuje certyfikat zakodowany Base 64.</span><span class="sxs-lookup"><span data-stu-id="79896-124">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="79896-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79896-125">-DefaultProfile</span></span>
<span data-ttu-id="79896-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="79896-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="79896-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="79896-127">-EndDate</span></span>
<span data-ttu-id="79896-128">Efektywna Data zakończenia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="79896-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="79896-129">Domyślną wartością daty zakończenia jest rok od dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="79896-129">The default end date value is one year from today.</span></span> <span data-ttu-id="79896-130">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub przed datą ważności certyfikatu x509.</span><span class="sxs-lookup"><span data-stu-id="79896-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="79896-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="79896-131">-ObjectId</span></span>
<span data-ttu-id="79896-132">Identyfikator obiektu podmiotu usługi, do którego mają zostać dodane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="79896-132">The object id of the service principal to add the credentials to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpObjectIdWithPasswordParameterSet, SpObjectIdWithCertValueParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79896-133">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="79896-133">-Password</span></span>
<span data-ttu-id="79896-134">Hasło, które ma zostać skojarzone z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="79896-134">The password to be associated with the application.</span></span>

```yaml
Type: System.Security.SecureString
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Security.SecureString
Parameter Sets: ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79896-135">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="79896-135">-ServicePrincipalName</span></span>
<span data-ttu-id="79896-136">Nazwa (SPN) podmiotu usługi, do którego mają zostać dodane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="79896-136">The name (SPN) of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="79896-137">-Serviceprincipalobject</span><span class="sxs-lookup"><span data-stu-id="79896-137">-ServicePrincipalObject</span></span>
<span data-ttu-id="79896-138">Obiekt główny usługi, do którego mają zostać dodane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="79896-138">The service principal object to add the credentials to.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: ServicePrincipalObjectWithCertValueParameterSet, ServicePrincipalObjectWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79896-139">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="79896-139">-StartDate</span></span>
<span data-ttu-id="79896-140">Efektywna Data rozpoczęcia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="79896-140">The effective start date of the credential usage.</span></span>
<span data-ttu-id="79896-141">Domyślna wartość daty rozpoczęcia przypada dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="79896-141">The default start date value is today.</span></span> <span data-ttu-id="79896-142">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub po dniu, od którego certyfikat x509 jest ważny.</span><span class="sxs-lookup"><span data-stu-id="79896-142">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="79896-143">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="79896-143">-Confirm</span></span>
<span data-ttu-id="79896-144">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79896-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79896-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79896-145">-WhatIf</span></span>
<span data-ttu-id="79896-146">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="79896-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79896-147">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="79896-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79896-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79896-148">CommonParameters</span></span>
<span data-ttu-id="79896-149">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="79896-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79896-150">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79896-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79896-151">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="79896-151">INPUTS</span></span>

### <span data-ttu-id="79896-152">System. GUID</span><span class="sxs-lookup"><span data-stu-id="79896-152">System.Guid</span></span>

### <span data-ttu-id="79896-153">System. String</span><span class="sxs-lookup"><span data-stu-id="79896-153">System.String</span></span>

### <span data-ttu-id="79896-154">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="79896-154">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="79896-155">Parametry: serviceprincipalobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="79896-155">Parameters: ServicePrincipalObject (ByValue)</span></span>

### <span data-ttu-id="79896-156">System. Security. SecureString</span><span class="sxs-lookup"><span data-stu-id="79896-156">System.Security.SecureString</span></span>

### <span data-ttu-id="79896-157">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="79896-157">System.DateTime</span></span>

## <span data-ttu-id="79896-158">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="79896-158">OUTPUTS</span></span>

### <span data-ttu-id="79896-159">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="79896-159">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="79896-160">Microsoft. Azure. Commands. resources. models. Authorization. PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="79896-160">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="79896-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="79896-161">NOTES</span></span>

## <span data-ttu-id="79896-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="79896-162">RELATED LINKS</span></span>

[<span data-ttu-id="79896-163">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="79896-163">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="79896-164">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="79896-164">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="79896-165">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="79896-165">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



