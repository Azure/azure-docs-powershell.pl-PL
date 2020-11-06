---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
ms.openlocfilehash: 0c823dd974fd2d01c7502c4cf45e67769e442526
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544531"
---
# <span data-ttu-id="0f6ee-101">Add-AzureRmVMAdditionalUnattendContent</span><span class="sxs-lookup"><span data-stu-id="0f6ee-101">Add-AzureRmVMAdditionalUnattendContent</span></span>

## <span data-ttu-id="0f6ee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0f6ee-102">SYNOPSIS</span></span>
<span data-ttu-id="0f6ee-103">Dodaje informacje do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-103">Adds information to the unattended Windows Setup answer file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f6ee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0f6ee-104">SYNTAX</span></span>

```
Add-AzureRmVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [<CommonParameters>]
```

## <span data-ttu-id="0f6ee-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0f6ee-105">DESCRIPTION</span></span>
<span data-ttu-id="0f6ee-106">Polecenie cmdlet **Add-AzureRmVMAdditionalUnattendContent** umożliwia dodanie informacji do pliku odpowiedzi instalacji nienadzorowanej systemu Windows.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-106">The **Add-AzureRmVMAdditionalUnattendContent** cmdlet adds information to the unattended Windows Setup answer file.</span></span>
<span data-ttu-id="0f6ee-107">Określ dodatkowe kodowanie Base 64 informacje o formacie XML, które to polecenie cmdlet dodaje do pliku unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-107">Specify additional base 64 encoded .xml formatted information that this cmdlet adds to the unattend.xml file.</span></span>

## <span data-ttu-id="0f6ee-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0f6ee-108">EXAMPLES</span></span>

### <span data-ttu-id="0f6ee-109">Przykład 1: dodawanie zawartości do unattend.xml</span><span class="sxs-lookup"><span data-stu-id="0f6ee-109">Example 1: Add content to unattend.xml</span></span>
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzureRmVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

<span data-ttu-id="0f6ee-110">Pierwsze polecenie pobiera zestaw dostępności o nazwie AvailablitySet03 w grupie zasobów o nazwie ResourceGroup11, a następnie zapisuje ten obiekt w zmiennej $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-110">The first command gets the availability set named AvailablitySet03 in the resource group named ResourceGroup11, and then stores that object in the $AvailabilitySet variable.</span></span>

<span data-ttu-id="0f6ee-111">Drugie polecenie tworzy obiekt maszyny wirtualnej, a następnie zapisuje go w zmiennej $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-111">The second command creates a virtual machine object, and then stores it in the $VirtualMachine variable.</span></span>
<span data-ttu-id="0f6ee-112">Polecenie przypisuje nazwę i rozmiar maszynie wirtualnej.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-112">The command assigns a name and size to the virtual machine.</span></span>
<span data-ttu-id="0f6ee-113">Maszyna wirtualna należy do zestawu dostępności przechowywanego w $AvailabilitySet.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-113">The virtual machine belongs to the availability set stored in $AvailabilitySet.</span></span>

<span data-ttu-id="0f6ee-114">Trzecie polecenie tworzy obiekt Credential, korzystając z polecenia cmdlet Get-Credential, a następnie zapisuje wynik w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-114">The third command creates a credential object by using the Get-Credential cmdlet, and then stores the result in the $Credential variable.</span></span>
<span data-ttu-id="0f6ee-115">Polecenie monituje o podanie nazwy użytkownika i hasła.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-115">The command prompts you for a user name and password.</span></span>
<span data-ttu-id="0f6ee-116">Aby uzyskać więcej informacji, wpisz tekst `Get-Help Get-Credential` .</span><span class="sxs-lookup"><span data-stu-id="0f6ee-116">For more information, type `Get-Help Get-Credential`.</span></span>

<span data-ttu-id="0f6ee-117">W czwartym poleceniu użyto polecenia cmdlet **Set-AzureRmVMOperatingSystem** w celu skonfigurowania maszyny wirtualnej przechowywanej w $VirtualMachine.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-117">The fourth command uses the **Set-AzureRmVMOperatingSystem** cmdlet to configure the virtual machine stored in $VirtualMachine.</span></span>

<span data-ttu-id="0f6ee-118">W piątym poleceniu jest przypisywana zawartość zmiennej $AucContent.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-118">The fifth command assigns content to the $AucContent variable.</span></span>
<span data-ttu-id="0f6ee-119">Zawartość zawiera hasło.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-119">The content includes a password.</span></span>

<span data-ttu-id="0f6ee-120">Polecenie ostatnie powoduje dodanie zawartości przechowywanej w $AucContent do pliku unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-120">The final command adds the content stored in $AucContent to the unattend.xml file.</span></span>

## <span data-ttu-id="0f6ee-121">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0f6ee-121">PARAMETERS</span></span>

### <span data-ttu-id="0f6ee-122">-Content (zawartość)</span><span class="sxs-lookup"><span data-stu-id="0f6ee-122">-Content</span></span>
<span data-ttu-id="0f6ee-123">Określa zakodowaną w podstawie 64 zawartość w formacie XML.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-123">Specifies base 64 encoded XML formatted content.</span></span>
<span data-ttu-id="0f6ee-124">To polecenie cmdlet umożliwia dodanie zawartości do pliku unattend.xml.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-124">This cmdlet adds the content to the unattend.xml file.</span></span>
<span data-ttu-id="0f6ee-125">Zawartość XML musi być mniejsza niż 4 KB i musi zawierać element główny ustawienia lub funkcję, które zostaną wstawione przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-125">The XML content must be less than 4 KB and must include the root element for the setting or feature that this cmdlet inserts.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6ee-126">-SettingName</span><span class="sxs-lookup"><span data-stu-id="0f6ee-126">-SettingName</span></span>
<span data-ttu-id="0f6ee-127">Określa nazwę ustawienia, którego dotyczy zawartość.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-127">Specifies the name of the setting to which the content applies.</span></span>
<span data-ttu-id="0f6ee-128">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0f6ee-128">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="0f6ee-129">FirstLogonCommands</span><span class="sxs-lookup"><span data-stu-id="0f6ee-129">FirstLogonCommands</span></span>
- <span data-ttu-id="0f6ee-130">Autologowanie</span><span class="sxs-lookup"><span data-stu-id="0f6ee-130">AutoLogon</span></span>

```yaml
Type: SettingNames
Parameter Sets: (All)
Aliases: 
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6ee-131">-VM</span><span class="sxs-lookup"><span data-stu-id="0f6ee-131">-VM</span></span>
<span data-ttu-id="0f6ee-132">Określa obiekt maszyny wirtualnej, który jest modyfikowany przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-132">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="0f6ee-133">Aby uzyskać obiekt maszyny wirtualnej, użyj polecenia cmdlet [Get-AzureRmVM](./Get-AzureRmVM.md) .</span><span class="sxs-lookup"><span data-stu-id="0f6ee-133">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="0f6ee-134">Utwórz obiekt maszyny wirtualnej za pomocą polecenia cmdlet [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) .</span><span class="sxs-lookup"><span data-stu-id="0f6ee-134">Create a virtual machine object by using the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0f6ee-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f6ee-135">CommonParameters</span></span>
<span data-ttu-id="0f6ee-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f6ee-137">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f6ee-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f6ee-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0f6ee-138">INPUTS</span></span>

### <span data-ttu-id="0f6ee-139">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0f6ee-139">None</span></span>
<span data-ttu-id="0f6ee-140">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="0f6ee-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="0f6ee-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0f6ee-141">OUTPUTS</span></span>

## <span data-ttu-id="0f6ee-142">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0f6ee-142">NOTES</span></span>

## <span data-ttu-id="0f6ee-143">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0f6ee-143">RELATED LINKS</span></span>

[<span data-ttu-id="0f6ee-144">Get-AzureRmAvailabilitySet</span><span class="sxs-lookup"><span data-stu-id="0f6ee-144">Get-AzureRmAvailabilitySet</span></span>](./Get-AzureRmAvailabilitySet.md)

[<span data-ttu-id="0f6ee-145">Set-AzureRmVMOperatingSystem</span><span class="sxs-lookup"><span data-stu-id="0f6ee-145">Set-AzureRmVMOperatingSystem</span></span>](./Set-AzureRmVMOperatingSystem.md)

[<span data-ttu-id="0f6ee-146">Nowe — AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="0f6ee-146">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
