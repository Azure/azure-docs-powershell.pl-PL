---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: AA58B897-EFA0-4321-9246-ED8E11AB3538
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7a0e0d5cac7ac27bf7eeefe8e3eb995a82a32ea4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054948"
---
# <span data-ttu-id="2053a-101">New-AzureSSHKey</span><span class="sxs-lookup"><span data-stu-id="2053a-101">New-AzureSSHKey</span></span>

## <span data-ttu-id="2053a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2053a-102">SYNOPSIS</span></span>
<span data-ttu-id="2053a-103">Tworzy obiekt klucza SSH, aby wstawić istniejący certyfikat do nowej maszyny wirtualnej opartej na platformie Linux.</span><span class="sxs-lookup"><span data-stu-id="2053a-103">Creates a SSH Key object to insert an existing certificate into a new Linux-based Azure virtual machines.</span></span>

## <span data-ttu-id="2053a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2053a-104">SYNTAX</span></span>

### <span data-ttu-id="2053a-105">para</span><span class="sxs-lookup"><span data-stu-id="2053a-105">keypair</span></span>
```
New-AzureSSHKey [-KeyPair] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2053a-106">publickey</span><span class="sxs-lookup"><span data-stu-id="2053a-106">publickey</span></span>
```
New-AzureSSHKey [-PublicKey] [-Fingerprint] <String> [-Path] <String> [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2053a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2053a-107">DESCRIPTION</span></span>
<span data-ttu-id="2053a-108">Polecenie cmdlet **New-AzureSSHKey** tworzy obiekt klucza SSH dla certyfikatu, który został już dodany do platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2053a-108">The **New-AzureSSHKey** cmdlet creates an SSH Key object for a certificate that has already been added to Azure.</span></span>
<span data-ttu-id="2053a-109">Ten obiekt klucza SSH może być następnie używany przez **nowe-AzureProvisioningConfig** podczas tworzenia obiektu konfiguracji dla nowej maszyny wirtualnej przy użyciu **nowych funkcji-AzureVM** lub podczas tworzenia nowej maszyny wirtualnej z opcją **New-AzureQuickVM**.</span><span class="sxs-lookup"><span data-stu-id="2053a-109">This SSH Key object can then be used by **New-AzureProvisioningConfig** when creating the configuration object for a new virtual machine using **New-AzureVM** , or when creating a new virtual machine with **New-AzureQuickVM**.</span></span>
<span data-ttu-id="2053a-110">Po dołączeniu w ramach skryptu tworzenia maszyny wirtualnej do nowej maszyny wirtualnej zostanie dodany określony klucz publiczny SSH lub para kluczy.</span><span class="sxs-lookup"><span data-stu-id="2053a-110">When included as part of a virtual machine creation script, this adds the specified SSH Public Key or Key Pair to the new virtual machine.</span></span>

## <span data-ttu-id="2053a-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2053a-111">EXAMPLES</span></span>

### <span data-ttu-id="2053a-112">Przykład 1: Tworzenie obiektu Ustawienia certyfikatu</span><span class="sxs-lookup"><span data-stu-id="2053a-112">Example 1: Create a certificate setting object</span></span>
```
PS C:\> $myLxCert = New-AzureSSHKey -Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
```

<span data-ttu-id="2053a-113">To polecenie tworzy obiekt ustawienia certyfikatu dla istniejącego certyfikatu, a następnie zapisuje obiekt w zmiennej do późniejszego użycia.</span><span class="sxs-lookup"><span data-stu-id="2053a-113">This command creates a certificate setting object for an existing certificate and then stores the object in a variable for later use.</span></span>

### <span data-ttu-id="2053a-114">Przykład 2: Dodawanie certyfikatu do usługi</span><span class="sxs-lookup"><span data-stu-id="2053a-114">Example 2: Add a certificate to a service</span></span>
```
PS C:\> Add-AzureCertificate -ServiceName "MySvc" -CertToDeploy "C:\temp\MyLxCert.cer"
$myLxCert = New-AzureSSHKey ?Fingerprint "D7BECD4D63EBAF86023BB4F1A5FBF5C2C924902A" -Path "/home/username/.ssh/authorized_keys"
New-AzureVMConfig -Name "MyVM2" -InstanceSize Small -ImageName $LxImage `
          | Add-AzureProvisioningConfig -Linux -LinuxUser $lxUser -SSHPublicKeys $myLxCert -Password 'pass@word1' `
          | New-AzureVM -ServiceName "MySvc"
```

<span data-ttu-id="2053a-115">To polecenie umożliwia dodanie certyfikatu do usługi Azure, a następnie utworzenie nowej maszyny wirtualnej Linux używającej tego certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="2053a-115">This command adds a certificate to an Azure service, and then creates a new Linux virtual machine that uses the certificate.</span></span>

## <span data-ttu-id="2053a-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2053a-116">PARAMETERS</span></span>

### <span data-ttu-id="2053a-117">-Odcisk cyfrowy</span><span class="sxs-lookup"><span data-stu-id="2053a-117">-Fingerprint</span></span>
<span data-ttu-id="2053a-118">Określa odcisk palca certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="2053a-118">Specifies the fingerprint of the certificate.</span></span>

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

### <span data-ttu-id="2053a-119">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2053a-119">-InformationAction</span></span>
<span data-ttu-id="2053a-120">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="2053a-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2053a-121">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2053a-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2053a-122">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="2053a-122">Continue</span></span>
- <span data-ttu-id="2053a-123">Ignorować</span><span class="sxs-lookup"><span data-stu-id="2053a-123">Ignore</span></span>
- <span data-ttu-id="2053a-124">Inquire</span><span class="sxs-lookup"><span data-stu-id="2053a-124">Inquire</span></span>
- <span data-ttu-id="2053a-125">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2053a-125">SilentlyContinue</span></span>
- <span data-ttu-id="2053a-126">Przestaw</span><span class="sxs-lookup"><span data-stu-id="2053a-126">Stop</span></span>
- <span data-ttu-id="2053a-127">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="2053a-127">Suspend</span></span>

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

### <span data-ttu-id="2053a-128">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2053a-128">-InformationVariable</span></span>
<span data-ttu-id="2053a-129">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="2053a-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2053a-130">-Para</span><span class="sxs-lookup"><span data-stu-id="2053a-130">-KeyPair</span></span>
<span data-ttu-id="2053a-131">Określa, że to polecenie cmdlet tworzy obiekt służący do wstawiania pary kluczy SSH do nowej konfiguracji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2053a-131">Specifies that this cmdlet creates an object for inserting an SSH Key Pair into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: keypair
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2053a-132">-Path</span><span class="sxs-lookup"><span data-stu-id="2053a-132">-Path</span></span>
<span data-ttu-id="2053a-133">Określa ścieżkę do przechowywania klucza publicznego SSH lub pary kluczy.</span><span class="sxs-lookup"><span data-stu-id="2053a-133">Specifies the path to store the SSH Public Key or Key Pair.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2053a-134">-PublicKey</span><span class="sxs-lookup"><span data-stu-id="2053a-134">-PublicKey</span></span>
<span data-ttu-id="2053a-135">Określa, że to polecenie cmdlet tworzy obiekt służący do wstawiania klucza publicznego SSH do nowej konfiguracji maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2053a-135">Specifies that this cmdlet creates an object for inserting an SSH Public Key into the new virtual machine configuration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: publickey
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2053a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2053a-136">CommonParameters</span></span>
<span data-ttu-id="2053a-137">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2053a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2053a-138">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2053a-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2053a-139">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2053a-139">INPUTS</span></span>

## <span data-ttu-id="2053a-140">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2053a-140">OUTPUTS</span></span>

## <span data-ttu-id="2053a-141">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2053a-141">NOTES</span></span>

## <span data-ttu-id="2053a-142">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2053a-142">RELATED LINKS</span></span>

[<span data-ttu-id="2053a-143">Dodaj-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="2053a-143">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="2053a-144">Nowe — AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="2053a-144">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="2053a-145">Nowe — AzureVM</span><span class="sxs-lookup"><span data-stu-id="2053a-145">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="2053a-146">Nowe — AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="2053a-146">New-AzureQuickVM</span></span>](./New-AzureQuickVM.md)


