---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: D602F910-B26F-473D-B5B6-C7BDFB0A14CB
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmADServicePrincipal.md
ms.openlocfilehash: 4b327193a8dcbfecae8f13fa234da703d1a93cfb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719254"
---
# <span data-ttu-id="64129-101">New-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="64129-101">New-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="64129-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="64129-102">SYNOPSIS</span></span>
<span data-ttu-id="64129-103">Tworzy nowy podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="64129-103">Creates a new azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64129-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="64129-104">SYNTAX</span></span>

### <span data-ttu-id="64129-105">ApplicationWithoutCredentialParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="64129-105">ApplicationWithoutCredentialParameterSet (Default)</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64129-106">ApplicationWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="64129-106">ApplicationWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64129-107">ApplicationWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="64129-107">ApplicationWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64129-108">ApplicationWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="64129-108">ApplicationWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64129-109">ApplicationWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="64129-109">ApplicationWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId <Guid> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64129-110">DisplayNameWithoutCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="64129-110">DisplayNameWithoutCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64129-111">DisplayNameWithPasswordPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="64129-111">DisplayNameWithPasswordPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -Password <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64129-112">DisplayNameWithPasswordCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="64129-112">DisplayNameWithPasswordCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -PasswordCredentials <PSADPasswordCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64129-113">DisplayNameWithKeyPlainParameterSet</span><span class="sxs-lookup"><span data-stu-id="64129-113">DisplayNameWithKeyPlainParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -CertValue <String> [-StartDate <DateTime>]
 [-EndDate <DateTime>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="64129-114">DisplayNameWithKeyCredentialParameterSet</span><span class="sxs-lookup"><span data-stu-id="64129-114">DisplayNameWithKeyCredentialParameterSet</span></span>
```
New-AzureRmADServicePrincipal -DisplayName <String> -KeyCredentials <PSADKeyCredential[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="64129-115">Opis</span><span class="sxs-lookup"><span data-stu-id="64129-115">DESCRIPTION</span></span>
<span data-ttu-id="64129-116">Tworzy nowy podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="64129-116">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="64129-117">Uwaga: polecenie cmdlet powoduje również niejawne utworzenie aplikacji i ustawienie jej właściwości (Jeśli identyfikator aplikacji nie jest dostarczany).</span><span class="sxs-lookup"><span data-stu-id="64129-117">Note: The cmdlet also implicitly creates an application and sets its properties (if the ApplicationId is not provided).</span></span>
<span data-ttu-id="64129-118">W celu zaktualizowania parametrów specyficznych dla aplikacji użyj polecenia cmdlet Set-AzureRmADApplication.</span><span class="sxs-lookup"><span data-stu-id="64129-118">In order to update the application specific parameters please use Set-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="64129-119">Przykłady</span><span class="sxs-lookup"><span data-stu-id="64129-119">EXAMPLES</span></span>

### <span data-ttu-id="64129-120">--------------------------Przykład 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="64129-120">--------------------------  Example 1  --------------------------</span></span>
```
New-AzureRmADServicePrincipal -ApplicationId 34a28ad2-dec4-4a41-bc3b-d22ddf90000e
```

<span data-ttu-id="64129-121">Tworzy nowy podmiot zabezpieczeń usługi Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="64129-121">Creates a new azure active directory service principal.</span></span>

<span data-ttu-id="64129-122">Identyfikator obiektu typu DisplayName</span><span class="sxs-lookup"><span data-stu-id="64129-122">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="64129-123">DemoApp serviceprincipal f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span><span class="sxs-lookup"><span data-stu-id="64129-123">DemoApp                        ServicePrincipal               f95b6f5c-fc98-4af0-bb8a-34a14ca1dca1</span></span>

### <span data-ttu-id="64129-124">--------------------------Przykład 2--------------------------</span><span class="sxs-lookup"><span data-stu-id="64129-124">--------------------------  Example 2  --------------------------</span></span>
```
New-AzureRmADServicePrincipal -DisplayName SPForNoExistingApp
```

<span data-ttu-id="64129-125">Tworzy nowy podmiot zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="64129-125">Creates a new service principal.</span></span>
<span data-ttu-id="64129-126">Polecenie cmdlet powoduje również niejawne utworzenie aplikacji, ponieważ nie jest ona podana.</span><span class="sxs-lookup"><span data-stu-id="64129-126">The cmdlet also implicitly creates an application since one is not provided.</span></span>

<span data-ttu-id="64129-127">Identyfikator obiektu typu DisplayName</span><span class="sxs-lookup"><span data-stu-id="64129-127">DisplayName                    Type                           ObjectId</span></span>
-----------                    ----                           --------
<span data-ttu-id="64129-128">SPForNoExistingApp serviceprincipal 784136ca-3ae2-4fdd-a388-89d993e7c780</span><span class="sxs-lookup"><span data-stu-id="64129-128">SPForNoExistingApp             ServicePrincipal               784136ca-3ae2-4fdd-a388-89d993e7c780</span></span>

## <span data-ttu-id="64129-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="64129-129">PARAMETERS</span></span>

### <span data-ttu-id="64129-130">-Identyfikator aplikacji</span><span class="sxs-lookup"><span data-stu-id="64129-130">-ApplicationId</span></span>
<span data-ttu-id="64129-131">Unikatowy identyfikator aplikacji dla podmiotu zabezpieczeń usługi w dzierżawie.</span><span class="sxs-lookup"><span data-stu-id="64129-131">The unique application id for a service principal in a tenant.</span></span>
<span data-ttu-id="64129-132">Po utworzeniu tej właściwości nie można jej zmienić.</span><span class="sxs-lookup"><span data-stu-id="64129-132">Once created this property cannot be changed.</span></span>
<span data-ttu-id="64129-133">Jeśli nie podano identyfikatora aplikacji, zostanie on wygenerowany.</span><span class="sxs-lookup"><span data-stu-id="64129-133">If an application id is not specified, one will be generated.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ApplicationWithoutCredentialParameterSet, ApplicationWithPasswordPlainParameterSet, ApplicationWithPasswordCredentialParameterSet, ApplicationWithKeyPlainParameterSet, ApplicationWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64129-134">-CertValue</span><span class="sxs-lookup"><span data-stu-id="64129-134">-CertValue</span></span>
<span data-ttu-id="64129-135">Wartość "asymetrycznego" typu poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="64129-135">The value of the "asymmetric" credential type.</span></span>
<span data-ttu-id="64129-136">Reprezentuje certyfikat zakodowany Base 64.</span><span class="sxs-lookup"><span data-stu-id="64129-136">It represents the base 64 encoded certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithKeyPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64129-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="64129-137">-DisplayName</span></span>
<span data-ttu-id="64129-138">Przyjazna nazwa podmiotu zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="64129-138">The friendly name of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: DisplayNameWithoutCredentialParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithPasswordCredentialParameterSet, DisplayNameWithKeyPlainParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64129-139">-EndDate</span><span class="sxs-lookup"><span data-stu-id="64129-139">-EndDate</span></span>
<span data-ttu-id="64129-140">Efektywna Data zakończenia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="64129-140">The effective end date of the credential usage.</span></span>
<span data-ttu-id="64129-141">Domyślną wartością daty zakończenia jest rok od dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="64129-141">The default end date value is one year from today.</span></span> <span data-ttu-id="64129-142">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub przed datą ważności certyfikatu x509.</span><span class="sxs-lookup"><span data-stu-id="64129-142">For an "asymmetric" type credential, this must be set to on or before the date that the X509 certificate is valid.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64129-143">-Poświadczenia</span><span class="sxs-lookup"><span data-stu-id="64129-143">-KeyCredentials</span></span>
<span data-ttu-id="64129-144">Lista poświadczeń certyfikatu skojarzonych z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="64129-144">The list of certificate credentials associated with the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADKeyCredential[]
Parameter Sets: ApplicationWithKeyCredentialParameterSet, DisplayNameWithKeyCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64129-145">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="64129-145">-Password</span></span>
<span data-ttu-id="64129-146">Hasło, które ma zostać skojarzone z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="64129-146">The password to be associated with the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: ApplicationWithPasswordPlainParameterSet, DisplayNameWithPasswordPlainParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64129-147">-PasswordCredentials</span><span class="sxs-lookup"><span data-stu-id="64129-147">-PasswordCredentials</span></span>
<span data-ttu-id="64129-148">Lista poświadczeń hasła skojarzonych z podmiotem zabezpieczeń usługi.</span><span class="sxs-lookup"><span data-stu-id="64129-148">The list of password credentials associated with the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADPasswordCredential[]
Parameter Sets: ApplicationWithPasswordCredentialParameterSet, DisplayNameWithPasswordCredentialParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64129-149">-DataRozpoczęcia</span><span class="sxs-lookup"><span data-stu-id="64129-149">-StartDate</span></span>
<span data-ttu-id="64129-150">Efektywna Data rozpoczęcia użycia poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="64129-150">The effective start date of the credential usage.</span></span>
<span data-ttu-id="64129-151">Domyślna wartość daty rozpoczęcia przypada dzisiaj.</span><span class="sxs-lookup"><span data-stu-id="64129-151">The default start date value is today.</span></span> <span data-ttu-id="64129-152">W przypadku poświadczenia typu asymetrycznego należy ustawić tę opcję na wartość w dniu lub po dniu, od którego certyfikat x509 jest ważny.</span><span class="sxs-lookup"><span data-stu-id="64129-152">For an "asymmetric" type credential, this must be set to on or after the date that the X509 certificate is valid from.</span></span>

```yaml
Type: System.DateTime
Parameter Sets: ApplicationWithPasswordPlainParameterSet, ApplicationWithKeyPlainParameterSet, DisplayNameWithPasswordPlainParameterSet, DisplayNameWithKeyPlainParameterSet
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64129-153">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="64129-153">-Confirm</span></span>
<span data-ttu-id="64129-154">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="64129-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="64129-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="64129-155">-WhatIf</span></span>
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

### <span data-ttu-id="64129-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64129-156">-DefaultProfile</span></span>
<span data-ttu-id="64129-157">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="64129-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="64129-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64129-158">CommonParameters</span></span>
<span data-ttu-id="64129-159">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64129-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64129-160">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64129-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64129-161">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="64129-161">INPUTS</span></span>

## <span data-ttu-id="64129-162">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="64129-162">OUTPUTS</span></span>

### <span data-ttu-id="64129-163">Microsoft.Azure.Graph.RBAC.Version1_6. pozycji. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="64129-163">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="64129-164">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="64129-164">NOTES</span></span>
<span data-ttu-id="64129-165">Słowa kluczowe: Azure, azurerm, ramię, zasób, zarządzanie, Menedżer, zasób, Grupa, szablon, wdrożenie</span><span class="sxs-lookup"><span data-stu-id="64129-165">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="64129-166">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="64129-166">RELATED LINKS</span></span>

[<span data-ttu-id="64129-167">Remove-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="64129-167">Remove-AzureRmADServicePrincipal</span></span>](./Remove-AzureRmADServicePrincipal.md)

[<span data-ttu-id="64129-168">Get-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="64129-168">Get-AzureRmADServicePrincipal</span></span>](./Get-AzureRmADServicePrincipal.md)

[<span data-ttu-id="64129-169">Nowe — AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="64129-169">New-AzureRmADApplication</span></span>](./New-AzureRmADApplication.md)

[<span data-ttu-id="64129-170">Remove-AzureRmADApplication</span><span class="sxs-lookup"><span data-stu-id="64129-170">Remove-AzureRmADApplication</span></span>](./Remove-AzureRmADApplication.md)

[<span data-ttu-id="64129-171">Get-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="64129-171">Get-AzureRmADSpCredential</span></span>](./Get-AzureRmADSpCredential.md)

[<span data-ttu-id="64129-172">Nowe — AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="64129-172">New-AzureRmADSpCredential</span></span>](./New-AzureRmADSpCredential.md)

[<span data-ttu-id="64129-173">Remove-AzureRmADSpCredential</span><span class="sxs-lookup"><span data-stu-id="64129-173">Remove-AzureRmADSpCredential</span></span>](./Remove-AzureRmADSpCredential.md)

