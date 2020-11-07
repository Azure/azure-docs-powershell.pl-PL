---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermadappcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
ms.openlocfilehash: d4d7cb0a188b4c00c4ea0c07140b3360c98805aa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717698"
---
# <span data-ttu-id="30208-101">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="30208-101">New-AzureRmADAppCredential</span></span>

## <span data-ttu-id="30208-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30208-102">SYNOPSIS</span></span>
<span data-ttu-id="30208-103">Umożliwia dodanie poświadczenia do istniejącej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="30208-103">Adds a credential to an existing application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30208-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30208-104">SYNTAX</span></span>

### <span data-ttu-id="30208-105">ApplicationObjectIdWithPasswordParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="30208-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30208-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="30208-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30208-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="30208-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="30208-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="30208-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -Password <SecureString> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="30208-109">Opis</span><span class="sxs-lookup"><span data-stu-id="30208-109">DESCRIPTION</span></span>
<span data-ttu-id="30208-110">Za pomocą polecenia cmdlet New-AzureRmADAppCredential można dodać nowe poświadczenia lub wycofać poświadczenia dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="30208-110">The New-AzureRmADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="30208-111">Aplikacja jest identyfikowana przez podanie identyfikatora obiektu aplikacji lub identyfikatora aplikacji.</span><span class="sxs-lookup"><span data-stu-id="30208-111">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="30208-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30208-112">EXAMPLES</span></span>

### <span data-ttu-id="30208-113">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="30208-113">Example 1</span></span>
```
PS E:\> $SecureStringPassword = ConvertTo-SecureString -String "password" -AsPlainText -Force
PS E:\> New-AzureRmADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password $SecureStringPassword
```

<span data-ttu-id="30208-114">Nowe poświadczenie hasła zostanie dodane do istniejącej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="30208-114">A new password credential is added to an existing application.</span></span>
<span data-ttu-id="30208-115">W tym przykładzie podana wartość hasła zostanie dodana do aplikacji przy użyciu identyfikatora obiektu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="30208-115">In this example, the supplied password value is added to the application using the application object id.</span></span>

### <span data-ttu-id="30208-116">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="30208-116">Example 2</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="30208-117">Do istniejącej aplikacji zostanie dodane nowe poświadczenie klucza.</span><span class="sxs-lookup"><span data-stu-id="30208-117">A new key credential is added to an existing application.</span></span>
<span data-ttu-id="30208-118">W tym przykładzie został dodany publiczny certyfikat x509 zakodowany algorytmem Base64 ("MojaApl. cer") do aplikacji przy użyciu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="30208-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the application using the applicationId.</span></span>

### <span data-ttu-id="30208-119">Przykład 3</span><span class="sxs-lookup"><span data-stu-id="30208-119">Example 3</span></span>
```
PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue
```

## <span data-ttu-id="30208-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30208-120">PARAMETERS</span></span>

### <span data-ttu-id="30208-121">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="30208-121">-ApplicationId</span></span>
<span data-ttu-id="30208-122">Identyfikator aplikacji, do której mają zostać dodane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="30208-122">The id of the application to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30208-123">-CertValue</span><span class="sxs-lookup"><span data-stu-id="30208-123">-CertValue</span></span>
<span data-ttu-id="30208-124">Wartość "asymetrycznego" typu poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="30208-124">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="30208-125">Reprezentuje certyfikat zakodowany Base 64.</span><span class="sxs-lookup"><span data-stu-id="30208-125">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithCertValueParameterSet, ApplicationIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30208-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30208-126">-DefaultProfile</span></span>
<span data-ttu-id="30208-127">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="30208-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30208-128">-EndDate</span><span class="sxs-lookup"><span data-stu-id="30208-128">-EndDate</span></span>
<span data-ttu-id="30208-129">Efektywna Data zakończenia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="30208-129">The effective end date of the credential usage.</span></span>
<span data-ttu-id="30208-130">Domyślną wartością daty zakończenia jest rok od dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="30208-130">The default end date value is one year from today.</span></span> <span data-ttu-id="30208-131">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub przed datą ważności certyfikatu x509.</span><span class="sxs-lookup"><span data-stu-id="30208-131">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30208-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="30208-132">-ObjectId</span></span>
<span data-ttu-id="30208-133">Identyfikator obiektu aplikacji, do którego mają zostać dodane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="30208-133">The object id of the application to add the credentials to.</span></span>

```yaml
Type: String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationObjectIdWithCertValueParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30208-134">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="30208-134">-Password</span></span>
<span data-ttu-id="30208-135">Hasło, które ma zostać skojarzone z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="30208-135">The password to be associated with the application.</span></span>

```yaml
Type: SecureString
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30208-136">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="30208-136">-StartDate</span></span>
<span data-ttu-id="30208-137">Efektywna Data rozpoczęcia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="30208-137">The effective start date of the credential usage.</span></span>
<span data-ttu-id="30208-138">Domyślna wartość daty rozpoczęcia przypada dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="30208-138">The default start date value is today.</span></span>
<span data-ttu-id="30208-139">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub po dniu, od którego certyfikat x509 jest ważny.</span><span class="sxs-lookup"><span data-stu-id="30208-139">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: DateTime
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="30208-140">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="30208-140">-Confirm</span></span>
<span data-ttu-id="30208-141">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30208-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30208-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30208-142">-WhatIf</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30208-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30208-143">CommonParameters</span></span>
<span data-ttu-id="30208-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30208-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30208-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30208-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30208-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30208-146">INPUTS</span></span>

### <span data-ttu-id="30208-147">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="30208-147">None</span></span>
<span data-ttu-id="30208-148">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="30208-148">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="30208-149">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30208-149">OUTPUTS</span></span>

### <span data-ttu-id="30208-150">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="30208-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="30208-151">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30208-151">NOTES</span></span>

## <span data-ttu-id="30208-152">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30208-152">RELATED LINKS</span></span>

[<span data-ttu-id="30208-153">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="30208-153">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="30208-154">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="30208-154">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="30208-155">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="30208-155">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

