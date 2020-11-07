---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 063BAA79-484D-48CF-9170-3808813752BD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADSpCredential.md
ms.openlocfilehash: 814da56d9b925e19deac81dad886604d562e05e9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719252"
---
# <span data-ttu-id="5969f-101">New-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5969f-101">New-AzureRmADSpCredential</span></span>

## <span data-ttu-id="5969f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5969f-102">SYNOPSIS</span></span>
<span data-ttu-id="5969f-103">Umożliwia dodanie poświadczenia do istniejącego podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="5969f-103">Adds a credential to an existing service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5969f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5969f-104">SYNTAX</span></span>

### <span data-ttu-id="5969f-105">SpObjectIdWithPasswordParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="5969f-105">SpObjectIdWithPasswordParameterSet (Default)</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -Password <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5969f-106">SpObjectIdWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="5969f-106">SpObjectIdWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ObjectId <String> -CertValue <String> [-StartDate <DateTime>] [-EndDate <DateTime>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5969f-107">SPNWithCertValueParameterSet</span><span class="sxs-lookup"><span data-stu-id="5969f-107">SPNWithCertValueParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5969f-108">SPNWithPasswordParameterSet</span><span class="sxs-lookup"><span data-stu-id="5969f-108">SPNWithPasswordParameterSet</span></span>
```
New-AzureRmADSpCredential -ServicePrincipalName <String> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5969f-109">Opis</span><span class="sxs-lookup"><span data-stu-id="5969f-109">DESCRIPTION</span></span>
<span data-ttu-id="5969f-110">Za pomocą polecenia cmdlet New-AzureRmADSpCredential można dodać nowe poświadczenia lub wycofać poświadczenia dla podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="5969f-110">The New-AzureRmADSpCredential cmdlet can be used to add a new credential or to roll credentials for a service principal.</span></span>
<span data-ttu-id="5969f-111">Wartość główna usługi jest identyfikowana przez podanie identyfikatora obiektu lub nazwy głównej usługi.</span><span class="sxs-lookup"><span data-stu-id="5969f-111">The service principal is identified by supplying either the object id or service principal name.</span></span>

## <span data-ttu-id="5969f-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5969f-112">EXAMPLES</span></span>

### <span data-ttu-id="5969f-113">--------------------------Przykład 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5969f-113">--------------------------  Example 1  --------------------------</span></span>
```
PS E:\> New-AzureRmADSpCredential -ObjectId 1f99cf81-0146-4f4e-beae-2007d0668476 -Password "P@ssw0rd!"
```

<span data-ttu-id="5969f-114">Nowe poświadczenie hasła zostanie dodane do istniejącego podmiotu usługi.</span><span class="sxs-lookup"><span data-stu-id="5969f-114">A new password credential is added to an existing service principal.</span></span>
<span data-ttu-id="5969f-115">W tym przykładzie podana wartość hasła jest dodawana do podmiotu zabezpieczeń usługi przy użyciu obiektu objectId.</span><span class="sxs-lookup"><span data-stu-id="5969f-115">In this example, the supplied password value is added to the service principal using the objectId.</span></span>

### <span data-ttu-id="5969f-116">--------------------------Przykład 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="5969f-116">--------------------------  Example 2  --------------------------</span></span>
```
$cer = New-Object System.Security.Cryptography.X509Certificates.X509Certificate 

$cer.Import("C:\myapp.cer") 

$binCert = $cer.GetRawCertData() 

$credValue = [System.Convert]::ToBase64String($binCert)

PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue -StartDate $cer.GetEffectiveDateString() -EndDate $cer.GetExpirationDateString()
```

<span data-ttu-id="5969f-117">Do istniejącego podmiotu usługi jest dodawane nowe poświadczenie klucza.</span><span class="sxs-lookup"><span data-stu-id="5969f-117">A new key credential is added to an existing service principal.</span></span>
<span data-ttu-id="5969f-118">W tym przykładzie certyfikat certyfikatu x509 zakodowany w formacie base64 ("MojaApl. cer") jest dodawany do podmiotu zabezpieczeń usługi przy użyciu jego nazwy SPN.</span><span class="sxs-lookup"><span data-stu-id="5969f-118">In this example, the supplied base64 encoded public X509 certificate ("myapp.cer") is added to the service principal using its SPN.</span></span>

### <span data-ttu-id="5969f-119">--------------------------Przykład 3--------------------------</span><span class="sxs-lookup"><span data-stu-id="5969f-119">--------------------------  Example 3  --------------------------</span></span>
<span data-ttu-id="5969f-120">@ {Paragraph = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="5969f-120">@{paragraph=PS C:\\\>}</span></span>







```
PS E:\> New-AzureRmADSpCredential -ServicePrincipalName "http://test123" -CertValue $credValue
```

## <span data-ttu-id="5969f-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5969f-121">PARAMETERS</span></span>

### <span data-ttu-id="5969f-122">-CertValue</span><span class="sxs-lookup"><span data-stu-id="5969f-122">-CertValue</span></span>
<span data-ttu-id="5969f-123">Wartość "asymetrycznego" typu poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="5969f-123">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="5969f-124">Reprezentuje certyfikat zakodowany Base 64.</span><span class="sxs-lookup"><span data-stu-id="5969f-124">It represents the base 64 encoded certificate.</span></span>

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

### <span data-ttu-id="5969f-125">-EndDate</span><span class="sxs-lookup"><span data-stu-id="5969f-125">-EndDate</span></span>
<span data-ttu-id="5969f-126">Efektywna Data zakończenia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="5969f-126">The effective end date of the credential usage.</span></span>
<span data-ttu-id="5969f-127">Domyślną wartością daty zakończenia jest rok od dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="5969f-127">The default end date value is one year from today.</span></span> <span data-ttu-id="5969f-128">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub przed datą ważności certyfikatu x509.</span><span class="sxs-lookup"><span data-stu-id="5969f-128">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

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

### <span data-ttu-id="5969f-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="5969f-129">-ObjectId</span></span>
<span data-ttu-id="5969f-130">Identyfikator obiektu podmiotu usługi, do którego mają zostać dodane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="5969f-130">The object id of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="5969f-131">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="5969f-131">-Password</span></span>
<span data-ttu-id="5969f-132">Hasło, które ma zostać skojarzone z aplikacją.</span><span class="sxs-lookup"><span data-stu-id="5969f-132">The password to be associated with the application.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithPasswordParameterSet, SPNWithPasswordParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5969f-133">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="5969f-133">-ServicePrincipalName</span></span>
<span data-ttu-id="5969f-134">Nazwa (SPN) podmiotu usługi, do którego mają zostać dodane poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="5969f-134">The name (SPN) of the service principal to add the credentials to.</span></span>

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

### <span data-ttu-id="5969f-135">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="5969f-135">-StartDate</span></span>
<span data-ttu-id="5969f-136">Efektywna Data rozpoczęcia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="5969f-136">The effective start date of the credential usage.</span></span>
<span data-ttu-id="5969f-137">Domyślna wartość daty rozpoczęcia przypada dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="5969f-137">The default start date value is today.</span></span> <span data-ttu-id="5969f-138">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub po dniu, od którego certyfikat x509 jest ważny.</span><span class="sxs-lookup"><span data-stu-id="5969f-138">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

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

### <span data-ttu-id="5969f-139">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5969f-139">-Confirm</span></span>
<span data-ttu-id="5969f-140">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5969f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5969f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5969f-141">-WhatIf</span></span>
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

### <span data-ttu-id="5969f-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5969f-142">-DefaultProfile</span></span>
<span data-ttu-id="5969f-143">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="5969f-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5969f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5969f-144">CommonParameters</span></span>
<span data-ttu-id="5969f-145">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5969f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5969f-146">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5969f-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5969f-147">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5969f-147">INPUTS</span></span>

## <span data-ttu-id="5969f-148">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5969f-148">OUTPUTS</span></span>

### <span data-ttu-id="5969f-149">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADCredential</span><span class="sxs-lookup"><span data-stu-id="5969f-149">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADCredential</span></span>

## <span data-ttu-id="5969f-150">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5969f-150">NOTES</span></span>

## <span data-ttu-id="5969f-151">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5969f-151">RELATED LINKS</span></span>

[<span data-ttu-id="5969f-152">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5969f-152">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="5969f-153">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="5969f-153">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

[<span data-ttu-id="5969f-154">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="5969f-154">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)



