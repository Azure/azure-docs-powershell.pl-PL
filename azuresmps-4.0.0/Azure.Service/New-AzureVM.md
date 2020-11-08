---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 1999C880-F8F9-4CED-91A9-33E9BBDFE27D
online version: ''
schema: 2.0.0
ms.openlocfilehash: 09a3d7be7bf71e73443dcbb31464ee6f7f19b43a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055166"
---
# <span data-ttu-id="c02e1-101">New-AzureVM</span><span class="sxs-lookup"><span data-stu-id="c02e1-101">New-AzureVM</span></span>

## <span data-ttu-id="c02e1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c02e1-102">SYNOPSIS</span></span>
<span data-ttu-id="c02e1-103">Umożliwia utworzenie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c02e1-103">Creates an Azure virtual machine.</span></span>

## <span data-ttu-id="c02e1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c02e1-104">SYNTAX</span></span>

### <span data-ttu-id="c02e1-105">ExistingService (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c02e1-105">ExistingService (Default)</span></span>
```
New-AzureVM -ServiceName <String> [-DeploymentLabel <String>] [-DeploymentName <String>] [-VNetName <String>]
 [-DnsSettings <DnsServer[]>] [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]>
 [-WaitForBoot] [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="c02e1-106">Usługa serviceservice</span><span class="sxs-lookup"><span data-stu-id="c02e1-106">CreateService</span></span>
```
New-AzureVM -ServiceName <String> [-Location <String>] [-AffinityGroup <String>] [-ServiceLabel <String>]
 [-ReverseDnsFqdn <String>] [-ServiceDescription <String>] [-DeploymentLabel <String>]
 [-DeploymentName <String>] [-VNetName <String>] [-DnsSettings <DnsServer[]>]
 [-InternalLoadBalancerConfig <InternalLoadBalancerConfig>] -VMs <PersistentVM[]> [-WaitForBoot]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="c02e1-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c02e1-107">DESCRIPTION</span></span>
<span data-ttu-id="c02e1-108">Polecenie cmdlet **New-AzureVM** umożliwia dodanie nowej maszyny wirtualnej do istniejącej usługi Azure lub utworzenie maszyny wirtualnej i usługi w bieżącej subskrypcji, jeśli została określona *Lokalizacja* lub *AffinityGroup* .</span><span class="sxs-lookup"><span data-stu-id="c02e1-108">The **New-AzureVM** cmdlet adds a new virtual machine to an existing Azure service, or creates a virtual machine and service in the current subscription if either the *Location* or *AffinityGroup* is specified.</span></span>

## <span data-ttu-id="c02e1-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c02e1-109">EXAMPLES</span></span>

### <span data-ttu-id="c02e1-110">Przykład 1: Tworzenie maszyny wirtualnej dla konfiguracji systemu Windows</span><span class="sxs-lookup"><span data-stu-id="c02e1-110">Example 1: Create a virtual machine for a Windows configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine07" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername PsTestAdmin | New-AzureVM -ServiceName "ContosoService" -AffinityGroup "Contoso" -WaitForBoot
```

<span data-ttu-id="c02e1-111">To polecenie tworzy konfigurację obsługi na podstawie konfiguracji maszyny wirtualnej dla systemu operacyjnego Windows i używa jej do tworzenia maszyny wirtualnej w określonej grupie koligacji.</span><span class="sxs-lookup"><span data-stu-id="c02e1-111">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="c02e1-112">Przykład 2: Tworzenie maszyny wirtualnej dla konfiguracji systemu Linux</span><span class="sxs-lookup"><span data-stu-id="c02e1-112">Example 2: Create a virtual machine for a Linux configuration</span></span>
```
PS C:\> New-AzureVMConfig -Name "SUSEVM02" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[7].ImageName | Add-AzureProvisioningConfig -Linux -LinuxUser "RootMain" -Password "password" -AdminUsername PsTestAdmin | New-AzureVM
```

<span data-ttu-id="c02e1-113">To polecenie tworzy konfigurację obsługi na podstawie konfiguracji maszyny wirtualnej dla systemu Linux i używa jej do tworzenia maszyny wirtualnej w określonej grupie koligacji.</span><span class="sxs-lookup"><span data-stu-id="c02e1-113">This command creates a provisioning configuration based on a virtual machine configuration for Linux, and uses it to create a virtual machine in a specified affinity group.</span></span>

### <span data-ttu-id="c02e1-114">Przykład 3: Tworzenie maszyny wirtualnej i Dodawanie dysku z danymi</span><span class="sxs-lookup"><span data-stu-id="c02e1-114">Example 3: Create a virtual machine and add a data disk</span></span>
```
PS C:\> $Images = Get-AzureVMImage
PS C:\> $Image = $Images[4]
PS C:\> $VirtualMachine02 = New-AzureVMConfig -Name "VirtualMachine02" -InstanceSize ExtraSmall -ImageName $myImage.ImageName | Add-AzureProvisioningConfig -Windows -Password "password" | Add-AzureDataDisk -CreateNew -DiskSizeInGB 50 -DiskLabel "DataDisk50" -LUN 0
```

<span data-ttu-id="c02e1-115">Dwa pierwsze polecenia uzyskują dostępne obrazy za pomocą polecenia cmdlet **Get-AzureVMImage** i zapisuje je w zmiennej $Image.</span><span class="sxs-lookup"><span data-stu-id="c02e1-115">The first two commands get available images by using the **Get-AzureVMImage** cmdlet, and stores one of them in the $Image variable.</span></span>

<span data-ttu-id="c02e1-116">To polecenie tworzy konfigurację obsługi na podstawie konfiguracji maszyny wirtualnej dla systemu operacyjnego Windows i używa jej do tworzenia maszyny wirtualnej z dyskiem danych platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c02e1-116">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with an Azure data disk.</span></span>

### <span data-ttu-id="c02e1-117">Przykład 4: Tworzenie maszyny wirtualnej z zastrzeżonym adresem IP</span><span class="sxs-lookup"><span data-stu-id="c02e1-117">Example 4: Create a virtual machine with a reserved IP address</span></span>
```
PS C:\> New-AzureVMConfig -Name "VirtualMachine06" -InstanceSize ExtraSmall -ImageName (Get-AzureVMImage)[4].ImageName | Add-AzureProvisioningConfig -Windows -Password $adminPassword -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService02" -AffinityGroup "Contoso" -ReservedIPName $ipName
```

<span data-ttu-id="c02e1-118">To polecenie tworzy konfigurację obsługi na podstawie konfiguracji maszyny wirtualnej dla systemu operacyjnego Windows i używa jej do tworzenia maszyny wirtualnej z zastrzeżonym adresem IP.</span><span class="sxs-lookup"><span data-stu-id="c02e1-118">This command creates a provisioning configuration based on a virtual machine configuration for the Windows operating system, and uses it to create a virtual machine with a reserved IP address.</span></span>

## <span data-ttu-id="c02e1-119">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c02e1-119">PARAMETERS</span></span>

### <span data-ttu-id="c02e1-120">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="c02e1-120">-AffinityGroup</span></span>
<span data-ttu-id="c02e1-121">Określa grupę koligacji platformy Azure, w której znajduje się usługa chmury.</span><span class="sxs-lookup"><span data-stu-id="c02e1-121">Specifies the Azure affinity group in which the cloud service resides.</span></span>
<span data-ttu-id="c02e1-122">Ten parametr jest wymagany tylko wtedy, gdy to polecenie cmdlet tworzy usługę w chmurze.</span><span class="sxs-lookup"><span data-stu-id="c02e1-122">This parameter is required only when this cmdlet creates a cloud service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c02e1-123">-DeploymentLabel</span><span class="sxs-lookup"><span data-stu-id="c02e1-123">-DeploymentLabel</span></span>
<span data-ttu-id="c02e1-124">Określa etykietę wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="c02e1-124">Specifies a label for the deployment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c02e1-125">-Deploymentname</span><span class="sxs-lookup"><span data-stu-id="c02e1-125">-DeploymentName</span></span>
<span data-ttu-id="c02e1-126">Określa nazwę wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="c02e1-126">Specifies a deployment name.</span></span>
<span data-ttu-id="c02e1-127">Jeśli nie podano tego polecenia, to polecenie cmdlet użyje nazwy usługi jako nazwy wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="c02e1-127">If not specified, this cmdlet uses the service name as the deployment name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c02e1-128">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="c02e1-128">-DnsSettings</span></span>
<span data-ttu-id="c02e1-129">Określa obiekt serwera DNS definiujący ustawienia DNS nowego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="c02e1-129">Specifies a DNS Server object that defines the DNS settings for the new deployment.</span></span>

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c02e1-130">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="c02e1-130">-InformationAction</span></span>
<span data-ttu-id="c02e1-131">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="c02e1-131">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c02e1-132">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="c02e1-132">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c02e1-133">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="c02e1-133">Continue</span></span>
- <span data-ttu-id="c02e1-134">Ignorować</span><span class="sxs-lookup"><span data-stu-id="c02e1-134">Ignore</span></span>
- <span data-ttu-id="c02e1-135">Inquire</span><span class="sxs-lookup"><span data-stu-id="c02e1-135">Inquire</span></span>
- <span data-ttu-id="c02e1-136">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c02e1-136">SilentlyContinue</span></span>
- <span data-ttu-id="c02e1-137">Przestaw</span><span class="sxs-lookup"><span data-stu-id="c02e1-137">Stop</span></span>
- <span data-ttu-id="c02e1-138">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="c02e1-138">Suspend</span></span>

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

### <span data-ttu-id="c02e1-139">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c02e1-139">-InformationVariable</span></span>
<span data-ttu-id="c02e1-140">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="c02e1-140">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c02e1-141">-InternalLoadBalancerConfig</span><span class="sxs-lookup"><span data-stu-id="c02e1-141">-InternalLoadBalancerConfig</span></span>
<span data-ttu-id="c02e1-142">Umożliwia określenie wewnętrznego modułu równoważenia obciążenia.</span><span class="sxs-lookup"><span data-stu-id="c02e1-142">Specifies an internal load balancer.</span></span>
<span data-ttu-id="c02e1-143">Ten parametr nie jest stosowany.</span><span class="sxs-lookup"><span data-stu-id="c02e1-143">This parameter is not used.</span></span>

```yaml
Type: InternalLoadBalancerConfig
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c02e1-144">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="c02e1-144">-Location</span></span>
<span data-ttu-id="c02e1-145">Określa lokalizację, w której znajduje się nowa usługa.</span><span class="sxs-lookup"><span data-stu-id="c02e1-145">Specifies the location that hosts the new service.</span></span>
<span data-ttu-id="c02e1-146">Jeśli usługa już istnieje, nie określaj tego parametru.</span><span class="sxs-lookup"><span data-stu-id="c02e1-146">If the service already exists, do not specify this parameter.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c02e1-147">-Profile</span><span class="sxs-lookup"><span data-stu-id="c02e1-147">-Profile</span></span>
<span data-ttu-id="c02e1-148">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c02e1-148">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c02e1-149">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="c02e1-149">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c02e1-150">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="c02e1-150">-ReservedIPName</span></span>
<span data-ttu-id="c02e1-151">Określa nazwę zastrzeżonego adresu IP.</span><span class="sxs-lookup"><span data-stu-id="c02e1-151">Specifies the name of the reserved IP address.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c02e1-152">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="c02e1-152">-ReverseDnsFqdn</span></span>
<span data-ttu-id="c02e1-153">Określa w pełni kwalifikowaną nazwę domeny dla zwrotnego DNS.</span><span class="sxs-lookup"><span data-stu-id="c02e1-153">Specifies the fully-qualified domain name for reverse DNS.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c02e1-154">-Opis</span><span class="sxs-lookup"><span data-stu-id="c02e1-154">-ServiceDescription</span></span>
<span data-ttu-id="c02e1-155">Określa opis nowej usługi.</span><span class="sxs-lookup"><span data-stu-id="c02e1-155">Specifies a description for the new service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c02e1-156">-Servicelabel</span><span class="sxs-lookup"><span data-stu-id="c02e1-156">-ServiceLabel</span></span>
<span data-ttu-id="c02e1-157">Określa etykietę nowej usługi.</span><span class="sxs-lookup"><span data-stu-id="c02e1-157">Specifies a label for the new service.</span></span>

```yaml
Type: String
Parameter Sets: CreateService
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c02e1-158">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="c02e1-158">-ServiceName</span></span>
<span data-ttu-id="c02e1-159">Określa nową lub istniejącą nazwę usługi.</span><span class="sxs-lookup"><span data-stu-id="c02e1-159">Specifies the new or existing service name.</span></span>

<span data-ttu-id="c02e1-160">Jeśli usługa nie istnieje, to polecenie cmdlet utworzy je za Ciebie.</span><span class="sxs-lookup"><span data-stu-id="c02e1-160">If the service does not exist, this cmdlet creates it for you.</span></span>
<span data-ttu-id="c02e1-161">Użyj parametru *Location* lub *AffinityGroup* , aby określić, gdzie utworzyć usługę.</span><span class="sxs-lookup"><span data-stu-id="c02e1-161">Use the *Location* or *AffinityGroup* parameter to specify where to create the service.</span></span>

<span data-ttu-id="c02e1-162">Jeśli ta usługa istnieje, parametr *Lokalizacja* lub *AffinityGroup* nie jest potrzebny.</span><span class="sxs-lookup"><span data-stu-id="c02e1-162">If the service exists, the *Location* or *AffinityGroup* parameter is not needed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c02e1-163">-VMs</span><span class="sxs-lookup"><span data-stu-id="c02e1-163">-VMs</span></span>
<span data-ttu-id="c02e1-164">Określa listę obiektów maszyny wirtualnej, które mają zostać utworzone.</span><span class="sxs-lookup"><span data-stu-id="c02e1-164">Specifies a list of virtual machine objects to create.</span></span>

```yaml
Type: PersistentVM[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c02e1-165">-VNetName</span><span class="sxs-lookup"><span data-stu-id="c02e1-165">-VNetName</span></span>
<span data-ttu-id="c02e1-166">Określa nazwę sieci wirtualnej, w której to polecenie cmdlet wdraża maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="c02e1-166">Specifies the virtual network name where this cmdlet deploys the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c02e1-167">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="c02e1-167">-WaitForBoot</span></span>
<span data-ttu-id="c02e1-168">Określa, że to polecenie cmdlet oczekuje, że maszyna wirtualna będzie mieć dostęp do stanu **ReadyRole** .</span><span class="sxs-lookup"><span data-stu-id="c02e1-168">Specifies that this cmdlet waits for the virtual machine to reach the **ReadyRole** state.</span></span>
<span data-ttu-id="c02e1-169">To polecenie cmdlet kończy się niepowodzeniem, jeśli maszyna wirtualna jest w jednym z następujących stanów podczas oczekiwania: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.</span><span class="sxs-lookup"><span data-stu-id="c02e1-169">This cmdlet fails if the virtual machine falls in one of the following states while waiting: FailedStartingVM, ProvisioningFailed, ProvisioningTimeout.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c02e1-170">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c02e1-170">CommonParameters</span></span>
<span data-ttu-id="c02e1-171">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c02e1-171">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c02e1-172">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c02e1-172">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c02e1-173">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c02e1-173">INPUTS</span></span>

## <span data-ttu-id="c02e1-174">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c02e1-174">OUTPUTS</span></span>

## <span data-ttu-id="c02e1-175">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c02e1-175">NOTES</span></span>

## <span data-ttu-id="c02e1-176">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c02e1-176">RELATED LINKS</span></span>

[<span data-ttu-id="c02e1-177">Dodaj-AzureDataDisk</span><span class="sxs-lookup"><span data-stu-id="c02e1-177">Add-AzureDataDisk</span></span>](./Add-AzureDataDisk.md)

[<span data-ttu-id="c02e1-178">Dodaj-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="c02e1-178">Add-AzureProvisioningConfig</span></span>](./Add-AzureProvisioningConfig.md)

[<span data-ttu-id="c02e1-179">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="c02e1-179">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="c02e1-180">Nowe — AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="c02e1-180">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)


