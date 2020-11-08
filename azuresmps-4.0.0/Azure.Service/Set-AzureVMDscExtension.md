---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 649D0A6C-77CE-4E49-AFF8-DF70ABE9FA13
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4bb63ff2ffecc3cab8c7d227d10afdd8374dde2a
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061821"
---
# <span data-ttu-id="ae7d8-101">Set-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ae7d8-101">Set-AzureVMDscExtension</span></span>

## <span data-ttu-id="ae7d8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ae7d8-102">SYNOPSIS</span></span>
<span data-ttu-id="ae7d8-103">Konfiguruje rozszerzenie DSC na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-103">Configures the DSC extension on a virtual machine.</span></span>

## <span data-ttu-id="ae7d8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ae7d8-104">SYNTAX</span></span>

```
Set-AzureVMDscExtension [-ReferenceName <String>] [-ConfigurationArgument <Hashtable>]
 [-ConfigurationDataPath <String>] [-ConfigurationArchive] <String> [-ConfigurationName <String>]
 [-ContainerName <String>] [-Force] [-StorageContext <AzureStorageContext>] [-Version <String>]
 [-StorageEndpointSuffix <String>] [-WmfVersion <String>] [-DataCollection <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae7d8-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ae7d8-105">DESCRIPTION</span></span>
<span data-ttu-id="ae7d8-106">Polecenie cmdlet **Set-AzureVMDscExtension** Konfigurowanie żądanego rozszerzenia konfiguracji stanu (DSC) na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-106">The **Set-AzureVMDscExtension** cmdlet configures the Desired State Configuration (DSC) extension on a virtual machine.</span></span>

## <span data-ttu-id="ae7d8-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ae7d8-107">EXAMPLES</span></span>

### <span data-ttu-id="ae7d8-108">Przykład 1: Konfigurowanie rozszerzenia DSC na maszynie wirtualnej</span><span class="sxs-lookup"><span data-stu-id="ae7d8-108">Example 1: Configure the DSC extension on a virtual machine</span></span>
```
PS C:\> Set-AzureVMDscExtension -VM $VM -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Path = 'C:\MyDirectory' }
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Contoso.Compute.BGInfo}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd6
OperationStatus             : OK
```

<span data-ttu-id="ae7d8-109">To polecenie umożliwia skonfigurowanie rozszerzenia DSC na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-109">This command configures the DSC extension on a virtual machine.</span></span>

<span data-ttu-id="ae7d8-110">Pakiet MyConfiguration.ps1.zip musi być wcześniej przekazany do magazynu Azure Storage przy użyciu polecenia **Publikuj-AzureVMDscConfiguration** i zawiera MyConfiguration.ps1 skryptu i modułów, od których zależy.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-110">The MyConfiguration.ps1.zip package must have been previously uploaded to Azure storage using the **Publish-AzureVMDscConfiguration** command and includes the MyConfiguration.ps1 script and the modules it depends on.</span></span>

<span data-ttu-id="ae7d8-111">Argument moja konfiguracja wskazuje określoną konfigurację DSC w skrypcie do wykonania.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-111">The MyConfiguration argument indicates the specific DSC configuration within the script to execute.</span></span>
<span data-ttu-id="ae7d8-112">Parametr- *ConfigurationArgument* określa tablicę skrótów z argumentami przekazanymi do funkcji konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-112">The - *ConfigurationArgument* parameter specifies a hashtable with the arguments that is passed to the configuration function.</span></span>

### <span data-ttu-id="ae7d8-113">Przykład 2: Konfigurowanie rozszerzenia DSC na maszynie wirtualnej przy użyciu ścieżki do danych konfiguracji</span><span class="sxs-lookup"><span data-stu-id="ae7d8-113">Example 2: Configure the DSC extension on a virtual machine using a path to the configuration data</span></span>
```
PS C:\> $VM | Set-AzureVMDscExtension -ConfigurationArchive MyConfiguration.ps1.zip  -ConfigurationName MyConfiguration -ConfigurationArgument @{ Credential = Get-Credential } -ConfigurationDataPath MyConfigurationData.psd1
DeploymentName              : my-vm-svc
Name                        : my-vm
Label                       :
VM                          : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVM
InstanceStatus              : ReadyRole
IpAddress                   : 10.10.10.10
InstanceStateDetails        :
PowerState                  : Started
InstanceErrorCode           :
InstanceFaultDomain         : 0
InstanceName                : my-vm
InstanceUpgradeDomain       : 0
InstanceSize                : Small
AvailabilitySetName         :
DNSName                     : http://my-vm-svc.cloudapp.net/
Status                      : ReadyRole
GuestAgentStatus            : Microsoft.WindowsAzure.Commands.ServiceManagement.Model.PersistentVMModel.GuestAgentStatus
ResourceExtensionStatusList : {Microsoft.Compute.BGInfo, Microsoft.Powershell.DSC}
PublicIPAddress             :
PublicIPName                :
ServiceName                 : my-vm-svc
OperationDescription        : Get-AzureVM
OperationId                 : a0217a7af900c1f8a212299a3333cdbd7
OperationStatus             : OK
```

<span data-ttu-id="ae7d8-114">To polecenie umożliwia skonfigurowanie rozszerzenia DSC na maszynie wirtualnej przy użyciu ścieżki do danych konfiguracyjnych.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-114">This command configures the DSC extension on a virtual machine using a path to the configuration data.</span></span>

## <span data-ttu-id="ae7d8-115">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ae7d8-115">PARAMETERS</span></span>

### <span data-ttu-id="ae7d8-116">-ConfigurationArchive</span><span class="sxs-lookup"><span data-stu-id="ae7d8-116">-ConfigurationArchive</span></span>
<span data-ttu-id="ae7d8-117">Określa nazwę pakietu konfiguracji (pliku zip), który został wcześniej przekazany za pomocą narzędzia publikowanie-AzureVMDscConfiguration.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-117">Specifies the name of the configuration package (.zip file) that was previously uploaded by Publish-AzureVMDscConfiguration.</span></span>
<span data-ttu-id="ae7d8-118">Ten parametr musi określać tylko nazwę pliku bez ścieżki.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-118">This parameter must specify only the name of the file, without any path.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7d8-119">-ConfigurationArgument</span><span class="sxs-lookup"><span data-stu-id="ae7d8-119">-ConfigurationArgument</span></span>
<span data-ttu-id="ae7d8-120">Określa tablicę skrótów określającą argumenty funkcji konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-120">Specifies a hashtable specifying the arguments to the configuration function.</span></span>
<span data-ttu-id="ae7d8-121">Klucze odpowiadają nazwom parametrów i wartościom parametrów.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-121">The keys correspond to the parameter names and the values to the parameter values.</span></span>

<span data-ttu-id="ae7d8-122">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ae7d8-122">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae7d8-123">typy pierwotne</span><span class="sxs-lookup"><span data-stu-id="ae7d8-123">primitive types</span></span>
- <span data-ttu-id="ae7d8-124">ciąg</span><span class="sxs-lookup"><span data-stu-id="ae7d8-124">string</span></span>
- <span data-ttu-id="ae7d8-125">macierzy</span><span class="sxs-lookup"><span data-stu-id="ae7d8-125">array</span></span>
- <span data-ttu-id="ae7d8-126">PSCredential</span><span class="sxs-lookup"><span data-stu-id="ae7d8-126">PSCredential</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7d8-127">-ConfigurationDataPath</span><span class="sxs-lookup"><span data-stu-id="ae7d8-127">-ConfigurationDataPath</span></span>
<span data-ttu-id="ae7d8-128">Określa ścieżkę pliku psd1, który określa dane funkcji konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-128">Specifies the path of a .psd1 file that specifies the data for the configuration function.</span></span>
<span data-ttu-id="ae7d8-129">Ten plik musi zawierać tablicę Hashtable, jak opisano w oddzieleniu danych dotyczących konfiguracji i środowiska https://msdn.microsoft.com/en-us/PowerShell/DSC/configData .</span><span class="sxs-lookup"><span data-stu-id="ae7d8-129">This file must contain a hashtable as described in Separating Configuration and Environment Datahttps://msdn.microsoft.com/en-us/PowerShell/DSC/configData.</span></span>

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

### <span data-ttu-id="ae7d8-130">-ConfigurationName</span><span class="sxs-lookup"><span data-stu-id="ae7d8-130">-ConfigurationName</span></span>
<span data-ttu-id="ae7d8-131">Określa nazwę skryptu lub modułu konfiguracji wywoływanego przez rozszerzenie DSC.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-131">Specifies the name of the configuration script or module that is invoked by the DSC extension.</span></span>

<span data-ttu-id="ae7d8-132">Wartość tego parametru musi być nazwą jednej z funkcji konfiguracji zawartych w skryptach lub modułach spakowanych w *ConfigurationArchive*.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-132">The value of this parameter must be the name of one of the configuration functions contained in the scripts or modules packaged in *ConfigurationArchive*.</span></span>

<span data-ttu-id="ae7d8-133">To polecenie cmdlet domyślnie określa nazwę pliku podaną przez parametr *ConfigurationArchive* , jeśli pominięto ten parametr, wyłączając wszystkie rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-133">This cmdlet defaults to the name of the file given by the *ConfigurationArchive* parameter if you omit this parameter, excluding any extension.</span></span>
<span data-ttu-id="ae7d8-134">Jeśli na przykład *ConfigurationArchive* jest "SalesWebSite.ps1.zip", wartością domyślną *konfiguracji ConfigurationName* jest "SalesWebSite".</span><span class="sxs-lookup"><span data-stu-id="ae7d8-134">For instance, if *ConfigurationArchive* is "SalesWebSite.ps1.zip", the default value for *ConfigurationName* is "SalesWebSite".</span></span>

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

### <span data-ttu-id="ae7d8-135">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ae7d8-135">-ContainerName</span></span>
<span data-ttu-id="ae7d8-136">Określa nazwę kontenera magazynu platformy Azure, w którym znajduje się *ConfigurationArchive* .</span><span class="sxs-lookup"><span data-stu-id="ae7d8-136">Specifies the name of the Azure storage container where the *ConfigurationArchive* is located.</span></span>

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

### <span data-ttu-id="ae7d8-137">-DataCollection</span><span class="sxs-lookup"><span data-stu-id="ae7d8-137">-DataCollection</span></span>
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

### <span data-ttu-id="ae7d8-138">-Force</span><span class="sxs-lookup"><span data-stu-id="ae7d8-138">-Force</span></span>
<span data-ttu-id="ae7d8-139">Wskazuje, że to polecenie cmdlet zastępuje istniejące obiekty blob.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-139">Indicates that this cmdlet overwrites existing blobs.</span></span>

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

### <span data-ttu-id="ae7d8-140">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="ae7d8-140">-InformationAction</span></span>
<span data-ttu-id="ae7d8-141">Określa, jak to polecenie cmdlet reaguje na zdarzenie informacyjne.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-141">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="ae7d8-142">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ae7d8-142">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae7d8-143">Kontynuacj</span><span class="sxs-lookup"><span data-stu-id="ae7d8-143">Continue</span></span>
- <span data-ttu-id="ae7d8-144">Ignorować</span><span class="sxs-lookup"><span data-stu-id="ae7d8-144">Ignore</span></span>
- <span data-ttu-id="ae7d8-145">Inquire</span><span class="sxs-lookup"><span data-stu-id="ae7d8-145">Inquire</span></span>
- <span data-ttu-id="ae7d8-146">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="ae7d8-146">SilentlyContinue</span></span>
- <span data-ttu-id="ae7d8-147">Przestaw</span><span class="sxs-lookup"><span data-stu-id="ae7d8-147">Stop</span></span>
- <span data-ttu-id="ae7d8-148">Wykonywanie</span><span class="sxs-lookup"><span data-stu-id="ae7d8-148">Suspend</span></span>

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

### <span data-ttu-id="ae7d8-149">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="ae7d8-149">-InformationVariable</span></span>
<span data-ttu-id="ae7d8-150">Określa zmienną informacyjną.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-150">Specifies an information variable.</span></span>

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

### <span data-ttu-id="ae7d8-151">-Profile</span><span class="sxs-lookup"><span data-stu-id="ae7d8-151">-Profile</span></span>
<span data-ttu-id="ae7d8-152">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-152">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ae7d8-153">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-153">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ae7d8-154">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="ae7d8-154">-ReferenceName</span></span>
<span data-ttu-id="ae7d8-155">Określa ciąg zdefiniowany przez użytkownika, za pomocą którego można odwołać się do rozszerzenia.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-155">Specifies a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="ae7d8-156">Ten parametr jest określany po pierwszym dodaniu rozszerzenia do maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-156">This parameter is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="ae7d8-157">W przypadku kolejnych aktualizacji przed aktualizacją rozszerzenia należy określić poprzednio wykorzystaną nazwę odwołania.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-157">For subsequent updates, you should specify the previously used reference name while you update the extension.</span></span>
<span data-ttu-id="ae7d8-158">Element *ReferenceName* przypisany do rozszerzenia jest zwracany przy użyciu polecenia cmdlet **Get-AzureVM** .</span><span class="sxs-lookup"><span data-stu-id="ae7d8-158">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

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

### <span data-ttu-id="ae7d8-159">-StorageContext</span><span class="sxs-lookup"><span data-stu-id="ae7d8-159">-StorageContext</span></span>
<span data-ttu-id="ae7d8-160">Określa kontekst usługi Azure Storage, który zapewnia ustawienia zabezpieczeń używane do uzyskiwania dostępu do skryptu konfiguracji.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-160">Specifies the Azure storage context that provides the security settings used to access the configuration script.</span></span>
<span data-ttu-id="ae7d8-161">Ten kontekst zapewnia dostęp do odczytu kontenera określonego przez parametr *ContainerName* .</span><span class="sxs-lookup"><span data-stu-id="ae7d8-161">This context provides read access to the container specified by the *ContainerName* parameter.</span></span>

```yaml
Type: AzureStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ae7d8-162">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="ae7d8-162">-StorageEndpointSuffix</span></span>
<span data-ttu-id="ae7d8-163">Określa sufiks punktu końcowego DNS dla wszystkich usług magazynowania, na przykład "core.contoso.net".</span><span class="sxs-lookup"><span data-stu-id="ae7d8-163">Specifies the DNS endpoint suffix for all storage services, for instance, "core.contoso.net".</span></span>

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

### <span data-ttu-id="ae7d8-164">-Version</span><span class="sxs-lookup"><span data-stu-id="ae7d8-164">-Version</span></span>
<span data-ttu-id="ae7d8-165">Określa określoną wersję rozszerzenia DSC, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-165">Specifies the specific version of the DSC extension to use.</span></span>
<span data-ttu-id="ae7d8-166">Wartość domyślna jest ustawiona na "1. \*", jeśli ten parametr nie jest określony.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-166">The default value is set to "1.\*" if this parameter is not specified.</span></span>

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

### <span data-ttu-id="ae7d8-167">-VM</span><span class="sxs-lookup"><span data-stu-id="ae7d8-167">-VM</span></span>
<span data-ttu-id="ae7d8-168">Określa trwały obiekt maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-168">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="ae7d8-169">-WmfVersion</span><span class="sxs-lookup"><span data-stu-id="ae7d8-169">-WmfVersion</span></span>
<span data-ttu-id="ae7d8-170">Określa wersję narzędzia Windows Management Framework (WMF) do zainstalowania na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-170">Specifies the version of the Windows Management Framework (WMF) to install on the virtual machine.</span></span>
<span data-ttu-id="ae7d8-171">Rozszerzenie DSC zależy od funkcji DSC, które są dostępne tylko w przypadku aktualizacji WMF.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-171">The DSC Extension depends on DSC features that are only available in the WMF updates.</span></span>
<span data-ttu-id="ae7d8-172">Ten parametr określa wersję aktualizacji do zainstalowania na maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-172">This parameter specifies which version of the update to install on the virtual machine.</span></span>
<span data-ttu-id="ae7d8-173">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="ae7d8-173">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="ae7d8-174">4,0.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-174">4.0.</span></span>
<span data-ttu-id="ae7d8-175">Instaluje program WMF 4,0, chyba że jest już zainstalowana nowsza wersja.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-175">Installs WMF 4.0 unless a newer version is already installed.</span></span>
- <span data-ttu-id="ae7d8-176">5,0.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-176">5.0.</span></span>
<span data-ttu-id="ae7d8-177">Instaluje najnowszą wersję plików WMF 5,0.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-177">Installs the latest release of WMF 5.0.</span></span>
- <span data-ttu-id="ae7d8-178">późniejsza.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-178">latest.</span></span>
<span data-ttu-id="ae7d8-179">Instaluje najnowszą wersję plików WMF, obecnie 5,0.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-179">Installs the latest WMF, currently WMF 5.0.</span></span>

<span data-ttu-id="ae7d8-180">Wartość domyślna to najnowsza.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-180">The default value is latest.</span></span>

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

### <span data-ttu-id="ae7d8-181">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ae7d8-181">-Confirm</span></span>
<span data-ttu-id="ae7d8-182">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-182">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7d8-183">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae7d8-183">-WhatIf</span></span>
<span data-ttu-id="ae7d8-184">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-184">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae7d8-185">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-185">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae7d8-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae7d8-186">CommonParameters</span></span>
<span data-ttu-id="ae7d8-187">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ae7d8-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae7d8-188">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae7d8-188">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae7d8-189">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ae7d8-189">INPUTS</span></span>

## <span data-ttu-id="ae7d8-190">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ae7d8-190">OUTPUTS</span></span>

## <span data-ttu-id="ae7d8-191">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ae7d8-191">NOTES</span></span>

## <span data-ttu-id="ae7d8-192">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ae7d8-192">RELATED LINKS</span></span>

[<span data-ttu-id="ae7d8-193">Get-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ae7d8-193">Get-AzureVMDscExtension</span></span>](./Get-AzureVMDscExtension.md)

[<span data-ttu-id="ae7d8-194">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ae7d8-194">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="ae7d8-195">Remove-AzureVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="ae7d8-195">Remove-AzureVMDscExtension</span></span>](./Remove-AzureVMDscExtension.md)

[<span data-ttu-id="ae7d8-196">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="ae7d8-196">Get-AzureVM</span></span>](./Get-AzureVM.md)

[<span data-ttu-id="ae7d8-197">Publikowanie — AzureVMDscConfiguration</span><span class="sxs-lookup"><span data-stu-id="ae7d8-197">Publish-AzureVMDscConfiguration</span></span>](./Publish-AzureVMDscConfiguration.md)


