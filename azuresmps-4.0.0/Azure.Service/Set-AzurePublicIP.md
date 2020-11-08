---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: BFD4E4AD-8F1B-4E4E-BF52-435A6EEAA060
online version: ''
schema: 2.0.0
ms.openlocfilehash: 6beed021bfc12db3a3fdb1a66ee8ae6fe2e1e9b9
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054921"
---
# <span data-ttu-id="ef62c-101">Set-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="ef62c-101">Set-AzurePublicIP</span></span>

## <span data-ttu-id="ef62c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ef62c-102">SYNOPSIS</span></span>
<span data-ttu-id="ef62c-103">Dodaje publiczny adres IP do maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ef62c-103">Adds a Public IP to an Azure virtual machine.</span></span>

## <span data-ttu-id="ef62c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ef62c-104">SYNTAX</span></span>

```
Set-AzurePublicIP [-PublicIPName] <String> [[-IdleTimeoutInMinutes] <Int32>] [[-DomainNameLabel] <String>]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="ef62c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ef62c-105">DESCRIPTION</span></span>
<span data-ttu-id="ef62c-106">Polecenie cmdlet **Set-AzurePublicIP** dodaje publiczny adres IP do maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="ef62c-106">The **Set-AzurePublicIP** cmdlet adds a Public IP to an Azure virtual machine.</span></span>
<span data-ttu-id="ef62c-107">Jeśli uruchamiasz to polecenie cmdlet dla istniejącej maszyny wirtualnej, zaktualizuj maszynę wirtualną, aby zaimplementować zmiany.</span><span class="sxs-lookup"><span data-stu-id="ef62c-107">If you run this cmdlet for an existing virtual machine, update the virtual machine to implement your changes.</span></span>
<span data-ttu-id="ef62c-108">Możesz określić etykietę nazwy domeny, aby utworzyć odpowiedni wpis DNS dla publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="ef62c-108">You can specify a domain name label to create a corresponding DNS entry for the public IP.</span></span>

## <span data-ttu-id="ef62c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ef62c-109">EXAMPLES</span></span>

### <span data-ttu-id="ef62c-110">Przykład 1: Dodawanie publicznego adresu IP do istniejącej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ef62c-110">Example 1: Add a Public IP to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" | Update-AzureVM
```

<span data-ttu-id="ef62c-111">To polecenie pobiera maszynę wirtualną o nazwie FTPInstance w usłudze o nazwie FTPInAzure przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="ef62c-111">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="ef62c-112">Polecenie przekazanie maszyny wirtualnej do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="ef62c-112">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ef62c-113">Bieżące polecenie cmdlet umożliwia dodanie publicznej nazwy ftpip.</span><span class="sxs-lookup"><span data-stu-id="ef62c-113">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="ef62c-114">Polecenie przekazanie maszyny wirtualnej do polecenia cmdlet **Update-AzureVM** , które implementuje wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="ef62c-114">The command passes the virtual machine to the **Update-AzureVM** cmdlet, which implements your changes.</span></span>

### <span data-ttu-id="ef62c-115">Przykład 2: Dodawanie publicznego adresu IP do nowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ef62c-115">Example 2: Add a Public IP to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="ef62c-116">To polecenie tworzy obiekt konfiguracji maszyny wirtualnej przy użyciu polecenia cmdlet **New-AzureVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="ef62c-116">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="ef62c-117">Polecenie przekazuje ten obiekt do polecenia cmdlet **Add-AzureProvisioningConfig** , które zapewnia dodatkową konfigurację.</span><span class="sxs-lookup"><span data-stu-id="ef62c-117">The command passes that object to the **Add-AzureProvisioningConfig** cmdlet, which provides additional configuration.</span></span>
<span data-ttu-id="ef62c-118">Bieżące polecenie cmdlet umożliwia dodanie publicznej nazwy ftpip.</span><span class="sxs-lookup"><span data-stu-id="ef62c-118">The current cmdlet adds the Public IP name ftpip.</span></span>
<span data-ttu-id="ef62c-119">Polecenie przekazanie konfiguracji do polecenia cmdlet **New-AzureVM** , które powoduje utworzenie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ef62c-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="ef62c-120">Przykład 3: Dodawanie publicznego adresu IP i etykiety do istniejącej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ef62c-120">Example 3: Add a Public IP and label to an existing virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "FTPInAzure" -Name "FTPInstance" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | Update-AzureVM
```

<span data-ttu-id="ef62c-121">To polecenie pobiera maszynę wirtualną o nazwie FTPInstance w usłudze o nazwie FTPInAzure przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="ef62c-121">This command gets the virtual machine named FTPInstance in the service named FTPInAzure by using the **Get-AzureVM** cmdlet.</span></span>
<span data-ttu-id="ef62c-122">Polecenie przekazanie maszyny wirtualnej do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="ef62c-122">The command passes that virtual machine to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="ef62c-123">Bieżące polecenie cmdlet dodaje publiczną nazwę IP ftpip i etykietę ipname.</span><span class="sxs-lookup"><span data-stu-id="ef62c-123">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="ef62c-124">Polecenie aktualizuje maszynę wirtualną, która implementuje wprowadzone zmiany.</span><span class="sxs-lookup"><span data-stu-id="ef62c-124">The command updates the virtual machine, which implements your changes.</span></span>

### <span data-ttu-id="ef62c-125">Przykład 4: Dodawanie publicznego adresu IP i etykiety do nowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ef62c-125">Example 4: Add a Public IP and label to a new virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "FTPInstance" -InstanceSize Small -ImageName $images[50].ImageName | Add-AzureProvisioningConfig -Windows -AdminUsername "AdminMain" -Password "password" | Set-AzurePublicIP -PublicIPName "ftpip" -DomainNameLabel "ipname" | New-AzureVM -ServiceName "FTPinAzure" -Location "North Central US"
```

<span data-ttu-id="ef62c-126">To polecenie tworzy obiekt konfiguracji maszyny wirtualnej, a następnie przekazuje ten obiekt do **dodatku Add-AzureProvisioningConfig** , który zapewnia dodatkową konfigurację.</span><span class="sxs-lookup"><span data-stu-id="ef62c-126">This command creates a virtual machine configuration object, and then passes that object to **Add-AzureProvisioningConfig** , which provides additional configuration.</span></span>
<span data-ttu-id="ef62c-127">Bieżące polecenie cmdlet dodaje publiczną nazwę IP ftpip i etykietę ipname.</span><span class="sxs-lookup"><span data-stu-id="ef62c-127">The current cmdlet adds the Public IP name ftpip and the label ipname.</span></span>
<span data-ttu-id="ef62c-128">Polecenie tworzy maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="ef62c-128">The command creates the virtual machine.</span></span>

## <span data-ttu-id="ef62c-129">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ef62c-129">PARAMETERS</span></span>

### <span data-ttu-id="ef62c-130">-DomainNameLabel</span><span class="sxs-lookup"><span data-stu-id="ef62c-130">-DomainNameLabel</span></span>
<span data-ttu-id="ef62c-131">Określa nazwę, która ma być używana dla odpowiedniego wpisu DNS dla publicznego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="ef62c-131">Specifies the name to use for a corresponding DNS entry for the public IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62c-132">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="ef62c-132">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="ef62c-133">Określa okres czasu bezczynności protokołu TCP w minutach.</span><span class="sxs-lookup"><span data-stu-id="ef62c-133">Specifies the TCP idle time-out period in minutes.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62c-134">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ef62c-134">-InformationAction</span></span>
<span data-ttu-id="ef62c-135">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="ef62c-135">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ef62c-136">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ef62c-136">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ef62c-137">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="ef62c-137">Continue</span></span>
- <span data-ttu-id="ef62c-138">Ignorować</span><span class="sxs-lookup"><span data-stu-id="ef62c-138">Ignore</span></span>
- <span data-ttu-id="ef62c-139">Inquire</span><span class="sxs-lookup"><span data-stu-id="ef62c-139">Inquire</span></span>
- <span data-ttu-id="ef62c-140">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ef62c-140">SilentlyContinue</span></span>
- <span data-ttu-id="ef62c-141">Przestaw</span><span class="sxs-lookup"><span data-stu-id="ef62c-141">Stop</span></span>
- <span data-ttu-id="ef62c-142">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="ef62c-142">Suspend</span></span>

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

### <span data-ttu-id="ef62c-143">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ef62c-143">-InformationVariable</span></span>
<span data-ttu-id="ef62c-144">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="ef62c-144">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ef62c-145">-Profile</span><span class="sxs-lookup"><span data-stu-id="ef62c-145">-Profile</span></span>
<span data-ttu-id="ef62c-146">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef62c-146">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ef62c-147">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ef62c-147">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef62c-148">-PublicIPName</span><span class="sxs-lookup"><span data-stu-id="ef62c-148">-PublicIPName</span></span>
<span data-ttu-id="ef62c-149">Określa publiczną nazwę IP.</span><span class="sxs-lookup"><span data-stu-id="ef62c-149">Specifies the Public IP name.</span></span>

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

### <span data-ttu-id="ef62c-150">-VM</span><span class="sxs-lookup"><span data-stu-id="ef62c-150">-VM</span></span>
<span data-ttu-id="ef62c-151">Określa maszynę wirtualną, do której to polecenie cmdlet dodaje publiczny adres IP.</span><span class="sxs-lookup"><span data-stu-id="ef62c-151">Specifies the virtual machine to which this cmdlet adds Public IP.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ef62c-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef62c-152">CommonParameters</span></span>
<span data-ttu-id="ef62c-153">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef62c-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef62c-154">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef62c-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef62c-155">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ef62c-155">INPUTS</span></span>

## <span data-ttu-id="ef62c-156">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ef62c-156">OUTPUTS</span></span>

### <span data-ttu-id="ef62c-157">Microsoft. platformy windowsazure. Commands. servicemanagement. model. IPersistentVM</span><span class="sxs-lookup"><span data-stu-id="ef62c-157">Microsoft.WindowsAzure.Commands.ServiceManagement.Model.IPersistentVM</span></span>

## <span data-ttu-id="ef62c-158">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ef62c-158">NOTES</span></span>

## <span data-ttu-id="ef62c-159">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ef62c-159">RELATED LINKS</span></span>

[<span data-ttu-id="ef62c-160">Get-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="ef62c-160">Get-AzurePublicIP</span></span>](./Get-AzurePublicIP.md)

[<span data-ttu-id="ef62c-161">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ef62c-161">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="ef62c-162">Nowe — AzureVM</span><span class="sxs-lookup"><span data-stu-id="ef62c-162">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="ef62c-163">Nowe — AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="ef62c-163">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)

[<span data-ttu-id="ef62c-164">Remove-AzurePublicIP</span><span class="sxs-lookup"><span data-stu-id="ef62c-164">Remove-AzurePublicIP</span></span>](./Remove-AzurePublicIP.md)

[<span data-ttu-id="ef62c-165">Update-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ef62c-165">Update-AzureVM</span></span>](./Update-AzureVM.md)


