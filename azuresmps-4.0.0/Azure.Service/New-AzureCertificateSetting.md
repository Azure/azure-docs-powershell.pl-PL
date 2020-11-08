---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 11919623-9EDF-42A3-93FE-54E93D76D3D0
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7492dbdea0f924e364ac1acf5ce30476e34782d6
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054898"
---
# <span data-ttu-id="15443-101">New-AzureCertificateSetting</span><span class="sxs-lookup"><span data-stu-id="15443-101">New-AzureCertificateSetting</span></span>

## <span data-ttu-id="15443-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="15443-102">SYNOPSIS</span></span>
<span data-ttu-id="15443-103">Tworzy obiekt ustawienia certyfikatu dla certyfikatu w usłudze.</span><span class="sxs-lookup"><span data-stu-id="15443-103">Creates a certificate setting object for a certificate is in a service.</span></span>

## <span data-ttu-id="15443-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="15443-104">SYNTAX</span></span>

```
New-AzureCertificateSetting [[-StoreName] <String>] [-Thumbprint] <String>
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="15443-105">Opis</span><span class="sxs-lookup"><span data-stu-id="15443-105">DESCRIPTION</span></span>
<span data-ttu-id="15443-106">Polecenie cmdlet **New-AzureCertificateSetting** tworzy obiekt ustawienia certyfikatu dla certyfikatu, który znajduje się w usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="15443-106">The **New-AzureCertificateSetting** cmdlet creates a certificate setting object for a certificate that is in an Azure service.</span></span>

<span data-ttu-id="15443-107">Za pomocą obiektu Ustawienia certyfikatu można utworzyć obiekt konfiguracji przy użyciu polecenia cmdlet **Add-AzureProvisioningConfig** .</span><span class="sxs-lookup"><span data-stu-id="15443-107">You can use a certificate setting object to create a configuration object by using the **Add-AzureProvisioningConfig** cmdlet.</span></span>
<span data-ttu-id="15443-108">Użyj obiektu konfiguracji do utworzenia maszyny wirtualnej za pomocą polecenia cmdlet **New-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="15443-108">Use a configuration object to create virtual machine by using the **New-AzureVM** cmdlet.</span></span>
<span data-ttu-id="15443-109">Za pomocą obiektu Ustawienia certyfikatu można utworzyć maszynę wirtualną przy użyciu polecenia cmdlet **New-AzureQuickVM** .</span><span class="sxs-lookup"><span data-stu-id="15443-109">You can use a certificate setting object to create a virtual machine by using the **New-AzureQuickVM** cmdlet.</span></span>

## <span data-ttu-id="15443-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="15443-110">EXAMPLES</span></span>

### <span data-ttu-id="15443-111">Przykład 1: Tworzenie obiektu Ustawienia certyfikatu</span><span class="sxs-lookup"><span data-stu-id="15443-111">Example 1: Create a certificate setting object</span></span>
```
PS C:\> New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My"
```

<span data-ttu-id="15443-112">To polecenie tworzy obiekt ustawienia certyfikatu dla istniejącego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="15443-112">This command creates a certificate setting object for an existing certificate.</span></span>

### <span data-ttu-id="15443-113">Przykład 2: Tworzenie maszyny wirtualnej używającej obiektu ustawień konfiguracji</span><span class="sxs-lookup"><span data-stu-id="15443-113">Example 2: Create a virtual machine that uses a configuration setting object</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "ContosoService" -CertToDeploy "C:\temp\ContosoCert.cer"
PS C:\> $CertificateSetting = New-AzureCertificateSetting -Thumbprint "D7BECD4D63EBAF86023BB41FA5FBF5C2C924902A" -StoreName "My" 
PS C:\> $Image = Get-AzureVMImage -ImageName "ContosoStandard"
PS C:\> New-AzureVMConfig -Name "VirtualMachine17" -InstanceSize Small -ImageName $Image | Add-AzureProvisioningConfig -Windows -Certificates $CertificateSetting -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="15443-114">Pierwsze polecenie dodaje certyfikat ContosoCert. cer do usługi o nazwie ContosoService przy użyciu polecenia cmdlet **Add-AzureCertificate** .</span><span class="sxs-lookup"><span data-stu-id="15443-114">The first command adds the certificate ContosoCert.cer to the service named ContosoService by using the **Add-AzureCertificate** cmdlet.</span></span>

<span data-ttu-id="15443-115">Drugie polecenie tworzy obiekt ustawienia certyfikatu, a następnie zapisuje go w zmiennej $CertificateSetting.</span><span class="sxs-lookup"><span data-stu-id="15443-115">The second command creates a certificate setting object, and then stores it in the $CertificateSetting variable.</span></span>

<span data-ttu-id="15443-116">Trzecie polecenie pobiera obraz z repozytorium obrazów przy użyciu polecenia cmdlet **Get-AzureVMImage** .</span><span class="sxs-lookup"><span data-stu-id="15443-116">The third command gets an image from the image repository by using the **Get-AzureVMImage** cmdlet.</span></span>
<span data-ttu-id="15443-117">To polecenie zapisuje obraz w zmiennej $Image.</span><span class="sxs-lookup"><span data-stu-id="15443-117">This command store the image in the $Image variable.</span></span>

<span data-ttu-id="15443-118">Ostatnie polecenie tworzy obiekt konfiguracji maszyny wirtualnej na podstawie obrazu w $Image przy użyciu polecenia cmdlet **New-AzureVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="15443-118">The final command creates a virtual machine configuration object based on the image in $Image by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="15443-119">Polecenie przekazuje ten obiekt do polecenia cmdlet **Add-AzureProvisioningConfig** przy użyciu operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="15443-119">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="15443-120">Polecenie cmdlet umożliwia dodanie informacji o aprowizacji do konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="15443-120">That cmdlet add provisioning information to the configuration.</span></span>
<span data-ttu-id="15443-121">Polecenie przekazuje obiekt do polecenia cmdlet **New-AzureVM** , które powoduje utworzenie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="15443-121">The command passes the object to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

## <span data-ttu-id="15443-122">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="15443-122">PARAMETERS</span></span>

### <span data-ttu-id="15443-123">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="15443-123">-InformationAction</span></span>
<span data-ttu-id="15443-124">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="15443-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="15443-125">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="15443-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="15443-126">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="15443-126">Continue</span></span>
- <span data-ttu-id="15443-127">Ignorować</span><span class="sxs-lookup"><span data-stu-id="15443-127">Ignore</span></span>
- <span data-ttu-id="15443-128">Inquire</span><span class="sxs-lookup"><span data-stu-id="15443-128">Inquire</span></span>
- <span data-ttu-id="15443-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="15443-129">SilentlyContinue</span></span>
- <span data-ttu-id="15443-130">Przestaw</span><span class="sxs-lookup"><span data-stu-id="15443-130">Stop</span></span>
- <span data-ttu-id="15443-131">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="15443-131">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15443-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="15443-132">-InformationVariable</span></span>
<span data-ttu-id="15443-133">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="15443-133">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15443-134">-Pole NazwaSklepu</span><span class="sxs-lookup"><span data-stu-id="15443-134">-StoreName</span></span>
<span data-ttu-id="15443-135">Określa magazyn certyfikatów, w którym ma zostać umieszczony certyfikat.</span><span class="sxs-lookup"><span data-stu-id="15443-135">Specifies the certificate store in which to put the certificate.</span></span>
<span data-ttu-id="15443-136">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="15443-136">Valid values are:</span></span> 

- <span data-ttu-id="15443-137">Adresowej</span><span class="sxs-lookup"><span data-stu-id="15443-137">AddressBook</span></span>
- <span data-ttu-id="15443-138">AuthRoot</span><span class="sxs-lookup"><span data-stu-id="15443-138">AuthRoot</span></span>
- <span data-ttu-id="15443-139">CertificateAuthority</span><span class="sxs-lookup"><span data-stu-id="15443-139">CertificateAuthority</span></span>
- <span data-ttu-id="15443-140">— Zabronione</span><span class="sxs-lookup"><span data-stu-id="15443-140">Disallowed</span></span>
- <span data-ttu-id="15443-141">MOJE</span><span class="sxs-lookup"><span data-stu-id="15443-141">My</span></span>
- <span data-ttu-id="15443-142">Poziomie głównym</span><span class="sxs-lookup"><span data-stu-id="15443-142">Root</span></span>
- <span data-ttu-id="15443-143">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="15443-143">TrustedPeople</span></span>
- <span data-ttu-id="15443-144">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="15443-144">TrustedPublisher</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15443-145">-Odcisk palca</span><span class="sxs-lookup"><span data-stu-id="15443-145">-Thumbprint</span></span>
<span data-ttu-id="15443-146">Określa odcisk palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="15443-146">Specifies the thumbprint of the certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15443-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15443-147">CommonParameters</span></span>
<span data-ttu-id="15443-148">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15443-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15443-149">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="15443-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15443-150">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15443-150">INPUTS</span></span>

## <span data-ttu-id="15443-151">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="15443-151">OUTPUTS</span></span>

## <span data-ttu-id="15443-152">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="15443-152">NOTES</span></span>

## <span data-ttu-id="15443-153">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15443-153">RELATED LINKS</span></span>

[<span data-ttu-id="15443-154">Dodaj-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="15443-154">Add-AzureCertificate</span></span>](./Add-AzureCertificate.md)

[<span data-ttu-id="15443-155">Dodaj-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="15443-155">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="15443-156">Get-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="15443-156">Get-AzureCertificate</span></span>](./Get-AzureCertificate.md)

[<span data-ttu-id="15443-157">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="15443-157">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="15443-158">Nowe — AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="15443-158">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)

[<span data-ttu-id="15443-159">Nowe — AzureVM</span><span class="sxs-lookup"><span data-stu-id="15443-159">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="15443-160">Remove-AzureCertificate</span><span class="sxs-lookup"><span data-stu-id="15443-160">Remove-AzureCertificate</span></span>](./Remove-AzureCertificate.md)


