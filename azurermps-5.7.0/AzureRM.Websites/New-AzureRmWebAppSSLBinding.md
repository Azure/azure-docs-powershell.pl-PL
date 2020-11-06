---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 910239BE-9E48-4DC5-85EA-CC6D466FE62F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappsslbinding
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppSSLBinding.md
ms.openlocfilehash: d3971c2838b3fed04e1aa38d96e2cd27b2e8276e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550440"
---
# <span data-ttu-id="14a0d-101">New-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="14a0d-101">New-AzureRmWebAppSSLBinding</span></span>

## <span data-ttu-id="14a0d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="14a0d-102">SYNOPSIS</span></span>
<span data-ttu-id="14a0d-103">Tworzy powiązanie certyfikatu SSL dla aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="14a0d-103">Creates an SSL certificate binding for an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14a0d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="14a0d-104">SYNTAX</span></span>

### <span data-ttu-id="14a0d-105">S1</span><span class="sxs-lookup"><span data-stu-id="14a0d-105">S1</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-CertificateFilePath] <String> [-CertificatePassword] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="14a0d-106">S2</span><span class="sxs-lookup"><span data-stu-id="14a0d-106">S2</span></span>
```
New-AzureRmWebAppSSLBinding [-ResourceGroupName] <String> [-WebAppName] <String> [[-Slot] <String>]
 [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14a0d-107">S3</span><span class="sxs-lookup"><span data-stu-id="14a0d-107">S3</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>]
 [-CertificateFilePath] <String> [-CertificatePassword] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="14a0d-108">Stanu</span><span class="sxs-lookup"><span data-stu-id="14a0d-108">S4</span></span>
```
New-AzureRmWebAppSSLBinding [-WebApp] <Site> [-Name] <String> [[-SslState] <SslState>] [-Thumbprint] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14a0d-109">Opis</span><span class="sxs-lookup"><span data-stu-id="14a0d-109">DESCRIPTION</span></span>
<span data-ttu-id="14a0d-110">Polecenie cmdlet **New-AzureRmWebAppSSLBinding** tworzy powiązanie certyfikatu SSL (Secure Socket Layer) z aplikacją Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="14a0d-110">The **New-AzureRmWebAppSSLBinding** cmdlet creates a Secure Socket Layer (SSL) certificate binding for an Azure Web App.</span></span>
<span data-ttu-id="14a0d-111">Polecenie cmdlet tworzy powiązanie SSL na dwa sposoby:</span><span class="sxs-lookup"><span data-stu-id="14a0d-111">The cmdlet creates an SSL binding in two ways:</span></span> 

- <span data-ttu-id="14a0d-112">Możesz powiązać aplikację sieci Web z istniejącym certyfikatem.</span><span class="sxs-lookup"><span data-stu-id="14a0d-112">You can bind a Web App to an existing certificate.</span></span>
- <span data-ttu-id="14a0d-113">Możesz przekazać nowy certyfikat, a następnie powiązać aplikację internetową z tym nowym certyfikatem.</span><span class="sxs-lookup"><span data-stu-id="14a0d-113">You can upload a new certificate and then bind the Web App to this new certificate.</span></span>

<span data-ttu-id="14a0d-114">Niezależnie od tego, która metoda jest używana, certyfikat i aplikacja sieci Web muszą być skojarzone z tą samą grupą zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="14a0d-114">Regardless of which approach you use, the certificate and the Web App must be associated with the same Azure resource group.</span></span>
<span data-ttu-id="14a0d-115">Jeśli masz aplikację sieci Web w grupie zasobów A i chcesz powiązać tę aplikację sieci Web z certyfikatem w grupie zasobów B, jedynym sposobem na przekazanie kopii certyfikatu do grupy zasobów A.</span><span class="sxs-lookup"><span data-stu-id="14a0d-115">If you have a Web App in Resource Group A and you want to bind that Web App to a certificate in Resource Group B, the only way to do that is to upload a copy of the certificate to Resource Group A.</span></span>

<span data-ttu-id="14a0d-116">Jeśli przekazujesz nowy certyfikat, pamiętaj o następujących wymaganiach dotyczących certyfikatu SSL usługi Azure:</span><span class="sxs-lookup"><span data-stu-id="14a0d-116">If you upload a new certificate, keep in mind the following requirements for an Azure SSL certificate:</span></span> 

- <span data-ttu-id="14a0d-117">Certyfikat musi zawierać klucz prywatny.</span><span class="sxs-lookup"><span data-stu-id="14a0d-117">The certificate must contain a private key.</span></span> 
- <span data-ttu-id="14a0d-118">Certyfikat musi korzystać z formatu Personal Information Exchange (PFX).</span><span class="sxs-lookup"><span data-stu-id="14a0d-118">The certificate must use the Personal Information Exchange (PFX) format.</span></span> 
- <span data-ttu-id="14a0d-119">Nazwa podmiotu certyfikatu musi odpowiadać domenie używanej do uzyskiwania dostępu do aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="14a0d-119">The certificate's subject name must match the domain used to access the Web App.</span></span> 
- <span data-ttu-id="14a0d-120">Certyfikat musi zawierać co najmniej 2048-bitowe szyfrowanie.</span><span class="sxs-lookup"><span data-stu-id="14a0d-120">The certificate must use a minimum of 2048-bit encryption.</span></span>

## <span data-ttu-id="14a0d-121">Przykłady</span><span class="sxs-lookup"><span data-stu-id="14a0d-121">EXAMPLES</span></span>

### <span data-ttu-id="14a0d-122">Przykład 1: powiązanie certyfikatu z aplikacją sieci Web</span><span class="sxs-lookup"><span data-stu-id="14a0d-122">Example 1: Bind a certificate to a Web App</span></span>
```
PS C:\>New-AzureRmWebAppSSLBinding -ResourceGroupName "ContosoResourceGroup" -WebAppName "ContosoWebApp" -Thumbprint "E3A38EBA60CAA1C162785A2E1C44A15AD450199C3" -Name "www.contoso.com"
```

<span data-ttu-id="14a0d-123">To polecenie wiąże istniejący certyfikat platformy Azure (certyfikat z E3A38EBA60CAA1C162785A2E1C44A15AD450199C3em odcisku palca) aplikacji internetowej o nazwie ContosoWebApp.</span><span class="sxs-lookup"><span data-stu-id="14a0d-123">This command binds an existing Azure certificate (a certificate with the Thumbprint E3A38EBA60CAA1C162785A2E1C44A15AD450199C3) to the web app named ContosoWebApp.</span></span>

## <span data-ttu-id="14a0d-124">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="14a0d-124">PARAMETERS</span></span>

### <span data-ttu-id="14a0d-125">-CertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="14a0d-125">-CertificateFilePath</span></span>
<span data-ttu-id="14a0d-126">Określa ścieżkę pliku dla certyfikatu, który ma zostać przekazany.</span><span class="sxs-lookup"><span data-stu-id="14a0d-126">Specifies the file path for the certificate to be uploaded.</span></span>

<span data-ttu-id="14a0d-127">Parametr *CertificateFilePath* jest wymagany tylko wtedy, gdy certyfikat nie został jeszcze przekazany na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="14a0d-127">The *CertificateFilePath* parameter is only required if the certificate has not yet been uploaded to Azure.</span></span>

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a0d-128">-CertificatePassword</span><span class="sxs-lookup"><span data-stu-id="14a0d-128">-CertificatePassword</span></span>
<span data-ttu-id="14a0d-129">Określa hasło odszyfrowywania dla certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="14a0d-129">Specifies the decryption password for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: S1, S3
Aliases: 

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a0d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14a0d-130">-DefaultProfile</span></span>
<span data-ttu-id="14a0d-131">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="14a0d-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14a0d-132">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="14a0d-132">-Name</span></span>
<span data-ttu-id="14a0d-133">Określa nazwę aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="14a0d-133">Specifies the name of the Web App.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a0d-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="14a0d-134">-ResourceGroupName</span></span>
<span data-ttu-id="14a0d-135">Określa nazwę grupy zasobów, do której przypisano certyfikat.</span><span class="sxs-lookup"><span data-stu-id="14a0d-135">Specifies the name of the resource group that the certificate is assigned to.</span></span>

<span data-ttu-id="14a0d-136">Nie można użyć parametru *ResourceGroupName* i parametru *aplikacji* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="14a0d-136">You cannot use the *ResourceGroupName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a0d-137">-Slot</span><span class="sxs-lookup"><span data-stu-id="14a0d-137">-Slot</span></span>
<span data-ttu-id="14a0d-138">Określa nazwę miejsca wdrożenia aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="14a0d-138">Specifies the name of the Web App deployment slot.</span></span>
<span data-ttu-id="14a0d-139">Możesz użyć polecenia cmdlet Get-AzureRMWebAppSlot, aby uzyskać gniazdo.</span><span class="sxs-lookup"><span data-stu-id="14a0d-139">You can use the Get-AzureRMWebAppSlot cmdlet to get a slot.</span></span>

<span data-ttu-id="14a0d-140">Miejsca do wdrożenia umożliwiają przemieszczanie i sprawdzanie aplikacji sieci Web bez możliwości dostępu do aplikacji internetowych.</span><span class="sxs-lookup"><span data-stu-id="14a0d-140">Deployment slots provide a way for you to stage and validate web apps without those apps being accessible over the Internet.</span></span>
<span data-ttu-id="14a0d-141">Zazwyczaj zmiany zostaną wdrożone w witrynie etapowej, poprawność tych zmian, a następnie wdrożone w witrynie produkcja (z ułatwieniami dostępu do Internetu).</span><span class="sxs-lookup"><span data-stu-id="14a0d-141">Typically you will deploy your changes to a staging site, validate those changes, and then deploy to the production (Internet-accessible) site.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a0d-142">-SslState</span><span class="sxs-lookup"><span data-stu-id="14a0d-142">-SslState</span></span>
<span data-ttu-id="14a0d-143">Określa, czy certyfikat jest włączony.</span><span class="sxs-lookup"><span data-stu-id="14a0d-143">Specifies whether the certificate is enabled.</span></span>
<span data-ttu-id="14a0d-144">Ustaw parametr *SSLState* na wartość 1, aby włączyć certyfikat, lub ustaw dla *SSLState* wartość 0, aby wyłączyć certyfikat.</span><span class="sxs-lookup"><span data-stu-id="14a0d-144">Set the *SSLState* parameter to 1 to enable the certificate, or set *SSLState* to 0 to disable the certificate.</span></span>

```yaml
Type: SslState
Parameter Sets: (All)
Aliases: 
Accepted values: Disabled, SniEnabled, IpBasedEnabled

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a0d-145">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="14a0d-145">-Thumbprint</span></span>
<span data-ttu-id="14a0d-146">Określa unikatowy identyfikator certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="14a0d-146">Specifies the unique identifier for the certificate.</span></span>

```yaml
Type: String
Parameter Sets: S2, S4
Aliases: 

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a0d-147">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="14a0d-147">-WebApp</span></span>
<span data-ttu-id="14a0d-148">Określa aplikację sieci Web.</span><span class="sxs-lookup"><span data-stu-id="14a0d-148">Specifies a Web App.</span></span>
<span data-ttu-id="14a0d-149">Aby uzyskać aplikację sieci Web, użyj polecenia cmdlet Get-AzureRmWebApp.</span><span class="sxs-lookup"><span data-stu-id="14a0d-149">To get a Web App, use the Get-AzureRmWebApp cmdlet.</span></span>

<span data-ttu-id="14a0d-150">Parametru *aplikacji* nie można używać w tym samym poleceniu, co parametr *ResourceGroupName* i/lub *WebAppName*.</span><span class="sxs-lookup"><span data-stu-id="14a0d-150">You cannot use the *WebApp* parameter in the same command as the *ResourceGroupName* parameter and/or the *WebAppName*.</span></span>

```yaml
Type: Site
Parameter Sets: S3, S4
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="14a0d-151">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="14a0d-151">-WebAppName</span></span>
<span data-ttu-id="14a0d-152">Określa nazwę aplikacji sieci Web, dla której jest tworzone nowe powiązanie SSL.</span><span class="sxs-lookup"><span data-stu-id="14a0d-152">Specifies the name of the Web App for which the new SSL binding is being created.</span></span>

<span data-ttu-id="14a0d-153">Nie można użyć parametru *WebAppName* i parametru *aplikacji* w tym samym poleceniu.</span><span class="sxs-lookup"><span data-stu-id="14a0d-153">You cannot use the *WebAppName* parameter and the *WebApp* parameter in the same command.</span></span>

```yaml
Type: String
Parameter Sets: S1, S2
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14a0d-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14a0d-154">CommonParameters</span></span>
<span data-ttu-id="14a0d-155">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="14a0d-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14a0d-156">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14a0d-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14a0d-157">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="14a0d-157">INPUTS</span></span>

### <span data-ttu-id="14a0d-158">Klienta</span><span class="sxs-lookup"><span data-stu-id="14a0d-158">Site</span></span>
<span data-ttu-id="14a0d-159">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="14a0d-159">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="14a0d-160">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="14a0d-160">OUTPUTS</span></span>

## <span data-ttu-id="14a0d-161">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="14a0d-161">NOTES</span></span>

## <span data-ttu-id="14a0d-162">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="14a0d-162">RELATED LINKS</span></span>

[<span data-ttu-id="14a0d-163">Get-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="14a0d-163">Get-AzureRmWebAppSSLBinding</span></span>](./Get-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="14a0d-164">Remove-AzureRmWebAppSSLBinding</span><span class="sxs-lookup"><span data-stu-id="14a0d-164">Remove-AzureRmWebAppSSLBinding</span></span>](./Remove-AzureRmWebAppSSLBinding.md)

[<span data-ttu-id="14a0d-165">Get-AzureRMWebAppSlot</span><span class="sxs-lookup"><span data-stu-id="14a0d-165">Get-AzureRMWebAppSlot</span></span>](./Get-AzureRMWebAppSlot.md)

[<span data-ttu-id="14a0d-166">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="14a0d-166">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)


