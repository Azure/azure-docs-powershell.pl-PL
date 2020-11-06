---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 98836BC0-AB4F-4F24-88BE-E7DD350B71E8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADAppCredential.md
ms.openlocfilehash: 15b3e3fd90a7bacf87062bc12269ca2853276370
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93553777"
---
# <span data-ttu-id="cb203-101">New-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="cb203-101">New-AzureRmADAppCredential</span></span>

## <span data-ttu-id="cb203-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cb203-102">SYNOPSIS</span></span>
<span data-ttu-id="cb203-103">Umożliwia dodanie poświadczenia do istniejącej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cb203-103">Adds a credential to an existing application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cb203-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cb203-104">SYNTAX</span></span>

### <span data-ttu-id="cb203-105">ApplicationObjectIdWithPasswordParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="cb203-105">ApplicationObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -Password <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb203-106">ApplicationObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb203-106">ApplicationObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb203-107">ApplicationIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb203-107">ApplicationIdWithCertValueParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cb203-108">ApplicationIdWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="cb203-108">ApplicationIdWithPasswordParameterSet</span></span>
```
New-AzureRmADAppCredential -ApplicationId <String> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cb203-109">Opis</span><span class="sxs-lookup"><span data-stu-id="cb203-109">DESCRIPTION</span></span>
<span data-ttu-id="cb203-110">Za pomocą polecenia cmdlet New-AzureRmADAppCredential można dodać nowe poświadczenia lub wycofać poświadczenia dla aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cb203-110">The New-AzureRmADAppCredential cmdlet can be used to add a new credential or to roll credentials for an application.</span></span>
<span data-ttu-id="cb203-111">Aplikacja jest identyfikowana przez podanie identyfikatora obiektu aplikacji lub identyfikatora aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cb203-111">The application is identified by supplying either the application object id or application Id.</span></span>

## <span data-ttu-id="cb203-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cb203-112">EXAMPLES</span></span>

### <span data-ttu-id="cb203-113">--------------------------Przykład 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="cb203-113">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> New-AzureRmADAppCredential -ObjectId 1f89cf81-0146-4f4e-beae-2007d0668416 -Password P@ssw0rd!
```

<span data-ttu-id="cb203-114">Nowe poświadczenie hasła zostanie dodane do istniejącej aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cb203-114">A new password credential is added to an existing application.</span></span>
<span data-ttu-id="cb203-115">W tym przykładzie podana wartość hasła zostanie dodana do aplikacji przy użyciu identyfikatora obiektu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cb203-115">In this example, the supplied password value is added to the application using the application object id.</span></span>

### <span data-ttu-id="cb203-116">--------------------------Przykład 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="cb203-116">--------------------------  Example 2  --------------------------</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="cb203-117">Do istniejącej aplikacji zostanie dodane nowe poświadczenie klucza.</span><span class="sxs-lookup"><span data-stu-id="cb203-117">A new key credential is added to an existing application.</span></span>
<span data-ttu-id="cb203-118">W tym przykładzie został dodany publiczny certyfikat x509 zakodowany algorytmem Base64 ("MojaApl. cer") do aplikacji przy użyciu aplikacji.</span><span class="sxs-lookup"><span data-stu-id="cb203-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the application using the applicationId.</span></span>

### <span data-ttu-id="cb203-119">--------------------------Przykład 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="cb203-119">--------------------------  Example 3  --------------------------</span></span>
```
PS E:\> New-AzureRmADAppCredential -ApplicationId 4589cd6b-3d79-4bb4-93b8-a0b99f3bfc58 -CertValue $credValue
```

## <span data-ttu-id="cb203-120">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cb203-120">PARAMETERS</span></span>

### <span data-ttu-id="cb203-121">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="cb203-121">-ApplicationId</span></span>
<span data-ttu-id="cb203-122">Identyfikator aplikacji, do której mają zostać dodane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="cb203-122">The id of the application to add the credentials to.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationIdWithCertValueParameterSet, ApplicationIdWithPasswordParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb203-123">-CertValue</span><span class="sxs-lookup"><span data-stu-id="cb203-123">-CertValue</span></span>
<span data-ttu-id="cb203-124">Wartość "asymetrycznego" typu poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="cb203-124">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="cb203-125">Reprezentuje certyfikat zakodowany Base 64.</span><span class="sxs-lookup"><span data-stu-id="cb203-125">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="cb203-126">-EndDate</span><span class="sxs-lookup"><span data-stu-id="cb203-126">-EndDate</span></span>
<span data-ttu-id="cb203-127">Efektywna Data zakończenia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="cb203-127">The effective end date of the credential usage.</span></span>
<span data-ttu-id="cb203-128">Domyślną wartością daty zakończenia jest rok od dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="cb203-128">The default end date value is one year from today.</span></span> <span data-ttu-id="cb203-129">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub przed datą ważności certyfikatu x509.</span><span class="sxs-lookup"><span data-stu-id="cb203-129">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="cb203-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="cb203-130">-ObjectId</span></span>
<span data-ttu-id="cb203-131">Identyfikator obiektu aplikacji, do którego mają zostać dodane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="cb203-131">The object id of the application to add the credentials to.</span></span>

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

### <span data-ttu-id="cb203-132">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="cb203-132">-Password</span></span>
<span data-ttu-id="cb203-133">Hasło, które ma zostać skojarzone z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="cb203-133">The password to be associated with the application.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationObjectIdWithPasswordParameterSet, ApplicationIdWithPasswordParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cb203-134">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="cb203-134">-StartDate</span></span>
<span data-ttu-id="cb203-135">Efektywna Data rozpoczęcia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="cb203-135">The effective start date of the credential usage.</span></span>
<span data-ttu-id="cb203-136">Domyślna wartość daty rozpoczęcia przypada dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="cb203-136">The default start date value is today.</span></span>
<span data-ttu-id="cb203-137">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub po dniu, od którego certyfikat x509 jest ważny.</span><span class="sxs-lookup"><span data-stu-id="cb203-137">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="cb203-138">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cb203-138">-Confirm</span></span>
<span data-ttu-id="cb203-139">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cb203-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cb203-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cb203-140">-WhatIf</span></span>
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

### <span data-ttu-id="cb203-141">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cb203-141">-DefaultProfile</span></span>
<span data-ttu-id="cb203-142">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cb203-142">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cb203-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cb203-143">CommonParameters</span></span>
<span data-ttu-id="cb203-144">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cb203-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cb203-145">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cb203-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cb203-146">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cb203-146">INPUTS</span></span>

## <span data-ttu-id="cb203-147">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cb203-147">OUTPUTS</span></span>

### <span data-ttu-id="cb203-148">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="cb203-148">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="cb203-149">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cb203-149">NOTES</span></span>

## <span data-ttu-id="cb203-150">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cb203-150">RELATED LINKS</span></span>

[<span data-ttu-id="cb203-151">Get-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="cb203-151">Get-AzureRmADAppCredential</span></span>](./Get-AzureRmADAppCredential.md)

[<span data-ttu-id="cb203-152">Remove-AzureRmADAppCredential</span><span class="sxs-lookup"><span data-stu-id="cb203-152">Remove-AzureRmADAppCredential</span></span>](./Remove-AzureRmADAppCredential.md)

[<span data-ttu-id="cb203-153">Get-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="cb203-153">Get-AzureRmADApplication</span></span>](./Get-AzureRmADApplication.md)

