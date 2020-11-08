---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 0B3EF123-8424-4CCA-95E8-01301B70CBDC
online version: ''
schema: 2.0.0
ms.openlocfilehash: f84db81f51a4f8d0da605917f99e14c1721cd89d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055348"
---
# <span data-ttu-id="2ff59-101">Add-AzureProvisioningConfig</span><span class="sxs-lookup"><span data-stu-id="2ff59-101">Add-AzureProvisioningConfig</span></span>

## <span data-ttu-id="2ff59-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2ff59-102">SYNOPSIS</span></span>
<span data-ttu-id="2ff59-103">Dodaje konfigurację inicjowania obsługi maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2ff59-103">Adds provisioning configuration for an Azure virtual machine.</span></span>

## <span data-ttu-id="2ff59-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2ff59-104">SYNTAX</span></span>

### <span data-ttu-id="2ff59-105">Windows (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="2ff59-105">Windows (Default)</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>] [-Windows]
 [-AdminUsername <String>] [-Password <String>] [-ResetPasswordOnFirstLogon] [-DisableAutomaticUpdates]
 [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>] [-EnableWinRMHttp]
 [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>] [-X509Certificates <X509Certificate2[]>]
 [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2ff59-106">Linux</span><span class="sxs-lookup"><span data-stu-id="2ff59-106">Linux</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-Linux] [-LinuxUser <String>]
 [-DisableSSH] [-NoSSHEndpoint] [-NoSSHPassword] [-SSHPublicKeys <SSHPublicKeyList>]
 [-SSHKeyPairs <SSHKeyPairList>] [-CustomDataFile <String>] [-Password <String>] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="2ff59-107">WindowsDomain</span><span class="sxs-lookup"><span data-stu-id="2ff59-107">WindowsDomain</span></span>
```
Add-AzureProvisioningConfig -VM <IPersistentVM> [-DisableGuestAgent] [-CustomDataFile <String>]
 -AdminUsername <String> [-WindowsDomain] [-Password <String>] [-ResetPasswordOnFirstLogon]
 [-DisableAutomaticUpdates] [-NoRDPEndpoint] [-TimeZone <String>] [-Certificates <CertificateSettingList>]
 -JoinDomain <String> -Domain <String> -DomainUserName <String> -DomainPassword <String>
 [-MachineObjectOU <String>] [-EnableWinRMHttp] [-DisableWinRMHttps] [-WinRMCertificate <X509Certificate2>]
 [-X509Certificates <X509Certificate2[]>] [-NoExportPrivateKey] [-NoWinRMEndpoint] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="2ff59-108">Opis</span><span class="sxs-lookup"><span data-stu-id="2ff59-108">DESCRIPTION</span></span>
<span data-ttu-id="2ff59-109">Polecenie cmdlet **Add-AzureProvisioningConfig** umożliwia dodanie informacji o konfiguracji inicjowania obsługi do konfiguracji maszyny wirtualnej platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="2ff59-109">The **Add-AzureProvisioningConfig** cmdlet adds provisioning configuration information to an Azure virtual machine configuration.</span></span>
<span data-ttu-id="2ff59-110">Za pomocą obiektu konfiguracji można utworzyć maszynę wirtualną.</span><span class="sxs-lookup"><span data-stu-id="2ff59-110">You can use the configuration object to create a virtual machine.</span></span>

<span data-ttu-id="2ff59-111">To polecenie cmdlet obsługuje różne konfiguracje obsługi, w tym autonomiczne serwery z systemem Windows, serwery systemu Windows połączone z domeną usługi Active Directory oraz serwery z systemem Linux.</span><span class="sxs-lookup"><span data-stu-id="2ff59-111">This cmdlet supports different provisioning configurations, including standalone Windows servers, Windows servers joined to an Active Directory domain, and Linux-based servers.</span></span>

<span data-ttu-id="2ff59-112">Aby utworzyć serwer przyłączony domeny usługi Active Directory, określ w pełni kwalifikowaną nazwę domeny domeny usługi Active Directory oraz poświadczenia domeny użytkownika, który ma uprawnienia do dołączania do maszyny wirtualnej w domenie.</span><span class="sxs-lookup"><span data-stu-id="2ff59-112">To create an Active Directory domain joined server, specify the fully qualified domain name of the Active Directory domain and the domain credentials of a user who has permission to join the virtual machine to the domain.</span></span>

## <span data-ttu-id="2ff59-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2ff59-113">EXAMPLES</span></span>

### <span data-ttu-id="2ff59-114">Przykład 1. Tworzenie autonomicznej maszyny wirtualnej</span><span class="sxs-lookup"><span data-stu-id="2ff59-114">Example 1: Create a standalone virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="2ff59-115">To polecenie tworzy obiekt konfiguracji maszyny wirtualnej przy użyciu polecenia cmdlet **New-AzureVMConfig** .</span><span class="sxs-lookup"><span data-stu-id="2ff59-115">This command creates a virtual machine configuration object by using the **New-AzureVMConfig** cmdlet.</span></span>
<span data-ttu-id="2ff59-116">Polecenie przekazuje ten obiekt do bieżącego polecenia cmdlet za pomocą operatora potoku.</span><span class="sxs-lookup"><span data-stu-id="2ff59-116">The command passes that object to the current cmdlet by using the pipeline operator.</span></span>
<span data-ttu-id="2ff59-117">Bieżące polecenie cmdlet umożliwia dodanie konfiguracji inicjowania obsługi dla maszyny wirtualnej z uruchomionym systemem operacyjnym Windows.</span><span class="sxs-lookup"><span data-stu-id="2ff59-117">The current cmdlet adds provisioning configuration for a virtual machine that runs the Windows operating system.</span></span>
<span data-ttu-id="2ff59-118">Konfiguracja obejmuje nazwę użytkownika i hasło administratora.</span><span class="sxs-lookup"><span data-stu-id="2ff59-118">The configuration includes the administrator user name and password.</span></span>
<span data-ttu-id="2ff59-119">Polecenie przekazanie konfiguracji do polecenia cmdlet **New-AzureVM** , które powoduje utworzenie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2ff59-119">The command passes the configuration to the **New-AzureVM** cmdlet, which creates the virtual machine.</span></span>

### <span data-ttu-id="2ff59-120">Przykład 2: Tworzenie maszyny wirtualnej przyłączonego do domeny</span><span class="sxs-lookup"><span data-stu-id="2ff59-120">Example 2: Create a domain joined virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "DomainVM" -InstanceSize Small -ImageName "Image09" | Add-AzureProvisioningConfig -WindowsDomain -Password "password" -AdminUsername "AdminMain" -ResetPasswordOnFirstLogon -JoinDomain "contoso.com" -Domain "contoso" -DomainUserName "DomainAdminUser" -DomainPassword "DomainPassword" -MachineObjectOU 'OU=AzureVMs,DC=contoso,DC=com' | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="2ff59-121">To polecenie tworzy obiekt konfiguracji maszyny wirtualnej, a następnie przekazuje go do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ff59-121">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="2ff59-122">Bieżące polecenie cmdlet umożliwia dodanie konfiguracji inicjowania obsługi maszyny wirtualnej w celu dołączenia jej do domeny contoso.</span><span class="sxs-lookup"><span data-stu-id="2ff59-122">The current cmdlet adds provisioning configuration for a virtual machine to be joined with the contoso domain.</span></span>
<span data-ttu-id="2ff59-123">Polecenie zawiera nazwę użytkownika i hasło potrzebne do przyłączenia maszyny wirtualnej do domeny.</span><span class="sxs-lookup"><span data-stu-id="2ff59-123">The command includes user name and password necessary to join the virtual machine to the domain.</span></span>
<span data-ttu-id="2ff59-124">Konfiguracja wymaga, aby użytkownik zmienił hasło użytkownika przy pierwszym logowaniu.</span><span class="sxs-lookup"><span data-stu-id="2ff59-124">The configuration requires the user to change the user password at the first logon.</span></span>
<span data-ttu-id="2ff59-125">Polecenie tworzy maszynę wirtualną na podstawie obiektu inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="2ff59-125">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="2ff59-126">Przykład 3: Tworzenie maszyny wirtualnej opartej na systemie Linux</span><span class="sxs-lookup"><span data-stu-id="2ff59-126">Example 3: Create a Linux-based virtual machine</span></span>
```
PS C:\> New-AzureVMConfig -Name "LinuxVM" -InstanceSize Small -ImageName "LinuxImage03" | Add-AzureProvisioningConfig -Linux -LinuxUser "LinuxRoot" -Password "password" | New-AzureVM -ServiceName "ContosoService"
```

<span data-ttu-id="2ff59-127">To polecenie tworzy obiekt konfiguracji maszyny wirtualnej, a następnie przekazuje go do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ff59-127">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="2ff59-128">Bieżące polecenie cmdlet umożliwia dodanie konfiguracji inicjowania obsługi dla maszyny wirtualnej, na której jest uruchomiony system operacyjny Linux.</span><span class="sxs-lookup"><span data-stu-id="2ff59-128">The current cmdlet adds provisioning configuration for a virtual machine that runs the Linux operating system.</span></span>
<span data-ttu-id="2ff59-129">Konfiguracja obejmuje główną nazwę użytkownika i hasło.</span><span class="sxs-lookup"><span data-stu-id="2ff59-129">The configuration includes the root user name and password.</span></span>
<span data-ttu-id="2ff59-130">Polecenie tworzy maszynę wirtualną na podstawie obiektu inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="2ff59-130">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="2ff59-131">Przykład 4: Tworzenie maszyny wirtualnej zawierającej certyfikaty dla usługi WinRM</span><span class="sxs-lookup"><span data-stu-id="2ff59-131">Example 4: Create a virtual machine that includes certificates for WinRM</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image11" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -WinRMCertificate $certs[0] -X509Certificates $certs[1], $certs[2] | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="2ff59-132">Pierwsze polecenie pobiera certyfikaty z magazynu certyfikatów, a następnie zapisuje je w zmiennej tablicowej $certs.</span><span class="sxs-lookup"><span data-stu-id="2ff59-132">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="2ff59-133">Drugie polecenie tworzy obiekt konfiguracji maszyny wirtualnej, a następnie przekazuje go do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ff59-133">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="2ff59-134">Bieżące polecenie cmdlet umożliwia dodanie konfiguracji inicjowania obsługi, zawierającej certyfikaty dla usługi WinRM.</span><span class="sxs-lookup"><span data-stu-id="2ff59-134">The current cmdlet adds provisioning configuration that includes certificates for WinRM.</span></span>
<span data-ttu-id="2ff59-135">Polecenie tworzy maszynę wirtualną na podstawie obiektu inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="2ff59-135">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="2ff59-136">Przykład 5: Tworzenie maszyny wirtualnej z obsługą usługi WinRM za pośrednictwem protokołu HTTP</span><span class="sxs-lookup"><span data-stu-id="2ff59-136">Example 5: Create a virtual machine that has WinRM enabled over HTTP</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image14" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -EnableWinRMHttp | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="2ff59-137">To polecenie tworzy obiekt konfiguracji maszyny wirtualnej, a następnie przekazuje go do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ff59-137">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="2ff59-138">Bieżące polecenie cmdlet umożliwia dodanie konfiguracji inicjowania obsługi z obsługą usługi WinRM za pośrednictwem protokołu HTTP.</span><span class="sxs-lookup"><span data-stu-id="2ff59-138">The current cmdlet adds provisioning configuration that has WinRM enabled over HTTP.</span></span>
<span data-ttu-id="2ff59-139">Polecenie tworzy maszynę wirtualną na podstawie obiektu inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="2ff59-139">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="2ff59-140">Przykład 6: Tworzenie maszyny wirtualnej z wyłączonym WinRM w usłudze HTTPS</span><span class="sxs-lookup"><span data-stu-id="2ff59-140">Example 6: Create a virtual machine that has WinRM disabled over HTTPS</span></span>
```
PS C:\> New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -DisableWinRMHttps | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="2ff59-141">To polecenie tworzy obiekt konfiguracji maszyny wirtualnej, a następnie przekazuje go do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ff59-141">This command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="2ff59-142">Bieżące polecenie cmdlet umożliwia dodanie konfiguracji inicjowania obsługi, która wyłącza usługę WinRM przez HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2ff59-142">The current cmdlet adds provisioning configuration that disables WinRM over HTTPS.</span></span>
<span data-ttu-id="2ff59-143">Polecenie tworzy maszynę wirtualną na podstawie obiektu inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="2ff59-143">The command creates the virtual machine based on the provisioning object.</span></span>

### <span data-ttu-id="2ff59-144">Przykład 7: Tworzenie maszyny wirtualnej bez eksportowania kluczy</span><span class="sxs-lookup"><span data-stu-id="2ff59-144">Example 7: Create a virtual machine with no key export</span></span>
```
PS C:\> $certs = Get-ChildItem Cert:\CurrentUser\My
New-AzureVMConfig -Name "NonDomainVM" -InstanceSize Small -ImageName "Image07" | Add-AzureProvisioningConfig -Windows -Password "password" -AdminUsername "AdminMain" -X509Certificates $certs[0], $certs[1] -NoExportPrivateKey | New-AzureVM -ServiceName "ContosoService" -WaitForBoot
```

<span data-ttu-id="2ff59-145">Pierwsze polecenie pobiera certyfikaty z magazynu certyfikatów, a następnie zapisuje je w zmiennej tablicowej $certs.</span><span class="sxs-lookup"><span data-stu-id="2ff59-145">The first command gets certificates from a certificate store, and then stores them in the $certs array variable.</span></span>

<span data-ttu-id="2ff59-146">Drugie polecenie tworzy obiekt konfiguracji maszyny wirtualnej, a następnie przekazuje go do bieżącego polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ff59-146">The second command creates a virtual machine configuration object, and then passes it to the current cmdlet.</span></span>
<span data-ttu-id="2ff59-147">Bieżące polecenie cmdlet umożliwia dodanie konfiguracji inicjowania obsługi dla maszyny wirtualnej zawierającej certyfikaty i nie powoduje wyeksportowania kluczy prywatnych.</span><span class="sxs-lookup"><span data-stu-id="2ff59-147">The current cmdlet adds provisioning configuration for a virtual machine that includes certificates and does not export private keys.</span></span>
<span data-ttu-id="2ff59-148">Polecenie tworzy maszynę wirtualną na podstawie obiektu inicjowania obsługi.</span><span class="sxs-lookup"><span data-stu-id="2ff59-148">The command creates the virtual machine based on the provisioning object.</span></span>

## <span data-ttu-id="2ff59-149">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2ff59-149">PARAMETERS</span></span>

### <span data-ttu-id="2ff59-150">-AdminUsername</span><span class="sxs-lookup"><span data-stu-id="2ff59-150">-AdminUsername</span></span>
<span data-ttu-id="2ff59-151">Określa nazwę użytkownika konta administratora, którą tworzy ta konfiguracja na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2ff59-151">Specifies the user name of the Administrator account that this configuration creates on the virtual machine.</span></span>

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

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-152">-Certificates</span><span class="sxs-lookup"><span data-stu-id="2ff59-152">-Certificates</span></span>
<span data-ttu-id="2ff59-153">Określa zestaw certyfikatów, które są instalowane w ramach tej konfiguracji na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2ff59-153">Specifies a set of certificates that this configuration installs on the virtual machine.</span></span>

```yaml
Type: CertificateSettingList
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-154">-CustomDataFile</span><span class="sxs-lookup"><span data-stu-id="2ff59-154">-CustomDataFile</span></span>
<span data-ttu-id="2ff59-155">Określa plik danych dla maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2ff59-155">Specifies a data file for the virtual machine.</span></span>
<span data-ttu-id="2ff59-156">To polecenie cmdlet koduje zawartość pliku jako Base64.</span><span class="sxs-lookup"><span data-stu-id="2ff59-156">This cmdlet encodes the contents of the file as Base64.</span></span>
<span data-ttu-id="2ff59-157">Plik musi być mniejszy niż 64 kilobajtów.</span><span class="sxs-lookup"><span data-stu-id="2ff59-157">The file must be less than 64 kilobytes long.</span></span>

<span data-ttu-id="2ff59-158">Jeśli system operacyjny gościa to system operacyjny Windows, ta konfiguracja zapisuje te dane jako plik binarny o nazwie%SYSTEMDRIVE%\AzureData\CustomData.bin.</span><span class="sxs-lookup"><span data-stu-id="2ff59-158">If the guest operating system is the Windows operating system, this configuration saves this data as a binary file named %SYSTEMDRIVE%\AzureData\CustomData.bin.</span></span>

<span data-ttu-id="2ff59-159">Jeśli system operacyjny gościa to Linux, ta konfiguracja przekazuje dane przy użyciu pliku ovf-env.xml.</span><span class="sxs-lookup"><span data-stu-id="2ff59-159">If the guest operating system is Linux, this configuration passes the data by using the ovf-env.xml file.</span></span>
<span data-ttu-id="2ff59-160">Konfiguracja kopiuje ten plik do katalogu/var/lib/waagent.</span><span class="sxs-lookup"><span data-stu-id="2ff59-160">Configuration copies that file to the /var/lib/waagent directory.</span></span>
<span data-ttu-id="2ff59-161">Agent również przechowuje dane zakodowane w formacie base64 w/var/lib/waagent/CustomData.</span><span class="sxs-lookup"><span data-stu-id="2ff59-161">The agent also stores the Base64 encoded data in /var/lib/waagent/CustomData.</span></span>

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

### <span data-ttu-id="2ff59-162">-DisableAutomaticUpdates</span><span class="sxs-lookup"><span data-stu-id="2ff59-162">-DisableAutomaticUpdates</span></span>
<span data-ttu-id="2ff59-163">Wskazuje, że ta konfiguracja wyłącza aktualizacje automatyczne.</span><span class="sxs-lookup"><span data-stu-id="2ff59-163">Indicates that this configuration disables automatic updates.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-164">-DisableGuestAgent</span><span class="sxs-lookup"><span data-stu-id="2ff59-164">-DisableGuestAgent</span></span>
<span data-ttu-id="2ff59-165">Wskazuje, że ta konfiguracja wyłącza infrastrukturę jako agenta gościa usługi (IaaS).</span><span class="sxs-lookup"><span data-stu-id="2ff59-165">Indicates that this configuration disables the infrastructure as a service (IaaS) guest agent.</span></span>

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

### <span data-ttu-id="2ff59-166">-DisableSSH</span><span class="sxs-lookup"><span data-stu-id="2ff59-166">-DisableSSH</span></span>
<span data-ttu-id="2ff59-167">Wskazuje, że ta konfiguracja wyłącza SSH.</span><span class="sxs-lookup"><span data-stu-id="2ff59-167">Indicates that this configuration disables SSH.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-168">-DisableWinRMHttps</span><span class="sxs-lookup"><span data-stu-id="2ff59-168">-DisableWinRMHttps</span></span>
<span data-ttu-id="2ff59-169">Wskazuje, że ta konfiguracja wyłącza usługę Windows Remote Management (WinRM) w protokole HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2ff59-169">Indicates that this configuration disables Windows Remote Management (WinRM) on HTTPS.</span></span>
<span data-ttu-id="2ff59-170">Domyślnie usługa WinRM jest włączona przy użyciu protokołu HTTPS.</span><span class="sxs-lookup"><span data-stu-id="2ff59-170">By default, WinRM is enabled over HTTPS.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-171">-Domain</span><span class="sxs-lookup"><span data-stu-id="2ff59-171">-Domain</span></span>
<span data-ttu-id="2ff59-172">Określa nazwę domeny konta, która ma uprawnienia do dodawania komputera do domeny.</span><span class="sxs-lookup"><span data-stu-id="2ff59-172">Specifies the name of the domain of the account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-173">-DomainPassword</span><span class="sxs-lookup"><span data-stu-id="2ff59-173">-DomainPassword</span></span>
<span data-ttu-id="2ff59-174">Określa hasło konta użytkownika, które ma uprawnienia do dodawania komputera do domeny.</span><span class="sxs-lookup"><span data-stu-id="2ff59-174">Specifies the password of the user account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-175">-DomainUserName</span><span class="sxs-lookup"><span data-stu-id="2ff59-175">-DomainUserName</span></span>
<span data-ttu-id="2ff59-176">Określa nazwę konta użytkownika, które ma uprawnienia do dodawania komputera do domeny.</span><span class="sxs-lookup"><span data-stu-id="2ff59-176">Specifies the name of the user account that has permission to add the computer to a domain.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-177">-EnableWinRMHttp</span><span class="sxs-lookup"><span data-stu-id="2ff59-177">-EnableWinRMHttp</span></span>
<span data-ttu-id="2ff59-178">Wskazuje, że ta konfiguracja włącza usługę WinRM przez HTTP.</span><span class="sxs-lookup"><span data-stu-id="2ff59-178">Indicates that this configuration enables WinRM over HTTP.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-179">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="2ff59-179">-InformationAction</span></span>
<span data-ttu-id="2ff59-180">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="2ff59-180">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="2ff59-181">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2ff59-181">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2ff59-182">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="2ff59-182">Continue</span></span>
- <span data-ttu-id="2ff59-183">Ignorować</span><span class="sxs-lookup"><span data-stu-id="2ff59-183">Ignore</span></span>
- <span data-ttu-id="2ff59-184">Inquire</span><span class="sxs-lookup"><span data-stu-id="2ff59-184">Inquire</span></span>
- <span data-ttu-id="2ff59-185">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="2ff59-185">SilentlyContinue</span></span>
- <span data-ttu-id="2ff59-186">Przestaw</span><span class="sxs-lookup"><span data-stu-id="2ff59-186">Stop</span></span>
- <span data-ttu-id="2ff59-187">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="2ff59-187">Suspend</span></span>

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

### <span data-ttu-id="2ff59-188">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="2ff59-188">-InformationVariable</span></span>
<span data-ttu-id="2ff59-189">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="2ff59-189">Specifies an information variable.</span></span>

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

### <span data-ttu-id="2ff59-190">-JoinDomain</span><span class="sxs-lookup"><span data-stu-id="2ff59-190">-JoinDomain</span></span>
<span data-ttu-id="2ff59-191">Określa w pełni kwalifikowaną nazwę domeny (FQDN) domeny, do której należy dołączyć.</span><span class="sxs-lookup"><span data-stu-id="2ff59-191">Specifies the fully qualified domain name (FQDN) of the domain to join.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-192">-Linux</span><span class="sxs-lookup"><span data-stu-id="2ff59-192">-Linux</span></span>
<span data-ttu-id="2ff59-193">Wskazuje, że w tej konfiguracji jest tworzona konfiguracja systemu Linux.</span><span class="sxs-lookup"><span data-stu-id="2ff59-193">Indicates that this configuration creates a Linux configuration.</span></span>

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

### <span data-ttu-id="2ff59-194">-LinuxUser</span><span class="sxs-lookup"><span data-stu-id="2ff59-194">-LinuxUser</span></span>
<span data-ttu-id="2ff59-195">Określa nazwę użytkownika konta administracyjnego systemu Linux, którą ta konfiguracja tworzy na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2ff59-195">Specifies the user name of the Linux administrative account that this configuration creates on the virtual machine.</span></span>

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

### <span data-ttu-id="2ff59-196">-MachineObjectOU</span><span class="sxs-lookup"><span data-stu-id="2ff59-196">-MachineObjectOU</span></span>
<span data-ttu-id="2ff59-197">Określa w pełni kwalifikowaną nazwę jednostki organizacyjnej, w której konfiguracja tworzy konto komputera.</span><span class="sxs-lookup"><span data-stu-id="2ff59-197">Specifies the fully qualified name of the organizational unit (OU) in which the configuration creates the computer account.</span></span>

```yaml
Type: String
Parameter Sets: WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-198">-NoExportPrivateKey</span><span class="sxs-lookup"><span data-stu-id="2ff59-198">-NoExportPrivateKey</span></span>
<span data-ttu-id="2ff59-199">Wskazuje, że ta konfiguracja nie przekazuje klucza prywatnego.</span><span class="sxs-lookup"><span data-stu-id="2ff59-199">Indicates that this configuration does not upload the private key.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-200">-NoRDPEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ff59-200">-NoRDPEndpoint</span></span>
<span data-ttu-id="2ff59-201">Wskazuje, że ta konfiguracja służy do tworzenia maszyny wirtualnej bez punktu końcowego pulpitu zdalnego.</span><span class="sxs-lookup"><span data-stu-id="2ff59-201">Indicates that this configuration creates a virtual machine without a remote desktop endpoint.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-202">-NoSSHEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ff59-202">-NoSSHEndpoint</span></span>
<span data-ttu-id="2ff59-203">Wskazuje, że ta konfiguracja służy do tworzenia maszyny wirtualnej bez punktu końcowego SSH.</span><span class="sxs-lookup"><span data-stu-id="2ff59-203">Indicates that this configuration creates a virtual machine without an SSH endpoint.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-204">-NoSSHPassword</span><span class="sxs-lookup"><span data-stu-id="2ff59-204">-NoSSHPassword</span></span>
<span data-ttu-id="2ff59-205">Wskazuje, że ta konfiguracja umożliwia utworzenie maszyny wirtualnej bez hasła SSH.</span><span class="sxs-lookup"><span data-stu-id="2ff59-205">Indicates that this configuration creates a virtual machine without an SSH password.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Linux
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-206">-NoWinRMEndpoint</span><span class="sxs-lookup"><span data-stu-id="2ff59-206">-NoWinRMEndpoint</span></span>
<span data-ttu-id="2ff59-207">Wskazuje, że ta konfiguracja nie powoduje dodania punktu końcowego usługi WinRM do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2ff59-207">Indicates that this configuration does not add a WinRM endpoint for the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-208">-Password (hasło)</span><span class="sxs-lookup"><span data-stu-id="2ff59-208">-Password</span></span>
<span data-ttu-id="2ff59-209">Określa hasło konta administratora.</span><span class="sxs-lookup"><span data-stu-id="2ff59-209">Specifies the password of the administrator account.</span></span>

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

### <span data-ttu-id="2ff59-210">-Profile</span><span class="sxs-lookup"><span data-stu-id="2ff59-210">-Profile</span></span>
<span data-ttu-id="2ff59-211">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2ff59-211">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="2ff59-212">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="2ff59-212">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="2ff59-213">-ResetPasswordOnFirstLogon</span><span class="sxs-lookup"><span data-stu-id="2ff59-213">-ResetPasswordOnFirstLogon</span></span>
<span data-ttu-id="2ff59-214">Wskazuje, że maszyna wirtualna wymaga od użytkownika zmiany hasła przy pierwszym logowaniu.</span><span class="sxs-lookup"><span data-stu-id="2ff59-214">Indicates that the virtual machine requires the user to change the password at the first logon.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-215">-SSHKeyPairs</span><span class="sxs-lookup"><span data-stu-id="2ff59-215">-SSHKeyPairs</span></span>
<span data-ttu-id="2ff59-216">Określa pary kluczy SSH.</span><span class="sxs-lookup"><span data-stu-id="2ff59-216">Specifies SSH key pairs.</span></span>

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

### <span data-ttu-id="2ff59-217">-SSHPublicKeys</span><span class="sxs-lookup"><span data-stu-id="2ff59-217">-SSHPublicKeys</span></span>
<span data-ttu-id="2ff59-218">Określa klucze publiczne SSH.</span><span class="sxs-lookup"><span data-stu-id="2ff59-218">Specifies SSH public keys.</span></span>

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

### <span data-ttu-id="2ff59-219">-TimeZone</span><span class="sxs-lookup"><span data-stu-id="2ff59-219">-TimeZone</span></span>
<span data-ttu-id="2ff59-220">Określa strefę czasową dla maszyny wirtualnej, na przykład Pacyficzny czas standardowy lub Kanada (środkowy czas standardowy).</span><span class="sxs-lookup"><span data-stu-id="2ff59-220">Specifies the time zone for the virtual machine, for example, Pacific Standard Time or Canada Central Standard Time.</span></span>

```yaml
Type: String
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-221">-VM</span><span class="sxs-lookup"><span data-stu-id="2ff59-221">-VM</span></span>
<span data-ttu-id="2ff59-222">Określa obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="2ff59-222">Specifies a virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-223">-Windows</span><span class="sxs-lookup"><span data-stu-id="2ff59-223">-Windows</span></span>
<span data-ttu-id="2ff59-224">Wskazuje, że w tej konfiguracji jest tworzona autonomiczna maszyna wirtualna z uruchomionym systemem operacyjnym Windows.</span><span class="sxs-lookup"><span data-stu-id="2ff59-224">Indicates that this configuration creates a standalone virtual machine that runs the Windows operating system.</span></span>

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

### <span data-ttu-id="2ff59-225">-WindowsDomain</span><span class="sxs-lookup"><span data-stu-id="2ff59-225">-WindowsDomain</span></span>
<span data-ttu-id="2ff59-226">Wskazuje, że w tej konfiguracji jest tworzony system Windows Server dołączony do domeny usługi Active Directory.</span><span class="sxs-lookup"><span data-stu-id="2ff59-226">Indicates that this configuration creates Windows server that is joined to an Active Directory domain.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WindowsDomain
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-227">-WinRMCertificate</span><span class="sxs-lookup"><span data-stu-id="2ff59-227">-WinRMCertificate</span></span>
<span data-ttu-id="2ff59-228">Określa certyfikat, który jest skojarzony z tą konfiguracją do punktu końcowego usługi WinRM.</span><span class="sxs-lookup"><span data-stu-id="2ff59-228">Specifies a certificate that this configuration associates to a WinRM endpoint.</span></span>

```yaml
Type: X509Certificate2
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-229">-X509</span><span class="sxs-lookup"><span data-stu-id="2ff59-229">-X509Certificates</span></span>
<span data-ttu-id="2ff59-230">Określa tablicę certyfikatów x509, które są wdrażane w usłudze hostowanej.</span><span class="sxs-lookup"><span data-stu-id="2ff59-230">Specifies an array of X509 certificates that are deployed to a hosted service.</span></span>

```yaml
Type: X509Certificate2[]
Parameter Sets: Windows, WindowsDomain
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ff59-231">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ff59-231">CommonParameters</span></span>
<span data-ttu-id="2ff59-232">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2ff59-232">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ff59-233">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2ff59-233">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ff59-234">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2ff59-234">INPUTS</span></span>

## <span data-ttu-id="2ff59-235">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2ff59-235">OUTPUTS</span></span>

## <span data-ttu-id="2ff59-236">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2ff59-236">NOTES</span></span>

## <span data-ttu-id="2ff59-237">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2ff59-237">RELATED LINKS</span></span>

[<span data-ttu-id="2ff59-238">Nowe — AzureVM</span><span class="sxs-lookup"><span data-stu-id="2ff59-238">New-AzureVM</span></span>](./New-AzureVM.md)

[<span data-ttu-id="2ff59-239">Nowe — AzureVMConfig</span><span class="sxs-lookup"><span data-stu-id="2ff59-239">New-AzureVMConfig</span></span>](./New-AzureVMConfig.md)


