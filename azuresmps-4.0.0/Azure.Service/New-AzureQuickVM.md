---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: F94584BC-EC02-412D-B089-B98A6FF8F505
online version: ''
schema: 2.0.0
ms.openlocfilehash: a5b7758a7316fa6c34ffe6b5225cd252f39c5d7c
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94054875"
---
# <span data-ttu-id="9c461-101">New-AzureQuickVM</span><span class="sxs-lookup"><span data-stu-id="9c461-101">New-AzureQuickVM</span></span>

## <span data-ttu-id="9c461-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9c461-102">SYNOPSIS</span></span>
<span data-ttu-id="9c461-103">Umożliwia skonfigurowanie i utworzenie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9c461-103">Configures and creates an Azure virtual machine.</span></span>

## <span data-ttu-id="9c461-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9c461-104">SYNTAX</span></span>

### <span data-ttu-id="9c461-105">Windows (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="9c461-105">Windows (Default)</span></span>
```
New-AzureQuickVM [-Windows] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-AdminUsername <String>]
 [-Certificates <CertificateSettingList>] [-WaitForBoot] [-DisableWinRMHttps] [-EnableWinRMHttp]
 [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey]
 [-NoWinRMEndpoint] [-VNetName <String>] [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>]
 [-HostCaching <String>] [-AvailabilitySetName <String>] [-InstanceSize <String>] [-MediaLocation <String>]
 [-DisableGuestAgent] [-CustomDataFile <String>] [-ReservedIPName <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="9c461-106">Linux</span><span class="sxs-lookup"><span data-stu-id="9c461-106">Linux</span></span>
```
New-AzureQuickVM [-Linux] -ServiceName <String> [-Name <String>] -ImageName <String> [-Password <String>]
 [-ReverseDnsFqdn <String>] [-Location <String>] [-AffinityGroup <String>] [-LinuxUser <String>] [-WaitForBoot]
 [-SSHPublicKeys <SSHPublicKeyList>] [-SSHKeyPairs <SSHKeyPairList>] [-VNetName <String>]
 [-SubnetNames <String[]>] [-DnsSettings <DnsServer[]>] [-HostCaching <String>] [-AvailabilitySetName <String>]
 [-InstanceSize <String>] [-MediaLocation <String>] [-DisableGuestAgent] [-CustomDataFile <String>]
 [-ReservedIPName <String>] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="9c461-107">Opis</span><span class="sxs-lookup"><span data-stu-id="9c461-107">DESCRIPTION</span></span>
<span data-ttu-id="9c461-108">Polecenie cmdlet **New-AzureQuickVM** umożliwia skonfigurowanie i utworzenie maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9c461-108">The **New-AzureQuickVM** cmdlet configures and creates an Azure virtual machine.</span></span>
<span data-ttu-id="9c461-109">To polecenie cmdlet umożliwia wdrożenie maszyny wirtualnej w istniejącej usłudze Azure.</span><span class="sxs-lookup"><span data-stu-id="9c461-109">This cmdlet can deploy a virtual machine into an existing Azure service.</span></span>
<span data-ttu-id="9c461-110">To polecenie cmdlet może również utworzyć usługę Azure obsługującą nową maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="9c461-110">This cmdlet can alternatively create an Azure service that hosts the new virtual machine.</span></span>

## <span data-ttu-id="9c461-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9c461-111">EXAMPLES</span></span>

### <span data-ttu-id="9c461-112">Przykład 1: Tworzenie maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9c461-112">Example 1: Create a virtual machine</span></span>
```
PS C:\> New-AzureQuickVM -Windows -ServiceName "ContosoService17" -Name "VirutalMachine01" -ImageName "Image07" -Password "password" -AdminUsername "AdminMain" -WaitForBoot
```

<span data-ttu-id="9c461-113">To polecenie tworzy maszynę wirtualną z uruchomionym systemem operacyjnym Windows w istniejącej usłudze.</span><span class="sxs-lookup"><span data-stu-id="9c461-113">This command creates a virtual machine that runs the Windows operating system in an existing service.</span></span>
<span data-ttu-id="9c461-114">Polecenie cmdlet jest podstawą maszyny wirtualnej na określonym obrazie.</span><span class="sxs-lookup"><span data-stu-id="9c461-114">The cmdlet bases the virtual machine on the specified image.</span></span>
<span data-ttu-id="9c461-115">Polecenie określa parametr *WaitForBoot* .</span><span class="sxs-lookup"><span data-stu-id="9c461-115">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="9c461-116">Dlatego polecenie cmdlet oczekuje na uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c461-116">Therefore, the cmdlet waits for the virtual machine to start.</span></span>

### <span data-ttu-id="9c461-117">Przykład 2: Tworzenie maszyny wirtualnej z użyciem certyfikatów</span><span class="sxs-lookup"><span data-stu-id="9c461-117">Example 2: Create a virtual machine that by using certificates</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
PS C:\> New-AzureQuickVM -Windows -ServiceName "MySvc1" -name "MyWinVM1" -ImageName "Image07" -Password "password" -AdminUserName "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] -WaitForBoot
```

<span data-ttu-id="9c461-118">Pierwsze polecenie pobiera certyfikaty ze sklepu i przechowuje je w zmiennej $certs.</span><span class="sxs-lookup"><span data-stu-id="9c461-118">The first command gets certificates from a store, and stores them in the $certs variable.</span></span>

<span data-ttu-id="9c461-119">Drugie polecenie tworzy maszynę wirtualną z uruchomionym systemem operacyjnym Windows w istniejącej usłudze z obrazu.</span><span class="sxs-lookup"><span data-stu-id="9c461-119">The second command creates a virtual machine that runs the Windows operating system in an existing service from an image.</span></span>
<span data-ttu-id="9c461-120">Na maszynie wirtualnej jest włączony domyślnie odbiornik https usługi WinRM.</span><span class="sxs-lookup"><span data-stu-id="9c461-120">By default, WinRM Https listener is enabled on the virtual machine.</span></span>
<span data-ttu-id="9c461-121">Polecenie określa parametr *WaitForBoot* .</span><span class="sxs-lookup"><span data-stu-id="9c461-121">The command specifies the *WaitForBoot* parameter.</span></span>
<span data-ttu-id="9c461-122">Dlatego polecenie cmdlet oczekuje na uruchomienie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c461-122">Therefore, the cmdlet waits for the virtual machine to start.</span></span>
<span data-ttu-id="9c461-123">Polecenie przekazuje certyfikat usługi WinRM i certyfikat x509 usłudze hostowanej.</span><span class="sxs-lookup"><span data-stu-id="9c461-123">The command uploads a WinRM Certificate and X509Certificates to the hosted service.</span></span>

### <span data-ttu-id="9c461-124">Przykład 3: Tworzenie maszyny wirtualnej z uruchomionym systemem operacyjnym Linux</span><span class="sxs-lookup"><span data-stu-id="9c461-124">Example 3: Create a virtual machine that runs the Linux operating system</span></span>
```
PS C:\> New-AzureQuickVM -Linux -ServiceName "ContosoServiceLinux01" -Name "LinuxVirtualMachine01" -ImageName "LinuxImage01" -LinuxUser "RootMain" -Password "password" -Location "Central US"
```

<span data-ttu-id="9c461-125">To polecenie tworzy maszynę wirtualną, która uruchamia system operacyjny Linux z obrazu.</span><span class="sxs-lookup"><span data-stu-id="9c461-125">This command creates a virtual machine that runs the Linux operating system from an image.</span></span>
<span data-ttu-id="9c461-126">To polecenie tworzy usługę do obsługi nowej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c461-126">This command creates a service to host the new virtual machine.</span></span>
<span data-ttu-id="9c461-127">Polecenie określa lokalizację usługi.</span><span class="sxs-lookup"><span data-stu-id="9c461-127">The command specifies a location for the service.</span></span>

### <span data-ttu-id="9c461-128">Przykład 4: Tworzenie maszyny wirtualnej i tworzenie usługi do obsługi nowej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="9c461-128">Example 4: Create a virtual machine and create a service to host the new virtual machine</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService03" -Name " VirtualMachine25" -ImageName $images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name
```

<span data-ttu-id="9c461-129">Pierwsze polecenie uzyskuje lokalizacje za pomocą polecenia cmdlet **Get-AzureLocation** , a następnie zapisuje je w zmiennej tablicowej $Locations.</span><span class="sxs-lookup"><span data-stu-id="9c461-129">The first command gets locations by using the **Get-AzureLocation** cmdlet, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="9c461-130">Drugie polecenie pobiera dostępne obrazy za pomocą polecenia cmdlet **Get-AzureVMImage** , a następnie zapisuje je w zmiennej tablicowej $images.</span><span class="sxs-lookup"><span data-stu-id="9c461-130">The second command gets available images by using the **Get-AzureVMImage** cmdlet, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="9c461-131">Polecenie ostatnie powoduje utworzenie dużej maszyny wirtualnej o nazwie VirtualMachine25.</span><span class="sxs-lookup"><span data-stu-id="9c461-131">The final command creates a large virtual machine named VirtualMachine25.</span></span>
<span data-ttu-id="9c461-132">Na maszynie wirtualnej jest uruchamiany system operacyjny Windows.</span><span class="sxs-lookup"><span data-stu-id="9c461-132">The virtual machine runs the Windows operating system.</span></span>
<span data-ttu-id="9c461-133">Jest ona oparta na jednym z obrazów w $Images.</span><span class="sxs-lookup"><span data-stu-id="9c461-133">It is based on one of the images in $Images.</span></span>
<span data-ttu-id="9c461-134">Polecenie utworzy usługę o nazwie ContosoService03 dla nowej maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c461-134">The command creates a service named ContosoService03 for the new virtual machine.</span></span>
<span data-ttu-id="9c461-135">Usługa znajduje się w lokalizacji $Locations.</span><span class="sxs-lookup"><span data-stu-id="9c461-135">The service is in a location in $Locations.</span></span>

### <span data-ttu-id="9c461-136">Przykład 5: Tworzenie maszyny wirtualnej zawierającej zarezerwowaną nazwę IP</span><span class="sxs-lookup"><span data-stu-id="9c461-136">Example 5: Create a virtual machine that has a reserved IP name</span></span>
```
PS C:\> $Locations = Get-AzureLocation
PS C:\> $Images = Get-AzureVMImage
PS C:\> New-AzureQuickVM -Windows -InstanceSize "Large" -ServiceName "ContosoService04" -Name "VirtualMachine27" -ImageName $Images[4].imagename -Password "password" -AdminUsername "AdminMain" -Location $Locations[0].name -ReservedIPName $ipName
```

<span data-ttu-id="9c461-137">Pierwsze polecenie uzyskuje lokalizacje, a następnie zapisuje je w zmiennej tablicowej $Locations.</span><span class="sxs-lookup"><span data-stu-id="9c461-137">The first command gets locations, and then stores them in the $Locations array variable.</span></span>

<span data-ttu-id="9c461-138">Drugie polecenie pobiera dostępne obrazy, a następnie zapisuje je w zmiennej tablicowej $Images.</span><span class="sxs-lookup"><span data-stu-id="9c461-138">The second command gets available images, and then stores them in the $Images array variable.</span></span>

<span data-ttu-id="9c461-139">Polecenie ostatnie powoduje utworzenie maszyny wirtualnej o nazwie VirtualMachine27 na podstawie jednego z obrazów w $Images.</span><span class="sxs-lookup"><span data-stu-id="9c461-139">The final command creates a virtual machine named VirtualMachine27 based on one of the images in $Images.</span></span>
<span data-ttu-id="9c461-140">Polecenie tworzy usługę w lokalizacji w $Locations.</span><span class="sxs-lookup"><span data-stu-id="9c461-140">The command creates a service in a location in $Locations.</span></span>
<span data-ttu-id="9c461-141">Maszyna wirtualna ma zarezerwowaną nazwę IP, uprzednio przechowywaną w zmiennej $ipName.</span><span class="sxs-lookup"><span data-stu-id="9c461-141">The virtual machine has a reserved IP name, previously stored in the $ipName variable.</span></span>

## <span data-ttu-id="9c461-142">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9c461-142">PARAMETERS</span></span>

### <span data-ttu-id="9c461-143">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="9c461-143">-AdminUsername</span></span>
<span data-ttu-id="9c461-144">Określa nazwę użytkownika konta administratora, które to polecenie cmdlet tworzy na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c461-144">Specifies the user name of the Administrator account that this cmdlet creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c461-145">-AffinityGroup</span><span class="sxs-lookup"><span data-stu-id="9c461-145">-AffinityGroup</span></span>
<span data-ttu-id="9c461-146">Określa grupę koligacji dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c461-146">Specifies the affinity group for the virtual machine.</span></span>
<span data-ttu-id="9c461-147">Ten parametr lub parametr *Lokalizacja* można określić tylko wtedy, gdy to polecenie cmdlet utworzy usługę Azure dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c461-147">Specify this parameter or the *Location* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

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

### <span data-ttu-id="9c461-148">-AvailabilitySetName</span><span class="sxs-lookup"><span data-stu-id="9c461-148">-AvailabilitySetName</span></span>
<span data-ttu-id="9c461-149">Określa nazwę zestawu dostępności, w którym to polecenie cmdlet tworzy maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="9c461-149">Specifies the name of the availability set in which this cmdlet creates the virtual machine.</span></span>

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

### <span data-ttu-id="9c461-150">-Certificates</span><span class="sxs-lookup"><span data-stu-id="9c461-150">-Certificates</span></span>
<span data-ttu-id="9c461-151">Określa listę certyfikatów, których używa ten aplet polecenia w celu utworzenia usługi.</span><span class="sxs-lookup"><span data-stu-id="9c461-151">Specifies a list of certificates that this cmdlet uses to create the service.</span></span>

```yaml
Type: CertificateSettingList
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c461-152">-CustomDataFile</span><span class="sxs-lookup"><span data-stu-id="9c461-152">-CustomDataFile</span></span>
<span data-ttu-id="9c461-153">Określa plik danych dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c461-153">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="9c461-154">To polecenie cmdlet koduje zawartość pliku jako Base64.</span><span class="sxs-lookup"><span data-stu-id="9c461-154">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="9c461-155">Plik musi być mniejszy niż 64 kilobajtów.</span><span class="sxs-lookup"><span data-stu-id="9c461-155">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="9c461-156">Jeśli system operacyjny gościa to system operacyjny Windows, to polecenie cmdlet zapisuje te dane jako plik binarny o nazwie%SYSTEMDRIVE%\AzureData\CustomData.bin.</span><span class="sxs-lookup"><span data-stu-id="9c461-156">If the guest operating system is the Windows operating system, this cmdlet saves this data as a binary file that is named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="9c461-157">Jeśli system operacyjny gościa to Linux, to polecenie cmdlet przekazuje dane przy użyciu pliku ovf-env.xml.</span><span class="sxs-lookup"><span data-stu-id="9c461-157">If the guest operating system is Linux, this cmdlet passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="9c461-158">Program instalacyjny skopiuje ten plik do katalogu/var/lib/waagent.</span><span class="sxs-lookup"><span data-stu-id="9c461-158">Installation copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="9c461-159">Agent również przechowuje dane zakodowane w formacie base64 w/var/lib/waagent/CustomData.</span><span class="sxs-lookup"><span data-stu-id="9c461-159">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

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

### <span data-ttu-id="9c461-160">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="9c461-160">-DisableGuestAgent</span></span>
<span data-ttu-id="9c461-161">Wskazuje, że to polecenie cmdlet wyłącza infrastrukturę jako usługę IaaS (Agent gościa).</span><span class="sxs-lookup"><span data-stu-id="9c461-161">Indicates that this cmdlet disables the infrastructure as a service (IaaS) provision guest agent.</span></span>

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

### <span data-ttu-id="9c461-162">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="9c461-162">-DisableWinRMHttps</span></span>
<span data-ttu-id="9c461-163">Wskazuje, że to polecenie cmdlet wyłącza zdalne zarządzanie systemem Windows (WinRM) na protokole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9c461-163">Indicates that this cmdlet disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="9c461-164">Domyślnie usługa WinRM jest włączona przy użyciu protokołu HTTPS.</span><span class="sxs-lookup"><span data-stu-id="9c461-164">By default, WinRM is enabled over HTTPS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c461-165">-DnsSettings</span><span class="sxs-lookup"><span data-stu-id="9c461-165">-DnsSettings</span></span>
<span data-ttu-id="9c461-166">Określa tablicę obiektów serwera DNS definiujących ustawienia DNS nowego wdrożenia.</span><span class="sxs-lookup"><span data-stu-id="9c461-166">Specifies an array of DNS server objects that defines the DNS settings for the new deployment.</span></span>
<span data-ttu-id="9c461-167">Aby utworzyć obiekt **DnsServer** , użyj polecenia cmdlet **New-AzureDns** .</span><span class="sxs-lookup"><span data-stu-id="9c461-167">To create a **DnsServer** object, use the **New-AzureDns** cmdlet.</span></span>

```yaml
Type: DnsServer[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c461-168">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="9c461-168">-EnableWinRMHttp</span></span>
<span data-ttu-id="9c461-169">Wskazuje, że to polecenie cmdlet włącza usługę WinRM przez HTTP.</span><span class="sxs-lookup"><span data-stu-id="9c461-169">Indicates that this cmdlet enables WinRM over HTTP.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c461-170">-HostCaching</span><span class="sxs-lookup"><span data-stu-id="9c461-170">-HostCaching</span></span>
<span data-ttu-id="9c461-171">Określa tryb buforowania hosta dla dysku systemu operacyjnego.</span><span class="sxs-lookup"><span data-stu-id="9c461-171">Specifies the host caching mode for the operating system disk.</span></span>
<span data-ttu-id="9c461-172">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="9c461-172">Valid values are:</span></span> 

- <span data-ttu-id="9c461-173">Odczytu</span><span class="sxs-lookup"><span data-stu-id="9c461-173">ReadOnly</span></span>
- <span data-ttu-id="9c461-174">ReadWrite</span><span class="sxs-lookup"><span data-stu-id="9c461-174">ReadWrite</span></span>

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

### <span data-ttu-id="9c461-175">-ImageName</span><span class="sxs-lookup"><span data-stu-id="9c461-175">-ImageName</span></span>
<span data-ttu-id="9c461-176">Określa nazwę obrazu dysku, którego używa polecenie cmdlet do tworzenia dysku z systemem operacyjnym.</span><span class="sxs-lookup"><span data-stu-id="9c461-176">Specifies the name of the disk image this cmdlet uses to create the operating system disk.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c461-177">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="9c461-177">-InformationAction</span></span>
<span data-ttu-id="9c461-178">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="9c461-178">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="9c461-179">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="9c461-179">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9c461-180">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="9c461-180">Continue</span></span>
- <span data-ttu-id="9c461-181">Ignorować</span><span class="sxs-lookup"><span data-stu-id="9c461-181">Ignore</span></span>
- <span data-ttu-id="9c461-182">Inquire</span><span class="sxs-lookup"><span data-stu-id="9c461-182">Inquire</span></span>
- <span data-ttu-id="9c461-183">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="9c461-183">SilentlyContinue</span></span>
- <span data-ttu-id="9c461-184">Przestaw</span><span class="sxs-lookup"><span data-stu-id="9c461-184">Stop</span></span>
- <span data-ttu-id="9c461-185">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="9c461-185">Suspend</span></span>

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

### <span data-ttu-id="9c461-186">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="9c461-186">-InformationVariable</span></span>
<span data-ttu-id="9c461-187">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="9c461-187">Specifies an information variable.</span></span>

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

### <span data-ttu-id="9c461-188">-InstanceSize</span><span class="sxs-lookup"><span data-stu-id="9c461-188">-InstanceSize</span></span>
<span data-ttu-id="9c461-189">Określa rozmiar wystąpienia.</span><span class="sxs-lookup"><span data-stu-id="9c461-189">Specifies the size of the instance.</span></span>
<span data-ttu-id="9c461-190">Prawidłowe wartości:</span><span class="sxs-lookup"><span data-stu-id="9c461-190">Valid values are:</span></span> 

- <span data-ttu-id="9c461-191">ExtraSmall</span><span class="sxs-lookup"><span data-stu-id="9c461-191">ExtraSmall</span></span>
- <span data-ttu-id="9c461-192">Mała</span><span class="sxs-lookup"><span data-stu-id="9c461-192">Small</span></span>
- <span data-ttu-id="9c461-193">Pożywkę</span><span class="sxs-lookup"><span data-stu-id="9c461-193">Medium</span></span>
- <span data-ttu-id="9c461-194">Większej</span><span class="sxs-lookup"><span data-stu-id="9c461-194">Large</span></span>
- <span data-ttu-id="9c461-195">ExtraLarge</span><span class="sxs-lookup"><span data-stu-id="9c461-195">ExtraLarge</span></span>
- <span data-ttu-id="9c461-196">A5</span><span class="sxs-lookup"><span data-stu-id="9c461-196">A5</span></span>
- <span data-ttu-id="9c461-197">A6</span><span class="sxs-lookup"><span data-stu-id="9c461-197">A6</span></span>
- <span data-ttu-id="9c461-198">A7</span><span class="sxs-lookup"><span data-stu-id="9c461-198">A7</span></span>
- <span data-ttu-id="9c461-199">A8</span><span class="sxs-lookup"><span data-stu-id="9c461-199">A8</span></span>
- <span data-ttu-id="9c461-200">A9</span><span class="sxs-lookup"><span data-stu-id="9c461-200">A9</span></span>
- <span data-ttu-id="9c461-201">Basic_A0</span><span class="sxs-lookup"><span data-stu-id="9c461-201">Basic_A0</span></span>
- <span data-ttu-id="9c461-202">Basic_A1</span><span class="sxs-lookup"><span data-stu-id="9c461-202">Basic_A1</span></span>
- <span data-ttu-id="9c461-203">Basic_A2</span><span class="sxs-lookup"><span data-stu-id="9c461-203">Basic_A2</span></span>
- <span data-ttu-id="9c461-204">Basic_A3</span><span class="sxs-lookup"><span data-stu-id="9c461-204">Basic_A3</span></span>
- <span data-ttu-id="9c461-205">Basic_A4</span><span class="sxs-lookup"><span data-stu-id="9c461-205">Basic_A4</span></span>
- <span data-ttu-id="9c461-206">Standard_D1</span><span class="sxs-lookup"><span data-stu-id="9c461-206">Standard_D1</span></span>
- <span data-ttu-id="9c461-207">Standard_D2</span><span class="sxs-lookup"><span data-stu-id="9c461-207">Standard_D2</span></span>
- <span data-ttu-id="9c461-208">Standard_D3</span><span class="sxs-lookup"><span data-stu-id="9c461-208">Standard_D3</span></span>
- <span data-ttu-id="9c461-209">Standard_D4</span><span class="sxs-lookup"><span data-stu-id="9c461-209">Standard_D4</span></span>
- <span data-ttu-id="9c461-210">Standard_D11</span><span class="sxs-lookup"><span data-stu-id="9c461-210">Standard_D11</span></span>
- <span data-ttu-id="9c461-211">Standard_D12</span><span class="sxs-lookup"><span data-stu-id="9c461-211">Standard_D12</span></span>
- <span data-ttu-id="9c461-212">Standard_D13</span><span class="sxs-lookup"><span data-stu-id="9c461-212">Standard_D13</span></span>
- <span data-ttu-id="9c461-213">Standard_D14</span><span class="sxs-lookup"><span data-stu-id="9c461-213">Standard_D14</span></span>

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

### <span data-ttu-id="9c461-214">-Linux</span><span class="sxs-lookup"><span data-stu-id="9c461-214">-Linux</span></span>
<span data-ttu-id="9c461-215">Wskazuje, że to polecenie cmdlet tworzy maszynę wirtualną opartą na systemie Linux.</span><span class="sxs-lookup"><span data-stu-id="9c461-215">Indicates that this cmdlet creates a Linux based virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c461-216">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="9c461-216">-LinuxUser</span></span>
<span data-ttu-id="9c461-217">Określa nazwę użytkownika konta administracyjnego Linux, które to polecenie cmdlet tworzy na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c461-217">Specifies the user name of the Linux administrative account that this cmdlet creates on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c461-218">— Lokalizacja</span><span class="sxs-lookup"><span data-stu-id="9c461-218">-Location</span></span>
<span data-ttu-id="9c461-219">Określa platformę Azure Datacenter, na której znajduje się maszyna wirtualna.</span><span class="sxs-lookup"><span data-stu-id="9c461-219">Specifies the Azure datacenter that hosts the virtual machine.</span></span>
<span data-ttu-id="9c461-220">W przypadku określenia tego parametru polecenie cmdlet tworzy usługę platformy Azure w określonej lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="9c461-220">If you specify this parameter, the cmdlet creates an Azure service in the specified location.</span></span>
<span data-ttu-id="9c461-221">Ten parametr lub parametr *AffinityGroup* należy określić tylko wtedy, gdy to polecenie cmdlet utworzy usługę Azure dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c461-221">Specify this parameter or the *AffinityGroup* parameter only if this cmdlet creates an Azure service for the virtual machine.</span></span>

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

### <span data-ttu-id="9c461-222">-MediaLocation</span><span class="sxs-lookup"><span data-stu-id="9c461-222">-MediaLocation</span></span>
<span data-ttu-id="9c461-223">Określa lokalizację magazynu platformy Azure, w którym to polecenie cmdlet tworzy dyski maszyn wirtualnych.</span><span class="sxs-lookup"><span data-stu-id="9c461-223">Specifies the Azure Storage location where this cmdlet creates the virtual machines disks.</span></span>

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

### <span data-ttu-id="9c461-224">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9c461-224">-Name</span></span>
<span data-ttu-id="9c461-225">Określa nazwę maszyny wirtualnej, którą tworzy polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c461-225">Specifies the name of the virtual machine that this cmdlet creates.</span></span>

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

### <span data-ttu-id="9c461-226">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="9c461-226">-NoExportPrivateKey</span></span>
<span data-ttu-id="9c461-227">Wskazuje, że ta konfiguracja nie przekazuje klucza prywatnego.</span><span class="sxs-lookup"><span data-stu-id="9c461-227">Indicates that this configuration does not upload the private key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c461-228">-NoWinRMEndpoint</span><span class="sxs-lookup"><span data-stu-id="9c461-228">-NoWinRMEndpoint</span></span>
<span data-ttu-id="9c461-229">Wskazuje, że to polecenie cmdlet nie dodaje punktu końcowego WinRM do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c461-229">Indicates that this cmdlet does not add a WinRM endpoint for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c461-230">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="9c461-230">-Password</span></span>
<span data-ttu-id="9c461-231">Określa hasło dla konta administracyjnego.</span><span class="sxs-lookup"><span data-stu-id="9c461-231">Specifies the password for the administrative account.</span></span>

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

### <span data-ttu-id="9c461-232">-Profile</span><span class="sxs-lookup"><span data-stu-id="9c461-232">-Profile</span></span>
<span data-ttu-id="9c461-233">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9c461-233">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9c461-234">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="9c461-234">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9c461-235">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="9c461-235">-ReservedIPName</span></span>
<span data-ttu-id="9c461-236">Określa zastrzeżoną nazwę IP.</span><span class="sxs-lookup"><span data-stu-id="9c461-236">Specifies the reserved IP name.</span></span>

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

### <span data-ttu-id="9c461-237">-ReverseDnsFqdn</span><span class="sxs-lookup"><span data-stu-id="9c461-237">-ReverseDnsFqdn</span></span>
<span data-ttu-id="9c461-238">Określa w pełni kwalifikowaną nazwę domeny dla wyszukiwania wstecznego DNS.</span><span class="sxs-lookup"><span data-stu-id="9c461-238">Specifies the fully qualified domain name for reverse DNS look up.</span></span>

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

### <span data-ttu-id="9c461-239">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="9c461-239">-ServiceName</span></span>
<span data-ttu-id="9c461-240">Określa nazwę nowej lub istniejącej usługi platformy Azure, do której to polecenie cmdlet doda nową maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="9c461-240">Specifies the name of a new or existing Azure service to which this cmdlet adds the new virtual machine.</span></span>

<span data-ttu-id="9c461-241">Jeśli określisz nową usługę, to polecenie cmdlet tworzy je.</span><span class="sxs-lookup"><span data-stu-id="9c461-241">If you specify a new service, this cmdlets creates it.</span></span>
<span data-ttu-id="9c461-242">Aby utworzyć nową usługę, należy określić *lokalizację* lub parametr *AffinityGroup* .</span><span class="sxs-lookup"><span data-stu-id="9c461-242">To create a new service, you must specify the *Location* or *AffinityGroup* parameter.</span></span>

<span data-ttu-id="9c461-243">Jeśli określisz istniejącą usługę, nie określaj *lokalizacji* ani *AffinityGroup*.</span><span class="sxs-lookup"><span data-stu-id="9c461-243">If you specify an existing service, do not specify *Location* or *AffinityGroup*.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c461-244">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="9c461-244">-SSHKeyPairs</span></span>
<span data-ttu-id="9c461-245">Określa pary kluczy SSH.</span><span class="sxs-lookup"><span data-stu-id="9c461-245">Specifies SSH key pairs.</span></span>

```yaml
Type: SSHKeyPairList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c461-246">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="9c461-246">-SSHPublicKeys</span></span>
<span data-ttu-id="9c461-247">Określa klucze publiczne SSH.</span><span class="sxs-lookup"><span data-stu-id="9c461-247">Specifies SSH public keys.</span></span>

```yaml
Type: SSHPublicKeyList
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c461-248">-SubnetNames</span><span class="sxs-lookup"><span data-stu-id="9c461-248">-SubnetNames</span></span>
<span data-ttu-id="9c461-249">Określa tablicę nazw podsieci dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c461-249">Specifies an array of names of subnet for the virtual machine.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c461-250">-VNetName</span><span class="sxs-lookup"><span data-stu-id="9c461-250">-VNetName</span></span>
<span data-ttu-id="9c461-251">Określa nazwę sieci wirtualnej dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="9c461-251">Specifies the name of a virtual network for the virtual machine.</span></span>

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

### <span data-ttu-id="9c461-252">-WaitForBoot</span><span class="sxs-lookup"><span data-stu-id="9c461-252">-WaitForBoot</span></span>
<span data-ttu-id="9c461-253">Wskazuje, że to polecenie cmdlet oczekuje, że maszyna wirtualna będzie mieć dostęp do ReadyRole stanu.</span><span class="sxs-lookup"><span data-stu-id="9c461-253">Indicates that this cmdlet waits for the virtual machine to reach the state ReadyRole.</span></span>
<span data-ttu-id="9c461-254">Jeśli maszyna wirtualna osiągnie jedno z następujących stanów, polecenie cmdlet nie powiedzie się: FailedStartingVM, ProvisioningFailed lub ProvisioningTimeout.</span><span class="sxs-lookup"><span data-stu-id="9c461-254">If the virtual machine reaches one of the following states, the cmdlet fails: FailedStartingVM, ProvisioningFailed, or ProvisioningTimeout.</span></span>

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

### <span data-ttu-id="9c461-255">-Windows</span><span class="sxs-lookup"><span data-stu-id="9c461-255">-Windows</span></span>
<span data-ttu-id="9c461-256">Wskazuje, że w tym poleceniu cmdlet jest tworzona maszyna wirtualna systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="9c461-256">Indicates that this cmdlet creates a Windows virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c461-257">-WinRMCertificate</span><span class="sxs-lookup"><span data-stu-id="9c461-257">-WinRMCertificate</span></span>
<span data-ttu-id="9c461-258">Określa certyfikat, który jest skojarzony z tym poleceniem cmdlet do punktu końcowego usługi WinRM.</span><span class="sxs-lookup"><span data-stu-id="9c461-258">Specifies a certificate that this cmdlet associates to a WinRM endpoint.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c461-259">-X509</span><span class="sxs-lookup"><span data-stu-id="9c461-259">-X509Certificates</span></span>
<span data-ttu-id="9c461-260">Określa tablicę certyfikatów x509, które są wdrażane w usłudze hostowanej.</span><span class="sxs-lookup"><span data-stu-id="9c461-260">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9c461-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c461-261">CommonParameters</span></span>
<span data-ttu-id="9c461-262">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9c461-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c461-263">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c461-263">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c461-264">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9c461-264">INPUTS</span></span>

## <span data-ttu-id="9c461-265">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9c461-265">OUTPUTS</span></span>

## <span data-ttu-id="9c461-266">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9c461-266">NOTES</span></span>

## <span data-ttu-id="9c461-267">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9c461-267">RELATED LINKS</span></span>

[<span data-ttu-id="9c461-268">Get-AzureLocation</span><span class="sxs-lookup"><span data-stu-id="9c461-268">Get-AzureLocation</span></span>](./Get-AzureLocation.md)

[<span data-ttu-id="9c461-269">Get-AzureVMImage</span><span class="sxs-lookup"><span data-stu-id="9c461-269">Get-AzureVMImage</span></span>](./Get-AzureVMImage.md)

[<span data-ttu-id="9c461-270">Nowe — AzureDns</span><span class="sxs-lookup"><span data-stu-id="9c461-270">New-AzureDns</span></span>](./New-AzureDns.md)


