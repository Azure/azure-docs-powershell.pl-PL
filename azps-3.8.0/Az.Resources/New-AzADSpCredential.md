---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azadspcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzADSpCredential.md
ms.openlocfilehash: 98f127386a606881a0f8359e605ee2b96168a9b5
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895829"
---
# <span data-ttu-id="f86aa-101">New-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="f86aa-101">New-AzADSpCredential</span></span>

## <span data-ttu-id="f86aa-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f86aa-102">SYNOPSIS</span></span>
<span data-ttu-id="f86aa-103">Umożliwia dodanie poświadczenia do istniejącego podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="f86aa-103">Adds a credential to an existing service principal.</span></span>

## <span data-ttu-id="f86aa-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f86aa-104">SYNTAX</span></span>

### <span data-ttu-id="f86aa-105">SpObjectIdWithPasswordParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f86aa-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzADSpCredential -ObjectId <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f86aa-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="f86aa-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f86aa-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="f86aa-107">SPNWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f86aa-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="f86aa-108">SPNWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalName <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f86aa-109">ServicePrincipalObjectWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="f86aa-109">ServicePrincipalObjectWithCertValueParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f86aa-110">ServicePrincipalObjectWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="f86aa-110">ServicePrincipalObjectWithPasswordParameterSet</span></span>
```
New-AzADSpCredential -ServicePrincipalObject <PSADServicePrincipal> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f86aa-111">Opis</span><span class="sxs-lookup"><span data-stu-id="f86aa-111">DESCRIPTION</span></span>
<span data-ttu-id="f86aa-112">Za pomocą polecenia cmdlet New-AzADSpCredential można dodać nowe poświadczenia lub wycofać poświadczenia dla podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="f86aa-112">The New-AzADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="f86aa-113">Wartość główna usługi jest identyfikowana przez podanie identyfikatora obiektu lub nazwy głównej usługi.</span><span class="sxs-lookup"><span data-stu-id="f86aa-113">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="f86aa-114">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f86aa-114">EXAMPLES</span></span>

### <span data-ttu-id="f86aa-115">Przykład 1-Tworzenie nowego poświadczenia podmiotu zabezpieczeń usługi przy użyciu wygenerowanego hasła</span><span class="sxs-lookup"><span data-stu-id="f86aa-115">Example 1 - Create a new service principal credential using a generated password</span></span>

```
PS C:\> New-AzADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="f86aa-116">Nowe poświadczenie hasła zostanie dodane do istniejącego podmiotu usługi z identyfikatorem obiektu "1f99cf81-0146-4f4e-beae-2007d0668476".</span><span class="sxs-lookup"><span data-stu-id="f86aa-116">A new password credential is added to the existing service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476'.</span></span>

### <span data-ttu-id="f86aa-117">Przykład 2 — Tworzenie nowego poświadczenia podmiotu zabezpieczeń usługi przy użyciu certyfikatu</span><span class="sxs-lookup"><span data-stu-id="f86aa-117">Example 2 - Create a new service principal credential using a certificate</span></span>

```
PS C:\> $cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate2
PS C:\> $cer.Import("C:\myapp.cer")
PS C:\> $binCert = $cer.GetRawCertData()
PS C:\> $credValue = [System.Convert]::ToBase64String($binCert)
PS C:\> New-AzADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.NotBefore -EndDate $cer.NotAfter
```

<span data-ttu-id="f86aa-118">Publiczny certyfikat x509 zakodowany w formacie base64 ("MojaApl. cer") jest dodawany do istniejącego podmiotu usługi przy użyciu jego nazwy SPN.</span><span class="sxs-lookup"><span data-stu-id="f86aa-118">The supplied base64 encoded public X509 certificate ("myapp.cer") is added to the existing service principal using its SPN.</span></span>

### <span data-ttu-id="f86aa-119">Przykład 3 — Tworzenie nowego poświadczenia podmiotu zabezpieczeń usługi przy użyciu połączeń rurowych</span><span class="sxs-lookup"><span data-stu-id="f86aa-119">Example 3 - Create a new service principal credential using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 | New-AzADSpCredential

Secret    : System.Security.SecureString
StartDate : 11/12/2018 9:36:05 PM
EndDate   : 11/12/2019 9:36:05 PM
KeyId     : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
Type      : Password
```

<span data-ttu-id="f86aa-120">Pobiera podmiot zabezpieczeń usługi o identyfikatorze obiektu "1f99cf81-0146-4f4e-beae-2007d0668476" i potoki, które mają New-AzADSpCredential, aby utworzyć nową główną nazwę poświadczenia usługi dla tego podmiotu usługi z wygenerowanym hasłem.</span><span class="sxs-lookup"><span data-stu-id="f86aa-120">Gets the service principal with object id '1f99cf81-0146-4f4e-beae-2007d0668476' and pipes that to the New-AzADSpCredential to create a new service principal credential for that service principal with a generated password.</span></span>

## <span data-ttu-id="f86aa-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f86aa-121">PARAMETERS</span></span>

### <span data-ttu-id="f86aa-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="f86aa-122">-CertValue</span></span>
<span data-ttu-id="f86aa-123">Wartość "asymetrycznego" typu poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="f86aa-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="f86aa-124">Reprezentuje certyfikat zakodowany Base 64.</span><span class="sxs-lookup"><span data-stu-id="f86aa-124">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="f86aa-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f86aa-125">-DefaultProfile</span></span>
<span data-ttu-id="f86aa-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f86aa-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f86aa-127">-EndDate</span><span class="sxs-lookup"><span data-stu-id="f86aa-127">-EndDate</span></span>
<span data-ttu-id="f86aa-128">Efektywna Data zakończenia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="f86aa-128">The effective end date of the credential usage.</span></span>
<span data-ttu-id="f86aa-129">Domyślną wartością daty zakończenia jest rok od dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="f86aa-129">The default end date value is one year from today.</span></span>
<span data-ttu-id="f86aa-130">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub przed datą ważności certyfikatu x509.</span><span class="sxs-lookup"><span data-stu-id="f86aa-130">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="f86aa-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f86aa-131">-ObjectId</span></span>
<span data-ttu-id="f86aa-132">Identyfikator obiektu podmiotu usługi, do którego mają zostać dodane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="f86aa-132">The object id of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="f86aa-133">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f86aa-133">-ServicePrincipalName</span></span>
<span data-ttu-id="f86aa-134">Nazwa (SPN) podmiotu usługi, do którego mają zostać dodane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="f86aa-134">The name (SPN) of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="f86aa-135">-Serviceprincipalobject</span><span class="sxs-lookup"><span data-stu-id="f86aa-135">-ServicePrincipalObject</span></span>
<span data-ttu-id="f86aa-136">Obiekt główny usługi, do którego mają zostać dodane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="f86aa-136">The service principal object to add the credentials to.</span></span>

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

### <span data-ttu-id="f86aa-137">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="f86aa-137">-StartDate</span></span>
<span data-ttu-id="f86aa-138">Efektywna Data rozpoczęcia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="f86aa-138">The effective start date of the credential usage.</span></span>
<span data-ttu-id="f86aa-139">Domyślna wartość daty rozpoczęcia przypada dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="f86aa-139">The default start date value is today.</span></span>
<span data-ttu-id="f86aa-140">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub po dniu, od którego certyfikat x509 jest ważny.</span><span class="sxs-lookup"><span data-stu-id="f86aa-140">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="f86aa-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f86aa-141">-Confirm</span></span>
<span data-ttu-id="f86aa-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f86aa-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f86aa-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f86aa-143">-WhatIf</span></span>
<span data-ttu-id="f86aa-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f86aa-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f86aa-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f86aa-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f86aa-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f86aa-146">CommonParameters</span></span>
<span data-ttu-id="f86aa-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f86aa-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f86aa-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f86aa-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f86aa-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f86aa-149">INPUTS</span></span>

### <span data-ttu-id="f86aa-150">System. String</span><span class="sxs-lookup"><span data-stu-id="f86aa-150">System.String</span></span>

### <span data-ttu-id="f86aa-151">Microsoft. Azure. Commands. pozycji. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f86aa-151">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

### <span data-ttu-id="f86aa-152">System. DateTime</span><span class="sxs-lookup"><span data-stu-id="f86aa-152">System.DateTime</span></span>

## <span data-ttu-id="f86aa-153">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f86aa-153">OUTPUTS</span></span>

### <span data-ttu-id="f86aa-154">Microsoft. Azure. Commands. pozycji. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="f86aa-154">Microsoft.Azure.Commands.ActiveDirectory.PSADCredential</span></span>

### <span data-ttu-id="f86aa-155">Microsoft. Azure. Commands. resources. models. Authorization. PSADCredentialWrapper</span><span class="sxs-lookup"><span data-stu-id="f86aa-155">Microsoft.Azure.Commands.Resources.Models.Authorization.PSADCredentialWrapper</span></span>

## <span data-ttu-id="f86aa-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f86aa-156">NOTES</span></span>

## <span data-ttu-id="f86aa-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f86aa-157">RELATED LINKS</span></span>

[<span data-ttu-id="f86aa-158">Get-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="f86aa-158">Get-AzADSpCredential</span></span>](./Get-AzADSpCredential.md)

[<span data-ttu-id="f86aa-159">Remove-AzADSpCredential</span><span class="sxs-lookup"><span data-stu-id="f86aa-159">Remove-AzADSpCredential</span></span>](./Remove-AzADSpCredential.md)

[<span data-ttu-id="f86aa-160">Get-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f86aa-160">Get-AzADServicePrincipal</span></span>](./Get-AzADServicePrincipal.md)



