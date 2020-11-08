---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: AA7BD103-5C91-4E3B-9E46-2CAEDA5BA615
online version: ''
schema: 2.0.0
ms.openlocfilehash: d8f5643756cfad93399664298378e97264dedc2f
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/08/2020
ms.locfileid: "94061868"
---
# <span data-ttu-id="8ac32-101">New-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8ac32-101">New-WAPackVM</span></span>

## <span data-ttu-id="8ac32-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8ac32-102">SYNOPSIS</span></span>
<span data-ttu-id="8ac32-103">Umożliwia utworzenie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8ac32-103">Creates a virtual machine.</span></span>

## <span data-ttu-id="8ac32-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8ac32-104">SYNTAX</span></span>

### <span data-ttu-id="8ac32-105">CreateVMFromTemplate (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8ac32-105">CreateVMFromTemplate (Default)</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>]
 [-ProductKey <String>] [-Windows] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8ac32-106">CreateLinuxVMFromTemplate</span><span class="sxs-lookup"><span data-stu-id="8ac32-106">CreateLinuxVMFromTemplate</span></span>
```
New-WAPackVM -Name <String> -Template <VMTemplate> -VMCredential <PSCredential> [-VNet <VMNetwork>] [-Linux]
 [-AdministratorSSHKey <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="8ac32-107">CreateVMFromOSDisk</span><span class="sxs-lookup"><span data-stu-id="8ac32-107">CreateVMFromOSDisk</span></span>
```
New-WAPackVM -Name <String> [-VNet <VMNetwork>] -OSDisk <VirtualHardDisk> -VMSizeProfile <HardwareProfile>
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="8ac32-108">Opis</span><span class="sxs-lookup"><span data-stu-id="8ac32-108">DESCRIPTION</span></span>
<span data-ttu-id="8ac32-109">Te tematy są przestarzałe i zostaną usunięte w przyszłości.</span><span class="sxs-lookup"><span data-stu-id="8ac32-109">These topics are deprecated and will be removed in the future.</span></span>
<span data-ttu-id="8ac32-110">W tym temacie opisano polecenie cmdlet w wersji 0.8.1 modułu PowerShell platformy Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="8ac32-110">This topic describes the cmdlet in the 0.8.1 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="8ac32-111">Aby sprawdzić używaną wersję modułu, należy wpisać ją w konsoli programu Azure PowerShell `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="8ac32-111">To find out the version of the module you're using, from the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="8ac32-112">Polecenie cmdlet **New-WAPackVM** umożliwia utworzenie maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8ac32-112">The **New-WAPackVM** cmdlet creates a virtual machine.</span></span>

## <span data-ttu-id="8ac32-113">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8ac32-113">EXAMPLES</span></span>

### <span data-ttu-id="8ac32-114">Przykład 1: Tworzenie maszyny wirtualnej dla systemu operacyjnego Windows przy użyciu szablonu</span><span class="sxs-lookup"><span data-stu-id="8ac32-114">Example 1: Create a virtual machine for the Windows operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate04"PS C:\> New-WAPackVM -Name "ContosoV023" -Template $Template -VMCredential $Credentials -Windows
```

<span data-ttu-id="8ac32-115">Pierwsze polecenie tworzy obiekt **PSCredential** , a następnie zapisuje go w zmiennej $Credentials.</span><span class="sxs-lookup"><span data-stu-id="8ac32-115">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>
<span data-ttu-id="8ac32-116">Polecenie cmdlet monituje o podanie konta i hasła.</span><span class="sxs-lookup"><span data-stu-id="8ac32-116">The cmdlet prompts you for an account and password.</span></span>
<span data-ttu-id="8ac32-117">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="8ac32-117">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="8ac32-118">Drugie polecenie pobiera szablon maszyny wirtualnej o nazwie ContosoTemplate04 przy użyciu polecenia cmdlet **Get-WAPackVMTemplate** , a następnie zapisuje go w zmiennej $Template.</span><span class="sxs-lookup"><span data-stu-id="8ac32-118">The second command gets the virtual machine template named ContosoTemplate04 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="8ac32-119">Polecenie ostatnie powoduje utworzenie maszyny wirtualnej o nazwie ContosoV023 na podstawie szablonu przechowywanego w zmiennej $Template.</span><span class="sxs-lookup"><span data-stu-id="8ac32-119">The final command creates a virtual machine named ContosoV023, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="8ac32-120">W tym poleceniu jest określany parametr *Windows* , a w związku z tym na maszynie wirtualnej musi być uruchomiona wersja systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="8ac32-120">The command specifies the *Windows* parameter, and, therefore, the virtual machine must run a version of the Windows operating system.</span></span>

### <span data-ttu-id="8ac32-121">Przykład 2: Tworzenie maszyny wirtualnej dla systemu operacyjnego Linux przy użyciu szablonu</span><span class="sxs-lookup"><span data-stu-id="8ac32-121">Example 2: Create a virtual machine for the Linux operating system by using a template</span></span>
```
PS C:\> $Credentials = Get-Credential
PS C:\> $Template = Get-WAPackVMTemplate -Name "ContosoTemplate19"
PS C:\> New-WAPackVM -Linux -Name "ContosoV028" -Template $Template -VMCredential $Credentials
```

<span data-ttu-id="8ac32-122">Pierwsze polecenie tworzy obiekt **PSCredential** , a następnie zapisuje go w zmiennej $Credentials.</span><span class="sxs-lookup"><span data-stu-id="8ac32-122">The first command creates a **PSCredential** object, and then stores it in the $Credentials variable.</span></span>

<span data-ttu-id="8ac32-123">Drugie polecenie pobiera szablon maszyny wirtualnej o nazwie ContosoTemplate19 przy użyciu polecenia cmdlet **Get-WAPackVMTemplate** , a następnie zapisuje go w zmiennej $Template.</span><span class="sxs-lookup"><span data-stu-id="8ac32-123">The second command gets the virtual machine template named ContosoTemplate19 by using the **Get-WAPackVMTemplate** cmdlet, and then stores it in the $Template variable.</span></span>

<span data-ttu-id="8ac32-124">Polecenie ostatnie powoduje utworzenie maszyny wirtualnej o nazwie ContosoV028 na podstawie szablonu przechowywanego w zmiennej $Template.</span><span class="sxs-lookup"><span data-stu-id="8ac32-124">The final command creates a virtual machine named ContosoV028, based on the template stored in the $Template variable.</span></span>
<span data-ttu-id="8ac32-125">W tym poleceniu jest określany parametr *Linux* , a w związku z tym na maszynie wirtualnej musi być uruchomiona wersja systemu operacyjnego Linux.</span><span class="sxs-lookup"><span data-stu-id="8ac32-125">The command specifies the *Linux* parameter, and, therefore, the virtual machine must run a version of the Linux operating system.</span></span>

### <span data-ttu-id="8ac32-126">Przykład 3: Tworzenie maszyny wirtualnej na dysku z systemem operacyjnym i profilu rozmiaru</span><span class="sxs-lookup"><span data-stu-id="8ac32-126">Example 3: Create a virtual machine from an operating system disk and size profile</span></span>
```
PS C:\> $OSDisk = Get-WAPackVMOSDisk -Name "ContosoDiskOS"
PS C:\> $SizeProfile = Get-WAPackVMSizeProfile -Name "MediumSizeVM"
PS C:\> New-WAPackVM -Name "ContosoV073" -OSDisk $OSDisk -VMSizeProfile $SizeProfile
```

<span data-ttu-id="8ac32-127">Pierwsze polecenie uzyskuje dysk z systemem operacyjnym o nazwie ContosoDiskOS przy użyciu polecenia cmdlet **Get-WAPackVMOSDisk** , a następnie zapisuje go w zmiennej $OSDisk.</span><span class="sxs-lookup"><span data-stu-id="8ac32-127">The first command gets an operating system disk named ContosoDiskOS by using the **Get-WAPackVMOSDisk** cmdlet, and then stores it in the $OSDisk variable.</span></span>

<span data-ttu-id="8ac32-128">Drugie polecenie pobiera profil rozmiaru o nazwie MediumSizeVM przy użyciu polecenia cmdlet **Get-WAPackVMSizeProfile** , a następnie zapisuje go w zmiennej $SizeProfile.</span><span class="sxs-lookup"><span data-stu-id="8ac32-128">The second command gets the size profile named MediumSizeVM by using the **Get-WAPackVMSizeProfile** cmdlet, and then stores it in the $SizeProfile variable.</span></span>

<span data-ttu-id="8ac32-129">Polecenie ostatnie powoduje utworzenie maszyny wirtualnej o nazwie ContosoV073 z dysku systemu operacyjnego zapisanego w $OSDisk i profilu rozmiaru przechowywanego w $SizeProfile.</span><span class="sxs-lookup"><span data-stu-id="8ac32-129">The final command creates a virtual machine named ContosoV073 from the operating system disk stored in $OSDisk and the size profile stored in $SizeProfile.</span></span>

## <span data-ttu-id="8ac32-130">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8ac32-130">PARAMETERS</span></span>

### <span data-ttu-id="8ac32-131">-AdministratorSSHKey</span><span class="sxs-lookup"><span data-stu-id="8ac32-131">-AdministratorSSHKey</span></span>
<span data-ttu-id="8ac32-132">Określa klucz Secure Shell (SSH) dla konta administratora.</span><span class="sxs-lookup"><span data-stu-id="8ac32-132">Specifies the Secure Shell (SSH) key for the Administrator account.</span></span>

```yaml
Type: String
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac32-133">-Linux</span><span class="sxs-lookup"><span data-stu-id="8ac32-133">-Linux</span></span>
<span data-ttu-id="8ac32-134">Wskazuje, że polecenie cmdlet umożliwia utworzenie maszyny wirtualnej w celu uruchomienia systemu operacyjnego Linux.</span><span class="sxs-lookup"><span data-stu-id="8ac32-134">Indicates that the cmdlet creates a virtual machine to run the Linux operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac32-135">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="8ac32-135">-Name</span></span>
<span data-ttu-id="8ac32-136">Określa nazwę maszyny wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="8ac32-136">Specifies a name for the virtual machine.</span></span>

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

### <span data-ttu-id="8ac32-137">-OSDisk</span><span class="sxs-lookup"><span data-stu-id="8ac32-137">-OSDisk</span></span>
<span data-ttu-id="8ac32-138">Określa dysk systemu operacyjnego jako obiekt **VirtualHardDisk** .</span><span class="sxs-lookup"><span data-stu-id="8ac32-138">Specifies an operating system disk as a **VirtualHardDisk** object.</span></span>
<span data-ttu-id="8ac32-139">Aby uzyskać dysk z systemem operacyjnym, użyj polecenia cmdlet **Get-WAPackVMOSDisk** .</span><span class="sxs-lookup"><span data-stu-id="8ac32-139">To obtain an operating system disk, use the **Get-WAPackVMOSDisk** cmdlet.</span></span>

```yaml
Type: VirtualHardDisk
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac32-140">-ProductKey</span><span class="sxs-lookup"><span data-stu-id="8ac32-140">-ProductKey</span></span>
<span data-ttu-id="8ac32-141">Określa klucz produktu.</span><span class="sxs-lookup"><span data-stu-id="8ac32-141">Specifies a product key.</span></span>
<span data-ttu-id="8ac32-142">Klucz produktu to 25-cyfrowy numer identyfikujący licencję produktu.</span><span class="sxs-lookup"><span data-stu-id="8ac32-142">The product key is a 25 digit number that identifies the product license.</span></span>
<span data-ttu-id="8ac32-143">Użyj klucza produktu dla systemu operacyjnego, który planujesz zainstalować na maszynie wirtualnej lub hoście.</span><span class="sxs-lookup"><span data-stu-id="8ac32-143">Use a product key for an operating system that you plan to install on a virtual machine or host.</span></span>

```yaml
Type: String
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac32-144">-Profile</span><span class="sxs-lookup"><span data-stu-id="8ac32-144">-Profile</span></span>
<span data-ttu-id="8ac32-145">Określa Profil platformy Azure, na podstawie którego jest odczytywane to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8ac32-145">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="8ac32-146">Jeśli nie podano profilu, to polecenie cmdlet odczytuje lokalny profil domyślny.</span><span class="sxs-lookup"><span data-stu-id="8ac32-146">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="8ac32-147">— Szablon</span><span class="sxs-lookup"><span data-stu-id="8ac32-147">-Template</span></span>
<span data-ttu-id="8ac32-148">Określa szablon.</span><span class="sxs-lookup"><span data-stu-id="8ac32-148">Specifies a template.</span></span>
<span data-ttu-id="8ac32-149">Polecenie cmdlet umożliwia utworzenie maszyny wirtualnej na podstawie określonego szablonu.</span><span class="sxs-lookup"><span data-stu-id="8ac32-149">The cmdlet creates a virtual machine based on the template that you specify.</span></span>
<span data-ttu-id="8ac32-150">Aby uzyskać obiekt szablonu, użyj polecenia cmdlet Get-WAPackVMTemplate.</span><span class="sxs-lookup"><span data-stu-id="8ac32-150">To obtain a template object, use the Get-WAPackVMTemplate cmdlet.</span></span>

```yaml
Type: VMTemplate
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac32-151">-VMCredential</span><span class="sxs-lookup"><span data-stu-id="8ac32-151">-VMCredential</span></span>
<span data-ttu-id="8ac32-152">Określa poświadczenie dla lokalnego konta administratora.</span><span class="sxs-lookup"><span data-stu-id="8ac32-152">Specifies the credential for the local Administrator account.</span></span>
<span data-ttu-id="8ac32-153">Aby uzyskać obiekt **PSCredential** , użyj polecenia cmdlet **Get-Credential** .</span><span class="sxs-lookup"><span data-stu-id="8ac32-153">To obtain a **PSCredential** object, use the **Get-Credential** cmdlet.</span></span>
<span data-ttu-id="8ac32-154">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="8ac32-154">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: PSCredential
Parameter Sets: CreateVMFromTemplate, CreateLinuxVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac32-155">-VMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="8ac32-155">-VMSizeProfile</span></span>
<span data-ttu-id="8ac32-156">Określa profil rozmiaru maszyny wirtualnej jako obiekt **HardwareProfile** .</span><span class="sxs-lookup"><span data-stu-id="8ac32-156">Specifies a size profile for a virtual machine as a **HardwareProfile** object.</span></span>
<span data-ttu-id="8ac32-157">Aby uzyskać profil rozmiaru, użyj polecenia cmdlet **Get-WAPackVMSizeProfile** .</span><span class="sxs-lookup"><span data-stu-id="8ac32-157">To obtain a size profile, use the **Get-WAPackVMSizeProfile** cmdlet.</span></span>

```yaml
Type: HardwareProfile
Parameter Sets: CreateVMFromOSDisk
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac32-158">-VNet</span><span class="sxs-lookup"><span data-stu-id="8ac32-158">-VNet</span></span>
<span data-ttu-id="8ac32-159">Określa sieć wirtualną.</span><span class="sxs-lookup"><span data-stu-id="8ac32-159">Specifies a virtual network.</span></span>
<span data-ttu-id="8ac32-160">Polecenie cmdlet umożliwia połączenie maszyny wirtualnej z określoną siecią wirtualną.</span><span class="sxs-lookup"><span data-stu-id="8ac32-160">The cmdlet connects the virtual machine to the virtual network that you specify.</span></span>
<span data-ttu-id="8ac32-161">Aby uzyskać sieć wirtualną, użyj polecenia cmdlet **Get-WAPackVNet** .</span><span class="sxs-lookup"><span data-stu-id="8ac32-161">To obtain a virtual network, use the **Get-WAPackVNet** cmdlet.</span></span>

```yaml
Type: VMNetwork
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac32-162">-Windows</span><span class="sxs-lookup"><span data-stu-id="8ac32-162">-Windows</span></span>
<span data-ttu-id="8ac32-163">Wskazuje, że polecenie cmdlet umożliwia utworzenie maszyny wirtualnej do uruchamiania systemu operacyjnego Windows.</span><span class="sxs-lookup"><span data-stu-id="8ac32-163">Indicates that the cmdlet creates a virtual machine to run the Windows operating system.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CreateVMFromTemplate
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ac32-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ac32-164">CommonParameters</span></span>
<span data-ttu-id="8ac32-165">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8ac32-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ac32-166">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8ac32-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ac32-167">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8ac32-167">INPUTS</span></span>

## <span data-ttu-id="8ac32-168">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8ac32-168">OUTPUTS</span></span>

## <span data-ttu-id="8ac32-169">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8ac32-169">NOTES</span></span>

## <span data-ttu-id="8ac32-170">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8ac32-170">RELATED LINKS</span></span>

[<span data-ttu-id="8ac32-171">Get-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8ac32-171">Get-WAPackVM</span></span>](./Get-WAPackVM.md)

[<span data-ttu-id="8ac32-172">Remove-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8ac32-172">Remove-WAPackVM</span></span>](./Remove-WAPackVM.md)

[<span data-ttu-id="8ac32-173">Restart-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8ac32-173">Restart-WAPackVM</span></span>](./Restart-WAPackVM.md)

[<span data-ttu-id="8ac32-174">Życiorys — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8ac32-174">Resume-WAPackVM</span></span>](./Resume-WAPackVM.md)

[<span data-ttu-id="8ac32-175">Set-WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8ac32-175">Set-WAPackVM</span></span>](./Set-WAPackVM.md)

[<span data-ttu-id="8ac32-176">Start — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8ac32-176">Start-WAPackVM</span></span>](./Start-WAPackVM.md)

[<span data-ttu-id="8ac32-177">Zatrzymaj — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8ac32-177">Stop-WAPackVM</span></span>](./Stop-WAPackVM.md)

[<span data-ttu-id="8ac32-178">Suspend — WAPackVM</span><span class="sxs-lookup"><span data-stu-id="8ac32-178">Suspend-WAPackVM</span></span>](./Suspend-WAPackVM.md)

[<span data-ttu-id="8ac32-179">Get-WAPackVMSizeProfile</span><span class="sxs-lookup"><span data-stu-id="8ac32-179">Get-WAPackVMSizeProfile</span></span>](./Get-WAPackVMSizeProfile.md)

[<span data-ttu-id="8ac32-180">Get-WAPackVMTemplate</span><span class="sxs-lookup"><span data-stu-id="8ac32-180">Get-WAPackVMTemplate</span></span>](./Get-WAPackVMTemplate.md)

[<span data-ttu-id="8ac32-181">Get-WAPackVMOSDisk</span><span class="sxs-lookup"><span data-stu-id="8ac32-181">Get-WAPackVMOSDisk</span></span>](./Get-WAPackVMOSDisk.md)


