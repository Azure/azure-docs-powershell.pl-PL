---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppSSLBinding.md
ms.openlocfilehash: 2fff18033febbab23083127628959d2fca9305a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242931"
---
# <span data-ttu-id="06b20-101">New-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="06b20-101">New-AzWebAppSSLBinding</span></span>

## <span data-ttu-id="06b20-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06b20-102">SYNOPSIS</span></span>
<span data-ttu-id="06b20-103">Tworzy powiązanie certyfikatu SSL dla aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="06b20-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

## <span data-ttu-id="06b20-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="06b20-104">SYNTAX</span></span>

### <span data-ttu-id="06b20-105">S1</span><span class="sxs-lookup"><span data-stu-id="06b20-105">S1</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="06b20-106">S2</span><span class="sxs-lookup"><span data-stu-id="06b20-106">S2</span></span>
```
New-AzWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>] [-Name] <String>
 [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06b20-107">S3</span><span class="sxs-lookup"><span data-stu-id="06b20-107">S3</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="06b20-108">S4</span><span class="sxs-lookup"><span data-stu-id="06b20-108">S4</span></span>
```
New-AzWebAppSSLBinding [-WebApp] <PSSite> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="06b20-109">OPIS</span><span class="sxs-lookup"><span data-stu-id="06b20-109">DESCRIPTION</span></span>
<span data-ttu-id="06b20-110">Polecenie **cmdlet New-AzWebAppSSLBinding** tworzy powiązanie certyfikatu SSL (Secure Socket Layer) dla aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="06b20-110">The **New-AzWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="06b20-111">Polecenie cmdlet tworzy powiązanie PROTOKOŁU SSL na dwa sposoby:</span><span class="sxs-lookup"><span data-stu-id="06b20-111">The cmdlet creates an SSL binding in two ways:</span></span> 
- <span data-ttu-id="06b20-112">Aplikację Sieci Web można powiązać z istniejącym certyfikatem.</span><span class="sxs-lookup"><span data-stu-id="06b20-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="06b20-113">Możesz przekazać nowy certyfikat, a następnie powiązać aplikację Web App z tym nowym certyfikatem.</span><span class="sxs-lookup"><span data-stu-id="06b20-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>
<span data-ttu-id="06b20-114">Niezależnie od tego, której metody używasz, certyfikat i aplikacja sieci Web muszą być skojarzone z tą samą grupą zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="06b20-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="06b20-115">Jeśli masz aplikację sieci Web w grupie Zasobów A i chcesz powiązać ten certyfikat z certyfikatem w grupie Zasobów B, jedynym sposobem jest przekazanie kopii certyfikatu do grupy zasobów A. W przypadku przekazywania nowego certyfikatu pamiętaj o następujących wymaganiach dotyczących certyfikatu AZURE SSL:</span><span class="sxs-lookup"><span data-stu-id="06b20-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A. If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 
- <span data-ttu-id="06b20-116">Certyfikat musi zawierać klucz prywatny.</span><span class="sxs-lookup"><span data-stu-id="06b20-116">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="06b20-117">Certyfikat musi mieć format wymiany informacji osobistych (PFX).</span><span class="sxs-lookup"><span data-stu-id="06b20-117">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="06b20-118">Nazwa podmiotu certyfikatu musi być dopasowana do domeny używanej do uzyskiwania dostępu do aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="06b20-118">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="06b20-119">Certyfikat musi korzystać z co najmniej 2048-bitowego szyfrowania.</span><span class="sxs-lookup"><span data-stu-id="06b20-119">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="06b20-120">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="06b20-120">EXAMPLES</span></span>

### <span data-ttu-id="06b20-121">Przykład 1. Powiązanie certyfikatu z aplikacją Web App</span><span class="sxs-lookup"><span data-stu-id="06b20-121">Example 1: Bind a certificate to a Web App</span></span>
```powershell
PS C:\>New-AzWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="06b20-122">To polecenie wiąże istniejący certyfikat platformy Azure (certyfikat z kciukiem E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) z aplikacją sieci Web o nazwie ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="06b20-122">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

### <span data-ttu-id="06b20-123">Przykład 2</span><span class="sxs-lookup"><span data-stu-id="06b20-123">Example 2</span></span>

<span data-ttu-id="06b20-124">Tworzy powiązanie certyfikatu SSL dla aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="06b20-124">Creates an SSL certificate binding for an Azure Web App.</span></span> <span data-ttu-id="06b20-125">(wygenerowane automatycznie)</span><span class="sxs-lookup"><span data-stu-id="06b20-125">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
New-AzWebAppSSLBinding -Name 'www.contoso.com' -ResourceGroupName 'ContosoResourceGroup' -SslState Disabled -Thumbprint 'E3A38EBA60CAA1C162785A2E1C44A15AD450199C3' -WebAppName 'ContosoWebApp'
```

## <span data-ttu-id="06b20-126">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="06b20-126">PARAMETERS</span></span>

### <span data-ttu-id="06b20-127">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="06b20-127">-CertificateFilePath</span></span>
<span data-ttu-id="06b20-128">Określa ścieżkę pliku certyfikatu do przesłania.</span><span class="sxs-lookup"><span data-stu-id="06b20-128">Specifies the file path for the certificate to be uploaded.</span></span>
<span data-ttu-id="06b20-129">Parametr *CertificateFilePath* jest wymagany tylko wtedy, gdy certyfikat nie został jeszcze przekazany do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="06b20-129">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b20-130">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="06b20-130">-CertificatePassword</span></span>
<span data-ttu-id="06b20-131">Określa hasło do odszyfrowywania certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="06b20-131">Specifies the decryption password for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S3
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b20-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06b20-132">-DefaultProfile</span></span>
<span data-ttu-id="06b20-133">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="06b20-133">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06b20-134">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="06b20-134">-Name</span></span>
<span data-ttu-id="06b20-135">Określa nazwę aplikacji Sieci Web.</span><span class="sxs-lookup"><span data-stu-id="06b20-135">Specifies the name of the Web App.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b20-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06b20-136">-ResourceGroupName</span></span>
<span data-ttu-id="06b20-137">Określa nazwę grupy zasobów, do których jest przypisany certyfikat.</span><span class="sxs-lookup"><span data-stu-id="06b20-137">Specifies the name of the resource group that the certificate is assigned to.</span></span>
<span data-ttu-id="06b20-138">W tym samym *poleceniu nie można* użyć parametru ResourceGroupName ani *parametru WebApp.*</span><span class="sxs-lookup"><span data-stu-id="06b20-138">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b20-139">— Slot</span><span class="sxs-lookup"><span data-stu-id="06b20-139">-Slot</span></span>
<span data-ttu-id="06b20-140">Określa nazwę miejsca wdrożenia aplikacji Web App.</span><span class="sxs-lookup"><span data-stu-id="06b20-140">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="06b20-141">Możesz użyć Get-AzWebAppSlot cmdlet, aby uzyskać miejsce.</span><span class="sxs-lookup"><span data-stu-id="06b20-141">You can use the Get-AzWebAppSlot cmdlet to get a slot.</span></span>
<span data-ttu-id="06b20-142">W aplikacjach wdrożeniowych można etapować i weryfikować aplikacje sieci Web bez dostępu do nich przez Internet.</span><span class="sxs-lookup"><span data-stu-id="06b20-142">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="06b20-143">Zazwyczaj zmiany są wdrażane w witrynie tymczasowej, weryfikowane, a następnie wdrażane w witrynie produkcyjnej (dostępnej w Internecie).</span><span class="sxs-lookup"><span data-stu-id="06b20-143">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b20-144">-SslState</span><span class="sxs-lookup"><span data-stu-id="06b20-144">-SslState</span></span>
<span data-ttu-id="06b20-145">Określa, czy certyfikat jest włączony.</span><span class="sxs-lookup"><span data-stu-id="06b20-145">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="06b20-146">Ustaw dla *parametru SSLState* wartość 1, aby włączyć certyfikat, lub ustaw wartość *SSLState* na 0, aby wyłączyć certyfikat.</span><span class="sxs-lookup"><span data-stu-id="06b20-146">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.WebSites.Models.SslState]
Parameter Sets: (All)
Aliases:
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b20-147">- Thumbprint</span><span class="sxs-lookup"><span data-stu-id="06b20-147">-Thumbprint</span></span>
<span data-ttu-id="06b20-148">Określa identyfikator unikatowy certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="06b20-148">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: S2, S4
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b20-149">— WebApp</span><span class="sxs-lookup"><span data-stu-id="06b20-149">-WebApp</span></span>
<span data-ttu-id="06b20-150">Określa aplikację sieci Web.</span><span class="sxs-lookup"><span data-stu-id="06b20-150">Specifies a Web App.</span></span>
<span data-ttu-id="06b20-151">Aby uzyskać aplikację Sieci Web, użyj Get-AzWebApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="06b20-151">To get a Web App, use the Get-AzWebApp cmdlet.</span></span>
<span data-ttu-id="06b20-152">Nie można użyć *parametru WebApp* w tym samym poleceniu co parametr *ResourceGroupName* i/lub *nazwa_sieci Web.*</span><span class="sxs-lookup"><span data-stu-id="06b20-152">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S3, S4
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="06b20-153">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="06b20-153">-WebAppName</span></span>
<span data-ttu-id="06b20-154">Określa nazwę aplikacji sieci Web, dla której jest tworzone nowe powiązanie SSL.</span><span class="sxs-lookup"><span data-stu-id="06b20-154">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>
<span data-ttu-id="06b20-155">W tym samym poleceniu nie można użyć parametru *WebAppName* ani parametru *WebApp.*</span><span class="sxs-lookup"><span data-stu-id="06b20-155">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: System.String
Parameter Sets: S1, S2
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06b20-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06b20-156">CommonParameters</span></span>
<span data-ttu-id="06b20-157">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="06b20-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06b20-158">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06b20-158">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06b20-159">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06b20-159">INPUTS</span></span>

### <span data-ttu-id="06b20-160">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="06b20-160">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="06b20-161">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="06b20-161">OUTPUTS</span></span>

### <span data-ttu-id="06b20-162">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span><span class="sxs-lookup"><span data-stu-id="06b20-162">Microsoft.Azure.Management.WebSites.Models.HostNameSslState</span></span>

## <span data-ttu-id="06b20-163">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="06b20-163">NOTES</span></span>

## <span data-ttu-id="06b20-164">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="06b20-164">RELATED LINKS</span></span>

[<span data-ttu-id="06b20-165">Get-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="06b20-165">Get-AzWebAppSSLBinding</span></span>](./Get-AzWebAppSSLBinding.md)

[<span data-ttu-id="06b20-166">Remove-AzWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="06b20-166">Remove-AzWebAppSSLBinding</span></span>](./Remove-AzWebAppSSLBinding.md)

[<span data-ttu-id="06b20-167">Get-AzWebAppslot</span><span class="sxs-lookup"><span data-stu-id="06b20-167">Get-AzWebAppSlot</span></span>](./Get-AzWebAppSlot.md)

[<span data-ttu-id="06b20-168">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="06b20-168">Get-AzWebApp</span></span>](./Get-AzWebApp.md)


